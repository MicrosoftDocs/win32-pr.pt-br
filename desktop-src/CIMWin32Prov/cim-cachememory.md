---
description: A \_ classe CIM CacheMemory define os recursos e o gerenciamento da memória cache.
ms.assetid: cdf35122-2057-45fa-818b-ce542d8e82b0
ms.tgt_platform: multiple
title: Classe CIM_CacheMemory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CacheMemory
- CIM_CacheMemory.Caption
- CIM_CacheMemory.Description
- CIM_CacheMemory.InstallDate
- CIM_CacheMemory.Name
- CIM_CacheMemory.Status
- CIM_CacheMemory.Availability
- CIM_CacheMemory.ConfigManagerErrorCode
- CIM_CacheMemory.ConfigManagerUserConfig
- CIM_CacheMemory.CreationClassName
- CIM_CacheMemory.DeviceID
- CIM_CacheMemory.PowerManagementCapabilities
- CIM_CacheMemory.ErrorCleared
- CIM_CacheMemory.ErrorDescription
- CIM_CacheMemory.LastErrorCode
- CIM_CacheMemory.PNPDeviceID
- CIM_CacheMemory.PowerManagementSupported
- CIM_CacheMemory.StatusInfo
- CIM_CacheMemory.SystemCreationClassName
- CIM_CacheMemory.SystemName
- CIM_CacheMemory.Access
- CIM_CacheMemory.BlockSize
- CIM_CacheMemory.NumberOfBlocks
- CIM_CacheMemory.Purpose
- CIM_CacheMemory.ErrorMethodology
- CIM_CacheMemory.AdditionalErrorData
- CIM_CacheMemory.CorrectableError
- CIM_CacheMemory.EndingAddress
- CIM_CacheMemory.ErrorAccess
- CIM_CacheMemory.ErrorAddress
- CIM_CacheMemory.ErrorData
- CIM_CacheMemory.ErrorDataOrder
- CIM_CacheMemory.ErrorInfo
- CIM_CacheMemory.ErrorResolution
- CIM_CacheMemory.ErrorTime
- CIM_CacheMemory.ErrorTransferSize
- CIM_CacheMemory.OtherErrorDescription
- CIM_CacheMemory.StartingAddress
- CIM_CacheMemory.SystemLevelAddress
- CIM_CacheMemory.Associativity
- CIM_CacheMemory.CacheType
- CIM_CacheMemory.FlushTimer
- CIM_CacheMemory.Level
- CIM_CacheMemory.LineSize
- CIM_CacheMemory.ReadPolicy
- CIM_CacheMemory.ReplacementPolicy
- CIM_CacheMemory.WritePolicy
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0b7a7add96c523dae6b683d597ba36953c605d28
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826511"
---
# <a name="cim_cachememory-class"></a><span data-ttu-id="44c55-103">\_Classe CIM CacheMemory</span><span class="sxs-lookup"><span data-stu-id="44c55-103">CIM\_CacheMemory class</span></span>

<span data-ttu-id="44c55-104">A classe **CIM \_ CacheMemory** define os recursos e o gerenciamento da memória cache.</span><span class="sxs-lookup"><span data-stu-id="44c55-104">The **CIM\_CacheMemory** class defines the capabilities and management of cache memory.</span></span>

<span data-ttu-id="44c55-105">A memória cache é a RAM dedicada ou alocada em que um processador procura dados pela primeira vez.</span><span class="sxs-lookup"><span data-stu-id="44c55-105">Cache memory is the dedicated or allocated RAM where a processor first searches for data.</span></span> <span data-ttu-id="44c55-106">Os dados na memória de cache são entregues rapidamente ao processador e geralmente são descritos por sua proximidade com o processador (por exemplo, cache primário ou secundário).</span><span class="sxs-lookup"><span data-stu-id="44c55-106">Data in cache memory is quickly delivered to the processor and is usually described by its proximity to the processor (for example, primary or secondary cache).</span></span> <span data-ttu-id="44c55-107">Uma unidade de disco que inclui a RAM alocada para manter os dados de leitura ou adjacentes mais recentes do disco (para acelerar a recuperação) também é modelada como memória de cache.</span><span class="sxs-lookup"><span data-stu-id="44c55-107">A disk drive that includes RAM allocated for holding the disk's most recently read or adjacent data (to speed up retrieval) is also modeled as cache memory.</span></span>

> [!Note]  
> <span data-ttu-id="44c55-108">A memória de cache não é um buffer no nível do aplicativo ou do sistema operacional; é a RAM que foi alocada para armazenar em cache os dados do processador.</span><span class="sxs-lookup"><span data-stu-id="44c55-108">Cache memory is not an operating-system or application-level buffer; it is RAM that has been allocated for caching processor data.</span></span>

 

> [!IMPORTANT]
> <span data-ttu-id="44c55-109">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="44c55-109">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="44c55-110">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="44c55-110">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="44c55-111">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="44c55-111">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="44c55-112">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="44c55-112">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="44c55-113">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="44c55-113">Syntax</span></span>

``` syntax
[abstract, UUID("{FAF76B65-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_CacheMemory : CIM_Memory
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
  uint64   NumberOfBlocks;
  string   Purpose;
  string   ErrorMethodology;
  uint8    AdditionalErrorData[];
  boolean  CorrectableError;
  uint64   EndingAddress;
  uint16   ErrorAccess;
  uint64   ErrorAddress;
  uint8    ErrorData[];
  uint16   ErrorDataOrder;
  uint16   ErrorInfo;
  uint64   ErrorResolution;
  datetime ErrorTime;
  uint32   ErrorTransferSize;
  string   OtherErrorDescription;
  uint64   StartingAddress;
  boolean  SystemLevelAddress;
  uint16   Associativity;
  uint16   CacheType;
  uint32   FlushTimer;
  uint16   Level;
  uint32   LineSize;
  uint16   ReadPolicy;
  uint16   ReplacementPolicy;
  uint16   WritePolicy;
};
```

## <a name="members"></a><span data-ttu-id="44c55-114">Membros</span><span class="sxs-lookup"><span data-stu-id="44c55-114">Members</span></span>

<span data-ttu-id="44c55-115">A classe **CIM \_ CacheMemory** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="44c55-115">The **CIM\_CacheMemory** class has these types of members:</span></span>

