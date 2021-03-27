---
description: Essa classe é a classe de tipo de evento para eventos de início e término de thread. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: d9e3e33a-0e59-4753-a8d8-5320cbae9d95
title: Classe Thread_TypeGroup1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Thread_TypeGroup1
- Thread_TypeGroup1.ProcessId
- Thread_TypeGroup1.TThreadId
- Thread_TypeGroup1.StackBase
- Thread_TypeGroup1.StackLimit
- Thread_TypeGroup1.UserStackBase
- Thread_TypeGroup1.UserStackLimit
- Thread_TypeGroup1.Affinity
- Thread_TypeGroup1.Win32StartAddr
- Thread_TypeGroup1.TebBase
- Thread_TypeGroup1.SubProcessTag
- Thread_TypeGroup1.BasePriority
- Thread_TypeGroup1.PagePriority
- Thread_TypeGroup1.IoPriority
- Thread_TypeGroup1.ThreadFlags
api_type:
- NA
api_location: ''
ms.openlocfilehash: 75352efbe044f5fee837c496c394fe28e2dbbbfb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091149"
---
# <a name="thread_typegroup1-class"></a><span data-ttu-id="35d28-104">\_Classe TypeGroup1 de thread</span><span class="sxs-lookup"><span data-stu-id="35d28-104">Thread\_TypeGroup1 class</span></span>

<span data-ttu-id="35d28-105">Essa classe é a classe de tipo de evento para eventos de início e término de thread.</span><span class="sxs-lookup"><span data-stu-id="35d28-105">This class is the event type class for thread start and end events.</span></span>

<span data-ttu-id="35d28-106">A sintaxe a seguir é simplificada do código MOF.</span><span class="sxs-lookup"><span data-stu-id="35d28-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="35d28-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="35d28-107">Syntax</span></span>

``` syntax
[EventType{1, 2, 3, 4}, EventTypeName{"Start", "End", "DCStart", "DCEnd"}]
class Thread_TypeGroup1 : Thread
{
  uint32 ProcessId;
  uint32 TThreadId;
  uint32 StackBase;
  uint32 StackLimit;
  uint32 UserStackBase;
  uint32 UserStackLimit;
  uint32 Affinity;
  uint32 Win32StartAddr;
  uint32 TebBase;
  uint32 SubProcessTag;
  uint8  BasePriority;
  uint8  PagePriority;
  uint8  IoPriority;
  uint8  ThreadFlags;
};
```

## <a name="members"></a><span data-ttu-id="35d28-108">Membros</span><span class="sxs-lookup"><span data-stu-id="35d28-108">Members</span></span>

<span data-ttu-id="35d28-109">A classe **thread \_ TypeGroup1** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="35d28-109">The **Thread\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="35d28-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="35d28-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="35d28-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="35d28-111">Properties</span></span>

<span data-ttu-id="35d28-112">A classe **thread \_ TypeGroup1** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="35d28-112">The **Thread\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="35d28-113">Afinidade</span><span class="sxs-lookup"><span data-stu-id="35d28-113">Affinity</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35d28-114">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="35d28-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="35d28-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="35d28-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="35d28-116">Qualificadores: WmiDataId (7), ponteiro</span><span class="sxs-lookup"><span data-stu-id="35d28-116">Qualifiers: WmiDataId(7), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="35d28-117">O conjunto de processadores nos quais o thread tem permissão para ser executado.</span><span class="sxs-lookup"><span data-stu-id="35d28-117">The set of processors on which the thread is allowed to run.</span></span>

</dd> <dt>

<span data-ttu-id="35d28-118">BasePriority</span><span class="sxs-lookup"><span data-stu-id="35d28-118">BasePriority</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35d28-119">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="35d28-119">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="35d28-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="35d28-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="35d28-121">Qualificadores: WmiDataId (11)</span><span class="sxs-lookup"><span data-stu-id="35d28-121">Qualifiers: WmiDataId(11)</span></span>
</dt> </dl>

<span data-ttu-id="35d28-122">A prioridade do Agendador do thread (consulte a função [**SetThreadPriority**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadpriority) ).</span><span class="sxs-lookup"><span data-stu-id="35d28-122">The scheduler priority of the thread (see the [**SetThreadPriority**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadpriority) function).</span></span>

</dd> <dt>

