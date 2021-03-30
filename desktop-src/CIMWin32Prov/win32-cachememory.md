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
# <a name="win32_cachememory-class"></a><span data-ttu-id="10d37-103">\_Classe Win32 CacheMemory</span><span class="sxs-lookup"><span data-stu-id="10d37-103">Win32\_CacheMemory class</span></span>

<span data-ttu-id="10d37-104">A [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ CacheMemory do Win32** representa a memória de cache interna e externa em um sistema de computador.</span><span class="sxs-lookup"><span data-stu-id="10d37-104">The **Win32\_CacheMemory** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents internal and external cache memory on a computer system.</span></span>

<span data-ttu-id="10d37-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="10d37-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="10d37-106">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="10d37-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="10d37-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="10d37-107">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="10d37-108">Membros</span><span class="sxs-lookup"><span data-stu-id="10d37-108">Members</span></span>

<span data-ttu-id="10d37-109">A classe **Win32 \_ CacheMemory** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="10d37-109">The **Win32\_CacheMemory** class has these types of members:</span></span>

-   [<span data-ttu-id="10d37-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="10d37-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="10d37-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="10d37-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="10d37-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="10d37-112">Methods</span></span>

<span data-ttu-id="10d37-113">A classe **Win32 \_ CacheMemory** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="10d37-113">The **Win32\_CacheMemory** class has these methods.</span></span>



| <span data-ttu-id="10d37-114">Método</span><span class="sxs-lookup"><span data-stu-id="10d37-114">Method</span></span>            | <span data-ttu-id="10d37-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="10d37-115">Description</span></span>                                                                                                                                                                                                  |
|:------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="10d37-116">**Redefinir**</span><span class="sxs-lookup"><span data-stu-id="10d37-116">**Reset**</span></span>         | <span data-ttu-id="10d37-117">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="10d37-117">Not implemented.</span></span> <span data-ttu-id="10d37-118">Para implementar esse método, consulte o método [**Reset**](reset-method-in-class-cim-controller.md) no [**CIM \_ CacheMemory**](cim-cachememory.md) para obter a documentação.</span><span class="sxs-lookup"><span data-stu-id="10d37-118">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_CacheMemory**](cim-cachememory.md) for documentation.</span></span><br/>                 |
| <span data-ttu-id="10d37-119">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="10d37-119">**SetPowerState**</span></span> | <span data-ttu-id="10d37-120">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="10d37-120">Not implemented.</span></span> <span data-ttu-id="10d37-121">Para implementar esse método, consulte o método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) no [**CIM \_ CacheMemory**](cim-cachememory.md) para obter a documentação.</span><span class="sxs-lookup"><span data-stu-id="10d37-121">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_CacheMemory**](cim-cachememory.md) for documentation.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="10d37-122">Propriedades</span><span class="sxs-lookup"><span data-stu-id="10d37-122">Properties</span></span>

<span data-ttu-id="10d37-123">A classe **Win32 \_ CacheMemory** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="10d37-123">The **Win32\_CacheMemory** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="10d37-124">**Acesso**</span><span class="sxs-lookup"><span data-stu-id="10d37-124">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10d37-125">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="10d37-125">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="10d37-126">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="10d37-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="10d37-127">Tipo de acesso.</span><span class="sxs-lookup"><span data-stu-id="10d37-127">Type of access.</span></span>

<span data-ttu-id="10d37-128">Essa propriedade é herdada do [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="10d37-128">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="10d37-129"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="10d37-129"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>

<span data-ttu-id="10d37-130"><span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>**Legível** (1)</span><span class="sxs-lookup"><span data-stu-id="10d37-130"><span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>**Readable** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>

<span data-ttu-id="10d37-131"><span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>**Gravável** (2)</span><span class="sxs-lookup"><span data-stu-id="10d37-131"><span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>**Writeable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="10d37-132">Gravável</span><span class="sxs-lookup"><span data-stu-id="10d37-132">Writable</span></span>

</dd> <dt>

<span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>

<span data-ttu-id="10d37-133"><span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>**Suporte de leitura/gravação** (3)</span><span class="sxs-lookup"><span data-stu-id="10d37-133"><span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>**Read/Write Supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>

<span data-ttu-id="10d37-134"><span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>**Gravar uma vez** (4)</span><span class="sxs-lookup"><span data-stu-id="10d37-134"><span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>**Write Once** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="10d37-135">**AdditionalErrorData**</span><span class="sxs-lookup"><span data-stu-id="10d37-135">**AdditionalErrorData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10d37-136">Tipo de dados: matriz **uint8**</span><span class="sxs-lookup"><span data-stu-id="10d37-136">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="10d37-137">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="10d37-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10d37-138">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivo de memória DMTF \| 2,18 "," MIF. \|Matriz de memória física da DMTF \| 1,13 "), [**máx**](/windows/desktop/WmiSdk/standard-qualifiers) . (64)</span><span class="sxs-lookup"><span data-stu-id="10d37-138">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.18", "MIF.DMTF\|Physical Memory Array\|001.13"), [**MAX**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="10d37-139">Matriz de octetos que contém informações de erro adicionais.</span><span class="sxs-lookup"><span data-stu-id="10d37-139">Array of octets that hold additional error information.</span></span> <span data-ttu-id="10d37-140">Um exemplo é a síndrome de ECC ou o retorno dos bits de verificação se uma metodologia de erro baseada em CRC for usada.</span><span class="sxs-lookup"><span data-stu-id="10d37-140">An example is ECC Syndrome or the return of the check bits if a CRC-based error methodology is used.</span></span> <span data-ttu-id="10d37-141">No último caso, se um erro de bit único for reconhecido e o algoritmo CRC for conhecido, será possível determinar o bit exato que falhou.</span><span class="sxs-lookup"><span data-stu-id="10d37-141">In the latter case, if a single-bit error is recognized and the CRC algorithm is known, it is possible to determine the exact bit that failed.</span></span> <span data-ttu-id="10d37-142">Esse tipo de dados (síndrome de ECC, bit de verificação, dados de bits de paridade ou outras informações fornecidas pelo fornecedor) está incluído neste campo.</span><span class="sxs-lookup"><span data-stu-id="10d37-142">This type of data (ECC Syndrome, Check Bit, Parity Bit data, or other vendor supplied information) is included in this field.</span></span> <span data-ttu-id="10d37-143">Se a propriedade **errorInfo** for igual a 3 (OK), essa propriedade não terá significado.</span><span class="sxs-lookup"><span data-stu-id="10d37-143">If the **ErrorInfo** property is equal to 3 (OK), then this property has no meaning.</span></span>

<span data-ttu-id="10d37-144">Essa propriedade é herdada [**da \_ memória CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="10d37-144">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="10d37-145">**Capacidade de associação**</span><span class="sxs-lookup"><span data-stu-id="10d37-145">**Associativity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10d37-146">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="10d37-146">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="10d37-147">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="10d37-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10d37-148">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Cache do sistema DMTF \| 3,15 ")</span><span class="sxs-lookup"><span data-stu-id="10d37-148">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Cache\|003.15")</span></span>
</dt> </dl>

<span data-ttu-id="10d37-149">Uma enumeração de inteiros que define a associação de cache do sistema.</span><span class="sxs-lookup"><span data-stu-id="10d37-149">An integer enumeration that defines the system cache associativity.</span></span>

<span data-ttu-id="10d37-150">Esse valor é proveniente do membro de **Associação** da estrutura de **informações de cache** nas informações de SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="10d37-150">This value comes from the **Associativity** member of the **Cache Information** structure in the SMBIOS information.</span></span>

<span data-ttu-id="10d37-151">Essa propriedade é herdada do [**CIM \_ CacheMemory**](cim-cachememory.md).</span><span class="sxs-lookup"><span data-stu-id="10d37-151">This property is inherited from [**CIM\_CacheMemory**](cim-cachememory.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="10d37-152">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="10d37-152">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="10d37-153">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="10d37-153">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Direct_Mapped"></span><span id="direct_mapped"></span><span id="DIRECT_MAPPED"></span>

<span data-ttu-id="10d37-154">**Mapeado direto** (3)</span><span class="sxs-lookup"><span data-stu-id="10d37-154">**Direct Mapped** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="2-way_Set-Associative"></span><span id="2-way_set-associative"></span><span id="2-WAY_SET-ASSOCIATIVE"></span>

<span data-ttu-id="10d37-155">**conjunto de 2 vias-associativo** (4)</span><span class="sxs-lookup"><span data-stu-id="10d37-155">**2-way Set-Associative** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="4-way_Set-Associative"></span><span id="4-way_set-associative"></span><span id="4-WAY_SET-ASSOCIATIVE"></span>

<span data-ttu-id="10d37-156">**conjunto de 4 vias-associativo** (5)</span><span class="sxs-lookup"><span data-stu-id="10d37-156">**4-way Set-Associative** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Fully_Associative"></span><span id="fully_associative"></span><span id="FULLY_ASSOCIATIVE"></span>

<span data-ttu-id="10d37-157">**Totalmente associativo** (6)</span><span class="sxs-lookup"><span data-stu-id="10d37-157">**Fully Associative** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="8-way_Set-Associative"></span><span id="8-way_set-associative"></span><span id="8-WAY_SET-ASSOCIATIVE"></span>

<span data-ttu-id="10d37-158">**conjunto de 8 vias – associativo** (7)</span><span class="sxs-lookup"><span data-stu-id="10d37-158">**8-way Set-Associative** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="16-way_Set-Associative"></span><span id="16-way_set-associative"></span><span id="16-WAY_SET-ASSOCIATIVE"></span>

<span data-ttu-id="10d37-159">**conjunto de 16 vias – associativo** (8)</span><span class="sxs-lookup"><span data-stu-id="10d37-159">**16-way Set-Associative** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="10d37-160">**Disponibilidade**</span><span class="sxs-lookup"><span data-stu-id="10d37-160">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10d37-161">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="10d37-161">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="10d37-162">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="10d37-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10d37-163">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operacional da DMTF \| 3,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="10d37-163">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="10d37-164">Disponibilidade e status do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="10d37-164">Availability and status of the device.</span></span>

<span data-ttu-id="10d37-165">Esse valor é proveniente do membro de **configuração de cache** da estrutura de **informações de cache** nas informações de SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="10d37-165">This value comes from the **Cache Configuration** member of the **Cache Information** structure in the SMBIOS information.</span></span>

<span data-ttu-id="10d37-166">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="10d37-166">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="10d37-167"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="10d37-167"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="10d37-168"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="10d37-168"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="10d37-169"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Execução/energia completa** (3)</span><span class="sxs-lookup"><span data-stu-id="10d37-169"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="10d37-170">Energia completa ou em execução</span><span class="sxs-lookup"><span data-stu-id="10d37-170">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="10d37-171"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Aviso** (4)</span><span class="sxs-lookup"><span data-stu-id="10d37-171"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="10d37-172"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Em teste** (5)</span><span class="sxs-lookup"><span data-stu-id="10d37-172"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="10d37-173"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Não aplicável** (6)</span><span class="sxs-lookup"><span data-stu-id="10d37-173"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="10d37-174"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desligar (7** )</span><span class="sxs-lookup"><span data-stu-id="10d37-174"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="10d37-175"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off line** (8)</span><span class="sxs-lookup"><span data-stu-id="10d37-175"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="10d37-176"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fora do imposto** (9)</span><span class="sxs-lookup"><span data-stu-id="10d37-176"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="10d37-177"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="10d37-177"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="10d37-178"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Não instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="10d37-178"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="10d37-179"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Erro de instalação** (12)</span><span class="sxs-lookup"><span data-stu-id="10d37-179"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="10d37-180"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Economia **de energia-desconhecido** (13)</span><span class="sxs-lookup"><span data-stu-id="10d37-180"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="10d37-181">O dispositivo é conhecido por estar em um modo de economia de energia, mas seu status exato é desconhecido.</span><span class="sxs-lookup"><span data-stu-id="10d37-181">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="10d37-182"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Economia **de energia-modo de baixa energia** (14)</span><span class="sxs-lookup"><span data-stu-id="10d37-182"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="10d37-183">O dispositivo está em um estado de economia de energia, mas ainda está funcionando e pode exibir o desempenho degradado.</span><span class="sxs-lookup"><span data-stu-id="10d37-183">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="10d37-184"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save-em espera** (15)</span><span class="sxs-lookup"><span data-stu-id="10d37-184"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="10d37-185">O dispositivo não está funcionando, mas pode ser levado a uma potência completa rapidamente.</span><span class="sxs-lookup"><span data-stu-id="10d37-185">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="10d37-186"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energia** (16)</span><span class="sxs-lookup"><span data-stu-id="10d37-186"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="10d37-187"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Economia **de energia-aviso** (17)</span><span class="sxs-lookup"><span data-stu-id="10d37-187"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="10d37-188">O dispositivo está em um estado de aviso, embora também esteja em um modo de economia de energia.</span><span class="sxs-lookup"><span data-stu-id="10d37-188">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="10d37-189"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>Em **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="10d37-189"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="10d37-190">O dispositivo está em pausa.</span><span class="sxs-lookup"><span data-stu-id="10d37-190">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="10d37-191"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Não pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="10d37-191"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="10d37-192">O dispositivo não está pronto.</span><span class="sxs-lookup"><span data-stu-id="10d37-192">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="10d37-193"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Não configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="10d37-193"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="10d37-194">O dispositivo não está configurado.</span><span class="sxs-lookup"><span data-stu-id="10d37-194">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="10d37-195"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Desativado** (21)</span><span class="sxs-lookup"><span data-stu-id="10d37-195"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="10d37-196">O dispositivo está silencioso.</span><span class="sxs-lookup"><span data-stu-id="10d37-196">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="10d37-197">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="10d37-197">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10d37-198">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="10d37-198">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="10d37-199">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="10d37-199">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10d37-200">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| host-REsources-MIB. hrStorageAllocationUnits "), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ")</span><span class="sxs-lookup"><span data-stu-id="10d37-200">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageAllocationUnits"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="10d37-201">Tamanho em bytes dos blocos que formam esta extensão de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="10d37-201">Size in bytes of the blocks that form this storage extent.</span></span> <span data-ttu-id="10d37-202">Se for desconhecido ou se um conceito de bloco não for válido (por exemplo, para extensões de agregação, memória ou discos lógicos), insira 1.</span><span class="sxs-lookup"><span data-stu-id="10d37-202">If unknown or if a block concept is not valid (for example, for aggregate extents, memory, or logical disks), enter a 1.</span></span>

