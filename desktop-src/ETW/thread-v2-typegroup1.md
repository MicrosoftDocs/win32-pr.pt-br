---
description: Classe Thread_V2_TypeGroup1-essa classe é a classe de tipo de evento para eventos de início e término de thread. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: c24b4bc9-2a05-444c-be41-b4dfd0511b93
title: Classe Thread_V2_TypeGroup1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Thread_V2_TypeGroup1
- Thread_V2_TypeGroup1.ProcessId
- Thread_V2_TypeGroup1.TThreadId
- Thread_V2_TypeGroup1.StackBase
- Thread_V2_TypeGroup1.StackLimit
- Thread_V2_TypeGroup1.UserStackBase
- Thread_V2_TypeGroup1.UserStackLimit
- Thread_V2_TypeGroup1.StartAddr
- Thread_V2_TypeGroup1.Win32StartAddr
- Thread_V2_TypeGroup1.TebBase
- Thread_V2_TypeGroup1.SubProcessTag
api_type:
- NA
api_location: ''
ms.openlocfilehash: 24ac4655fc374c40eb530828229a319f9ee1375e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105654"
---
# <a name="thread_v2_typegroup1-class"></a><span data-ttu-id="78cb6-104">\_ \_ Classe TypeGroup1 do thread v2</span><span class="sxs-lookup"><span data-stu-id="78cb6-104">Thread\_V2\_TypeGroup1 class</span></span>

<span data-ttu-id="78cb6-105">Essa classe é a classe de tipo de evento para eventos de início e término de thread.</span><span class="sxs-lookup"><span data-stu-id="78cb6-105">This class is the event type class for thread start and end events.</span></span>

<span data-ttu-id="78cb6-106">A sintaxe a seguir é simplificada do código MOF.</span><span class="sxs-lookup"><span data-stu-id="78cb6-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="78cb6-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="78cb6-107">Syntax</span></span>

``` syntax
[EventType{1, 2, 3, 4}, EventTypeName{"Start", "End", "DCStart", "DCEnd"}]
class Thread_V2_TypeGroup1 : Thread_V2
{
  uint32 ProcessId;
  uint32 TThreadId;
  uint32 StackBase;
  uint32 StackLimit;
  uint32 UserStackBase;
  uint32 UserStackLimit;
  uint32 StartAddr;
  uint32 Win32StartAddr;
  uint32 TebBase;
  uint32 SubProcessTag;
};
```

## <a name="members"></a><span data-ttu-id="78cb6-108">Membros</span><span class="sxs-lookup"><span data-stu-id="78cb6-108">Members</span></span>

<span data-ttu-id="78cb6-109">A **classe \_ \_ TypeGroup1 do thread v2** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="78cb6-109">The **Thread\_V2\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="78cb6-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="78cb6-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="78cb6-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="78cb6-111">Properties</span></span>

<span data-ttu-id="78cb6-112">A **classe \_ \_ TypeGroup1 do thread v2** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="78cb6-112">The **Thread\_V2\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="78cb6-113">ProcessId</span><span class="sxs-lookup"><span data-stu-id="78cb6-113">ProcessId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78cb6-114">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="78cb6-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="78cb6-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="78cb6-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="78cb6-116">Qualificadores: WmiDataId (1), formato ("x")</span><span class="sxs-lookup"><span data-stu-id="78cb6-116">Qualifiers: WmiDataId(1), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="78cb6-117">Identificador de processo do thread envolvido no evento.</span><span class="sxs-lookup"><span data-stu-id="78cb6-117">Process identifier of the thread involved in the event.</span></span>

</dd> <dt>

<span data-ttu-id="78cb6-118">StackBase</span><span class="sxs-lookup"><span data-stu-id="78cb6-118">StackBase</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78cb6-119">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="78cb6-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="78cb6-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="78cb6-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="78cb6-121">Qualificadores: WmiDataId (3), ponteiro</span><span class="sxs-lookup"><span data-stu-id="78cb6-121">Qualifiers: WmiDataId(3), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="78cb6-122">Endereço base da pilha do thread.</span><span class="sxs-lookup"><span data-stu-id="78cb6-122">Base address of the thread's stack.</span></span>

</dd> <dt>

<span data-ttu-id="78cb6-123">StackLimit</span><span class="sxs-lookup"><span data-stu-id="78cb6-123">StackLimit</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78cb6-124">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="78cb6-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="78cb6-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="78cb6-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="78cb6-126">Qualificadores: WmiDataId (4), ponteiro</span><span class="sxs-lookup"><span data-stu-id="78cb6-126">Qualifiers: WmiDataId(4), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="78cb6-127">Limite da pilha do thread.</span><span class="sxs-lookup"><span data-stu-id="78cb6-127">Limit of the thread's stack.</span></span>

</dd> <dt>

<span data-ttu-id="78cb6-128">StartAddr</span><span class="sxs-lookup"><span data-stu-id="78cb6-128">StartAddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78cb6-129">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="78cb6-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="78cb6-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="78cb6-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="78cb6-131">Qualificadores: WmiDataId (7), ponteiro</span><span class="sxs-lookup"><span data-stu-id="78cb6-131">Qualifiers: WmiDataId(7), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="78cb6-132">Endereço de memória no qual o rastreamento é iniciado.</span><span class="sxs-lookup"><span data-stu-id="78cb6-132">Memory address at which the trace starts.</span></span>

</dd> <dt>