-   [<span data-ttu-id="44c55-116">Métodos</span><span class="sxs-lookup"><span data-stu-id="44c55-116">Methods</span></span>](#methods)
-   [<span data-ttu-id="44c55-117">Propriedades</span><span class="sxs-lookup"><span data-stu-id="44c55-117">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="44c55-118">Métodos</span><span class="sxs-lookup"><span data-stu-id="44c55-118">Methods</span></span>

<span data-ttu-id="44c55-119">A classe **CIM \_ CacheMemory** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="44c55-119">The **CIM\_CacheMemory** class has these methods.</span></span>



| <span data-ttu-id="44c55-120">Método</span><span class="sxs-lookup"><span data-stu-id="44c55-120">Method</span></span>                                                                 | <span data-ttu-id="44c55-121">Descrição</span><span class="sxs-lookup"><span data-stu-id="44c55-121">Description</span></span>                                                                                                                                |
|:-----------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="44c55-122">**Redefinir**</span><span class="sxs-lookup"><span data-stu-id="44c55-122">**Reset**</span></span>](reset-method-in-class-cim-cachememory.md)                 | <span data-ttu-id="44c55-123">Solicita uma redefinição do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="44c55-123">Requests a reset of the logical device.</span></span> <span data-ttu-id="44c55-124">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="44c55-124">Not implemented by WMI.</span></span><br/>                                                                 |
| [<span data-ttu-id="44c55-125">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="44c55-125">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-cachememory.md) | <span data-ttu-id="44c55-126">Define o estado de energia desejado para um dispositivo lógico e quando o dispositivo deve ser colocado nesse estado.</span><span class="sxs-lookup"><span data-stu-id="44c55-126">Defines the desired power state for a logical device and when the device should be put into that state.</span></span> <span data-ttu-id="44c55-127">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="44c55-127">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="44c55-128">Propriedades</span><span class="sxs-lookup"><span data-stu-id="44c55-128">Properties</span></span>

<span data-ttu-id="44c55-129">A classe **CIM \_ CacheMemory** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="44c55-129">The **CIM\_CacheMemory** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="44c55-130">**Acesso**</span><span class="sxs-lookup"><span data-stu-id="44c55-130">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44c55-131">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="44c55-131">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="44c55-132">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="44c55-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="44c55-133">Descreve as propriedades de leitura/gravação da mídia.</span><span class="sxs-lookup"><span data-stu-id="44c55-133">Describes the read/write properties of the media.</span></span>

<span data-ttu-id="44c55-134">Essa propriedade é herdada do [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="44c55-134">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="44c55-135">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="44c55-135">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>

<span data-ttu-id="44c55-136">**Legível** (1)</span><span class="sxs-lookup"><span data-stu-id="44c55-136">**Readable** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>

<span data-ttu-id="44c55-137">**Gravável** (2)</span><span class="sxs-lookup"><span data-stu-id="44c55-137">**Writeable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>

<span data-ttu-id="44c55-138">**Suporte de leitura/gravação** (3)</span><span class="sxs-lookup"><span data-stu-id="44c55-138">**Read/Write Supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>

<span data-ttu-id="44c55-139">**Gravar uma vez** (4)</span><span class="sxs-lookup"><span data-stu-id="44c55-139">**Write Once** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="44c55-140">**AdditionalErrorData**</span><span class="sxs-lookup"><span data-stu-id="44c55-140">**AdditionalErrorData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44c55-141">Tipo de dados: matriz **uint8**</span><span class="sxs-lookup"><span data-stu-id="44c55-141">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="44c55-142">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="44c55-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="44c55-143">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivo de memória DMTF \| 2,18 "," MIF. \|Matriz de memória física da DMTF \| 1,13 "), [**máx**](/windows/desktop/WmiSdk/standard-qualifiers) . (64)</span><span class="sxs-lookup"><span data-stu-id="44c55-143">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.18", "MIF.DMTF\|Physical Memory Array\|001.13"), [**MAX**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="44c55-144">Matriz de octetos que contém informações de erro adicionais.</span><span class="sxs-lookup"><span data-stu-id="44c55-144">Array of octets that hold additional error information.</span></span> <span data-ttu-id="44c55-145">Um exemplo é a verificação de erros e a síndrome de correção (ECC) ou o retorno dos bits de verificação se uma metodologia de erro baseada em CRC for usada.</span><span class="sxs-lookup"><span data-stu-id="44c55-145">An example is Error Checking and Correcting (ECC) Syndrome, or the return of the check bits if a CRC-based error methodology is used.</span></span> <span data-ttu-id="44c55-146">No último caso, se um erro de bit único for reconhecido e o algoritmo CRC for conhecido, o bit exato que falhou poderá ser determinado.</span><span class="sxs-lookup"><span data-stu-id="44c55-146">In the latter case, if a single-bit error is recognized and the CRC algorithm is known, the exact bit that failed can be determined.</span></span> <span data-ttu-id="44c55-147">Esse tipo de dados (síndrome de ECC, dados de verificação de bits ou de bits de paridade ou outras informações fornecidas pelo fornecedor) está incluído neste campo.</span><span class="sxs-lookup"><span data-stu-id="44c55-147">This type of data (ECC Syndrome, check-bit or parity-bit data, or other vendor supplied information) is included in this field.</span></span> <span data-ttu-id="44c55-148">Se a propriedade **errorInfo** for igual a 3 ("OK"), essa propriedade não terá significado.</span><span class="sxs-lookup"><span data-stu-id="44c55-148">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<span data-ttu-id="44c55-149">Essa propriedade é herdada [**da \_ memória CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="44c55-149">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="44c55-150">**Capacidade de associação**</span><span class="sxs-lookup"><span data-stu-id="44c55-150">**Associativity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44c55-151">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="44c55-151">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="44c55-152">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="44c55-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="44c55-153">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Cache do sistema DMTF \| 3,15 ")</span><span class="sxs-lookup"><span data-stu-id="44c55-153">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Cache\|003.15")</span></span>
</dt> </dl>

<span data-ttu-id="44c55-154">Enumeração que define a associação de cache do sistema.</span><span class="sxs-lookup"><span data-stu-id="44c55-154">Enumeration that defines the system cache associativity.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="44c55-155">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="44c55-155">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="44c55-156">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="44c55-156">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Direct_Mapped"></span><span id="direct_mapped"></span><span id="DIRECT_MAPPED"></span>

<span data-ttu-id="44c55-157">**Mapeado direto** (3)</span><span class="sxs-lookup"><span data-stu-id="44c55-157">**Direct Mapped** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="2-way_Set-Associative"></span><span id="2-way_set-associative"></span><span id="2-WAY_SET-ASSOCIATIVE"></span>

<span data-ttu-id="44c55-158">**conjunto de 2 vias-associativo** (4)</span><span class="sxs-lookup"><span data-stu-id="44c55-158">**2-way Set-Associative** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="4-way_Set-Associative"></span><span id="4-way_set-associative"></span><span id="4-WAY_SET-ASSOCIATIVE"></span>

<span data-ttu-id="44c55-159">**conjunto de 4 vias-associativo** (5)</span><span class="sxs-lookup"><span data-stu-id="44c55-159">**4-way Set-Associative** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Fully_Associative"></span><span id="fully_associative"></span><span id="FULLY_ASSOCIATIVE"></span>

<span data-ttu-id="44c55-160">**Totalmente associativo** (6)</span><span class="sxs-lookup"><span data-stu-id="44c55-160">**Fully Associative** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="8-way_Set-Associative"></span><span id="8-way_set-associative"></span><span id="8-WAY_SET-ASSOCIATIVE"></span>

<span data-ttu-id="44c55-161">**conjunto de 8 vias – associativo** (7)</span><span class="sxs-lookup"><span data-stu-id="44c55-161">**8-way Set-Associative** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="16-way_Set-Associative"></span><span id="16-way_set-associative"></span><span id="16-WAY_SET-ASSOCIATIVE"></span>

<span data-ttu-id="44c55-162">**conjunto de 16 vias – associativo** (8)</span><span class="sxs-lookup"><span data-stu-id="44c55-162">**16-way Set-Associative** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="44c55-163">**Disponibilidade**</span><span class="sxs-lookup"><span data-stu-id="44c55-163">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44c55-164">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="44c55-164">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="44c55-165">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="44c55-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="44c55-166">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operacional da DMTF \| 3,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="44c55-166">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="44c55-167">Disponibilidade e status do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="44c55-167">Availability and status of the device.</span></span>

<span data-ttu-id="44c55-168">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="44c55-168">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="44c55-169"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="44c55-169"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="44c55-170"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="44c55-170"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="44c55-171"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Execução/energia completa** (3)</span><span class="sxs-lookup"><span data-stu-id="44c55-171"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="44c55-172"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Aviso** (4)</span><span class="sxs-lookup"><span data-stu-id="44c55-172"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="44c55-173"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Em teste** (5)</span><span class="sxs-lookup"><span data-stu-id="44c55-173"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="44c55-174"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Não aplicável** (6)</span><span class="sxs-lookup"><span data-stu-id="44c55-174"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="44c55-175"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desligar (7** )</span><span class="sxs-lookup"><span data-stu-id="44c55-175"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="44c55-176"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off line** (8)</span><span class="sxs-lookup"><span data-stu-id="44c55-176"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="44c55-177"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fora do imposto** (9)</span><span class="sxs-lookup"><span data-stu-id="44c55-177"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="44c55-178"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="44c55-178"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="44c55-179"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Não instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="44c55-179"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="44c55-180"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Erro de instalação** (12)</span><span class="sxs-lookup"><span data-stu-id="44c55-180"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="44c55-181"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Economia **de energia-desconhecido** (13)</span><span class="sxs-lookup"><span data-stu-id="44c55-181"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="44c55-182">O dispositivo é conhecido por estar em um modo de economia de energia, mas seu status exato é desconhecido.</span><span class="sxs-lookup"><span data-stu-id="44c55-182">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="44c55-183"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Economia **de energia-modo de baixa energia** (14)</span><span class="sxs-lookup"><span data-stu-id="44c55-183"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="44c55-184">O dispositivo está em um estado de economia de energia, mas ainda está funcionando e pode exibir o desempenho degradado.</span><span class="sxs-lookup"><span data-stu-id="44c55-184">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="44c55-185"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save-em espera** (15)</span><span class="sxs-lookup"><span data-stu-id="44c55-185"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="44c55-186">O dispositivo não está funcionando, mas pode ser levado a uma potência completa rapidamente.</span><span class="sxs-lookup"><span data-stu-id="44c55-186">The device is not functioning but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="44c55-187"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energia** (16)</span><span class="sxs-lookup"><span data-stu-id="44c55-187"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="44c55-188"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Economia **de energia-aviso** (17)</span><span class="sxs-lookup"><span data-stu-id="44c55-188"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="44c55-189">O dispositivo está em um estado de aviso, embora também esteja em um modo de economia de energia.</span><span class="sxs-lookup"><span data-stu-id="44c55-189">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="44c55-190"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>Em **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="44c55-190"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="44c55-191">O dispositivo está em pausa.</span><span class="sxs-lookup"><span data-stu-id="44c55-191">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="44c55-192"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Não pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="44c55-192"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="44c55-193">O dispositivo não está pronto.</span><span class="sxs-lookup"><span data-stu-id="44c55-193">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="44c55-194"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Não configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="44c55-194"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="44c55-195">O dispositivo não está configurado.</span><span class="sxs-lookup"><span data-stu-id="44c55-195">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="44c55-196"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Desativado** (21)</span><span class="sxs-lookup"><span data-stu-id="44c55-196"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="44c55-197">O dispositivo está silencioso.</span><span class="sxs-lookup"><span data-stu-id="44c55-197">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="44c55-198">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="44c55-198">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44c55-199">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="44c55-199">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="44c55-200">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="44c55-200">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="44c55-201">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| host-REsources-MIB. hrStorageAllocationUnits "), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ")</span><span class="sxs-lookup"><span data-stu-id="44c55-201">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageAllocationUnits"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="44c55-202">Tamanho, em bytes, dos blocos que formam a extensão de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="44c55-202">Size, in bytes, of the blocks that form the storage extent.</span></span> <span data-ttu-id="44c55-203">Se o tamanho do bloco variável, o tamanho máximo do bloco, em bytes, deverá ser especificado.</span><span class="sxs-lookup"><span data-stu-id="44c55-203">If variable block size, then the maximum block size, in bytes, should be specified.</span></span> <span data-ttu-id="44c55-204">Se o tamanho do bloco for desconhecido ou se um conceito de bloco não for válido (por exemplo, para extensões de agregação, memória ou discos lógicos), insira um 1 (um).</span><span class="sxs-lookup"><span data-stu-id="44c55-204">If the block size is unknown, or if a block concept is not valid (for example, for aggregate extents, memory, or logical disks), enter a 1 (one).</span></span>

<span data-ttu-id="44c55-205">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="44c55-205">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="44c55-206">Essa propriedade é herdada do [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="44c55-206">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="44c55-207">**CacheType**</span><span class="sxs-lookup"><span data-stu-id="44c55-207">**CacheType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44c55-208">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="44c55-208">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="44c55-209">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="44c55-209">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="44c55-210">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Cache do sistema DMTF \| 3,9 ")</span><span class="sxs-lookup"><span data-stu-id="44c55-210">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Cache\|003.9")</span></span>
</dt> </dl>

<span data-ttu-id="44c55-211">Especifica o cache de instruções, o cache de dados ou ambos.</span><span class="sxs-lookup"><span data-stu-id="44c55-211">Specifies instruction caching, data caching, or both.</span></span> <span data-ttu-id="44c55-212">"Other" e "Unknown" também podem ser definidos.</span><span class="sxs-lookup"><span data-stu-id="44c55-212">"Other" and "Unknown" also can be defined.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="44c55-213">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="44c55-213">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="44c55-214">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="44c55-214">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Instruction"></span><span id="instruction"></span><span id="INSTRUCTION"></span>

<span data-ttu-id="44c55-215">**Instrução** (3)</span><span class="sxs-lookup"><span data-stu-id="44c55-215">**Instruction** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Data"></span><span id="data"></span><span id="DATA"></span>

<span data-ttu-id="44c55-216">**Dados** (4)</span><span class="sxs-lookup"><span data-stu-id="44c55-216">**Data** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Unified"></span><span id="unified"></span><span id="UNIFIED"></span>

<span data-ttu-id="44c55-217">**Unificado** (5)</span><span class="sxs-lookup"><span data-stu-id="44c55-217">**Unified** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="44c55-218">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="44c55-218">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44c55-219">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="44c55-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="44c55-220">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="44c55-220">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="44c55-221">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="44c55-221">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="44c55-222">Uma breve descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="44c55-222">A short textual description of the object.</span></span>

<span data-ttu-id="44c55-223">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="44c55-223">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="44c55-224">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="44c55-224">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44c55-225">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="44c55-225">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="44c55-226">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="44c55-226">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="44c55-227">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="44c55-227">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="44c55-228">Código de erro do Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="44c55-228">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="44c55-229">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="44c55-229">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="44c55-230">**Este dispositivo está funcionando corretamente.**</span><span class="sxs-lookup"><span data-stu-id="44c55-230">**This device is working properly.**</span></span> <span data-ttu-id="44c55-231"> acima (0)</span><span class="sxs-lookup"><span data-stu-id="44c55-231">(0)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="44c55-232">**Este dispositivo não está configurado corretamente.**</span><span class="sxs-lookup"><span data-stu-id="44c55-232">**This device is not configured correctly.**</span></span> <span data-ttu-id="44c55-233">(1)</span><span class="sxs-lookup"><span data-stu-id="44c55-233">(1)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="44c55-234">**O Windows não pode carregar o driver para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="44c55-234">**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="44c55-235">(2)</span><span class="sxs-lookup"><span data-stu-id="44c55-235">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="44c55-236">**O driver para este dispositivo pode estar corrompido ou o sistema pode estar com pouca memória ou outros recursos.**</span><span class="sxs-lookup"><span data-stu-id="44c55-236">**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="44c55-237">(3)</span><span class="sxs-lookup"><span data-stu-id="44c55-237">(3)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="44c55-238">**Este dispositivo não está funcionando corretamente. Um de seus drivers ou seu registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="44c55-238">**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="44c55-239">(4)</span><span class="sxs-lookup"><span data-stu-id="44c55-239">(4)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="44c55-240">**O driver para este dispositivo precisa de um recurso que o Windows não possa gerenciar.**</span><span class="sxs-lookup"><span data-stu-id="44c55-240">**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="44c55-241">(5)</span><span class="sxs-lookup"><span data-stu-id="44c55-241">(5)</span></span>


</dt> <dd></dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="44c55-242">**A configuração de inicialização para este dispositivo está em conflito com outros dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="44c55-242">**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="44c55-243"> (6)</span><span class="sxs-lookup"><span data-stu-id="44c55-243">(6)</span></span>


</dt> <dd></dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="44c55-244">**Não é possível filtrar.**</span><span class="sxs-lookup"><span data-stu-id="44c55-244">**Cannot filter.**</span></span> <span data-ttu-id="44c55-245">(7)</span><span class="sxs-lookup"><span data-stu-id="44c55-245">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="44c55-246">**O carregador de driver para o dispositivo está ausente.**</span><span class="sxs-lookup"><span data-stu-id="44c55-246">**The driver loader for the device is missing.**</span></span> <span data-ttu-id="44c55-247">(8)</span><span class="sxs-lookup"><span data-stu-id="44c55-247">(8)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="44c55-248">**Este dispositivo não está funcionando corretamente porque o firmware de controle está relatando os recursos para o dispositivo incorretamente.**</span><span class="sxs-lookup"><span data-stu-id="44c55-248">**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="44c55-249">(9)</span><span class="sxs-lookup"><span data-stu-id="44c55-249">(9)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="44c55-250">**Este dispositivo não pode ser iniciado.**</span><span class="sxs-lookup"><span data-stu-id="44c55-250">**This device cannot start.**</span></span> <span data-ttu-id="44c55-251">(10)</span><span class="sxs-lookup"><span data-stu-id="44c55-251">(10)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="44c55-252">**Este dispositivo falhou.**</span><span class="sxs-lookup"><span data-stu-id="44c55-252">**This device failed.**</span></span> <span data-ttu-id="44c55-253">(11)</span><span class="sxs-lookup"><span data-stu-id="44c55-253">(11)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="44c55-254">**Este dispositivo não pode encontrar recursos livres suficientes que podem ser usados.**</span><span class="sxs-lookup"><span data-stu-id="44c55-254">**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="44c55-255">12</span><span class="sxs-lookup"><span data-stu-id="44c55-255">(12)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="44c55-256">**O Windows não pode verificar os recursos deste dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="44c55-256">**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="44c55-257">(13)</span><span class="sxs-lookup"><span data-stu-id="44c55-257">(13)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="44c55-258">**Este dispositivo não funcionará corretamente até que você reinicie o computador.**</span><span class="sxs-lookup"><span data-stu-id="44c55-258">**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="44c55-259">(14)</span><span class="sxs-lookup"><span data-stu-id="44c55-259">(14)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="44c55-260">**Este dispositivo não está funcionando corretamente porque provavelmente há um problema de nova enumeração.**</span><span class="sxs-lookup"><span data-stu-id="44c55-260">**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="44c55-261">(15)</span><span class="sxs-lookup"><span data-stu-id="44c55-261">(15)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="44c55-262">**O Windows não pode identificar todos os recursos que este dispositivo usa.**</span><span class="sxs-lookup"><span data-stu-id="44c55-262">**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="44c55-263">(16)</span><span class="sxs-lookup"><span data-stu-id="44c55-263">(16)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="44c55-264">**Este dispositivo está solicitando um tipo de recurso desconhecido.**</span><span class="sxs-lookup"><span data-stu-id="44c55-264">**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="44c55-265">(17)</span><span class="sxs-lookup"><span data-stu-id="44c55-265">(17)</span></span>


</dt> <dd></dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="44c55-266">**Reinstale os drivers para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="44c55-266">**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="44c55-267">(18)</span><span class="sxs-lookup"><span data-stu-id="44c55-267">(18)</span></span>


</dt> <dd></dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="44c55-268">**Falha ao usar o carregador VxD.**</span><span class="sxs-lookup"><span data-stu-id="44c55-268">**Failure using the VxD loader.**</span></span> <span data-ttu-id="44c55-269">(19)</span><span class="sxs-lookup"><span data-stu-id="44c55-269">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="44c55-270">**O registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="44c55-270">**Your registry might be corrupted.**</span></span> <span data-ttu-id="44c55-271">(20)</span><span class="sxs-lookup"><span data-stu-id="44c55-271">(20)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="44c55-272">**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware. O Windows está removendo este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="44c55-272">**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="44c55-273">(21)</span><span class="sxs-lookup"><span data-stu-id="44c55-273">(21)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="44c55-274">**Este dispositivo está desabilitado.**</span><span class="sxs-lookup"><span data-stu-id="44c55-274">**This device is disabled.**</span></span> <span data-ttu-id="44c55-275">(22)</span><span class="sxs-lookup"><span data-stu-id="44c55-275">(22)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="44c55-276">**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware.**</span><span class="sxs-lookup"><span data-stu-id="44c55-276">**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="44c55-277">(23)</span><span class="sxs-lookup"><span data-stu-id="44c55-277">(23)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="44c55-278">**Este dispositivo não está presente, não está funcionando corretamente ou não tem todos os drivers instalados.**</span><span class="sxs-lookup"><span data-stu-id="44c55-278">**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="44c55-279">(24)</span><span class="sxs-lookup"><span data-stu-id="44c55-279">(24)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="44c55-280">**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="44c55-280">**Windows is still setting up this device.**</span></span> <span data-ttu-id="44c55-281">(25)</span><span class="sxs-lookup"><span data-stu-id="44c55-281">(25)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="44c55-282">**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="44c55-282">**Windows is still setting up this device.**</span></span> <span data-ttu-id="44c55-283">(26)</span><span class="sxs-lookup"><span data-stu-id="44c55-283">(26)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="44c55-284">**Este dispositivo não tem uma configuração de log válida.**</span><span class="sxs-lookup"><span data-stu-id="44c55-284">**This device does not have valid log configuration.**</span></span> <span data-ttu-id="44c55-285">(27)</span><span class="sxs-lookup"><span data-stu-id="44c55-285">(27)</span></span>


</dt> <dd></dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="44c55-286">**Os drivers para este dispositivo não estão instalados.**</span><span class="sxs-lookup"><span data-stu-id="44c55-286">**The drivers for this device are not installed.**</span></span> <span data-ttu-id="44c55-287">(28)</span><span class="sxs-lookup"><span data-stu-id="44c55-287">(28)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="44c55-288">**Este dispositivo está desabilitado porque o firmware do dispositivo não forneceu os recursos necessários.**</span><span class="sxs-lookup"><span data-stu-id="44c55-288">**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="44c55-289">(29)</span><span class="sxs-lookup"><span data-stu-id="44c55-289">(29)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="44c55-290">**Este dispositivo está usando um recurso de IRQ (solicitação de interrupção) que outro dispositivo está usando.**</span><span class="sxs-lookup"><span data-stu-id="44c55-290">**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="44c55-291">(30)</span><span class="sxs-lookup"><span data-stu-id="44c55-291">(30)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="44c55-292">**Este dispositivo não está funcionando corretamente porque o Windows não pode carregar os drivers necessários para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="44c55-292">**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="44c55-293">(31)</span><span class="sxs-lookup"><span data-stu-id="44c55-293">(31)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="44c55-294">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="44c55-294">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44c55-295">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="44c55-295">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="44c55-296">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="44c55-296">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="44c55-297">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="44c55-297">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="44c55-298">Se for **true**, o dispositivo estará usando uma configuração definida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="44c55-298">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="44c55-299">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="44c55-299">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="44c55-300">**CorrectableError**</span><span class="sxs-lookup"><span data-stu-id="44c55-300">**CorrectableError**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44c55-301">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="44c55-301">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="44c55-302">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="44c55-302">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="44c55-303">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivo de memória DMTF \| 2,12 "," MIF. \|Matriz de memória física da DMTF \| 1,8 ")</span><span class="sxs-lookup"><span data-stu-id="44c55-303">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.12", "MIF.DMTF\|Physical Memory Array\|001.8")</span></span>
</dt> </dl>

