---
title: Propriedade RepetitionPattern. Duration
description: Para scripts, Obtém ou define por quanto tempo o padrão é repetido.
ms.assetid: 41a56414-981b-440a-b51a-228125baf303
keywords:
- Agendador de Tarefas da Propriedade Duration
- Propriedade Duration Agendador de Tarefas, objeto RepetitionPattern
- Agendador de Tarefas de objeto RepetitionPattern, Propriedade Duration
topic_type:
- apiref
api_name:
- RepetitionPattern.Duration
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51ff18330fd69bb54fdfb489b72f9470f707aed8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105758108"
---
# <a name="repetitionpatternduration-property"></a><span data-ttu-id="8c86f-106">Propriedade RepetitionPattern. Duration</span><span class="sxs-lookup"><span data-stu-id="8c86f-106">RepetitionPattern.Duration property</span></span>

<span data-ttu-id="8c86f-107">Para scripts, Obtém ou define por quanto tempo o padrão é repetido.</span><span class="sxs-lookup"><span data-stu-id="8c86f-107">For scripting, gets or sets how long the pattern is repeated.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c86f-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8c86f-108">Syntax</span></span>


```VB
RepetitionPattern.Duration As String
```



## <a name="property-value"></a><span data-ttu-id="8c86f-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="8c86f-109">Property value</span></span>

<span data-ttu-id="8c86f-110">Por quanto tempo o padrão é repetido.</span><span class="sxs-lookup"><span data-stu-id="8c86f-110">How long the pattern is repeated.</span></span> <span data-ttu-id="8c86f-111">O formato dessa cadeia de caracteres é PnYnMnDTnHnMnS, onde nY é o número de anos, o nM é o número de meses, nD é o número de dias, ' T' é o separador de data/hora, nH é o número de horas, nM é o número de minutos e nS é o número de segundos (por exemplo, PT5M especifica 5 minutos e P1M4DT2H5M especifica um mês, quatro dias, duas horas e cinco minutos).</span><span class="sxs-lookup"><span data-stu-id="8c86f-111">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span> <span data-ttu-id="8c86f-112">O tempo mínimo permitido é de um minuto.</span><span class="sxs-lookup"><span data-stu-id="8c86f-112">The minimum time allowed is one minute.</span></span>

<span data-ttu-id="8c86f-113">Se nenhum valor for especificado para a duração, o padrão será repetido indefinidamente.</span><span class="sxs-lookup"><span data-stu-id="8c86f-113">If no value is specified for the duration, then the pattern is repeated indefinitely.</span></span>

## <a name="remarks"></a><span data-ttu-id="8c86f-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="8c86f-114">Remarks</span></span>

<span data-ttu-id="8c86f-115">Se você especificar uma duração de repetição para uma tarefa, também deverá especificar o intervalo de repetição.</span><span class="sxs-lookup"><span data-stu-id="8c86f-115">If you specify a repetition duration for a task, you must also specify the repetition interval.</span></span>

<span data-ttu-id="8c86f-116">Ao ler ou gravar XML em uma tarefa, a duração da repetição é especificada no elemento [**Duration**](taskschedulerschema-duration-repetitiontype-element.md) do esquema de Agendador de tarefas.</span><span class="sxs-lookup"><span data-stu-id="8c86f-116">When reading or writing XML for a task, the repetition duration is specified in the [**Duration**](taskschedulerschema-duration-repetitiontype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c86f-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8c86f-117">Requirements</span></span>



| <span data-ttu-id="8c86f-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="8c86f-118">Requirement</span></span> | <span data-ttu-id="8c86f-119">Valor</span><span class="sxs-lookup"><span data-stu-id="8c86f-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8c86f-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8c86f-120">Minimum supported client</span></span><br/> | <span data-ttu-id="8c86f-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8c86f-121">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="8c86f-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8c86f-122">Minimum supported server</span></span><br/> | <span data-ttu-id="8c86f-123">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="8c86f-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="8c86f-124">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="8c86f-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="8c86f-125"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="8c86f-125"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="8c86f-126">DLL</span><span class="sxs-lookup"><span data-stu-id="8c86f-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8c86f-127"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8c86f-127"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c86f-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="8c86f-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c86f-129">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="8c86f-129">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





