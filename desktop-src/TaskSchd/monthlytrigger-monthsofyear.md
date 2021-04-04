---
title: Propriedade MonthlyTrigger. MonthsOfYear
description: Para scripts, Obtém ou define os meses do ano durante os quais a tarefa é executada. | Propriedade MonthlyTrigger. MonthsOfYear
ms.assetid: cf26a815-7f4f-4b7a-8db8-a4bd9b77cf49
keywords:
- Agendador de Tarefas da Propriedade MonthsOfYear
- Propriedade MonthsOfYear Agendador de Tarefas, objeto MonthlyTrigger
- Objeto MonthlyTrigger Agendador de Tarefas, Propriedade MonthsOfYear
topic_type:
- apiref
api_name:
- MonthlyTrigger.MonthsOfYear
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5683fb1c85e470ca7c82b069929de0351ea7cffe
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103837819"
---
# <a name="monthlytriggermonthsofyear-property"></a><span data-ttu-id="d1b9b-107">Propriedade MonthlyTrigger. MonthsOfYear</span><span class="sxs-lookup"><span data-stu-id="d1b9b-107">MonthlyTrigger.MonthsOfYear property</span></span>

<span data-ttu-id="d1b9b-108">Para scripts, Obtém ou define os meses do ano durante os quais a tarefa é executada.</span><span class="sxs-lookup"><span data-stu-id="d1b9b-108">For scripting, gets or sets the months of the year during which the task runs.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1b9b-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d1b9b-109">Syntax</span></span>


```VB
MonthlyTrigger.MonthsOfYear As short
```



## <a name="property-value"></a><span data-ttu-id="d1b9b-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="d1b9b-110">Property value</span></span>

<span data-ttu-id="d1b9b-111">Uma máscara de bits bit que indica os meses do ano durante os quais a tarefa é executada.</span><span class="sxs-lookup"><span data-stu-id="d1b9b-111">A bitwise mask that indicates the months of the year during which the task runs.</span></span>

## <a name="remarks"></a><span data-ttu-id="d1b9b-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="d1b9b-112">Remarks</span></span>

<span data-ttu-id="d1b9b-113">A tabela a seguir mostra o mapeamento da máscara de bits bit que é usada por essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="d1b9b-113">The following table shows the mapping of the bitwise mask that is used by this property.</span></span>