<span data-ttu-id="44c55-304">Se **for true**, o erro mais recente era corrigível.</span><span class="sxs-lookup"><span data-stu-id="44c55-304">If **TRUE**, the most recent error was correctable.</span></span> <span data-ttu-id="44c55-305">Se a propriedade **errorInfo** for igual a 3 ("OK"), essa propriedade não terá significado.</span><span class="sxs-lookup"><span data-stu-id="44c55-305">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<span data-ttu-id="44c55-306">Essa propriedade é herdada [**da \_ memória CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="44c55-306">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="44c55-307">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="44c55-307">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44c55-308">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="44c55-308">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="44c55-309">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="44c55-309">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="44c55-310">Qualificadores: [ **\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="44c55-310">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="44c55-311">Nome da classe ou subclasse usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="44c55-311">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="44c55-312">Quando usado com outras propriedades de chave da classe, essa propriedade permite que todas as instâncias da classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="44c55-312">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="44c55-313">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="44c55-313">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="44c55-314">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="44c55-314">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44c55-315">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="44c55-315">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="44c55-316">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="44c55-316">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="44c55-317">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="44c55-317">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="44c55-318">Uma descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="44c55-318">A textual description of the object.</span></span>

<span data-ttu-id="44c55-319">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="44c55-319">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="44c55-320">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="44c55-320">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44c55-321">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="44c55-321">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="44c55-322">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="44c55-322">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="44c55-323">Qualificadores: [ **\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="44c55-323">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="44c55-324">Endereço ou outras informações de identificação para nomear exclusivamente o dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="44c55-324">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="44c55-325">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="44c55-325">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="44c55-326">**EndingAddress**</span><span class="sxs-lookup"><span data-stu-id="44c55-326">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44c55-327">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="44c55-327">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="44c55-328">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="44c55-328">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="44c55-329">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. Os \| endereços mapeados da matriz de memória DMTF \| 1,4 "," MIF. \|Endereços mapeados do dispositivo \| de memória DMTF 1,5 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" kilobytes ")</span><span class="sxs-lookup"><span data-stu-id="44c55-329">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Array Mapped Addresses\|001.4", "MIF.DMTF\|Memory Device Mapped Addresses\|001.5"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="44c55-330">Endereço final referenciado por um aplicativo ou sistema operacional e mapeado por um controlador de memória para este objeto de memória.</span><span class="sxs-lookup"><span data-stu-id="44c55-330">Ending address referenced by an application or operating system and mapped by a memory controller for this memory object.</span></span> <span data-ttu-id="44c55-331">O endereço final é especificado em kilobytes.</span><span class="sxs-lookup"><span data-stu-id="44c55-331">The ending address is specified in kilobytes.</span></span>

<span data-ttu-id="44c55-332">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="44c55-332">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="44c55-333">Essa propriedade é herdada [**da \_ memória CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="44c55-333">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="44c55-334">**ErrorAccess**</span><span class="sxs-lookup"><span data-stu-id="44c55-334">**ErrorAccess**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44c55-335">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="44c55-335">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="44c55-336">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="44c55-336">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="44c55-337">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivo de memória DMTF \| 2,15 "," MIF. \|Matriz de memória física da DMTF \| 1,10 ")</span><span class="sxs-lookup"><span data-stu-id="44c55-337">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.15", "MIF.DMTF\|Physical Memory Array\|001.10")</span></span>
</dt> </dl>