<span data-ttu-id="35d28-123">IoPriority</span><span class="sxs-lookup"><span data-stu-id="35d28-123">IoPriority</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35d28-124">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="35d28-124">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="35d28-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="35d28-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="35d28-126">Qualificadores: WmiDataId (13)</span><span class="sxs-lookup"><span data-stu-id="35d28-126">Qualifiers: WmiDataId(13)</span></span>
</dt> </dl>

<span data-ttu-id="35d28-127">Uma dica de prioridade de e/s para agendar o IOs gerado pelo thread.</span><span class="sxs-lookup"><span data-stu-id="35d28-127">An IO priority hint for scheduling IOs generated by the thread.</span></span>

</dd> <dt>

<span data-ttu-id="35d28-128">PagePriority</span><span class="sxs-lookup"><span data-stu-id="35d28-128">PagePriority</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35d28-129">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="35d28-129">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="35d28-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="35d28-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="35d28-131">Qualificadores: WmiDataId (12)</span><span class="sxs-lookup"><span data-stu-id="35d28-131">Qualifiers: WmiDataId(12)</span></span>
</dt> </dl>

<span data-ttu-id="35d28-132">Uma dica de prioridade de página de memória para páginas de memória acessadas pelo thread.</span><span class="sxs-lookup"><span data-stu-id="35d28-132">A memory page priority hint for memory pages accessed by the thread.</span></span>

</dd> <dt>

<span data-ttu-id="35d28-133">ProcessId</span><span class="sxs-lookup"><span data-stu-id="35d28-133">ProcessId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35d28-134">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="35d28-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="35d28-135">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="35d28-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="35d28-136">Qualificadores: WmiDataId (1), formato ("x")</span><span class="sxs-lookup"><span data-stu-id="35d28-136">Qualifiers: WmiDataId(1), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="35d28-137">Identificador de processo do thread envolvido no evento.</span><span class="sxs-lookup"><span data-stu-id="35d28-137">Process identifier of the thread involved in the event.</span></span>

</dd> <dt>

<span data-ttu-id="35d28-138">StackBase</span><span class="sxs-lookup"><span data-stu-id="35d28-138">StackBase</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35d28-139">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="35d28-139">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="35d28-140">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="35d28-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="35d28-141">Qualificadores: WmiDataId (3), ponteiro</span><span class="sxs-lookup"><span data-stu-id="35d28-141">Qualifiers: WmiDataId(3), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="35d28-142">Endereço base da pilha do thread.</span><span class="sxs-lookup"><span data-stu-id="35d28-142">Base address of the thread's stack.</span></span>

</dd> <dt>

<span data-ttu-id="35d28-143">StackLimit</span><span class="sxs-lookup"><span data-stu-id="35d28-143">StackLimit</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35d28-144">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="35d28-144">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="35d28-145">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="35d28-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="35d28-146">Qualificadores: WmiDataId (4), ponteiro</span><span class="sxs-lookup"><span data-stu-id="35d28-146">Qualifiers: WmiDataId(4), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="35d28-147">Limite da pilha do thread.</span><span class="sxs-lookup"><span data-stu-id="35d28-147">Limit of the thread's stack.</span></span>

</dd> <dt>

<span data-ttu-id="35d28-148">SubProcessTag</span><span class="sxs-lookup"><span data-stu-id="35d28-148">SubProcessTag</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35d28-149">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="35d28-149">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="35d28-150">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="35d28-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="35d28-151">Qualificadores: WmiDataId (10), formato ("x")</span><span class="sxs-lookup"><span data-stu-id="35d28-151">Qualifiers: WmiDataId(10), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="35d28-152">Identifica o serviço se o thread pertence a um serviço; caso contrário, zero.</span><span class="sxs-lookup"><span data-stu-id="35d28-152">Identifies the service if the thread is owned by a service; otherwise, zero.</span></span>

</dd> <dt>

<span data-ttu-id="35d28-153">TebBase</span><span class="sxs-lookup"><span data-stu-id="35d28-153">TebBase</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35d28-154">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="35d28-154">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="35d28-155">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="35d28-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="35d28-156">Qualificadores: WmiDataId (9), ponteiro</span><span class="sxs-lookup"><span data-stu-id="35d28-156">Qualifiers: WmiDataId(9), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="35d28-157">Endereço base do bloco do ambiente de thread.</span><span class="sxs-lookup"><span data-stu-id="35d28-157">Thread environment block base address.</span></span>

</dd> <dt>