<span data-ttu-id="10d37-203">Essa propriedade é herdada do [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="10d37-203">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="10d37-204">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="10d37-204">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="10d37-205">**CacheSpeed**</span><span class="sxs-lookup"><span data-stu-id="10d37-205">**CacheSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10d37-206">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="10d37-206">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="10d37-207">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="10d37-207">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10d37-208">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| velocidade de cache do tipo SMBIOS 7 \| "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("nanossegundos")</span><span class="sxs-lookup"><span data-stu-id="10d37-208">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 7\|Cache Speed"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("nanoseconds")</span></span>
</dt> </dl>

<span data-ttu-id="10d37-209">Velocidade do cache.</span><span class="sxs-lookup"><span data-stu-id="10d37-209">Speed of the cache.</span></span>

<span data-ttu-id="10d37-210">Esse valor é proveniente do membro de **velocidade de cache** da estrutura de **informações de cache** nas informações de SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="10d37-210">This value comes from the **Cache Speed** member of the **Cache Information** structure in the SMBIOS information.</span></span>

</dd> <dt>

<span data-ttu-id="10d37-211">**CacheType**</span><span class="sxs-lookup"><span data-stu-id="10d37-211">**CacheType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10d37-212">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="10d37-212">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="10d37-213">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="10d37-213">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10d37-214">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Cache do sistema DMTF \| 3,9 ")</span><span class="sxs-lookup"><span data-stu-id="10d37-214">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Cache\|003.9")</span></span>
</dt> </dl>

<span data-ttu-id="10d37-215">Tipo de cache.</span><span class="sxs-lookup"><span data-stu-id="10d37-215">Type of cache.</span></span>

<span data-ttu-id="10d37-216">Esse valor é proveniente do membro do **tipo de cache System** da estrutura de **informações do cache** nas informações do SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="10d37-216">This value comes from the **System Cache Type** member of the **Cache Information** structure in the SMBIOS information.</span></span>

