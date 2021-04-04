---
title: Propriedade MonthlyDOWTrigger. MonthsOfYear
description: Para scripts, Obtém ou define os meses do ano durante os quais a tarefa é executada. | Propriedade MonthlyDOWTrigger. MonthsOfYear
ms.assetid: 4ab7ab43-9c9b-4cd3-be8f-1989b83e8cf3
keywords:
- Agendador de Tarefas da Propriedade MonthsOfYear
- Propriedade MonthsOfYear Agendador de Tarefas, objeto MonthlyDOWTrigger
- Objeto MonthlyDOWTrigger Agendador de Tarefas, Propriedade MonthsOfYear
topic_type:
- apiref
api_name:
- MonthlyDOWTrigger.MonthsOfYear
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c345cd3de12d7dba3450f62bdb18bfdcee496b13
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103837869"
---
# <a name="monthlydowtriggermonthsofyear-property"></a><span data-ttu-id="2e703-107">Propriedade MonthlyDOWTrigger. MonthsOfYear</span><span class="sxs-lookup"><span data-stu-id="2e703-107">MonthlyDOWTrigger.MonthsOfYear property</span></span>

<span data-ttu-id="2e703-108">Para scripts, Obtém ou define os meses do ano durante os quais a tarefa é executada.</span><span class="sxs-lookup"><span data-stu-id="2e703-108">For scripting, gets or sets the months of the year during which the task runs.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e703-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="2e703-109">Syntax</span></span>


```VB
MonthlyDOWTrigger.MonthsOfYear As short
```



## <a name="property-value"></a><span data-ttu-id="2e703-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="2e703-110">Property value</span></span>

<span data-ttu-id="2e703-111">Uma máscara de bits bit que indica os meses do ano durante os quais a tarefa é executada.</span><span class="sxs-lookup"><span data-stu-id="2e703-111">A bitwise mask that indicates the months of the year during which the task runs.</span></span>

## <a name="remarks"></a><span data-ttu-id="2e703-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="2e703-112">Remarks</span></span>

<span data-ttu-id="2e703-113">A tabela a seguir mostra o mapeamento da máscara de bits bit que é usada por essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="2e703-113">The following table shows the mapping of the bitwise mask used by this property.</span></span>



