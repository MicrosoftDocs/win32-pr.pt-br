---
description: Essa classe é a classe de tipo de evento para eventos de contador de processo. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: 7f1fa1c4-a2ff-4a1c-ac9d-e922a13c99a1
title: Classe Process_V2_TypeGroup2
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Process_V2_TypeGroup2
- Process_V2_TypeGroup2.ProcessId
- Process_V2_TypeGroup2.PageFaultCount
- Process_V2_TypeGroup2.HandleCount
- Process_V2_TypeGroup2.Reserved
- Process_V2_TypeGroup2.PeakVirtualSize
- Process_V2_TypeGroup2.PeakWorkingSetSize
- Process_V2_TypeGroup2.PeakPagefileUsage
- Process_V2_TypeGroup2.QuotaPeakPagedPoolUsage
- Process_V2_TypeGroup2.QuotaPeakNonPagedPoolUsage
- Process_V2_TypeGroup2.VirtualSize
- Process_V2_TypeGroup2.WorkingSetSize
- Process_V2_TypeGroup2.PagefileUsage
- Process_V2_TypeGroup2.QuotaPagedPoolUsage
- Process_V2_TypeGroup2.QuotaNonPagedPoolUsage
- Process_V2_TypeGroup2.PrivatePageCount
api_type:
- NA
api_location: ''
ms.openlocfilehash: 284b77da03b53f9c2662c8729a7bf6606c45630a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829683"
---
# <a name="process_v2_typegroup2-class"></a><span data-ttu-id="f1613-104">\_Classe Process v2 \_ TypeGroup2</span><span class="sxs-lookup"><span data-stu-id="f1613-104">Process\_V2\_TypeGroup2 class</span></span>

<span data-ttu-id="f1613-105">Essa classe é a classe de tipo de evento para eventos de contador de processo.</span><span class="sxs-lookup"><span data-stu-id="f1613-105">This class is the event type class for process counter events.</span></span>

<span data-ttu-id="f1613-106">A sintaxe a seguir é simplificada do código MOF.</span><span class="sxs-lookup"><span data-stu-id="f1613-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1613-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f1613-107">Syntax</span></span>

``` syntax
[EventType{32, 33}, EventTypeName{"PerfCtr", PerfCtrRundown"}]
class Process_V2_TypeGroup2 : Process_V2
{
  uint32 ProcessId;
  uint32 PageFaultCount;
  uint32 HandleCount;
  uint32 Reserved;
  object PeakVirtualSize;
  object PeakWorkingSetSize;
  object PeakPagefileUsage;
  object QuotaPeakPagedPoolUsage;
  object QuotaPeakNonPagedPoolUsage;
  object VirtualSize;
  object WorkingSetSize;
  object PagefileUsage;
  object QuotaPagedPoolUsage;
  object QuotaNonPagedPoolUsage;
  object PrivatePageCount;
};
```

## <a name="members"></a><span data-ttu-id="f1613-108">Membros</span><span class="sxs-lookup"><span data-stu-id="f1613-108">Members</span></span>

<span data-ttu-id="f1613-109">A classe **process \_ v2 \_ TypeGroup2** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="f1613-109">The **Process\_V2\_TypeGroup2** class has these types of members:</span></span>

