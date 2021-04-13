---
title: Propriedade MonthlyDOWTrigger. DaysOfWeek
description: Para scripts, Obtém ou define os dias da semana durante os quais a tarefa é executada.
ms.assetid: dd9b2463-69a1-4e77-a8f7-26b186d3d02d
keywords:
- Agendador de Tarefas da Propriedade DaysOfWeek
- Propriedade DaysOfWeek Agendador de Tarefas, objeto MonthlyDOWTrigger
- Objeto MonthlyDOWTrigger Agendador de Tarefas, Propriedade DaysOfWeek
topic_type:
- apiref
api_name:
- MonthlyDOWTrigger.DaysOfWeek
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15344650dabdec2bcbacf91397b37b97ce3f0772
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455713"
---
# <a name="monthlydowtriggerdaysofweek-property"></a><span data-ttu-id="eebf1-106">Propriedade MonthlyDOWTrigger. DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="eebf1-106">MonthlyDOWTrigger.DaysOfWeek property</span></span>

<span data-ttu-id="eebf1-107">Para scripts, Obtém ou define os dias da semana durante os quais a tarefa é executada.</span><span class="sxs-lookup"><span data-stu-id="eebf1-107">For scripting, gets or sets the days of the week during which the task runs.</span></span>

## <a name="syntax"></a><span data-ttu-id="eebf1-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="eebf1-108">Syntax</span></span>


```VB
MonthlyDOWTrigger.DaysOfWeek As short
```



## <a name="property-value"></a><span data-ttu-id="eebf1-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="eebf1-109">Property value</span></span>

<span data-ttu-id="eebf1-110">Uma máscara de bits bit que indica os dias da semana durante os quais a tarefa é executada.</span><span class="sxs-lookup"><span data-stu-id="eebf1-110">A bitwise mask that indicates the days of the week during which the task runs.</span></span>

## <a name="remarks"></a><span data-ttu-id="eebf1-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="eebf1-111">Remarks</span></span>

<span data-ttu-id="eebf1-112">A tabela a seguir mostra o mapeamento da máscara de bits bit que é usada por essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="eebf1-112">The following table shows the mapping of the bitwise mask used by this property.</span></span>



| <span data-ttu-id="eebf1-113">Dia da semana</span><span class="sxs-lookup"><span data-stu-id="eebf1-113">Day of Week</span></span> | <span data-ttu-id="eebf1-114">Valor hex</span><span class="sxs-lookup"><span data-stu-id="eebf1-114">Hex Value</span></span> | <span data-ttu-id="eebf1-115">Valor decimal</span><span class="sxs-lookup"><span data-stu-id="eebf1-115">Decimal Value</span></span> |
|-------------|-----------|---------------|
| <span data-ttu-id="eebf1-116">Sunday</span><span class="sxs-lookup"><span data-stu-id="eebf1-116">Sunday</span></span>      | <span data-ttu-id="eebf1-117">0x01</span><span class="sxs-lookup"><span data-stu-id="eebf1-117">0x01</span></span>      | <span data-ttu-id="eebf1-118">1</span><span class="sxs-lookup"><span data-stu-id="eebf1-118">1</span></span>             |
| <span data-ttu-id="eebf1-119">Monday</span><span class="sxs-lookup"><span data-stu-id="eebf1-119">Monday</span></span>      | <span data-ttu-id="eebf1-120">0x02</span><span class="sxs-lookup"><span data-stu-id="eebf1-120">0x02</span></span>      | <span data-ttu-id="eebf1-121">2</span><span class="sxs-lookup"><span data-stu-id="eebf1-121">2</span></span>             |
| <span data-ttu-id="eebf1-122">Terça-feira</span><span class="sxs-lookup"><span data-stu-id="eebf1-122">Tuesday</span></span>     | <span data-ttu-id="eebf1-123">0x04</span><span class="sxs-lookup"><span data-stu-id="eebf1-123">0x04</span></span>      | <span data-ttu-id="eebf1-124">4</span><span class="sxs-lookup"><span data-stu-id="eebf1-124">4</span></span>             |
| <span data-ttu-id="eebf1-125">Quarta-feira</span><span class="sxs-lookup"><span data-stu-id="eebf1-125">Wednesday</span></span>   | <span data-ttu-id="eebf1-126">0x08</span><span class="sxs-lookup"><span data-stu-id="eebf1-126">0x08</span></span>      | <span data-ttu-id="eebf1-127">8</span><span class="sxs-lookup"><span data-stu-id="eebf1-127">8</span></span>             |
| <span data-ttu-id="eebf1-128">Quinta-feira</span><span class="sxs-lookup"><span data-stu-id="eebf1-128">Thursday</span></span>    | <span data-ttu-id="eebf1-129">0x10</span><span class="sxs-lookup"><span data-stu-id="eebf1-129">0x10</span></span>      | <span data-ttu-id="eebf1-130">16</span><span class="sxs-lookup"><span data-stu-id="eebf1-130">16</span></span>            |
| <span data-ttu-id="eebf1-131">Friday</span><span class="sxs-lookup"><span data-stu-id="eebf1-131">Friday</span></span>      | <span data-ttu-id="eebf1-132">0x20</span><span class="sxs-lookup"><span data-stu-id="eebf1-132">0x20</span></span>      | <span data-ttu-id="eebf1-133">32</span><span class="sxs-lookup"><span data-stu-id="eebf1-133">32</span></span>            |
| <span data-ttu-id="eebf1-134">Sábado</span><span class="sxs-lookup"><span data-stu-id="eebf1-134">Saturday</span></span>    | <span data-ttu-id="eebf1-135">0x40</span><span class="sxs-lookup"><span data-stu-id="eebf1-135">0x40</span></span>      | <span data-ttu-id="eebf1-136">64</span><span class="sxs-lookup"><span data-stu-id="eebf1-136">64</span></span>            |



 

<span data-ttu-id="eebf1-137">Ao ler ou gravar XML para uma tarefa, os dias da semana de um calendário mensal de dia da semana são especificados pelo elemento [**DaysOfWeek**](taskschedulerschema-daysofweek-monthlydayofweekscheduletype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="eebf1-137">When reading or writing XML for a task, the days of the week of a monthly day-of-week calendar are specified by the [**DaysOfWeek**](taskschedulerschema-daysofweek-monthlydayofweekscheduletype-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="eebf1-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eebf1-138">Requirements</span></span>



| <span data-ttu-id="eebf1-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="eebf1-139">Requirement</span></span> | <span data-ttu-id="eebf1-140">Valor</span><span class="sxs-lookup"><span data-stu-id="eebf1-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="eebf1-141">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="eebf1-141">Minimum supported client</span></span><br/> | <span data-ttu-id="eebf1-142">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="eebf1-142">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="eebf1-143">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="eebf1-143">Minimum supported server</span></span><br/> | <span data-ttu-id="eebf1-144">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="eebf1-144">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="eebf1-145">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="eebf1-145">Type library</span></span><br/>             | <dl> <span data-ttu-id="eebf1-146"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="eebf1-146"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="eebf1-147">DLL</span><span class="sxs-lookup"><span data-stu-id="eebf1-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eebf1-148"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eebf1-148"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eebf1-149">Confira também</span><span class="sxs-lookup"><span data-stu-id="eebf1-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eebf1-150">**MonthlyDOWTrigger**</span><span class="sxs-lookup"><span data-stu-id="eebf1-150">**MonthlyDOWTrigger**</span></span>](monthlydowtrigger.md)
</dt> <dt>

[<span data-ttu-id="eebf1-151">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="eebf1-151">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