<span data-ttu-id="10d37-217">Essa propriedade é herdada do [**CIM \_ CacheMemory**](cim-cachememory.md).</span><span class="sxs-lookup"><span data-stu-id="10d37-217">This property is inherited from [**CIM\_CacheMemory**](cim-cachememory.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="10d37-218">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="10d37-218">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="10d37-219">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="10d37-219">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Instruction"></span><span id="instruction"></span><span id="INSTRUCTION"></span>

<span data-ttu-id="10d37-220">**Instrução** (3)</span><span class="sxs-lookup"><span data-stu-id="10d37-220">**Instruction** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Data"></span><span id="data"></span><span id="DATA"></span>

<span data-ttu-id="10d37-221">**Dados** (4)</span><span class="sxs-lookup"><span data-stu-id="10d37-221">**Data** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Unified"></span><span id="unified"></span><span id="UNIFIED"></span>

<span data-ttu-id="10d37-222">**Unificado** (5)</span><span class="sxs-lookup"><span data-stu-id="10d37-222">**Unified** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="10d37-223">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="10d37-223">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10d37-224">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="10d37-224">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="10d37-225">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="10d37-225">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10d37-226">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="10d37-226">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="10d37-227">Breve descrição do objeto de uma cadeia de caracteres de uma linha.</span><span class="sxs-lookup"><span data-stu-id="10d37-227">Short description of the object a one-line string.</span></span>

<span data-ttu-id="10d37-228">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="10d37-228">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="10d37-229">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="10d37-229">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10d37-230">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="10d37-230">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="10d37-231">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="10d37-231">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10d37-232">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="10d37-232">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="10d37-233">Código de erro do Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="10d37-233">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="10d37-234">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="10d37-234">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="10d37-235"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Este dispositivo está funcionando corretamente.**</span><span class="sxs-lookup"><span data-stu-id="10d37-235"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="10d37-236"> acima (0)</span><span class="sxs-lookup"><span data-stu-id="10d37-236">(0)</span></span>


</dt> <dd>

<span data-ttu-id="10d37-237">O dispositivo está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="10d37-237">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="10d37-238"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Este dispositivo não está configurado corretamente.**</span><span class="sxs-lookup"><span data-stu-id="10d37-238"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="10d37-239">(1)</span><span class="sxs-lookup"><span data-stu-id="10d37-239">(1)</span></span>


</dt> <dd>

<span data-ttu-id="10d37-240">O dispositivo não está configurado corretamente.</span><span class="sxs-lookup"><span data-stu-id="10d37-240">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="10d37-241"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**O Windows não pode carregar o driver para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="10d37-241"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="10d37-242">(2)</span><span class="sxs-lookup"><span data-stu-id="10d37-242">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="10d37-243"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**O driver para este dispositivo pode estar corrompido ou o sistema pode estar com pouca memória ou outros recursos.**</span><span class="sxs-lookup"><span data-stu-id="10d37-243"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="10d37-244">(3)</span><span class="sxs-lookup"><span data-stu-id="10d37-244">(3)</span></span>


</dt> <dd>

<span data-ttu-id="10d37-245">O driver para este dispositivo pode estar corrompido ou o sistema pode estar com pouca memória ou outros recursos.</span><span class="sxs-lookup"><span data-stu-id="10d37-245">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="10d37-246"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Este dispositivo não está funcionando corretamente. Um de seus drivers ou seu registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="10d37-246"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="10d37-247">(4)</span><span class="sxs-lookup"><span data-stu-id="10d37-247">(4)</span></span>


</dt> <dd>

<span data-ttu-id="10d37-248">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="10d37-248">Device is not working properly.</span></span> <span data-ttu-id="10d37-249">Um de seus drivers ou o registro pode estar corrompido.</span><span class="sxs-lookup"><span data-stu-id="10d37-249">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="10d37-250"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**O driver para este dispositivo precisa de um recurso que o Windows não possa gerenciar.**</span><span class="sxs-lookup"><span data-stu-id="10d37-250"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="10d37-251">(5)</span><span class="sxs-lookup"><span data-stu-id="10d37-251">(5)</span></span>


</dt> <dd>

<span data-ttu-id="10d37-252">O driver para o dispositivo requer um recurso que o Windows não pode gerenciar.</span><span class="sxs-lookup"><span data-stu-id="10d37-252">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="10d37-253"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**A configuração de inicialização para este dispositivo está em conflito com outros dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="10d37-253"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="10d37-254"> (6)</span><span class="sxs-lookup"><span data-stu-id="10d37-254">(6)</span></span>


</dt> <dd>

<span data-ttu-id="10d37-255">A configuração de inicialização para o dispositivo está em conflito com outros dispositivos.</span><span class="sxs-lookup"><span data-stu-id="10d37-255">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="10d37-256"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Não é possível filtrar.**</span><span class="sxs-lookup"><span data-stu-id="10d37-256"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="10d37-257">(7)</span><span class="sxs-lookup"><span data-stu-id="10d37-257">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="10d37-258"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**O carregador de driver para o dispositivo está ausente.**</span><span class="sxs-lookup"><span data-stu-id="10d37-258"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="10d37-259">(8)</span><span class="sxs-lookup"><span data-stu-id="10d37-259">(8)</span></span>


</dt> <dd>

<span data-ttu-id="10d37-260">O carregador de driver para o dispositivo está ausente.</span><span class="sxs-lookup"><span data-stu-id="10d37-260">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="10d37-261"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Este dispositivo não está funcionando corretamente porque o firmware de controle está relatando os recursos para o dispositivo incorretamente.**</span><span class="sxs-lookup"><span data-stu-id="10d37-261"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="10d37-262">(9)</span><span class="sxs-lookup"><span data-stu-id="10d37-262">(9)</span></span>


</dt> <dd>

<span data-ttu-id="10d37-263">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="10d37-263">Device is not working properly.</span></span> <span data-ttu-id="10d37-264">O firmware de controle está relatando incorretamente os recursos para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="10d37-264">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="10d37-265"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Este dispositivo não pode ser iniciado.**</span><span class="sxs-lookup"><span data-stu-id="10d37-265"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="10d37-266">(10)</span><span class="sxs-lookup"><span data-stu-id="10d37-266">(10)</span></span>


</dt> <dd>

<span data-ttu-id="10d37-267">Não é possível iniciar o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="10d37-267">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="10d37-268"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Este dispositivo falhou.**</span><span class="sxs-lookup"><span data-stu-id="10d37-268"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="10d37-269">(11)</span><span class="sxs-lookup"><span data-stu-id="10d37-269">(11)</span></span>


</dt> <dd>

<span data-ttu-id="10d37-270">Falha no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="10d37-270">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="10d37-271"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Este dispositivo não pode encontrar recursos livres suficientes que podem ser usados.**</span><span class="sxs-lookup"><span data-stu-id="10d37-271"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="10d37-272">12</span><span class="sxs-lookup"><span data-stu-id="10d37-272">(12)</span></span>


</dt> <dd>

<span data-ttu-id="10d37-273">O dispositivo não pode encontrar recursos livres suficientes para usar.</span><span class="sxs-lookup"><span data-stu-id="10d37-273">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="10d37-274"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**O Windows não pode verificar os recursos deste dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="10d37-274"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="10d37-275">(13)</span><span class="sxs-lookup"><span data-stu-id="10d37-275">(13)</span></span>


</dt> <dd>

<span data-ttu-id="10d37-276">O Windows não pode verificar os recursos do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="10d37-276">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="10d37-277"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Este dispositivo não funcionará corretamente até que você reinicie o computador.**</span><span class="sxs-lookup"><span data-stu-id="10d37-277"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="10d37-278">(14)</span><span class="sxs-lookup"><span data-stu-id="10d37-278">(14)</span></span>


</dt> <dd>

<span data-ttu-id="10d37-279">O dispositivo não funcionará corretamente até que o computador seja reiniciado.</span><span class="sxs-lookup"><span data-stu-id="10d37-279">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="10d37-280"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Este dispositivo não está funcionando corretamente porque provavelmente há um problema de nova enumeração.**</span><span class="sxs-lookup"><span data-stu-id="10d37-280"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="10d37-281">(15)</span><span class="sxs-lookup"><span data-stu-id="10d37-281">(15)</span></span>


</dt> <dd>

<span data-ttu-id="10d37-282">O dispositivo não está funcionando corretamente devido a um possível problema de reenumeração.</span><span class="sxs-lookup"><span data-stu-id="10d37-282">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="10d37-283"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**O Windows não pode identificar todos os recursos que este dispositivo usa.**</span><span class="sxs-lookup"><span data-stu-id="10d37-283"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="10d37-284">(16)</span><span class="sxs-lookup"><span data-stu-id="10d37-284">(16)</span></span>


</dt> <dd>

<span data-ttu-id="10d37-285">O Windows não pode identificar todos os recursos que o dispositivo usa.</span><span class="sxs-lookup"><span data-stu-id="10d37-285">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="10d37-286"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Este dispositivo está solicitando um tipo de recurso desconhecido.**</span><span class="sxs-lookup"><span data-stu-id="10d37-286"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="10d37-287">(17)</span><span class="sxs-lookup"><span data-stu-id="10d37-287">(17)</span></span>


</dt> <dd>

<span data-ttu-id="10d37-288">O dispositivo está solicitando um tipo de recurso desconhecido.</span><span class="sxs-lookup"><span data-stu-id="10d37-288">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="10d37-289"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstale os drivers para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="10d37-289"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="10d37-290">(18)</span><span class="sxs-lookup"><span data-stu-id="10d37-290">(18)</span></span>


</dt> <dd>

<span data-ttu-id="10d37-291">Os drivers de dispositivo devem ser reinstalados.</span><span class="sxs-lookup"><span data-stu-id="10d37-291">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="10d37-292"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Falha ao usar o carregador VxD.**</span><span class="sxs-lookup"><span data-stu-id="10d37-292"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="10d37-293">(19)</span><span class="sxs-lookup"><span data-stu-id="10d37-293">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="10d37-294"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**O registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="10d37-294"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="10d37-295">(20)</span><span class="sxs-lookup"><span data-stu-id="10d37-295">(20)</span></span>


</dt> <dd>

<span data-ttu-id="10d37-296">O registro pode estar corrompido.</span><span class="sxs-lookup"><span data-stu-id="10d37-296">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="10d37-297"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware. O Windows está removendo este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="10d37-297"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="10d37-298">(21)</span><span class="sxs-lookup"><span data-stu-id="10d37-298">(21)</span></span>


</dt> <dd>

<span data-ttu-id="10d37-299">Falha do sistema.</span><span class="sxs-lookup"><span data-stu-id="10d37-299">System failure.</span></span> <span data-ttu-id="10d37-300">Se a alteração do driver de dispositivo não for eficaz, consulte a documentação do hardware.</span><span class="sxs-lookup"><span data-stu-id="10d37-300">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="10d37-301">O Windows está removendo o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="10d37-301">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="10d37-302"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Este dispositivo está desabilitado.**</span><span class="sxs-lookup"><span data-stu-id="10d37-302"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="10d37-303">(22)</span><span class="sxs-lookup"><span data-stu-id="10d37-303">(22)</span></span>


</dt> <dd>

<span data-ttu-id="10d37-304">O dispositivo está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="10d37-304">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="10d37-305"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware.**</span><span class="sxs-lookup"><span data-stu-id="10d37-305"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="10d37-306">(23)</span><span class="sxs-lookup"><span data-stu-id="10d37-306">(23)</span></span>


</dt> <dd>

<span data-ttu-id="10d37-307">Falha do sistema.</span><span class="sxs-lookup"><span data-stu-id="10d37-307">System failure.</span></span> <span data-ttu-id="10d37-308">Se a alteração do driver de dispositivo não for eficaz, consulte a documentação do hardware.</span><span class="sxs-lookup"><span data-stu-id="10d37-308">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="10d37-309"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Este dispositivo não está presente, não está funcionando corretamente ou não tem todos os drivers instalados.**</span><span class="sxs-lookup"><span data-stu-id="10d37-309"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="10d37-310">(24)</span><span class="sxs-lookup"><span data-stu-id="10d37-310">(24)</span></span>


</dt> <dd>

<span data-ttu-id="10d37-311">O dispositivo não está presente, não está funcionando corretamente ou não tem todos os seus drivers instalados.</span><span class="sxs-lookup"><span data-stu-id="10d37-311">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="10d37-312"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="10d37-312"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="10d37-313">(25)</span><span class="sxs-lookup"><span data-stu-id="10d37-313">(25)</span></span>


</dt> <dd>

<span data-ttu-id="10d37-314">O Windows ainda está configurando o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="10d37-314">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="10d37-315"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="10d37-315"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="10d37-316">(26)</span><span class="sxs-lookup"><span data-stu-id="10d37-316">(26)</span></span>


</dt> <dd>

<span data-ttu-id="10d37-317">O Windows ainda está configurando o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="10d37-317">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="10d37-318"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Este dispositivo não tem uma configuração de log válida.**</span><span class="sxs-lookup"><span data-stu-id="10d37-318"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="10d37-319">(27)</span><span class="sxs-lookup"><span data-stu-id="10d37-319">(27)</span></span>


</dt> <dd>

<span data-ttu-id="10d37-320">O dispositivo não tem uma configuração de log válida.</span><span class="sxs-lookup"><span data-stu-id="10d37-320">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="10d37-321"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Os drivers para este dispositivo não estão instalados.**</span><span class="sxs-lookup"><span data-stu-id="10d37-321"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="10d37-322">(28)</span><span class="sxs-lookup"><span data-stu-id="10d37-322">(28)</span></span>


</dt> <dd>

<span data-ttu-id="10d37-323">Os drivers de dispositivo não estão instalados.</span><span class="sxs-lookup"><span data-stu-id="10d37-323">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="10d37-324"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Este dispositivo está desabilitado porque o firmware do dispositivo não forneceu os recursos necessários.**</span><span class="sxs-lookup"><span data-stu-id="10d37-324"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="10d37-325">(29)</span><span class="sxs-lookup"><span data-stu-id="10d37-325">(29)</span></span>


</dt> <dd>

<span data-ttu-id="10d37-326">O dispositivo está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="10d37-326">Device is disabled.</span></span> <span data-ttu-id="10d37-327">O firmware do dispositivo não forneceu os recursos necessários.</span><span class="sxs-lookup"><span data-stu-id="10d37-327">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="10d37-328"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Este dispositivo está usando um recurso de IRQ (solicitação de interrupção) que outro dispositivo está usando.**</span><span class="sxs-lookup"><span data-stu-id="10d37-328"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="10d37-329">(30)</span><span class="sxs-lookup"><span data-stu-id="10d37-329">(30)</span></span>


</dt> <dd>

<span data-ttu-id="10d37-330">O dispositivo está usando um recurso de IRQ que outro dispositivo está usando.</span><span class="sxs-lookup"><span data-stu-id="10d37-330">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="10d37-331"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Este dispositivo não está funcionando corretamente porque o Windows não pode carregar os drivers necessários para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="10d37-331"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="10d37-332">(31)</span><span class="sxs-lookup"><span data-stu-id="10d37-332">(31)</span></span>


</dt> <dd>

<span data-ttu-id="10d37-333">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="10d37-333">Device is not working properly.</span></span> <span data-ttu-id="10d37-334">O Windows não pode carregar os drivers de dispositivo necessários.</span><span class="sxs-lookup"><span data-stu-id="10d37-334">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="10d37-335">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="10d37-335">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10d37-336">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="10d37-336">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="10d37-337">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="10d37-337">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10d37-338">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="10d37-338">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="10d37-339">Se for **true**, o dispositivo estará usando uma configuração definida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="10d37-339">If **True**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="10d37-340">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="10d37-340">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="10d37-341">**CorrectableError**</span><span class="sxs-lookup"><span data-stu-id="10d37-341">**CorrectableError**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10d37-342">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="10d37-342">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="10d37-343">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="10d37-343">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10d37-344">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivo de memória DMTF \| 2,12 "," MIF. \|Matriz de memória física da DMTF \| 1,8 ")</span><span class="sxs-lookup"><span data-stu-id="10d37-344">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.12", "MIF.DMTF\|Physical Memory Array\|001.8")</span></span>
</dt> </dl>

<span data-ttu-id="10d37-345">Se **for true**, o erro mais recente era corrigível.</span><span class="sxs-lookup"><span data-stu-id="10d37-345">If **True**, the most recent error was correctable.</span></span> <span data-ttu-id="10d37-346">Se a propriedade **errorInfo** for igual a 3 (OK), essa propriedade não terá significado.</span><span class="sxs-lookup"><span data-stu-id="10d37-346">If the **ErrorInfo** property is equal to 3 (OK), then this property has no meaning.</span></span>