-   [<span data-ttu-id="f1613-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="f1613-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f1613-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="f1613-111">Properties</span></span>

<span data-ttu-id="f1613-112">A classe **process \_ v2 \_ TypeGroup2** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="f1613-112">The **Process\_V2\_TypeGroup2** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f1613-113">**HandleCount**</span><span class="sxs-lookup"><span data-stu-id="f1613-113">**HandleCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1613-114">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f1613-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f1613-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f1613-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1613-116">Qualificadores: WmiDataId (3)</span><span class="sxs-lookup"><span data-stu-id="f1613-116">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="f1613-117">Contagem de identificadores usados.</span><span class="sxs-lookup"><span data-stu-id="f1613-117">Count of used handles.</span></span>

</dd> <dt>

<span data-ttu-id="f1613-118">**PageFaultCount**</span><span class="sxs-lookup"><span data-stu-id="f1613-118">**PageFaultCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1613-119">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f1613-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f1613-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f1613-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1613-121">Qualificadores: WmiDataId (2)</span><span class="sxs-lookup"><span data-stu-id="f1613-121">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="f1613-122">Contagem de falhas de página.</span><span class="sxs-lookup"><span data-stu-id="f1613-122">Count of page faults.</span></span>

</dd> <dt>

<span data-ttu-id="f1613-123">**PagefileUsage**</span><span class="sxs-lookup"><span data-stu-id="f1613-123">**PagefileUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1613-124">Tipo de dados: **objeto**</span><span class="sxs-lookup"><span data-stu-id="f1613-124">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="f1613-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f1613-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1613-126">Qualificadores: WmiDataId (12), extensão ("tamanho")</span><span class="sxs-lookup"><span data-stu-id="f1613-126">Qualifiers: WmiDataId(12), Extension("SizeT")</span></span>
</dt> </dl>

<span data-ttu-id="f1613-127">Uso do arquivo de paginação atual.</span><span class="sxs-lookup"><span data-stu-id="f1613-127">Current page file usage.</span></span>

</dd> <dt>

<span data-ttu-id="f1613-128">**PeakPagefileUsage**</span><span class="sxs-lookup"><span data-stu-id="f1613-128">**PeakPagefileUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1613-129">Tipo de dados: **objeto**</span><span class="sxs-lookup"><span data-stu-id="f1613-129">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="f1613-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f1613-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1613-131">Qualificadores: WmiDataId (7), extensão ("Tamanhot")</span><span class="sxs-lookup"><span data-stu-id="f1613-131">Qualifiers: WmiDataId(7), Extension("SizeT")</span></span>
</dt> </dl>

<span data-ttu-id="f1613-132">Tamanho de arquivo de paginação maior usado.</span><span class="sxs-lookup"><span data-stu-id="f1613-132">Largest page file size used.</span></span>

</dd> <dt>

<span data-ttu-id="f1613-133">**PeakVirtualSize**</span><span class="sxs-lookup"><span data-stu-id="f1613-133">**PeakVirtualSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1613-134">Tipo de dados: **objeto**</span><span class="sxs-lookup"><span data-stu-id="f1613-134">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="f1613-135">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f1613-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1613-136">Qualificadores: WmiDataId (5), extensão ("tamanho")</span><span class="sxs-lookup"><span data-stu-id="f1613-136">Qualifiers: WmiDataId(5), Extension("SizeT")</span></span>
</dt> </dl>

<span data-ttu-id="f1613-137">Maior tamanho de página virtual usado.</span><span class="sxs-lookup"><span data-stu-id="f1613-137">Largest virtual page size used.</span></span>

</dd> <dt>

<span data-ttu-id="f1613-138">**PeakWorkingSetSize**</span><span class="sxs-lookup"><span data-stu-id="f1613-138">**PeakWorkingSetSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1613-139">Tipo de dados: **objeto**</span><span class="sxs-lookup"><span data-stu-id="f1613-139">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="f1613-140">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f1613-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1613-141">Qualificadores: WmiDataId (6), extensão ("tamanho")</span><span class="sxs-lookup"><span data-stu-id="f1613-141">Qualifiers: WmiDataId(6), Extension("SizeT")</span></span>
</dt> </dl>

<span data-ttu-id="f1613-142">Maior tamanho de conjunto de trabalho usado.</span><span class="sxs-lookup"><span data-stu-id="f1613-142">Largest working set size used.</span></span>

</dd> <dt>

<span data-ttu-id="f1613-143">**PrivatePageCount**</span><span class="sxs-lookup"><span data-stu-id="f1613-143">**PrivatePageCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1613-144">Tipo de dados: **objeto**</span><span class="sxs-lookup"><span data-stu-id="f1613-144">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="f1613-145">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f1613-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1613-146">Qualificadores: WmiDataId (15), extensão ("tamanho")</span><span class="sxs-lookup"><span data-stu-id="f1613-146">Qualifiers: WmiDataId(15), Extension("SizeT")</span></span>
</dt> </dl>

<span data-ttu-id="f1613-147">Contagem de páginas físicas privadas atuais.</span><span class="sxs-lookup"><span data-stu-id="f1613-147">Current private physical page count.</span></span>

</dd> <dt>

<span data-ttu-id="f1613-148">ProcessId</span><span class="sxs-lookup"><span data-stu-id="f1613-148">ProcessId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1613-149">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f1613-149">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f1613-150">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f1613-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1613-151">Qualificadores: WmiDataId (1), formato ("x")</span><span class="sxs-lookup"><span data-stu-id="f1613-151">Qualifiers: WmiDataId(1), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="f1613-152">Identificador de processo global que você pode usar para identificar um processo.</span><span class="sxs-lookup"><span data-stu-id="f1613-152">Global process identifier that you can use to identify a process.</span></span> <span data-ttu-id="f1613-153">O valor é válido a partir do momento em que um processo é criado até ser encerrado.</span><span class="sxs-lookup"><span data-stu-id="f1613-153">The value is valid from the time a process is created until it is terminated.</span></span>

</dd> <dt>

<span data-ttu-id="f1613-154">**QuotaNonPagedPoolUsage**</span><span class="sxs-lookup"><span data-stu-id="f1613-154">**QuotaNonPagedPoolUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1613-155">Tipo de dados: **objeto**</span><span class="sxs-lookup"><span data-stu-id="f1613-155">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="f1613-156">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f1613-156">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1613-157">Qualificadores: WmiDataId (14), extensão ("Tamanhot")</span><span class="sxs-lookup"><span data-stu-id="f1613-157">Qualifiers: WmiDataId(14), Extension("SizeT")</span></span>
</dt> </dl>

<span data-ttu-id="f1613-158">Uso atual da memória não paginável confirmada.</span><span class="sxs-lookup"><span data-stu-id="f1613-158">Current committed non-paged memory usage.</span></span>

</dd> <dt>

<span data-ttu-id="f1613-159">**QuotaPagedPoolUsage**</span><span class="sxs-lookup"><span data-stu-id="f1613-159">**QuotaPagedPoolUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1613-160">Tipo de dados: **objeto**</span><span class="sxs-lookup"><span data-stu-id="f1613-160">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="f1613-161">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f1613-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1613-162">Qualificadores: WmiDataId (13), extensão ("tamanho")</span><span class="sxs-lookup"><span data-stu-id="f1613-162">Qualifiers: WmiDataId(13), Extension("SizeT")</span></span>
</dt> </dl>

<span data-ttu-id="f1613-163">Uso atual da memória paginável confirmada.</span><span class="sxs-lookup"><span data-stu-id="f1613-163">Current committed paged memory usage.</span></span>

</dd> <dt>

<span data-ttu-id="f1613-164">**QuotaPeakNonPagedPoolUsage**</span><span class="sxs-lookup"><span data-stu-id="f1613-164">**QuotaPeakNonPagedPoolUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1613-165">Tipo de dados: **objeto**</span><span class="sxs-lookup"><span data-stu-id="f1613-165">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="f1613-166">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f1613-166">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1613-167">Qualificadores: WmiDataId (9), extensão ("Tamanhot")</span><span class="sxs-lookup"><span data-stu-id="f1613-167">Qualifiers: WmiDataId(9), Extension("SizeT")</span></span>
</dt> </dl>

<span data-ttu-id="f1613-168">Maior memória confirmada que não foi paginável usada.</span><span class="sxs-lookup"><span data-stu-id="f1613-168">Largest committed non-paged memory used.</span></span>

</dd> <dt>

<span data-ttu-id="f1613-169">**QuotaPeakPagedPoolUsage**</span><span class="sxs-lookup"><span data-stu-id="f1613-169">**QuotaPeakPagedPoolUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1613-170">Tipo de dados: **objeto**</span><span class="sxs-lookup"><span data-stu-id="f1613-170">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="f1613-171">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f1613-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1613-172">Qualificadores: WmiDataId (8), extensão ("tamanho")</span><span class="sxs-lookup"><span data-stu-id="f1613-172">Qualifiers: WmiDataId(8), Extension("SizeT")</span></span>
</dt> </dl>

<span data-ttu-id="f1613-173">Maior memória paginável confirmada usada.</span><span class="sxs-lookup"><span data-stu-id="f1613-173">Largest committed paged memory used.</span></span>

</dd> <dt>

<span data-ttu-id="f1613-174">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="f1613-174">**Reserved**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1613-175">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f1613-175">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f1613-176">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f1613-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1613-177">Qualificadores: WmiDataId (4)</span><span class="sxs-lookup"><span data-stu-id="f1613-177">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="f1613-178">Reservado.</span><span class="sxs-lookup"><span data-stu-id="f1613-178">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="f1613-179">**VirtualSize**</span><span class="sxs-lookup"><span data-stu-id="f1613-179">**VirtualSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1613-180">Tipo de dados: **objeto**</span><span class="sxs-lookup"><span data-stu-id="f1613-180">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="f1613-181">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f1613-181">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1613-182">Qualificadores: WmiDataId (10), extensão ("tamanho")</span><span class="sxs-lookup"><span data-stu-id="f1613-182">Qualifiers: WmiDataId(10), Extension("SizeT")</span></span>
</dt> </dl>

<span data-ttu-id="f1613-183">Tamanho atual da página virtual.</span><span class="sxs-lookup"><span data-stu-id="f1613-183">Current virtual page size.</span></span>

</dd> <dt>

<span data-ttu-id="f1613-184">**WorkingSetSize**</span><span class="sxs-lookup"><span data-stu-id="f1613-184">**WorkingSetSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1613-185">Tipo de dados: **objeto**</span><span class="sxs-lookup"><span data-stu-id="f1613-185">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="f1613-186">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f1613-186">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1613-187">Qualificadores: WmiDataId (11), extensão ("Tamanhot")</span><span class="sxs-lookup"><span data-stu-id="f1613-187">Qualifiers: WmiDataId(11), Extension("SizeT")</span></span>
</dt> </dl>

<span data-ttu-id="f1613-188">Tamanho atual do conjunto de trabalho.</span><span class="sxs-lookup"><span data-stu-id="f1613-188">Current working set size.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f1613-189">Comentários</span><span class="sxs-lookup"><span data-stu-id="f1613-189">Remarks</span></span>

<span data-ttu-id="f1613-190">Esses eventos são registrados quando o processo termina.</span><span class="sxs-lookup"><span data-stu-id="f1613-190">These events are logged when the process ends.</span></span> <span data-ttu-id="f1613-191">O evento indica como um processo tratou de uso de memória.</span><span class="sxs-lookup"><span data-stu-id="f1613-191">The event indicates how a process handled memory usage.</span></span>

## <a name="requirements"></a><span data-ttu-id="f1613-192">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f1613-192">Requirements</span></span>



| <span data-ttu-id="f1613-193">Requisito</span><span class="sxs-lookup"><span data-stu-id="f1613-193">Requirement</span></span> | <span data-ttu-id="f1613-194">Valor</span><span class="sxs-lookup"><span data-stu-id="f1613-194">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f1613-195">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f1613-195">Minimum supported client</span></span><br/> | <span data-ttu-id="f1613-196">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f1613-196">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="f1613-197">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f1613-197">Minimum supported server</span></span><br/> | <span data-ttu-id="f1613-198">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f1613-198">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f1613-199">Confira também</span><span class="sxs-lookup"><span data-stu-id="f1613-199">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1613-200">**Processo \_ v2**</span><span class="sxs-lookup"><span data-stu-id="f1613-200">**Process\_V2**</span></span>](process-v2.md)
</dt> </dl>

 

 




