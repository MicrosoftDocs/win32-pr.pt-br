---
description: Evento de rastreamento de gerenciamento de memória para uma operação de alocação de heap.
ms.assetid: 572DEC3B-F909-45E5-849F-707AA62F2F5E
title: ETW_HEAP_EVENT_ALLOC evento (Ntwmi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ETW_HEAP_EVENT_ALLOC
api_type:
- HeaderDef
api_location:
- ntwmi.h
ms.openlocfilehash: 57e09ed1785f31b6203c526f2b6d42cc4815a266
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296373"
---
# <a name="etw_heap_event_alloc-event"></a><span data-ttu-id="6855d-103">\_Evento de \_ alocação de evento de heap do ETW \_</span><span class="sxs-lookup"><span data-stu-id="6855d-103">ETW\_HEAP\_EVENT\_ALLOC event</span></span>

<span data-ttu-id="6855d-104">O evento de alocação de evento de heap do ETW é um evento de rastreamento de gerenciamento de memória para uma operação de alocação de heap. **\_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="6855d-104">The **ETW\_HEAP\_EVENT\_ALLOC** event is a memory management tracing event for a heap allocation operation.</span></span>


```C++
typedef struct ETW_HEAP_EVENT_ALLOC
```



## <a name="parameters"></a><span data-ttu-id="6855d-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6855d-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6855d-106">*HeapHandle*</span><span class="sxs-lookup"><span data-stu-id="6855d-106">*HeapHandle*</span></span> 
</dt> <dd>

<span data-ttu-id="6855d-107">O identificador do heap em que a memória foi alocada.</span><span class="sxs-lookup"><span data-stu-id="6855d-107">The handle of the heap where the memory was allocated.</span></span> <span data-ttu-id="6855d-108">Esse é o identificador de heap que um aplicativo passou para a função [**AllocateHeap**](/previous-versions/windows/desktop/legacy/aa374721(v=vs.85)) quando a memória foi alocada.</span><span class="sxs-lookup"><span data-stu-id="6855d-108">This is the heap handle an app passed to the [**AllocateHeap**](/previous-versions/windows/desktop/legacy/aa374721(v=vs.85)) function when the memory was allocated.</span></span>

</dd> <dt>

<span data-ttu-id="6855d-109">*Tamanho*</span><span class="sxs-lookup"><span data-stu-id="6855d-109">*Size*</span></span> 
</dt> <dd>

<span data-ttu-id="6855d-110">O tamanho em bytes alocado a partir do heap.</span><span class="sxs-lookup"><span data-stu-id="6855d-110">The size in bytes allocated from the heap.</span></span>

</dd> <dt>

<span data-ttu-id="6855d-111">*Endereço*</span><span class="sxs-lookup"><span data-stu-id="6855d-111">*Address*</span></span> 
</dt> <dd>

<span data-ttu-id="6855d-112">O endereço da memória que foi alocada.</span><span class="sxs-lookup"><span data-stu-id="6855d-112">The address of the memory that was allocated.</span></span>

</dd> <dt>

<span data-ttu-id="6855d-113">*Origem*</span><span class="sxs-lookup"><span data-stu-id="6855d-113">*Source*</span></span> 
</dt> <dd>

<span data-ttu-id="6855d-114">A origem da memória que o alocador usou para a alocação de heap.</span><span class="sxs-lookup"><span data-stu-id="6855d-114">The source of the memory that the allocator used for the heap allocation.</span></span>

<span data-ttu-id="6855d-115">A tabela a seguir lista os possíveis valores para o parâmetro de *origem* , conforme definido no arquivo de cabeçalho *ntetw. h* :</span><span class="sxs-lookup"><span data-stu-id="6855d-115">The following table lists the possible values for the *Source* parameter as defined in the *ntetw.h* header file:</span></span>



| <span data-ttu-id="6855d-116">Valor</span><span class="sxs-lookup"><span data-stu-id="6855d-116">Value</span></span>                                                                                                                                                                                                                                                                               | <span data-ttu-id="6855d-117">Significado</span><span class="sxs-lookup"><span data-stu-id="6855d-117">Meaning</span></span>                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span id="MEMORY_FROM_LOOKASIDE"></span><span id="memory_from_lookaside"></span><dl> <span data-ttu-id="6855d-118"><dt>**Memória \_ do DA \_ parte da**</dt> parte <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="6855d-118"><dt>**MEMORY\_FROM\_LOOKASIDE**</dt> <dt>1</dt></span></span> </dl>                                       | <span data-ttu-id="6855d-119">Memória da lista à parte.</span><span class="sxs-lookup"><span data-stu-id="6855d-119">Memory from the lookaside list.</span></span><br/>                                   |
| <span id="MEMORY_FROM_LOWFRAG"></span><span id="memory_from_lowfrag"></span><dl> <span data-ttu-id="6855d-120"><dt>**Memória \_ do DO \_ LOWFRAG**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="6855d-120"><dt>**MEMORY\_FROM\_LOWFRAG**</dt> <dt>2</dt></span></span> </dl>                                             | <span data-ttu-id="6855d-121">Memória do heap de baixa fragmentação.</span><span class="sxs-lookup"><span data-stu-id="6855d-121">Memory from the low-fragmentation heap.</span></span><br/>                           |
| <span id="MEMORY_FROM_MAINPATH"></span><span id="memory_from_mainpath"></span><dl> <span data-ttu-id="6855d-122"><dt>**Memória \_ do DO \_ MAINPATH**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="6855d-122"><dt>**MEMORY\_FROM\_MAINPATH**</dt> <dt>3</dt></span></span> </dl>                                          | <span data-ttu-id="6855d-123">Memória do caminho de código principal.</span><span class="sxs-lookup"><span data-stu-id="6855d-123">Memory from main code path.</span></span><br/>                                       |
| <span id="MEMORY_FROM_SLOWPATH____________________"></span><span id="memory_from_slowpath____________________"></span><dl> <span data-ttu-id="6855d-124"><dt> **Memória \_ do \_ SLOWPATH**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="6855d-124"><dt>**MEMORY\_FROM\_SLOWPATH** </dt> <dt>4</dt></span></span> </dl> | <span data-ttu-id="6855d-125">Memória do caminho lento.</span><span class="sxs-lookup"><span data-stu-id="6855d-125">Memory from slow path.</span></span><br/>                                            |
| <span id="MEMORY_FROM_INVALID"></span><span id="memory_from_invalid"></span><dl> <span data-ttu-id="6855d-126"><dt>**Memória \_ do DE \_**</dt> <dt>5</dt> inválido</span><span class="sxs-lookup"><span data-stu-id="6855d-126"><dt>**MEMORY\_FROM\_INVALID**</dt> <dt>5</dt></span></span> </dl>                                             | <span data-ttu-id="6855d-127">Memória inválida.</span><span class="sxs-lookup"><span data-stu-id="6855d-127">Memory that was not valid.</span></span><br/>                                        |
| <span id="MEMORY_FROM_SEGMENT_HEAP"></span><span id="memory_from_segment_heap"></span><dl> <span data-ttu-id="6855d-128"><dt>**Memória \_ do DO \_ \_ heap de segmento**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="6855d-128"><dt>**MEMORY\_FROM\_SEGMENT\_HEAP**</dt> <dt>6</dt></span></span> </dl>                             | <span data-ttu-id="6855d-129">Esse valor é reservado para uso futuro e nunca será retornado.</span><span class="sxs-lookup"><span data-stu-id="6855d-129">This value is reserved for future use and will never be returned.</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6855d-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="6855d-130">Remarks</span></span>

<span data-ttu-id="6855d-131">O evento de alocação de eventos de heap do ETW é registrado em todas as alocações de heap. **\_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="6855d-131">The **ETW\_HEAP\_EVENT\_ALLOC** event is logged on all heap allocations.</span></span>

## <a name="requirements"></a><span data-ttu-id="6855d-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6855d-132">Requirements</span></span>



| <span data-ttu-id="6855d-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="6855d-133">Requirement</span></span> | <span data-ttu-id="6855d-134">Valor</span><span class="sxs-lookup"><span data-stu-id="6855d-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6855d-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6855d-135">Minimum supported client</span></span><br/> | <span data-ttu-id="6855d-136">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="6855d-136">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="6855d-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6855d-137">Minimum supported server</span></span><br/> | <span data-ttu-id="6855d-138">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="6855d-138">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="6855d-139">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6855d-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="6855d-140"><dt>Ntwmi. h</dt></span><span class="sxs-lookup"><span data-stu-id="6855d-140"><dt>Ntwmi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6855d-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="6855d-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6855d-142">Eventos de rastreamento de gerenciamento de memória</span><span class="sxs-lookup"><span data-stu-id="6855d-142">Memory Management Tracing Events</span></span>](memory-management-tracing-events.md)
</dt> </dl>

 

 
