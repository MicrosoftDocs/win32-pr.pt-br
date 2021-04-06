---
description: Evento de rastreamento de gerenciamento de memória para uma operação de heap livre.
ms.assetid: 0CCC59F1-AB96-4B7A-9A86-19CA4FBA4A8A
title: ETW_HEAP_EVENT_FREE evento (Ntwmi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ETW_HEAP_EVENT_FREE
api_type:
- HeaderDef
api_location:
- ntwmi.h
ms.openlocfilehash: fd30eccb5848917d752441df79881078dc14d36e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827043"
---
# <a name="etw_heap_event_free-event"></a><span data-ttu-id="0881b-103">\_ \_ Evento gratuito de evento de heap do ETW \_</span><span class="sxs-lookup"><span data-stu-id="0881b-103">ETW\_HEAP\_EVENT\_FREE event</span></span>

<span data-ttu-id="0881b-104">O **evento \_ \_ \_ gratuito do evento de heap do ETW** é um evento de rastreamento de gerenciamento de memória para uma operação de heap livre.</span><span class="sxs-lookup"><span data-stu-id="0881b-104">The **ETW\_HEAP\_EVENT\_FREE** event is a memory management tracing event for a heap free operation.</span></span>


```C++
typedef struct ETW_HEAP_EVENT_FREE
```



## <a name="parameters"></a><span data-ttu-id="0881b-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0881b-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0881b-106">*HeapHandle*</span><span class="sxs-lookup"><span data-stu-id="0881b-106">*HeapHandle*</span></span> 
</dt> <dd>

<span data-ttu-id="0881b-107">O identificador do heap em que a memória foi alocada.</span><span class="sxs-lookup"><span data-stu-id="0881b-107">The handle of the heap where the memory was allocated.</span></span> <span data-ttu-id="0881b-108">Esse é o identificador de heap que um aplicativo passou para a função [**AllocateHeap**](/previous-versions/windows/desktop/legacy/aa374721(v=vs.85)) quando a memória foi alocada.</span><span class="sxs-lookup"><span data-stu-id="0881b-108">This is the heap handle an app passed to the [**AllocateHeap**](/previous-versions/windows/desktop/legacy/aa374721(v=vs.85)) function when the memory was allocated.</span></span>

</dd> <dt>

<span data-ttu-id="0881b-109">*Endereço*</span><span class="sxs-lookup"><span data-stu-id="0881b-109">*Address*</span></span> 
</dt> <dd>

<span data-ttu-id="0881b-110">O endereço da memória que foi liberada.</span><span class="sxs-lookup"><span data-stu-id="0881b-110">The address of the memory that was freed.</span></span>

</dd> <dt>

<span data-ttu-id="0881b-111">*Origem*</span><span class="sxs-lookup"><span data-stu-id="0881b-111">*Source*</span></span> 
</dt> <dd>

<span data-ttu-id="0881b-112">A origem da memória que o alocador usou para a alocação de heap.</span><span class="sxs-lookup"><span data-stu-id="0881b-112">The source of the memory that the allocator used for the heap allocation.</span></span>

<span data-ttu-id="0881b-113">A tabela a seguir lista os possíveis valores para o parâmetro de *origem* , conforme definido no arquivo de cabeçalho *ntetw. h* :</span><span class="sxs-lookup"><span data-stu-id="0881b-113">The following table lists the possible values for the *Source* parameter as defined in the *ntetw.h* header file:</span></span>



| <span data-ttu-id="0881b-114">Valor</span><span class="sxs-lookup"><span data-stu-id="0881b-114">Value</span></span>                                                                                                                                                                                                                                                                               | <span data-ttu-id="0881b-115">Significado</span><span class="sxs-lookup"><span data-stu-id="0881b-115">Meaning</span></span>                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span id="MEMORY_FROM_LOOKASIDE"></span><span id="memory_from_lookaside"></span><dl> <span data-ttu-id="0881b-116"><dt>**Memória \_ do DA \_ parte da**</dt> parte <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="0881b-116"><dt>**MEMORY\_FROM\_LOOKASIDE**</dt> <dt>1</dt></span></span> </dl>                                       | <span data-ttu-id="0881b-117">Memória da lista à parte.</span><span class="sxs-lookup"><span data-stu-id="0881b-117">Memory from the lookaside list.</span></span><br/>                                   |
| <span id="MEMORY_FROM_LOWFRAG"></span><span id="memory_from_lowfrag"></span><dl> <span data-ttu-id="0881b-118"><dt>**Memória \_ do DO \_ LOWFRAG**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="0881b-118"><dt>**MEMORY\_FROM\_LOWFRAG**</dt> <dt>2</dt></span></span> </dl>                                             | <span data-ttu-id="0881b-119">Memória do heap de baixa fragmentação.</span><span class="sxs-lookup"><span data-stu-id="0881b-119">Memory from the low-fragmentation heap.</span></span><br/>                           |
| <span id="MEMORY_FROM_MAINPATH"></span><span id="memory_from_mainpath"></span><dl> <span data-ttu-id="0881b-120"><dt>**Memória \_ do DO \_ MAINPATH**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="0881b-120"><dt>**MEMORY\_FROM\_MAINPATH**</dt> <dt>3</dt></span></span> </dl>                                          | <span data-ttu-id="0881b-121">Memória do caminho de código principal.</span><span class="sxs-lookup"><span data-stu-id="0881b-121">Memory from main code path.</span></span><br/>                                       |
| <span id="MEMORY_FROM_SLOWPATH____________________"></span><span id="memory_from_slowpath____________________"></span><dl> <span data-ttu-id="0881b-122"><dt> **Memória \_ do \_ SLOWPATH**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="0881b-122"><dt>**MEMORY\_FROM\_SLOWPATH** </dt> <dt>4</dt></span></span> </dl> | <span data-ttu-id="0881b-123">Memória de c lento.</span><span class="sxs-lookup"><span data-stu-id="0881b-123">Memory from slow c.</span></span><br/>                                               |
| <span id="MEMORY_FROM_INVALID"></span><span id="memory_from_invalid"></span><dl> <span data-ttu-id="0881b-124"><dt>**Memória \_ do DE \_**</dt> <dt>5</dt> inválido</span><span class="sxs-lookup"><span data-stu-id="0881b-124"><dt>**MEMORY\_FROM\_INVALID**</dt> <dt>5</dt></span></span> </dl>                                             | <span data-ttu-id="0881b-125">Memória inválida.</span><span class="sxs-lookup"><span data-stu-id="0881b-125">Memory that was not valid.</span></span><br/>                                        |
| <span id="MEMORY_FROM_SEGMENT_HEAP"></span><span id="memory_from_segment_heap"></span><dl> <span data-ttu-id="0881b-126"><dt>**Memória \_ do DO \_ \_ heap de segmento**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="0881b-126"><dt>**MEMORY\_FROM\_SEGMENT\_HEAP**</dt> <dt>6</dt></span></span> </dl>                             | <span data-ttu-id="0881b-127">Esse valor é reservado para uso futuro e nunca será retornado.</span><span class="sxs-lookup"><span data-stu-id="0881b-127">This value is reserved for future use and will never be returned.</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0881b-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="0881b-128">Remarks</span></span>

<span data-ttu-id="0881b-129">O **evento \_ \_ \_ gratuito do evento de heap do ETW** é registrado em todas as operações livres de heap.</span><span class="sxs-lookup"><span data-stu-id="0881b-129">The **ETW\_HEAP\_EVENT\_FREE** event is logged on all heap free operations.</span></span>

## <a name="requirements"></a><span data-ttu-id="0881b-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0881b-130">Requirements</span></span>



| <span data-ttu-id="0881b-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="0881b-131">Requirement</span></span> | <span data-ttu-id="0881b-132">Valor</span><span class="sxs-lookup"><span data-stu-id="0881b-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0881b-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0881b-133">Minimum supported client</span></span><br/> | <span data-ttu-id="0881b-134">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="0881b-134">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="0881b-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0881b-135">Minimum supported server</span></span><br/> | <span data-ttu-id="0881b-136">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="0881b-136">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="0881b-137">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0881b-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="0881b-138"><dt>Ntwmi. h</dt></span><span class="sxs-lookup"><span data-stu-id="0881b-138"><dt>Ntwmi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0881b-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="0881b-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0881b-140">Eventos de rastreamento de gerenciamento de memória</span><span class="sxs-lookup"><span data-stu-id="0881b-140">Memory Management Tracing Events</span></span>](memory-management-tracing-events.md)
</dt> </dl>

 

 