<span data-ttu-id="44c55-338">Operação de acesso à memória que causou o último erro.</span><span class="sxs-lookup"><span data-stu-id="44c55-338">Memory access operation that caused the last error.</span></span> <span data-ttu-id="44c55-339">O tipo de erro é descrito pela propriedade **errorInfo** .</span><span class="sxs-lookup"><span data-stu-id="44c55-339">The type of error is described by the **ErrorInfo** property.</span></span> <span data-ttu-id="44c55-340">Se a propriedade **errorInfo** for igual a 3 ("OK"), essa propriedade não terá significado.</span><span class="sxs-lookup"><span data-stu-id="44c55-340">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<span data-ttu-id="44c55-341">Essa propriedade é herdada [**da \_ memória CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="44c55-341">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="44c55-342">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="44c55-342">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="44c55-343">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="44c55-343">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Read"></span><span id="read"></span><span id="READ"></span>

<span data-ttu-id="44c55-344">**Leitura** (3)</span><span class="sxs-lookup"><span data-stu-id="44c55-344">**Read** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write"></span><span id="write"></span><span id="WRITE"></span>

<span data-ttu-id="44c55-345">**Gravação** (4)</span><span class="sxs-lookup"><span data-stu-id="44c55-345">**Write** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Partial_Write"></span><span id="partial_write"></span><span id="PARTIAL_WRITE"></span>

<span data-ttu-id="44c55-346">**Gravação parcial** (5)</span><span class="sxs-lookup"><span data-stu-id="44c55-346">**Partial Write** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="44c55-347">**ErrorAddress**</span><span class="sxs-lookup"><span data-stu-id="44c55-347">**ErrorAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44c55-348">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="44c55-348">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="44c55-349">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="44c55-349">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="44c55-350">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivo de memória DMTF \| 2,19 "," MIF. \|Dispositivo de memória DMTF \| 2,20 "," MIF. \|Matriz de memória física da DMTF \| 1,14 ")</span><span class="sxs-lookup"><span data-stu-id="44c55-350">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.19", "MIF.DMTF\|Memory Device\|002.20", "MIF.DMTF\|Physical Memory Array\|001.14")</span></span>
</dt> </dl>