| <span data-ttu-id="d1b9b-114">Mês</span><span class="sxs-lookup"><span data-stu-id="d1b9b-114">Month</span></span>     | <span data-ttu-id="d1b9b-115">Valor hex.</span><span class="sxs-lookup"><span data-stu-id="d1b9b-115">Hex value</span></span> | <span data-ttu-id="d1b9b-116">Valor decimal</span><span class="sxs-lookup"><span data-stu-id="d1b9b-116">Decimal value</span></span> |
|-----------|-----------|---------------|
| <span data-ttu-id="d1b9b-117">Janeiro</span><span class="sxs-lookup"><span data-stu-id="d1b9b-117">January</span></span>   | <span data-ttu-id="d1b9b-118">0X01</span><span class="sxs-lookup"><span data-stu-id="d1b9b-118">0X01</span></span>      | <span data-ttu-id="d1b9b-119">1</span><span class="sxs-lookup"><span data-stu-id="d1b9b-119">1</span></span>             |
| <span data-ttu-id="d1b9b-120">Fevereiro</span><span class="sxs-lookup"><span data-stu-id="d1b9b-120">February</span></span>  | <span data-ttu-id="d1b9b-121">0x02</span><span class="sxs-lookup"><span data-stu-id="d1b9b-121">0x02</span></span>      | <span data-ttu-id="d1b9b-122">2</span><span class="sxs-lookup"><span data-stu-id="d1b9b-122">2</span></span>             |
| <span data-ttu-id="d1b9b-123">Março</span><span class="sxs-lookup"><span data-stu-id="d1b9b-123">March</span></span>     | <span data-ttu-id="d1b9b-124">0X04</span><span class="sxs-lookup"><span data-stu-id="d1b9b-124">0X04</span></span>      | <span data-ttu-id="d1b9b-125">4</span><span class="sxs-lookup"><span data-stu-id="d1b9b-125">4</span></span>             |
| <span data-ttu-id="d1b9b-126">Abril</span><span class="sxs-lookup"><span data-stu-id="d1b9b-126">April</span></span>     | <span data-ttu-id="d1b9b-127">0X08</span><span class="sxs-lookup"><span data-stu-id="d1b9b-127">0X08</span></span>      | <span data-ttu-id="d1b9b-128">8</span><span class="sxs-lookup"><span data-stu-id="d1b9b-128">8</span></span>             |
| <span data-ttu-id="d1b9b-129">Mai</span><span class="sxs-lookup"><span data-stu-id="d1b9b-129">May</span></span>       | <span data-ttu-id="d1b9b-130">0X10</span><span class="sxs-lookup"><span data-stu-id="d1b9b-130">0X10</span></span>      | <span data-ttu-id="d1b9b-131">16</span><span class="sxs-lookup"><span data-stu-id="d1b9b-131">16</span></span>            |
| <span data-ttu-id="d1b9b-132">Junho</span><span class="sxs-lookup"><span data-stu-id="d1b9b-132">June</span></span>      | <span data-ttu-id="d1b9b-133">0X20</span><span class="sxs-lookup"><span data-stu-id="d1b9b-133">0X20</span></span>      | <span data-ttu-id="d1b9b-134">32</span><span class="sxs-lookup"><span data-stu-id="d1b9b-134">32</span></span>            |
| <span data-ttu-id="d1b9b-135">Julho</span><span class="sxs-lookup"><span data-stu-id="d1b9b-135">July</span></span>      | <span data-ttu-id="d1b9b-136">0x40</span><span class="sxs-lookup"><span data-stu-id="d1b9b-136">0x40</span></span>      | <span data-ttu-id="d1b9b-137">64</span><span class="sxs-lookup"><span data-stu-id="d1b9b-137">64</span></span>            |
| <span data-ttu-id="d1b9b-138">Agosto</span><span class="sxs-lookup"><span data-stu-id="d1b9b-138">August</span></span>    | <span data-ttu-id="d1b9b-139">0X80</span><span class="sxs-lookup"><span data-stu-id="d1b9b-139">0X80</span></span>      | <span data-ttu-id="d1b9b-140">128</span><span class="sxs-lookup"><span data-stu-id="d1b9b-140">128</span></span>           |
| <span data-ttu-id="d1b9b-141">Setembro</span><span class="sxs-lookup"><span data-stu-id="d1b9b-141">September</span></span> | <span data-ttu-id="d1b9b-142">0X100</span><span class="sxs-lookup"><span data-stu-id="d1b9b-142">0X100</span></span>     | <span data-ttu-id="d1b9b-143">256</span><span class="sxs-lookup"><span data-stu-id="d1b9b-143">256</span></span>           |
| <span data-ttu-id="d1b9b-144">Outubro</span><span class="sxs-lookup"><span data-stu-id="d1b9b-144">October</span></span>   | <span data-ttu-id="d1b9b-145">0X200</span><span class="sxs-lookup"><span data-stu-id="d1b9b-145">0X200</span></span>     | <span data-ttu-id="d1b9b-146">512</span><span class="sxs-lookup"><span data-stu-id="d1b9b-146">512</span></span>           |
| <span data-ttu-id="d1b9b-147">Novembro</span><span class="sxs-lookup"><span data-stu-id="d1b9b-147">November</span></span>  | <span data-ttu-id="d1b9b-148">0X400</span><span class="sxs-lookup"><span data-stu-id="d1b9b-148">0X400</span></span>     | <span data-ttu-id="d1b9b-149">1024</span><span class="sxs-lookup"><span data-stu-id="d1b9b-149">1024</span></span>          |
| <span data-ttu-id="d1b9b-150">Dezembro</span><span class="sxs-lookup"><span data-stu-id="d1b9b-150">December</span></span>  | <span data-ttu-id="d1b9b-151">0X800</span><span class="sxs-lookup"><span data-stu-id="d1b9b-151">0X800</span></span>     | <span data-ttu-id="d1b9b-152">2.048</span><span class="sxs-lookup"><span data-stu-id="d1b9b-152">2048</span></span>          |



 

<span data-ttu-id="d1b9b-153">Ao ler ou gravar seu próprio XML para uma tarefa, os meses do ano são especificados usando o elemento [**months**](taskschedulerschema-months-monthlyscheduletype-element.md) do esquema de Agendador de tarefas.</span><span class="sxs-lookup"><span data-stu-id="d1b9b-153">When reading or writing your own XML for a task, the months of the year are specified using the [**Months**](taskschedulerschema-months-monthlyscheduletype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1b9b-154">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d1b9b-154">Requirements</span></span>



| <span data-ttu-id="d1b9b-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="d1b9b-155">Requirement</span></span> | <span data-ttu-id="d1b9b-156">Valor</span><span class="sxs-lookup"><span data-stu-id="d1b9b-156">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d1b9b-157">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d1b9b-157">Minimum supported client</span></span><br/> | <span data-ttu-id="d1b9b-158">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d1b9b-158">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="d1b9b-159">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d1b9b-159">Minimum supported server</span></span><br/> | <span data-ttu-id="d1b9b-160">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d1b9b-160">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d1b9b-161">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="d1b9b-161">Type library</span></span><br/>             | <dl> <span data-ttu-id="d1b9b-162"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="d1b9b-162"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="d1b9b-163">DLL</span><span class="sxs-lookup"><span data-stu-id="d1b9b-163">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d1b9b-164"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d1b9b-164"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d1b9b-165">Confira também</span><span class="sxs-lookup"><span data-stu-id="d1b9b-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1b9b-166">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="d1b9b-166">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="d1b9b-167">**MonthlyTrigger**</span><span class="sxs-lookup"><span data-stu-id="d1b9b-167">**MonthlyTrigger**</span></span>](monthlytrigger.md)
</dt> </dl>

 

 





