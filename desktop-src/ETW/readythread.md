---
description: Essa classe é a classe de tipo de evento para eventos de thread prontos. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: 861ab070-5536-4897-b523-9b09a7d59b3e
title: Classe ReadyThread
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ReadyThread
- ReadyThread.TThreadId
- ReadyThread.AdjustReason
- ReadyThread.AdjustIncrement
- ReadyThread.Flag
- ReadyThread.Reserved
api_type:
- NA
api_location: ''
ms.openlocfilehash: e10029c0397c16a5a5eb30be6e3db64c0baec596
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827268"
---
# <a name="readythread-class"></a><span data-ttu-id="567c3-104">Classe ReadyThread</span><span class="sxs-lookup"><span data-stu-id="567c3-104">ReadyThread class</span></span>

<span data-ttu-id="567c3-105">Essa classe é a classe de tipo de evento para eventos de thread prontos.</span><span class="sxs-lookup"><span data-stu-id="567c3-105">This class is the event type class for ready thread events.</span></span>

<span data-ttu-id="567c3-106">A sintaxe a seguir é simplificada do código MOF.</span><span class="sxs-lookup"><span data-stu-id="567c3-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="567c3-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="567c3-107">Syntax</span></span>

``` syntax
[EventType{50}, EventTypeName{"ReadyThread"}]
class ReadyThread : Thread_V2
{
  uint32 TThreadId;
  sint8  AdjustReason;
  sint8  AdjustIncrement;
  sint8  Flag;
  sint8  Reserved;
};
```

## <a name="members"></a><span data-ttu-id="567c3-108">Membros</span><span class="sxs-lookup"><span data-stu-id="567c3-108">Members</span></span>

<span data-ttu-id="567c3-109">A classe **ReadyThread** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="567c3-109">The **ReadyThread** class has these types of members:</span></span>

