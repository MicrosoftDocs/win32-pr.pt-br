---
title: Propriedade TaskSettings. Priority
description: Para scripts, Obtém ou define o nível de prioridade da tarefa.
ms.assetid: 2548fcb6-c649-4822-a2ea-77546aac2ec5
keywords:
- Agendador de Tarefas da propriedade Priority
- Propriedade Priority Agendador de Tarefas, objeto TaskSettings
- Agendador de Tarefas de objeto TaskSettings, Propriedade Priority
topic_type:
- apiref
api_name:
- TaskSettings.Priority
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 282c688d63bb21f2dc0bab43acde7f089fa960b2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918084"
---
# <a name="tasksettingspriority-property"></a><span data-ttu-id="a0884-106">Propriedade TaskSettings. Priority</span><span class="sxs-lookup"><span data-stu-id="a0884-106">TaskSettings.Priority property</span></span>

<span data-ttu-id="a0884-107">Para scripts, Obtém ou define o nível de prioridade da tarefa.</span><span class="sxs-lookup"><span data-stu-id="a0884-107">For scripting, gets or sets the priority level of the task.</span></span>

<span data-ttu-id="a0884-108">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="a0884-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0884-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="a0884-109">Syntax</span></span>


```VB
TaskSettings.Priority As Integer
```



## <a name="property-value"></a><span data-ttu-id="a0884-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="a0884-110">Property value</span></span>

<span data-ttu-id="a0884-111">O nível de prioridade (0-10) da tarefa.</span><span class="sxs-lookup"><span data-stu-id="a0884-111">The priority level (0-10) of the task.</span></span> <span data-ttu-id="a0884-112">O padrão é 7.</span><span class="sxs-lookup"><span data-stu-id="a0884-112">The default is 7.</span></span>

## <a name="remarks"></a><span data-ttu-id="a0884-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="a0884-113">Remarks</span></span>

<span data-ttu-id="a0884-114">O nível de prioridade 0 é a prioridade mais alta, e o nível de prioridade 10 é a prioridade mais baixa.</span><span class="sxs-lookup"><span data-stu-id="a0884-114">Priority level 0 is the highest priority, and priority level 10 is the lowest priority.</span></span> <span data-ttu-id="a0884-115">O valor padrão é 7.</span><span class="sxs-lookup"><span data-stu-id="a0884-115">The default value is 7.</span></span> <span data-ttu-id="a0884-116">Os níveis de prioridade 7 e 8 são usados para tarefas em segundo plano, e os níveis de prioridade 4, 5 e 6 são usados para tarefas interativas.</span><span class="sxs-lookup"><span data-stu-id="a0884-116">Priority levels 7 and 8 are used for background tasks, and priority levels 4, 5, and 6 are used for interactive tasks.</span></span>

<span data-ttu-id="a0884-117">A ação da tarefa é iniciada em um processo com uma prioridade baseada em um valor de classe de prioridade.</span><span class="sxs-lookup"><span data-stu-id="a0884-117">The task's action is started in a process with a priority that is based on a Priority Class value.</span></span> <span data-ttu-id="a0884-118">Um valor de nível de prioridade (prioridade de thread) é usado para o manipulador COM, a caixa de mensagem e as ações de tarefa de email.</span><span class="sxs-lookup"><span data-stu-id="a0884-118">A Priority Level value (thread priority) is used for COM handler, message box, and email task actions.</span></span> <span data-ttu-id="a0884-119">Para obter mais informações sobre a classe de prioridade e os valores de nível de prioridade, consulte [prioridades de agendamento](/windows/desktop/ProcThread/scheduling-priorities).</span><span class="sxs-lookup"><span data-stu-id="a0884-119">For more information about the Priority Class and Priority Level values, see [Scheduling Priorities](/windows/desktop/ProcThread/scheduling-priorities).</span></span> <span data-ttu-id="a0884-120">A tabela a seguir lista os valores possíveis para o parâmetro *Priority* e os valores de classe de prioridade e nível de prioridade correspondentes.</span><span class="sxs-lookup"><span data-stu-id="a0884-120">The following table lists the possible values for the *priority* parameter, and the corresponding Priority Class and Priority Level values.</span></span>



