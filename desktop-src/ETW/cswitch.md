---
description: Essa classe é a classe de tipo de evento para eventos de alternância de contexto. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: 3f9f84d0-18a9-493c-b104-8236b2bd8404
title: Classe CSwitch
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSwitch
- CSwitch.NewThreadId
- CSwitch.OldThreadId
- CSwitch.NewThreadPriority
- CSwitch.OldThreadPriority
- CSwitch.PreviousCState
- CSwitch.SpareByte
- CSwitch.OldThreadWaitReason
- CSwitch.OldThreadWaitMode
- CSwitch.OldThreadState
- CSwitch.OldThreadWaitIdealProcessor
- CSwitch.NewThreadWaitTime
- CSwitch.Reserved
api_type:
- NA
api_location: ''
ms.openlocfilehash: 91004ca276140271e8d73c3fc226e83c4e03d1fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164744"
---
# <a name="cswitch-class"></a><span data-ttu-id="efe58-104">Classe CSwitch</span><span class="sxs-lookup"><span data-stu-id="efe58-104">CSwitch class</span></span>

<span data-ttu-id="efe58-105">Essa classe é a classe de tipo de evento para eventos de alternância de contexto.</span><span class="sxs-lookup"><span data-stu-id="efe58-105">This class is the event type class for context switch events.</span></span>

<span data-ttu-id="efe58-106">A sintaxe a seguir é simplificada do código MOF.</span><span class="sxs-lookup"><span data-stu-id="efe58-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="efe58-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="efe58-107">Syntax</span></span>

``` syntax
[EventType{36}, EventTypeName{"CSwitch"}]
class CSwitch : Thread_V2
{
  uint32 NewThreadId;
  uint32 OldThreadId;
  sint8  NewThreadPriority;
  sint8  OldThreadPriority;
  uint8  PreviousCState;
  sint8  SpareByte;
  sint8  OldThreadWaitReason;
  sint8  OldThreadWaitMode;
  sint8  OldThreadState;
  sint8  OldThreadWaitIdealProcessor;
  uint32 NewThreadWaitTime;
  uint32 Reserved;
};
```

## <a name="members"></a><span data-ttu-id="efe58-108">Membros</span><span class="sxs-lookup"><span data-stu-id="efe58-108">Members</span></span>

<span data-ttu-id="efe58-109">A classe **CSwitch** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="efe58-109">The **CSwitch** class has these types of members:</span></span>