<span data-ttu-id="10d37-347">Essa propriedade é herdada [**da \_ memória CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="10d37-347">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="10d37-348">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="10d37-348">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10d37-349">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="10d37-349">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="10d37-350">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="10d37-350">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10d37-351">Qualificadores: [ **\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="10d37-351">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="10d37-352">Nome da primeira classe concreta a ser exibida na cadeia de herança usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="10d37-352">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="10d37-353">Quando usado com as outras propriedades de chave da classe, a propriedade permite que todas as instâncias dessa classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="10d37-353">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="10d37-354">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="10d37-354">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="10d37-355">**CurrentSRAM**</span><span class="sxs-lookup"><span data-stu-id="10d37-355">**CurrentSRAM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10d37-356">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="10d37-356">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="10d37-357">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="10d37-357">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10d37-358">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| tipo de SRAM atual do tipo SMBIOS 7 \| ")</span><span class="sxs-lookup"><span data-stu-id="10d37-358">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 7\|Current SRAM Type")</span></span>
</dt> </dl>

<span data-ttu-id="10d37-359">Matriz de tipos de memória de acesso aleatório estático (SRAM) que está sendo usada para a memória de cache.</span><span class="sxs-lookup"><span data-stu-id="10d37-359">Array of types of Static Random Access Memory (SRAM) being used for the cache memory.</span></span>

<span data-ttu-id="10d37-360">Esse valor é proveniente do membro de **tipo de SRAM atual** da estrutura de **informações de cache** nas informações de SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="10d37-360">This value comes from the **Current SRAM Type** member of the **Cache Information** structure in the SMBIOS information.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="10d37-361">**Outro** (0)</span><span class="sxs-lookup"><span data-stu-id="10d37-361">**Other** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="10d37-362">**Desconhecido** (1)</span><span class="sxs-lookup"><span data-stu-id="10d37-362">**Unknown** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Non-Burst"></span><span id="non-burst"></span><span id="NON-BURST"></span>

<span data-ttu-id="10d37-363">**Não intermitente** (2)</span><span class="sxs-lookup"><span data-stu-id="10d37-363">**Non-Burst** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Burst"></span><span id="burst"></span><span id="BURST"></span>

<span data-ttu-id="10d37-364">**Intermitência** (3)</span><span class="sxs-lookup"><span data-stu-id="10d37-364">**Burst** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Pipeline_Burst"></span><span id="pipeline_burst"></span><span id="PIPELINE_BURST"></span>

<span data-ttu-id="10d37-365">**Disparo de pipeline** (4)</span><span class="sxs-lookup"><span data-stu-id="10d37-365">**Pipeline Burst** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Synchronous"></span><span id="synchronous"></span><span id="SYNCHRONOUS"></span>

<span data-ttu-id="10d37-366">**Síncrono** (5)</span><span class="sxs-lookup"><span data-stu-id="10d37-366">**Synchronous** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Asynchronous"></span><span id="asynchronous"></span><span id="ASYNCHRONOUS"></span>

<span data-ttu-id="10d37-367">**Assíncrono** (6)</span><span class="sxs-lookup"><span data-stu-id="10d37-367">**Asynchronous** (6)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="10d37-368">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="10d37-368">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10d37-369">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="10d37-369">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="10d37-370">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="10d37-370">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10d37-371">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="10d37-371">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="10d37-372">Descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="10d37-372">Description of the object.</span></span>

<span data-ttu-id="10d37-373">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="10d37-373">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="10d37-374">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="10d37-374">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10d37-375">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="10d37-375">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="10d37-376">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="10d37-376">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10d37-377">Qualificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceID"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="10d37-377">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceId"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="10d37-378">Identificador exclusivo do cache representado por uma instância do **Win32 \_ CacheMemory**.</span><span class="sxs-lookup"><span data-stu-id="10d37-378">Unique identifier of the cache represented by an instance of **Win32\_CacheMemory**.</span></span>

<span data-ttu-id="10d37-379">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="10d37-379">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="10d37-380">Exemplo: "memória cache 1"</span><span class="sxs-lookup"><span data-stu-id="10d37-380">Example: "Cache Memory 1"</span></span>

</dd> <dt>

<span data-ttu-id="10d37-381">**EndingAddress**</span><span class="sxs-lookup"><span data-stu-id="10d37-381">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10d37-382">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="10d37-382">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="10d37-383">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="10d37-383">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10d37-384">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. Os \| endereços mapeados da matriz de memória DMTF \| 1,4 "," MIF. \|Endereços mapeados do dispositivo \| de memória DMTF 1,5 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" kilobytes ")</span><span class="sxs-lookup"><span data-stu-id="10d37-384">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Array Mapped Addresses\|001.4", "MIF.DMTF\|Memory Device Mapped Addresses\|001.5"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="10d37-385">Endereço final, referenciado por um aplicativo ou sistema operacional e mapeado por um controlador de memória, para esse objeto de memória.</span><span class="sxs-lookup"><span data-stu-id="10d37-385">Ending address, referenced by an application or operating system and mapped by a memory controller, for this memory object.</span></span> <span data-ttu-id="10d37-386">O endereço final é especificado em kilobytes.</span><span class="sxs-lookup"><span data-stu-id="10d37-386">The ending address is specified in kilobytes.</span></span>

<span data-ttu-id="10d37-387">Essa propriedade é herdada [**da \_ memória CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="10d37-387">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<span data-ttu-id="10d37-388">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="10d37-388">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="10d37-389">**ErrorAccess**</span><span class="sxs-lookup"><span data-stu-id="10d37-389">**ErrorAccess**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10d37-390">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="10d37-390">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="10d37-391">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="10d37-391">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10d37-392">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivo de memória DMTF \| 2,15 "," MIF. \|Matriz de memória física da DMTF \| 1,10 ")</span><span class="sxs-lookup"><span data-stu-id="10d37-392">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.15", "MIF.DMTF\|Physical Memory Array\|001.10")</span></span>
</dt> </dl>

<span data-ttu-id="10d37-393">Operação de acesso à memória que causou o último erro.</span><span class="sxs-lookup"><span data-stu-id="10d37-393">Memory access operation that caused the last error.</span></span> <span data-ttu-id="10d37-394">O tipo de erro é descrito pela propriedade **errorInfo** .</span><span class="sxs-lookup"><span data-stu-id="10d37-394">The type of error is described by the **ErrorInfo** property.</span></span> <span data-ttu-id="10d37-395">Se **errorInfo** for igual a 3 (OK), essa propriedade não terá significado.</span><span class="sxs-lookup"><span data-stu-id="10d37-395">If **ErrorInfo** is equal to 3 (OK), then this property has no meaning.</span></span>

<span data-ttu-id="10d37-396">Essa propriedade é herdada [**da \_ memória CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="10d37-396">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="10d37-397">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="10d37-397">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="10d37-398">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="10d37-398">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Read"></span><span id="read"></span><span id="READ"></span>

<span data-ttu-id="10d37-399">**Leitura** (3)</span><span class="sxs-lookup"><span data-stu-id="10d37-399">**Read** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write"></span><span id="write"></span><span id="WRITE"></span>

<span data-ttu-id="10d37-400">**Gravação** (4)</span><span class="sxs-lookup"><span data-stu-id="10d37-400">**Write** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Partial_Write"></span><span id="partial_write"></span><span id="PARTIAL_WRITE"></span>

<span data-ttu-id="10d37-401">**Gravação parcial** (5)</span><span class="sxs-lookup"><span data-stu-id="10d37-401">**Partial Write** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="10d37-402">**ErrorAddress**</span><span class="sxs-lookup"><span data-stu-id="10d37-402">**ErrorAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10d37-403">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="10d37-403">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="10d37-404">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="10d37-404">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10d37-405">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivo de memória DMTF \| 2,19 "," MIF. \|Dispositivo de memória DMTF \| 2,20 "," MIF. \|Matriz de memória física da DMTF \| 1,14 ")</span><span class="sxs-lookup"><span data-stu-id="10d37-405">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.19", "MIF.DMTF\|Memory Device\|002.20", "MIF.DMTF\|Physical Memory Array\|001.14")</span></span>
</dt> </dl>

<span data-ttu-id="10d37-406">Endereço do último erro de memória.</span><span class="sxs-lookup"><span data-stu-id="10d37-406">Address of the last memory error.</span></span> <span data-ttu-id="10d37-407">O tipo de erro é descrito pela propriedade **errorInfo** .</span><span class="sxs-lookup"><span data-stu-id="10d37-407">The type of error is described by the **ErrorInfo** property.</span></span> <span data-ttu-id="10d37-408">Se **errorInfo** for igual a 3 (OK), essa propriedade não terá significado.</span><span class="sxs-lookup"><span data-stu-id="10d37-408">If **ErrorInfo** is equal to 3 (OK), then this property has no meaning.</span></span>

<span data-ttu-id="10d37-409">Essa propriedade é herdada [**da \_ memória CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="10d37-409">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<span data-ttu-id="10d37-410">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="10d37-410">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="10d37-411">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="10d37-411">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10d37-412">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="10d37-412">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="10d37-413">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="10d37-413">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="10d37-414">Se **for true**, o erro relatado em **LastErrorCode** agora será limpo.</span><span class="sxs-lookup"><span data-stu-id="10d37-414">If **True**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="10d37-415">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="10d37-415">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="10d37-416">**ErrorCorrectType**</span><span class="sxs-lookup"><span data-stu-id="10d37-416">**ErrorCorrectType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10d37-417">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="10d37-417">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="10d37-418">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="10d37-418">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10d37-419">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| tipo de correção de erro do tipo SMBIOS 7 \| ")</span><span class="sxs-lookup"><span data-stu-id="10d37-419">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 7\|Error Correction Type")</span></span>
</dt> </dl>

<span data-ttu-id="10d37-420">Método de correção de erro usado pela memória de cache.</span><span class="sxs-lookup"><span data-stu-id="10d37-420">Error correction method used by the cache memory.</span></span>

<span data-ttu-id="10d37-421">Esse valor é proveniente do membro de **tipo de correção de erro** da estrutura de informações de **cache** nas informações de SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="10d37-421">This value comes from the **Error Correction Type** member of the **Cache Information** structure in the SMBIOS information.</span></span>

<dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="10d37-422">**Reservado** (0)</span><span class="sxs-lookup"><span data-stu-id="10d37-422">**Reserved** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="10d37-423">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="10d37-423">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="10d37-424">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="10d37-424">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="10d37-425">**Nenhum** (3)</span><span class="sxs-lookup"><span data-stu-id="10d37-425">**None** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Parity"></span><span id="parity"></span><span id="PARITY"></span>

<span data-ttu-id="10d37-426">**Paridade** (4)</span><span class="sxs-lookup"><span data-stu-id="10d37-426">**Parity** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Single-bit_ECC"></span><span id="single-bit_ecc"></span><span id="SINGLE-BIT_ECC"></span>

<span data-ttu-id="10d37-427">**ECC de bit único** (5)</span><span class="sxs-lookup"><span data-stu-id="10d37-427">**Single-bit ECC** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Multi-bit_ECC"></span><span id="multi-bit_ecc"></span><span id="MULTI-BIT_ECC"></span>