<span data-ttu-id="44c55-351">Endereço do último erro de memória.</span><span class="sxs-lookup"><span data-stu-id="44c55-351">Address of the last memory error.</span></span> <span data-ttu-id="44c55-352">O tipo de erro é descrito pela propriedade **errorInfo** .</span><span class="sxs-lookup"><span data-stu-id="44c55-352">The type of error is described by the **ErrorInfo** property.</span></span> <span data-ttu-id="44c55-353">Se a propriedade **errorInfo** for igual a 3 ("OK"), essa propriedade não terá significado.</span><span class="sxs-lookup"><span data-stu-id="44c55-353">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<span data-ttu-id="44c55-354">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="44c55-354">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="44c55-355">Essa propriedade é herdada [**da \_ memória CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="44c55-355">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="44c55-356">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="44c55-356">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44c55-357">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="44c55-357">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="44c55-358">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="44c55-358">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="44c55-359">Se **for true**, o erro relatado na propriedade **LastErrorCode** será apagado agora.</span><span class="sxs-lookup"><span data-stu-id="44c55-359">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="44c55-360">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="44c55-360">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="44c55-361">**ErrorData**</span><span class="sxs-lookup"><span data-stu-id="44c55-361">**ErrorData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44c55-362">Tipo de dados: matriz **uint8**</span><span class="sxs-lookup"><span data-stu-id="44c55-362">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="44c55-363">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="44c55-363">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="44c55-364">Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivo de memória DMTF \| 2,17 "," MIF. \|Matriz de memória física da DMTF \| 1,12 "), [**máx**](/windows/desktop/WmiSdk/standard-qualifiers) . (64)</span><span class="sxs-lookup"><span data-stu-id="44c55-364">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.17", "MIF.DMTF\|Physical Memory Array\|001.12"), [**MAX**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="44c55-365">Dados capturados durante o último acesso de memória incorreto.</span><span class="sxs-lookup"><span data-stu-id="44c55-365">Data captured during the last erroneous memory access.</span></span> <span data-ttu-id="44c55-366">Os dados ocupam os primeiros *n* octetos da matriz que são necessários para manter o número de bits especificado pela propriedade **ErrorTransferSize** .</span><span class="sxs-lookup"><span data-stu-id="44c55-366">The data occupies the first *n* octets of the array that are necessary to hold the number of bits specified by the **ErrorTransferSize** property.</span></span> <span data-ttu-id="44c55-367">Se **ErrorTransferSize** for 0, essa propriedade não terá significado.</span><span class="sxs-lookup"><span data-stu-id="44c55-367">If **ErrorTransferSize** is 0, then this property has no meaning.</span></span>

<span data-ttu-id="44c55-368">Essa propriedade é herdada [**da \_ memória CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="44c55-368">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="44c55-369">**ErrorDataOrder**</span><span class="sxs-lookup"><span data-stu-id="44c55-369">**ErrorDataOrder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44c55-370">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="44c55-370">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="44c55-371">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="44c55-371">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="44c55-372">Ordem dos dados armazenados na propriedade **ErrorData** .</span><span class="sxs-lookup"><span data-stu-id="44c55-372">Order of data stored in the **ErrorData** property.</span></span> <span data-ttu-id="44c55-373">Se **ErrorTransferSize** for 0, essa propriedade não terá significado.</span><span class="sxs-lookup"><span data-stu-id="44c55-373">If **ErrorTransferSize** is 0, then this property has no meaning.</span></span>

<span data-ttu-id="44c55-374">Essa propriedade é herdada [**da \_ memória CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="44c55-374">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="44c55-375"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="44c55-375"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="44c55-376">Desconhecido.</span><span class="sxs-lookup"><span data-stu-id="44c55-376">Unknown.</span></span>

</dd> <dt>

<span id="Least_Significant_Byte_First"></span><span id="least_significant_byte_first"></span><span id="LEAST_SIGNIFICANT_BYTE_FIRST"></span>

<span data-ttu-id="44c55-377"><span id="Least_Significant_Byte_First"></span><span id="least_significant_byte_first"></span><span id="LEAST_SIGNIFICANT_BYTE_FIRST"></span>**Byte menos significativo primeiro** (1)</span><span class="sxs-lookup"><span data-stu-id="44c55-377"><span id="Least_Significant_Byte_First"></span><span id="least_significant_byte_first"></span><span id="LEAST_SIGNIFICANT_BYTE_FIRST"></span>**Least Significant Byte First** (1)</span></span>


</dt> <dd>

<span data-ttu-id="44c55-378">Byte menos significativo primeiro.</span><span class="sxs-lookup"><span data-stu-id="44c55-378">Least significant byte first.</span></span>

</dd> <dt>

<span id="Most_Significant_Byte_First"></span><span id="most_significant_byte_first"></span><span id="MOST_SIGNIFICANT_BYTE_FIRST"></span>

<span data-ttu-id="44c55-379"><span id="Most_Significant_Byte_First"></span><span id="most_significant_byte_first"></span><span id="MOST_SIGNIFICANT_BYTE_FIRST"></span>**Byte mais significativo primeiro** (2)</span><span class="sxs-lookup"><span data-stu-id="44c55-379"><span id="Most_Significant_Byte_First"></span><span id="most_significant_byte_first"></span><span id="MOST_SIGNIFICANT_BYTE_FIRST"></span>**Most Significant Byte First** (2)</span></span>


</dt> <dd>

<span data-ttu-id="44c55-380">Byte mais significativo primeiro.</span><span class="sxs-lookup"><span data-stu-id="44c55-380">Most significant byte first.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="44c55-381">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="44c55-381">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44c55-382">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="44c55-382">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="44c55-383">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="44c55-383">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="44c55-384">Cadeia de caracteres de forma livre que fornece informações sobre o erro registrado na propriedade **LastErrorCode** e as ações corretivas a serem executadas.</span><span class="sxs-lookup"><span data-stu-id="44c55-384">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="44c55-385">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="44c55-385">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="44c55-386">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="44c55-386">**ErrorInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44c55-387">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="44c55-387">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="44c55-388">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="44c55-388">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="44c55-389">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivo de memória DMTF \| 2,12 "," MIF. \|Matriz de memória física da DMTF \| 1,8 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ memória CIM**](cim-memory.md).**OtherErrorDescription**")</span><span class="sxs-lookup"><span data-stu-id="44c55-389">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.12", "MIF.DMTF\|Physical Memory Array\|001.8"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Memory**](cim-memory.md).**OtherErrorDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="44c55-390">Tipo de erro que ocorreu mais recentemente.</span><span class="sxs-lookup"><span data-stu-id="44c55-390">Type of error that occurred most recently.</span></span> <span data-ttu-id="44c55-391">Os valores de 12 a 14 são indefinidos no esquema CIM porque a DMI combina a semântica do tipo de erro e se ela foi corrigida.</span><span class="sxs-lookup"><span data-stu-id="44c55-391">The values 12 through 14 are undefined in the CIM schema because DMI mixes the semantics of the error type and whether it was correctable.</span></span> <span data-ttu-id="44c55-392">Se um erro é corrigível é indicado na propriedade **CorrectableError** .</span><span class="sxs-lookup"><span data-stu-id="44c55-392">Whether an error is correctable is indicated in the **CorrectableError** property.</span></span>

<span data-ttu-id="44c55-393">Essa propriedade é herdada [**da \_ memória CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="44c55-393">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="44c55-394"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="44c55-394"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="44c55-395">Outros.</span><span class="sxs-lookup"><span data-stu-id="44c55-395">Other.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="44c55-396"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="44c55-396"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd>

<span data-ttu-id="44c55-397">Desconhecido.</span><span class="sxs-lookup"><span data-stu-id="44c55-397">Unknown.</span></span>

</dd> <dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="44c55-398"><span id="OK"></span><span id="ok"></span>**OK** (3)</span><span class="sxs-lookup"><span data-stu-id="44c55-398"><span id="OK"></span><span id="ok"></span>**OK** (3)</span></span>


</dt> <dd>

<span data-ttu-id="44c55-399">OK.</span><span class="sxs-lookup"><span data-stu-id="44c55-399">OK.</span></span>

</dd> <dt>

<span id="Bad_Read"></span><span id="bad_read"></span><span id="BAD_READ"></span>

<span data-ttu-id="44c55-400"><span id="Bad_Read"></span><span id="bad_read"></span><span id="BAD_READ"></span>**Leitura inadequada** (4)</span><span class="sxs-lookup"><span data-stu-id="44c55-400"><span id="Bad_Read"></span><span id="bad_read"></span><span id="BAD_READ"></span>**Bad Read** (4)</span></span>


</dt> <dd>

<span data-ttu-id="44c55-401">Leitura inadequada.</span><span class="sxs-lookup"><span data-stu-id="44c55-401">Bad read.</span></span>

</dd> <dt>

<span id="Parity_Error"></span><span id="parity_error"></span><span id="PARITY_ERROR"></span>

<span data-ttu-id="44c55-402"><span id="Parity_Error"></span><span id="parity_error"></span><span id="PARITY_ERROR"></span>**Erro de paridade** (5)</span><span class="sxs-lookup"><span data-stu-id="44c55-402"><span id="Parity_Error"></span><span id="parity_error"></span><span id="PARITY_ERROR"></span>**Parity Error** (5)</span></span>


</dt> <dd>

<span data-ttu-id="44c55-403">Erro de paridade.</span><span class="sxs-lookup"><span data-stu-id="44c55-403">Parity error.</span></span>

</dd> <dt>

<span id="Single-Bit_Error"></span><span id="single-bit_error"></span><span id="SINGLE-BIT_ERROR"></span>

<span data-ttu-id="44c55-404"><span id="Single-Bit_Error"></span><span id="single-bit_error"></span><span id="SINGLE-BIT_ERROR"></span>**Erro de bit único** (6)</span><span class="sxs-lookup"><span data-stu-id="44c55-404"><span id="Single-Bit_Error"></span><span id="single-bit_error"></span><span id="SINGLE-BIT_ERROR"></span>**Single-Bit Error** (6)</span></span>


</dt> <dd>

<span data-ttu-id="44c55-405">Erro de bit único.</span><span class="sxs-lookup"><span data-stu-id="44c55-405">Single-bit error.</span></span>

</dd> <dt>

<span id="Double-Bit_Error"></span><span id="double-bit_error"></span><span id="DOUBLE-BIT_ERROR"></span>

<span data-ttu-id="44c55-406"><span id="Double-Bit_Error"></span><span id="double-bit_error"></span><span id="DOUBLE-BIT_ERROR"></span>**Erro de bit duplo** (7)</span><span class="sxs-lookup"><span data-stu-id="44c55-406"><span id="Double-Bit_Error"></span><span id="double-bit_error"></span><span id="DOUBLE-BIT_ERROR"></span>**Double-Bit Error** (7)</span></span>


</dt> <dd>

<span data-ttu-id="44c55-407">Erro de bit duplo.</span><span class="sxs-lookup"><span data-stu-id="44c55-407">Double-bit error.</span></span>

</dd> <dt>

<span id="Multi-Bit_Error"></span><span id="multi-bit_error"></span><span id="MULTI-BIT_ERROR"></span>

<span data-ttu-id="44c55-408"><span id="Multi-Bit_Error"></span><span id="multi-bit_error"></span><span id="MULTI-BIT_ERROR"></span>**Erro de vários bits** (8)</span><span class="sxs-lookup"><span data-stu-id="44c55-408"><span id="Multi-Bit_Error"></span><span id="multi-bit_error"></span><span id="MULTI-BIT_ERROR"></span>**Multi-Bit Error** (8)</span></span>


</dt> <dd>

<span data-ttu-id="44c55-409">Erro de vários bits.</span><span class="sxs-lookup"><span data-stu-id="44c55-409">Multi-bit error.</span></span>

</dd> <dt>

<span id="Nibble_Error"></span><span id="nibble_error"></span><span id="NIBBLE_ERROR"></span>

<span data-ttu-id="44c55-410"><span id="Nibble_Error"></span><span id="nibble_error"></span><span id="NIBBLE_ERROR"></span>**Erro de Nibble** (9)</span><span class="sxs-lookup"><span data-stu-id="44c55-410"><span id="Nibble_Error"></span><span id="nibble_error"></span><span id="NIBBLE_ERROR"></span>**Nibble Error** (9)</span></span>


</dt> <dd>

<span data-ttu-id="44c55-411">Erro de Nibble.</span><span class="sxs-lookup"><span data-stu-id="44c55-411">Nibble error.</span></span>

</dd> <dt>

<span id="Checksum_Error"></span><span id="checksum_error"></span><span id="CHECKSUM_ERROR"></span>

<span data-ttu-id="44c55-412"><span id="Checksum_Error"></span><span id="checksum_error"></span><span id="CHECKSUM_ERROR"></span>**Erro de soma de verificação** (10)</span><span class="sxs-lookup"><span data-stu-id="44c55-412"><span id="Checksum_Error"></span><span id="checksum_error"></span><span id="CHECKSUM_ERROR"></span>**Checksum Error** (10)</span></span>


</dt> <dd>

<span data-ttu-id="44c55-413">Erro de soma de verificação.</span><span class="sxs-lookup"><span data-stu-id="44c55-413">Checksum error.</span></span>

</dd> <dt>

<span id="CRC_Error"></span><span id="crc_error"></span><span id="CRC_ERROR"></span>

<span data-ttu-id="44c55-414"><span id="CRC_Error"></span><span id="crc_error"></span><span id="CRC_ERROR"></span>**Erro de CRC** (11)</span><span class="sxs-lookup"><span data-stu-id="44c55-414"><span id="CRC_Error"></span><span id="crc_error"></span><span id="CRC_ERROR"></span>**CRC Error** (11)</span></span>


</dt> <dd>

<span data-ttu-id="44c55-415">Erro de CRC.</span><span class="sxs-lookup"><span data-stu-id="44c55-415">CRC error.</span></span>

</dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="44c55-416"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>**Indefinido** (12)</span><span class="sxs-lookup"><span data-stu-id="44c55-416"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>**Undefined** (12)</span></span>


</dt> <dd>

<span data-ttu-id="44c55-417">Indefinido.</span><span class="sxs-lookup"><span data-stu-id="44c55-417">Undefined.</span></span>

</dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="44c55-418"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>**Indefinido** (13)</span><span class="sxs-lookup"><span data-stu-id="44c55-418"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>**Undefined** (13)</span></span>


</dt> <dd>

<span data-ttu-id="44c55-419">Indefinido.</span><span class="sxs-lookup"><span data-stu-id="44c55-419">Undefined.</span></span>

</dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="44c55-420"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>**Indefinido** (14)</span><span class="sxs-lookup"><span data-stu-id="44c55-420"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>**Undefined** (14)</span></span>


</dt> <dd>

<span data-ttu-id="44c55-421">Indefinido.</span><span class="sxs-lookup"><span data-stu-id="44c55-421">Undefined.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="44c55-422">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="44c55-422">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44c55-423">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="44c55-423">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="44c55-424">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="44c55-424">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="44c55-425">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Matriz de memória física da DMTF \| 1,7 ")</span><span class="sxs-lookup"><span data-stu-id="44c55-425">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Physical Memory Array\|001.7")</span></span>
</dt> </dl>

<span data-ttu-id="44c55-426">Indica se os algoritmos de paridade ou CRC, ECC ou outros mecanismos são usados.</span><span class="sxs-lookup"><span data-stu-id="44c55-426">Indicates whether parity or CRC algorithms, ECC or other mechanisms are used.</span></span> <span data-ttu-id="44c55-427">Também é possível fornecer detalhes sobre o algoritmo.</span><span class="sxs-lookup"><span data-stu-id="44c55-427">Details on the algorithm can also be supplied.</span></span>

<span data-ttu-id="44c55-428">Essa propriedade é herdada [**da \_ memória CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="44c55-428">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="44c55-429">**ErrorResolution**</span><span class="sxs-lookup"><span data-stu-id="44c55-429">**ErrorResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44c55-430">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="44c55-430">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="44c55-431">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="44c55-431">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="44c55-432">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivo de memória DMTF \| 2,21 "," MIF. \|Matriz de memória física da DMTF \| 1,15 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ")</span><span class="sxs-lookup"><span data-stu-id="44c55-432">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.21", "MIF.DMTF\|Physical Memory Array\|001.15"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="44c55-433">Especifica o intervalo, em bytes, para o qual o último erro pode ser resolvido.</span><span class="sxs-lookup"><span data-stu-id="44c55-433">Specifies the range, in bytes, to which the last error can be resolved.</span></span> <span data-ttu-id="44c55-434">Por exemplo, se os endereços de erro forem resolvidos para o bit 11 (ou seja, em uma base de página típica), os erros poderão ser resolvidos para os limites de 4 KB e essa propriedade será definida como 4000.</span><span class="sxs-lookup"><span data-stu-id="44c55-434">For example, if error addresses are resolved to bit 11 (that is, on a typical page basis), then errors can be resolved to 4 KB boundaries and this property is set to 4000.</span></span> <span data-ttu-id="44c55-435">Se a propriedade **errorInfo** for igual a 3 ("OK"), essa propriedade não terá significado.</span><span class="sxs-lookup"><span data-stu-id="44c55-435">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<span data-ttu-id="44c55-436">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="44c55-436">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="44c55-437">Essa propriedade é herdada [**da \_ memória CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="44c55-437">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="44c55-438">**ErrorTime**</span><span class="sxs-lookup"><span data-stu-id="44c55-438">**ErrorTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44c55-439">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="44c55-439">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="44c55-440">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="44c55-440">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="44c55-441">Data e hora em que ocorreu o último erro de memória.</span><span class="sxs-lookup"><span data-stu-id="44c55-441">Date and time that the last memory error occurred.</span></span> <span data-ttu-id="44c55-442">O tipo de erro é descrito pela propriedade **errorInfo** .</span><span class="sxs-lookup"><span data-stu-id="44c55-442">The type of error is described by the **ErrorInfo** property.</span></span> <span data-ttu-id="44c55-443">Se a propriedade **errorInfo** for igual a 3 ("OK"), essa propriedade não terá significado.</span><span class="sxs-lookup"><span data-stu-id="44c55-443">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<span data-ttu-id="44c55-444">Essa propriedade é herdada [**da \_ memória CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="44c55-444">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="44c55-445">**ErrorTransferSize**</span><span class="sxs-lookup"><span data-stu-id="44c55-445">**ErrorTransferSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44c55-446">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="44c55-446">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="44c55-447">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="44c55-447">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="44c55-448">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivo de memória DMTF \| 2,16 "," MIF. \|Matriz de memória física da DMTF \| 1,11 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" bits ")</span><span class="sxs-lookup"><span data-stu-id="44c55-448">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.16", "MIF.DMTF\|Physical Memory Array\|001.11"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="44c55-449">Tamanho da transferência de dados, em bits, que causou o último erro.</span><span class="sxs-lookup"><span data-stu-id="44c55-449">Size of the data transfer, in bits, that caused the last error.</span></span> <span data-ttu-id="44c55-450">Um valor de 0 indica que não há erro.</span><span class="sxs-lookup"><span data-stu-id="44c55-450">A value of 0 indicates no error.</span></span> <span data-ttu-id="44c55-451">Se a propriedade **errorInfo** for igual a 3 ("OK"), essa propriedade deverá ser definida como 0.</span><span class="sxs-lookup"><span data-stu-id="44c55-451">If the **ErrorInfo** property is equal to 3 ("OK"), then this property should be set to 0.</span></span>

<span data-ttu-id="44c55-452">Essa propriedade é herdada [**da \_ memória CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="44c55-452">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="44c55-453">**FlushTimer**</span><span class="sxs-lookup"><span data-stu-id="44c55-453">**FlushTimer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44c55-454">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="44c55-454">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="44c55-455">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="44c55-455">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="44c55-456">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Cache do sistema DMTF \| 3,14 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" segundos ")</span><span class="sxs-lookup"><span data-stu-id="44c55-456">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Cache\|003.14"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("seconds")</span></span>
</dt> </dl>

<span data-ttu-id="44c55-457">Quantidade máxima de tempo, em segundos, que as linhas sujas ou buckets podem permanecer no cache antes de serem liberados.</span><span class="sxs-lookup"><span data-stu-id="44c55-457">Maximum amount of time, in seconds, dirty lines or buckets may remain in the cache before they are flushed.</span></span> <span data-ttu-id="44c55-458">Um valor de 0 indica que uma liberação de cache não é controlada por um timer de liberação.</span><span class="sxs-lookup"><span data-stu-id="44c55-458">A value of 0 indicates that a cache flush is not controlled by a flushing timer.</span></span>

</dd> <dt>

<span data-ttu-id="44c55-459">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="44c55-459">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44c55-460">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="44c55-460">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="44c55-461">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="44c55-461">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="44c55-462">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="44c55-462">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="44c55-463">Indica quando o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="44c55-463">Indicates when the object was installed.</span></span> <span data-ttu-id="44c55-464">A falta de um valor não indica que o objeto não está instalado.</span><span class="sxs-lookup"><span data-stu-id="44c55-464">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="44c55-465">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="44c55-465">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="44c55-466">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="44c55-466">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44c55-467">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="44c55-467">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="44c55-468">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="44c55-468">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="44c55-469">Código do último erro relatado pelo dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="44c55-469">Last error code reported by the logical device.</span></span>

<span data-ttu-id="44c55-470">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="44c55-470">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="44c55-471">**Level**</span><span class="sxs-lookup"><span data-stu-id="44c55-471">**Level**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44c55-472">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="44c55-472">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="44c55-473">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="44c55-473">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="44c55-474">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Cache do sistema DMTF \| 3,2 ")</span><span class="sxs-lookup"><span data-stu-id="44c55-474">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Cache\|003.2")</span></span>
</dt> </dl>

<span data-ttu-id="44c55-475">Especifica se este é o cache primário, secundário ou terciário.</span><span class="sxs-lookup"><span data-stu-id="44c55-475">Specifies whether this is the primary, secondary or tertiary cache.</span></span> <span data-ttu-id="44c55-476">"Outros", "desconhecido" e "não aplicável" também podem ser definidos.</span><span class="sxs-lookup"><span data-stu-id="44c55-476">"Other", "Unknown", and "Not Applicable" also can be defined.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="44c55-477"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="44c55-477"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="44c55-478">Outros.</span><span class="sxs-lookup"><span data-stu-id="44c55-478">Other.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="44c55-479"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="44c55-479"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd>

<span data-ttu-id="44c55-480">Desconhecido.</span><span class="sxs-lookup"><span data-stu-id="44c55-480">Unknown.</span></span>

</dd> <dt>

<span id="Primary"></span><span id="primary"></span><span id="PRIMARY"></span>

<span data-ttu-id="44c55-481"><span id="Primary"></span><span id="primary"></span><span id="PRIMARY"></span>**Primário** (3)</span><span class="sxs-lookup"><span data-stu-id="44c55-481"><span id="Primary"></span><span id="primary"></span><span id="PRIMARY"></span>**Primary** (3)</span></span>


</dt> <dd>

<span data-ttu-id="44c55-482">Primária.</span><span class="sxs-lookup"><span data-stu-id="44c55-482">Primary.</span></span>

</dd> <dt>

<span id="Secondary"></span><span id="secondary"></span><span id="SECONDARY"></span>

<span data-ttu-id="44c55-483"><span id="Secondary"></span><span id="secondary"></span><span id="SECONDARY"></span>**Secundário** (4)</span><span class="sxs-lookup"><span data-stu-id="44c55-483"><span id="Secondary"></span><span id="secondary"></span><span id="SECONDARY"></span>**Secondary** (4)</span></span>


</dt> <dd>

<span data-ttu-id="44c55-484">Secundário.</span><span class="sxs-lookup"><span data-stu-id="44c55-484">Secondary.</span></span>

</dd> <dt>

<span id="Tertiary"></span><span id="tertiary"></span><span id="TERTIARY"></span>

<span data-ttu-id="44c55-485"><span id="Tertiary"></span><span id="tertiary"></span><span id="TERTIARY"></span>**Terciário** (5)</span><span class="sxs-lookup"><span data-stu-id="44c55-485"><span id="Tertiary"></span><span id="tertiary"></span><span id="TERTIARY"></span>**Tertiary** (5)</span></span>


</dt> <dd>

<span data-ttu-id="44c55-486">Terceira.</span><span class="sxs-lookup"><span data-stu-id="44c55-486">Tertiary.</span></span>

</dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="44c55-487"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Não aplicável** (6)</span><span class="sxs-lookup"><span data-stu-id="44c55-487"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd>

<span data-ttu-id="44c55-488">Não aplicável.</span><span class="sxs-lookup"><span data-stu-id="44c55-488">Not applicable.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="44c55-489">**Linhas de**</span><span class="sxs-lookup"><span data-stu-id="44c55-489">**LineSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44c55-490">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="44c55-490">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="44c55-491">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="44c55-491">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="44c55-492">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Cache do sistema DMTF \| 3,10 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ")</span><span class="sxs-lookup"><span data-stu-id="44c55-492">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Cache\|003.10"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="44c55-493">Tamanho, em bytes, de um único Bucket ou linha de cache.</span><span class="sxs-lookup"><span data-stu-id="44c55-493">Size, in bytes, of a single cache bucket or line.</span></span>

</dd> <dt>

<span data-ttu-id="44c55-494">**Nome**</span><span class="sxs-lookup"><span data-stu-id="44c55-494">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44c55-495">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="44c55-495">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="44c55-496">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="44c55-496">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="44c55-497">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="44c55-497">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="44c55-498">Rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="44c55-498">Label by which the object is known.</span></span> <span data-ttu-id="44c55-499">Quando em uma subclasse, essa propriedade pode ser substituída como uma propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="44c55-499">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="44c55-500">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="44c55-500">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="44c55-501">**NumberOfBlocks**</span><span class="sxs-lookup"><span data-stu-id="44c55-501">**NumberOfBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44c55-502">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="44c55-502">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="44c55-503">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="44c55-503">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="44c55-504">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| host-REsources-MIB. hrStorageSize ")</span><span class="sxs-lookup"><span data-stu-id="44c55-504">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageSize")</span></span>
</dt> </dl>

