---
title: Propriedade TaskSettings. StartWhenAvailable
description: Para scripts, Obtém ou define um valor booliano que indica que o Agendador de Tarefas pode iniciar a tarefa a qualquer momento depois que o horário agendado tiver passado.
ms.assetid: 911de67c-baf8-4346-9b4c-e39e5f96c0fe
keywords:
- Agendador de Tarefas da propriedade StartWhenAvailable
- Propriedade StartWhenAvailable Agendador de Tarefas, objeto TaskSettings
- Objeto TaskSettings Agendador de Tarefas, Propriedade StartWhenAvailable
topic_type:
- apiref
api_name:
- TaskSettings.StartWhenAvailable
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63325fbf7aa9186e5748294c2ef57302efa0c79b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455695"
---
# <a name="tasksettingsstartwhenavailable-property"></a><span data-ttu-id="3455c-106">Propriedade TaskSettings. StartWhenAvailable</span><span class="sxs-lookup"><span data-stu-id="3455c-106">TaskSettings.StartWhenAvailable property</span></span>

<span data-ttu-id="3455c-107">Para scripts, Obtém ou define um valor booliano que indica que o Agendador de Tarefas pode iniciar a tarefa a qualquer momento depois que o horário agendado tiver passado.</span><span class="sxs-lookup"><span data-stu-id="3455c-107">For scripting, gets or sets a Boolean value that indicates that the Task Scheduler can start the task at any time after its scheduled time has passed.</span></span>

<span data-ttu-id="3455c-108">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="3455c-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="3455c-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="3455c-109">Syntax</span></span>


```VB
TaskSettings.StartWhenAvailable As Boolean
```



## <a name="property-value"></a><span data-ttu-id="3455c-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="3455c-110">Property value</span></span>

<span data-ttu-id="3455c-111">Se for true, a propriedade indicará que o Agendador de Tarefas pode iniciar a tarefa a qualquer momento depois que o horário agendado tiver passado.</span><span class="sxs-lookup"><span data-stu-id="3455c-111">If True, the property indicates that the Task Scheduler can start the task at any time after its scheduled time has passed.</span></span> <span data-ttu-id="3455c-112">O padrão é False.</span><span class="sxs-lookup"><span data-stu-id="3455c-112">The default is False.</span></span>

## <a name="remarks"></a><span data-ttu-id="3455c-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="3455c-113">Remarks</span></span>

<span data-ttu-id="3455c-114">Essa propriedade se aplica somente a tarefas baseadas em tempo com um limite final ou tarefas baseadas em tempo que são definidas para repetir infinitamente.</span><span class="sxs-lookup"><span data-stu-id="3455c-114">This property applies only to time-based tasks with an end boundary or time-based tasks that are set to repeat infinitely.</span></span>

<span data-ttu-id="3455c-115">As tarefas que são iniciadas após o horário agendado passaram (devido à propriedade [**StartWhenAvailable**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_startwhenavailable) ser definida como true) são enfileiradas na fila de tarefas do serviço de Agendador de tarefas e elas são iniciadas após um atraso.</span><span class="sxs-lookup"><span data-stu-id="3455c-115">Tasks that are started after the scheduled time has passed (because of the [**StartWhenAvailable**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_startwhenavailable) property being set to True) are queued in the Task Scheduler service's queue of tasks and they are started after a delay.</span></span> <span data-ttu-id="3455c-116">O atraso padrão é 10 minutos.</span><span class="sxs-lookup"><span data-stu-id="3455c-116">The default delay is 10 minutes.</span></span>

<span data-ttu-id="3455c-117">Ao ler ou gravar XML para uma tarefa, essa configuração é especificada no elemento [**StartWhenAvailable**](taskschedulerschema-startwhenavailable-settingstype-element.md) do esquema de Agendador de tarefas.</span><span class="sxs-lookup"><span data-stu-id="3455c-117">When reading or writing XML for a task, this setting is specified in the [**StartWhenAvailable**](taskschedulerschema-startwhenavailable-settingstype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="3455c-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3455c-118">Requirements</span></span>



| <span data-ttu-id="3455c-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="3455c-119">Requirement</span></span> | <span data-ttu-id="3455c-120">Valor</span><span class="sxs-lookup"><span data-stu-id="3455c-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3455c-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3455c-121">Minimum supported client</span></span><br/> | <span data-ttu-id="3455c-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3455c-122">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="3455c-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3455c-123">Minimum supported server</span></span><br/> | <span data-ttu-id="3455c-124">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3455c-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="3455c-125">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="3455c-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="3455c-126"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="3455c-126"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="3455c-127">DLL</span><span class="sxs-lookup"><span data-stu-id="3455c-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3455c-128"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3455c-128"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3455c-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="3455c-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3455c-130">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="3455c-130">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





