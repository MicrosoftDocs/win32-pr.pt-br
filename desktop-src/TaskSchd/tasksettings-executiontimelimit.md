---
title: TaskSettings.ExePropriedade cutionTimeLimit
description: Para scripts, Obtém ou define a quantidade de tempo permitido para concluir a tarefa.
ms.assetid: 5b8b8d4b-e705-4407-95c9-bf8baacb58c1
keywords:
- Agendador de Tarefas da propriedade ExecutionTimeLimit
- Propriedade ExecutionTimeLimit Agendador de Tarefas, objeto TaskSettings
- Objeto TaskSettings Agendador de Tarefas, Propriedade ExecutionTimeLimit
topic_type:
- apiref
api_name:
- TaskSettings.ExecutionTimeLimit
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de01d68fa7fe6c21f022d8a21863887e57016c5c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105760319"
---
# <a name="tasksettingsexecutiontimelimit-property"></a><span data-ttu-id="aa5f3-106">TaskSettings.ExePropriedade cutionTimeLimit</span><span class="sxs-lookup"><span data-stu-id="aa5f3-106">TaskSettings.ExecutionTimeLimit property</span></span>

<span data-ttu-id="aa5f3-107">Para scripts, Obtém ou define a quantidade de tempo permitido para concluir a tarefa.</span><span class="sxs-lookup"><span data-stu-id="aa5f3-107">For scripting, gets or sets the amount of time that is allowed to complete the task.</span></span> <span data-ttu-id="aa5f3-108">Por padrão, uma tarefa será interrompida em 72 horas depois de começar a ser executada.</span><span class="sxs-lookup"><span data-stu-id="aa5f3-108">By default, a task will be stopped 72 hours after it starts to run.</span></span> <span data-ttu-id="aa5f3-109">Você pode alterar isso alterando essa configuração.</span><span class="sxs-lookup"><span data-stu-id="aa5f3-109">You can change this by changing this setting.</span></span>

<span data-ttu-id="aa5f3-110">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="aa5f3-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa5f3-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="aa5f3-111">Syntax</span></span>


```VB
TaskSettings.ExecutionTimeLimit As String
```



## <a name="property-value"></a><span data-ttu-id="aa5f3-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="aa5f3-112">Property value</span></span>

<span data-ttu-id="aa5f3-113">A quantidade de tempo permitido para concluir a tarefa.</span><span class="sxs-lookup"><span data-stu-id="aa5f3-113">The amount of time that is allowed to complete the task.</span></span> <span data-ttu-id="aa5f3-114">O formato dessa cadeia de caracteres é PnYnMnDTnHnMnS, onde nY é o número de anos, o nM é o número de meses, nD é o número de dias, ' T' é o separador de data/hora, nH é o número de horas, nM é o número de minutos e nS é o número de segundos (por exemplo, PT5M especifica 5 minutos e P1M4DT2H5M especifica um mês, quatro dias, duas horas e cinco minutos).</span><span class="sxs-lookup"><span data-stu-id="aa5f3-114">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span> <span data-ttu-id="aa5f3-115">Um valor de PT0S permitirá que a tarefa seja executada indefinidamente.</span><span class="sxs-lookup"><span data-stu-id="aa5f3-115">A value of PT0S will enable the task to run indefinitely.</span></span> <span data-ttu-id="aa5f3-116">Quando esse parâmetro é definido como Nothing, o limite de tempo de execução é infinito.</span><span class="sxs-lookup"><span data-stu-id="aa5f3-116">When this parameter is set to Nothing, the execution time limit is infinite.</span></span>

## <a name="remarks"></a><span data-ttu-id="aa5f3-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="aa5f3-117">Remarks</span></span>

<span data-ttu-id="aa5f3-118">Ao ler ou gravar XML para uma tarefa, essa configuração é especificada no elemento [**ExecutionTimeLimit**](taskschedulerschema-executiontimelimit-settingstype-element.md) do esquema de Agendador de tarefas.</span><span class="sxs-lookup"><span data-stu-id="aa5f3-118">When reading or writing XML for a task, this setting is specified in the [**ExecutionTimeLimit**](taskschedulerschema-executiontimelimit-settingstype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="aa5f3-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aa5f3-119">Requirements</span></span>



| <span data-ttu-id="aa5f3-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="aa5f3-120">Requirement</span></span> | <span data-ttu-id="aa5f3-121">Valor</span><span class="sxs-lookup"><span data-stu-id="aa5f3-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="aa5f3-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="aa5f3-122">Minimum supported client</span></span><br/> | <span data-ttu-id="aa5f3-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="aa5f3-123">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="aa5f3-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="aa5f3-124">Minimum supported server</span></span><br/> | <span data-ttu-id="aa5f3-125">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="aa5f3-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="aa5f3-126">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="aa5f3-126">Type library</span></span><br/>             | <dl> <span data-ttu-id="aa5f3-127"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="aa5f3-127"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="aa5f3-128">DLL</span><span class="sxs-lookup"><span data-stu-id="aa5f3-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aa5f3-129"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aa5f3-129"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aa5f3-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="aa5f3-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa5f3-131">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="aa5f3-131">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





