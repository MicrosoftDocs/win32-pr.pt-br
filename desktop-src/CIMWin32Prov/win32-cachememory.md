---
description: O Win32 \_ CacheMemory&\# 32; A classe WMI representa a memória de cache interna e externa em um sistema de computador.
ms.assetid: 9cfb992d-fbac-4e56-b4f3-61c0c93f5852
ms.tgt_platform: multiple
title: Classe Win32_CacheMemory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_CacheMemory
- Win32_CacheMemory.Reset
- Win32_CacheMemory.SetPowerState
- Win32_CacheMemory.Access
- Win32_CacheMemory.AdditionalErrorData
- Win32_CacheMemory.Associativity
- Win32_CacheMemory.Availability
- Win32_CacheMemory.BlockSize
- Win32_CacheMemory.CacheSpeed
- Win32_CacheMemory.CacheType
- Win32_CacheMemory.Caption
- Win32_CacheMemory.ConfigManagerErrorCode
- Win32_CacheMemory.ConfigManagerUserConfig
- Win32_CacheMemory.CorrectableError
- Win32_CacheMemory.CreationClassName
- Win32_CacheMemory.CurrentSRAM
- Win32_CacheMemory.Description
- Win32_CacheMemory.DeviceID
- Win32_CacheMemory.EndingAddress
- Win32_CacheMemory.ErrorAccess
- Win32_CacheMemory.ErrorAddress
- Win32_CacheMemory.ErrorCleared
- Win32_CacheMemory.ErrorCorrectType
- Win32_CacheMemory.ErrorData
- Win32_CacheMemory.ErrorDataOrder
- Win32_CacheMemory.ErrorDescription
- Win32_CacheMemory.ErrorInfo
- Win32_CacheMemory.ErrorMethodology
- Win32_CacheMemory.ErrorResolution
- Win32_CacheMemory.ErrorTime
- Win32_CacheMemory.ErrorTransferSize
- Win32_CacheMemory.FlushTimer
- Win32_CacheMemory.InstallDate
- Win32_CacheMemory.InstalledSize
- Win32_CacheMemory.LastErrorCode
- Win32_CacheMemory.Level
- Win32_CacheMemory.LineSize
- Win32_CacheMemory.Location
- Win32_CacheMemory.MaxCacheSize
- Win32_CacheMemory.Name
- Win32_CacheMemory.NumberOfBlocks
- Win32_CacheMemory.OtherErrorDescription
- Win32_CacheMemory.PNPDeviceID
- Win32_CacheMemory.PowerManagementCapabilities
- Win32_CacheMemory.PowerManagementSupported
- Win32_CacheMemory.Purpose
- Win32_CacheMemory.ReadPolicy
- Win32_CacheMemory.ReplacementPolicy
- Win32_CacheMemory.StartingAddress
- Win32_CacheMemory.Status
- Win32_CacheMemory.StatusInfo
- Win32_CacheMemory.SupportedSRAM
- Win32_CacheMemory.SystemCreationClassName
- Win32_CacheMemory.SystemLevelAddress
- Win32_CacheMemory.SystemName
- Win32_CacheMemory.WritePolicy
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 83a8fefbe1104f24f208d232b8f6bc134efefd83
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826590"
---
# <a name="win32_cachememory-class"></a><span data-ttu-id="df9d9-103">\_Classe Win32 CacheMemory</span><span class="sxs-lookup"><span data-stu-id="df9d9-103">Win32\_CacheMemory class</span></span>