<span data-ttu-id="10d37-428">**ECC de vários bits** (6)</span><span class="sxs-lookup"><span data-stu-id="10d37-428">**Multi-bit ECC** (6)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="10d37-429">**ErrorData**</span><span class="sxs-lookup"><span data-stu-id="10d37-429">**ErrorData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10d37-430">Tipo de dados: matriz **uint8**</span><span class="sxs-lookup"><span data-stu-id="10d37-430">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="10d37-431">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="10d37-431">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10d37-432">Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivo de memória DMTF \| 2,17 "," MIF. \|Matriz de memória física da DMTF \| 1,12 "), [**máx**](/windows/desktop/WmiSdk/standard-qualifiers) . (64)</span><span class="sxs-lookup"><span data-stu-id="10d37-432">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.17", "MIF.DMTF\|Physical Memory Array\|001.12"), [**MAX**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="10d37-433">Matriz de dados capturados durante o último acesso de memória incorreto.</span><span class="sxs-lookup"><span data-stu-id="10d37-433">Array of data captured during the last erroneous memory access.</span></span> <span data-ttu-id="10d37-434">Os dados ocupam os primeiros *n* octetos da matriz necessários para manter o número de bits especificado pela propriedade **ErrorTransferSize** .</span><span class="sxs-lookup"><span data-stu-id="10d37-434">The data occupies the first *n* octets of the array necessary to hold the number of bits specified by the **ErrorTransferSize** property.</span></span> <span data-ttu-id="10d37-435">Se **ErrorTransferSize** for 0 (zero), essa propriedade não terá significado.</span><span class="sxs-lookup"><span data-stu-id="10d37-435">If **ErrorTransferSize** is 0 (zero), then this property has no meaning.</span></span>

<span data-ttu-id="10d37-436">Essa propriedade é herdada [**da \_ memória CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="10d37-436">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="10d37-437">**ErrorDataOrder**</span><span class="sxs-lookup"><span data-stu-id="10d37-437">**ErrorDataOrder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10d37-438">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="10d37-438">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="10d37-439">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="10d37-439">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="10d37-440">Ordenação de dados armazenados na propriedade **ErrorData** .</span><span class="sxs-lookup"><span data-stu-id="10d37-440">Ordering for data stored in the **ErrorData** property.</span></span> <span data-ttu-id="10d37-441">Se **ErrorTransferSize** for 0 (zero), essa propriedade não terá significado.</span><span class="sxs-lookup"><span data-stu-id="10d37-441">If **ErrorTransferSize** is 0 (zero), then this property has no meaning.</span></span>

<span data-ttu-id="10d37-442">Essa propriedade é herdada [**da \_ memória CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="10d37-442">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="10d37-443">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="10d37-443">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Least_Significant_Byte_First"></span><span id="least_significant_byte_first"></span><span id="LEAST_SIGNIFICANT_BYTE_FIRST"></span>

<span data-ttu-id="10d37-444">**Byte menos significativo primeiro** (1)</span><span class="sxs-lookup"><span data-stu-id="10d37-444">**Least Significant Byte First** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Most_Significant_Byte_First"></span><span id="most_significant_byte_first"></span><span id="MOST_SIGNIFICANT_BYTE_FIRST"></span>

<span data-ttu-id="10d37-445">**Byte mais significativo primeiro** (2)</span><span class="sxs-lookup"><span data-stu-id="10d37-445">**Most Significant Byte First** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="10d37-446">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="10d37-446">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10d37-447">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="10d37-447">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="10d37-448">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="10d37-448">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="10d37-449">Mais informações sobre o erro registrado em **LastErrorCode** e informações sobre as ações corretivas que podem ser executadas.</span><span class="sxs-lookup"><span data-stu-id="10d37-449">More information about the error recorded in **LastErrorCode**, and information on any corrective actions that may be taken.</span></span>

<span data-ttu-id="10d37-450">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="10d37-450">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="10d37-451">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="10d37-451">**ErrorInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10d37-452">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="10d37-452">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="10d37-453">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="10d37-453">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10d37-454">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivo de memória DMTF \| 2,12 "," MIF. \|Matriz de memória física da DMTF \| 1,8 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ memória CIM**](cim-memory.md).**OtherErrorDescription**")</span><span class="sxs-lookup"><span data-stu-id="10d37-454">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.12", "MIF.DMTF\|Physical Memory Array\|001.8"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Memory**](cim-memory.md).**OtherErrorDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="10d37-455">Tipo de erro que ocorreu mais recentemente.</span><span class="sxs-lookup"><span data-stu-id="10d37-455">Type of error that occurred most recently.</span></span> <span data-ttu-id="10d37-456">Os valores 12-14 são indefinidos no esquema CIM porque, no DMI, eles misturam a semântica do tipo de erro e se ele era corrigível ou não.</span><span class="sxs-lookup"><span data-stu-id="10d37-456">The values 12-14 are undefined in the CIM schema because in DMI they mix the semantics of the type of error and whether it was correctable or not.</span></span> <span data-ttu-id="10d37-457">O último é indicado na propriedade **CorrectableError**.</span><span class="sxs-lookup"><span data-stu-id="10d37-457">The latter is indicated in the property **CorrectableError**.</span></span>

<span data-ttu-id="10d37-458">Essa propriedade é herdada [**da \_ memória CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="10d37-458">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="10d37-459">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="10d37-459">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="10d37-460">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="10d37-460">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="10d37-461">**OK** (3)</span><span class="sxs-lookup"><span data-stu-id="10d37-461">**OK** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Bad_Read"></span><span id="bad_read"></span><span id="BAD_READ"></span>

<span data-ttu-id="10d37-462">**Leitura inadequada** (4)</span><span class="sxs-lookup"><span data-stu-id="10d37-462">**Bad Read** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Parity_Error"></span><span id="parity_error"></span><span id="PARITY_ERROR"></span>

<span data-ttu-id="10d37-463">**Erro de paridade** (5)</span><span class="sxs-lookup"><span data-stu-id="10d37-463">**Parity Error** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Single-Bit_Error"></span><span id="single-bit_error"></span><span id="SINGLE-BIT_ERROR"></span>

<span data-ttu-id="10d37-464">**Erro de bit único** (6)</span><span class="sxs-lookup"><span data-stu-id="10d37-464">**Single-Bit Error** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Double-Bit_Error"></span><span id="double-bit_error"></span><span id="DOUBLE-BIT_ERROR"></span>

<span data-ttu-id="10d37-465">**Erro de bit duplo** (7)</span><span class="sxs-lookup"><span data-stu-id="10d37-465">**Double-Bit Error** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Multi-Bit_Error"></span><span id="multi-bit_error"></span><span id="MULTI-BIT_ERROR"></span>

<span data-ttu-id="10d37-466">**Erro de vários bits** (8)</span><span class="sxs-lookup"><span data-stu-id="10d37-466">**Multi-Bit Error** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Nibble_Error"></span><span id="nibble_error"></span><span id="NIBBLE_ERROR"></span>

<span data-ttu-id="10d37-467">**Erro de Nibble** (9)</span><span class="sxs-lookup"><span data-stu-id="10d37-467">**Nibble Error** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Checksum_Error"></span><span id="checksum_error"></span><span id="CHECKSUM_ERROR"></span>

<span data-ttu-id="10d37-468">**Erro de soma de verificação** (10)</span><span class="sxs-lookup"><span data-stu-id="10d37-468">**Checksum Error** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="CRC_Error"></span><span id="crc_error"></span><span id="CRC_ERROR"></span>

<span data-ttu-id="10d37-469">**Erro de CRC** (11)</span><span class="sxs-lookup"><span data-stu-id="10d37-469">**CRC Error** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="10d37-470">**Indefinido** (12)</span><span class="sxs-lookup"><span data-stu-id="10d37-470">**Undefined** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="10d37-471">**Indefinido** (13)</span><span class="sxs-lookup"><span data-stu-id="10d37-471">**Undefined** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="10d37-472">**Indefinido** (14)</span><span class="sxs-lookup"><span data-stu-id="10d37-472">**Undefined** (14)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="10d37-473">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="10d37-473">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10d37-474">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="10d37-474">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="10d37-475">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="10d37-475">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10d37-476">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Matriz de memória física da DMTF \| 1,7 ")</span><span class="sxs-lookup"><span data-stu-id="10d37-476">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Physical Memory Array\|001.7")</span></span>
</dt> </dl>

<span data-ttu-id="10d37-477">Detalhes sobre os algoritmos de paridade ou CRC, ECC ou outros mecanismos usados.</span><span class="sxs-lookup"><span data-stu-id="10d37-477">Details on the parity or CRC algorithms, ECC, or other mechanisms used.</span></span>

<span data-ttu-id="10d37-478">Essa propriedade é herdada [**da \_ memória CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="10d37-478">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="10d37-479">**ErrorResolution**</span><span class="sxs-lookup"><span data-stu-id="10d37-479">**ErrorResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10d37-480">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="10d37-480">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="10d37-481">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="10d37-481">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10d37-482">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivo de memória DMTF \| 2,21 "," MIF. \|Matriz de memória física da DMTF \| 1,15 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ")</span><span class="sxs-lookup"><span data-stu-id="10d37-482">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.21", "MIF.DMTF\|Physical Memory Array\|001.15"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="10d37-483">Intervalo, em bytes, para o qual o último erro pode ser resolvido.</span><span class="sxs-lookup"><span data-stu-id="10d37-483">Range, in bytes, to which the last error can be resolved.</span></span> <span data-ttu-id="10d37-484">Por exemplo, se os endereços de erro forem resolvidos para o bit 11 (ou seja, em uma base de página típica), os erros poderão ser resolvidos para os limites de 4 KB e essa propriedade será definida como 4000.</span><span class="sxs-lookup"><span data-stu-id="10d37-484">For example, if error addresses are resolved to bit 11 (that is, on a typical page basis), then errors can be resolved to 4 KB boundaries and this property is set to 4000.</span></span> <span data-ttu-id="10d37-485">Se a propriedade **errorInfo** for igual a 3 (OK), essa propriedade não terá significado.</span><span class="sxs-lookup"><span data-stu-id="10d37-485">If the **ErrorInfo** property is equal to 3 (OK), then this property has no meaning.</span></span>

<span data-ttu-id="10d37-486">Essa propriedade é herdada [**da \_ memória CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="10d37-486">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<span data-ttu-id="10d37-487">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="10d37-487">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="10d37-488">**ErrorTime**</span><span class="sxs-lookup"><span data-stu-id="10d37-488">**ErrorTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10d37-489">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="10d37-489">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="10d37-490">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="10d37-490">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="10d37-491">Hora em que ocorreu o último erro de memória.</span><span class="sxs-lookup"><span data-stu-id="10d37-491">Time that the last memory error occurred.</span></span> <span data-ttu-id="10d37-492">O tipo de erro é descrito pela propriedade **errorInfo** .</span><span class="sxs-lookup"><span data-stu-id="10d37-492">The type of error is described by the **ErrorInfo** property.</span></span> <span data-ttu-id="10d37-493">Se a propriedade **errorInfo** for igual a 3 (OK), essa propriedade não terá significado.</span><span class="sxs-lookup"><span data-stu-id="10d37-493">If the **ErrorInfo** property is equal to 3 (OK), then this property has no meaning.</span></span>

<span data-ttu-id="10d37-494">Essa propriedade é herdada [**da \_ memória CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="10d37-494">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="10d37-495">**ErrorTransferSize**</span><span class="sxs-lookup"><span data-stu-id="10d37-495">**ErrorTransferSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10d37-496">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="10d37-496">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="10d37-497">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="10d37-497">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10d37-498">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivo de memória DMTF \| 2,16 "," MIF. \|Matriz de memória física da DMTF \| 1,11 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" bits ")</span><span class="sxs-lookup"><span data-stu-id="10d37-498">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.16", "MIF.DMTF\|Physical Memory Array\|001.11"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="10d37-499">Tamanho da transferência de dados em bits que causou o último erro.</span><span class="sxs-lookup"><span data-stu-id="10d37-499">Size of the data transfer in bits that caused the last error.</span></span> <span data-ttu-id="10d37-500">0 (zero) indica que não há erro.</span><span class="sxs-lookup"><span data-stu-id="10d37-500">0 (zero) indicates no error.</span></span> <span data-ttu-id="10d37-501">Se a propriedade **errorInfo** for igual a 3 (OK), essa propriedade deverá ser definida como 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="10d37-501">If the **ErrorInfo** property is equal to 3 (OK), then this property should be set to 0 (zero).</span></span>

<span data-ttu-id="10d37-502">Essa propriedade é herdada [**da \_ memória CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="10d37-502">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="10d37-503">**FlushTimer**</span><span class="sxs-lookup"><span data-stu-id="10d37-503">**FlushTimer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10d37-504">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="10d37-504">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="10d37-505">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="10d37-505">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10d37-506">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Cache do sistema DMTF \| 3,14 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" segundos ")</span><span class="sxs-lookup"><span data-stu-id="10d37-506">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Cache\|003.14"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("seconds")</span></span>
</dt> </dl>

<span data-ttu-id="10d37-507">Quantidade máxima de tempo, em segundos, que as linhas sujas ou buckets podem permanecer no cache antes de serem liberados.</span><span class="sxs-lookup"><span data-stu-id="10d37-507">Maximum amount of time, in seconds, dirty lines or buckets may remain in the cache before they are flushed.</span></span> <span data-ttu-id="10d37-508">Um valor de 0 (zero) indica que uma liberação de cache não é controlada por um temporizador de liberação.</span><span class="sxs-lookup"><span data-stu-id="10d37-508">A value of 0 (zero) indicates that a cache flush is not controlled by a flushing timer.</span></span>

<span data-ttu-id="10d37-509">Essa propriedade é herdada do [**CIM \_ CacheMemory**](cim-cachememory.md).</span><span class="sxs-lookup"><span data-stu-id="10d37-509">This property is inherited from [**CIM\_CacheMemory**](cim-cachememory.md).</span></span>

</dd> <dt>

<span data-ttu-id="10d37-510">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="10d37-510">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10d37-511">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="10d37-511">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="10d37-512">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="10d37-512">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10d37-513">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="10d37-513">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="10d37-514">Data e hora em que o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="10d37-514">Date and time the object was installed.</span></span> <span data-ttu-id="10d37-515">Essa propriedade não precisa de um valor para indicar que o objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="10d37-515">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="10d37-516">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="10d37-516">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="10d37-517">**InstalledSize**</span><span class="sxs-lookup"><span data-stu-id="10d37-517">**InstalledSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10d37-518">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="10d37-518">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="10d37-519">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="10d37-519">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10d37-520">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("tamanho do SMBIOS do \| tipo 7 \| instalado"), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span><span class="sxs-lookup"><span data-stu-id="10d37-520">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 7\|Installed Size"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="10d37-521">Tamanho atual da memória de cache instalada.</span><span class="sxs-lookup"><span data-stu-id="10d37-521">Current size of the installed cache memory.</span></span>

<span data-ttu-id="10d37-522">Esse valor é proveniente do membro de **Tamanho instalado** da estrutura de **informações de cache** nas informações de SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="10d37-522">This value comes from the **Installed Size** member of the **Cache Information** structure in the SMBIOS information.</span></span>

</dd> <dt>

<span data-ttu-id="10d37-523">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="10d37-523">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10d37-524">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="10d37-524">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="10d37-525">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="10d37-525">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="10d37-526">Código do último erro relatado pelo dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="10d37-526">Last error code reported by the logical device.</span></span>

<span data-ttu-id="10d37-527">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="10d37-527">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="10d37-528">**Level**</span><span class="sxs-lookup"><span data-stu-id="10d37-528">**Level**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10d37-529">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="10d37-529">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="10d37-530">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="10d37-530">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10d37-531">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Cache do sistema DMTF \| 3,2 ")</span><span class="sxs-lookup"><span data-stu-id="10d37-531">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Cache\|003.2")</span></span>
</dt> </dl>

<span data-ttu-id="10d37-532">Nível do cache.</span><span class="sxs-lookup"><span data-stu-id="10d37-532">Level of the cache.</span></span>

<span data-ttu-id="10d37-533">Esse valor é proveniente do membro de **configuração de cache** da estrutura de **informações de cache** nas informações de SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="10d37-533">This value comes from the **Cache Configuration** member of the **Cache Information** structure in the SMBIOS information.</span></span>

<span data-ttu-id="10d37-534">Essa propriedade é herdada do [**CIM \_ CacheMemory**](cim-cachememory.md).</span><span class="sxs-lookup"><span data-stu-id="10d37-534">This property is inherited from [**CIM\_CacheMemory**](cim-cachememory.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="10d37-535"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="10d37-535"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="10d37-536"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="10d37-536"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Primary"></span><span id="primary"></span><span id="PRIMARY"></span>

<span data-ttu-id="10d37-537"><span id="Primary"></span><span id="primary"></span><span id="PRIMARY"></span>**Primário** (3)</span><span class="sxs-lookup"><span data-stu-id="10d37-537"><span id="Primary"></span><span id="primary"></span><span id="PRIMARY"></span>**Primary** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Secondary"></span><span id="secondary"></span><span id="SECONDARY"></span>

<span data-ttu-id="10d37-538"><span id="Secondary"></span><span id="secondary"></span><span id="SECONDARY"></span>**Secundário** (4)</span><span class="sxs-lookup"><span data-stu-id="10d37-538"><span id="Secondary"></span><span id="secondary"></span><span id="SECONDARY"></span>**Secondary** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Tertiary"></span><span id="tertiary"></span><span id="TERTIARY"></span>

<span data-ttu-id="10d37-539"><span id="Tertiary"></span><span id="tertiary"></span><span id="TERTIARY"></span>**Terciário** (5)</span><span class="sxs-lookup"><span data-stu-id="10d37-539"><span id="Tertiary"></span><span id="tertiary"></span><span id="TERTIARY"></span>**Tertiary** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="10d37-540"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Não aplicável** (6)</span><span class="sxs-lookup"><span data-stu-id="10d37-540"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="10d37-541">**Linhas de**</span><span class="sxs-lookup"><span data-stu-id="10d37-541">**LineSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10d37-542">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="10d37-542">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="10d37-543">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="10d37-543">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10d37-544">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Cache do sistema DMTF \| 3,10 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ")</span><span class="sxs-lookup"><span data-stu-id="10d37-544">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Cache\|003.10"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="10d37-545">Tamanho, em bytes, de um único Bucket ou linha de cache.</span><span class="sxs-lookup"><span data-stu-id="10d37-545">Size, in bytes, of a single cache bucket or line.</span></span>

<span data-ttu-id="10d37-546">Essa propriedade é herdada do [**CIM \_ CacheMemory**](cim-cachememory.md).</span><span class="sxs-lookup"><span data-stu-id="10d37-546">This property is inherited from [**CIM\_CacheMemory**](cim-cachememory.md).</span></span>

</dd> <dt>

<span data-ttu-id="10d37-547">**Localidade**</span><span class="sxs-lookup"><span data-stu-id="10d37-547">**Location**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10d37-548">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="10d37-548">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="10d37-549">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="10d37-549">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10d37-550">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| local do tipo SMBIOS 7 \| ")</span><span class="sxs-lookup"><span data-stu-id="10d37-550">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 7\|Location")</span></span>
</dt> </dl>

<span data-ttu-id="10d37-551">Local físico da memória de cache.</span><span class="sxs-lookup"><span data-stu-id="10d37-551">Physical location of the cache memory.</span></span>

<span data-ttu-id="10d37-552">Esse valor é proveniente do membro de **configuração de cache** da estrutura de **informações de cache** nas informações de SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="10d37-552">This value comes from the **Cache Configuration** member of the **Cache Information** structure in the SMBIOS information.</span></span>

<dt>

<span id="Internal"></span><span id="internal"></span><span id="INTERNAL"></span>

<span data-ttu-id="10d37-553">**Interno** (0)</span><span class="sxs-lookup"><span data-stu-id="10d37-553">**Internal** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="External"></span><span id="external"></span><span id="EXTERNAL"></span>

<span data-ttu-id="10d37-554">**Externo** (1)</span><span class="sxs-lookup"><span data-stu-id="10d37-554">**External** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="10d37-555">**Reservado** (2)</span><span class="sxs-lookup"><span data-stu-id="10d37-555">**Reserved** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="10d37-556">**Desconhecido** (3)</span><span class="sxs-lookup"><span data-stu-id="10d37-556">**Unknown** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="10d37-557">**MaxCacheSize**</span><span class="sxs-lookup"><span data-stu-id="10d37-557">**MaxCacheSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10d37-558">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="10d37-558">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="10d37-559">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="10d37-559">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10d37-560">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| tamanho máximo de cache do SMBIOS tipo 7 \| "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span><span class="sxs-lookup"><span data-stu-id="10d37-560">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 7\|Maximum Cache Size"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="10d37-561">Tamanho máximo de cache instalável nessa memória de cache específica.</span><span class="sxs-lookup"><span data-stu-id="10d37-561">Maximum cache size installable to this particular cache memory.</span></span>

<span data-ttu-id="10d37-562">Esse valor é proveniente do membro de **tamanho máximo do cache** da estrutura de **informações do cache** nas informações do SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="10d37-562">This value comes from the **Maximum Cache Size** member of the **Cache Information** structure in the SMBIOS information.</span></span>

</dd> <dt>

<span data-ttu-id="10d37-563">**Nome**</span><span class="sxs-lookup"><span data-stu-id="10d37-563">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10d37-564">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="10d37-564">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="10d37-565">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="10d37-565">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10d37-566">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="10d37-566">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="10d37-567">Rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="10d37-567">Label by which the object is known.</span></span> <span data-ttu-id="10d37-568">Quando em uma subclasse, a propriedade pode ser substituída para ser uma propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="10d37-568">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="10d37-569">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="10d37-569">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="10d37-570">**NumberOfBlocks**</span><span class="sxs-lookup"><span data-stu-id="10d37-570">**NumberOfBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10d37-571">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="10d37-571">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="10d37-572">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="10d37-572">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10d37-573">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| host-REsources-MIB. hrStorageSize ")</span><span class="sxs-lookup"><span data-stu-id="10d37-573">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageSize")</span></span>
</dt> </dl>

<span data-ttu-id="10d37-574">Número total de blocos consecutivos, cada um deles bloqueando o tamanho do valor contido na propriedade **BlockSize** , que formam essa extensão de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="10d37-574">Total number of consecutive blocks, each block the size of the value contained in the **BlockSize** property, which form this storage extent.</span></span> <span data-ttu-id="10d37-575">O tamanho total da extensão de armazenamento pode ser calculado multiplicando o valor da propriedade **BlockSize** pelo valor dessa propriedade.</span><span class="sxs-lookup"><span data-stu-id="10d37-575">Total size of the storage extent can be calculated by multiplying the value of the **BlockSize** property by the value of this property.</span></span> <span data-ttu-id="10d37-576">Se o valor de **BlockSize** for 1, essa propriedade será o tamanho total da extensão de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="10d37-576">If the value of **BlockSize** is 1, this property is the total size of the storage extent.</span></span>

<span data-ttu-id="10d37-577">Essa propriedade é herdada do [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="10d37-577">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="10d37-578">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="10d37-578">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="10d37-579">**OtherErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="10d37-579">**OtherErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10d37-580">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="10d37-580">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="10d37-581">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="10d37-581">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10d37-582">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ memória CIM**](cim-memory.md).**ErrorInfo**")</span><span class="sxs-lookup"><span data-stu-id="10d37-582">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Memory**](cim-memory.md).**ErrorInfo**")</span></span>
</dt> </dl>