| <span data-ttu-id="a0884-121">*Prioridade* da tarefa</span><span class="sxs-lookup"><span data-stu-id="a0884-121">Task *priority*</span></span> | <span data-ttu-id="a0884-122">Classe de prioridade</span><span class="sxs-lookup"><span data-stu-id="a0884-122">Priority Class</span></span>                 | <span data-ttu-id="a0884-123">Nível de prioridade</span><span class="sxs-lookup"><span data-stu-id="a0884-123">Priority Level</span></span>                   |
|-----------------|--------------------------------|----------------------------------|
| <span data-ttu-id="a0884-124">0</span><span class="sxs-lookup"><span data-stu-id="a0884-124">0</span></span>               | <span data-ttu-id="a0884-125">\_classe de prioridade em tempo real \_</span><span class="sxs-lookup"><span data-stu-id="a0884-125">REALTIME\_PRIORITY\_CLASS</span></span>      | <span data-ttu-id="a0884-126">tempo de prioridade de THREAD \_ \_ \_ crítico</span><span class="sxs-lookup"><span data-stu-id="a0884-126">THREAD\_PRIORITY\_TIME\_CRITICAL</span></span> |
| <span data-ttu-id="a0884-127">1</span><span class="sxs-lookup"><span data-stu-id="a0884-127">1</span></span>               | <span data-ttu-id="a0884-128">\_classe de prioridade alta \_</span><span class="sxs-lookup"><span data-stu-id="a0884-128">HIGH\_PRIORITY\_CLASS</span></span>          | <span data-ttu-id="a0884-129">prioridade de THREAD \_ \_ mais alta</span><span class="sxs-lookup"><span data-stu-id="a0884-129">THREAD\_PRIORITY\_HIGHEST</span></span>        |
| <span data-ttu-id="a0884-130">2</span><span class="sxs-lookup"><span data-stu-id="a0884-130">2</span></span>               | <span data-ttu-id="a0884-131">ACIMA \_ da \_ classe de prioridade normal \_</span><span class="sxs-lookup"><span data-stu-id="a0884-131">ABOVE\_NORMAL\_PRIORITY\_CLASS</span></span> | <span data-ttu-id="a0884-132">prioridade de THREAD \_ \_ acima do \_ normal</span><span class="sxs-lookup"><span data-stu-id="a0884-132">THREAD\_PRIORITY\_ABOVE\_NORMAL</span></span>  |
| <span data-ttu-id="a0884-133">3</span><span class="sxs-lookup"><span data-stu-id="a0884-133">3</span></span>               | <span data-ttu-id="a0884-134">ACIMA \_ da \_ classe de prioridade normal \_</span><span class="sxs-lookup"><span data-stu-id="a0884-134">ABOVE\_NORMAL\_PRIORITY\_CLASS</span></span> | <span data-ttu-id="a0884-135">prioridade de THREAD \_ \_ acima do \_ normal</span><span class="sxs-lookup"><span data-stu-id="a0884-135">THREAD\_PRIORITY\_ABOVE\_NORMAL</span></span>  |
| <span data-ttu-id="a0884-136">4</span><span class="sxs-lookup"><span data-stu-id="a0884-136">4</span></span>               | <span data-ttu-id="a0884-137">\_classe de prioridade normal \_</span><span class="sxs-lookup"><span data-stu-id="a0884-137">NORMAL\_PRIORITY\_CLASS</span></span>        | <span data-ttu-id="a0884-138">prioridade de THREAD \_ \_ normal</span><span class="sxs-lookup"><span data-stu-id="a0884-138">THREAD\_PRIORITY\_NORMAL</span></span>         |
| <span data-ttu-id="a0884-139">5</span><span class="sxs-lookup"><span data-stu-id="a0884-139">5</span></span>               | <span data-ttu-id="a0884-140">\_classe de prioridade normal \_</span><span class="sxs-lookup"><span data-stu-id="a0884-140">NORMAL\_PRIORITY\_CLASS</span></span>        | <span data-ttu-id="a0884-141">prioridade de THREAD \_ \_ normal</span><span class="sxs-lookup"><span data-stu-id="a0884-141">THREAD\_PRIORITY\_NORMAL</span></span>         |
| <span data-ttu-id="a0884-142">6</span><span class="sxs-lookup"><span data-stu-id="a0884-142">6</span></span>               | <span data-ttu-id="a0884-143">\_classe de prioridade normal \_</span><span class="sxs-lookup"><span data-stu-id="a0884-143">NORMAL\_PRIORITY\_CLASS</span></span>        | <span data-ttu-id="a0884-144">prioridade de THREAD \_ \_ normal</span><span class="sxs-lookup"><span data-stu-id="a0884-144">THREAD\_PRIORITY\_NORMAL</span></span>         |
| <span data-ttu-id="a0884-145">7</span><span class="sxs-lookup"><span data-stu-id="a0884-145">7</span></span>               | <span data-ttu-id="a0884-146">ABAIXO \_ da \_ classe de prioridade normal \_</span><span class="sxs-lookup"><span data-stu-id="a0884-146">BELOW\_NORMAL\_PRIORITY\_CLASS</span></span> | <span data-ttu-id="a0884-147">prioridade de THREAD \_ \_ abaixo do \_ normal</span><span class="sxs-lookup"><span data-stu-id="a0884-147">THREAD\_PRIORITY\_BELOW\_NORMAL</span></span>  |
| <span data-ttu-id="a0884-148">8</span><span class="sxs-lookup"><span data-stu-id="a0884-148">8</span></span>               | <span data-ttu-id="a0884-149">ABAIXO \_ da \_ classe de prioridade normal \_</span><span class="sxs-lookup"><span data-stu-id="a0884-149">BELOW\_NORMAL\_PRIORITY\_CLASS</span></span> | <span data-ttu-id="a0884-150">prioridade de THREAD \_ \_ abaixo do \_ normal</span><span class="sxs-lookup"><span data-stu-id="a0884-150">THREAD\_PRIORITY\_BELOW\_NORMAL</span></span>  |
| <span data-ttu-id="a0884-151">9</span><span class="sxs-lookup"><span data-stu-id="a0884-151">9</span></span>               | <span data-ttu-id="a0884-152">\_classe de prioridade ociosa \_</span><span class="sxs-lookup"><span data-stu-id="a0884-152">IDLE\_PRIORITY\_CLASS</span></span>          | <span data-ttu-id="a0884-153">\_prioridade \_ mais baixa da thread</span><span class="sxs-lookup"><span data-stu-id="a0884-153">THREAD\_PRIORITY\_LOWEST</span></span>         |
| <span data-ttu-id="a0884-154">10</span><span class="sxs-lookup"><span data-stu-id="a0884-154">10</span></span>              | <span data-ttu-id="a0884-155">\_classe de prioridade ociosa \_</span><span class="sxs-lookup"><span data-stu-id="a0884-155">IDLE\_PRIORITY\_CLASS</span></span>          | <span data-ttu-id="a0884-156">prioridade de THREAD \_ \_ ociosa</span><span class="sxs-lookup"><span data-stu-id="a0884-156">THREAD\_PRIORITY\_IDLE</span></span>           |



 

