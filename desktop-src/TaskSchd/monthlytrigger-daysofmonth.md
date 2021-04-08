---
title: Propriedade MonthlyTrigger. DaysOfMonth
description: Para scripts, Obtém ou define os dias do mês durante os quais a tarefa é executada.
ms.assetid: 4da80d0f-ae0c-4e56-b51b-6ee6ab309d7c
keywords:
- Agendador de Tarefas da propriedade DaysOfMonth
- Propriedade DaysOfMonth Agendador de Tarefas, objeto MonthlyTrigger
- Objeto MonthlyTrigger Agendador de Tarefas, Propriedade DaysOfMonth
topic_type:
- apiref
api_name:
- MonthlyTrigger.DaysOfMonth
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81a3bd671266cfbe459218367fadf20fd52f94a7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085782"
---
# <a name="monthlytriggerdaysofmonth-property"></a><span data-ttu-id="24968-106">Propriedade MonthlyTrigger. DaysOfMonth</span><span class="sxs-lookup"><span data-stu-id="24968-106">MonthlyTrigger.DaysOfMonth property</span></span>

<span data-ttu-id="24968-107">Para scripts, Obtém ou define os dias do mês durante os quais a tarefa é executada.</span><span class="sxs-lookup"><span data-stu-id="24968-107">For scripting, gets or sets the days of the month during which the task runs.</span></span>

## <a name="syntax"></a><span data-ttu-id="24968-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="24968-108">Syntax</span></span>


```VB
MonthlyTrigger.DaysOfMonth As long
```



## <a name="property-value"></a><span data-ttu-id="24968-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="24968-109">Property value</span></span>

<span data-ttu-id="24968-110">Uma máscara de bits bit que indica os dias do mês durante os quais a tarefa é executada.</span><span class="sxs-lookup"><span data-stu-id="24968-110">A bitwise mask that indicates the days of the month during which the task runs.</span></span>

## <a name="remarks"></a><span data-ttu-id="24968-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="24968-111">Remarks</span></span>