<span data-ttu-id="10d37-583">Cadeia de caracteres de forma livre que fornece mais informações se a propriedade **ErrorType** estiver definida como 1, outra.</span><span class="sxs-lookup"><span data-stu-id="10d37-583">Free-form string providing more information if the **ErrorType** property is set to 1, Other.</span></span> <span data-ttu-id="10d37-584">Caso contrário, essa cadeia de caracteres não tem significado.</span><span class="sxs-lookup"><span data-stu-id="10d37-584">Otherwise, this string has no meaning.</span></span>

<span data-ttu-id="10d37-585">Essa propriedade é herdada [**da \_ memória CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="10d37-585">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="10d37-586">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="10d37-586">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10d37-587">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="10d37-587">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="10d37-588">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="10d37-588">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10d37-589">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="10d37-589">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="10d37-590">Identificador de dispositivo do Windows Plug and Play do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="10d37-590">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="10d37-591">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="10d37-591">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="10d37-592">Exemplo: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="10d37-592">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="10d37-593">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="10d37-593">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10d37-594">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="10d37-594">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="10d37-595">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="10d37-595">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="10d37-596">Matriz de recursos específicos relacionados à energia de um dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="10d37-596">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="10d37-597">Essa propriedade é herdada **de \_ LogicalDevice CIM**.</span><span class="sxs-lookup"><span data-stu-id="10d37-597">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="10d37-598"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="10d37-598"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="10d37-599"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="10d37-599"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="10d37-600"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Desabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="10d37-600"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="10d37-601"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="10d37-601"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="10d37-602">Os recursos de gerenciamento de energia estão habilitados no momento, mas o conjunto de recursos exato é desconhecido ou as informações não estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="10d37-602">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="10d37-603"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de economia de energia inseridos automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="10d37-603"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="10d37-604">O dispositivo pode alterar seu estado de energia com base no uso ou em outros critérios.</span><span class="sxs-lookup"><span data-stu-id="10d37-604">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="10d37-605"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energia configurável** (5)</span><span class="sxs-lookup"><span data-stu-id="10d37-605"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="10d37-606">Há suporte para o método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="10d37-606">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="10d37-607">Esse método é encontrado na classe pai **de \_ LogicalDevice CIM** e pode ser implementado.</span><span class="sxs-lookup"><span data-stu-id="10d37-607">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="10d37-608">Para obter mais informações, consulte [Designing formato MOF (MOF) classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="10d37-608">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="10d37-609"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energia com suporte** (6)</span><span class="sxs-lookup"><span data-stu-id="10d37-609"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="10d37-610">O método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) pode ser invocado com o parâmetro *PowerState* definido como 5 (ciclo de energia).</span><span class="sxs-lookup"><span data-stu-id="10d37-610">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="10d37-611"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Energia cronometrada com suporte** (7)</span><span class="sxs-lookup"><span data-stu-id="10d37-611"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="10d37-612">Tempo Power-On com suporte</span><span class="sxs-lookup"><span data-stu-id="10d37-612">Timed Power-On Supported</span></span>

<span data-ttu-id="10d37-613">O método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) pode ser invocado com o parâmetro *PowerState* definido como 5 (ciclo de energia) e o *tempo* definido como uma data e hora e um intervalo específicos para o Power-on.</span><span class="sxs-lookup"><span data-stu-id="10d37-613">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="10d37-614">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="10d37-614">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10d37-615">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="10d37-615">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="10d37-616">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="10d37-616">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="10d37-617">Se **for true**, o dispositivo poderá ser gerenciado por energia (pode ser colocado no modo de suspensão e assim por diante).</span><span class="sxs-lookup"><span data-stu-id="10d37-617">If **True**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="10d37-618">A propriedade não indica que os recursos de gerenciamento de energia estão habilitados no momento, apenas que o dispositivo lógico é capaz de gerenciamento de energia.</span><span class="sxs-lookup"><span data-stu-id="10d37-618">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="10d37-619">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="10d37-619">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="10d37-620">**Finalidade**</span><span class="sxs-lookup"><span data-stu-id="10d37-620">**Purpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10d37-621">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="10d37-621">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="10d37-622">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="10d37-622">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="10d37-623">Cadeia de caracteres de forma livre que descreve a mídia e seu uso.</span><span class="sxs-lookup"><span data-stu-id="10d37-623">Free-form string describing the media and its use.</span></span>

