---
description: Evento de rastreamento de gerenciamento de memória para uma operação de realocação de heap.
ms.assetid: D8080B7B-CECC-40DB-B52A-2C3E4F04ABA9
title: ETW_HEAP_EVENT_REALLOC evento (Ntwmi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ETW_HEAP_EVENT_REALLOC
api_type:
- HeaderDef
api_location:
- ntwmi.h
ms.openlocfilehash: 7aec225793967c38b97fecae88d28141e48a3cfd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105787088"
---
# <a name="etw_heap_event_realloc-event"></a><span data-ttu-id="77370-103">\_Evento de \_ realocação de evento de heap do ETW \_</span><span class="sxs-lookup"><span data-stu-id="77370-103">ETW\_HEAP\_EVENT\_REALLOC event</span></span>

<span data-ttu-id="77370-104">O evento de **\_ \_ \_ realocação do evento de heap do ETW** é um evento de rastreamento de gerenciamento de memória para uma operação de realocação de heap.</span><span class="sxs-lookup"><span data-stu-id="77370-104">The **ETW\_HEAP\_EVENT\_REALLOC** event is a memory management tracing event for a heap reallocation operation.</span></span>


```C++
typedef struct ETW_HEAP_EVENT_REALLOC
```



## <a name="parameters"></a><span data-ttu-id="77370-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="77370-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="77370-106">*HeapHandle*</span><span class="sxs-lookup"><span data-stu-id="77370-106">*HeapHandle*</span></span> 
</dt> <dd>

<span data-ttu-id="77370-107">O identificador do heap em que a memória foi alocada.</span><span class="sxs-lookup"><span data-stu-id="77370-107">The handle of the heap where the memory was allocated.</span></span> <span data-ttu-id="77370-108">Esse é o identificador de heap que um aplicativo passou para a função [**AllocateHeap**](/previous-versions/windows/desktop/legacy/aa374721(v=vs.85)) quando a memória foi alocada.</span><span class="sxs-lookup"><span data-stu-id="77370-108">This is the heap handle an app passed to the [**AllocateHeap**](/previous-versions/windows/desktop/legacy/aa374721(v=vs.85)) function when the memory was allocated.</span></span>

</dd> <dt>

<span data-ttu-id="77370-109">*NewAddress*</span><span class="sxs-lookup"><span data-stu-id="77370-109">*NewAddress*</span></span> 
</dt> <dd>

<span data-ttu-id="77370-110">O novo endereço da memória que foi alocada.</span><span class="sxs-lookup"><span data-stu-id="77370-110">The new address of the memory that was allocated.</span></span>

</dd> <dt>

<span data-ttu-id="77370-111">*OldAddress*</span><span class="sxs-lookup"><span data-stu-id="77370-111">*OldAddress*</span></span> 
</dt> <dd>

<span data-ttu-id="77370-112">O endereço antigo da memória que foi alocada anteriormente.</span><span class="sxs-lookup"><span data-stu-id="77370-112">The old address of the memory that was previously allocated.</span></span>

</dd> <dt>

<span data-ttu-id="77370-113">*NewSize*</span><span class="sxs-lookup"><span data-stu-id="77370-113">*NewSize*</span></span> 
</dt> <dd>

<span data-ttu-id="77370-114">O novo tamanho em bytes alocado a partir do heap.</span><span class="sxs-lookup"><span data-stu-id="77370-114">The new size in bytes allocated from the heap.</span></span>

</dd> <dt>

<span data-ttu-id="77370-115">*OldSize*</span><span class="sxs-lookup"><span data-stu-id="77370-115">*OldSize*</span></span> 
</dt> <dd>

<span data-ttu-id="77370-116">O tamanho antigo em bytes alocados anteriormente do heap.</span><span class="sxs-lookup"><span data-stu-id="77370-116">The old size in bytes previously allocated from the heap.</span></span>

</dd> <dt>

<span data-ttu-id="77370-117">*Origem*</span><span class="sxs-lookup"><span data-stu-id="77370-117">*Source*</span></span> 
</dt> <dd>

<span data-ttu-id="77370-118">A origem da memória que o alocador usou para a alocação de heap.</span><span class="sxs-lookup"><span data-stu-id="77370-118">The source of the memory that the allocator used for the heap allocation.</span></span>

<span data-ttu-id="77370-119">A tabela a seguir lista os possíveis valores para o parâmetro de *origem* , conforme definido no arquivo de cabeçalho *ntetw. h* :</span><span class="sxs-lookup"><span data-stu-id="77370-119">The following table lists the possible values for the *Source* parameter as defined in the *ntetw.h* header file:</span></span>



| <span data-ttu-id="77370-120">Valor</span><span class="sxs-lookup"><span data-stu-id="77370-120">Value</span></span>                                                                                                                                                                                                                                                                               | <span data-ttu-id="77370-121">Significado</span><span class="sxs-lookup"><span data-stu-id="77370-121">Meaning</span></span>                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span id="MEMORY_FROM_LOOKASIDE"></span><span id="memory_from_lookaside"></span><dl> <span data-ttu-id="77370-122"><dt>**Memória \_ do DA \_ parte da**</dt> parte <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="77370-122"><dt>**MEMORY\_FROM\_LOOKASIDE**</dt> <dt>1</dt></span></span> </dl>                                       | <span data-ttu-id="77370-123">Memória da lista à parte.</span><span class="sxs-lookup"><span data-stu-id="77370-123">Memory from the lookaside list.</span></span><br/>                                   |
| <span id="MEMORY_FROM_LOWFRAG"></span><span id="memory_from_lowfrag"></span><dl> <span data-ttu-id="77370-124"><dt>**Memória \_ do DO \_ LOWFRAG**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="77370-124"><dt>**MEMORY\_FROM\_LOWFRAG**</dt> <dt>2</dt></span></span> </dl>                                             | <span data-ttu-id="77370-125">Memória do heap de baixa fragmentação.</span><span class="sxs-lookup"><span data-stu-id="77370-125">Memory from the low-fragmentation heap.</span></span><br/>                           |
| <span id="MEMORY_FROM_MAINPATH"></span><span id="memory_from_mainpath"></span><dl> <span data-ttu-id="77370-126"><dt>**Memória \_ do DO \_ MAINPATH**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="77370-126"><dt>**MEMORY\_FROM\_MAINPATH**</dt> <dt>3</dt></span></span> </dl>                                          | <span data-ttu-id="77370-127">Memória do caminho de código principal.</span><span class="sxs-lookup"><span data-stu-id="77370-127">Memory from main code path.</span></span><br/>                                       |
| <span id="MEMORY_FROM_SLOWPATH____________________"></span><span id="memory_from_slowpath____________________"></span><dl> <span data-ttu-id="77370-128"><dt> **Memória \_ do \_ SLOWPATH**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="77370-128"><dt>**MEMORY\_FROM\_SLOWPATH** </dt> <dt>4</dt></span></span> </dl> | <span data-ttu-id="77370-129">Memória de c lento.</span><span class="sxs-lookup"><span data-stu-id="77370-129">Memory from slow c.</span></span><br/>                                               |
| <span id="MEMORY_FROM_INVALID"></span><span id="memory_from_invalid"></span><dl> <span data-ttu-id="77370-130"><dt>**Memória \_ do DE \_**</dt> <dt>5</dt> inválido</span><span class="sxs-lookup"><span data-stu-id="77370-130"><dt>**MEMORY\_FROM\_INVALID**</dt> <dt>5</dt></span></span> </dl>                                             | <span data-ttu-id="77370-131">Memória inválida.</span><span class="sxs-lookup"><span data-stu-id="77370-131">Memory that was not valid.</span></span><br/>                                        |
| <span id="MEMORY_FROM_SEGMENT_HEAP"></span><span id="memory_from_segment_heap"></span><dl> <span data-ttu-id="77370-132"><dt>**Memória \_ do DO \_ \_ heap de segmento**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="77370-132"><dt>**MEMORY\_FROM\_SEGMENT\_HEAP**</dt> <dt>6</dt></span></span> </dl>                             | <span data-ttu-id="77370-133">Esse valor é reservado para uso futuro e nunca será retornado.</span><span class="sxs-lookup"><span data-stu-id="77370-133">This value is reserved for future use and will never be returned.</span></span><br/> |



 

</dd> </dl>

<span data-ttu-id="77370-134">Este evento não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="77370-134">This event has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="77370-135">Comentários</span><span class="sxs-lookup"><span data-stu-id="77370-135">Remarks</span></span>

<span data-ttu-id="77370-136">O evento de **\_ \_ \_ realocação do evento de heap do ETW** é registrado em todas as realocações de heap.</span><span class="sxs-lookup"><span data-stu-id="77370-136">The **ETW\_HEAP\_EVENT\_REALLOC** event is logged on all heap reallocations.</span></span>

## <a name="requirements"></a><span data-ttu-id="77370-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="77370-137">Requirements</span></span>



| <span data-ttu-id="77370-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="77370-138">Requirement</span></span> | <span data-ttu-id="77370-139">Valor</span><span class="sxs-lookup"><span data-stu-id="77370-139">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="77370-140">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="77370-140">Minimum supported client</span></span><br/> | <span data-ttu-id="77370-141">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="77370-141">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="77370-142">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="77370-142">Minimum supported server</span></span><br/> | <span data-ttu-id="77370-143">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="77370-143">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="77370-144">parâmetro</span><span class="sxs-lookup"><span data-stu-id="77370-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="77370-145"><dt>Ntwmi. h</dt></span><span class="sxs-lookup"><span data-stu-id="77370-145"><dt>Ntwmi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="77370-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="77370-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77370-147">Eventos de rastreamento de gerenciamento de memória</span><span class="sxs-lookup"><span data-stu-id="77370-147">Memory Management Tracing Events</span></span>](memory-management-tracing-events.md)
</dt> </dl>

 

 