| <span data-ttu-id="24968-112">Dia do mês</span><span class="sxs-lookup"><span data-stu-id="24968-112">Day of month</span></span> | <span data-ttu-id="24968-113">Valor hex.</span><span class="sxs-lookup"><span data-stu-id="24968-113">Hex value</span></span>  | <span data-ttu-id="24968-114">Valor decimal</span><span class="sxs-lookup"><span data-stu-id="24968-114">Decimal value</span></span> |
|--------------|------------|---------------|
| <span data-ttu-id="24968-115">1</span><span class="sxs-lookup"><span data-stu-id="24968-115">1</span></span>            | <span data-ttu-id="24968-116">0x01</span><span class="sxs-lookup"><span data-stu-id="24968-116">0x01</span></span>       | <span data-ttu-id="24968-117">1</span><span class="sxs-lookup"><span data-stu-id="24968-117">1</span></span>             |
| <span data-ttu-id="24968-118">2</span><span class="sxs-lookup"><span data-stu-id="24968-118">2</span></span>            | <span data-ttu-id="24968-119">0x02</span><span class="sxs-lookup"><span data-stu-id="24968-119">0x02</span></span>       | <span data-ttu-id="24968-120">2</span><span class="sxs-lookup"><span data-stu-id="24968-120">2</span></span>             |
| <span data-ttu-id="24968-121">3</span><span class="sxs-lookup"><span data-stu-id="24968-121">3</span></span>            | <span data-ttu-id="24968-122">0x04</span><span class="sxs-lookup"><span data-stu-id="24968-122">0x04</span></span>       | <span data-ttu-id="24968-123">4</span><span class="sxs-lookup"><span data-stu-id="24968-123">4</span></span>             |
| <span data-ttu-id="24968-124">4</span><span class="sxs-lookup"><span data-stu-id="24968-124">4</span></span>            | <span data-ttu-id="24968-125">0x08</span><span class="sxs-lookup"><span data-stu-id="24968-125">0x08</span></span>       | <span data-ttu-id="24968-126">8</span><span class="sxs-lookup"><span data-stu-id="24968-126">8</span></span>             |
| <span data-ttu-id="24968-127">5</span><span class="sxs-lookup"><span data-stu-id="24968-127">5</span></span>            | <span data-ttu-id="24968-128">0x10</span><span class="sxs-lookup"><span data-stu-id="24968-128">0x10</span></span>       | <span data-ttu-id="24968-129">16</span><span class="sxs-lookup"><span data-stu-id="24968-129">16</span></span>            |
| <span data-ttu-id="24968-130">6</span><span class="sxs-lookup"><span data-stu-id="24968-130">6</span></span>            | <span data-ttu-id="24968-131">0x20</span><span class="sxs-lookup"><span data-stu-id="24968-131">0x20</span></span>       | <span data-ttu-id="24968-132">32</span><span class="sxs-lookup"><span data-stu-id="24968-132">32</span></span>            |
| <span data-ttu-id="24968-133">7</span><span class="sxs-lookup"><span data-stu-id="24968-133">7</span></span>            | <span data-ttu-id="24968-134">0x40</span><span class="sxs-lookup"><span data-stu-id="24968-134">0x40</span></span>       | <span data-ttu-id="24968-135">64</span><span class="sxs-lookup"><span data-stu-id="24968-135">64</span></span>            |
| <span data-ttu-id="24968-136">8</span><span class="sxs-lookup"><span data-stu-id="24968-136">8</span></span>            | <span data-ttu-id="24968-137">0x80</span><span class="sxs-lookup"><span data-stu-id="24968-137">0x80</span></span>       | <span data-ttu-id="24968-138">128</span><span class="sxs-lookup"><span data-stu-id="24968-138">128</span></span>           |
| <span data-ttu-id="24968-139">9</span><span class="sxs-lookup"><span data-stu-id="24968-139">9</span></span>            | <span data-ttu-id="24968-140">0x100</span><span class="sxs-lookup"><span data-stu-id="24968-140">0x100</span></span>      | <span data-ttu-id="24968-141">256</span><span class="sxs-lookup"><span data-stu-id="24968-141">256</span></span>           |
| <span data-ttu-id="24968-142">10</span><span class="sxs-lookup"><span data-stu-id="24968-142">10</span></span>           | <span data-ttu-id="24968-143">0x200</span><span class="sxs-lookup"><span data-stu-id="24968-143">0x200</span></span>      | <span data-ttu-id="24968-144">512</span><span class="sxs-lookup"><span data-stu-id="24968-144">512</span></span>           |
| <span data-ttu-id="24968-145">11</span><span class="sxs-lookup"><span data-stu-id="24968-145">11</span></span>           | <span data-ttu-id="24968-146">0x400</span><span class="sxs-lookup"><span data-stu-id="24968-146">0x400</span></span>      | <span data-ttu-id="24968-147">1024</span><span class="sxs-lookup"><span data-stu-id="24968-147">1024</span></span>          |
| <span data-ttu-id="24968-148">12</span><span class="sxs-lookup"><span data-stu-id="24968-148">12</span></span>           | <span data-ttu-id="24968-149">0x800</span><span class="sxs-lookup"><span data-stu-id="24968-149">0x800</span></span>      | <span data-ttu-id="24968-150">2.048</span><span class="sxs-lookup"><span data-stu-id="24968-150">2048</span></span>          |
| <span data-ttu-id="24968-151">13</span><span class="sxs-lookup"><span data-stu-id="24968-151">13</span></span>           | <span data-ttu-id="24968-152">0x1000</span><span class="sxs-lookup"><span data-stu-id="24968-152">0x1000</span></span>     | <span data-ttu-id="24968-153">4096</span><span class="sxs-lookup"><span data-stu-id="24968-153">4096</span></span>          |
| <span data-ttu-id="24968-154">14</span><span class="sxs-lookup"><span data-stu-id="24968-154">14</span></span>           | <span data-ttu-id="24968-155">0x2000</span><span class="sxs-lookup"><span data-stu-id="24968-155">0x2000</span></span>     | <span data-ttu-id="24968-156">8192</span><span class="sxs-lookup"><span data-stu-id="24968-156">8192</span></span>          |
| <span data-ttu-id="24968-157">15</span><span class="sxs-lookup"><span data-stu-id="24968-157">15</span></span>           | <span data-ttu-id="24968-158">0x4000</span><span class="sxs-lookup"><span data-stu-id="24968-158">0x4000</span></span>     | <span data-ttu-id="24968-159">16384</span><span class="sxs-lookup"><span data-stu-id="24968-159">16384</span></span>         |
| <span data-ttu-id="24968-160">16</span><span class="sxs-lookup"><span data-stu-id="24968-160">16</span></span>           | <span data-ttu-id="24968-161">0x8000</span><span class="sxs-lookup"><span data-stu-id="24968-161">0x8000</span></span>     | <span data-ttu-id="24968-162">32768</span><span class="sxs-lookup"><span data-stu-id="24968-162">32768</span></span>         |
| <span data-ttu-id="24968-163">17</span><span class="sxs-lookup"><span data-stu-id="24968-163">17</span></span>           | <span data-ttu-id="24968-164">0x10000</span><span class="sxs-lookup"><span data-stu-id="24968-164">0x10000</span></span>    | <span data-ttu-id="24968-165">65536</span><span class="sxs-lookup"><span data-stu-id="24968-165">65536</span></span>         |
| <span data-ttu-id="24968-166">18</span><span class="sxs-lookup"><span data-stu-id="24968-166">18</span></span>           | <span data-ttu-id="24968-167">0x20000</span><span class="sxs-lookup"><span data-stu-id="24968-167">0x20000</span></span>    | <span data-ttu-id="24968-168">131072</span><span class="sxs-lookup"><span data-stu-id="24968-168">131072</span></span>        |
| <span data-ttu-id="24968-169">19</span><span class="sxs-lookup"><span data-stu-id="24968-169">19</span></span>           | <span data-ttu-id="24968-170">0x40000</span><span class="sxs-lookup"><span data-stu-id="24968-170">0x40000</span></span>    | <span data-ttu-id="24968-171">262144</span><span class="sxs-lookup"><span data-stu-id="24968-171">262144</span></span>        |
| <span data-ttu-id="24968-172">20</span><span class="sxs-lookup"><span data-stu-id="24968-172">20</span></span>           | <span data-ttu-id="24968-173">0x80000</span><span class="sxs-lookup"><span data-stu-id="24968-173">0x80000</span></span>    | <span data-ttu-id="24968-174">524288</span><span class="sxs-lookup"><span data-stu-id="24968-174">524288</span></span>        |
| <span data-ttu-id="24968-175">21</span><span class="sxs-lookup"><span data-stu-id="24968-175">21</span></span>           | <span data-ttu-id="24968-176">0x100000</span><span class="sxs-lookup"><span data-stu-id="24968-176">0x100000</span></span>   | <span data-ttu-id="24968-177">1048576</span><span class="sxs-lookup"><span data-stu-id="24968-177">1048576</span></span>       |
| <span data-ttu-id="24968-178">22</span><span class="sxs-lookup"><span data-stu-id="24968-178">22</span></span>           | <span data-ttu-id="24968-179">0x200000</span><span class="sxs-lookup"><span data-stu-id="24968-179">0x200000</span></span>   | <span data-ttu-id="24968-180">2097152</span><span class="sxs-lookup"><span data-stu-id="24968-180">2097152</span></span>       |
| <span data-ttu-id="24968-181">23</span><span class="sxs-lookup"><span data-stu-id="24968-181">23</span></span>           | <span data-ttu-id="24968-182">0x400000</span><span class="sxs-lookup"><span data-stu-id="24968-182">0x400000</span></span>   | <span data-ttu-id="24968-183">4194304</span><span class="sxs-lookup"><span data-stu-id="24968-183">4194304</span></span>       |
| <span data-ttu-id="24968-184">24</span><span class="sxs-lookup"><span data-stu-id="24968-184">24</span></span>           | <span data-ttu-id="24968-185">0x800000</span><span class="sxs-lookup"><span data-stu-id="24968-185">0x800000</span></span>   | <span data-ttu-id="24968-186">8388608</span><span class="sxs-lookup"><span data-stu-id="24968-186">8388608</span></span>       |
| <span data-ttu-id="24968-187">25</span><span class="sxs-lookup"><span data-stu-id="24968-187">25</span></span>           | <span data-ttu-id="24968-188">0x1000000</span><span class="sxs-lookup"><span data-stu-id="24968-188">0x1000000</span></span>  | <span data-ttu-id="24968-189">16777216</span><span class="sxs-lookup"><span data-stu-id="24968-189">16777216</span></span>      |
| <span data-ttu-id="24968-190">26</span><span class="sxs-lookup"><span data-stu-id="24968-190">26</span></span>           | <span data-ttu-id="24968-191">0x2000000</span><span class="sxs-lookup"><span data-stu-id="24968-191">0x2000000</span></span>  | <span data-ttu-id="24968-192">33554432</span><span class="sxs-lookup"><span data-stu-id="24968-192">33554432</span></span>      |
| <span data-ttu-id="24968-193">27</span><span class="sxs-lookup"><span data-stu-id="24968-193">27</span></span>           | <span data-ttu-id="24968-194">0x4000000</span><span class="sxs-lookup"><span data-stu-id="24968-194">0x4000000</span></span>  | <span data-ttu-id="24968-195">67108864</span><span class="sxs-lookup"><span data-stu-id="24968-195">67108864</span></span>      |
| <span data-ttu-id="24968-196">28</span><span class="sxs-lookup"><span data-stu-id="24968-196">28</span></span>           | <span data-ttu-id="24968-197">0x8000000</span><span class="sxs-lookup"><span data-stu-id="24968-197">0x8000000</span></span>  | <span data-ttu-id="24968-198">134217728</span><span class="sxs-lookup"><span data-stu-id="24968-198">134217728</span></span>     |
| <span data-ttu-id="24968-199">29</span><span class="sxs-lookup"><span data-stu-id="24968-199">29</span></span>           | <span data-ttu-id="24968-200">0x10000000</span><span class="sxs-lookup"><span data-stu-id="24968-200">0x10000000</span></span> | <span data-ttu-id="24968-201">268435456</span><span class="sxs-lookup"><span data-stu-id="24968-201">268435456</span></span>     |
| <span data-ttu-id="24968-202">30</span><span class="sxs-lookup"><span data-stu-id="24968-202">30</span></span>           | <span data-ttu-id="24968-203">0x20000000</span><span class="sxs-lookup"><span data-stu-id="24968-203">0x20000000</span></span> | <span data-ttu-id="24968-204">536870912</span><span class="sxs-lookup"><span data-stu-id="24968-204">536870912</span></span>     |
| <span data-ttu-id="24968-205">31</span><span class="sxs-lookup"><span data-stu-id="24968-205">31</span></span>           | <span data-ttu-id="24968-206">0x40000000</span><span class="sxs-lookup"><span data-stu-id="24968-206">0x40000000</span></span> | <span data-ttu-id="24968-207">1073741824</span><span class="sxs-lookup"><span data-stu-id="24968-207">1073741824</span></span>    |
| <span data-ttu-id="24968-208">Último</span><span class="sxs-lookup"><span data-stu-id="24968-208">Last</span></span>         | <span data-ttu-id="24968-209">0x80000000</span><span class="sxs-lookup"><span data-stu-id="24968-209">0x80000000</span></span> | <span data-ttu-id="24968-210">2147483648</span><span class="sxs-lookup"><span data-stu-id="24968-210">2147483648</span></span>    |



 

