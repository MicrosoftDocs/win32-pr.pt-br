---
title: Propriedade MonthlyDOWTrigger. WeeksOfMonth
description: Para scripts, Obtém ou define as semanas do mês durante as quais a tarefa é executada.
ms.assetid: 62c3b654-622e-4a71-b77e-1b3fd5fb46b8
keywords:
- Agendador de Tarefas da propriedade WeeksOfMonth
- Propriedade WeeksOfMonth Agendador de Tarefas, objeto MonthlyDOWTrigger
- Objeto MonthlyDOWTrigger Agendador de Tarefas, Propriedade WeeksOfMonth
topic_type:
- apiref
api_name:
- MonthlyDOWTrigger.WeeksOfMonth
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7efea628e6eefdef07bdc50b9719a7c404f78bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454843"
---
# <a name="monthlydowtriggerweeksofmonth-property"></a><span data-ttu-id="7db00-106">Propriedade MonthlyDOWTrigger. WeeksOfMonth</span><span class="sxs-lookup"><span data-stu-id="7db00-106">MonthlyDOWTrigger.WeeksOfMonth property</span></span>

<span data-ttu-id="7db00-107">Para scripts, Obtém ou define as semanas do mês durante as quais a tarefa é executada.</span><span class="sxs-lookup"><span data-stu-id="7db00-107">For scripting, gets or sets the weeks of the month during which the task runs.</span></span>

## <a name="syntax"></a><span data-ttu-id="7db00-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="7db00-108">Syntax</span></span>


```VB
MonthlyDOWTrigger.WeeksOfMonth As short
```



## <a name="property-value"></a><span data-ttu-id="7db00-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="7db00-109">Property value</span></span>

<span data-ttu-id="7db00-110">Uma máscara de bits bit que indica os dias da semana durante os quais a tarefa é executada.</span><span class="sxs-lookup"><span data-stu-id="7db00-110">A bitwise mask that indicates the days of the week during which the task runs.</span></span>

## <a name="remarks"></a><span data-ttu-id="7db00-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="7db00-111">Remarks</span></span>

<span data-ttu-id="7db00-112">A tabela a seguir mostra o mapeamento da máscara de bits bit que é usada por essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="7db00-112">The following table shows the mapping of the bitwise mask used by this property.</span></span>



| <span data-ttu-id="7db00-113">Semana</span><span class="sxs-lookup"><span data-stu-id="7db00-113">Week</span></span>                     | <span data-ttu-id="7db00-114">Valor hex</span><span class="sxs-lookup"><span data-stu-id="7db00-114">Hex Value</span></span> | <span data-ttu-id="7db00-115">Valor decimal</span><span class="sxs-lookup"><span data-stu-id="7db00-115">Decimal Value</span></span> |
|--------------------------|-----------|---------------|
| <span data-ttu-id="7db00-116">Primeira semana do mês</span><span class="sxs-lookup"><span data-stu-id="7db00-116">First week of the month</span></span>  | <span data-ttu-id="7db00-117">0X01</span><span class="sxs-lookup"><span data-stu-id="7db00-117">0X01</span></span>      | <span data-ttu-id="7db00-118">1</span><span class="sxs-lookup"><span data-stu-id="7db00-118">1</span></span>             |
| <span data-ttu-id="7db00-119">Segunda semana do mês</span><span class="sxs-lookup"><span data-stu-id="7db00-119">Second week of the month</span></span> | <span data-ttu-id="7db00-120">0x02</span><span class="sxs-lookup"><span data-stu-id="7db00-120">0x02</span></span>      | <span data-ttu-id="7db00-121">2</span><span class="sxs-lookup"><span data-stu-id="7db00-121">2</span></span>             |
| <span data-ttu-id="7db00-122">Terceira semana do mês</span><span class="sxs-lookup"><span data-stu-id="7db00-122">Third week of the month</span></span>  | <span data-ttu-id="7db00-123">0X04</span><span class="sxs-lookup"><span data-stu-id="7db00-123">0X04</span></span>      | <span data-ttu-id="7db00-124">4</span><span class="sxs-lookup"><span data-stu-id="7db00-124">4</span></span>             |
| <span data-ttu-id="7db00-125">Quarta semana do mês</span><span class="sxs-lookup"><span data-stu-id="7db00-125">Fourth week of the month</span></span> | <span data-ttu-id="7db00-126">0X08</span><span class="sxs-lookup"><span data-stu-id="7db00-126">0X08</span></span>      | <span data-ttu-id="7db00-127">8</span><span class="sxs-lookup"><span data-stu-id="7db00-127">8</span></span>             |



 

<span data-ttu-id="7db00-128">Ao ler ou gravar XML para uma tarefa, os dias da semana de um calendário mensal de dia da semana são especificados pelo elemento [**Weeks**](taskschedulerschema-weeks-monthlydayofweekscheduletype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="7db00-128">When reading or writing XML for a task, the days of the week of a monthly day-of-week calendar are specified by the [**Weeks**](taskschedulerschema-weeks-monthlydayofweekscheduletype-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="7db00-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7db00-129">Requirements</span></span>



| <span data-ttu-id="7db00-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="7db00-130">Requirement</span></span> | <span data-ttu-id="7db00-131">Valor</span><span class="sxs-lookup"><span data-stu-id="7db00-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7db00-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7db00-132">Minimum supported client</span></span><br/> | <span data-ttu-id="7db00-133">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7db00-133">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="7db00-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7db00-134">Minimum supported server</span></span><br/> | <span data-ttu-id="7db00-135">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="7db00-135">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="7db00-136">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="7db00-136">Type library</span></span><br/>             | <dl> <span data-ttu-id="7db00-137"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="7db00-137"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="7db00-138">DLL</span><span class="sxs-lookup"><span data-stu-id="7db00-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7db00-139"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7db00-139"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7db00-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="7db00-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7db00-141">**MonthlyDOWTrigger**</span><span class="sxs-lookup"><span data-stu-id="7db00-141">**MonthlyDOWTrigger**</span></span>](monthlydowtrigger.md)
</dt> <dt>

[<span data-ttu-id="7db00-142">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="7db00-142">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





