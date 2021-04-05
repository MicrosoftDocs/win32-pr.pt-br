---
title: Trigger.ExePropriedade cutionTimeLimit
description: Para scripts, Obtém ou define a quantidade máxima de tempo que a tarefa iniciada pelo gatilho tem permissão para ser executada.
ms.assetid: 9993b362-f8f7-429b-a16a-1845d6f0f5e0
keywords:
- Agendador de Tarefas da propriedade ExecutionTimeLimit
- Agendador de Tarefas da propriedade ExecutionTimeLimit, objeto de gatilho
- Objeto disparador Agendador de Tarefas, Propriedade ExecutionTimeLimit
topic_type:
- apiref
api_name:
- Trigger.ExecutionTimeLimit
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 974a9adebf8ca29fe8626c938c37580d0628771b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918208"
---
# <a name="triggerexecutiontimelimit-property"></a><span data-ttu-id="f5c37-106">Trigger.ExePropriedade cutionTimeLimit</span><span class="sxs-lookup"><span data-stu-id="f5c37-106">Trigger.ExecutionTimeLimit property</span></span>

<span data-ttu-id="f5c37-107">Para scripts, Obtém ou define a quantidade máxima de tempo que a tarefa iniciada pelo gatilho tem permissão para ser executada.</span><span class="sxs-lookup"><span data-stu-id="f5c37-107">For scripting, gets or sets the maximum amount of time that the task launched by the trigger is allowed to run.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5c37-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="f5c37-108">Syntax</span></span>


```VB
Trigger.ExecutionTimeLimit As String
```



## <a name="property-value"></a><span data-ttu-id="f5c37-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="f5c37-109">Property value</span></span>

<span data-ttu-id="f5c37-110">A quantidade máxima de tempo que a tarefa iniciada pelo gatilho tem permissão para ser executada.</span><span class="sxs-lookup"><span data-stu-id="f5c37-110">The maximum amount of time that the task launched by the trigger is allowed to run.</span></span> <span data-ttu-id="f5c37-111">O formato dessa cadeia de caracteres é PnYnMnDTnHnMnS, onde nY é o número de anos, o nM é o número de meses, nD é o número de dias, ' T' é o separador de data/hora, nH é o número de horas, nM é o número de minutos e nS é o número de segundos (por exemplo, PT5M especifica 5 minutos e P1M4DT2H5M especifica um mês, quatro dias, duas horas e cinco minutos).</span><span class="sxs-lookup"><span data-stu-id="f5c37-111">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span>

## <a name="remarks"></a><span data-ttu-id="f5c37-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="f5c37-112">Remarks</span></span>

<span data-ttu-id="f5c37-113">Ao ler ou gravar XML para uma tarefa, o limite de tempo de execução é especificado no elemento [**ExecutionTimeLimit**](taskschedulerschema-executiontimelimit-triggerbasetype-element.md) do esquema de Agendador de tarefas.</span><span class="sxs-lookup"><span data-stu-id="f5c37-113">When reading or writing XML for a task, the execution time limit is specified in the [**ExecutionTimeLimit**](taskschedulerschema-executiontimelimit-triggerbasetype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="f5c37-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f5c37-114">Requirements</span></span>



| <span data-ttu-id="f5c37-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="f5c37-115">Requirement</span></span> | <span data-ttu-id="f5c37-116">Valor</span><span class="sxs-lookup"><span data-stu-id="f5c37-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f5c37-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f5c37-117">Minimum supported client</span></span><br/> | <span data-ttu-id="f5c37-118">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f5c37-118">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="f5c37-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f5c37-119">Minimum supported server</span></span><br/> | <span data-ttu-id="f5c37-120">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f5c37-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f5c37-121">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="f5c37-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="f5c37-122"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="f5c37-122"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="f5c37-123">DLL</span><span class="sxs-lookup"><span data-stu-id="f5c37-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f5c37-124"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f5c37-124"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f5c37-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="f5c37-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5c37-126">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="f5c37-126">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