<span data-ttu-id="a0884-157">Ao ler ou gravar XML para uma tarefa, essa configuração é especificada no elemento [**Priority (settingstype)**](taskschedulerschema-priority-settingstype-element.md) do esquema de Agendador de tarefas.</span><span class="sxs-lookup"><span data-stu-id="a0884-157">When reading or writing XML for a task, this setting is specified in the [**Priority (settingsType)**](taskschedulerschema-priority-settingstype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="a0884-158">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a0884-158">Requirements</span></span>



| <span data-ttu-id="a0884-159">Requisito</span><span class="sxs-lookup"><span data-stu-id="a0884-159">Requirement</span></span> | <span data-ttu-id="a0884-160">Valor</span><span class="sxs-lookup"><span data-stu-id="a0884-160">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a0884-161">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a0884-161">Minimum supported client</span></span><br/> | <span data-ttu-id="a0884-162">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a0884-162">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="a0884-163">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a0884-163">Minimum supported server</span></span><br/> | <span data-ttu-id="a0884-164">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a0884-164">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a0884-165">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="a0884-165">Type library</span></span><br/>             | <dl> <span data-ttu-id="a0884-166"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="a0884-166"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="a0884-167">DLL</span><span class="sxs-lookup"><span data-stu-id="a0884-167">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a0884-168"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a0884-168"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a0884-169">Confira também</span><span class="sxs-lookup"><span data-stu-id="a0884-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0884-170">**TaskSettings**</span><span class="sxs-lookup"><span data-stu-id="a0884-170">**TaskSettings**</span></span>](tasksettings.md)
</dt> </dl>

 

