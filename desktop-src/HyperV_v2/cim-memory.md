---
description: Representa os recursos e o gerenciamento de dispositivos lógicos relacionados à memória.
ms.assetid: 802c1c0e-7eab-4a17-9a29-6502ece6cb24
title: Classe CIM_Memory (gerenciamento do Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Memory
- CIM_Memory.Volatile
- CIM_Memory.ErrorMethodology
- CIM_Memory.StartingAddress
- CIM_Memory.EndingAddress
- CIM_Memory.ErrorInfo
- CIM_Memory.OtherErrorDescription
- CIM_Memory.CorrectableError
- CIM_Memory.ErrorTime
- CIM_Memory.ErrorAccess
- CIM_Memory.ErrorTransferSize
- CIM_Memory.ErrorData
- CIM_Memory.ErrorDataOrder
- CIM_Memory.ErrorAddress
- CIM_Memory.SystemLevelAddress
- CIM_Memory.ErrorResolution
- CIM_Memory.AdditionalErrorData
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 410d580542421aee153b610726bed1f438efbcde
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104506011"
---
# <a name="cim_memory-class-hyper-v-management"></a><span data-ttu-id="fcbcb-103">Classe CIM_Memory (gerenciamento do Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="fcbcb-103">CIM_Memory class (Hyper-V management)</span></span>

<span data-ttu-id="fcbcb-104">Representa os recursos e o gerenciamento de dispositivos lógicos relacionados à memória.</span><span class="sxs-lookup"><span data-stu-id="fcbcb-104">Represents the capabilities and management of memory-related logical devices.</span></span>

## <a name="syntax"></a><span data-ttu-id="fcbcb-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fcbcb-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.8.0"), UMLPackagePath("CIM::Device::Memory"), AMENDMENT]
class CIM_Memory : CIM_StorageExtent
{
  boolean  Volatile;
  string   ErrorMethodology;
  uint64   StartingAddress;
  uint64   EndingAddress;
  uint16   ErrorInfo;
  string   OtherErrorDescription;
  boolean  CorrectableError;
  datetime ErrorTime;
  uint16   ErrorAccess;
  uint32   ErrorTransferSize;
  uint8    ErrorData[];
  uint16   ErrorDataOrder;
  uint64   ErrorAddress;
  boolean  SystemLevelAddress;
  uint64   ErrorResolution;
  uint8    AdditionalErrorData[];
};
```

## <a name="members"></a><span data-ttu-id="fcbcb-106">Membros</span><span class="sxs-lookup"><span data-stu-id="fcbcb-106">Members</span></span>

<span data-ttu-id="fcbcb-107">A classe de **\_ memória CIM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="fcbcb-107">The **CIM\_Memory** class has these types of members:</span></span>

-   [<span data-ttu-id="fcbcb-108">Propriedades</span><span class="sxs-lookup"><span data-stu-id="fcbcb-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fcbcb-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="fcbcb-109">Properties</span></span>

<span data-ttu-id="fcbcb-110">A classe de **\_ memória CIM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="fcbcb-110">The **CIM\_Memory** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fcbcb-111">**AdditionalErrorData**</span><span class="sxs-lookup"><span data-stu-id="fcbcb-111">**AdditionalErrorData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fcbcb-112">Tipo de dados: matriz **uint8**</span><span class="sxs-lookup"><span data-stu-id="fcbcb-112">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="fcbcb-113">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fcbcb-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fcbcb-114">Qualificadores: [**preteridos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ MemoryError. AdditionalErrorData"), **octetstring**, [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivo de memória DMTF \| 5,18 "," MIF. \|Matriz de memória física da DMTF \| 1,13 ")</span><span class="sxs-lookup"><span data-stu-id="fcbcb-114">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM\_MemoryError.AdditionalErrorData"), **OctetString**, [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|005.18", "MIF.DMTF\|Physical Memory Array\|001.13")</span></span>
</dt> </dl>

<span data-ttu-id="fcbcb-115">Uma matriz de octetos que contém informações adicionais sobre o erro.</span><span class="sxs-lookup"><span data-stu-id="fcbcb-115">An array of octets that contains additional error information.</span></span> <span data-ttu-id="fcbcb-116">Um exemplo é a síndrome de ECC ou o retorno dos bits de verificação se uma metodologia de erro baseada em CRC for usada.</span><span class="sxs-lookup"><span data-stu-id="fcbcb-116">An example is ECC syndrome or the return of the check bits if a CRC-based error methodology is used.</span></span> <span data-ttu-id="fcbcb-117">No último caso, se um único erro de bit for reconhecido e o algoritmo CRC for conhecido, será possível determinar o bit exato que falhou.</span><span class="sxs-lookup"><span data-stu-id="fcbcb-117">In the latter case, if a single bit error is recognized and the CRC algorithm is known, it is possible to determine the exact bit that failed.</span></span>

<span data-ttu-id="fcbcb-118">Se a propriedade **errorInfo** contiver "3" (OK), essa propriedade não será usada.</span><span class="sxs-lookup"><span data-stu-id="fcbcb-118">If the **ErrorInfo** property contains "3" (OK), this property is not used.</span></span>

</dd> <dt>

<span data-ttu-id="fcbcb-119">**CorrectableError**</span><span class="sxs-lookup"><span data-stu-id="fcbcb-119">**CorrectableError**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fcbcb-120">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="fcbcb-120">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="fcbcb-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fcbcb-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fcbcb-122">Qualificadores: [**preteridos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ MemoryError. CorrectableError"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Matriz de memória física da DMTF \| 1,8 ")</span><span class="sxs-lookup"><span data-stu-id="fcbcb-122">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM\_MemoryError.CorrectableError"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Physical Memory Array\|001.8")</span></span>
</dt> </dl>

<span data-ttu-id="fcbcb-123">**true** se o erro mais recente for corrigível; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="fcbcb-123">**true** if the most recent error is correctable; otherwise, **false**.</span></span> <span data-ttu-id="fcbcb-124">Se a propriedade **errorInfo** contiver "3" (OK), essa propriedade não será usada.</span><span class="sxs-lookup"><span data-stu-id="fcbcb-124">If the **ErrorInfo** property contains "3" (OK), this property is not used.</span></span>

</dd> <dt>

<span data-ttu-id="fcbcb-125">**EndingAddress**</span><span class="sxs-lookup"><span data-stu-id="fcbcb-125">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fcbcb-126">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="fcbcb-126">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="fcbcb-127">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fcbcb-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fcbcb-128">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("quilobytes"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. Os \| endereços mapeados da matriz de memória DMTF \| 1,4 "," MIF. \|Endereços mapeados do dispositivo de memória DMTF \| 1,5 "), **PUnit** (" byte \* 10 ^ 3 ")</span><span class="sxs-lookup"><span data-stu-id="fcbcb-128">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("KiloBytes"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Array Mapped Addresses\|001.4", "MIF.DMTF\|Memory Device Mapped Addresses\|001.5"), **PUnit** ("byte \* 10^3")</span></span>
</dt> </dl>

<span data-ttu-id="fcbcb-129">O endereço final que é referenciado por um aplicativo ou sistema operacional e é mapeado por um controlador de memória para o objeto de memória.</span><span class="sxs-lookup"><span data-stu-id="fcbcb-129">The ending address that is referenced by an application or operating system, and mapped by a memory controller for the memory object.</span></span> <span data-ttu-id="fcbcb-130">O endereço final é especificado em kilobytes.</span><span class="sxs-lookup"><span data-stu-id="fcbcb-130">The ending address is specified in kilobytes.</span></span>

</dd> <dt>

<span data-ttu-id="fcbcb-131">**ErrorAccess**</span><span class="sxs-lookup"><span data-stu-id="fcbcb-131">**ErrorAccess**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fcbcb-132">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fcbcb-132">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fcbcb-133">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fcbcb-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fcbcb-134">Qualificadores: [**preteridos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ MemoryError. ErrorAccess"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Matriz de memória física da DMTF \| 1,10 ")</span><span class="sxs-lookup"><span data-stu-id="fcbcb-134">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM\_MemoryError.ErrorAccess"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Physical Memory Array\|001.10")</span></span>
</dt> </dl>

<span data-ttu-id="fcbcb-135">A operação de acesso à memória que causou o último erro.</span><span class="sxs-lookup"><span data-stu-id="fcbcb-135">The memory access operation that caused the last error.</span></span> <span data-ttu-id="fcbcb-136">Se a propriedade **errorInfo** contiver "3" (OK), essa propriedade não será usada.</span><span class="sxs-lookup"><span data-stu-id="fcbcb-136">If the **ErrorInfo** property contains "3" (OK), this property is not used.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="fcbcb-137">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="fcbcb-137">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="fcbcb-138">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="fcbcb-138">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Read"></span><span id="read"></span><span id="READ"></span>

<span data-ttu-id="fcbcb-139">**Leitura** (3)</span><span class="sxs-lookup"><span data-stu-id="fcbcb-139">**Read** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write"></span><span id="write"></span><span id="WRITE"></span>

<span data-ttu-id="fcbcb-140">**Gravação** (4)</span><span class="sxs-lookup"><span data-stu-id="fcbcb-140">**Write** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Partial_Write"></span><span id="partial_write"></span><span id="PARTIAL_WRITE"></span>

<span data-ttu-id="fcbcb-141">**Gravação parcial** (5)</span><span class="sxs-lookup"><span data-stu-id="fcbcb-141">**Partial Write** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="fcbcb-142">**ErrorAddress**</span><span class="sxs-lookup"><span data-stu-id="fcbcb-142">**ErrorAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fcbcb-143">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="fcbcb-143">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="fcbcb-144">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fcbcb-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fcbcb-145">Qualificadores: [**preteridos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ MemoryError. StartingAddress"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivo de memória DMTF \| 5,19 "," MIF. \|Matriz de memória física da DMTF \| 1,14 ")</span><span class="sxs-lookup"><span data-stu-id="fcbcb-145">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM\_MemoryError.StartingAddress"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|005.19", "MIF.DMTF\|Physical Memory Array\|001.14")</span></span>
</dt> </dl>

<span data-ttu-id="fcbcb-146">O endereço do último erro de memória.</span><span class="sxs-lookup"><span data-stu-id="fcbcb-146">The address of the last memory error.</span></span> <span data-ttu-id="fcbcb-147">O tipo de erro é descrito pela propriedade **errorInfo** .</span><span class="sxs-lookup"><span data-stu-id="fcbcb-147">The type of error is described by the **ErrorInfo** property.</span></span> <span data-ttu-id="fcbcb-148">Se a propriedade **errorInfo** contiver "3" (OK), essa propriedade não será usada.</span><span class="sxs-lookup"><span data-stu-id="fcbcb-148">If the **ErrorInfo** property contains "3" (OK), this property is not used.</span></span>

</dd> <dt>

<span data-ttu-id="fcbcb-149">**ErrorData**</span><span class="sxs-lookup"><span data-stu-id="fcbcb-149">**ErrorData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fcbcb-150">Tipo de dados: matriz **uint8**</span><span class="sxs-lookup"><span data-stu-id="fcbcb-150">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="fcbcb-151">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fcbcb-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fcbcb-152">Qualificadores: [**preterido**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ MemoryError. ErrorData"), **octetstring**, [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Matriz de memória física da DMTF \| 1,12 ")</span><span class="sxs-lookup"><span data-stu-id="fcbcb-152">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM\_MemoryError.ErrorData"), **OctetString**, [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Physical Memory Array\|001.12")</span></span>
</dt> </dl>

<span data-ttu-id="fcbcb-153">Uma matriz que contém dados capturados durante o último acesso de memória errado.</span><span class="sxs-lookup"><span data-stu-id="fcbcb-153">An array that contains data captured during the last erroneous memory access.</span></span> <span data-ttu-id="fcbcb-154">Os dados ocupam os primeiros n octetos da matriz necessários para manter o número de bits especificado pela propriedade **ErrorTransferSize** .</span><span class="sxs-lookup"><span data-stu-id="fcbcb-154">The data occupies the first n octets of the array necessary to hold the number of bits specified by the **ErrorTransferSize** property.</span></span>

<span data-ttu-id="fcbcb-155">Se a propriedade **ErrorTransferSize** contiver "0" (OK), essa propriedade não será usada.</span><span class="sxs-lookup"><span data-stu-id="fcbcb-155">If the **ErrorTransferSize** property contains "0" (OK), this property is not used.</span></span>

</dd> <dt>

<span data-ttu-id="fcbcb-156">**ErrorDataOrder**</span><span class="sxs-lookup"><span data-stu-id="fcbcb-156">**ErrorDataOrder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fcbcb-157">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fcbcb-157">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fcbcb-158">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fcbcb-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fcbcb-159">Qualificadores: [**preteridos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ MemoryError. ErrorDataOrder")</span><span class="sxs-lookup"><span data-stu-id="fcbcb-159">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM\_MemoryError.ErrorDataOrder")</span></span>
</dt> </dl>

<span data-ttu-id="fcbcb-160">A ordenação de dados armazenados na propriedade **ErrorData** .</span><span class="sxs-lookup"><span data-stu-id="fcbcb-160">The ordering for data stored in the **ErrorData** property.</span></span> <span data-ttu-id="fcbcb-161">"Byte menos significativo primeiro" (valor = 1) ou "o byte mais significativo primeiro" (2) pode ser especificado.</span><span class="sxs-lookup"><span data-stu-id="fcbcb-161">"Least Significant Byte First" (value=1) or "Most Significant Byte First" (2) can be specified.</span></span> <span data-ttu-id="fcbcb-162">Se a propriedade **ErrorTransferSize** contiver "0" (OK), essa propriedade não será usada.</span><span class="sxs-lookup"><span data-stu-id="fcbcb-162">If the **ErrorTransferSize** property contains "0" (OK), this property is not used.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="fcbcb-163">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="fcbcb-163">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Least_Significant_Byte_First"></span><span id="least_significant_byte_first"></span><span id="LEAST_SIGNIFICANT_BYTE_FIRST"></span>

<span data-ttu-id="fcbcb-164">**Byte menos significativo primeiro** (1)</span><span class="sxs-lookup"><span data-stu-id="fcbcb-164">**Least Significant Byte First** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Most_Significant_Byte_First"></span><span id="most_significant_byte_first"></span><span id="MOST_SIGNIFICANT_BYTE_FIRST"></span>

<span data-ttu-id="fcbcb-165">**Byte mais significativo primeiro** (2)</span><span class="sxs-lookup"><span data-stu-id="fcbcb-165">**Most Significant Byte First** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="fcbcb-166">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="fcbcb-166">**ErrorInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fcbcb-167">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fcbcb-167">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fcbcb-168">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fcbcb-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fcbcb-169">Qualificadores: [**preteridos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ MemoryError. ErrorInfo"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivo de memória DMTF \| 5,12 "," MIF. \|Matriz de memória física da DMTF \| 1,8 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ memória CIM**.**OtherErrorDescription**")</span><span class="sxs-lookup"><span data-stu-id="fcbcb-169">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM\_MemoryError.ErrorInfo"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|005.12", "MIF.DMTF\|Physical Memory Array\|001.8"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Memory**.**OtherErrorDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="fcbcb-170">O tipo do último erro a ocorrer.</span><span class="sxs-lookup"><span data-stu-id="fcbcb-170">The type of the last error to occur.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="fcbcb-171">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="fcbcb-171">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="fcbcb-172">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="fcbcb-172">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="fcbcb-173">**OK** (3)</span><span class="sxs-lookup"><span data-stu-id="fcbcb-173">**OK** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Bad_Read"></span><span id="bad_read"></span><span id="BAD_READ"></span>

<span data-ttu-id="fcbcb-174">**Leitura inadequada** (4)</span><span class="sxs-lookup"><span data-stu-id="fcbcb-174">**Bad Read** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Parity_Error"></span><span id="parity_error"></span><span id="PARITY_ERROR"></span>

<span data-ttu-id="fcbcb-175">**Erro de paridade** (5)</span><span class="sxs-lookup"><span data-stu-id="fcbcb-175">**Parity Error** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Single-Bit_Error"></span><span id="single-bit_error"></span><span id="SINGLE-BIT_ERROR"></span>

<span data-ttu-id="fcbcb-176">**Erro de bit único** (6)</span><span class="sxs-lookup"><span data-stu-id="fcbcb-176">**Single-Bit Error** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Double-Bit_Error"></span><span id="double-bit_error"></span><span id="DOUBLE-BIT_ERROR"></span>

<span data-ttu-id="fcbcb-177">**Erro de bit duplo** (7)</span><span class="sxs-lookup"><span data-stu-id="fcbcb-177">**Double-Bit Error** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Multi-Bit_Error"></span><span id="multi-bit_error"></span><span id="MULTI-BIT_ERROR"></span>

<span data-ttu-id="fcbcb-178">**Erro de vários bits** (8)</span><span class="sxs-lookup"><span data-stu-id="fcbcb-178">**Multi-Bit Error** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Nibble_Error"></span><span id="nibble_error"></span><span id="NIBBLE_ERROR"></span>

<span data-ttu-id="fcbcb-179">**Erro de Nibble** (9)</span><span class="sxs-lookup"><span data-stu-id="fcbcb-179">**Nibble Error** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Checksum_Error"></span><span id="checksum_error"></span><span id="CHECKSUM_ERROR"></span>

<span data-ttu-id="fcbcb-180">**Erro de soma de verificação** (10)</span><span class="sxs-lookup"><span data-stu-id="fcbcb-180">**Checksum Error** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="CRC_Error"></span><span id="crc_error"></span><span id="CRC_ERROR"></span>

<span data-ttu-id="fcbcb-181">**Erro de CRC** (11)</span><span class="sxs-lookup"><span data-stu-id="fcbcb-181">**CRC Error** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="fcbcb-182">**Indefinido** (12)</span><span class="sxs-lookup"><span data-stu-id="fcbcb-182">**Undefined** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="fcbcb-183">**Indefinido** (13)</span><span class="sxs-lookup"><span data-stu-id="fcbcb-183">**Undefined** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="fcbcb-184">**Indefinido** (14)</span><span class="sxs-lookup"><span data-stu-id="fcbcb-184">**Undefined** (14)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="fcbcb-185">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="fcbcb-185">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fcbcb-186">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="fcbcb-186">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fcbcb-187">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fcbcb-187">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fcbcb-188">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ErrorMethodology"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Matriz de memória física da DMTF \| 1,7 ")</span><span class="sxs-lookup"><span data-stu-id="fcbcb-188">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ErrorMethodology"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Physical Memory Array\|001.7")</span></span>
</dt> </dl>

<span data-ttu-id="fcbcb-189">Indica se algoritmos de paridade, algoritmos de CRC, ECC ou outros mecanismos são usados pelo objeto de memória.</span><span class="sxs-lookup"><span data-stu-id="fcbcb-189">Indicates whether parity algorithms, CRC algorithms, ECC, or other mechanisms are used by the memory object.</span></span> <span data-ttu-id="fcbcb-190">Também é possível fornecer detalhes sobre o algoritmo.</span><span class="sxs-lookup"><span data-stu-id="fcbcb-190">Details on the algorithm can also be supplied.</span></span>

</dd> <dt>

<span data-ttu-id="fcbcb-191">**ErrorResolution**</span><span class="sxs-lookup"><span data-stu-id="fcbcb-191">**ErrorResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fcbcb-192">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="fcbcb-192">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="fcbcb-193">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fcbcb-193">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fcbcb-194">Qualificadores: [**preteridos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ MemoryError. ErrorResolution"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivo de memória DMTF \| 5,21 "," MIF. \|Matriz de memória física da DMTF \| 1,15 "), **PUnit** (" byte ")</span><span class="sxs-lookup"><span data-stu-id="fcbcb-194">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM\_MemoryError.ErrorResolution"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|005.21", "MIF.DMTF\|Physical Memory Array\|001.15"), **PUnit** ("byte")</span></span>
</dt> </dl>

<span data-ttu-id="fcbcb-195">O intervalo, em bytes, no qual o último erro pode ser resolvido.</span><span class="sxs-lookup"><span data-stu-id="fcbcb-195">The range, in bytes, in which the last error can be resolved.</span></span> <span data-ttu-id="fcbcb-196">Por exemplo, se os endereços de erro forem resolvidos para 11 bits, como em uma base de página típica; em seguida, os erros podem ser resolvidos para limites de 4K e essa propriedade é definida como "4000".</span><span class="sxs-lookup"><span data-stu-id="fcbcb-196">For example, if error addresses are resolved to bit 11, such as on a typical page basis; then the errors can be resolved to 4K boundaries, and this property is set to "4000".</span></span> <span data-ttu-id="fcbcb-197">Se a propriedade **errorInfo** contiver "3" (OK), essa propriedade não será usada.</span><span class="sxs-lookup"><span data-stu-id="fcbcb-197">If the **ErrorInfo** property contains "3" (OK), this property is not used.</span></span>

</dd> <dt>

<span data-ttu-id="fcbcb-198">**ErrorTime**</span><span class="sxs-lookup"><span data-stu-id="fcbcb-198">**ErrorTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fcbcb-199">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="fcbcb-199">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="fcbcb-200">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fcbcb-200">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fcbcb-201">Qualificadores: [**preteridos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ MemoryError. ErrorTime")</span><span class="sxs-lookup"><span data-stu-id="fcbcb-201">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM\_MemoryError.ErrorTime")</span></span>
</dt> </dl>

<span data-ttu-id="fcbcb-202">A hora em que ocorreu o último erro de memória.</span><span class="sxs-lookup"><span data-stu-id="fcbcb-202">The time when the last memory error occurred.</span></span> <span data-ttu-id="fcbcb-203">Se a propriedade **errorInfo** contiver "3" (OK), essa propriedade não será usada.</span><span class="sxs-lookup"><span data-stu-id="fcbcb-203">If the **ErrorInfo** property contains "3" (OK), this property is not used.</span></span>

</dd> <dt>

<span data-ttu-id="fcbcb-204">**ErrorTransferSize**</span><span class="sxs-lookup"><span data-stu-id="fcbcb-204">**ErrorTransferSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fcbcb-205">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fcbcb-205">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fcbcb-206">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fcbcb-206">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fcbcb-207">Qualificadores: [**preteridos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ MemoryError. ErrorTransferSize"), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Matriz de memória física da DMTF \| 1,11 "), **PUnit** (" bit ")</span><span class="sxs-lookup"><span data-stu-id="fcbcb-207">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM\_MemoryError.ErrorTransferSize"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bits"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Physical Memory Array\|001.11"), **PUnit** ("bit")</span></span>
</dt> </dl>

<span data-ttu-id="fcbcb-208">O tamanho da transferência de dados, em bits, que causou o último erro.</span><span class="sxs-lookup"><span data-stu-id="fcbcb-208">The size of the data transfer, in bits, that caused the last error.</span></span> <span data-ttu-id="fcbcb-209">"0" indica que não há erro.</span><span class="sxs-lookup"><span data-stu-id="fcbcb-209">"0" indicates no error.</span></span> <span data-ttu-id="fcbcb-210">Se a propriedade **errorInfo** contiver "3" (OK), essa propriedade não será usada.</span><span class="sxs-lookup"><span data-stu-id="fcbcb-210">If the **ErrorInfo** property contains "3" (OK), this property is not used.</span></span>

</dd> <dt>

<span data-ttu-id="fcbcb-211">**OtherErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="fcbcb-211">**OtherErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fcbcb-212">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="fcbcb-212">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fcbcb-213">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fcbcb-213">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fcbcb-214">Qualificadores: [**preteridos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ MemoryError. OtherErrorDescription"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (**" \_ memória CIM**.**ErrorInfo**")</span><span class="sxs-lookup"><span data-stu-id="fcbcb-214">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM\_MemoryError.OtherErrorDescription"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Memory**.**ErrorInfo**")</span></span>
</dt> </dl>

<span data-ttu-id="fcbcb-215">Uma descrição do tipo de erro, quando a propriedade **ErrorType** é definida como "1" (Other).</span><span class="sxs-lookup"><span data-stu-id="fcbcb-215">A description of the error type, when the **ErrorType** property is set to "1" (other).</span></span>

</dd> <dt>

<span data-ttu-id="fcbcb-216">**StartingAddress**</span><span class="sxs-lookup"><span data-stu-id="fcbcb-216">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fcbcb-217">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="fcbcb-217">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="fcbcb-218">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fcbcb-218">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fcbcb-219">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("quilobytes"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. Os \| endereços mapeados da matriz de memória DMTF \| 1,3 "," MIF. \|Endereços mapeados do dispositivo de memória DMTF \| 1,4 "), **PUnit** (" byte \* 10 ^ 3 ")</span><span class="sxs-lookup"><span data-stu-id="fcbcb-219">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("KiloBytes"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Array Mapped Addresses\|001.3", "MIF.DMTF\|Memory Device Mapped Addresses\|001.4"), **PUnit** ("byte \* 10^3")</span></span>
</dt> </dl>

<span data-ttu-id="fcbcb-220">O endereço inicial que é referenciado por um aplicativo ou sistema operacional e é mapeado por um controlador de memória para o objeto de memória.</span><span class="sxs-lookup"><span data-stu-id="fcbcb-220">The starting address that is referenced by an application or operating system, and mapped by a memory controller for the memory object.</span></span> <span data-ttu-id="fcbcb-221">O endereço inicial é especificado em kilobytes.</span><span class="sxs-lookup"><span data-stu-id="fcbcb-221">The starting address is specified in kilobytes.</span></span>

</dd> <dt>

<span data-ttu-id="fcbcb-222">**SystemLevelAddress**</span><span class="sxs-lookup"><span data-stu-id="fcbcb-222">**SystemLevelAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fcbcb-223">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="fcbcb-223">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="fcbcb-224">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fcbcb-224">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fcbcb-225">Qualificadores: [**preteridos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_MemoryError.SystemLevelAddress")</span><span class="sxs-lookup"><span data-stu-id="fcbcb-225">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM\_MemoryError.SystemLevelAddress")</span></span>
</dt> </dl>

<span data-ttu-id="fcbcb-226">**true** se as informações de endereço na propriedade **ErrorAddress** forem um endereço de nível de sistema, **false** se for um endereço físico.</span><span class="sxs-lookup"><span data-stu-id="fcbcb-226">**true** if the address information in the **ErrorAddress** property is a system-level address, **false** if it is a physical address.</span></span>

</dd> <dt>

<span data-ttu-id="fcbcb-227">**Volátil**</span><span class="sxs-lookup"><span data-stu-id="fcbcb-227">**Volatile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fcbcb-228">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="fcbcb-228">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="fcbcb-229">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fcbcb-229">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fcbcb-230">**true** se a memória for volátil; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="fcbcb-230">**true** if the memory is volatile; otherwise, **false**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fcbcb-231">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fcbcb-231">Requirements</span></span>



| <span data-ttu-id="fcbcb-232">Requisito</span><span class="sxs-lookup"><span data-stu-id="fcbcb-232">Requirement</span></span> | <span data-ttu-id="fcbcb-233">Valor</span><span class="sxs-lookup"><span data-stu-id="fcbcb-233">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fcbcb-234">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fcbcb-234">Minimum supported client</span></span><br/> | <span data-ttu-id="fcbcb-235">Windows 8</span><span class="sxs-lookup"><span data-stu-id="fcbcb-235">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="fcbcb-236">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fcbcb-236">Minimum supported server</span></span><br/> | <span data-ttu-id="fcbcb-237">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="fcbcb-237">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="fcbcb-238">Namespace</span><span class="sxs-lookup"><span data-stu-id="fcbcb-238">Namespace</span></span><br/>                | <span data-ttu-id="fcbcb-239">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="fcbcb-239">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="fcbcb-240">MOF</span><span class="sxs-lookup"><span data-stu-id="fcbcb-240">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fcbcb-241"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fcbcb-241"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="fcbcb-242">DLL</span><span class="sxs-lookup"><span data-stu-id="fcbcb-242">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fcbcb-243"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="fcbcb-243"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="fcbcb-244">Confira também</span><span class="sxs-lookup"><span data-stu-id="fcbcb-244">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fcbcb-245">**\_STORAGEEXTENT CIM**</span><span class="sxs-lookup"><span data-stu-id="fcbcb-245">**CIM\_StorageExtent**</span></span>](cim-storageextent.md)
</dt> </dl>

 