<span data-ttu-id="44c55-505">Número de blocos consecutivos, cada um deles bloqueia o tamanho do valor contido na propriedade **BlockSize** , que formam a extensão de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="44c55-505">Number of consecutive blocks, each block the size of the value contained in the **BlockSize** property, that form the storage extent.</span></span> <span data-ttu-id="44c55-506">O tamanho total da extensão de armazenamento pode ser calculado multiplicando o valor da propriedade **BlockSize** pelo valor dessa propriedade.</span><span class="sxs-lookup"><span data-stu-id="44c55-506">Total size of the storage extent can be calculated by multiplying the value of the **BlockSize** property by the value of this property.</span></span> <span data-ttu-id="44c55-507">Se o valor de **BlockSize** for 1 (um), essa propriedade será o tamanho total da extensão de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="44c55-507">If the value of **BlockSize** is 1 (one), this property is the total size of the storage extent.</span></span>

<span data-ttu-id="44c55-508">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="44c55-508">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="44c55-509">Essa propriedade é herdada do [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="44c55-509">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="44c55-510">**OtherErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="44c55-510">**OtherErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44c55-511">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="44c55-511">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="44c55-512">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="44c55-512">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="44c55-513">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ memória CIM**](cim-memory.md).**ErrorInfo**")</span><span class="sxs-lookup"><span data-stu-id="44c55-513">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Memory**](cim-memory.md).**ErrorInfo**")</span></span>
</dt> </dl>

<span data-ttu-id="44c55-514">Cadeia de caracteres de forma livre que fornece informações se a propriedade **ErrorType** estiver definida como 1 ("other").</span><span class="sxs-lookup"><span data-stu-id="44c55-514">Free form string that provides information if the **ErrorType** property is set to 1 ("Other").</span></span> <span data-ttu-id="44c55-515">Se não estiver definido como 1, essa cadeia de caracteres não terá significado.</span><span class="sxs-lookup"><span data-stu-id="44c55-515">If it is not set to 1, then this string has no meaning.</span></span>

<span data-ttu-id="44c55-516">Essa propriedade é herdada [**da \_ memória CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="44c55-516">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="44c55-517">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="44c55-517">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44c55-518">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="44c55-518">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="44c55-519">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="44c55-519">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="44c55-520">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="44c55-520">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="44c55-521">Indica o identificador do dispositivo de Plug and Play do Win32 do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="44c55-521">Indicates the Win32 Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="44c55-522">Exemplo: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="44c55-522">Example: "\*PNP030b"</span></span>

<span data-ttu-id="44c55-523">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="44c55-523">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="44c55-524">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="44c55-524">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44c55-525">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="44c55-525">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="44c55-526">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="44c55-526">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="44c55-527">Indica os recursos específicos relacionados à energia do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="44c55-527">Indicates the specific power-related capabilities of the logical device.</span></span>

<span data-ttu-id="44c55-528">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="44c55-528">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="44c55-529"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="44c55-529"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="44c55-530">As capacidades relacionadas à energia são desconhecidas.</span><span class="sxs-lookup"><span data-stu-id="44c55-530">The power-related capacities are unknown.</span></span>

</dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="44c55-531"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="44c55-531"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="44c55-532">Não há suporte para capacidades relacionadas a energia para este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="44c55-532">Power-related capacities are not supported for this device.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="44c55-533"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Desabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="44c55-533"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd>

<span data-ttu-id="44c55-534">As capacidades relacionadas à energia foram desabilitadas.</span><span class="sxs-lookup"><span data-stu-id="44c55-534">Power-related capacities have been disabled.</span></span>

</dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="44c55-535"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="44c55-535"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="44c55-536">Os recursos de gerenciamento de energia estão habilitados no momento, mas o conjunto de recursos exato é desconhecido ou as informações não estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="44c55-536">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="44c55-537"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de economia de energia inseridos automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="44c55-537"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="44c55-538">O dispositivo pode alterar seu estado de energia com base no uso ou em outros critérios.</span><span class="sxs-lookup"><span data-stu-id="44c55-538">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="44c55-539"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energia configurável** (5)</span><span class="sxs-lookup"><span data-stu-id="44c55-539"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="44c55-540">Há suporte para o método **SetPowerState** .</span><span class="sxs-lookup"><span data-stu-id="44c55-540">The **SetPowerState** method is supported.</span></span> <span data-ttu-id="44c55-541">Esse método é encontrado na classe pai [**de \_ LogicalDevice CIM**](cim-logicaldevice.md) e pode ser implementado.</span><span class="sxs-lookup"><span data-stu-id="44c55-541">This method is found on the parent [**CIM\_LogicalDevice**](cim-logicaldevice.md) class and can be implemented.</span></span> <span data-ttu-id="44c55-542">Para obter mais informações, consulte [Designing formato MOF (MOF) classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="44c55-542">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="44c55-543"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energia com suporte** (6)</span><span class="sxs-lookup"><span data-stu-id="44c55-543"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="44c55-544">O método **SetPowerState** pode ser invocado com o parâmetro *PowerState* definido como 5 ("ciclo de energia").</span><span class="sxs-lookup"><span data-stu-id="44c55-544">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle").</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="44c55-545"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Energia cronometrada com suporte** (7)</span><span class="sxs-lookup"><span data-stu-id="44c55-545"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="44c55-546">O método **SetPowerState** pode ser invocado com o parâmetro *PowerState* definido como 5 ("ciclo de energia") e o parâmetro de *hora* definido como uma data e hora e um intervalo específicos para o Power-on.</span><span class="sxs-lookup"><span data-stu-id="44c55-546">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle") and the *Time* parameter set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="44c55-547">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="44c55-547">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44c55-548">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="44c55-548">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="44c55-549">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="44c55-549">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="44c55-550">Se for **true**, o dispositivo poderá ser gerenciado por energia, ou seja, colocado em um estado de economia de energia.</span><span class="sxs-lookup"><span data-stu-id="44c55-550">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="44c55-551">Se **for false**, o valor inteiro 1 ("sem suporte") deverá ser a única entrada na matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="44c55-551">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="44c55-552">Essa propriedade não indica se os recursos de gerenciamento de energia estão habilitados no momento ou se estão habilitados, quais recursos têm suporte.</span><span class="sxs-lookup"><span data-stu-id="44c55-552">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="44c55-553">Para obter mais informações, consulte a matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="44c55-553">For more information, see the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="44c55-554">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="44c55-554">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="44c55-555">**Finalidade**</span><span class="sxs-lookup"><span data-stu-id="44c55-555">**Purpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44c55-556">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="44c55-556">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="44c55-557">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="44c55-557">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="44c55-558">Cadeia de caracteres de forma livre que descreve a mídia e seu uso.</span><span class="sxs-lookup"><span data-stu-id="44c55-558">Free form string that describes the media and its use.</span></span>

<span data-ttu-id="44c55-559">Essa propriedade é herdada do [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="44c55-559">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="44c55-560">**As**</span><span class="sxs-lookup"><span data-stu-id="44c55-560">**ReadPolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44c55-561">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="44c55-561">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="44c55-562">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="44c55-562">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="44c55-563">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Cache do sistema DMTF \| 3,13 ")</span><span class="sxs-lookup"><span data-stu-id="44c55-563">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Cache\|003.13")</span></span>
</dt> </dl>

<span data-ttu-id="44c55-564">Política empregada pelo cache para lidar com solicitações de leitura.</span><span class="sxs-lookup"><span data-stu-id="44c55-564">Policy employed by the cache for handling read requests.</span></span> <span data-ttu-id="44c55-565">Se a política de leitura for determinada individualmente, ou seja, para cada solicitação, o valor 6 ("determinação por e/s") deverá ser especificado.</span><span class="sxs-lookup"><span data-stu-id="44c55-565">If the read policy is determined individually, that is, for each request, then the value 6 ("Determination per I/O") should be specified.</span></span> <span data-ttu-id="44c55-566">"Other" e "Unknown" também são valores válidos.</span><span class="sxs-lookup"><span data-stu-id="44c55-566">"Other" and "Unknown" are also valid values.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="44c55-567"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="44c55-567"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="44c55-568">Outros.</span><span class="sxs-lookup"><span data-stu-id="44c55-568">Other.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="44c55-569"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="44c55-569"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd>

<span data-ttu-id="44c55-570">Desconhecido.</span><span class="sxs-lookup"><span data-stu-id="44c55-570">Unknown.</span></span>

</dd> <dt>

<span id="Read"></span><span id="read"></span><span id="READ"></span>

<span data-ttu-id="44c55-571"><span id="Read"></span><span id="read"></span><span id="READ"></span>**Leitura** (3)</span><span class="sxs-lookup"><span data-stu-id="44c55-571"><span id="Read"></span><span id="read"></span><span id="READ"></span>**Read** (3)</span></span>


</dt> <dd>

<span data-ttu-id="44c55-572">Leitura.</span><span class="sxs-lookup"><span data-stu-id="44c55-572">Read.</span></span>

</dd> <dt>

<span id="Read-Ahead"></span><span id="read-ahead"></span><span id="READ-AHEAD"></span>

<span data-ttu-id="44c55-573"><span id="Read-Ahead"></span><span id="read-ahead"></span><span id="READ-AHEAD"></span>**Read-Ahead** (4)</span><span class="sxs-lookup"><span data-stu-id="44c55-573"><span id="Read-Ahead"></span><span id="read-ahead"></span><span id="READ-AHEAD"></span>**Read-Ahead** (4)</span></span>


</dt> <dd>

<span data-ttu-id="44c55-574">Read-Ahead.</span><span class="sxs-lookup"><span data-stu-id="44c55-574">Read-ahead.</span></span>

</dd> <dt>

<span id="Read_and_Read-Ahead"></span><span id="read_and_read-ahead"></span><span id="READ_AND_READ-AHEAD"></span>

<span data-ttu-id="44c55-575"><span id="Read_and_Read-Ahead"></span><span id="read_and_read-ahead"></span><span id="READ_AND_READ-AHEAD"></span>**Leitura e leitura antecipada** (5)</span><span class="sxs-lookup"><span data-stu-id="44c55-575"><span id="Read_and_Read-Ahead"></span><span id="read_and_read-ahead"></span><span id="READ_AND_READ-AHEAD"></span>**Read and Read-Ahead** (5)</span></span>


</dt> <dd>

<span data-ttu-id="44c55-576">Leitura e leitura antecipada.</span><span class="sxs-lookup"><span data-stu-id="44c55-576">Read and read-ahead.</span></span>

</dd> <dt>

<span id="Determination_Per_I_O"></span><span id="determination_per_i_o"></span><span id="DETERMINATION_PER_I_O"></span>

<span data-ttu-id="44c55-577"><span id="Determination_Per_I_O"></span><span id="determination_per_i_o"></span><span id="DETERMINATION_PER_I_O"></span>**Determinação por e/s** (6)</span><span class="sxs-lookup"><span data-stu-id="44c55-577"><span id="Determination_Per_I_O"></span><span id="determination_per_i_o"></span><span id="DETERMINATION_PER_I_O"></span>**Determination Per I/O** (6)</span></span>


</dt> <dd>

<span data-ttu-id="44c55-578">Determinação por e/s.</span><span class="sxs-lookup"><span data-stu-id="44c55-578">Determination per I/O.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="44c55-579">**ReplacementPolicy**</span><span class="sxs-lookup"><span data-stu-id="44c55-579">**ReplacementPolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44c55-580">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="44c55-580">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="44c55-581">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="44c55-581">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="44c55-582">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Cache do sistema DMTF \| 3,12 ")</span><span class="sxs-lookup"><span data-stu-id="44c55-582">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Cache\|003.12")</span></span>
</dt> </dl>