<span data-ttu-id="10d37-624">Esse valor é proveniente do membro de **designação de soquete** da estrutura de **informações de cache** nas informações de SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="10d37-624">This value comes from the **Socket Designation** member of the **Cache Information** structure in the SMBIOS information.</span></span>

<span data-ttu-id="10d37-625">Essa propriedade é herdada do [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="10d37-625">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="10d37-626">**As**</span><span class="sxs-lookup"><span data-stu-id="10d37-626">**ReadPolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10d37-627">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="10d37-627">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="10d37-628">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="10d37-628">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10d37-629">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Cache do sistema DMTF \| 3,13 ")</span><span class="sxs-lookup"><span data-stu-id="10d37-629">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Cache\|003.13")</span></span>
</dt> </dl>

<span data-ttu-id="10d37-630">Política que deve ser empregada pelo cache para lidar com solicitações de leitura.</span><span class="sxs-lookup"><span data-stu-id="10d37-630">Policy that shall be employed by the cache for handling read requests.</span></span>

<span data-ttu-id="10d37-631">Essa propriedade é herdada do [**CIM \_ CacheMemory**](cim-cachememory.md).</span><span class="sxs-lookup"><span data-stu-id="10d37-631">This property is inherited from [**CIM\_CacheMemory**](cim-cachememory.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="10d37-632">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="10d37-632">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="10d37-633">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="10d37-633">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Read"></span><span id="read"></span><span id="READ"></span>

<span data-ttu-id="10d37-634">**Leitura** (3)</span><span class="sxs-lookup"><span data-stu-id="10d37-634">**Read** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Read-Ahead"></span><span id="read-ahead"></span><span id="READ-AHEAD"></span>

<span data-ttu-id="10d37-635">**Read-Ahead** (4)</span><span class="sxs-lookup"><span data-stu-id="10d37-635">**Read-Ahead** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Read_and_Read-Ahead"></span><span id="read_and_read-ahead"></span><span id="READ_AND_READ-AHEAD"></span>

<span data-ttu-id="10d37-636">**Leitura e leitura antecipada** (5)</span><span class="sxs-lookup"><span data-stu-id="10d37-636">**Read and Read-Ahead** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Determination_Per_I_O"></span><span id="determination_per_i_o"></span><span id="DETERMINATION_PER_I_O"></span>

<span data-ttu-id="10d37-637">**Determinação por e/s** (6)</span><span class="sxs-lookup"><span data-stu-id="10d37-637">**Determination Per I/O** (6)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="10d37-638">**ReplacementPolicy**</span><span class="sxs-lookup"><span data-stu-id="10d37-638">**ReplacementPolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10d37-639">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="10d37-639">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="10d37-640">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="10d37-640">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10d37-641">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Cache do sistema DMTF \| 3,12 ")</span><span class="sxs-lookup"><span data-stu-id="10d37-641">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Cache\|003.12")</span></span>
</dt> </dl>

<span data-ttu-id="10d37-642">Algoritmo para determinar quais linhas de cache ou buckets devem ser reutilizados.</span><span class="sxs-lookup"><span data-stu-id="10d37-642">Algorithm to determine which cache lines or buckets should be reused.</span></span>

<span data-ttu-id="10d37-643">Essa propriedade é herdada do [**CIM \_ CacheMemory**](cim-cachememory.md).</span><span class="sxs-lookup"><span data-stu-id="10d37-643">This property is inherited from [**CIM\_CacheMemory**](cim-cachememory.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="10d37-644">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="10d37-644">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="10d37-645">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="10d37-645">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Least_Recently_Used__LRU_"></span><span id="least_recently_used__lru_"></span><span id="LEAST_RECENTLY_USED__LRU_"></span>

<span data-ttu-id="10d37-646">**Menos usado recentemente (LRU)** (3)</span><span class="sxs-lookup"><span data-stu-id="10d37-646">**Least Recently Used (LRU)** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="First_In_First_Out__FIFO_"></span><span id="first_in_first_out__fifo_"></span><span id="FIRST_IN_FIRST_OUT__FIFO_"></span>

<span data-ttu-id="10d37-647">**Primeiro a entrar, primeiro a sair (FIFO)** (4)</span><span class="sxs-lookup"><span data-stu-id="10d37-647">**First In First Out (FIFO)** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Last_In_First_Out__LIFO_"></span><span id="last_in_first_out__lifo_"></span><span id="LAST_IN_FIRST_OUT__LIFO_"></span>

<span data-ttu-id="10d37-648">**Último a entrar, primeiro a sair (UEPS)** (5)</span><span class="sxs-lookup"><span data-stu-id="10d37-648">**Last In First Out (LIFO)** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Least_Frequently_Used__LFU_"></span><span id="least_frequently_used__lfu_"></span><span id="LEAST_FREQUENTLY_USED__LFU_"></span>

<span data-ttu-id="10d37-649">**Usado com menos frequência (LFU)** (6)</span><span class="sxs-lookup"><span data-stu-id="10d37-649">**Least Frequently Used (LFU)** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Most_Frequently_Used__MFU_"></span><span id="most_frequently_used__mfu_"></span><span id="MOST_FREQUENTLY_USED__MFU_"></span>

<span data-ttu-id="10d37-650">**Usado com mais frequência (MFU)** (7)</span><span class="sxs-lookup"><span data-stu-id="10d37-650">**Most Frequently Used (MFU)** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Data_Dependent_Multiple_Algorithms"></span><span id="data_dependent_multiple_algorithms"></span><span id="DATA_DEPENDENT_MULTIPLE_ALGORITHMS"></span>

<span data-ttu-id="10d37-651">**Algoritmos múltiplos dependentes de dados** (8)</span><span class="sxs-lookup"><span data-stu-id="10d37-651">**Data Dependent Multiple Algorithms** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="10d37-652">**StartingAddress**</span><span class="sxs-lookup"><span data-stu-id="10d37-652">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10d37-653">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="10d37-653">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="10d37-654">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="10d37-654">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10d37-655">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. Os \| endereços mapeados da matriz de memória DMTF \| 1,3 "," MIF. \|Endereços mapeados do dispositivo \| de memória DMTF 1,4 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" kilobytes ")</span><span class="sxs-lookup"><span data-stu-id="10d37-655">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Array Mapped Addresses\|001.3", "MIF.DMTF\|Memory Device Mapped Addresses\|001.4"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="10d37-656">Endereço inicial, referenciado por um aplicativo ou sistema operacional e mapeado por um controlador de memória, para esse objeto de memória.</span><span class="sxs-lookup"><span data-stu-id="10d37-656">Beginning address, referenced by an application or operating system and mapped by a memory controller, for this memory object.</span></span> <span data-ttu-id="10d37-657">O endereço inicial é especificado em kilobytes.</span><span class="sxs-lookup"><span data-stu-id="10d37-657">The starting address is specified in kilobytes.</span></span>

