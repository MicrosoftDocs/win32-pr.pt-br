---
title: Propriedade TaskSettings. DeleteExpiredTaskAfter
description: Para scripts, Obtém ou define a quantidade de tempo que o Agendador de Tarefas aguardará antes de excluir a tarefa depois que ela expirar.
ms.assetid: c57d736c-e3ce-44b8-809e-44f7c0321d70
keywords:
- Agendador de Tarefas da propriedade DeleteExpiredTaskAfter
- Propriedade DeleteExpiredTaskAfter Agendador de Tarefas, objeto TaskSettings
- Objeto TaskSettings Agendador de Tarefas, Propriedade DeleteExpiredTaskAfter
topic_type:
- apiref
api_name:
- TaskSettings.DeleteExpiredTaskAfter
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9005ff7988353daa902b1bc3151c539713bb94ea
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454893"
---
# <a name="tasksettingsdeleteexpiredtaskafter-property"></a><span data-ttu-id="96572-106">Propriedade TaskSettings. DeleteExpiredTaskAfter</span><span class="sxs-lookup"><span data-stu-id="96572-106">TaskSettings.DeleteExpiredTaskAfter property</span></span>

<span data-ttu-id="96572-107">Para scripts, Obtém ou define a quantidade de tempo que o Agendador de Tarefas aguardará antes de excluir a tarefa depois que ela expirar.</span><span class="sxs-lookup"><span data-stu-id="96572-107">For scripting, gets or sets the amount of time that the Task Scheduler will wait before deleting the task after it expires.</span></span> <span data-ttu-id="96572-108">Se nenhum valor for especificado para essa propriedade, o serviço de Agendador de Tarefas não excluirá a tarefa.</span><span class="sxs-lookup"><span data-stu-id="96572-108">If no value is specified for this property, then the Task Scheduler service will not delete the task.</span></span>

<span data-ttu-id="96572-109">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="96572-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="96572-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="96572-110">Syntax</span></span>


```VB
TaskSettings.DeleteExpiredTaskAfter As String
```



## <a name="property-value"></a><span data-ttu-id="96572-111">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="96572-111">Property value</span></span>

<span data-ttu-id="96572-112">Uma cadeia de caracteres que Obtém ou define a quantidade de tempo que o Agendador de Tarefas aguardará antes de excluir a tarefa depois que ela expirar.</span><span class="sxs-lookup"><span data-stu-id="96572-112">A string that gets or sets the amount of time that the Task Scheduler will wait before deleting the task after it expires.</span></span> <span data-ttu-id="96572-113">O formato dessa cadeia de caracteres é PnYnMnDTnHnMnS, onde nY é o número de anos, o nM é o número de meses, nD é o número de dias, ' T' é o separador de data/hora, nH é o número de horas, nM é o número de minutos e nS é o número de segundos (por exemplo, PT5M especifica 5 minutos e P1M4DT2H5M especifica um mês, quatro dias, duas horas e cinco minutos).</span><span class="sxs-lookup"><span data-stu-id="96572-113">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span>

## <a name="remarks"></a><span data-ttu-id="96572-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="96572-114">Remarks</span></span>

<span data-ttu-id="96572-115">Uma tarefa expira depois que o limite final foi excedido para todos os gatilhos associados à tarefa.</span><span class="sxs-lookup"><span data-stu-id="96572-115">A task expires after the end boundary has been exceeded for all triggers associated with the task.</span></span> <span data-ttu-id="96572-116">O limite final de um gatilho é especificado pela propriedade de [limite](trigger-endboundary.md) de extremidade herdada por todos os objetos de gatilho.</span><span class="sxs-lookup"><span data-stu-id="96572-116">The end boundary for a trigger is specified by the [EndBoundary](trigger-endboundary.md) property inherited by all trigger objects.</span></span>

<span data-ttu-id="96572-117">Ao ler ou gravar XML para uma tarefa, essa configuração é especificada no elemento [**DeleteExpiredTaskAfter (settingstype)**](taskschedulerschema-deleteexpiredtaskafter-settingstype-element.md) do esquema de Agendador de tarefas.</span><span class="sxs-lookup"><span data-stu-id="96572-117">When reading or writing XML for a task, this setting is specified in the [**DeleteExpiredTaskAfter (settingsType)**](taskschedulerschema-deleteexpiredtaskafter-settingstype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="96572-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="96572-118">Requirements</span></span>



| <span data-ttu-id="96572-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="96572-119">Requirement</span></span> | <span data-ttu-id="96572-120">Valor</span><span class="sxs-lookup"><span data-stu-id="96572-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="96572-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="96572-121">Minimum supported client</span></span><br/> | <span data-ttu-id="96572-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="96572-122">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="96572-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="96572-123">Minimum supported server</span></span><br/> | <span data-ttu-id="96572-124">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="96572-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="96572-125">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="96572-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="96572-126"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="96572-126"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="96572-127">DLL</span><span class="sxs-lookup"><span data-stu-id="96572-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="96572-128"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="96572-128"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="96572-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="96572-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96572-130">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="96572-130">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