<span data-ttu-id="44c55-583">Enumeração de inteiros que descreve o algoritmo que determina quais linhas de cache ou buckets devem ser reutilizados.</span><span class="sxs-lookup"><span data-stu-id="44c55-583">Integer enumeration describing the algorithm that determines which cache lines or buckets should be re-used.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="44c55-584"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="44c55-584"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="44c55-585">Outros.</span><span class="sxs-lookup"><span data-stu-id="44c55-585">Other.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="44c55-586"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="44c55-586"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd>

<span data-ttu-id="44c55-587">Desconhecido.</span><span class="sxs-lookup"><span data-stu-id="44c55-587">Unknown.</span></span>

</dd> <dt>

<span id="Least_Recently_Used__LRU_"></span><span id="least_recently_used__lru_"></span><span id="LEAST_RECENTLY_USED__LRU_"></span>

<span data-ttu-id="44c55-588"><span id="Least_Recently_Used__LRU_"></span><span id="least_recently_used__lru_"></span><span id="LEAST_RECENTLY_USED__LRU_"></span>**Menos usado recentemente (LRU)** (3)</span><span class="sxs-lookup"><span data-stu-id="44c55-588"><span id="Least_Recently_Used__LRU_"></span><span id="least_recently_used__lru_"></span><span id="LEAST_RECENTLY_USED__LRU_"></span>**Least Recently Used (LRU)** (3)</span></span>


</dt> <dd>

<span data-ttu-id="44c55-589">Menos usados recentemente (LRU).</span><span class="sxs-lookup"><span data-stu-id="44c55-589">Least recently used (LRU).</span></span>

</dd> <dt>

<span id="First_In_First_Out__FIFO_"></span><span id="first_in_first_out__fifo_"></span><span id="FIRST_IN_FIRST_OUT__FIFO_"></span>

<span data-ttu-id="44c55-590"><span id="First_In_First_Out__FIFO_"></span><span id="first_in_first_out__fifo_"></span><span id="FIRST_IN_FIRST_OUT__FIFO_"></span>**Primeiro a entrar, primeiro a sair (FIFO)** (4)</span><span class="sxs-lookup"><span data-stu-id="44c55-590"><span id="First_In_First_Out__FIFO_"></span><span id="first_in_first_out__fifo_"></span><span id="FIRST_IN_FIRST_OUT__FIFO_"></span>**First In First Out (FIFO)** (4)</span></span>


</dt> <dd>

<span data-ttu-id="44c55-591">PEPS (primeiro a entrar, primeiro a sair).</span><span class="sxs-lookup"><span data-stu-id="44c55-591">First-in, first-out (FIFO).</span></span>

</dd> <dt>

<span id="Last_In_First_Out__LIFO_"></span><span id="last_in_first_out__lifo_"></span><span id="LAST_IN_FIRST_OUT__LIFO_"></span>

<span data-ttu-id="44c55-592"><span id="Last_In_First_Out__LIFO_"></span><span id="last_in_first_out__lifo_"></span><span id="LAST_IN_FIRST_OUT__LIFO_"></span>**Último a entrar, primeiro a sair (UEPS)** (5)</span><span class="sxs-lookup"><span data-stu-id="44c55-592"><span id="Last_In_First_Out__LIFO_"></span><span id="last_in_first_out__lifo_"></span><span id="LAST_IN_FIRST_OUT__LIFO_"></span>**Last In First Out (LIFO)** (5)</span></span>


</dt> <dd>

<span data-ttu-id="44c55-593">UEPS (último a entrar, primeiro a sair).</span><span class="sxs-lookup"><span data-stu-id="44c55-593">Last-in, first-out (LIFO).</span></span>

</dd> <dt>

<span id="Least_Frequently_Used__LFU_"></span><span id="least_frequently_used__lfu_"></span><span id="LEAST_FREQUENTLY_USED__LFU_"></span>

<span data-ttu-id="44c55-594"><span id="Least_Frequently_Used__LFU_"></span><span id="least_frequently_used__lfu_"></span><span id="LEAST_FREQUENTLY_USED__LFU_"></span>**Usado com menos frequência (LFU)** (6)</span><span class="sxs-lookup"><span data-stu-id="44c55-594"><span id="Least_Frequently_Used__LFU_"></span><span id="least_frequently_used__lfu_"></span><span id="LEAST_FREQUENTLY_USED__LFU_"></span>**Least Frequently Used (LFU)** (6)</span></span>


</dt> <dd>

<span data-ttu-id="44c55-595">Usado com menos frequência (LFU.)</span><span class="sxs-lookup"><span data-stu-id="44c55-595">Least frequently used (LFU.)</span></span>

</dd> <dt>

<span id="Most_Frequently_Used__MFU_"></span><span id="most_frequently_used__mfu_"></span><span id="MOST_FREQUENTLY_USED__MFU_"></span>

<span data-ttu-id="44c55-596"><span id="Most_Frequently_Used__MFU_"></span><span id="most_frequently_used__mfu_"></span><span id="MOST_FREQUENTLY_USED__MFU_"></span>**Usado com mais frequência (MFU)** (7)</span><span class="sxs-lookup"><span data-stu-id="44c55-596"><span id="Most_Frequently_Used__MFU_"></span><span id="most_frequently_used__mfu_"></span><span id="MOST_FREQUENTLY_USED__MFU_"></span>**Most Frequently Used (MFU)** (7)</span></span>


</dt> <dd>

<span data-ttu-id="44c55-597">MFU (mais frequentemente usado).</span><span class="sxs-lookup"><span data-stu-id="44c55-597">Most frequently used (MFU).</span></span>

</dd> <dt>

<span id="Data_Dependent_Multiple_Algorithms"></span><span id="data_dependent_multiple_algorithms"></span><span id="DATA_DEPENDENT_MULTIPLE_ALGORITHMS"></span>

<span data-ttu-id="44c55-598"><span id="Data_Dependent_Multiple_Algorithms"></span><span id="data_dependent_multiple_algorithms"></span><span id="DATA_DEPENDENT_MULTIPLE_ALGORITHMS"></span>**Algoritmos múltiplos dependentes de dados** (8)</span><span class="sxs-lookup"><span data-stu-id="44c55-598"><span id="Data_Dependent_Multiple_Algorithms"></span><span id="data_dependent_multiple_algorithms"></span><span id="DATA_DEPENDENT_MULTIPLE_ALGORITHMS"></span>**Data Dependent Multiple Algorithms** (8)</span></span>


</dt> <dd>

