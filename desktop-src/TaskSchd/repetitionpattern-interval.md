---
title: Propriedade RepetitionPattern. Interval
description: Para scripts, Obtém ou define o período de tempo entre cada reinicialização da tarefa.
ms.assetid: c48bd304-21f3-435e-99f5-3b2da0078bb8
keywords:
- Agendador de Tarefas de propriedade de intervalo
- Propriedade Interval Agendador de Tarefas, objeto RepetitionPattern
- Agendador de Tarefas de objeto RepetitionPattern, propriedade Interval
topic_type:
- apiref
api_name:
- RepetitionPattern.Interval
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c1e81920fffe5c9fd58dd36a028b924f54ebe6dd
ms.sourcegitcommit: b3a9abea47dea7374eac0f9a95a652ac6977fb2e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/20/2021
ms.locfileid: "107734171"
---
# <a name="repetitionpatterninterval-property"></a><span data-ttu-id="580c3-106">Propriedade RepetitionPattern. Interval</span><span class="sxs-lookup"><span data-stu-id="580c3-106">RepetitionPattern.Interval property</span></span>

<span data-ttu-id="580c3-107">Para scripts, Obtém ou define o período de tempo entre cada reinicialização da tarefa.</span><span class="sxs-lookup"><span data-stu-id="580c3-107">For scripting, gets or sets the amount of time between each restart of the task.</span></span>

## <a name="syntax"></a><span data-ttu-id="580c3-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="580c3-108">Syntax</span></span>


```VB
RepetitionPattern.Interval As String
```



## <a name="property-value"></a><span data-ttu-id="580c3-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="580c3-109">Property value</span></span>

<span data-ttu-id="580c3-110">A quantidade de tempo entre cada reinicialização da tarefa.</span><span class="sxs-lookup"><span data-stu-id="580c3-110">The amount of time between each restart of the task.</span></span> <span data-ttu-id="580c3-111">O formato dessa cadeia de caracteres é `P<days>DT<hours>H<minutes>M<seconds>S` (por exemplo, "PT5M" é de 5 minutos, "PT1H" é de 1 hora e "PT20M" é de 20 minutos).</span><span class="sxs-lookup"><span data-stu-id="580c3-111">The format for this string is `P<days>DT<hours>H<minutes>M<seconds>S` (for example, "PT5M" is 5 minutes, "PT1H" is 1 hour, and "PT20M" is 20 minutes).</span></span> <span data-ttu-id="580c3-112">O tempo máximo permitido é de 31 dias e o tempo mínimo permitido é de 1 minuto.</span><span class="sxs-lookup"><span data-stu-id="580c3-112">The maximum time allowed is 31 days, and the minimum time allowed is 1 minute.</span></span>

## <a name="remarks"></a><span data-ttu-id="580c3-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="580c3-113">Remarks</span></span>

<span data-ttu-id="580c3-114">Se você especificar uma duração de repetição para uma tarefa, também deverá especificar o intervalo de repetição.</span><span class="sxs-lookup"><span data-stu-id="580c3-114">If you specify a repetition duration for a task, you must also specify the repetition interval.</span></span>

<span data-ttu-id="580c3-115">Ao ler ou gravar XML para uma tarefa, o intervalo de repetição é especificado no elemento [**Interval**](taskschedulerschema-interval-repetitiontype-element.md) do esquema de Agendador de tarefas.</span><span class="sxs-lookup"><span data-stu-id="580c3-115">When reading or writing XML for a task, the repetition interval is specified in the [**Interval**](taskschedulerschema-interval-repetitiontype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="580c3-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="580c3-116">Requirements</span></span>



| <span data-ttu-id="580c3-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="580c3-117">Requirement</span></span> | <span data-ttu-id="580c3-118">Valor</span><span class="sxs-lookup"><span data-stu-id="580c3-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="580c3-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="580c3-119">Minimum supported client</span></span><br/> | <span data-ttu-id="580c3-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="580c3-120">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="580c3-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="580c3-121">Minimum supported server</span></span><br/> | <span data-ttu-id="580c3-122">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="580c3-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="580c3-123">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="580c3-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="580c3-124"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="580c3-124"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="580c3-125">DLL</span><span class="sxs-lookup"><span data-stu-id="580c3-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="580c3-126"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="580c3-126"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="580c3-127">Consulte também</span><span class="sxs-lookup"><span data-stu-id="580c3-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="580c3-128">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="580c3-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