| <span data-ttu-id="2e703-114">Mês</span><span class="sxs-lookup"><span data-stu-id="2e703-114">Month</span></span>     | <span data-ttu-id="2e703-115">Valor hex.</span><span class="sxs-lookup"><span data-stu-id="2e703-115">Hex value</span></span> | <span data-ttu-id="2e703-116">Valor decimal</span><span class="sxs-lookup"><span data-stu-id="2e703-116">Decimal value</span></span> |
|-----------|-----------|---------------|
| <span data-ttu-id="2e703-117">Janeiro</span><span class="sxs-lookup"><span data-stu-id="2e703-117">January</span></span>   | <span data-ttu-id="2e703-118">0X01</span><span class="sxs-lookup"><span data-stu-id="2e703-118">0X01</span></span>      | <span data-ttu-id="2e703-119">1</span><span class="sxs-lookup"><span data-stu-id="2e703-119">1</span></span>             |
| <span data-ttu-id="2e703-120">Fevereiro</span><span class="sxs-lookup"><span data-stu-id="2e703-120">February</span></span>  | <span data-ttu-id="2e703-121">0x02</span><span class="sxs-lookup"><span data-stu-id="2e703-121">0x02</span></span>      | <span data-ttu-id="2e703-122">2</span><span class="sxs-lookup"><span data-stu-id="2e703-122">2</span></span>             |
| <span data-ttu-id="2e703-123">Março</span><span class="sxs-lookup"><span data-stu-id="2e703-123">March</span></span>     | <span data-ttu-id="2e703-124">0X04</span><span class="sxs-lookup"><span data-stu-id="2e703-124">0X04</span></span>      | <span data-ttu-id="2e703-125">4</span><span class="sxs-lookup"><span data-stu-id="2e703-125">4</span></span>             |
| <span data-ttu-id="2e703-126">Abril</span><span class="sxs-lookup"><span data-stu-id="2e703-126">April</span></span>     | <span data-ttu-id="2e703-127">0X08</span><span class="sxs-lookup"><span data-stu-id="2e703-127">0X08</span></span>      | <span data-ttu-id="2e703-128">8</span><span class="sxs-lookup"><span data-stu-id="2e703-128">8</span></span>             |
| <span data-ttu-id="2e703-129">Mai</span><span class="sxs-lookup"><span data-stu-id="2e703-129">May</span></span>       | <span data-ttu-id="2e703-130">0X10</span><span class="sxs-lookup"><span data-stu-id="2e703-130">0X10</span></span>      | <span data-ttu-id="2e703-131">16</span><span class="sxs-lookup"><span data-stu-id="2e703-131">16</span></span>            |
| <span data-ttu-id="2e703-132">Junho</span><span class="sxs-lookup"><span data-stu-id="2e703-132">June</span></span>      | <span data-ttu-id="2e703-133">0X20</span><span class="sxs-lookup"><span data-stu-id="2e703-133">0X20</span></span>      | <span data-ttu-id="2e703-134">32</span><span class="sxs-lookup"><span data-stu-id="2e703-134">32</span></span>            |
| <span data-ttu-id="2e703-135">Julho</span><span class="sxs-lookup"><span data-stu-id="2e703-135">July</span></span>      | <span data-ttu-id="2e703-136">0x40</span><span class="sxs-lookup"><span data-stu-id="2e703-136">0x40</span></span>      | <span data-ttu-id="2e703-137">64</span><span class="sxs-lookup"><span data-stu-id="2e703-137">64</span></span>            |
| <span data-ttu-id="2e703-138">Agosto</span><span class="sxs-lookup"><span data-stu-id="2e703-138">August</span></span>    | <span data-ttu-id="2e703-139">0X80</span><span class="sxs-lookup"><span data-stu-id="2e703-139">0X80</span></span>      | <span data-ttu-id="2e703-140">128</span><span class="sxs-lookup"><span data-stu-id="2e703-140">128</span></span>           |
| <span data-ttu-id="2e703-141">Setembro</span><span class="sxs-lookup"><span data-stu-id="2e703-141">September</span></span> | <span data-ttu-id="2e703-142">0X100</span><span class="sxs-lookup"><span data-stu-id="2e703-142">0X100</span></span>     | <span data-ttu-id="2e703-143">256</span><span class="sxs-lookup"><span data-stu-id="2e703-143">256</span></span>           |
| <span data-ttu-id="2e703-144">Outubro</span><span class="sxs-lookup"><span data-stu-id="2e703-144">October</span></span>   | <span data-ttu-id="2e703-145">0X200</span><span class="sxs-lookup"><span data-stu-id="2e703-145">0X200</span></span>     | <span data-ttu-id="2e703-146">512</span><span class="sxs-lookup"><span data-stu-id="2e703-146">512</span></span>           |
| <span data-ttu-id="2e703-147">Novembro</span><span class="sxs-lookup"><span data-stu-id="2e703-147">November</span></span>  | <span data-ttu-id="2e703-148">0X400</span><span class="sxs-lookup"><span data-stu-id="2e703-148">0X400</span></span>     | <span data-ttu-id="2e703-149">1024</span><span class="sxs-lookup"><span data-stu-id="2e703-149">1024</span></span>          |
| <span data-ttu-id="2e703-150">Dezembro</span><span class="sxs-lookup"><span data-stu-id="2e703-150">December</span></span>  | <span data-ttu-id="2e703-151">0X800</span><span class="sxs-lookup"><span data-stu-id="2e703-151">0X800</span></span>     | <span data-ttu-id="2e703-152">2.048</span><span class="sxs-lookup"><span data-stu-id="2e703-152">2048</span></span>          |



 

<span data-ttu-id="2e703-153">Ao ler ou gravar XML para uma tarefa, os meses do ano de um calendário mensal de dia da semana são especificados pelo elemento [**months**](taskschedulerschema-months-monthlydayofweekscheduletype-element.md) do esquema de Agendador de tarefas.</span><span class="sxs-lookup"><span data-stu-id="2e703-153">When reading or writing XML for a task, the months of the year of a monthly day-of-week calendar are specified by the [**Months**](taskschedulerschema-months-monthlydayofweekscheduletype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e703-154">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2e703-154">Requirements</span></span>



| <span data-ttu-id="2e703-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="2e703-155">Requirement</span></span> | <span data-ttu-id="2e703-156">Valor</span><span class="sxs-lookup"><span data-stu-id="2e703-156">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2e703-157">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2e703-157">Minimum supported client</span></span><br/> | <span data-ttu-id="2e703-158">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2e703-158">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="2e703-159">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2e703-159">Minimum supported server</span></span><br/> | <span data-ttu-id="2e703-160">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="2e703-160">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="2e703-161">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="2e703-161">Type library</span></span><br/>             | <dl> <span data-ttu-id="2e703-162"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="2e703-162"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="2e703-163">DLL</span><span class="sxs-lookup"><span data-stu-id="2e703-163">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2e703-164"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2e703-164"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2e703-165">Confira também</span><span class="sxs-lookup"><span data-stu-id="2e703-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e703-166">**MonthlyDOWTrigger**</span><span class="sxs-lookup"><span data-stu-id="2e703-166">**MonthlyDOWTrigger**</span></span>](monthlydowtrigger.md)
</dt> <dt>

[<span data-ttu-id="2e703-167">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="2e703-167">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





