---
title: Propriedade TaskSettings. Compatibility
description: Para scripts, Obtém ou define um valor inteiro que indica a qual versão do Agendador de Tarefas uma tarefa é compatível.
ms.assetid: bbe21177-e010-4770-9068-9c5b41974ee5
keywords:
- Agendador de Tarefas de propriedade de compatibilidade
- Propriedade de compatibilidade Agendador de Tarefas, objeto TaskSettings
- Agendador de Tarefas de objeto TaskSettings, propriedade de compatibilidade
topic_type:
- apiref
api_name:
- TaskSettings.Compatibility
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08ba93d3716a8fb0e701cc783ec83abba40190d5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644478"
---
# <a name="tasksettingscompatibility-property"></a><span data-ttu-id="41ba1-106">Propriedade TaskSettings. Compatibility</span><span class="sxs-lookup"><span data-stu-id="41ba1-106">TaskSettings.Compatibility property</span></span>

<span data-ttu-id="41ba1-107">Para scripts, Obtém ou define um valor inteiro que indica a qual versão do Agendador de Tarefas uma tarefa é compatível.</span><span class="sxs-lookup"><span data-stu-id="41ba1-107">For scripting, gets or sets an integer value that indicates which version of Task Scheduler a task is compatible with.</span></span>

<span data-ttu-id="41ba1-108">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="41ba1-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="41ba1-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="41ba1-109">Syntax</span></span>


```VB
TaskSettings.Compatibility As Integer
```



## <a name="property-value"></a><span data-ttu-id="41ba1-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="41ba1-110">Property value</span></span>



| <span data-ttu-id="41ba1-111">Valor</span><span class="sxs-lookup"><span data-stu-id="41ba1-111">Value</span></span>                                                                                                                                                                                                                                         | <span data-ttu-id="41ba1-112">Significado</span><span class="sxs-lookup"><span data-stu-id="41ba1-112">Meaning</span></span>                                                    |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <span id="TASK_COMPATIBILITY_AT"></span><span id="task_compatibility_at"></span><dl> <span data-ttu-id="41ba1-113"><dt>**Tarefa \_ do COMPATIBILIDADE \_ em**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="41ba1-113"><dt>**TASK\_COMPATIBILITY\_AT**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="41ba1-114">A tarefa é compatível com o comando AT.</span><span class="sxs-lookup"><span data-stu-id="41ba1-114">The task is compatible with the AT command.</span></span><br/>     |
| <span id="TASK_COMPATIBILITY_V1"></span><span id="task_compatibility_v1"></span><dl> <span data-ttu-id="41ba1-115"><dt>**Tarefa \_ do COMPATIBILIDADE \_ v1**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="41ba1-115"><dt>**TASK\_COMPATIBILITY\_V1**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="41ba1-116">A tarefa é compatível com o Agendador de Tarefas 1,0.</span><span class="sxs-lookup"><span data-stu-id="41ba1-116">The task is compatible with Task Scheduler 1.0.</span></span><br/> |
| <span id="TASK_COMPATIBILITY_V2"></span><span id="task_compatibility_v2"></span><dl> <span data-ttu-id="41ba1-117"><dt>**Tarefa \_ do COMPATIBILIDADE \_ v2**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="41ba1-117"><dt>**TASK\_COMPATIBILITY\_V2**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="41ba1-118">A tarefa é compatível com o Agendador de Tarefas 2,0.</span><span class="sxs-lookup"><span data-stu-id="41ba1-118">The task is compatible with Task Scheduler 2.0.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="41ba1-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="41ba1-119">Remarks</span></span>

<span data-ttu-id="41ba1-120">A compatibilidade de tarefas, que é definida por meio da propriedade de [**compatibilidade**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_compatibility) , só deve ser definida como compatibilidade de tarefas \_ \_ v1 se uma tarefa precisar ser acessada ou modificada de um computador com Windows XP, Windows Server 2003 ou Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="41ba1-120">Task compatibility, which is set through the [**Compatibility**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_compatibility) property, should only be set to TASK\_COMPATIBILITY\_V1 if a task needs to be accessed or modified from a Windows XP, Windows Server 2003, or Windows 2000 computer.</span></span> <span data-ttu-id="41ba1-121">Caso contrário, é recomendável que Agendador de Tarefas compatibilidade 2,0 seja usada porque a tarefa terá mais recursos.</span><span class="sxs-lookup"><span data-stu-id="41ba1-121">Otherwise, it is recommended that Task Scheduler 2.0 compatibility be used because the task will have more features.</span></span>

<span data-ttu-id="41ba1-122">As tarefas compatíveis com o comando AT podem ter apenas um gatilho de tempo.</span><span class="sxs-lookup"><span data-stu-id="41ba1-122">Tasks compatible with the AT command can only have one time trigger.</span></span>

<span data-ttu-id="41ba1-123">As tarefas compatíveis com Agendador de Tarefas 1,0 só podem ter um gatilho de tempo, um gatilho de logon ou um gatilho de inicialização, e a tarefa pode ter apenas uma ação executável.</span><span class="sxs-lookup"><span data-stu-id="41ba1-123">Tasks compatible with Task Scheduler 1.0 can only have a time trigger, a logon trigger, or a boot trigger, and the task can only have an executable action.</span></span>

<span data-ttu-id="41ba1-124">Para obter mais informações sobre a compatibilidade de tarefas, consulte [What ' s New in Agendador de tarefas](what-s-new-in-task-scheduler.md) and [Tasks](tasks.md).</span><span class="sxs-lookup"><span data-stu-id="41ba1-124">For more information about task compatibility, see [What's New in Task Scheduler](what-s-new-in-task-scheduler.md) and [Tasks](tasks.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="41ba1-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="41ba1-125">Requirements</span></span>



| <span data-ttu-id="41ba1-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="41ba1-126">Requirement</span></span> | <span data-ttu-id="41ba1-127">Valor</span><span class="sxs-lookup"><span data-stu-id="41ba1-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="41ba1-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="41ba1-128">Minimum supported client</span></span><br/> | <span data-ttu-id="41ba1-129">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="41ba1-129">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="41ba1-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="41ba1-130">Minimum supported server</span></span><br/> | <span data-ttu-id="41ba1-131">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="41ba1-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="41ba1-132">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="41ba1-132">Type library</span></span><br/>             | <dl> <span data-ttu-id="41ba1-133"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="41ba1-133"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="41ba1-134">DLL</span><span class="sxs-lookup"><span data-stu-id="41ba1-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="41ba1-135"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="41ba1-135"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="41ba1-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="41ba1-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41ba1-137">**compatibilidade de tarefas \_**</span><span class="sxs-lookup"><span data-stu-id="41ba1-137">**TASK\_COMPATIBILITY**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_compatibility)
</dt> <dt>

[<span data-ttu-id="41ba1-138">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="41ba1-138">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