<span data-ttu-id="78cb6-133">SubProcessTag</span><span class="sxs-lookup"><span data-stu-id="78cb6-133">SubProcessTag</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78cb6-134">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="78cb6-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="78cb6-135">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="78cb6-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="78cb6-136">Qualificadores: WmiDataId (10), formato ("x")</span><span class="sxs-lookup"><span data-stu-id="78cb6-136">Qualifiers: WmiDataId(10), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="78cb6-137">Identifica o serviço se o thread pertence a um serviço; caso contrário, zero.</span><span class="sxs-lookup"><span data-stu-id="78cb6-137">Identifies the service if the thread is owned by a service; otherwise, zero.</span></span>

</dd> <dt>

<span data-ttu-id="78cb6-138">TebBase</span><span class="sxs-lookup"><span data-stu-id="78cb6-138">TebBase</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78cb6-139">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="78cb6-139">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="78cb6-140">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="78cb6-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="78cb6-141">Qualificadores: WmiDataId (9), ponteiro</span><span class="sxs-lookup"><span data-stu-id="78cb6-141">Qualifiers: WmiDataId(9), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="78cb6-142">Endereço base do bloco do ambiente de thread.</span><span class="sxs-lookup"><span data-stu-id="78cb6-142">Thread environment block base address.</span></span>

</dd> <dt>

<span data-ttu-id="78cb6-143">TThreadId</span><span class="sxs-lookup"><span data-stu-id="78cb6-143">TThreadId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78cb6-144">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="78cb6-144">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="78cb6-145">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="78cb6-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="78cb6-146">Qualificadores: WmiDataId (2), formato ("x")</span><span class="sxs-lookup"><span data-stu-id="78cb6-146">Qualifiers: WmiDataId(2), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="78cb6-147">Identificador de thread do thread envolvido no evento.</span><span class="sxs-lookup"><span data-stu-id="78cb6-147">Thread identifier of the thread involved in the event.</span></span>

</dd> <dt>

<span data-ttu-id="78cb6-148">UserStackBase</span><span class="sxs-lookup"><span data-stu-id="78cb6-148">UserStackBase</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78cb6-149">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="78cb6-149">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="78cb6-150">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="78cb6-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="78cb6-151">Qualificadores: WmiDataId (5), ponteiro</span><span class="sxs-lookup"><span data-stu-id="78cb6-151">Qualifiers: WmiDataId(5), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="78cb6-152">Endereço base da pilha do modo de usuário do thread.</span><span class="sxs-lookup"><span data-stu-id="78cb6-152">Base address of the thread's user-mode stack.</span></span>

</dd> <dt>

<span data-ttu-id="78cb6-153">UserStackLimit</span><span class="sxs-lookup"><span data-stu-id="78cb6-153">UserStackLimit</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78cb6-154">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="78cb6-154">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="78cb6-155">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="78cb6-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="78cb6-156">Qualificadores: WmiDataId (6), ponteiro</span><span class="sxs-lookup"><span data-stu-id="78cb6-156">Qualifiers: WmiDataId(6), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="78cb6-157">Limite da pilha do modo de usuário do thread.</span><span class="sxs-lookup"><span data-stu-id="78cb6-157">Limit of the thread's user-mode stack.</span></span>

</dd> <dt>

<span data-ttu-id="78cb6-158">Win32StartAddr</span><span class="sxs-lookup"><span data-stu-id="78cb6-158">Win32StartAddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78cb6-159">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="78cb6-159">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="78cb6-160">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="78cb6-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="78cb6-161">Qualificadores: WmiDataId (8), ponteiro</span><span class="sxs-lookup"><span data-stu-id="78cb6-161">Qualifiers: WmiDataId(8), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="78cb6-162">Endereço inicial da função a ser executada por este thread.</span><span class="sxs-lookup"><span data-stu-id="78cb6-162">Starting address of the function to be executed by this thread.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="78cb6-163">Comentários</span><span class="sxs-lookup"><span data-stu-id="78cb6-163">Remarks</span></span>

<span data-ttu-id="78cb6-164">Os tipos de evento DCStart e DCEnd enumeram os threads que estão sendo executados no momento em que a sessão do kernel é iniciada e termina, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="78cb6-164">The DCStart and DCEnd event types enumerate the threads that are currently running at the time the kernel session starts and ends, respectively.</span></span>

## <a name="requirements"></a><span data-ttu-id="78cb6-165">Requisitos</span><span class="sxs-lookup"><span data-stu-id="78cb6-165">Requirements</span></span>



| <span data-ttu-id="78cb6-166">Requisito</span><span class="sxs-lookup"><span data-stu-id="78cb6-166">Requirement</span></span> | <span data-ttu-id="78cb6-167">Valor</span><span class="sxs-lookup"><span data-stu-id="78cb6-167">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="78cb6-168">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="78cb6-168">Minimum supported client</span></span><br/> | <span data-ttu-id="78cb6-169">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="78cb6-169">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="78cb6-170">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="78cb6-170">Minimum supported server</span></span><br/> | <span data-ttu-id="78cb6-171">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="78cb6-171">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="78cb6-172">Consulte também</span><span class="sxs-lookup"><span data-stu-id="78cb6-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78cb6-173">**Thread**</span><span class="sxs-lookup"><span data-stu-id="78cb6-173">**Thread**</span></span>](thread.md)
</dt> <dt>

[<span data-ttu-id="78cb6-174">**Thread \_ v2**</span><span class="sxs-lookup"><span data-stu-id="78cb6-174">**Thread\_V2**</span></span>](thread-v2.md)
</dt> </dl>

 

 