<span data-ttu-id="df9d9-104">A [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ CacheMemory do Win32** representa a memória de cache interna e externa em um sistema de computador.</span><span class="sxs-lookup"><span data-stu-id="df9d9-104">The **Win32\_CacheMemory** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents internal and external cache memory on a computer system.</span></span>

<span data-ttu-id="df9d9-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="df9d9-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="df9d9-106">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="df9d9-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="df9d9-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="df9d9-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{FAF76B97-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class Win32_CacheMemory : CIM_CacheMemory
{
  uint16   Access;
  uint8    AdditionalErrorData[];
  uint16   Associativity;
  uint16   Availability;
  uint64   BlockSize;
  uint32   CacheSpeed;
  uint16   CacheType;
  string   Caption;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  boolean  CorrectableError;
  string   CreationClassName;
  uint16   CurrentSRAM[];
  string   Description;
  string   DeviceID;
  uint64   EndingAddress;
  uint16   ErrorAccess;
  uint64   ErrorAddress;
  boolean  ErrorCleared;
  uint16   ErrorCorrectType;
  uint8    ErrorData[];
  uint16   ErrorDataOrder;
  string   ErrorDescription;
  uint16   ErrorInfo;
  string   ErrorMethodology;
  uint64   ErrorResolution;
  datetime ErrorTime;
  uint32   ErrorTransferSize;
  uint32   FlushTimer;
  datetime InstallDate;
  uint32   InstalledSize;
  uint32   LastErrorCode;
  uint16   Level;
  uint32   LineSize;
  uint16   Location;
  uint32   MaxCacheSize;
  string   Name;
  uint64   NumberOfBlocks;
  string   OtherErrorDescription;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  string   Purpose;
  uint16   ReadPolicy;
  uint16   ReplacementPolicy;
  uint64   StartingAddress;
  string   Status;
  uint16   StatusInfo;
  uint16   SupportedSRAM[];
  string   SystemCreationClassName;
  boolean  SystemLevelAddress;
  string   SystemName;
  uint16   WritePolicy;
};
```

## <a name="members"></a><span data-ttu-id="df9d9-108">Membros</span><span class="sxs-lookup"><span data-stu-id="df9d9-108">Members</span></span>

<span data-ttu-id="df9d9-109">A classe **Win32 \_ CacheMemory** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="df9d9-109">The **Win32\_CacheMemory** class has these types of members:</span></span>

-   [<span data-ttu-id="df9d9-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="df9d9-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="df9d9-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="df9d9-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="df9d9-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="df9d9-112">Methods</span></span>

<span data-ttu-id="df9d9-113">A classe **Win32 \_ CacheMemory** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="df9d9-113">The **Win32\_CacheMemory** class has these methods.</span></span>



| <span data-ttu-id="df9d9-114">Método</span><span class="sxs-lookup"><span data-stu-id="df9d9-114">Method</span></span>            | <span data-ttu-id="df9d9-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="df9d9-115">Description</span></span>                                                                                                                                                                                                  |
|:------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="df9d9-116">**Redefinir**</span><span class="sxs-lookup"><span data-stu-id="df9d9-116">**Reset**</span></span>         | <span data-ttu-id="df9d9-117">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="df9d9-117">Not implemented.</span></span> <span data-ttu-id="df9d9-118">Para implementar esse método, consulte o método [**Reset**](reset-method-in-class-cim-controller.md) no [**CIM \_ CacheMemory**](cim-cachememory.md) para obter a documentação.</span><span class="sxs-lookup"><span data-stu-id="df9d9-118">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_CacheMemory**](cim-cachememory.md) for documentation.</span></span><br/>                 |
| <span data-ttu-id="df9d9-119">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="df9d9-119">**SetPowerState**</span></span> | <span data-ttu-id="df9d9-120">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="df9d9-120">Not implemented.</span></span> <span data-ttu-id="df9d9-121">Para implementar esse método, consulte o método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) no [**CIM \_ CacheMemory**](cim-cachememory.md) para obter a documentação.</span><span class="sxs-lookup"><span data-stu-id="df9d9-121">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_CacheMemory**](cim-cachememory.md) for documentation.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="df9d9-122">Propriedades</span><span class="sxs-lookup"><span data-stu-id="df9d9-122">Properties</span></span>

<span data-ttu-id="df9d9-123">A classe **Win32 \_ CacheMemory** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="df9d9-123">The **Win32\_CacheMemory** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="df9d9-124">**Acesso**</span><span class="sxs-lookup"><span data-stu-id="df9d9-124">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df9d9-125">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="df9d9-125">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="df9d9-126">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="df9d9-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="df9d9-127">Tipo de acesso.</span><span class="sxs-lookup"><span data-stu-id="df9d9-127">Type of access.</span></span>

<span data-ttu-id="df9d9-128">Essa propriedade é herdada do [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="df9d9-128">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="df9d9-129"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="df9d9-129"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>

<span data-ttu-id="df9d9-130"><span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>**Legível** (1)</span><span class="sxs-lookup"><span data-stu-id="df9d9-130"><span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>**Readable** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>

<span data-ttu-id="df9d9-131"><span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>**Gravável** (2)</span><span class="sxs-lookup"><span data-stu-id="df9d9-131"><span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>**Writeable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="df9d9-132">Gravável</span><span class="sxs-lookup"><span data-stu-id="df9d9-132">Writable</span></span>

</dd> <dt>

<span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>

<span data-ttu-id="df9d9-133"><span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>**Suporte de leitura/gravação** (3)</span><span class="sxs-lookup"><span data-stu-id="df9d9-133"><span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>**Read/Write Supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>

<span data-ttu-id="df9d9-134"><span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>**Gravar uma vez** (4)</span><span class="sxs-lookup"><span data-stu-id="df9d9-134"><span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>**Write Once** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="df9d9-135">**AdditionalErrorData**</span><span class="sxs-lookup"><span data-stu-id="df9d9-135">**AdditionalErrorData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df9d9-136">Tipo de dados: matriz **uint8**</span><span class="sxs-lookup"><span data-stu-id="df9d9-136">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="df9d9-137">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="df9d9-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="df9d9-138">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivo de memória DMTF \| 2,18 "," MIF. \|Matriz de memória física da DMTF \| 1,13 "), [**máx**](/windows/desktop/WmiSdk/standard-qualifiers) . (64)</span><span class="sxs-lookup"><span data-stu-id="df9d9-138">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.18", "MIF.DMTF\|Physical Memory Array\|001.13"), [**MAX**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="df9d9-139">Matriz de octetos que contém informações de erro adicionais.</span><span class="sxs-lookup"><span data-stu-id="df9d9-139">Array of octets that hold additional error information.</span></span> <span data-ttu-id="df9d9-140">Um exemplo é a síndrome de ECC ou o retorno dos bits de verificação se uma metodologia de erro baseada em CRC for usada.</span><span class="sxs-lookup"><span data-stu-id="df9d9-140">An example is ECC Syndrome or the return of the check bits if a CRC-based error methodology is used.</span></span> <span data-ttu-id="df9d9-141">No último caso, se um erro de bit único for reconhecido e o algoritmo CRC for conhecido, será possível determinar o bit exato que falhou.</span><span class="sxs-lookup"><span data-stu-id="df9d9-141">In the latter case, if a single-bit error is recognized and the CRC algorithm is known, it is possible to determine the exact bit that failed.</span></span> <span data-ttu-id="df9d9-142">Esse tipo de dados (síndrome de ECC, bit de verificação, dados de bits de paridade ou outras informações fornecidas pelo fornecedor) está incluído neste campo.</span><span class="sxs-lookup"><span data-stu-id="df9d9-142">This type of data (ECC Syndrome, Check Bit, Parity Bit data, or other vendor supplied information) is included in this field.</span></span> <span data-ttu-id="df9d9-143">Se a propriedade **errorInfo** for igual a 3 (OK), essa propriedade não terá significado.</span><span class="sxs-lookup"><span data-stu-id="df9d9-143">If the **ErrorInfo** property is equal to 3 (OK), then this property has no meaning.</span></span>

<span data-ttu-id="df9d9-144">Essa propriedade é herdada [**da \_ memória CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="df9d9-144">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="df9d9-145">**Capacidade de associação**</span><span class="sxs-lookup"><span data-stu-id="df9d9-145">**Associativity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df9d9-146">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="df9d9-146">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="df9d9-147">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="df9d9-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="df9d9-148">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Cache do sistema DMTF \| 3,15 ")</span><span class="sxs-lookup"><span data-stu-id="df9d9-148">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Cache\|003.15")</span></span>
</dt> </dl>

<span data-ttu-id="df9d9-149">Uma enumeração de inteiros que define a associação de cache do sistema.</span><span class="sxs-lookup"><span data-stu-id="df9d9-149">An integer enumeration that defines the system cache associativity.</span></span>

<span data-ttu-id="df9d9-150">Esse valor é proveniente do membro de **Associação** da estrutura de **informações de cache** nas informações de SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="df9d9-150">This value comes from the **Associativity** member of the **Cache Information** structure in the SMBIOS information.</span></span>

<span data-ttu-id="df9d9-151">Essa propriedade é herdada do [**CIM \_ CacheMemory**](cim-cachememory.md).</span><span class="sxs-lookup"><span data-stu-id="df9d9-151">This property is inherited from [**CIM\_CacheMemory**](cim-cachememory.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="df9d9-152">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="df9d9-152">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="df9d9-153">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="df9d9-153">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Direct_Mapped"></span><span id="direct_mapped"></span><span id="DIRECT_MAPPED"></span>

<span data-ttu-id="df9d9-154">**Mapeado direto** (3)</span><span class="sxs-lookup"><span data-stu-id="df9d9-154">**Direct Mapped** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="2-way_Set-Associative"></span><span id="2-way_set-associative"></span><span id="2-WAY_SET-ASSOCIATIVE"></span>

<span data-ttu-id="df9d9-155">**conjunto de 2 vias-associativo** (4)</span><span class="sxs-lookup"><span data-stu-id="df9d9-155">**2-way Set-Associative** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="4-way_Set-Associative"></span><span id="4-way_set-associative"></span><span id="4-WAY_SET-ASSOCIATIVE"></span>

<span data-ttu-id="df9d9-156">**conjunto de 4 vias-associativo** (5)</span><span class="sxs-lookup"><span data-stu-id="df9d9-156">**4-way Set-Associative** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Fully_Associative"></span><span id="fully_associative"></span><span id="FULLY_ASSOCIATIVE"></span>

<span data-ttu-id="df9d9-157">**Totalmente associativo** (6)</span><span class="sxs-lookup"><span data-stu-id="df9d9-157">**Fully Associative** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="8-way_Set-Associative"></span><span id="8-way_set-associative"></span><span id="8-WAY_SET-ASSOCIATIVE"></span>

<span data-ttu-id="df9d9-158">**conjunto de 8 vias – associativo** (7)</span><span class="sxs-lookup"><span data-stu-id="df9d9-158">**8-way Set-Associative** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="16-way_Set-Associative"></span><span id="16-way_set-associative"></span><span id="16-WAY_SET-ASSOCIATIVE"></span>

<span data-ttu-id="df9d9-159">**conjunto de 16 vias – associativo** (8)</span><span class="sxs-lookup"><span data-stu-id="df9d9-159">**16-way Set-Associative** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="df9d9-160">**Disponibilidade**</span><span class="sxs-lookup"><span data-stu-id="df9d9-160">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df9d9-161">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="df9d9-161">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="df9d9-162">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="df9d9-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="df9d9-163">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operacional da DMTF \| 3,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="df9d9-163">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="df9d9-164">Disponibilidade e status do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="df9d9-164">Availability and status of the device.</span></span>

<span data-ttu-id="df9d9-165">Esse valor é proveniente do membro de **configuração de cache** da estrutura de **informações de cache** nas informações de SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="df9d9-165">This value comes from the **Cache Configuration** member of the **Cache Information** structure in the SMBIOS information.</span></span>

<span data-ttu-id="df9d9-166">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="df9d9-166">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="df9d9-167"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="df9d9-167"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="df9d9-168"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="df9d9-168"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="df9d9-169"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Execução/energia completa** (3)</span><span class="sxs-lookup"><span data-stu-id="df9d9-169"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="df9d9-170">Energia completa ou em execução</span><span class="sxs-lookup"><span data-stu-id="df9d9-170">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="df9d9-171"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Aviso** (4)</span><span class="sxs-lookup"><span data-stu-id="df9d9-171"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="df9d9-172"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Em teste** (5)</span><span class="sxs-lookup"><span data-stu-id="df9d9-172"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="df9d9-173"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Não aplicável** (6)</span><span class="sxs-lookup"><span data-stu-id="df9d9-173"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="df9d9-174"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desligar (7** )</span><span class="sxs-lookup"><span data-stu-id="df9d9-174"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="df9d9-175"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off line** (8)</span><span class="sxs-lookup"><span data-stu-id="df9d9-175"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="df9d9-176"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fora do imposto** (9)</span><span class="sxs-lookup"><span data-stu-id="df9d9-176"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="df9d9-177"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="df9d9-177"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="df9d9-178"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Não instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="df9d9-178"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="df9d9-179"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Erro de instalação** (12)</span><span class="sxs-lookup"><span data-stu-id="df9d9-179"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="df9d9-180"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Economia **de energia-desconhecido** (13)</span><span class="sxs-lookup"><span data-stu-id="df9d9-180"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="df9d9-181">O dispositivo é conhecido por estar em um modo de economia de energia, mas seu status exato é desconhecido.</span><span class="sxs-lookup"><span data-stu-id="df9d9-181">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="df9d9-182"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Economia **de energia-modo de baixa energia** (14)</span><span class="sxs-lookup"><span data-stu-id="df9d9-182"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="df9d9-183">O dispositivo está em um estado de economia de energia, mas ainda está funcionando e pode exibir o desempenho degradado.</span><span class="sxs-lookup"><span data-stu-id="df9d9-183">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="df9d9-184"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save-em espera** (15)</span><span class="sxs-lookup"><span data-stu-id="df9d9-184"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="df9d9-185">O dispositivo não está funcionando, mas pode ser levado a uma potência completa rapidamente.</span><span class="sxs-lookup"><span data-stu-id="df9d9-185">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="df9d9-186"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energia** (16)</span><span class="sxs-lookup"><span data-stu-id="df9d9-186"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="df9d9-187"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Economia **de energia-aviso** (17)</span><span class="sxs-lookup"><span data-stu-id="df9d9-187"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="df9d9-188">O dispositivo está em um estado de aviso, embora também esteja em um modo de economia de energia.</span><span class="sxs-lookup"><span data-stu-id="df9d9-188">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="df9d9-189"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>Em **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="df9d9-189"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="df9d9-190">O dispositivo está em pausa.</span><span class="sxs-lookup"><span data-stu-id="df9d9-190">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="df9d9-191"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Não pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="df9d9-191"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="df9d9-192">O dispositivo não está pronto.</span><span class="sxs-lookup"><span data-stu-id="df9d9-192">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="df9d9-193"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Não configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="df9d9-193"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="df9d9-194">O dispositivo não está configurado.</span><span class="sxs-lookup"><span data-stu-id="df9d9-194">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="df9d9-195"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Desativado** (21)</span><span class="sxs-lookup"><span data-stu-id="df9d9-195"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="df9d9-196">O dispositivo está silencioso.</span><span class="sxs-lookup"><span data-stu-id="df9d9-196">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="df9d9-197">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="df9d9-197">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df9d9-198">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="df9d9-198">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="df9d9-199">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="df9d9-199">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="df9d9-200">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| host-REsources-MIB. hrStorageAllocationUnits "), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ")</span><span class="sxs-lookup"><span data-stu-id="df9d9-200">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageAllocationUnits"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="df9d9-201">Tamanho em bytes dos blocos que formam esta extensão de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="df9d9-201">Size in bytes of the blocks that form this storage extent.</span></span> <span data-ttu-id="df9d9-202">Se for desconhecido ou se um conceito de bloco não for válido (por exemplo, para extensões de agregação, memória ou discos lógicos), insira 1.</span><span class="sxs-lookup"><span data-stu-id="df9d9-202">If unknown or if a block concept is not valid (for example, for aggregate extents, memory, or logical disks), enter a 1.</span></span>

<span data-ttu-id="df9d9-203">Essa propriedade é herdada do [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="df9d9-203">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="df9d9-204">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="df9d9-204">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="df9d9-205">**CacheSpeed**</span><span class="sxs-lookup"><span data-stu-id="df9d9-205">**CacheSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df9d9-206">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="df9d9-206">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="df9d9-207">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="df9d9-207">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="df9d9-208">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| velocidade de cache do tipo SMBIOS 7 \| "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("nanossegundos")</span><span class="sxs-lookup"><span data-stu-id="df9d9-208">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 7\|Cache Speed"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("nanoseconds")</span></span>
</dt> </dl>

<span data-ttu-id="df9d9-209">Velocidade do cache.</span><span class="sxs-lookup"><span data-stu-id="df9d9-209">Speed of the cache.</span></span>

<span data-ttu-id="df9d9-210">Esse valor é proveniente do membro de **velocidade de cache** da estrutura de **informações de cache** nas informações de SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="df9d9-210">This value comes from the **Cache Speed** member of the **Cache Information** structure in the SMBIOS information.</span></span>

</dd> <dt>

<span data-ttu-id="df9d9-211">**CacheType**</span><span class="sxs-lookup"><span data-stu-id="df9d9-211">**CacheType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df9d9-212">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="df9d9-212">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="df9d9-213">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="df9d9-213">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="df9d9-214">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Cache do sistema DMTF \| 3,9 ")</span><span class="sxs-lookup"><span data-stu-id="df9d9-214">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Cache\|003.9")</span></span>
</dt> </dl>

<span data-ttu-id="df9d9-215">Tipo de cache.</span><span class="sxs-lookup"><span data-stu-id="df9d9-215">Type of cache.</span></span>

<span data-ttu-id="df9d9-216">Esse valor é proveniente do membro do **tipo de cache System** da estrutura de **informações do cache** nas informações do SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="df9d9-216">This value comes from the **System Cache Type** member of the **Cache Information** structure in the SMBIOS information.</span></span>

<span data-ttu-id="df9d9-217">Essa propriedade é herdada do [**CIM \_ CacheMemory**](cim-cachememory.md).</span><span class="sxs-lookup"><span data-stu-id="df9d9-217">This property is inherited from [**CIM\_CacheMemory**](cim-cachememory.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="df9d9-218">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="df9d9-218">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="df9d9-219">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="df9d9-219">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Instruction"></span><span id="instruction"></span><span id="INSTRUCTION"></span>

<span data-ttu-id="df9d9-220">**Instrução** (3)</span><span class="sxs-lookup"><span data-stu-id="df9d9-220">**Instruction** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Data"></span><span id="data"></span><span id="DATA"></span>

<span data-ttu-id="df9d9-221">**Dados** (4)</span><span class="sxs-lookup"><span data-stu-id="df9d9-221">**Data** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Unified"></span><span id="unified"></span><span id="UNIFIED"></span>

<span data-ttu-id="df9d9-222">**Unificado** (5)</span><span class="sxs-lookup"><span data-stu-id="df9d9-222">**Unified** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="df9d9-223">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="df9d9-223">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df9d9-224">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="df9d9-224">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="df9d9-225">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="df9d9-225">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="df9d9-226">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="df9d9-226">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="df9d9-227">Breve descrição do objeto de uma cadeia de caracteres de uma linha.</span><span class="sxs-lookup"><span data-stu-id="df9d9-227">Short description of the object a one-line string.</span></span>

<span data-ttu-id="df9d9-228">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="df9d9-228">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="df9d9-229">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="df9d9-229">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df9d9-230">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="df9d9-230">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="df9d9-231">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="df9d9-231">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="df9d9-232">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="df9d9-232">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="df9d9-233">Código de erro do Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="df9d9-233">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="df9d9-234">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="df9d9-234">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="df9d9-235"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Este dispositivo está funcionando corretamente.**</span><span class="sxs-lookup"><span data-stu-id="df9d9-235"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="df9d9-236"> acima (0)</span><span class="sxs-lookup"><span data-stu-id="df9d9-236">(0)</span></span>


</dt> <dd>

<span data-ttu-id="df9d9-237">O dispositivo está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="df9d9-237">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="df9d9-238"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Este dispositivo não está configurado corretamente.**</span><span class="sxs-lookup"><span data-stu-id="df9d9-238"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="df9d9-239">(1)</span><span class="sxs-lookup"><span data-stu-id="df9d9-239">(1)</span></span>


</dt> <dd>

<span data-ttu-id="df9d9-240">O dispositivo não está configurado corretamente.</span><span class="sxs-lookup"><span data-stu-id="df9d9-240">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="df9d9-241"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**O Windows não pode carregar o driver para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="df9d9-241"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="df9d9-242">(2)</span><span class="sxs-lookup"><span data-stu-id="df9d9-242">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="df9d9-243"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**O driver para este dispositivo pode estar corrompido ou o sistema pode estar com pouca memória ou outros recursos.**</span><span class="sxs-lookup"><span data-stu-id="df9d9-243"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="df9d9-244">(3)</span><span class="sxs-lookup"><span data-stu-id="df9d9-244">(3)</span></span>


</dt> <dd>

<span data-ttu-id="df9d9-245">O driver para este dispositivo pode estar corrompido ou o sistema pode estar com pouca memória ou outros recursos.</span><span class="sxs-lookup"><span data-stu-id="df9d9-245">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="df9d9-246"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Este dispositivo não está funcionando corretamente. Um de seus drivers ou seu registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="df9d9-246"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="df9d9-247">(4)</span><span class="sxs-lookup"><span data-stu-id="df9d9-247">(4)</span></span>


</dt> <dd>

<span data-ttu-id="df9d9-248">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="df9d9-248">Device is not working properly.</span></span> <span data-ttu-id="df9d9-249">Um de seus drivers ou o registro pode estar corrompido.</span><span class="sxs-lookup"><span data-stu-id="df9d9-249">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="df9d9-250"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**O driver para este dispositivo precisa de um recurso que o Windows não possa gerenciar.**</span><span class="sxs-lookup"><span data-stu-id="df9d9-250"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="df9d9-251">(5)</span><span class="sxs-lookup"><span data-stu-id="df9d9-251">(5)</span></span>


</dt> <dd>

<span data-ttu-id="df9d9-252">O driver para o dispositivo requer um recurso que o Windows não pode gerenciar.</span><span class="sxs-lookup"><span data-stu-id="df9d9-252">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="df9d9-253"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**A configuração de inicialização para este dispositivo está em conflito com outros dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="df9d9-253"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="df9d9-254"> (6)</span><span class="sxs-lookup"><span data-stu-id="df9d9-254">(6)</span></span>


</dt> <dd>

<span data-ttu-id="df9d9-255">A configuração de inicialização para o dispositivo está em conflito com outros dispositivos.</span><span class="sxs-lookup"><span data-stu-id="df9d9-255">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="df9d9-256"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Não é possível filtrar.**</span><span class="sxs-lookup"><span data-stu-id="df9d9-256"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="df9d9-257">(7)</span><span class="sxs-lookup"><span data-stu-id="df9d9-257">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="df9d9-258"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**O carregador de driver para o dispositivo está ausente.**</span><span class="sxs-lookup"><span data-stu-id="df9d9-258"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="df9d9-259">(8)</span><span class="sxs-lookup"><span data-stu-id="df9d9-259">(8)</span></span>


</dt> <dd>

<span data-ttu-id="df9d9-260">O carregador de driver para o dispositivo está ausente.</span><span class="sxs-lookup"><span data-stu-id="df9d9-260">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="df9d9-261"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Este dispositivo não está funcionando corretamente porque o firmware de controle está relatando os recursos para o dispositivo incorretamente.**</span><span class="sxs-lookup"><span data-stu-id="df9d9-261"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="df9d9-262">(9)</span><span class="sxs-lookup"><span data-stu-id="df9d9-262">(9)</span></span>


</dt> <dd>

<span data-ttu-id="df9d9-263">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="df9d9-263">Device is not working properly.</span></span> <span data-ttu-id="df9d9-264">O firmware de controle está relatando incorretamente os recursos para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="df9d9-264">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="df9d9-265"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Este dispositivo não pode ser iniciado.**</span><span class="sxs-lookup"><span data-stu-id="df9d9-265"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="df9d9-266">(10)</span><span class="sxs-lookup"><span data-stu-id="df9d9-266">(10)</span></span>


</dt> <dd>

<span data-ttu-id="df9d9-267">Não é possível iniciar o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="df9d9-267">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="df9d9-268"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Este dispositivo falhou.**</span><span class="sxs-lookup"><span data-stu-id="df9d9-268"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="df9d9-269">(11)</span><span class="sxs-lookup"><span data-stu-id="df9d9-269">(11)</span></span>


</dt> <dd>

<span data-ttu-id="df9d9-270">Falha no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="df9d9-270">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="df9d9-271"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Este dispositivo não pode encontrar recursos livres suficientes que podem ser usados.**</span><span class="sxs-lookup"><span data-stu-id="df9d9-271"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="df9d9-272">12</span><span class="sxs-lookup"><span data-stu-id="df9d9-272">(12)</span></span>


</dt> <dd>

<span data-ttu-id="df9d9-273">O dispositivo não pode encontrar recursos livres suficientes para usar.</span><span class="sxs-lookup"><span data-stu-id="df9d9-273">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="df9d9-274"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**O Windows não pode verificar os recursos deste dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="df9d9-274"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="df9d9-275">(13)</span><span class="sxs-lookup"><span data-stu-id="df9d9-275">(13)</span></span>


</dt> <dd>

<span data-ttu-id="df9d9-276">O Windows não pode verificar os recursos do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="df9d9-276">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="df9d9-277"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Este dispositivo não funcionará corretamente até que você reinicie o computador.**</span><span class="sxs-lookup"><span data-stu-id="df9d9-277"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="df9d9-278">(14)</span><span class="sxs-lookup"><span data-stu-id="df9d9-278">(14)</span></span>


</dt> <dd>

<span data-ttu-id="df9d9-279">O dispositivo não funcionará corretamente até que o computador seja reiniciado.</span><span class="sxs-lookup"><span data-stu-id="df9d9-279">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="df9d9-280"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Este dispositivo não está funcionando corretamente porque provavelmente há um problema de nova enumeração.**</span><span class="sxs-lookup"><span data-stu-id="df9d9-280"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="df9d9-281">(15)</span><span class="sxs-lookup"><span data-stu-id="df9d9-281">(15)</span></span>


</dt> <dd>

<span data-ttu-id="df9d9-282">O dispositivo não está funcionando corretamente devido a um possível problema de reenumeração.</span><span class="sxs-lookup"><span data-stu-id="df9d9-282">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="df9d9-283"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**O Windows não pode identificar todos os recursos que este dispositivo usa.**</span><span class="sxs-lookup"><span data-stu-id="df9d9-283"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="df9d9-284">(16)</span><span class="sxs-lookup"><span data-stu-id="df9d9-284">(16)</span></span>


</dt> <dd>

<span data-ttu-id="df9d9-285">O Windows não pode identificar todos os recursos que o dispositivo usa.</span><span class="sxs-lookup"><span data-stu-id="df9d9-285">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="df9d9-286"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Este dispositivo está solicitando um tipo de recurso desconhecido.**</span><span class="sxs-lookup"><span data-stu-id="df9d9-286"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="df9d9-287">(17)</span><span class="sxs-lookup"><span data-stu-id="df9d9-287">(17)</span></span>


</dt> <dd>

<span data-ttu-id="df9d9-288">O dispositivo está solicitando um tipo de recurso desconhecido.</span><span class="sxs-lookup"><span data-stu-id="df9d9-288">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="df9d9-289"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstale os drivers para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="df9d9-289"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="df9d9-290">(18)</span><span class="sxs-lookup"><span data-stu-id="df9d9-290">(18)</span></span>


</dt> <dd>

<span data-ttu-id="df9d9-291">Os drivers de dispositivo devem ser reinstalados.</span><span class="sxs-lookup"><span data-stu-id="df9d9-291">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="df9d9-292"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Falha ao usar o carregador VxD.**</span><span class="sxs-lookup"><span data-stu-id="df9d9-292"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="df9d9-293">(19)</span><span class="sxs-lookup"><span data-stu-id="df9d9-293">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="df9d9-294"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**O registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="df9d9-294"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="df9d9-295">(20)</span><span class="sxs-lookup"><span data-stu-id="df9d9-295">(20)</span></span>


</dt> <dd>

<span data-ttu-id="df9d9-296">O registro pode estar corrompido.</span><span class="sxs-lookup"><span data-stu-id="df9d9-296">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="df9d9-297"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware. O Windows está removendo este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="df9d9-297"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="df9d9-298">(21)</span><span class="sxs-lookup"><span data-stu-id="df9d9-298">(21)</span></span>


</dt> <dd>

<span data-ttu-id="df9d9-299">Falha do sistema.</span><span class="sxs-lookup"><span data-stu-id="df9d9-299">System failure.</span></span> <span data-ttu-id="df9d9-300">Se a alteração do driver de dispositivo não for eficaz, consulte a documentação do hardware.</span><span class="sxs-lookup"><span data-stu-id="df9d9-300">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="df9d9-301">O Windows está removendo o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="df9d9-301">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="df9d9-302"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Este dispositivo está desabilitado.**</span><span class="sxs-lookup"><span data-stu-id="df9d9-302"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="df9d9-303">(22)</span><span class="sxs-lookup"><span data-stu-id="df9d9-303">(22)</span></span>


</dt> <dd>

<span data-ttu-id="df9d9-304">O dispositivo está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="df9d9-304">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="df9d9-305"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware.**</span><span class="sxs-lookup"><span data-stu-id="df9d9-305"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="df9d9-306">(23)</span><span class="sxs-lookup"><span data-stu-id="df9d9-306">(23)</span></span>


</dt> <dd>

<span data-ttu-id="df9d9-307">Falha do sistema.</span><span class="sxs-lookup"><span data-stu-id="df9d9-307">System failure.</span></span> <span data-ttu-id="df9d9-308">Se a alteração do driver de dispositivo não for eficaz, consulte a documentação do hardware.</span><span class="sxs-lookup"><span data-stu-id="df9d9-308">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="df9d9-309"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Este dispositivo não está presente, não está funcionando corretamente ou não tem todos os drivers instalados.**</span><span class="sxs-lookup"><span data-stu-id="df9d9-309"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="df9d9-310">(24)</span><span class="sxs-lookup"><span data-stu-id="df9d9-310">(24)</span></span>


</dt> <dd>

<span data-ttu-id="df9d9-311">O dispositivo não está presente, não está funcionando corretamente ou não tem todos os seus drivers instalados.</span><span class="sxs-lookup"><span data-stu-id="df9d9-311">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="df9d9-312"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="df9d9-312"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="df9d9-313">(25)</span><span class="sxs-lookup"><span data-stu-id="df9d9-313">(25)</span></span>


</dt> <dd>

<span data-ttu-id="df9d9-314">O Windows ainda está configurando o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="df9d9-314">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="df9d9-315"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="df9d9-315"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="df9d9-316">(26)</span><span class="sxs-lookup"><span data-stu-id="df9d9-316">(26)</span></span>


</dt> <dd>

<span data-ttu-id="df9d9-317">O Windows ainda está configurando o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="df9d9-317">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="df9d9-318"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Este dispositivo não tem uma configuração de log válida.**</span><span class="sxs-lookup"><span data-stu-id="df9d9-318"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="df9d9-319">(27)</span><span class="sxs-lookup"><span data-stu-id="df9d9-319">(27)</span></span>


</dt> <dd>

<span data-ttu-id="df9d9-320">O dispositivo não tem uma configuração de log válida.</span><span class="sxs-lookup"><span data-stu-id="df9d9-320">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="df9d9-321"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Os drivers para este dispositivo não estão instalados.**</span><span class="sxs-lookup"><span data-stu-id="df9d9-321"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="df9d9-322">(28)</span><span class="sxs-lookup"><span data-stu-id="df9d9-322">(28)</span></span>


</dt> <dd>

<span data-ttu-id="df9d9-323">Os drivers de dispositivo não estão instalados.</span><span class="sxs-lookup"><span data-stu-id="df9d9-323">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="df9d9-324"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Este dispositivo está desabilitado porque o firmware do dispositivo não forneceu os recursos necessários.**</span><span class="sxs-lookup"><span data-stu-id="df9d9-324"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="df9d9-325">(29)</span><span class="sxs-lookup"><span data-stu-id="df9d9-325">(29)</span></span>


</dt> <dd>

<span data-ttu-id="df9d9-326">O dispositivo está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="df9d9-326">Device is disabled.</span></span> <span data-ttu-id="df9d9-327">O firmware do dispositivo não forneceu os recursos necessários.</span><span class="sxs-lookup"><span data-stu-id="df9d9-327">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="df9d9-328"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Este dispositivo está usando um recurso de IRQ (solicitação de interrupção) que outro dispositivo está usando.**</span><span class="sxs-lookup"><span data-stu-id="df9d9-328"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="df9d9-329">(30)</span><span class="sxs-lookup"><span data-stu-id="df9d9-329">(30)</span></span>


</dt> <dd>

<span data-ttu-id="df9d9-330">O dispositivo está usando um recurso de IRQ que outro dispositivo está usando.</span><span class="sxs-lookup"><span data-stu-id="df9d9-330">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="df9d9-331"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Este dispositivo não está funcionando corretamente porque o Windows não pode carregar os drivers necessários para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="df9d9-331"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="df9d9-332">(31)</span><span class="sxs-lookup"><span data-stu-id="df9d9-332">(31)</span></span>


</dt> <dd>

<span data-ttu-id="df9d9-333">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="df9d9-333">Device is not working properly.</span></span> <span data-ttu-id="df9d9-334">O Windows não pode carregar os drivers de dispositivo necessários.</span><span class="sxs-lookup"><span data-stu-id="df9d9-334">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="df9d9-335">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="df9d9-335">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df9d9-336">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="df9d9-336">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="df9d9-337">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="df9d9-337">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="df9d9-338">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="df9d9-338">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="df9d9-339">Se for **true**, o dispositivo estará usando uma configuração definida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="df9d9-339">If **True**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="df9d9-340">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="df9d9-340">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="df9d9-341">**CorrectableError**</span><span class="sxs-lookup"><span data-stu-id="df9d9-341">**CorrectableError**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df9d9-342">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="df9d9-342">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="df9d9-343">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="df9d9-343">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="df9d9-344">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivo de memória DMTF \| 2,12 "," MIF. \|Matriz de memória física da DMTF \| 1,8 ")</span><span class="sxs-lookup"><span data-stu-id="df9d9-344">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.12", "MIF.DMTF\|Physical Memory Array\|001.8")</span></span>
</dt> </dl>

<span data-ttu-id="df9d9-345">Se **for true**, o erro mais recente era corrigível.</span><span class="sxs-lookup"><span data-stu-id="df9d9-345">If **True**, the most recent error was correctable.</span></span> <span data-ttu-id="df9d9-346">Se a propriedade **errorInfo** for igual a 3 (OK), essa propriedade não terá significado.</span><span class="sxs-lookup"><span data-stu-id="df9d9-346">If the **ErrorInfo** property is equal to 3 (OK), then this property has no meaning.</span></span>

<span data-ttu-id="df9d9-347">Essa propriedade é herdada [**da \_ memória CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="df9d9-347">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="df9d9-348">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="df9d9-348">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df9d9-349">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="df9d9-349">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="df9d9-350">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="df9d9-350">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="df9d9-351">Qualificadores: [ **\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="df9d9-351">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="df9d9-352">Nome da primeira classe concreta a ser exibida na cadeia de herança usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="df9d9-352">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="df9d9-353">Quando usado com as outras propriedades de chave da classe, a propriedade permite que todas as instâncias dessa classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="df9d9-353">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="df9d9-354">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="df9d9-354">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="df9d9-355">**CurrentSRAM**</span><span class="sxs-lookup"><span data-stu-id="df9d9-355">**CurrentSRAM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df9d9-356">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="df9d9-356">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="df9d9-357">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="df9d9-357">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="df9d9-358">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| tipo de SRAM atual do tipo SMBIOS 7 \| ")</span><span class="sxs-lookup"><span data-stu-id="df9d9-358">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 7\|Current SRAM Type")</span></span>
</dt> </dl>

<span data-ttu-id="df9d9-359">Matriz de tipos de memória de acesso aleatório estático (SRAM) que está sendo usada para a memória de cache.</span><span class="sxs-lookup"><span data-stu-id="df9d9-359">Array of types of Static Random Access Memory (SRAM) being used for the cache memory.</span></span>

<span data-ttu-id="df9d9-360">Esse valor é proveniente do membro de **tipo de SRAM atual** da estrutura de **informações de cache** nas informações de SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="df9d9-360">This value comes from the **Current SRAM Type** member of the **Cache Information** structure in the SMBIOS information.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="df9d9-361">**Outro** (0)</span><span class="sxs-lookup"><span data-stu-id="df9d9-361">**Other** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="df9d9-362">**Desconhecido** (1)</span><span class="sxs-lookup"><span data-stu-id="df9d9-362">**Unknown** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Non-Burst"></span><span id="non-burst"></span><span id="NON-BURST"></span>

<span data-ttu-id="df9d9-363">**Não intermitente** (2)</span><span class="sxs-lookup"><span data-stu-id="df9d9-363">**Non-Burst** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Burst"></span><span id="burst"></span><span id="BURST"></span>

<span data-ttu-id="df9d9-364">**Intermitência** (3)</span><span class="sxs-lookup"><span data-stu-id="df9d9-364">**Burst** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Pipeline_Burst"></span><span id="pipeline_burst"></span><span id="PIPELINE_BURST"></span>

<span data-ttu-id="df9d9-365">**Disparo de pipeline** (4)</span><span class="sxs-lookup"><span data-stu-id="df9d9-365">**Pipeline Burst** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Synchronous"></span><span id="synchronous"></span><span id="SYNCHRONOUS"></span>

<span data-ttu-id="df9d9-366">**Síncrono** (5)</span><span class="sxs-lookup"><span data-stu-id="df9d9-366">**Synchronous** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Asynchronous"></span><span id="asynchronous"></span><span id="ASYNCHRONOUS"></span>

<span data-ttu-id="df9d9-367">**Assíncrono** (6)</span><span class="sxs-lookup"><span data-stu-id="df9d9-367">**Asynchronous** (6)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="df9d9-368">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="df9d9-368">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df9d9-369">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="df9d9-369">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="df9d9-370">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="df9d9-370">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="df9d9-371">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="df9d9-371">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="df9d9-372">Descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="df9d9-372">Description of the object.</span></span>

<span data-ttu-id="df9d9-373">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="df9d9-373">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="df9d9-374">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="df9d9-374">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df9d9-375">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="df9d9-375">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="df9d9-376">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="df9d9-376">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="df9d9-377">Qualificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceID"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="df9d9-377">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceId"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="df9d9-378">Identificador exclusivo do cache representado por uma instância do **Win32 \_ CacheMemory**.</span><span class="sxs-lookup"><span data-stu-id="df9d9-378">Unique identifier of the cache represented by an instance of **Win32\_CacheMemory**.</span></span>

<span data-ttu-id="df9d9-379">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="df9d9-379">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="df9d9-380">Exemplo: "memória cache 1"</span><span class="sxs-lookup"><span data-stu-id="df9d9-380">Example: "Cache Memory 1"</span></span>

</dd> <dt>

<span data-ttu-id="df9d9-381">**EndingAddress**</span><span class="sxs-lookup"><span data-stu-id="df9d9-381">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df9d9-382">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="df9d9-382">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="df9d9-383">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="df9d9-383">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="df9d9-384">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. Os \| endereços mapeados da matriz de memória DMTF \| 1,4 "," MIF. \|Endereços mapeados do dispositivo \| de memória DMTF 1,5 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" kilobytes ")</span><span class="sxs-lookup"><span data-stu-id="df9d9-384">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Array Mapped Addresses\|001.4", "MIF.DMTF\|Memory Device Mapped Addresses\|001.5"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="df9d9-385">Endereço final, referenciado por um aplicativo ou sistema operacional e mapeado por um controlador de memória, para esse objeto de memória.</span><span class="sxs-lookup"><span data-stu-id="df9d9-385">Ending address, referenced by an application or operating system and mapped by a memory controller, for this memory object.</span></span> <span data-ttu-id="df9d9-386">O endereço final é especificado em kilobytes.</span><span class="sxs-lookup"><span data-stu-id="df9d9-386">The ending address is specified in kilobytes.</span></span>

<span data-ttu-id="df9d9-387">Essa propriedade é herdada [**da \_ memória CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="df9d9-387">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<span data-ttu-id="df9d9-388">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="df9d9-388">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="df9d9-389">**ErrorAccess**</span><span class="sxs-lookup"><span data-stu-id="df9d9-389">**ErrorAccess**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df9d9-390">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="df9d9-390">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="df9d9-391">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="df9d9-391">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="df9d9-392">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivo de memória DMTF \| 2,15 "," MIF. \|Matriz de memória física da DMTF \| 1,10 ")</span><span class="sxs-lookup"><span data-stu-id="df9d9-392">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.15", "MIF.DMTF\|Physical Memory Array\|001.10")</span></span>
</dt> </dl>

<span data-ttu-id="df9d9-393">Operação de acesso à memória que causou o último erro.</span><span class="sxs-lookup"><span data-stu-id="df9d9-393">Memory access operation that caused the last error.</span></span> <span data-ttu-id="df9d9-394">O tipo de erro é descrito pela propriedade **errorInfo** .</span><span class="sxs-lookup"><span data-stu-id="df9d9-394">The type of error is described by the **ErrorInfo** property.</span></span> <span data-ttu-id="df9d9-395">Se **errorInfo** for igual a 3 (OK), essa propriedade não terá significado.</span><span class="sxs-lookup"><span data-stu-id="df9d9-395">If **ErrorInfo** is equal to 3 (OK), then this property has no meaning.</span></span>

<span data-ttu-id="df9d9-396">Essa propriedade é herdada [**da \_ memória CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="df9d9-396">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="df9d9-397">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="df9d9-397">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="df9d9-398">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="df9d9-398">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Read"></span><span id="read"></span><span id="READ"></span>

<span data-ttu-id="df9d9-399">**Leitura** (3)</span><span class="sxs-lookup"><span data-stu-id="df9d9-399">**Read** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write"></span><span id="write"></span><span id="WRITE"></span>

<span data-ttu-id="df9d9-400">**Gravação** (4)</span><span class="sxs-lookup"><span data-stu-id="df9d9-400">**Write** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Partial_Write"></span><span id="partial_write"></span><span id="PARTIAL_WRITE"></span>

<span data-ttu-id="df9d9-401">**Gravação parcial** (5)</span><span class="sxs-lookup"><span data-stu-id="df9d9-401">**Partial Write** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="df9d9-402">**ErrorAddress**</span><span class="sxs-lookup"><span data-stu-id="df9d9-402">**ErrorAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df9d9-403">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="df9d9-403">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="df9d9-404">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="df9d9-404">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="df9d9-405">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivo de memória DMTF \| 2,19 "," MIF. \|Dispositivo de memória DMTF \| 2,20 "," MIF. \|Matriz de memória física da DMTF \| 1,14 ")</span><span class="sxs-lookup"><span data-stu-id="df9d9-405">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.19", "MIF.DMTF\|Memory Device\|002.20", "MIF.DMTF\|Physical Memory Array\|001.14")</span></span>
</dt> </dl>

<span data-ttu-id="df9d9-406">Endereço do último erro de memória.</span><span class="sxs-lookup"><span data-stu-id="df9d9-406">Address of the last memory error.</span></span> <span data-ttu-id="df9d9-407">O tipo de erro é descrito pela propriedade **errorInfo** .</span><span class="sxs-lookup"><span data-stu-id="df9d9-407">The type of error is described by the **ErrorInfo** property.</span></span> <span data-ttu-id="df9d9-408">Se **errorInfo** for igual a 3 (OK), essa propriedade não terá significado.</span><span class="sxs-lookup"><span data-stu-id="df9d9-408">If **ErrorInfo** is equal to 3 (OK), then this property has no meaning.</span></span>

<span data-ttu-id="df9d9-409">Essa propriedade é herdada [**da \_ memória CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="df9d9-409">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<span data-ttu-id="df9d9-410">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="df9d9-410">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="df9d9-411">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="df9d9-411">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df9d9-412">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="df9d9-412">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="df9d9-413">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="df9d9-413">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="df9d9-414">Se **for true**, o erro relatado em **LastErrorCode** agora será limpo.</span><span class="sxs-lookup"><span data-stu-id="df9d9-414">If **True**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="df9d9-415">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="df9d9-415">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="df9d9-416">**ErrorCorrectType**</span><span class="sxs-lookup"><span data-stu-id="df9d9-416">**ErrorCorrectType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df9d9-417">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="df9d9-417">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="df9d9-418">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="df9d9-418">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="df9d9-419">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| tipo de correção de erro do tipo SMBIOS 7 \| ")</span><span class="sxs-lookup"><span data-stu-id="df9d9-419">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 7\|Error Correction Type")</span></span>
</dt> </dl>

<span data-ttu-id="df9d9-420">Método de correção de erro usado pela memória de cache.</span><span class="sxs-lookup"><span data-stu-id="df9d9-420">Error correction method used by the cache memory.</span></span>

<span data-ttu-id="df9d9-421">Esse valor é proveniente do membro de **tipo de correção de erro** da estrutura de informações de **cache** nas informações de SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="df9d9-421">This value comes from the **Error Correction Type** member of the **Cache Information** structure in the SMBIOS information.</span></span>

<dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="df9d9-422">**Reservado** (0)</span><span class="sxs-lookup"><span data-stu-id="df9d9-422">**Reserved** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="df9d9-423">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="df9d9-423">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="df9d9-424">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="df9d9-424">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="df9d9-425">**Nenhum** (3)</span><span class="sxs-lookup"><span data-stu-id="df9d9-425">**None** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Parity"></span><span id="parity"></span><span id="PARITY"></span>

<span data-ttu-id="df9d9-426">**Paridade** (4)</span><span class="sxs-lookup"><span data-stu-id="df9d9-426">**Parity** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Single-bit_ECC"></span><span id="single-bit_ecc"></span><span id="SINGLE-BIT_ECC"></span>

<span data-ttu-id="df9d9-427">**ECC de bit único** (5)</span><span class="sxs-lookup"><span data-stu-id="df9d9-427">**Single-bit ECC** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Multi-bit_ECC"></span><span id="multi-bit_ecc"></span><span id="MULTI-BIT_ECC"></span>

<span data-ttu-id="df9d9-428">**ECC de vários bits** (6)</span><span class="sxs-lookup"><span data-stu-id="df9d9-428">**Multi-bit ECC** (6)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="df9d9-429">**ErrorData**</span><span class="sxs-lookup"><span data-stu-id="df9d9-429">**ErrorData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df9d9-430">Tipo de dados: matriz **uint8**</span><span class="sxs-lookup"><span data-stu-id="df9d9-430">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="df9d9-431">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="df9d9-431">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="df9d9-432">Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivo de memória DMTF \| 2,17 "," MIF. \|Matriz de memória física da DMTF \| 1,12 "), [**máx**](/windows/desktop/WmiSdk/standard-qualifiers) . (64)</span><span class="sxs-lookup"><span data-stu-id="df9d9-432">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.17", "MIF.DMTF\|Physical Memory Array\|001.12"), [**MAX**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="df9d9-433">Matriz de dados capturados durante o último acesso de memória incorreto.</span><span class="sxs-lookup"><span data-stu-id="df9d9-433">Array of data captured during the last erroneous memory access.</span></span> <span data-ttu-id="df9d9-434">Os dados ocupam os primeiros *n* octetos da matriz necessários para manter o número de bits especificado pela propriedade **ErrorTransferSize** .</span><span class="sxs-lookup"><span data-stu-id="df9d9-434">The data occupies the first *n* octets of the array necessary to hold the number of bits specified by the **ErrorTransferSize** property.</span></span> <span data-ttu-id="df9d9-435">Se **ErrorTransferSize** for 0 (zero), essa propriedade não terá significado.</span><span class="sxs-lookup"><span data-stu-id="df9d9-435">If **ErrorTransferSize** is 0 (zero), then this property has no meaning.</span></span>

<span data-ttu-id="df9d9-436">Essa propriedade é herdada [**da \_ memória CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="df9d9-436">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="df9d9-437">**ErrorDataOrder**</span><span class="sxs-lookup"><span data-stu-id="df9d9-437">**ErrorDataOrder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df9d9-438">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="df9d9-438">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="df9d9-439">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="df9d9-439">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="df9d9-440">Ordenação de dados armazenados na propriedade **ErrorData** .</span><span class="sxs-lookup"><span data-stu-id="df9d9-440">Ordering for data stored in the **ErrorData** property.</span></span> <span data-ttu-id="df9d9-441">Se **ErrorTransferSize** for 0 (zero), essa propriedade não terá significado.</span><span class="sxs-lookup"><span data-stu-id="df9d9-441">If **ErrorTransferSize** is 0 (zero), then this property has no meaning.</span></span>

<span data-ttu-id="df9d9-442">Essa propriedade é herdada [**da \_ memória CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="df9d9-442">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="df9d9-443">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="df9d9-443">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Least_Significant_Byte_First"></span><span id="least_significant_byte_first"></span><span id="LEAST_SIGNIFICANT_BYTE_FIRST"></span>

<span data-ttu-id="df9d9-444">**Byte menos significativo primeiro** (1)</span><span class="sxs-lookup"><span data-stu-id="df9d9-444">**Least Significant Byte First** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Most_Significant_Byte_First"></span><span id="most_significant_byte_first"></span><span id="MOST_SIGNIFICANT_BYTE_FIRST"></span>

<span data-ttu-id="df9d9-445">**Byte mais significativo primeiro** (2)</span><span class="sxs-lookup"><span data-stu-id="df9d9-445">**Most Significant Byte First** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="df9d9-446">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="df9d9-446">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df9d9-447">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="df9d9-447">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="df9d9-448">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="df9d9-448">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="df9d9-449">Mais informações sobre o erro registrado em **LastErrorCode** e informações sobre as ações corretivas que podem ser executadas.</span><span class="sxs-lookup"><span data-stu-id="df9d9-449">More information about the error recorded in **LastErrorCode**, and information on any corrective actions that may be taken.</span></span>

<span data-ttu-id="df9d9-450">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="df9d9-450">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="df9d9-451">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="df9d9-451">**ErrorInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df9d9-452">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="df9d9-452">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="df9d9-453">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="df9d9-453">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="df9d9-454">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivo de memória DMTF \| 2,12 "," MIF. \|Matriz de memória física da DMTF \| 1,8 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ memória CIM**](cim-memory.md).**OtherErrorDescription**")</span><span class="sxs-lookup"><span data-stu-id="df9d9-454">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.12", "MIF.DMTF\|Physical Memory Array\|001.8"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Memory**](cim-memory.md).**OtherErrorDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="df9d9-455">Tipo de erro que ocorreu mais recentemente.</span><span class="sxs-lookup"><span data-stu-id="df9d9-455">Type of error that occurred most recently.</span></span> <span data-ttu-id="df9d9-456">Os valores 12-14 são indefinidos no esquema CIM porque, no DMI, eles misturam a semântica do tipo de erro e se ele era corrigível ou não.</span><span class="sxs-lookup"><span data-stu-id="df9d9-456">The values 12-14 are undefined in the CIM schema because in DMI they mix the semantics of the type of error and whether it was correctable or not.</span></span> <span data-ttu-id="df9d9-457">O último é indicado na propriedade **CorrectableError**.</span><span class="sxs-lookup"><span data-stu-id="df9d9-457">The latter is indicated in the property **CorrectableError**.</span></span>

<span data-ttu-id="df9d9-458">Essa propriedade é herdada [**da \_ memória CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="df9d9-458">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="df9d9-459">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="df9d9-459">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="df9d9-460">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="df9d9-460">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="df9d9-461">**OK** (3)</span><span class="sxs-lookup"><span data-stu-id="df9d9-461">**OK** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Bad_Read"></span><span id="bad_read"></span><span id="BAD_READ"></span>

<span data-ttu-id="df9d9-462">**Leitura inadequada** (4)</span><span class="sxs-lookup"><span data-stu-id="df9d9-462">**Bad Read** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Parity_Error"></span><span id="parity_error"></span><span id="PARITY_ERROR"></span>

<span data-ttu-id="df9d9-463">**Erro de paridade** (5)</span><span class="sxs-lookup"><span data-stu-id="df9d9-463">**Parity Error** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Single-Bit_Error"></span><span id="single-bit_error"></span><span id="SINGLE-BIT_ERROR"></span>

<span data-ttu-id="df9d9-464">**Erro de bit único** (6)</span><span class="sxs-lookup"><span data-stu-id="df9d9-464">**Single-Bit Error** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Double-Bit_Error"></span><span id="double-bit_error"></span><span id="DOUBLE-BIT_ERROR"></span>

<span data-ttu-id="df9d9-465">**Erro de bit duplo** (7)</span><span class="sxs-lookup"><span data-stu-id="df9d9-465">**Double-Bit Error** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Multi-Bit_Error"></span><span id="multi-bit_error"></span><span id="MULTI-BIT_ERROR"></span>

<span data-ttu-id="df9d9-466">**Erro de vários bits** (8)</span><span class="sxs-lookup"><span data-stu-id="df9d9-466">**Multi-Bit Error** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Nibble_Error"></span><span id="nibble_error"></span><span id="NIBBLE_ERROR"></span>

<span data-ttu-id="df9d9-467">**Erro de Nibble** (9)</span><span class="sxs-lookup"><span data-stu-id="df9d9-467">**Nibble Error** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Checksum_Error"></span><span id="checksum_error"></span><span id="CHECKSUM_ERROR"></span>

<span data-ttu-id="df9d9-468">**Erro de soma de verificação** (10)</span><span class="sxs-lookup"><span data-stu-id="df9d9-468">**Checksum Error** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="CRC_Error"></span><span id="crc_error"></span><span id="CRC_ERROR"></span>

<span data-ttu-id="df9d9-469">**Erro de CRC** (11)</span><span class="sxs-lookup"><span data-stu-id="df9d9-469">**CRC Error** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="df9d9-470">**Indefinido** (12)</span><span class="sxs-lookup"><span data-stu-id="df9d9-470">**Undefined** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="df9d9-471">**Indefinido** (13)</span><span class="sxs-lookup"><span data-stu-id="df9d9-471">**Undefined** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="df9d9-472">**Indefinido** (14)</span><span class="sxs-lookup"><span data-stu-id="df9d9-472">**Undefined** (14)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="df9d9-473">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="df9d9-473">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df9d9-474">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="df9d9-474">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="df9d9-475">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="df9d9-475">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="df9d9-476">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Matriz de memória física da DMTF \| 1,7 ")</span><span class="sxs-lookup"><span data-stu-id="df9d9-476">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Physical Memory Array\|001.7")</span></span>
</dt> </dl>

<span data-ttu-id="df9d9-477">Detalhes sobre os algoritmos de paridade ou CRC, ECC ou outros mecanismos usados.</span><span class="sxs-lookup"><span data-stu-id="df9d9-477">Details on the parity or CRC algorithms, ECC, or other mechanisms used.</span></span>

<span data-ttu-id="df9d9-478">Essa propriedade é herdada [**da \_ memória CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="df9d9-478">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="df9d9-479">**ErrorResolution**</span><span class="sxs-lookup"><span data-stu-id="df9d9-479">**ErrorResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df9d9-480">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="df9d9-480">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="df9d9-481">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="df9d9-481">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="df9d9-482">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivo de memória DMTF \| 2,21 "," MIF. \|Matriz de memória física da DMTF \| 1,15 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ")</span><span class="sxs-lookup"><span data-stu-id="df9d9-482">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.21", "MIF.DMTF\|Physical Memory Array\|001.15"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="df9d9-483">Intervalo, em bytes, para o qual o último erro pode ser resolvido.</span><span class="sxs-lookup"><span data-stu-id="df9d9-483">Range, in bytes, to which the last error can be resolved.</span></span> <span data-ttu-id="df9d9-484">Por exemplo, se os endereços de erro forem resolvidos para o bit 11 (ou seja, em uma base de página típica), os erros poderão ser resolvidos para os limites de 4 KB e essa propriedade será definida como 4000.</span><span class="sxs-lookup"><span data-stu-id="df9d9-484">For example, if error addresses are resolved to bit 11 (that is, on a typical page basis), then errors can be resolved to 4 KB boundaries and this property is set to 4000.</span></span> <span data-ttu-id="df9d9-485">Se a propriedade **errorInfo** for igual a 3 (OK), essa propriedade não terá significado.</span><span class="sxs-lookup"><span data-stu-id="df9d9-485">If the **ErrorInfo** property is equal to 3 (OK), then this property has no meaning.</span></span>

<span data-ttu-id="df9d9-486">Essa propriedade é herdada [**da \_ memória CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="df9d9-486">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<span data-ttu-id="df9d9-487">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="df9d9-487">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="df9d9-488">**ErrorTime**</span><span class="sxs-lookup"><span data-stu-id="df9d9-488">**ErrorTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df9d9-489">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="df9d9-489">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="df9d9-490">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="df9d9-490">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="df9d9-491">Hora em que ocorreu o último erro de memória.</span><span class="sxs-lookup"><span data-stu-id="df9d9-491">Time that the last memory error occurred.</span></span> <span data-ttu-id="df9d9-492">O tipo de erro é descrito pela propriedade **errorInfo** .</span><span class="sxs-lookup"><span data-stu-id="df9d9-492">The type of error is described by the **ErrorInfo** property.</span></span> <span data-ttu-id="df9d9-493">Se a propriedade **errorInfo** for igual a 3 (OK), essa propriedade não terá significado.</span><span class="sxs-lookup"><span data-stu-id="df9d9-493">If the **ErrorInfo** property is equal to 3 (OK), then this property has no meaning.</span></span>

<span data-ttu-id="df9d9-494">Essa propriedade é herdada [**da \_ memória CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="df9d9-494">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="df9d9-495">**ErrorTransferSize**</span><span class="sxs-lookup"><span data-stu-id="df9d9-495">**ErrorTransferSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df9d9-496">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="df9d9-496">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="df9d9-497">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="df9d9-497">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="df9d9-498">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivo de memória DMTF \| 2,16 "," MIF. \|Matriz de memória física da DMTF \| 1,11 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" bits ")</span><span class="sxs-lookup"><span data-stu-id="df9d9-498">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.16", "MIF.DMTF\|Physical Memory Array\|001.11"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="df9d9-499">Tamanho da transferência de dados em bits que causou o último erro.</span><span class="sxs-lookup"><span data-stu-id="df9d9-499">Size of the data transfer in bits that caused the last error.</span></span> <span data-ttu-id="df9d9-500">0 (zero) indica que não há erro.</span><span class="sxs-lookup"><span data-stu-id="df9d9-500">0 (zero) indicates no error.</span></span> <span data-ttu-id="df9d9-501">Se a propriedade **errorInfo** for igual a 3 (OK), essa propriedade deverá ser definida como 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="df9d9-501">If the **ErrorInfo** property is equal to 3 (OK), then this property should be set to 0 (zero).</span></span>

<span data-ttu-id="df9d9-502">Essa propriedade é herdada [**da \_ memória CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="df9d9-502">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="df9d9-503">**FlushTimer**</span><span class="sxs-lookup"><span data-stu-id="df9d9-503">**FlushTimer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df9d9-504">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="df9d9-504">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="df9d9-505">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="df9d9-505">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="df9d9-506">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Cache do sistema DMTF \| 3,14 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" segundos ")</span><span class="sxs-lookup"><span data-stu-id="df9d9-506">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Cache\|003.14"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("seconds")</span></span>
</dt> </dl>

<span data-ttu-id="df9d9-507">Quantidade máxima de tempo, em segundos, que as linhas sujas ou buckets podem permanecer no cache antes de serem liberados.</span><span class="sxs-lookup"><span data-stu-id="df9d9-507">Maximum amount of time, in seconds, dirty lines or buckets may remain in the cache before they are flushed.</span></span> <span data-ttu-id="df9d9-508">Um valor de 0 (zero) indica que uma liberação de cache não é controlada por um temporizador de liberação.</span><span class="sxs-lookup"><span data-stu-id="df9d9-508">A value of 0 (zero) indicates that a cache flush is not controlled by a flushing timer.</span></span>

<span data-ttu-id="df9d9-509">Essa propriedade é herdada do [**CIM \_ CacheMemory**](cim-cachememory.md).</span><span class="sxs-lookup"><span data-stu-id="df9d9-509">This property is inherited from [**CIM\_CacheMemory**](cim-cachememory.md).</span></span>

</dd> <dt>

<span data-ttu-id="df9d9-510">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="df9d9-510">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df9d9-511">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="df9d9-511">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="df9d9-512">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="df9d9-512">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="df9d9-513">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="df9d9-513">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="df9d9-514">Data e hora em que o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="df9d9-514">Date and time the object was installed.</span></span> <span data-ttu-id="df9d9-515">Essa propriedade não precisa de um valor para indicar que o objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="df9d9-515">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="df9d9-516">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="df9d9-516">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="df9d9-517">**InstalledSize**</span><span class="sxs-lookup"><span data-stu-id="df9d9-517">**InstalledSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df9d9-518">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="df9d9-518">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="df9d9-519">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="df9d9-519">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="df9d9-520">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("tamanho do SMBIOS do \| tipo 7 \| instalado"), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span><span class="sxs-lookup"><span data-stu-id="df9d9-520">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 7\|Installed Size"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="df9d9-521">Tamanho atual da memória de cache instalada.</span><span class="sxs-lookup"><span data-stu-id="df9d9-521">Current size of the installed cache memory.</span></span>

<span data-ttu-id="df9d9-522">Esse valor é proveniente do membro de **Tamanho instalado** da estrutura de **informações de cache** nas informações de SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="df9d9-522">This value comes from the **Installed Size** member of the **Cache Information** structure in the SMBIOS information.</span></span>

</dd> <dt>

<span data-ttu-id="df9d9-523">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="df9d9-523">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df9d9-524">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="df9d9-524">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="df9d9-525">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="df9d9-525">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="df9d9-526">Código do último erro relatado pelo dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="df9d9-526">Last error code reported by the logical device.</span></span>

<span data-ttu-id="df9d9-527">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="df9d9-527">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="df9d9-528">**Level**</span><span class="sxs-lookup"><span data-stu-id="df9d9-528">**Level**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df9d9-529">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="df9d9-529">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="df9d9-530">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="df9d9-530">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="df9d9-531">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Cache do sistema DMTF \| 3,2 ")</span><span class="sxs-lookup"><span data-stu-id="df9d9-531">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Cache\|003.2")</span></span>
</dt> </dl>

<span data-ttu-id="df9d9-532">Nível do cache.</span><span class="sxs-lookup"><span data-stu-id="df9d9-532">Level of the cache.</span></span>

<span data-ttu-id="df9d9-533">Esse valor é proveniente do membro de **configuração de cache** da estrutura de **informações de cache** nas informações de SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="df9d9-533">This value comes from the **Cache Configuration** member of the **Cache Information** structure in the SMBIOS information.</span></span>

<span data-ttu-id="df9d9-534">Essa propriedade é herdada do [**CIM \_ CacheMemory**](cim-cachememory.md).</span><span class="sxs-lookup"><span data-stu-id="df9d9-534">This property is inherited from [**CIM\_CacheMemory**](cim-cachememory.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="df9d9-535"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="df9d9-535"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="df9d9-536"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="df9d9-536"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Primary"></span><span id="primary"></span><span id="PRIMARY"></span>

<span data-ttu-id="df9d9-537"><span id="Primary"></span><span id="primary"></span><span id="PRIMARY"></span>**Primário** (3)</span><span class="sxs-lookup"><span data-stu-id="df9d9-537"><span id="Primary"></span><span id="primary"></span><span id="PRIMARY"></span>**Primary** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Secondary"></span><span id="secondary"></span><span id="SECONDARY"></span>

<span data-ttu-id="df9d9-538"><span id="Secondary"></span><span id="secondary"></span><span id="SECONDARY"></span>**Secundário** (4)</span><span class="sxs-lookup"><span data-stu-id="df9d9-538"><span id="Secondary"></span><span id="secondary"></span><span id="SECONDARY"></span>**Secondary** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Tertiary"></span><span id="tertiary"></span><span id="TERTIARY"></span>

<span data-ttu-id="df9d9-539"><span id="Tertiary"></span><span id="tertiary"></span><span id="TERTIARY"></span>**Terciário** (5)</span><span class="sxs-lookup"><span data-stu-id="df9d9-539"><span id="Tertiary"></span><span id="tertiary"></span><span id="TERTIARY"></span>**Tertiary** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="df9d9-540"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Não aplicável** (6)</span><span class="sxs-lookup"><span data-stu-id="df9d9-540"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="df9d9-541">**Linhas de**</span><span class="sxs-lookup"><span data-stu-id="df9d9-541">**LineSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df9d9-542">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="df9d9-542">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="df9d9-543">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="df9d9-543">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="df9d9-544">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Cache do sistema DMTF \| 3,10 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ")</span><span class="sxs-lookup"><span data-stu-id="df9d9-544">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Cache\|003.10"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="df9d9-545">Tamanho, em bytes, de um único Bucket ou linha de cache.</span><span class="sxs-lookup"><span data-stu-id="df9d9-545">Size, in bytes, of a single cache bucket or line.</span></span>

<span data-ttu-id="df9d9-546">Essa propriedade é herdada do [**CIM \_ CacheMemory**](cim-cachememory.md).</span><span class="sxs-lookup"><span data-stu-id="df9d9-546">This property is inherited from [**CIM\_CacheMemory**](cim-cachememory.md).</span></span>

</dd> <dt>

<span data-ttu-id="df9d9-547">**Localidade**</span><span class="sxs-lookup"><span data-stu-id="df9d9-547">**Location**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df9d9-548">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="df9d9-548">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="df9d9-549">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="df9d9-549">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="df9d9-550">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| local do tipo SMBIOS 7 \| ")</span><span class="sxs-lookup"><span data-stu-id="df9d9-550">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 7\|Location")</span></span>
</dt> </dl>

<span data-ttu-id="df9d9-551">Local físico da memória de cache.</span><span class="sxs-lookup"><span data-stu-id="df9d9-551">Physical location of the cache memory.</span></span>

<span data-ttu-id="df9d9-552">Esse valor é proveniente do membro de **configuração de cache** da estrutura de **informações de cache** nas informações de SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="df9d9-552">This value comes from the **Cache Configuration** member of the **Cache Information** structure in the SMBIOS information.</span></span>

<dt>

<span id="Internal"></span><span id="internal"></span><span id="INTERNAL"></span>

<span data-ttu-id="df9d9-553">**Interno** (0)</span><span class="sxs-lookup"><span data-stu-id="df9d9-553">**Internal** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="External"></span><span id="external"></span><span id="EXTERNAL"></span>

<span data-ttu-id="df9d9-554">**Externo** (1)</span><span class="sxs-lookup"><span data-stu-id="df9d9-554">**External** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="df9d9-555">**Reservado** (2)</span><span class="sxs-lookup"><span data-stu-id="df9d9-555">**Reserved** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="df9d9-556">**Desconhecido** (3)</span><span class="sxs-lookup"><span data-stu-id="df9d9-556">**Unknown** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="df9d9-557">**MaxCacheSize**</span><span class="sxs-lookup"><span data-stu-id="df9d9-557">**MaxCacheSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df9d9-558">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="df9d9-558">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="df9d9-559">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="df9d9-559">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="df9d9-560">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| tamanho máximo de cache do SMBIOS tipo 7 \| "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span><span class="sxs-lookup"><span data-stu-id="df9d9-560">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 7\|Maximum Cache Size"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="df9d9-561">Tamanho máximo de cache instalável nessa memória de cache específica.</span><span class="sxs-lookup"><span data-stu-id="df9d9-561">Maximum cache size installable to this particular cache memory.</span></span>

<span data-ttu-id="df9d9-562">Esse valor é proveniente do membro de **tamanho máximo do cache** da estrutura de **informações do cache** nas informações do SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="df9d9-562">This value comes from the **Maximum Cache Size** member of the **Cache Information** structure in the SMBIOS information.</span></span>

</dd> <dt>

<span data-ttu-id="df9d9-563">**Nome**</span><span class="sxs-lookup"><span data-stu-id="df9d9-563">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df9d9-564">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="df9d9-564">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="df9d9-565">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="df9d9-565">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="df9d9-566">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="df9d9-566">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="df9d9-567">Rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="df9d9-567">Label by which the object is known.</span></span> <span data-ttu-id="df9d9-568">Quando em uma subclasse, a propriedade pode ser substituída para ser uma propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="df9d9-568">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="df9d9-569">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="df9d9-569">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="df9d9-570">**NumberOfBlocks**</span><span class="sxs-lookup"><span data-stu-id="df9d9-570">**NumberOfBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df9d9-571">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="df9d9-571">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="df9d9-572">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="df9d9-572">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="df9d9-573">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| host-REsources-MIB. hrStorageSize ")</span><span class="sxs-lookup"><span data-stu-id="df9d9-573">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageSize")</span></span>
</dt> </dl>

<span data-ttu-id="df9d9-574">Número total de blocos consecutivos, cada um deles bloqueando o tamanho do valor contido na propriedade **BlockSize** , que formam essa extensão de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="df9d9-574">Total number of consecutive blocks, each block the size of the value contained in the **BlockSize** property, which form this storage extent.</span></span> <span data-ttu-id="df9d9-575">O tamanho total da extensão de armazenamento pode ser calculado multiplicando o valor da propriedade **BlockSize** pelo valor dessa propriedade.</span><span class="sxs-lookup"><span data-stu-id="df9d9-575">Total size of the storage extent can be calculated by multiplying the value of the **BlockSize** property by the value of this property.</span></span> <span data-ttu-id="df9d9-576">Se o valor de **BlockSize** for 1, essa propriedade será o tamanho total da extensão de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="df9d9-576">If the value of **BlockSize** is 1, this property is the total size of the storage extent.</span></span>

<span data-ttu-id="df9d9-577">Essa propriedade é herdada do [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="df9d9-577">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="df9d9-578">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="df9d9-578">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="df9d9-579">**OtherErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="df9d9-579">**OtherErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df9d9-580">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="df9d9-580">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="df9d9-581">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="df9d9-581">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="df9d9-582">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ memória CIM**](cim-memory.md).**ErrorInfo**")</span><span class="sxs-lookup"><span data-stu-id="df9d9-582">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Memory**](cim-memory.md).**ErrorInfo**")</span></span>
</dt> </dl>

<span data-ttu-id="df9d9-583">Cadeia de caracteres de forma livre que fornece mais informações se a propriedade **ErrorType** estiver definida como 1, outra.</span><span class="sxs-lookup"><span data-stu-id="df9d9-583">Free-form string providing more information if the **ErrorType** property is set to 1, Other.</span></span> <span data-ttu-id="df9d9-584">Caso contrário, essa cadeia de caracteres não tem significado.</span><span class="sxs-lookup"><span data-stu-id="df9d9-584">Otherwise, this string has no meaning.</span></span>

<span data-ttu-id="df9d9-585">Essa propriedade é herdada [**da \_ memória CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="df9d9-585">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="df9d9-586">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="df9d9-586">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df9d9-587">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="df9d9-587">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="df9d9-588">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="df9d9-588">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="df9d9-589">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="df9d9-589">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="df9d9-590">Identificador de dispositivo do Windows Plug and Play do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="df9d9-590">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="df9d9-591">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="df9d9-591">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="df9d9-592">Exemplo: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="df9d9-592">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="df9d9-593">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="df9d9-593">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df9d9-594">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="df9d9-594">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="df9d9-595">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="df9d9-595">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="df9d9-596">Matriz de recursos específicos relacionados à energia de um dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="df9d9-596">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="df9d9-597">Essa propriedade é herdada **de \_ LogicalDevice CIM**.</span><span class="sxs-lookup"><span data-stu-id="df9d9-597">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="df9d9-598"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="df9d9-598"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="df9d9-599"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="df9d9-599"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="df9d9-600"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Desabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="df9d9-600"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="df9d9-601"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="df9d9-601"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="df9d9-602">Os recursos de gerenciamento de energia estão habilitados no momento, mas o conjunto de recursos exato é desconhecido ou as informações não estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="df9d9-602">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="df9d9-603"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de economia de energia inseridos automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="df9d9-603"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="df9d9-604">O dispositivo pode alterar seu estado de energia com base no uso ou em outros critérios.</span><span class="sxs-lookup"><span data-stu-id="df9d9-604">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="df9d9-605"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energia configurável** (5)</span><span class="sxs-lookup"><span data-stu-id="df9d9-605"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="df9d9-606">Há suporte para o método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="df9d9-606">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="df9d9-607">Esse método é encontrado na classe pai **de \_ LogicalDevice CIM** e pode ser implementado.</span><span class="sxs-lookup"><span data-stu-id="df9d9-607">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="df9d9-608">Para obter mais informações, consulte [Designing formato MOF (MOF) classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="df9d9-608">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="df9d9-609"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energia com suporte** (6)</span><span class="sxs-lookup"><span data-stu-id="df9d9-609"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="df9d9-610">O método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) pode ser invocado com o parâmetro *PowerState* definido como 5 (ciclo de energia).</span><span class="sxs-lookup"><span data-stu-id="df9d9-610">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="df9d9-611"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Energia cronometrada com suporte** (7)</span><span class="sxs-lookup"><span data-stu-id="df9d9-611"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="df9d9-612">Tempo Power-On com suporte</span><span class="sxs-lookup"><span data-stu-id="df9d9-612">Timed Power-On Supported</span></span>

<span data-ttu-id="df9d9-613">O método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) pode ser invocado com o parâmetro *PowerState* definido como 5 (ciclo de energia) e o *tempo* definido como uma data e hora e um intervalo específicos para o Power-on.</span><span class="sxs-lookup"><span data-stu-id="df9d9-613">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="df9d9-614">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="df9d9-614">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df9d9-615">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="df9d9-615">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="df9d9-616">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="df9d9-616">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="df9d9-617">Se **for true**, o dispositivo poderá ser gerenciado por energia (pode ser colocado no modo de suspensão e assim por diante).</span><span class="sxs-lookup"><span data-stu-id="df9d9-617">If **True**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="df9d9-618">A propriedade não indica que os recursos de gerenciamento de energia estão habilitados no momento, apenas que o dispositivo lógico é capaz de gerenciamento de energia.</span><span class="sxs-lookup"><span data-stu-id="df9d9-618">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="df9d9-619">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="df9d9-619">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="df9d9-620">**Finalidade**</span><span class="sxs-lookup"><span data-stu-id="df9d9-620">**Purpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df9d9-621">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="df9d9-621">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="df9d9-622">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="df9d9-622">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="df9d9-623">Cadeia de caracteres de forma livre que descreve a mídia e seu uso.</span><span class="sxs-lookup"><span data-stu-id="df9d9-623">Free-form string describing the media and its use.</span></span>

<span data-ttu-id="df9d9-624">Esse valor é proveniente do membro de **designação de soquete** da estrutura de **informações de cache** nas informações de SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="df9d9-624">This value comes from the **Socket Designation** member of the **Cache Information** structure in the SMBIOS information.</span></span>

<span data-ttu-id="df9d9-625">Essa propriedade é herdada do [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="df9d9-625">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="df9d9-626">**As**</span><span class="sxs-lookup"><span data-stu-id="df9d9-626">**ReadPolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df9d9-627">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="df9d9-627">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="df9d9-628">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="df9d9-628">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="df9d9-629">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Cache do sistema DMTF \| 3,13 ")</span><span class="sxs-lookup"><span data-stu-id="df9d9-629">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Cache\|003.13")</span></span>
</dt> </dl>

<span data-ttu-id="df9d9-630">Política que deve ser empregada pelo cache para lidar com solicitações de leitura.</span><span class="sxs-lookup"><span data-stu-id="df9d9-630">Policy that shall be employed by the cache for handling read requests.</span></span>

<span data-ttu-id="df9d9-631">Essa propriedade é herdada do [**CIM \_ CacheMemory**](cim-cachememory.md).</span><span class="sxs-lookup"><span data-stu-id="df9d9-631">This property is inherited from [**CIM\_CacheMemory**](cim-cachememory.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="df9d9-632">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="df9d9-632">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="df9d9-633">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="df9d9-633">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Read"></span><span id="read"></span><span id="READ"></span>

<span data-ttu-id="df9d9-634">**Leitura** (3)</span><span class="sxs-lookup"><span data-stu-id="df9d9-634">**Read** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Read-Ahead"></span><span id="read-ahead"></span><span id="READ-AHEAD"></span>

<span data-ttu-id="df9d9-635">**Read-Ahead** (4)</span><span class="sxs-lookup"><span data-stu-id="df9d9-635">**Read-Ahead** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Read_and_Read-Ahead"></span><span id="read_and_read-ahead"></span><span id="READ_AND_READ-AHEAD"></span>

<span data-ttu-id="df9d9-636">**Leitura e leitura antecipada** (5)</span><span class="sxs-lookup"><span data-stu-id="df9d9-636">**Read and Read-Ahead** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Determination_Per_I_O"></span><span id="determination_per_i_o"></span><span id="DETERMINATION_PER_I_O"></span>

<span data-ttu-id="df9d9-637">**Determinação por e/s** (6)</span><span class="sxs-lookup"><span data-stu-id="df9d9-637">**Determination Per I/O** (6)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="df9d9-638">**ReplacementPolicy**</span><span class="sxs-lookup"><span data-stu-id="df9d9-638">**ReplacementPolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df9d9-639">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="df9d9-639">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="df9d9-640">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="df9d9-640">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="df9d9-641">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Cache do sistema DMTF \| 3,12 ")</span><span class="sxs-lookup"><span data-stu-id="df9d9-641">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Cache\|003.12")</span></span>
</dt> </dl>

<span data-ttu-id="df9d9-642">Algoritmo para determinar quais linhas de cache ou buckets devem ser reutilizados.</span><span class="sxs-lookup"><span data-stu-id="df9d9-642">Algorithm to determine which cache lines or buckets should be reused.</span></span>

<span data-ttu-id="df9d9-643">Essa propriedade é herdada do [**CIM \_ CacheMemory**](cim-cachememory.md).</span><span class="sxs-lookup"><span data-stu-id="df9d9-643">This property is inherited from [**CIM\_CacheMemory**](cim-cachememory.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="df9d9-644">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="df9d9-644">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="df9d9-645">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="df9d9-645">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Least_Recently_Used__LRU_"></span><span id="least_recently_used__lru_"></span><span id="LEAST_RECENTLY_USED__LRU_"></span>

<span data-ttu-id="df9d9-646">**Menos usado recentemente (LRU)** (3)</span><span class="sxs-lookup"><span data-stu-id="df9d9-646">**Least Recently Used (LRU)** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="First_In_First_Out__FIFO_"></span><span id="first_in_first_out__fifo_"></span><span id="FIRST_IN_FIRST_OUT__FIFO_"></span>

<span data-ttu-id="df9d9-647">**Primeiro a entrar, primeiro a sair (FIFO)** (4)</span><span class="sxs-lookup"><span data-stu-id="df9d9-647">**First In First Out (FIFO)** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Last_In_First_Out__LIFO_"></span><span id="last_in_first_out__lifo_"></span><span id="LAST_IN_FIRST_OUT__LIFO_"></span>

<span data-ttu-id="df9d9-648">**Último a entrar, primeiro a sair (UEPS)** (5)</span><span class="sxs-lookup"><span data-stu-id="df9d9-648">**Last In First Out (LIFO)** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Least_Frequently_Used__LFU_"></span><span id="least_frequently_used__lfu_"></span><span id="LEAST_FREQUENTLY_USED__LFU_"></span>

<span data-ttu-id="df9d9-649">**Usado com menos frequência (LFU)** (6)</span><span class="sxs-lookup"><span data-stu-id="df9d9-649">**Least Frequently Used (LFU)** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Most_Frequently_Used__MFU_"></span><span id="most_frequently_used__mfu_"></span><span id="MOST_FREQUENTLY_USED__MFU_"></span>

<span data-ttu-id="df9d9-650">**Usado com mais frequência (MFU)** (7)</span><span class="sxs-lookup"><span data-stu-id="df9d9-650">**Most Frequently Used (MFU)** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Data_Dependent_Multiple_Algorithms"></span><span id="data_dependent_multiple_algorithms"></span><span id="DATA_DEPENDENT_MULTIPLE_ALGORITHMS"></span>

<span data-ttu-id="df9d9-651">**Algoritmos múltiplos dependentes de dados** (8)</span><span class="sxs-lookup"><span data-stu-id="df9d9-651">**Data Dependent Multiple Algorithms** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="df9d9-652">**StartingAddress**</span><span class="sxs-lookup"><span data-stu-id="df9d9-652">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df9d9-653">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="df9d9-653">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="df9d9-654">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="df9d9-654">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="df9d9-655">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. Os \| endereços mapeados da matriz de memória DMTF \| 1,3 "," MIF. \|Endereços mapeados do dispositivo \| de memória DMTF 1,4 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" kilobytes ")</span><span class="sxs-lookup"><span data-stu-id="df9d9-655">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Array Mapped Addresses\|001.3", "MIF.DMTF\|Memory Device Mapped Addresses\|001.4"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="df9d9-656">Endereço inicial, referenciado por um aplicativo ou sistema operacional e mapeado por um controlador de memória, para esse objeto de memória.</span><span class="sxs-lookup"><span data-stu-id="df9d9-656">Beginning address, referenced by an application or operating system and mapped by a memory controller, for this memory object.</span></span> <span data-ttu-id="df9d9-657">O endereço inicial é especificado em kilobytes.</span><span class="sxs-lookup"><span data-stu-id="df9d9-657">The starting address is specified in kilobytes.</span></span>

<span data-ttu-id="df9d9-658">Essa propriedade é herdada [**da \_ memória CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="df9d9-658">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<span data-ttu-id="df9d9-659">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="df9d9-659">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="df9d9-660">**Status**</span><span class="sxs-lookup"><span data-stu-id="df9d9-660">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df9d9-661">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="df9d9-661">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="df9d9-662">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="df9d9-662">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="df9d9-663">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="df9d9-663">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="df9d9-664">Status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="df9d9-664">Current status of the object.</span></span> <span data-ttu-id="df9d9-665">Vários status de operação e não operacional podem ser definidos.</span><span class="sxs-lookup"><span data-stu-id="df9d9-665">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="df9d9-666">Os status operacionais incluem: "OK", "degradado" e "Pred falha" (um elemento, como uma unidade de disco rígido habilitado para inteligente, pode estar funcionando corretamente, mas prevendo uma falha em um futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="df9d9-666">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="df9d9-667">Os status não operacionais incluem: "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="df9d9-667">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="df9d9-668">O último, "Service", pode ser aplicado durante o espelhamento de espelho de um disco, recarregar uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="df9d9-668">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="df9d9-669">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="df9d9-669">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="df9d9-670">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="df9d9-670">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="df9d9-671">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="df9d9-671">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="df9d9-672">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="df9d9-672">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="df9d9-673">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="df9d9-673">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="df9d9-674">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="df9d9-674">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="df9d9-675">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="df9d9-675">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="df9d9-676">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="df9d9-676">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="df9d9-677">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="df9d9-677">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="df9d9-678">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="df9d9-678">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="df9d9-679">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="df9d9-679">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="df9d9-680">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="df9d9-680">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="df9d9-681">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="df9d9-681">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="df9d9-682">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="df9d9-682">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="df9d9-683">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="df9d9-683">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="df9d9-684">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="df9d9-684">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df9d9-685">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="df9d9-685">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="df9d9-686">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="df9d9-686">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="df9d9-687">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operacional da DMTF \| 3,3 ")</span><span class="sxs-lookup"><span data-stu-id="df9d9-687">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="df9d9-688">Estado do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="df9d9-688">State of the logical device.</span></span> <span data-ttu-id="df9d9-689">Se essa propriedade não se aplicar ao dispositivo lógico, o valor 5 (não aplicável) deverá ser usado.</span><span class="sxs-lookup"><span data-stu-id="df9d9-689">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="df9d9-690">Esse valor é proveniente do membro de **configuração de cache** da estrutura de **informações de cache** nas informações de SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="df9d9-690">This value comes from the **Cache Configuration** member of the **Cache Information** structure in the SMBIOS information.</span></span>

<span data-ttu-id="df9d9-691">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="df9d9-691">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="df9d9-692">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="df9d9-692">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="df9d9-693">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="df9d9-693">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="df9d9-694">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="df9d9-694">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="df9d9-695">**Desabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="df9d9-695">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="df9d9-696">**Não aplicável** (5)</span><span class="sxs-lookup"><span data-stu-id="df9d9-696">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="df9d9-697">**SupportedSRAM**</span><span class="sxs-lookup"><span data-stu-id="df9d9-697">**SupportedSRAM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df9d9-698">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="df9d9-698">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="df9d9-699">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="df9d9-699">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="df9d9-700">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| tipo de SRAM com suporte do tipo de SMBIOS 7 \| ")</span><span class="sxs-lookup"><span data-stu-id="df9d9-700">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 7\|Supported SRAM Type")</span></span>
</dt> </dl>

<span data-ttu-id="df9d9-701">Matriz de tipos com suporte de memória estática de acesso aleatório (SRAM) que pode ser usada para a memória de cache.</span><span class="sxs-lookup"><span data-stu-id="df9d9-701">Array of supported types of Static Random Access Memory (SRAM) that can be used for the cache memory.</span></span>

<span data-ttu-id="df9d9-702">Esse valor é proveniente do membro de **tipo de SRAM com suporte** da estrutura de **informações de cache** nas informações de SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="df9d9-702">This value comes from the **Supported SRAM Type** member of the **Cache Information** structure in the SMBIOS information.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="df9d9-703">**Outro** (0)</span><span class="sxs-lookup"><span data-stu-id="df9d9-703">**Other** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="df9d9-704">**Desconhecido** (1)</span><span class="sxs-lookup"><span data-stu-id="df9d9-704">**Unknown** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Non-Burst"></span><span id="non-burst"></span><span id="NON-BURST"></span>

<span data-ttu-id="df9d9-705">**Não intermitente** (2)</span><span class="sxs-lookup"><span data-stu-id="df9d9-705">**Non-Burst** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Burst"></span><span id="burst"></span><span id="BURST"></span>

<span data-ttu-id="df9d9-706">**Intermitência** (3)</span><span class="sxs-lookup"><span data-stu-id="df9d9-706">**Burst** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Pipeline_Burst"></span><span id="pipeline_burst"></span><span id="PIPELINE_BURST"></span>

<span data-ttu-id="df9d9-707">**Disparo de pipeline** (4)</span><span class="sxs-lookup"><span data-stu-id="df9d9-707">**Pipeline Burst** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Synchronous"></span><span id="synchronous"></span><span id="SYNCHRONOUS"></span>

<span data-ttu-id="df9d9-708">**Síncrono** (5)</span><span class="sxs-lookup"><span data-stu-id="df9d9-708">**Synchronous** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Asynchronous"></span><span id="asynchronous"></span><span id="ASYNCHRONOUS"></span>

<span data-ttu-id="df9d9-709">**Assíncrono** (6)</span><span class="sxs-lookup"><span data-stu-id="df9d9-709">**Asynchronous** (6)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="df9d9-710">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="df9d9-710">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df9d9-711">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="df9d9-711">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="df9d9-712">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="df9d9-712">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="df9d9-713">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="df9d9-713">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="df9d9-714">Valor da propriedade **CreationClassName** do computador de escopo.</span><span class="sxs-lookup"><span data-stu-id="df9d9-714">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="df9d9-715">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="df9d9-715">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="df9d9-716">**SystemLevelAddress**</span><span class="sxs-lookup"><span data-stu-id="df9d9-716">**SystemLevelAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df9d9-717">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="df9d9-717">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="df9d9-718">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="df9d9-718">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="df9d9-719">Se **for true**, as informações de endereço na propriedade **ErrorAddress** serão um endereço de nível de sistema.</span><span class="sxs-lookup"><span data-stu-id="df9d9-719">If **True**, the address information in the property **ErrorAddress** is a system-level address.</span></span> <span data-ttu-id="df9d9-720">Se for **false**, será um endereço físico.</span><span class="sxs-lookup"><span data-stu-id="df9d9-720">If **False**, it is a physical address.</span></span> <span data-ttu-id="df9d9-721">Se a propriedade **errorInfo** for igual a 3, essa propriedade não terá significado.</span><span class="sxs-lookup"><span data-stu-id="df9d9-721">If the **ErrorInfo** property is equal to 3, then this property has no meaning.</span></span>

<span data-ttu-id="df9d9-722">Essa propriedade é herdada [**da \_ memória CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="df9d9-722">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="df9d9-723">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="df9d9-723">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df9d9-724">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="df9d9-724">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="df9d9-725">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="df9d9-725">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="df9d9-726">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**Name**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="df9d9-726">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="df9d9-727">Nome do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="df9d9-727">Name of the scoping system.</span></span>

<span data-ttu-id="df9d9-728">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="df9d9-728">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="df9d9-729">**WritePolicy**</span><span class="sxs-lookup"><span data-stu-id="df9d9-729">**WritePolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df9d9-730">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="df9d9-730">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="df9d9-731">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="df9d9-731">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="df9d9-732">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Cache do sistema DMTF \| 3,5 ")</span><span class="sxs-lookup"><span data-stu-id="df9d9-732">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Cache\|003.5")</span></span>
</dt> </dl>

<span data-ttu-id="df9d9-733">Gravar definição de política.</span><span class="sxs-lookup"><span data-stu-id="df9d9-733">Write policy definition.</span></span>

<span data-ttu-id="df9d9-734">Esse valor é proveniente do membro de **configuração de cache** da estrutura de **informações de cache** nas informações de SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="df9d9-734">This value comes from the **Cache Configuration** member of the **Cache Information** structure in the SMBIOS information.</span></span>

<span data-ttu-id="df9d9-735">Essa propriedade é herdada do [**CIM \_ CacheMemory**](cim-cachememory.md).</span><span class="sxs-lookup"><span data-stu-id="df9d9-735">This property is inherited from [**CIM\_CacheMemory**](cim-cachememory.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="df9d9-736">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="df9d9-736">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="df9d9-737">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="df9d9-737">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Write_Back"></span><span id="write_back"></span><span id="WRITE_BACK"></span>

<span data-ttu-id="df9d9-738">**Write-back** (3)</span><span class="sxs-lookup"><span data-stu-id="df9d9-738">**Write Back** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write_Through"></span><span id="write_through"></span><span id="WRITE_THROUGH"></span>

<span data-ttu-id="df9d9-739">**Gravação por** (4)</span><span class="sxs-lookup"><span data-stu-id="df9d9-739">**Write Through** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Varies_with_Address"></span><span id="varies_with_address"></span><span id="VARIES_WITH_ADDRESS"></span>

<span data-ttu-id="df9d9-740">**Varia de acordo com o endereço** (5)</span><span class="sxs-lookup"><span data-stu-id="df9d9-740">**Varies with Address** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Determination_Per_I_O"></span><span id="determination_per_i_o"></span><span id="DETERMINATION_PER_I_O"></span>

<span data-ttu-id="df9d9-741">**Determinação por e/s** (6)</span><span class="sxs-lookup"><span data-stu-id="df9d9-741">**Determination Per I/O** (6)</span></span>


<span data-ttu-id="df9d9-742"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="df9d9-742"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="df9d9-743">Comentários</span><span class="sxs-lookup"><span data-stu-id="df9d9-743">Remarks</span></span>

<span data-ttu-id="df9d9-744">A classe **Win32 \_ CacheMemory** é derivada de [**CIM \_ CacheMemory**](cim-cachememory.md).</span><span class="sxs-lookup"><span data-stu-id="df9d9-744">The **Win32\_CacheMemory** class is derived from [**CIM\_CacheMemory**](cim-cachememory.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="df9d9-745">Requisitos</span><span class="sxs-lookup"><span data-stu-id="df9d9-745">Requirements</span></span>



| <span data-ttu-id="df9d9-746">Requisito</span><span class="sxs-lookup"><span data-stu-id="df9d9-746">Requirement</span></span> | <span data-ttu-id="df9d9-747">Valor</span><span class="sxs-lookup"><span data-stu-id="df9d9-747">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="df9d9-748">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="df9d9-748">Minimum supported client</span></span><br/> | <span data-ttu-id="df9d9-749">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="df9d9-749">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="df9d9-750">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="df9d9-750">Minimum supported server</span></span><br/> | <span data-ttu-id="df9d9-751">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="df9d9-751">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="df9d9-752">Namespace</span><span class="sxs-lookup"><span data-stu-id="df9d9-752">Namespace</span></span><br/>                | <span data-ttu-id="df9d9-753">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="df9d9-753">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="df9d9-754">MOF</span><span class="sxs-lookup"><span data-stu-id="df9d9-754">MOF</span></span><br/>                      | <dl> <span data-ttu-id="df9d9-755"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="df9d9-755"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="df9d9-756">DLL</span><span class="sxs-lookup"><span data-stu-id="df9d9-756">DLL</span></span><br/>                      | <dl> <span data-ttu-id="df9d9-757"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="df9d9-757"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="df9d9-758">Confira também</span><span class="sxs-lookup"><span data-stu-id="df9d9-758">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df9d9-759">**\_CACHEMEMORY CIM**</span><span class="sxs-lookup"><span data-stu-id="df9d9-759">**CIM\_CacheMemory**</span></span>](cim-cachememory.md)
</dt> <dt>

[<span data-ttu-id="df9d9-760">Classes de hardware do sistema de computador</span><span class="sxs-lookup"><span data-stu-id="df9d9-760">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

