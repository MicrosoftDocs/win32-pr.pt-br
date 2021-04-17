---
title: Propriedade WeeklyTrigger. WeeksInterval
description: Para scripts, Obtém ou define o intervalo entre as semanas no agendamento.
ms.assetid: 7992dee2-1725-4325-9fe9-eaff84fa5adc
keywords:
- Agendador de Tarefas da propriedade WeeksInterval
- Propriedade WeeksInterval Agendador de Tarefas, objeto WeeklyTrigger
- Objeto WeeklyTrigger Agendador de Tarefas, Propriedade WeeksInterval
topic_type:
- apiref
api_name:
- WeeklyTrigger.WeeksInterval
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4668b68d0b3f83e096284db35df799a63eb677b8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105782883"
---
# <a name="weeklytriggerweeksinterval-property"></a><span data-ttu-id="0bb7f-106">Propriedade WeeklyTrigger. WeeksInterval</span><span class="sxs-lookup"><span data-stu-id="0bb7f-106">WeeklyTrigger.WeeksInterval property</span></span>

<span data-ttu-id="0bb7f-107">Para scripts, Obtém ou define o intervalo entre as semanas no agendamento.</span><span class="sxs-lookup"><span data-stu-id="0bb7f-107">For scripting, gets or sets the interval between the weeks in the schedule.</span></span>

## <a name="syntax"></a><span data-ttu-id="0bb7f-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="0bb7f-108">Syntax</span></span>


```VB
WeeklyTrigger.WeeksInterval As short
```



## <a name="property-value"></a><span data-ttu-id="0bb7f-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="0bb7f-109">Property value</span></span>

<span data-ttu-id="0bb7f-110">O intervalo entre as semanas no agendamento.</span><span class="sxs-lookup"><span data-stu-id="0bb7f-110">The interval between the weeks in the schedule.</span></span>

## <a name="remarks"></a><span data-ttu-id="0bb7f-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="0bb7f-111">Remarks</span></span>

<span data-ttu-id="0bb7f-112">Um intervalo de 1 produz uma agenda semanal.</span><span class="sxs-lookup"><span data-stu-id="0bb7f-112">An interval of 1 produces a weekly schedule.</span></span> <span data-ttu-id="0bb7f-113">Um intervalo de 2 produz uma agenda de semana a cada uma.</span><span class="sxs-lookup"><span data-stu-id="0bb7f-113">An interval of 2 produces an every-other week schedule.</span></span>

<span data-ttu-id="0bb7f-114">Ao ler ou gravar seu próprio XML para uma tarefa, o intervalo de um agendamento semanal é especificado usando o elemento [**WeeksInterval**](taskschedulerschema-weeksinterval-weeklyscheduletype-element.md) do esquema de Agendador de tarefas.</span><span class="sxs-lookup"><span data-stu-id="0bb7f-114">When reading or writing your own XML for a task, the interval for a weekly schedule is specified using the [**WeeksInterval**](taskschedulerschema-weeksinterval-weeklyscheduletype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="0bb7f-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0bb7f-115">Requirements</span></span>



| <span data-ttu-id="0bb7f-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="0bb7f-116">Requirement</span></span> | <span data-ttu-id="0bb7f-117">Valor</span><span class="sxs-lookup"><span data-stu-id="0bb7f-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0bb7f-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0bb7f-118">Minimum supported client</span></span><br/> | <span data-ttu-id="0bb7f-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0bb7f-119">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="0bb7f-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0bb7f-120">Minimum supported server</span></span><br/> | <span data-ttu-id="0bb7f-121">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0bb7f-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="0bb7f-122">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="0bb7f-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="0bb7f-123"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="0bb7f-123"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="0bb7f-124">DLL</span><span class="sxs-lookup"><span data-stu-id="0bb7f-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0bb7f-125"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0bb7f-125"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0bb7f-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="0bb7f-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0bb7f-127">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="0bb7f-127">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