<span data-ttu-id="24968-211">Ao ler ou gravar seu próprio XML para uma tarefa, os dias do mês são especificados usando o elemento [**DaysOfMonth**](taskschedulerschema-daysofmonth-monthlyscheduletype-element.md) do esquema de Agendador de tarefas.</span><span class="sxs-lookup"><span data-stu-id="24968-211">When reading or writing your own XML for a task, the days of the month are specified using the [**DaysOfMonth**](taskschedulerschema-daysofmonth-monthlyscheduletype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="24968-212">Requisitos</span><span class="sxs-lookup"><span data-stu-id="24968-212">Requirements</span></span>



| <span data-ttu-id="24968-213">Requisito</span><span class="sxs-lookup"><span data-stu-id="24968-213">Requirement</span></span> | <span data-ttu-id="24968-214">Valor</span><span class="sxs-lookup"><span data-stu-id="24968-214">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="24968-215">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="24968-215">Minimum supported client</span></span><br/> | <span data-ttu-id="24968-216">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="24968-216">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="24968-217">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="24968-217">Minimum supported server</span></span><br/> | <span data-ttu-id="24968-218">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="24968-218">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="24968-219">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="24968-219">Type library</span></span><br/>             | <dl> <span data-ttu-id="24968-220"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="24968-220"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="24968-221">DLL</span><span class="sxs-lookup"><span data-stu-id="24968-221">DLL</span></span><br/>                      | <dl> <span data-ttu-id="24968-222"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="24968-222"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="24968-223">Confira também</span><span class="sxs-lookup"><span data-stu-id="24968-223">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24968-224">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="24968-224">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="24968-225">**MonthlyTrigger**</span><span class="sxs-lookup"><span data-stu-id="24968-225">**MonthlyTrigger**</span></span>](monthlytrigger.md)
</dt> </dl>

 

 