<span data-ttu-id="35d28-158">ThreadFlags</span><span class="sxs-lookup"><span data-stu-id="35d28-158">ThreadFlags</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35d28-159">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="35d28-159">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="35d28-160">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="35d28-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="35d28-161">Qualificadores: WmiDataId (14)</span><span class="sxs-lookup"><span data-stu-id="35d28-161">Qualifiers: WmiDataId(14)</span></span>
</dt> </dl>

<span data-ttu-id="35d28-162">Não usado.</span><span class="sxs-lookup"><span data-stu-id="35d28-162">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="35d28-163">TThreadId</span><span class="sxs-lookup"><span data-stu-id="35d28-163">TThreadId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35d28-164">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="35d28-164">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="35d28-165">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="35d28-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="35d28-166">Qualificadores: WmiDataId (2), formato ("x")</span><span class="sxs-lookup"><span data-stu-id="35d28-166">Qualifiers: WmiDataId(2), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="35d28-167">Identificador de thread do thread envolvido no evento.</span><span class="sxs-lookup"><span data-stu-id="35d28-167">Thread identifier of the thread involved in the event.</span></span>

</dd> <dt>

<span data-ttu-id="35d28-168">UserStackBase</span><span class="sxs-lookup"><span data-stu-id="35d28-168">UserStackBase</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35d28-169">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="35d28-169">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="35d28-170">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="35d28-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="35d28-171">Qualificadores: WmiDataId (5), ponteiro</span><span class="sxs-lookup"><span data-stu-id="35d28-171">Qualifiers: WmiDataId(5), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="35d28-172">Endereço base da pilha do modo de usuário do thread.</span><span class="sxs-lookup"><span data-stu-id="35d28-172">Base address of the thread's user-mode stack.</span></span>

</dd> <dt>

<span data-ttu-id="35d28-173">UserStackLimit</span><span class="sxs-lookup"><span data-stu-id="35d28-173">UserStackLimit</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35d28-174">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="35d28-174">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="35d28-175">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="35d28-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="35d28-176">Qualificadores: WmiDataId (6), ponteiro</span><span class="sxs-lookup"><span data-stu-id="35d28-176">Qualifiers: WmiDataId(6), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="35d28-177">Limite da pilha do modo de usuário do thread.</span><span class="sxs-lookup"><span data-stu-id="35d28-177">Limit of the thread's user-mode stack.</span></span>

</dd> <dt>

<span data-ttu-id="35d28-178">Win32StartAddr</span><span class="sxs-lookup"><span data-stu-id="35d28-178">Win32StartAddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35d28-179">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="35d28-179">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="35d28-180">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="35d28-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="35d28-181">Qualificadores: WmiDataId (8), ponteiro</span><span class="sxs-lookup"><span data-stu-id="35d28-181">Qualifiers: WmiDataId(8), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="35d28-182">Endereço inicial da função a ser executada por este thread.</span><span class="sxs-lookup"><span data-stu-id="35d28-182">Starting address of the function to be executed by this thread.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="35d28-183">Comentários</span><span class="sxs-lookup"><span data-stu-id="35d28-183">Remarks</span></span>

<span data-ttu-id="35d28-184">Os tipos de evento DCStart e DCEnd enumeram os threads que estão sendo executados no momento em que a sessão do kernel é iniciada e termina, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="35d28-184">The DCStart and DCEnd event types enumerate the threads that are currently running at the time the kernel session starts and ends, respectively.</span></span>

## <a name="requirements"></a><span data-ttu-id="35d28-185">Requisitos</span><span class="sxs-lookup"><span data-stu-id="35d28-185">Requirements</span></span>



| <span data-ttu-id="35d28-186">Requisito</span><span class="sxs-lookup"><span data-stu-id="35d28-186">Requirement</span></span> | <span data-ttu-id="35d28-187">Valor</span><span class="sxs-lookup"><span data-stu-id="35d28-187">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="35d28-188">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="35d28-188">Minimum supported client</span></span><br/> | <span data-ttu-id="35d28-189">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="35d28-189">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="35d28-190">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="35d28-190">Minimum supported server</span></span><br/> | <span data-ttu-id="35d28-191">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="35d28-191">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="35d28-192">Confira também</span><span class="sxs-lookup"><span data-stu-id="35d28-192">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35d28-193">**Processo**</span><span class="sxs-lookup"><span data-stu-id="35d28-193">**Thread**</span></span>](thread.md)
</dt> </dl>

 

 