<span data-ttu-id="10d37-658">Essa propriedade é herdada [**da \_ memória CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="10d37-658">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<span data-ttu-id="10d37-659">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="10d37-659">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="10d37-660">**Status**</span><span class="sxs-lookup"><span data-stu-id="10d37-660">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10d37-661">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="10d37-661">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="10d37-662">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="10d37-662">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10d37-663">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="10d37-663">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="10d37-664">Status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="10d37-664">Current status of the object.</span></span> <span data-ttu-id="10d37-665">Vários status de operação e não operacional podem ser definidos.</span><span class="sxs-lookup"><span data-stu-id="10d37-665">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="10d37-666">Os status operacionais incluem: "OK", "degradado" e "Pred falha" (um elemento, como uma unidade de disco rígido habilitado para inteligente, pode estar funcionando corretamente, mas prevendo uma falha em um futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="10d37-666">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="10d37-667">Os status não operacionais incluem: "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="10d37-667">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="10d37-668">O último, "Service", pode ser aplicado durante o espelhamento de espelho de um disco, recarregar uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="10d37-668">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="10d37-669">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="10d37-669">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="10d37-670">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="10d37-670">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="10d37-671">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="10d37-671">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="10d37-672">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="10d37-672">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="10d37-673">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="10d37-673">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="10d37-674">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="10d37-674">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="10d37-675">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="10d37-675">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="10d37-676">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="10d37-676">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="10d37-677">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="10d37-677">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="10d37-678">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="10d37-678">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="10d37-679">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="10d37-679">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="10d37-680">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="10d37-680">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="10d37-681">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="10d37-681">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="10d37-682">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="10d37-682">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="10d37-683">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="10d37-683">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="10d37-684">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="10d37-684">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10d37-685">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="10d37-685">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="10d37-686">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="10d37-686">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10d37-687">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operacional da DMTF \| 3,3 ")</span><span class="sxs-lookup"><span data-stu-id="10d37-687">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="10d37-688">Estado do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="10d37-688">State of the logical device.</span></span> <span data-ttu-id="10d37-689">Se essa propriedade não se aplicar ao dispositivo lógico, o valor 5 (não aplicável) deverá ser usado.</span><span class="sxs-lookup"><span data-stu-id="10d37-689">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="10d37-690">Esse valor é proveniente do membro de **configuração de cache** da estrutura de **informações de cache** nas informações de SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="10d37-690">This value comes from the **Cache Configuration** member of the **Cache Information** structure in the SMBIOS information.</span></span>

<span data-ttu-id="10d37-691">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="10d37-691">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="10d37-692">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="10d37-692">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="10d37-693">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="10d37-693">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="10d37-694">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="10d37-694">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="10d37-695">**Desabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="10d37-695">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="10d37-696">**Não aplicável** (5)</span><span class="sxs-lookup"><span data-stu-id="10d37-696">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="10d37-697">**SupportedSRAM**</span><span class="sxs-lookup"><span data-stu-id="10d37-697">**SupportedSRAM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10d37-698">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="10d37-698">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="10d37-699">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="10d37-699">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10d37-700">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| tipo de SRAM com suporte do tipo de SMBIOS 7 \| ")</span><span class="sxs-lookup"><span data-stu-id="10d37-700">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 7\|Supported SRAM Type")</span></span>
</dt> </dl>

<span data-ttu-id="10d37-701">Matriz de tipos com suporte de memória estática de acesso aleatório (SRAM) que pode ser usada para a memória de cache.</span><span class="sxs-lookup"><span data-stu-id="10d37-701">Array of supported types of Static Random Access Memory (SRAM) that can be used for the cache memory.</span></span>

<span data-ttu-id="10d37-702">Esse valor é proveniente do membro de **tipo de SRAM com suporte** da estrutura de **informações de cache** nas informações de SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="10d37-702">This value comes from the **Supported SRAM Type** member of the **Cache Information** structure in the SMBIOS information.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="10d37-703">**Outro** (0)</span><span class="sxs-lookup"><span data-stu-id="10d37-703">**Other** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="10d37-704">**Desconhecido** (1)</span><span class="sxs-lookup"><span data-stu-id="10d37-704">**Unknown** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Non-Burst"></span><span id="non-burst"></span><span id="NON-BURST"></span>

<span data-ttu-id="10d37-705">**Não intermitente** (2)</span><span class="sxs-lookup"><span data-stu-id="10d37-705">**Non-Burst** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Burst"></span><span id="burst"></span><span id="BURST"></span>

<span data-ttu-id="10d37-706">**Intermitência** (3)</span><span class="sxs-lookup"><span data-stu-id="10d37-706">**Burst** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Pipeline_Burst"></span><span id="pipeline_burst"></span><span id="PIPELINE_BURST"></span>

<span data-ttu-id="10d37-707">**Disparo de pipeline** (4)</span><span class="sxs-lookup"><span data-stu-id="10d37-707">**Pipeline Burst** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Synchronous"></span><span id="synchronous"></span><span id="SYNCHRONOUS"></span>

<span data-ttu-id="10d37-708">**Síncrono** (5)</span><span class="sxs-lookup"><span data-stu-id="10d37-708">**Synchronous** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Asynchronous"></span><span id="asynchronous"></span><span id="ASYNCHRONOUS"></span>

<span data-ttu-id="10d37-709">**Assíncrono** (6)</span><span class="sxs-lookup"><span data-stu-id="10d37-709">**Asynchronous** (6)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="10d37-710">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="10d37-710">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10d37-711">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="10d37-711">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="10d37-712">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="10d37-712">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10d37-713">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="10d37-713">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="10d37-714">Valor da propriedade **CreationClassName** do computador de escopo.</span><span class="sxs-lookup"><span data-stu-id="10d37-714">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="10d37-715">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="10d37-715">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="10d37-716">**SystemLevelAddress**</span><span class="sxs-lookup"><span data-stu-id="10d37-716">**SystemLevelAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10d37-717">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="10d37-717">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="10d37-718">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="10d37-718">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="10d37-719">Se **for true**, as informações de endereço na propriedade **ErrorAddress** serão um endereço de nível de sistema.</span><span class="sxs-lookup"><span data-stu-id="10d37-719">If **True**, the address information in the property **ErrorAddress** is a system-level address.</span></span> <span data-ttu-id="10d37-720">Se for **false**, será um endereço físico.</span><span class="sxs-lookup"><span data-stu-id="10d37-720">If **False**, it is a physical address.</span></span> <span data-ttu-id="10d37-721">Se a propriedade **errorInfo** for igual a 3, essa propriedade não terá significado.</span><span class="sxs-lookup"><span data-stu-id="10d37-721">If the **ErrorInfo** property is equal to 3, then this property has no meaning.</span></span>

<span data-ttu-id="10d37-722">Essa propriedade é herdada [**da \_ memória CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="10d37-722">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="10d37-723">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="10d37-723">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10d37-724">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="10d37-724">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="10d37-725">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="10d37-725">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10d37-726">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**Name**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="10d37-726">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="10d37-727">Nome do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="10d37-727">Name of the scoping system.</span></span>

<span data-ttu-id="10d37-728">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="10d37-728">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="10d37-729">**WritePolicy**</span><span class="sxs-lookup"><span data-stu-id="10d37-729">**WritePolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10d37-730">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="10d37-730">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="10d37-731">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="10d37-731">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10d37-732">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Cache do sistema DMTF \| 3,5 ")</span><span class="sxs-lookup"><span data-stu-id="10d37-732">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Cache\|003.5")</span></span>
</dt> </dl>

<span data-ttu-id="10d37-733">Gravar definição de política.</span><span class="sxs-lookup"><span data-stu-id="10d37-733">Write policy definition.</span></span>

<span data-ttu-id="10d37-734">Esse valor é proveniente do membro de **configuração de cache** da estrutura de **informações de cache** nas informações de SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="10d37-734">This value comes from the **Cache Configuration** member of the **Cache Information** structure in the SMBIOS information.</span></span>

<span data-ttu-id="10d37-735">Essa propriedade é herdada do [**CIM \_ CacheMemory**](cim-cachememory.md).</span><span class="sxs-lookup"><span data-stu-id="10d37-735">This property is inherited from [**CIM\_CacheMemory**](cim-cachememory.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="10d37-736">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="10d37-736">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="10d37-737">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="10d37-737">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Write_Back"></span><span id="write_back"></span><span id="WRITE_BACK"></span>

<span data-ttu-id="10d37-738">**Write-back** (3)</span><span class="sxs-lookup"><span data-stu-id="10d37-738">**Write Back** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write_Through"></span><span id="write_through"></span><span id="WRITE_THROUGH"></span>

<span data-ttu-id="10d37-739">**Gravação por** (4)</span><span class="sxs-lookup"><span data-stu-id="10d37-739">**Write Through** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Varies_with_Address"></span><span id="varies_with_address"></span><span id="VARIES_WITH_ADDRESS"></span>

<span data-ttu-id="10d37-740">**Varia de acordo com o endereço** (5)</span><span class="sxs-lookup"><span data-stu-id="10d37-740">**Varies with Address** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Determination_Per_I_O"></span><span id="determination_per_i_o"></span><span id="DETERMINATION_PER_I_O"></span>

<span data-ttu-id="10d37-741">**Determinação por e/s** (6)</span><span class="sxs-lookup"><span data-stu-id="10d37-741">**Determination Per I/O** (6)</span></span>


<span data-ttu-id="10d37-742"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="10d37-742"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="10d37-743">Comentários</span><span class="sxs-lookup"><span data-stu-id="10d37-743">Remarks</span></span>

<span data-ttu-id="10d37-744">A classe **Win32 \_ CacheMemory** é derivada de [**CIM \_ CacheMemory**](cim-cachememory.md).</span><span class="sxs-lookup"><span data-stu-id="10d37-744">The **Win32\_CacheMemory** class is derived from [**CIM\_CacheMemory**](cim-cachememory.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="10d37-745">Requisitos</span><span class="sxs-lookup"><span data-stu-id="10d37-745">Requirements</span></span>



| <span data-ttu-id="10d37-746">Requisito</span><span class="sxs-lookup"><span data-stu-id="10d37-746">Requirement</span></span> | <span data-ttu-id="10d37-747">Valor</span><span class="sxs-lookup"><span data-stu-id="10d37-747">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="10d37-748">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="10d37-748">Minimum supported client</span></span><br/> | <span data-ttu-id="10d37-749">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="10d37-749">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="10d37-750">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="10d37-750">Minimum supported server</span></span><br/> | <span data-ttu-id="10d37-751">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="10d37-751">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="10d37-752">Namespace</span><span class="sxs-lookup"><span data-stu-id="10d37-752">Namespace</span></span><br/>                | <span data-ttu-id="10d37-753">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="10d37-753">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="10d37-754">MOF</span><span class="sxs-lookup"><span data-stu-id="10d37-754">MOF</span></span><br/>                      | <dl> <span data-ttu-id="10d37-755"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="10d37-755"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="10d37-756">DLL</span><span class="sxs-lookup"><span data-stu-id="10d37-756">DLL</span></span><br/>                      | <dl> <span data-ttu-id="10d37-757"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="10d37-757"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="10d37-758">Confira também</span><span class="sxs-lookup"><span data-stu-id="10d37-758">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10d37-759">**\_CACHEMEMORY CIM**</span><span class="sxs-lookup"><span data-stu-id="10d37-759">**CIM\_CacheMemory**</span></span>](cim-cachememory.md)
</dt> <dt>

[<span data-ttu-id="10d37-760">Classes de hardware do sistema de computador</span><span class="sxs-lookup"><span data-stu-id="10d37-760">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