<span data-ttu-id="44c55-599">Algoritmos múltiplos dependentes de dados.</span><span class="sxs-lookup"><span data-stu-id="44c55-599">Data-dependent multiple algorithms.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="44c55-600">**StartingAddress**</span><span class="sxs-lookup"><span data-stu-id="44c55-600">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44c55-601">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="44c55-601">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="44c55-602">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="44c55-602">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="44c55-603">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. Os \| endereços mapeados da matriz de memória DMTF \| 1,3 "," MIF. \|Endereços mapeados do dispositivo \| de memória DMTF 1,4 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" kilobytes ")</span><span class="sxs-lookup"><span data-stu-id="44c55-603">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Array Mapped Addresses\|001.3", "MIF.DMTF\|Memory Device Mapped Addresses\|001.4"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="44c55-604">Endereço inicial, referenciado por um aplicativo ou sistema operacional e mapeado por um controlador de memória, para esse objeto de memória.</span><span class="sxs-lookup"><span data-stu-id="44c55-604">Beginning address, referenced by an application or operating system and mapped by a memory controller, for this memory object.</span></span> <span data-ttu-id="44c55-605">O endereço inicial é especificado em kilobytes.</span><span class="sxs-lookup"><span data-stu-id="44c55-605">The starting address is specified in kilobytes.</span></span>

<span data-ttu-id="44c55-606">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="44c55-606">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="44c55-607">Essa propriedade é herdada [**da \_ memória CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="44c55-607">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="44c55-608">**Status**</span><span class="sxs-lookup"><span data-stu-id="44c55-608">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44c55-609">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="44c55-609">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="44c55-610">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="44c55-610">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="44c55-611">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="44c55-611">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="44c55-612">Cadeia de caracteres que indica o status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="44c55-612">String that indicates the current status of the object.</span></span> <span data-ttu-id="44c55-613">O status operacional e não operacional pode ser definido.</span><span class="sxs-lookup"><span data-stu-id="44c55-613">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="44c55-614">O status operacional pode incluir "OK", "degradado" e "Pred falha".</span><span class="sxs-lookup"><span data-stu-id="44c55-614">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="44c55-615">"Pred Fail" indica que um elemento está funcionando corretamente, mas está prevendo uma falha (por exemplo, uma unidade de disco rígido habilitada para inteligente).</span><span class="sxs-lookup"><span data-stu-id="44c55-615">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="44c55-616">O status não operacional pode incluir "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="44c55-616">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="44c55-617">O "serviço" pode ser aplicado durante o espelhamento de disco – reprateando, recarregando uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="44c55-617">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="44c55-618">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="44c55-618">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="44c55-619">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="44c55-619">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="44c55-620">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="44c55-620">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="44c55-621">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="44c55-621">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="44c55-622">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="44c55-622">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="44c55-623">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="44c55-623">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="44c55-624">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="44c55-624">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="44c55-625">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="44c55-625">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="44c55-626">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="44c55-626">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="44c55-627">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="44c55-627">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="44c55-628">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="44c55-628">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="44c55-629">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="44c55-629">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="44c55-630">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="44c55-630">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="44c55-631">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="44c55-631">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="44c55-632">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="44c55-632">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="44c55-633">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="44c55-633">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44c55-634">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="44c55-634">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="44c55-635">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="44c55-635">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="44c55-636">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operacional da DMTF \| 3,3 ")</span><span class="sxs-lookup"><span data-stu-id="44c55-636">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="44c55-637">Estado do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="44c55-637">State of the logical device.</span></span> <span data-ttu-id="44c55-638">Se essa propriedade não se aplicar ao dispositivo lógico, o valor 5 ("não aplicável") deverá ser usado.</span><span class="sxs-lookup"><span data-stu-id="44c55-638">If this property does not apply to the logical device, the value 5 ("Not Applicable") should be used.</span></span>

<span data-ttu-id="44c55-639">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="44c55-639">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="44c55-640">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="44c55-640">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="44c55-641">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="44c55-641">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="44c55-642">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="44c55-642">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="44c55-643">**Desabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="44c55-643">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="44c55-644">**Não aplicável** (5)</span><span class="sxs-lookup"><span data-stu-id="44c55-644">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="44c55-645">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="44c55-645">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44c55-646">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="44c55-646">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="44c55-647">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="44c55-647">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="44c55-648">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="44c55-648">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="44c55-649">O nome da classe de criação do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="44c55-649">The scoping system's creation class name.</span></span>

<span data-ttu-id="44c55-650">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="44c55-650">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="44c55-651">**SystemLevelAddress**</span><span class="sxs-lookup"><span data-stu-id="44c55-651">**SystemLevelAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44c55-652">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="44c55-652">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="44c55-653">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="44c55-653">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="44c55-654">Indica se as informações de endereço na propriedade **ErrorAddress** são um endereço de nível de sistema (**true**) ou um endereço físico (**false**).</span><span class="sxs-lookup"><span data-stu-id="44c55-654">Indicates whether the address information in the **ErrorAddress** property is a system-level address (**TRUE**) or a physical address (**FALSE**).</span></span> <span data-ttu-id="44c55-655">Se a propriedade **errorInfo** for igual a 3 ("OK"), essa propriedade não terá significado.</span><span class="sxs-lookup"><span data-stu-id="44c55-655">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<span data-ttu-id="44c55-656">Essa propriedade é herdada [**da \_ memória CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="44c55-656">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="44c55-657">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="44c55-657">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44c55-658">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="44c55-658">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="44c55-659">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="44c55-659">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="44c55-660">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**Name**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="44c55-660">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="44c55-661">O nome do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="44c55-661">The scoping system's name.</span></span>

<span data-ttu-id="44c55-662">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="44c55-662">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="44c55-663">**WritePolicy**</span><span class="sxs-lookup"><span data-stu-id="44c55-663">**WritePolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44c55-664">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="44c55-664">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="44c55-665">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="44c55-665">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="44c55-666">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Cache do sistema DMTF \| 3,5 ")</span><span class="sxs-lookup"><span data-stu-id="44c55-666">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Cache\|003.5")</span></span>
</dt> </dl>

<span data-ttu-id="44c55-667">Define se o cache é Write-back ou write-through, ou se as informações "variam de acordo com o endereço" ou são definidas individualmente para cada entrada/saída.</span><span class="sxs-lookup"><span data-stu-id="44c55-667">Defines whether the cache is write-back or write-through, or whether the information "Varies with Address" or is defined individually for each input/output.</span></span> <span data-ttu-id="44c55-668">"Other" e "Unknown" também podem ser especificados.</span><span class="sxs-lookup"><span data-stu-id="44c55-668">"Other" and "Unknown" also can be specified.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="44c55-669"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="44c55-669"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="44c55-670">Outros.</span><span class="sxs-lookup"><span data-stu-id="44c55-670">Other.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="44c55-671"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="44c55-671"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd>

<span data-ttu-id="44c55-672">Desconhecido.</span><span class="sxs-lookup"><span data-stu-id="44c55-672">Unknown.</span></span>

</dd> <dt>

<span id="Write_Back"></span><span id="write_back"></span><span id="WRITE_BACK"></span>

<span data-ttu-id="44c55-673"><span id="Write_Back"></span><span id="write_back"></span><span id="WRITE_BACK"></span>**Write-back** (3)</span><span class="sxs-lookup"><span data-stu-id="44c55-673"><span id="Write_Back"></span><span id="write_back"></span><span id="WRITE_BACK"></span>**Write Back** (3)</span></span>


</dt> <dd>

<span data-ttu-id="44c55-674">Write-back.</span><span class="sxs-lookup"><span data-stu-id="44c55-674">Write back.</span></span>

</dd> <dt>

<span id="Write_Through"></span><span id="write_through"></span><span id="WRITE_THROUGH"></span>

<span data-ttu-id="44c55-675"><span id="Write_Through"></span><span id="write_through"></span><span id="WRITE_THROUGH"></span>**Gravação por** (4)</span><span class="sxs-lookup"><span data-stu-id="44c55-675"><span id="Write_Through"></span><span id="write_through"></span><span id="WRITE_THROUGH"></span>**Write Through** (4)</span></span>


</dt> <dd>

<span data-ttu-id="44c55-676">Gravação.</span><span class="sxs-lookup"><span data-stu-id="44c55-676">Write through.</span></span>

</dd> <dt>

<span id="Varies_with_Address"></span><span id="varies_with_address"></span><span id="VARIES_WITH_ADDRESS"></span>

<span data-ttu-id="44c55-677"><span id="Varies_with_Address"></span><span id="varies_with_address"></span><span id="VARIES_WITH_ADDRESS"></span>**Varia de acordo com o endereço** (5)</span><span class="sxs-lookup"><span data-stu-id="44c55-677"><span id="Varies_with_Address"></span><span id="varies_with_address"></span><span id="VARIES_WITH_ADDRESS"></span>**Varies with Address** (5)</span></span>


</dt> <dd>

<span data-ttu-id="44c55-678">Varia de acordo com o endereço.</span><span class="sxs-lookup"><span data-stu-id="44c55-678">Varies with address.</span></span>

</dd> <dt>

<span id="Determination_Per_I_O"></span><span id="determination_per_i_o"></span><span id="DETERMINATION_PER_I_O"></span>

<span data-ttu-id="44c55-679"><span id="Determination_Per_I_O"></span><span id="determination_per_i_o"></span><span id="DETERMINATION_PER_I_O"></span>**Determinação por e/s** (6)</span><span class="sxs-lookup"><span data-stu-id="44c55-679"><span id="Determination_Per_I_O"></span><span id="determination_per_i_o"></span><span id="DETERMINATION_PER_I_O"></span>**Determination Per I/O** (6)</span></span>


</dt> <dd>

<span data-ttu-id="44c55-680">Determinação por e/s.</span><span class="sxs-lookup"><span data-stu-id="44c55-680">Determination per I/O.</span></span>

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="44c55-681">Comentários</span><span class="sxs-lookup"><span data-stu-id="44c55-681">Remarks</span></span>

<span data-ttu-id="44c55-682">A classe **CIM \_ CacheMemory** é derivada da [**\_ memória CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="44c55-682">The **CIM\_CacheMemory** class is derived from [**CIM\_Memory**](cim-memory.md).</span></span>

<span data-ttu-id="44c55-683">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="44c55-683">WMI does not implement this class.</span></span> <span data-ttu-id="44c55-684">Para obter mais informações sobre classes derivadas de **CIM \_ CacheMemory**, consulte [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="44c55-684">For more information about classes derived from **CIM\_CacheMemory**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="44c55-685">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="44c55-685">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="44c55-686">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="44c55-686">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="44c55-687">Requisitos</span><span class="sxs-lookup"><span data-stu-id="44c55-687">Requirements</span></span>



| <span data-ttu-id="44c55-688">Requisito</span><span class="sxs-lookup"><span data-stu-id="44c55-688">Requirement</span></span> | <span data-ttu-id="44c55-689">Valor</span><span class="sxs-lookup"><span data-stu-id="44c55-689">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="44c55-690">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="44c55-690">Minimum supported client</span></span><br/> | <span data-ttu-id="44c55-691">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="44c55-691">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="44c55-692">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="44c55-692">Minimum supported server</span></span><br/> | <span data-ttu-id="44c55-693">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="44c55-693">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="44c55-694">Namespace</span><span class="sxs-lookup"><span data-stu-id="44c55-694">Namespace</span></span><br/>                | <span data-ttu-id="44c55-695">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="44c55-695">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="44c55-696">MOF</span><span class="sxs-lookup"><span data-stu-id="44c55-696">MOF</span></span><br/>                      | <dl> <span data-ttu-id="44c55-697"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="44c55-697"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="44c55-698">DLL</span><span class="sxs-lookup"><span data-stu-id="44c55-698">DLL</span></span><br/>                      | <dl> <span data-ttu-id="44c55-699"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="44c55-699"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="44c55-700">Confira também</span><span class="sxs-lookup"><span data-stu-id="44c55-700">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44c55-701">**\_Memória CIM**</span><span class="sxs-lookup"><span data-stu-id="44c55-701">**CIM\_Memory**</span></span>](cim-memory.md)
</dt> </dl>

 

