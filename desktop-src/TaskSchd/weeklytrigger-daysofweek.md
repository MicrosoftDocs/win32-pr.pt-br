---
title: Propriedade WeeklyTrigger. DaysOfWeek
description: Para scripts, Obtém ou define os dias da semana em que a tarefa é executada.
ms.assetid: 79f279d4-d6d2-428b-bbed-226e4eaaefb6
keywords:
- Agendador de Tarefas da Propriedade DaysOfWeek
- Propriedade DaysOfWeek Agendador de Tarefas, objeto WeeklyTrigger
- Objeto WeeklyTrigger Agendador de Tarefas, Propriedade DaysOfWeek
topic_type:
- apiref
api_name:
- WeeklyTrigger.DaysOfWeek
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7f0a27ef031e7baf46d2d3c0e33c23fb505c7ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499850"
---
# <a name="weeklytriggerdaysofweek-property"></a><span data-ttu-id="87c0c-106">Propriedade WeeklyTrigger. DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="87c0c-106">WeeklyTrigger.DaysOfWeek property</span></span>

<span data-ttu-id="87c0c-107">Para scripts, Obtém ou define os dias da semana em que a tarefa é executada.</span><span class="sxs-lookup"><span data-stu-id="87c0c-107">For scripting, gets or sets the days of the week on which the task runs.</span></span>

## <a name="syntax"></a><span data-ttu-id="87c0c-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="87c0c-108">Syntax</span></span>


```VB
WeeklyTrigger.DaysOfWeek As short
```



## <a name="property-value"></a><span data-ttu-id="87c0c-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="87c0c-109">Property value</span></span>

<span data-ttu-id="87c0c-110">Uma máscara de bits bit que indica os dias da semana em que a tarefa é executada.</span><span class="sxs-lookup"><span data-stu-id="87c0c-110">A bitwise mask that indicates the days of the week on which the task runs.</span></span>

## <a name="remarks"></a><span data-ttu-id="87c0c-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="87c0c-111">Remarks</span></span>

<span data-ttu-id="87c0c-112">A tabela a seguir mostra o mapeamento da máscara de bits bit que é usada por essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="87c0c-112">The following table shows the mapping of the bitwise mask used by this property.</span></span>



| <span data-ttu-id="87c0c-113">Mês</span><span class="sxs-lookup"><span data-stu-id="87c0c-113">Month</span></span>     | <span data-ttu-id="87c0c-114">Valor hex.</span><span class="sxs-lookup"><span data-stu-id="87c0c-114">Hex value</span></span> | <span data-ttu-id="87c0c-115">Valor decimal</span><span class="sxs-lookup"><span data-stu-id="87c0c-115">Decimal value</span></span> |
|-----------|-----------|---------------|
| <span data-ttu-id="87c0c-116">Sunday</span><span class="sxs-lookup"><span data-stu-id="87c0c-116">Sunday</span></span>    | <span data-ttu-id="87c0c-117">0X01</span><span class="sxs-lookup"><span data-stu-id="87c0c-117">0X01</span></span>      | <span data-ttu-id="87c0c-118">1</span><span class="sxs-lookup"><span data-stu-id="87c0c-118">1</span></span>             |
| <span data-ttu-id="87c0c-119">Monday</span><span class="sxs-lookup"><span data-stu-id="87c0c-119">Monday</span></span>    | <span data-ttu-id="87c0c-120">0x02</span><span class="sxs-lookup"><span data-stu-id="87c0c-120">0x02</span></span>      | <span data-ttu-id="87c0c-121">2</span><span class="sxs-lookup"><span data-stu-id="87c0c-121">2</span></span>             |
| <span data-ttu-id="87c0c-122">Terça-feira</span><span class="sxs-lookup"><span data-stu-id="87c0c-122">Tuesday</span></span>   | <span data-ttu-id="87c0c-123">0X04</span><span class="sxs-lookup"><span data-stu-id="87c0c-123">0X04</span></span>      | <span data-ttu-id="87c0c-124">4</span><span class="sxs-lookup"><span data-stu-id="87c0c-124">4</span></span>             |
| <span data-ttu-id="87c0c-125">Quarta-feira</span><span class="sxs-lookup"><span data-stu-id="87c0c-125">Wednesday</span></span> | <span data-ttu-id="87c0c-126">0X08</span><span class="sxs-lookup"><span data-stu-id="87c0c-126">0X08</span></span>      | <span data-ttu-id="87c0c-127">8</span><span class="sxs-lookup"><span data-stu-id="87c0c-127">8</span></span>             |
| <span data-ttu-id="87c0c-128">Quinta-feira</span><span class="sxs-lookup"><span data-stu-id="87c0c-128">Thursday</span></span>  | <span data-ttu-id="87c0c-129">0X10</span><span class="sxs-lookup"><span data-stu-id="87c0c-129">0X10</span></span>      | <span data-ttu-id="87c0c-130">16</span><span class="sxs-lookup"><span data-stu-id="87c0c-130">16</span></span>            |
| <span data-ttu-id="87c0c-131">Friday</span><span class="sxs-lookup"><span data-stu-id="87c0c-131">Friday</span></span>    | <span data-ttu-id="87c0c-132">0x20</span><span class="sxs-lookup"><span data-stu-id="87c0c-132">0x20</span></span>      | <span data-ttu-id="87c0c-133">32</span><span class="sxs-lookup"><span data-stu-id="87c0c-133">32</span></span>            |
| <span data-ttu-id="87c0c-134">Sábado</span><span class="sxs-lookup"><span data-stu-id="87c0c-134">Saturday</span></span>  | <span data-ttu-id="87c0c-135">0X40</span><span class="sxs-lookup"><span data-stu-id="87c0c-135">0X40</span></span>      | <span data-ttu-id="87c0c-136">64</span><span class="sxs-lookup"><span data-stu-id="87c0c-136">64</span></span>            |



 

<span data-ttu-id="87c0c-137">Ao ler ou gravar seu próprio XML para uma tarefa, os dias da semana são especificados usando o elemento [**DaysOfWeek**](taskschedulerschema-daysofweek-weeklyscheduletype-element.md) do esquema de Agendador de tarefas.</span><span class="sxs-lookup"><span data-stu-id="87c0c-137">When reading or writing your own XML for a task, the days of the week are specified using the [**DaysOfWeek**](taskschedulerschema-daysofweek-weeklyscheduletype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="87c0c-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="87c0c-138">Requirements</span></span>



| <span data-ttu-id="87c0c-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="87c0c-139">Requirement</span></span> | <span data-ttu-id="87c0c-140">Valor</span><span class="sxs-lookup"><span data-stu-id="87c0c-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="87c0c-141">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="87c0c-141">Minimum supported client</span></span><br/> | <span data-ttu-id="87c0c-142">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="87c0c-142">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="87c0c-143">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="87c0c-143">Minimum supported server</span></span><br/> | <span data-ttu-id="87c0c-144">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="87c0c-144">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="87c0c-145">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="87c0c-145">Type library</span></span><br/>             | <dl> <span data-ttu-id="87c0c-146"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="87c0c-146"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="87c0c-147">DLL</span><span class="sxs-lookup"><span data-stu-id="87c0c-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="87c0c-148"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="87c0c-148"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="87c0c-149">Confira também</span><span class="sxs-lookup"><span data-stu-id="87c0c-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87c0c-150">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="87c0c-150">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





