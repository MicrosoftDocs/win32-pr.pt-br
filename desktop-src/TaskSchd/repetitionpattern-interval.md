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
ms.openlocfilehash: 1d62bb821f4c5e61d344e21fafa4ba1265c73470
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499520"
---
# <a name="repetitionpatterninterval-property"></a><span data-ttu-id="f16f1-106">Propriedade RepetitionPattern. Interval</span><span class="sxs-lookup"><span data-stu-id="f16f1-106">RepetitionPattern.Interval property</span></span>

<span data-ttu-id="f16f1-107">Para scripts, Obtém ou define o período de tempo entre cada reinicialização da tarefa.</span><span class="sxs-lookup"><span data-stu-id="f16f1-107">For scripting, gets or sets the amount of time between each restart of the task.</span></span>

## <a name="syntax"></a><span data-ttu-id="f16f1-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="f16f1-108">Syntax</span></span>


```VB
RepetitionPattern.Interval As String
```



## <a name="property-value"></a><span data-ttu-id="f16f1-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="f16f1-109">Property value</span></span>

<span data-ttu-id="f16f1-110">A quantidade de tempo entre cada reinicialização da tarefa.</span><span class="sxs-lookup"><span data-stu-id="f16f1-110">The amount of time between each restart of the task.</span></span> <span data-ttu-id="f16f1-111">O formato para essa cadeia de caracteres é P <days> dt <hours> H <minutes> M <seconds> S (por exemplo, "PT5M" é de 5 minutos, "PT1H" é de 1 hora e "PT20M" é de 20 minutos).</span><span class="sxs-lookup"><span data-stu-id="f16f1-111">The format for this string is P<days>DT<hours>H<minutes>M<seconds>S (for example, "PT5M" is 5 minutes, "PT1H" is 1 hour, and "PT20M" is 20 minutes).</span></span> <span data-ttu-id="f16f1-112">O tempo máximo permitido é de 31 dias e o tempo mínimo permitido é de 1 minuto.</span><span class="sxs-lookup"><span data-stu-id="f16f1-112">The maximum time allowed is 31 days, and the minimum time allowed is 1 minute.</span></span>

## <a name="remarks"></a><span data-ttu-id="f16f1-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="f16f1-113">Remarks</span></span>

<span data-ttu-id="f16f1-114">Se você especificar uma duração de repetição para uma tarefa, também deverá especificar o intervalo de repetição.</span><span class="sxs-lookup"><span data-stu-id="f16f1-114">If you specify a repetition duration for a task, you must also specify the repetition interval.</span></span>

<span data-ttu-id="f16f1-115">Ao ler ou gravar XML para uma tarefa, o intervalo de repetição é especificado no elemento [**Interval**](taskschedulerschema-interval-repetitiontype-element.md) do esquema de Agendador de tarefas.</span><span class="sxs-lookup"><span data-stu-id="f16f1-115">When reading or writing XML for a task, the repetition interval is specified in the [**Interval**](taskschedulerschema-interval-repetitiontype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="f16f1-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f16f1-116">Requirements</span></span>



| <span data-ttu-id="f16f1-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="f16f1-117">Requirement</span></span> | <span data-ttu-id="f16f1-118">Valor</span><span class="sxs-lookup"><span data-stu-id="f16f1-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f16f1-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f16f1-119">Minimum supported client</span></span><br/> | <span data-ttu-id="f16f1-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f16f1-120">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="f16f1-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f16f1-121">Minimum supported server</span></span><br/> | <span data-ttu-id="f16f1-122">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f16f1-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f16f1-123">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="f16f1-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="f16f1-124"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="f16f1-124"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="f16f1-125">DLL</span><span class="sxs-lookup"><span data-stu-id="f16f1-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f16f1-126"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f16f1-126"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f16f1-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="f16f1-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f16f1-128">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="f16f1-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