-   [<span data-ttu-id="567c3-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="567c3-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="567c3-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="567c3-111">Properties</span></span>

<span data-ttu-id="567c3-112">A classe **ReadyThread** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="567c3-112">The **ReadyThread** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="567c3-113">AdjustIncrement</span><span class="sxs-lookup"><span data-stu-id="567c3-113">AdjustIncrement</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="567c3-114">Tipo de dados: **sint8**</span><span class="sxs-lookup"><span data-stu-id="567c3-114">Data type: **sint8**</span></span>
</dt> <dt>

<span data-ttu-id="567c3-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="567c3-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="567c3-116">Qualificadores: WmiDataId (3)</span><span class="sxs-lookup"><span data-stu-id="567c3-116">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="567c3-117">O valor pelo qual a prioridade está sendo ajustada.</span><span class="sxs-lookup"><span data-stu-id="567c3-117">The value by which the priority is being adjusted.</span></span>

</dd> <dt>

<span data-ttu-id="567c3-118">AdjustReason</span><span class="sxs-lookup"><span data-stu-id="567c3-118">AdjustReason</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="567c3-119">Tipo de dados: **sint8**</span><span class="sxs-lookup"><span data-stu-id="567c3-119">Data type: **sint8**</span></span>
</dt> <dt>

<span data-ttu-id="567c3-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="567c3-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="567c3-121">Qualificadores: WmiDataId (2)</span><span class="sxs-lookup"><span data-stu-id="567c3-121">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="567c3-122">O motivo para o aumento de prioridade.</span><span class="sxs-lookup"><span data-stu-id="567c3-122">The reason for the priority boost.</span></span>



| <span data-ttu-id="567c3-123">Valor</span><span class="sxs-lookup"><span data-stu-id="567c3-123">Value</span></span>                                                                        | <span data-ttu-id="567c3-124">Significado</span><span class="sxs-lookup"><span data-stu-id="567c3-124">Meaning</span></span>                                                                                                                 |
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="567c3-125"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="567c3-125"><dt>0</dt></span></span> </dl> | <span data-ttu-id="567c3-126">Ignore o incremento.</span><span class="sxs-lookup"><span data-stu-id="567c3-126">Ignore the increment.</span></span><br/>                                                                                        |
| <dl> <span data-ttu-id="567c3-127"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="567c3-127"><dt>1</dt></span></span> </dl> | <span data-ttu-id="567c3-128">Aplique o incremento, que irá decaimento incrementalmente ao final de cada Quantum.</span><span class="sxs-lookup"><span data-stu-id="567c3-128">Apply the increment, which will decay incrementally at the end of each quantum.</span></span><br/>                              |
| <dl> <span data-ttu-id="567c3-129"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="567c3-129"><dt>2</dt></span></span> </dl> | <span data-ttu-id="567c3-130">Aplique o incremento como um aumento que será decaimentodo em sua totalidade no Quantum (normalmente para doação de prioridade).</span><span class="sxs-lookup"><span data-stu-id="567c3-130">Apply the increment as a boost that will decay in its entirety at quantum (typically for priority donation).</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="567c3-131">Sinalizador</span><span class="sxs-lookup"><span data-stu-id="567c3-131">Flag</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="567c3-132">Tipo de dados: **sint8**</span><span class="sxs-lookup"><span data-stu-id="567c3-132">Data type: **sint8**</span></span>
</dt> <dt>

<span data-ttu-id="567c3-133">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="567c3-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="567c3-134">Qualificadores: WmiDataId (4)</span><span class="sxs-lookup"><span data-stu-id="567c3-134">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="567c3-135">A seguir estão os possíveis sinalizadores de Estado:</span><span class="sxs-lookup"><span data-stu-id="567c3-135">The following are the possible state flags:</span></span>



| <span data-ttu-id="567c3-136">Valor</span><span class="sxs-lookup"><span data-stu-id="567c3-136">Value</span></span>                                                                          | <span data-ttu-id="567c3-137">Significado</span><span class="sxs-lookup"><span data-stu-id="567c3-137">Meaning</span></span>                                                                    |
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="567c3-138"><dt>0x1</dt></span><span class="sxs-lookup"><span data-stu-id="567c3-138"><dt>0x1</dt></span></span> </dl> | <span data-ttu-id="567c3-139">O thread foi pronto do DPC (chamada de procedimento adiado).</span><span class="sxs-lookup"><span data-stu-id="567c3-139">The thread has been readied from DPC (deferred procedure call).</span></span><br/> |
| <dl> <span data-ttu-id="567c3-140"><dt>0x2</dt></span><span class="sxs-lookup"><span data-stu-id="567c3-140"><dt>0x2</dt></span></span> </dl> | <span data-ttu-id="567c3-141">A pilha do kernel está permutada no momento.</span><span class="sxs-lookup"><span data-stu-id="567c3-141">The kernel stack is currently swapped out.</span></span><br/>                      |
| <dl> <span data-ttu-id="567c3-142"><dt>0x4</dt></span><span class="sxs-lookup"><span data-stu-id="567c3-142"><dt>0x4</dt></span></span> </dl> | <span data-ttu-id="567c3-143">O espaço de endereço do processo é trocado.</span><span class="sxs-lookup"><span data-stu-id="567c3-143">The process address space is swapped out.</span></span><br/>                       |



 

<span data-ttu-id="567c3-144">Observe que, quando a pilha do kernel ou o espaço de endereço do processo for trocado, haverá um evento ReadyThread adicional depois que a pilha do kernel ou o espaço de endereço do processo tiver sido trocado novamente e o thread estiver pronto para ser despachado.</span><span class="sxs-lookup"><span data-stu-id="567c3-144">Note that when the kernel stack or the process address space is swapped out, there will be an additional ReadyThread event after the kernel stack or the process address space has been swapped back in and the thread is made ready to be dispatched.</span></span>

</dd> <dt>

<span data-ttu-id="567c3-145">Reservado</span><span class="sxs-lookup"><span data-stu-id="567c3-145">Reserved</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="567c3-146">Tipo de dados: **sint8**</span><span class="sxs-lookup"><span data-stu-id="567c3-146">Data type: **sint8**</span></span>
</dt> <dt>

<span data-ttu-id="567c3-147">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="567c3-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="567c3-148">Qualificadores: WmiDataId (5)</span><span class="sxs-lookup"><span data-stu-id="567c3-148">Qualifiers: WmiDataId(5)</span></span>
</dt> </dl>

<span data-ttu-id="567c3-149">Reservado.</span><span class="sxs-lookup"><span data-stu-id="567c3-149">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="567c3-150">TThreadId</span><span class="sxs-lookup"><span data-stu-id="567c3-150">TThreadId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="567c3-151">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="567c3-151">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="567c3-152">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="567c3-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="567c3-153">Qualificadores: WmiDataId (1), formato ("x")</span><span class="sxs-lookup"><span data-stu-id="567c3-153">Qualifiers: WmiDataId(1), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="567c3-154">O identificador de thread do thread que está sendo pronto para execução.</span><span class="sxs-lookup"><span data-stu-id="567c3-154">The thread identifier of the thread being readied for execution.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="567c3-155">Requisitos</span><span class="sxs-lookup"><span data-stu-id="567c3-155">Requirements</span></span>



| <span data-ttu-id="567c3-156">Requisito</span><span class="sxs-lookup"><span data-stu-id="567c3-156">Requirement</span></span> | <span data-ttu-id="567c3-157">Valor</span><span class="sxs-lookup"><span data-stu-id="567c3-157">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="567c3-158">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="567c3-158">Minimum supported client</span></span><br/> | <span data-ttu-id="567c3-159">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="567c3-159">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="567c3-160">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="567c3-160">Minimum supported server</span></span><br/> | <span data-ttu-id="567c3-161">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="567c3-161">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="567c3-162">Confira também</span><span class="sxs-lookup"><span data-stu-id="567c3-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="567c3-163">**Thread \_ v2**</span><span class="sxs-lookup"><span data-stu-id="567c3-163">**Thread\_V2**</span></span>](thread-v2.md)
</dt> </dl>

 

 




