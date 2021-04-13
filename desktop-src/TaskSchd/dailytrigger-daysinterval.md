---
title: Propriedade DailyTrigger. DaysInterval
description: Para scripts, Obtém ou define o intervalo entre os dias no agendamento.
ms.assetid: 13e9f6fd-62ee-4b19-8b3d-a6808e146340
keywords:
- Agendador de Tarefas da propriedade DaysInterval
- Propriedade DaysInterval Agendador de Tarefas, objeto DailyTrigger
- Objeto DailyTrigger Agendador de Tarefas, Propriedade DaysInterval
topic_type:
- apiref
api_name:
- DailyTrigger.DaysInterval
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6499f3b900fe10b2a2527c2e2ee675cca3151204
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499420"
---
# <a name="dailytriggerdaysinterval-property"></a><span data-ttu-id="eb304-106">Propriedade DailyTrigger. DaysInterval</span><span class="sxs-lookup"><span data-stu-id="eb304-106">DailyTrigger.DaysInterval property</span></span>

<span data-ttu-id="eb304-107">Para scripts, Obtém ou define o intervalo entre os dias no agendamento.</span><span class="sxs-lookup"><span data-stu-id="eb304-107">For scripting, gets or sets the interval between the days in the schedule.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb304-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="eb304-108">Syntax</span></span>


```VB
DailyTrigger.DaysInterval As short
```



## <a name="property-value"></a><span data-ttu-id="eb304-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="eb304-109">Property value</span></span>

<span data-ttu-id="eb304-110">O intervalo entre os dias no agendamento.</span><span class="sxs-lookup"><span data-stu-id="eb304-110">The interval between the days in the schedule.</span></span>

## <a name="remarks"></a><span data-ttu-id="eb304-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="eb304-111">Remarks</span></span>

<span data-ttu-id="eb304-112">Um intervalo de 1 produz uma agenda diária.</span><span class="sxs-lookup"><span data-stu-id="eb304-112">An interval of 1 produces a daily schedule.</span></span> <span data-ttu-id="eb304-113">Um intervalo de 2 produz uma agenda de dia a cada outro.</span><span class="sxs-lookup"><span data-stu-id="eb304-113">An interval of 2 produces an every-other day schedule.</span></span>

<span data-ttu-id="eb304-114">Ao ler ou gravar seu próprio XML para uma tarefa, o intervalo de um agendamento diário é especificado usando o elemento [**DaysInterval**](taskschedulerschema-daysinterval-dailyscheduletype-element.md) do esquema de Agendador de tarefas.</span><span class="sxs-lookup"><span data-stu-id="eb304-114">When reading or writing your own XML for a task, the interval for a daily schedule is specified using the [**DaysInterval**](taskschedulerschema-daysinterval-dailyscheduletype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="eb304-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eb304-115">Requirements</span></span>



| <span data-ttu-id="eb304-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="eb304-116">Requirement</span></span> | <span data-ttu-id="eb304-117">Valor</span><span class="sxs-lookup"><span data-stu-id="eb304-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="eb304-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="eb304-118">Minimum supported client</span></span><br/> | <span data-ttu-id="eb304-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="eb304-119">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="eb304-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="eb304-120">Minimum supported server</span></span><br/> | <span data-ttu-id="eb304-121">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="eb304-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="eb304-122">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="eb304-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="eb304-123"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="eb304-123"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="eb304-124">DLL</span><span class="sxs-lookup"><span data-stu-id="eb304-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eb304-125"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eb304-125"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eb304-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="eb304-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb304-127">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="eb304-127">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="eb304-128">**DailyTrigger**</span><span class="sxs-lookup"><span data-stu-id="eb304-128">**DailyTrigger**</span></span>](dailytrigger.md)
</dt> </dl>

 

 





