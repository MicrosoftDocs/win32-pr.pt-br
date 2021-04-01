---
title: Propriedade TaskSettings. RestartInterval
description: Para scripts, Obtém ou define um valor que especifica por quanto tempo o Agendador de Tarefas tentará reiniciar a tarefa.
ms.assetid: ad6f254d-55a8-478e-984e-a459f22043b5
keywords:
- Agendador de Tarefas da propriedade RestartInterval
- Propriedade RestartInterval Agendador de Tarefas, objeto TaskSettings
- Objeto TaskSettings Agendador de Tarefas, Propriedade RestartInterval
topic_type:
- apiref
api_name:
- TaskSettings.RestartInterval
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f511e43ebb1d61fd80f2fcab34aba092704b8338
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644380"
---
# <a name="tasksettingsrestartinterval-property"></a><span data-ttu-id="b3c73-106">Propriedade TaskSettings. RestartInterval</span><span class="sxs-lookup"><span data-stu-id="b3c73-106">TaskSettings.RestartInterval property</span></span>

<span data-ttu-id="b3c73-107">Para scripts, Obtém ou define um valor que especifica por quanto tempo o Agendador de Tarefas tentará reiniciar a tarefa.</span><span class="sxs-lookup"><span data-stu-id="b3c73-107">For scripting, gets or sets a value that specifies how long the Task Scheduler will attempt to restart the task.</span></span>

<span data-ttu-id="b3c73-108">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="b3c73-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3c73-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="b3c73-109">Syntax</span></span>


```VB
TaskSettings.RestartInterval As String
```



## <a name="property-value"></a><span data-ttu-id="b3c73-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="b3c73-110">Property value</span></span>

<span data-ttu-id="b3c73-111">Um valor que especifica quanto tempo o Agendador de Tarefas tentará reiniciar a tarefa.</span><span class="sxs-lookup"><span data-stu-id="b3c73-111">A value that specifies how long the Task Scheduler will attempt to restart the task.</span></span> <span data-ttu-id="b3c73-112">Se essa propriedade for definida, a propriedade [**RestartCount**](tasksettings-restartcount.md) também deverá ser definida.</span><span class="sxs-lookup"><span data-stu-id="b3c73-112">If this property is set, the [**RestartCount**](tasksettings-restartcount.md) property must also be set.</span></span> <span data-ttu-id="b3c73-113">O formato para essa cadeia de caracteres é P <days> dt <hours> H <minutes> M <seconds> S (por exemplo, "PT5M" é de 5 minutos, "PT1H" é de 1 hora e "PT20M" é de 20 minutos).</span><span class="sxs-lookup"><span data-stu-id="b3c73-113">The format for this string is P<days>DT<hours>H<minutes>M<seconds>S (for example, "PT5M" is 5 minutes, "PT1H" is 1 hour, and "PT20M" is 20 minutes).</span></span> <span data-ttu-id="b3c73-114">O tempo máximo permitido é de 31 dias e o tempo mínimo permitido é de 1 minuto.</span><span class="sxs-lookup"><span data-stu-id="b3c73-114">The maximum time allowed is 31 days, and the minimum time allowed is 1 minute.</span></span>

## <a name="remarks"></a><span data-ttu-id="b3c73-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="b3c73-115">Remarks</span></span>

<span data-ttu-id="b3c73-116">Ao ler ou gravar XML para uma tarefa, essa configuração é especificada no elemento [**Interval**](taskschedulerschema-interval-restarttype-element.md) do esquema de Agendador de tarefas.</span><span class="sxs-lookup"><span data-stu-id="b3c73-116">When reading or writing XML for a task, this setting is specified in the [**Interval**](taskschedulerschema-interval-restarttype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="b3c73-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b3c73-117">Requirements</span></span>



| <span data-ttu-id="b3c73-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="b3c73-118">Requirement</span></span> | <span data-ttu-id="b3c73-119">Valor</span><span class="sxs-lookup"><span data-stu-id="b3c73-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b3c73-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b3c73-120">Minimum supported client</span></span><br/> | <span data-ttu-id="b3c73-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b3c73-121">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="b3c73-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b3c73-122">Minimum supported server</span></span><br/> | <span data-ttu-id="b3c73-123">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b3c73-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b3c73-124">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="b3c73-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="b3c73-125"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="b3c73-125"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="b3c73-126">DLL</span><span class="sxs-lookup"><span data-stu-id="b3c73-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b3c73-127"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b3c73-127"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b3c73-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="b3c73-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3c73-129">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="b3c73-129">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