-   [<span data-ttu-id="efe58-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="efe58-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="efe58-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="efe58-111">Properties</span></span>

<span data-ttu-id="efe58-112">A classe **CSwitch** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="efe58-112">The **CSwitch** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="efe58-113">**NewThreadId**</span><span class="sxs-lookup"><span data-stu-id="efe58-113">**NewThreadId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="efe58-114">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="efe58-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="efe58-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="efe58-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="efe58-116">Qualificadores: WmiDataId (1), formato ("x")</span><span class="sxs-lookup"><span data-stu-id="efe58-116">Qualifiers: WmiDataId(1), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="efe58-117">Nova ID de thread após a opção.</span><span class="sxs-lookup"><span data-stu-id="efe58-117">New thread ID after the switch.</span></span>

</dd> <dt>

<span data-ttu-id="efe58-118">**NewThreadPriority**</span><span class="sxs-lookup"><span data-stu-id="efe58-118">**NewThreadPriority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="efe58-119">Tipo de dados: **sint8**</span><span class="sxs-lookup"><span data-stu-id="efe58-119">Data type: **sint8**</span></span>
</dt> <dt>

<span data-ttu-id="efe58-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="efe58-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="efe58-121">Qualificadores: WmiDataId (3)</span><span class="sxs-lookup"><span data-stu-id="efe58-121">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="efe58-122">Prioridade do thread do novo thread.</span><span class="sxs-lookup"><span data-stu-id="efe58-122">Thread priority of the new thread.</span></span>

</dd> <dt>

<span data-ttu-id="efe58-123">**NewThreadWaitTime**</span><span class="sxs-lookup"><span data-stu-id="efe58-123">**NewThreadWaitTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="efe58-124">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="efe58-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="efe58-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="efe58-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="efe58-126">Qualificadores: WmiDataId (11), formato ("x")</span><span class="sxs-lookup"><span data-stu-id="efe58-126">Qualifiers: WmiDataId(11), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="efe58-127">Tempo de espera para o novo thread.</span><span class="sxs-lookup"><span data-stu-id="efe58-127">Wait time for the new thread.</span></span>

</dd> <dt>

<span data-ttu-id="efe58-128">**OldThreadId**</span><span class="sxs-lookup"><span data-stu-id="efe58-128">**OldThreadId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="efe58-129">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="efe58-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="efe58-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="efe58-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="efe58-131">Qualificadores: WmiDataId (2), formato ("x")</span><span class="sxs-lookup"><span data-stu-id="efe58-131">Qualifiers: WmiDataId(2), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="efe58-132">ID de thread anterior.</span><span class="sxs-lookup"><span data-stu-id="efe58-132">Previous thread ID.</span></span>

</dd> <dt>

<span data-ttu-id="efe58-133">**OldThreadPriority**</span><span class="sxs-lookup"><span data-stu-id="efe58-133">**OldThreadPriority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="efe58-134">Tipo de dados: **sint8**</span><span class="sxs-lookup"><span data-stu-id="efe58-134">Data type: **sint8**</span></span>
</dt> <dt>

<span data-ttu-id="efe58-135">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="efe58-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="efe58-136">Qualificadores: WmiDataId (4)</span><span class="sxs-lookup"><span data-stu-id="efe58-136">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="efe58-137">Prioridade de thread do thread anterior.</span><span class="sxs-lookup"><span data-stu-id="efe58-137">Thread priority of the previous thread.</span></span>

</dd> <dt>

<span data-ttu-id="efe58-138">**OldThreadState**</span><span class="sxs-lookup"><span data-stu-id="efe58-138">**OldThreadState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="efe58-139">Tipo de dados: **sint8**</span><span class="sxs-lookup"><span data-stu-id="efe58-139">Data type: **sint8**</span></span>
</dt> <dt>

<span data-ttu-id="efe58-140">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="efe58-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="efe58-141">Qualificadores: WmiDataId (9)</span><span class="sxs-lookup"><span data-stu-id="efe58-141">Qualifiers: WmiDataId(9)</span></span>
</dt> </dl>

<span data-ttu-id="efe58-142">Estado do thread anterior.</span><span class="sxs-lookup"><span data-stu-id="efe58-142">State of the previous thread.</span></span> <span data-ttu-id="efe58-143">Estes são os valores de estado possíveis:</span><span class="sxs-lookup"><span data-stu-id="efe58-143">The following are the possible state values:</span></span>

| <span data-ttu-id="efe58-144">Estado</span><span class="sxs-lookup"><span data-stu-id="efe58-144">State</span></span> | <span data-ttu-id="efe58-145">Descrição</span><span class="sxs-lookup"><span data-stu-id="efe58-145">Description</span></span>                                   |
|-------|-----------------------------------------------|
| <span data-ttu-id="efe58-146">0</span><span class="sxs-lookup"><span data-stu-id="efe58-146">0</span></span>     | <span data-ttu-id="efe58-147">Inicializado</span><span class="sxs-lookup"><span data-stu-id="efe58-147">Initialized</span></span>                                   |
| <span data-ttu-id="efe58-148">1</span><span class="sxs-lookup"><span data-stu-id="efe58-148">1</span></span>     | <span data-ttu-id="efe58-149">Ready</span><span class="sxs-lookup"><span data-stu-id="efe58-149">Ready</span></span>                                         |
| <span data-ttu-id="efe58-150">2</span><span class="sxs-lookup"><span data-stu-id="efe58-150">2</span></span>     | <span data-ttu-id="efe58-151">Executando</span><span class="sxs-lookup"><span data-stu-id="efe58-151">Running</span></span>                                       |
| <span data-ttu-id="efe58-152">3</span><span class="sxs-lookup"><span data-stu-id="efe58-152">3</span></span>     | <span data-ttu-id="efe58-153">Standby</span><span class="sxs-lookup"><span data-stu-id="efe58-153">Standby</span></span>                                       |
| <span data-ttu-id="efe58-154">4</span><span class="sxs-lookup"><span data-stu-id="efe58-154">4</span></span>     | <span data-ttu-id="efe58-155">Terminado</span><span class="sxs-lookup"><span data-stu-id="efe58-155">Terminated</span></span>                                    |
| <span data-ttu-id="efe58-156">5</span><span class="sxs-lookup"><span data-stu-id="efe58-156">5</span></span>     | <span data-ttu-id="efe58-157">Aguardando</span><span class="sxs-lookup"><span data-stu-id="efe58-157">Waiting</span></span>                                       |
| <span data-ttu-id="efe58-158">6</span><span class="sxs-lookup"><span data-stu-id="efe58-158">6</span></span>     | <span data-ttu-id="efe58-159">Transição</span><span class="sxs-lookup"><span data-stu-id="efe58-159">Transition</span></span>                                    |
| <span data-ttu-id="efe58-160">7</span><span class="sxs-lookup"><span data-stu-id="efe58-160">7</span></span>     | <span data-ttu-id="efe58-161">DeferredReady (adicionado ao Windows Server 2003)</span><span class="sxs-lookup"><span data-stu-id="efe58-161">DeferredReady (added for Windows Server 2003)</span></span> |



 

</dd> <dt>

<span data-ttu-id="efe58-162">**OldThreadWaitIdealProcessor**</span><span class="sxs-lookup"><span data-stu-id="efe58-162">**OldThreadWaitIdealProcessor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="efe58-163">Tipo de dados: **sint8**</span><span class="sxs-lookup"><span data-stu-id="efe58-163">Data type: **sint8**</span></span>
</dt> <dt>

<span data-ttu-id="efe58-164">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="efe58-164">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="efe58-165">Qualificadores: WmiDataId (10), formato ("x")</span><span class="sxs-lookup"><span data-stu-id="efe58-165">Qualifiers: WmiDataId(10), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="efe58-166">Tempo de espera ideal do thread anterior.</span><span class="sxs-lookup"><span data-stu-id="efe58-166">Ideal wait time of the previous thread.</span></span>

</dd> <dt>

<span data-ttu-id="efe58-167">**OldThreadWaitMode**</span><span class="sxs-lookup"><span data-stu-id="efe58-167">**OldThreadWaitMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="efe58-168">Tipo de dados: **sint8**</span><span class="sxs-lookup"><span data-stu-id="efe58-168">Data type: **sint8**</span></span>
</dt> <dt>

<span data-ttu-id="efe58-169">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="efe58-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="efe58-170">Qualificadores: WmiDataId (8)</span><span class="sxs-lookup"><span data-stu-id="efe58-170">Qualifiers: WmiDataId(8)</span></span>
</dt> </dl>

<span data-ttu-id="efe58-171">Modo de espera para o thread anterior.</span><span class="sxs-lookup"><span data-stu-id="efe58-171">Wait mode for the previous thread.</span></span> <span data-ttu-id="efe58-172">O valores possíveis são os seguintes:</span><span class="sxs-lookup"><span data-stu-id="efe58-172">The following are the possible values:</span></span>

| <span data-ttu-id="efe58-173">Estado</span><span class="sxs-lookup"><span data-stu-id="efe58-173">State</span></span> | <span data-ttu-id="efe58-174">Descrição</span><span class="sxs-lookup"><span data-stu-id="efe58-174">Description</span></span> |
|-------|-------------|
| <span data-ttu-id="efe58-175">0</span><span class="sxs-lookup"><span data-stu-id="efe58-175">0</span></span>     | <span data-ttu-id="efe58-176">KernelMode</span><span class="sxs-lookup"><span data-stu-id="efe58-176">KernelMode</span></span>  |
| <span data-ttu-id="efe58-177">1</span><span class="sxs-lookup"><span data-stu-id="efe58-177">1</span></span>     | <span data-ttu-id="efe58-178">Modo</span><span class="sxs-lookup"><span data-stu-id="efe58-178">UserMode</span></span>    |



 

</dd> <dt>

<span data-ttu-id="efe58-179">**OldThreadWaitReason**</span><span class="sxs-lookup"><span data-stu-id="efe58-179">**OldThreadWaitReason**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="efe58-180">Tipo de dados: **sint8**</span><span class="sxs-lookup"><span data-stu-id="efe58-180">Data type: **sint8**</span></span>
</dt> <dt>

<span data-ttu-id="efe58-181">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="efe58-181">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="efe58-182">Qualificadores: WmiDataId (7)</span><span class="sxs-lookup"><span data-stu-id="efe58-182">Qualifiers: WmiDataId(7)</span></span>
</dt> </dl>

<span data-ttu-id="efe58-183">Motivo de espera para o thread anterior.</span><span class="sxs-lookup"><span data-stu-id="efe58-183">Wait reason for the previous thread.</span></span> <span data-ttu-id="efe58-184">O valores possíveis são os seguintes:</span><span class="sxs-lookup"><span data-stu-id="efe58-184">The following are the possible values:</span></span>

| <span data-ttu-id="efe58-185">Estado</span><span class="sxs-lookup"><span data-stu-id="efe58-185">State</span></span> | <span data-ttu-id="efe58-186">Descrição</span><span class="sxs-lookup"><span data-stu-id="efe58-186">Description</span></span>       |
|-------|-------------------|
| <span data-ttu-id="efe58-187">0</span><span class="sxs-lookup"><span data-stu-id="efe58-187">0</span></span>     | <span data-ttu-id="efe58-188">Executivo</span><span class="sxs-lookup"><span data-stu-id="efe58-188">Executive</span></span>         |
| <span data-ttu-id="efe58-189">1</span><span class="sxs-lookup"><span data-stu-id="efe58-189">1</span></span>     | <span data-ttu-id="efe58-190">FreePage</span><span class="sxs-lookup"><span data-stu-id="efe58-190">FreePage</span></span>          |
| <span data-ttu-id="efe58-191">2</span><span class="sxs-lookup"><span data-stu-id="efe58-191">2</span></span>     | <span data-ttu-id="efe58-192">PageIn</span><span class="sxs-lookup"><span data-stu-id="efe58-192">PageIn</span></span>            |
| <span data-ttu-id="efe58-193">3</span><span class="sxs-lookup"><span data-stu-id="efe58-193">3</span></span>     | <span data-ttu-id="efe58-194">PoolAllocation</span><span class="sxs-lookup"><span data-stu-id="efe58-194">PoolAllocation</span></span>    |
| <span data-ttu-id="efe58-195">4</span><span class="sxs-lookup"><span data-stu-id="efe58-195">4</span></span>     | <span data-ttu-id="efe58-196">DelayExecution</span><span class="sxs-lookup"><span data-stu-id="efe58-196">DelayExecution</span></span>    |
| <span data-ttu-id="efe58-197">5</span><span class="sxs-lookup"><span data-stu-id="efe58-197">5</span></span>     | <span data-ttu-id="efe58-198">Suspenso</span><span class="sxs-lookup"><span data-stu-id="efe58-198">Suspended</span></span>         |
| <span data-ttu-id="efe58-199">6</span><span class="sxs-lookup"><span data-stu-id="efe58-199">6</span></span>     | <span data-ttu-id="efe58-200">Solicitação de pedido</span><span class="sxs-lookup"><span data-stu-id="efe58-200">UserRequest</span></span>       |
| <span data-ttu-id="efe58-201">7</span><span class="sxs-lookup"><span data-stu-id="efe58-201">7</span></span>     | <span data-ttu-id="efe58-202">WrExecutive</span><span class="sxs-lookup"><span data-stu-id="efe58-202">WrExecutive</span></span>       |
| <span data-ttu-id="efe58-203">8</span><span class="sxs-lookup"><span data-stu-id="efe58-203">8</span></span>     | <span data-ttu-id="efe58-204">WrFreePage</span><span class="sxs-lookup"><span data-stu-id="efe58-204">WrFreePage</span></span>        |
| <span data-ttu-id="efe58-205">9</span><span class="sxs-lookup"><span data-stu-id="efe58-205">9</span></span>     | <span data-ttu-id="efe58-206">WrPageIn</span><span class="sxs-lookup"><span data-stu-id="efe58-206">WrPageIn</span></span>          |
| <span data-ttu-id="efe58-207">10</span><span class="sxs-lookup"><span data-stu-id="efe58-207">10</span></span>    | <span data-ttu-id="efe58-208">WrPoolAllocation</span><span class="sxs-lookup"><span data-stu-id="efe58-208">WrPoolAllocation</span></span>  |
| <span data-ttu-id="efe58-209">11</span><span class="sxs-lookup"><span data-stu-id="efe58-209">11</span></span>    | <span data-ttu-id="efe58-210">WrDelayExecution</span><span class="sxs-lookup"><span data-stu-id="efe58-210">WrDelayExecution</span></span>  |
| <span data-ttu-id="efe58-211">12</span><span class="sxs-lookup"><span data-stu-id="efe58-211">12</span></span>    | <span data-ttu-id="efe58-212">WrSuspended</span><span class="sxs-lookup"><span data-stu-id="efe58-212">WrSuspended</span></span>       |
| <span data-ttu-id="efe58-213">13</span><span class="sxs-lookup"><span data-stu-id="efe58-213">13</span></span>    | <span data-ttu-id="efe58-214">WrUserRequest</span><span class="sxs-lookup"><span data-stu-id="efe58-214">WrUserRequest</span></span>     |
| <span data-ttu-id="efe58-215">14</span><span class="sxs-lookup"><span data-stu-id="efe58-215">14</span></span>    | <span data-ttu-id="efe58-216">WrEventPair</span><span class="sxs-lookup"><span data-stu-id="efe58-216">WrEventPair</span></span>       |
| <span data-ttu-id="efe58-217">15</span><span class="sxs-lookup"><span data-stu-id="efe58-217">15</span></span>    | <span data-ttu-id="efe58-218">WrQueue</span><span class="sxs-lookup"><span data-stu-id="efe58-218">WrQueue</span></span>           |
| <span data-ttu-id="efe58-219">16</span><span class="sxs-lookup"><span data-stu-id="efe58-219">16</span></span>    | <span data-ttu-id="efe58-220">WrLpcReceive</span><span class="sxs-lookup"><span data-stu-id="efe58-220">WrLpcReceive</span></span>      |
| <span data-ttu-id="efe58-221">17</span><span class="sxs-lookup"><span data-stu-id="efe58-221">17</span></span>    | <span data-ttu-id="efe58-222">WrLpcReply</span><span class="sxs-lookup"><span data-stu-id="efe58-222">WrLpcReply</span></span>        |
| <span data-ttu-id="efe58-223">18</span><span class="sxs-lookup"><span data-stu-id="efe58-223">18</span></span>    | <span data-ttu-id="efe58-224">WrVirtualMemory</span><span class="sxs-lookup"><span data-stu-id="efe58-224">WrVirtualMemory</span></span>   |
| <span data-ttu-id="efe58-225">19</span><span class="sxs-lookup"><span data-stu-id="efe58-225">19</span></span>    | <span data-ttu-id="efe58-226">WrPageOut</span><span class="sxs-lookup"><span data-stu-id="efe58-226">WrPageOut</span></span>         |
| <span data-ttu-id="efe58-227">20</span><span class="sxs-lookup"><span data-stu-id="efe58-227">20</span></span>    | <span data-ttu-id="efe58-228">WrRendezvous</span><span class="sxs-lookup"><span data-stu-id="efe58-228">WrRendezvous</span></span>      |
| <span data-ttu-id="efe58-229">21</span><span class="sxs-lookup"><span data-stu-id="efe58-229">21</span></span>    | <span data-ttu-id="efe58-230">WrKeyedEvent</span><span class="sxs-lookup"><span data-stu-id="efe58-230">WrKeyedEvent</span></span>      |
| <span data-ttu-id="efe58-231">22</span><span class="sxs-lookup"><span data-stu-id="efe58-231">22</span></span>    | <span data-ttu-id="efe58-232">WrTerminated</span><span class="sxs-lookup"><span data-stu-id="efe58-232">WrTerminated</span></span>      |
| <span data-ttu-id="efe58-233">23</span><span class="sxs-lookup"><span data-stu-id="efe58-233">23</span></span>    | <span data-ttu-id="efe58-234">WrProcessInSwap</span><span class="sxs-lookup"><span data-stu-id="efe58-234">WrProcessInSwap</span></span>   |
| <span data-ttu-id="efe58-235">24</span><span class="sxs-lookup"><span data-stu-id="efe58-235">24</span></span>    | <span data-ttu-id="efe58-236">WrCpuRateControl</span><span class="sxs-lookup"><span data-stu-id="efe58-236">WrCpuRateControl</span></span>  |
| <span data-ttu-id="efe58-237">25</span><span class="sxs-lookup"><span data-stu-id="efe58-237">25</span></span>    | <span data-ttu-id="efe58-238">WrCalloutStack</span><span class="sxs-lookup"><span data-stu-id="efe58-238">WrCalloutStack</span></span>    |
| <span data-ttu-id="efe58-239">26</span><span class="sxs-lookup"><span data-stu-id="efe58-239">26</span></span>    | <span data-ttu-id="efe58-240">WrKernel</span><span class="sxs-lookup"><span data-stu-id="efe58-240">WrKernel</span></span>          |
| <span data-ttu-id="efe58-241">27</span><span class="sxs-lookup"><span data-stu-id="efe58-241">27</span></span>    | <span data-ttu-id="efe58-242">WrResource</span><span class="sxs-lookup"><span data-stu-id="efe58-242">WrResource</span></span>        |
| <span data-ttu-id="efe58-243">28</span><span class="sxs-lookup"><span data-stu-id="efe58-243">28</span></span>    | <span data-ttu-id="efe58-244">WrPushLock</span><span class="sxs-lookup"><span data-stu-id="efe58-244">WrPushLock</span></span>        |
| <span data-ttu-id="efe58-245">29</span><span class="sxs-lookup"><span data-stu-id="efe58-245">29</span></span>    | <span data-ttu-id="efe58-246">WrMutex</span><span class="sxs-lookup"><span data-stu-id="efe58-246">WrMutex</span></span>           |
| <span data-ttu-id="efe58-247">30</span><span class="sxs-lookup"><span data-stu-id="efe58-247">30</span></span>    | <span data-ttu-id="efe58-248">WrQuantumEnd</span><span class="sxs-lookup"><span data-stu-id="efe58-248">WrQuantumEnd</span></span>      |
| <span data-ttu-id="efe58-249">31</span><span class="sxs-lookup"><span data-stu-id="efe58-249">31</span></span>    | <span data-ttu-id="efe58-250">WrDispatchInt</span><span class="sxs-lookup"><span data-stu-id="efe58-250">WrDispatchInt</span></span>     |
| <span data-ttu-id="efe58-251">32</span><span class="sxs-lookup"><span data-stu-id="efe58-251">32</span></span>    | <span data-ttu-id="efe58-252">WrPreempted</span><span class="sxs-lookup"><span data-stu-id="efe58-252">WrPreempted</span></span>       |
| <span data-ttu-id="efe58-253">33</span><span class="sxs-lookup"><span data-stu-id="efe58-253">33</span></span>    | <span data-ttu-id="efe58-254">WrYieldExecution</span><span class="sxs-lookup"><span data-stu-id="efe58-254">WrYieldExecution</span></span>  |
| <span data-ttu-id="efe58-255">34</span><span class="sxs-lookup"><span data-stu-id="efe58-255">34</span></span>    | <span data-ttu-id="efe58-256">WrFastMutex</span><span class="sxs-lookup"><span data-stu-id="efe58-256">WrFastMutex</span></span>       |
| <span data-ttu-id="efe58-257">35</span><span class="sxs-lookup"><span data-stu-id="efe58-257">35</span></span>    | <span data-ttu-id="efe58-258">WrGuardedMutex</span><span class="sxs-lookup"><span data-stu-id="efe58-258">WrGuardedMutex</span></span>    |
| <span data-ttu-id="efe58-259">36</span><span class="sxs-lookup"><span data-stu-id="efe58-259">36</span></span>    | <span data-ttu-id="efe58-260">WrRundown</span><span class="sxs-lookup"><span data-stu-id="efe58-260">WrRundown</span></span>         |
| <span data-ttu-id="efe58-261">37</span><span class="sxs-lookup"><span data-stu-id="efe58-261">37</span></span>    | <span data-ttu-id="efe58-262">MaximumWaitReason</span><span class="sxs-lookup"><span data-stu-id="efe58-262">MaximumWaitReason</span></span> |



 

</dd> <dt>

<span data-ttu-id="efe58-263">**PreviousCState**</span><span class="sxs-lookup"><span data-stu-id="efe58-263">**PreviousCState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="efe58-264">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="efe58-264">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="efe58-265">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="efe58-265">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="efe58-266">Qualificadores: WmiDataId (5)</span><span class="sxs-lookup"><span data-stu-id="efe58-266">Qualifiers: WmiDataId(5)</span></span>
</dt> </dl>

<span data-ttu-id="efe58-267">O índice do estado C que foi usado pela última vez pelo processador.</span><span class="sxs-lookup"><span data-stu-id="efe58-267">The index of the C-state that was last used by the processor.</span></span> <span data-ttu-id="efe58-268">Um valor de 0 representa o estado ocioso mais leve com valores mais altos que representam os mais avançados.</span><span class="sxs-lookup"><span data-stu-id="efe58-268">A value of 0 represents the lightest idle state with higher values representing deeper C-states.</span></span>

</dd> <dt>

<span data-ttu-id="efe58-269">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="efe58-269">**Reserved**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="efe58-270">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="efe58-270">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="efe58-271">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="efe58-271">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="efe58-272">Qualificadores: WmiDataId (12)</span><span class="sxs-lookup"><span data-stu-id="efe58-272">Qualifiers: WmiDataId(12)</span></span>
</dt> </dl>

<span data-ttu-id="efe58-273">Reservado.</span><span class="sxs-lookup"><span data-stu-id="efe58-273">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="efe58-274">**SpareByte**</span><span class="sxs-lookup"><span data-stu-id="efe58-274">**SpareByte**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="efe58-275">Tipo de dados: **sint8**</span><span class="sxs-lookup"><span data-stu-id="efe58-275">Data type: **sint8**</span></span>
</dt> <dt>

<span data-ttu-id="efe58-276">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="efe58-276">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="efe58-277">Qualificadores: WmiDataId (6)</span><span class="sxs-lookup"><span data-stu-id="efe58-277">Qualifiers: WmiDataId(6)</span></span>
</dt> </dl>

<span data-ttu-id="efe58-278">Não usado.</span><span class="sxs-lookup"><span data-stu-id="efe58-278">Not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="efe58-279">Comentários</span><span class="sxs-lookup"><span data-stu-id="efe58-279">Remarks</span></span>

<span data-ttu-id="efe58-280">Esses eventos produzem um alto volume de eventos.</span><span class="sxs-lookup"><span data-stu-id="efe58-280">These events produce a high volume of events.</span></span>

## <a name="requirements"></a><span data-ttu-id="efe58-281">Requisitos</span><span class="sxs-lookup"><span data-stu-id="efe58-281">Requirements</span></span>



| <span data-ttu-id="efe58-282">Requisito</span><span class="sxs-lookup"><span data-stu-id="efe58-282">Requirement</span></span> | <span data-ttu-id="efe58-283">Valor</span><span class="sxs-lookup"><span data-stu-id="efe58-283">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="efe58-284">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="efe58-284">Minimum supported client</span></span><br/> | <span data-ttu-id="efe58-285">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="efe58-285">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="efe58-286">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="efe58-286">Minimum supported server</span></span><br/> | <span data-ttu-id="efe58-287">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="efe58-287">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="efe58-288">Confira também</span><span class="sxs-lookup"><span data-stu-id="efe58-288">See also</span></span>

<dl> <dt>

[<span data-ttu-id="efe58-289">**Processo**</span><span class="sxs-lookup"><span data-stu-id="efe58-289">**Thread**</span></span>](thread.md)
</dt> <dt>

[<span data-ttu-id="efe58-290">**Thread \_ v2**</span><span class="sxs-lookup"><span data-stu-id="efe58-290">**Thread\_V2**</span></span>](thread-v2.md)
</dt> </dl>

 

 




