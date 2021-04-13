---
title: Elemento Priority (settingstype)
description: Especifica o nível de prioridade para a tarefa.
ms.assetid: 4885fffa-b7d9-4f5e-b6e8-6f18b01c2427
keywords:
- Elemento Priority Agendador de Tarefas
topic_type:
- apiref
api_name:
- Priority
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ecda59ecbbe23550363fb30706d73bca54fcd925
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369336"
---
# <a name="priority-settingstype-element"></a><span data-ttu-id="f7400-104">Elemento Priority (settingstype)</span><span class="sxs-lookup"><span data-stu-id="f7400-104">Priority (settingsType) Element</span></span>

<span data-ttu-id="f7400-105">Especifica o nível de prioridade para a tarefa.</span><span class="sxs-lookup"><span data-stu-id="f7400-105">Specifies the priority level for the task.</span></span>

``` syntax
<xs:element name="Priority"
    type="priorityType"
    default="7"
    minOccurs="0"
 />
```

<span data-ttu-id="f7400-106">O elemento **Priority** é definido pelo tipo complexo [**settingstype**](taskschedulerschema-settingstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="f7400-106">The **Priority** element is defined by the [**settingsType**](taskschedulerschema-settingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="f7400-107">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="f7400-107">Parent element</span></span>



| <span data-ttu-id="f7400-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="f7400-108">Element</span></span>                                                           | <span data-ttu-id="f7400-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="f7400-109">Derived from</span></span>                                                         | <span data-ttu-id="f7400-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="f7400-110">Description</span></span>                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="f7400-111">**Configurações**</span><span class="sxs-lookup"><span data-stu-id="f7400-111">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md) | [<span data-ttu-id="f7400-112">**settingstype**</span><span class="sxs-lookup"><span data-stu-id="f7400-112">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md) | <span data-ttu-id="f7400-113">Contém as configurações que o Agendador de Tarefas usa para executar a tarefa.</span><span class="sxs-lookup"><span data-stu-id="f7400-113">Contains the settings that the Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="f7400-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="f7400-114">Remarks</span></span>

<span data-ttu-id="f7400-115">O nível de prioridade 0 é a prioridade mais alta, e o nível de prioridade 10 é a prioridade mais baixa.</span><span class="sxs-lookup"><span data-stu-id="f7400-115">Priority level 0 is the highest priority, and priority level 10 is the lowest priority.</span></span> <span data-ttu-id="f7400-116">O valor padrão é 7.</span><span class="sxs-lookup"><span data-stu-id="f7400-116">The default value is 7.</span></span> <span data-ttu-id="f7400-117">Os valores mínimo e máximo são definidos pelo tipo simples [**prioritytype**](taskschedulerschema-prioritytype-simpletype.md) .</span><span class="sxs-lookup"><span data-stu-id="f7400-117">The minimum and maximum values are set by the [**priorityType**](taskschedulerschema-prioritytype-simpletype.md) simple type.</span></span> <span data-ttu-id="f7400-118">Os níveis de prioridade 7 e 8 são usados para tarefas em segundo plano, e os níveis de prioridade 4, 5 e 6 são usados para tarefas interativas.</span><span class="sxs-lookup"><span data-stu-id="f7400-118">Priority levels 7 and 8 are used for background tasks, and priority levels 4, 5, and 6 are used for interactive tasks.</span></span>

<span data-ttu-id="f7400-119">A ação da tarefa é iniciada em um processo com uma prioridade baseada em um valor de classe de prioridade.</span><span class="sxs-lookup"><span data-stu-id="f7400-119">The task's action is started in a process with a priority that is based on a Priority Class value.</span></span> <span data-ttu-id="f7400-120">Um valor de nível de prioridade (prioridade de thread) é usado para o manipulador COM, a caixa de mensagem e as ações de tarefa de email.</span><span class="sxs-lookup"><span data-stu-id="f7400-120">A Priority Level value (thread priority) is used for COM handler, message box, and email task actions.</span></span> <span data-ttu-id="f7400-121">Para obter mais informações sobre a classe de prioridade e os valores de nível de prioridade, consulte [prioridades de agendamento](/windows/desktop/ProcThread/scheduling-priorities).</span><span class="sxs-lookup"><span data-stu-id="f7400-121">For more information about the Priority Class and Priority Level values, see [Scheduling Priorities](/windows/desktop/ProcThread/scheduling-priorities).</span></span> <span data-ttu-id="f7400-122">A tabela a seguir lista os valores possíveis para o elemento **Priority** e os valores de nível de prioridade e de classe de prioridade correspondentes.</span><span class="sxs-lookup"><span data-stu-id="f7400-122">The following table lists the possible values for the **Priority** element, and the corresponding Priority Class and Priority Level values.</span></span>



| <span data-ttu-id="f7400-123">Prioridade da tarefa</span><span class="sxs-lookup"><span data-stu-id="f7400-123">Task Priority</span></span> | <span data-ttu-id="f7400-124">Classe de prioridade</span><span class="sxs-lookup"><span data-stu-id="f7400-124">Priority Class</span></span>                 | <span data-ttu-id="f7400-125">Nível de prioridade</span><span class="sxs-lookup"><span data-stu-id="f7400-125">Priority Level</span></span>                   |
|---------------|--------------------------------|----------------------------------|
| <span data-ttu-id="f7400-126">0</span><span class="sxs-lookup"><span data-stu-id="f7400-126">0</span></span>             | <span data-ttu-id="f7400-127">\_classe de prioridade em tempo real \_</span><span class="sxs-lookup"><span data-stu-id="f7400-127">REALTIME\_PRIORITY\_CLASS</span></span>      | <span data-ttu-id="f7400-128">tempo de prioridade de THREAD \_ \_ \_ crítico</span><span class="sxs-lookup"><span data-stu-id="f7400-128">THREAD\_PRIORITY\_TIME\_CRITICAL</span></span> |
| <span data-ttu-id="f7400-129">1</span><span class="sxs-lookup"><span data-stu-id="f7400-129">1</span></span>             | <span data-ttu-id="f7400-130">\_classe de prioridade alta \_</span><span class="sxs-lookup"><span data-stu-id="f7400-130">HIGH\_PRIORITY\_CLASS</span></span>          | <span data-ttu-id="f7400-131">prioridade de THREAD \_ \_ mais alta</span><span class="sxs-lookup"><span data-stu-id="f7400-131">THREAD\_PRIORITY\_HIGHEST</span></span>        |
| <span data-ttu-id="f7400-132">2</span><span class="sxs-lookup"><span data-stu-id="f7400-132">2</span></span>             | <span data-ttu-id="f7400-133">ACIMA \_ da \_ classe de prioridade normal \_</span><span class="sxs-lookup"><span data-stu-id="f7400-133">ABOVE\_NORMAL\_PRIORITY\_CLASS</span></span> | <span data-ttu-id="f7400-134">prioridade de THREAD \_ \_ acima do \_ normal</span><span class="sxs-lookup"><span data-stu-id="f7400-134">THREAD\_PRIORITY\_ABOVE\_NORMAL</span></span>  |
| <span data-ttu-id="f7400-135">3</span><span class="sxs-lookup"><span data-stu-id="f7400-135">3</span></span>             | <span data-ttu-id="f7400-136">ACIMA \_ da \_ classe de prioridade normal \_</span><span class="sxs-lookup"><span data-stu-id="f7400-136">ABOVE\_NORMAL\_PRIORITY\_CLASS</span></span> | <span data-ttu-id="f7400-137">prioridade de THREAD \_ \_ acima do \_ normal</span><span class="sxs-lookup"><span data-stu-id="f7400-137">THREAD\_PRIORITY\_ABOVE\_NORMAL</span></span>  |
| <span data-ttu-id="f7400-138">4</span><span class="sxs-lookup"><span data-stu-id="f7400-138">4</span></span>             | <span data-ttu-id="f7400-139">\_classe de prioridade normal \_</span><span class="sxs-lookup"><span data-stu-id="f7400-139">NORMAL\_PRIORITY\_CLASS</span></span>        | <span data-ttu-id="f7400-140">prioridade de THREAD \_ \_ normal</span><span class="sxs-lookup"><span data-stu-id="f7400-140">THREAD\_PRIORITY\_NORMAL</span></span>         |
| <span data-ttu-id="f7400-141">5</span><span class="sxs-lookup"><span data-stu-id="f7400-141">5</span></span>             | <span data-ttu-id="f7400-142">\_classe de prioridade normal \_</span><span class="sxs-lookup"><span data-stu-id="f7400-142">NORMAL\_PRIORITY\_CLASS</span></span>        | <span data-ttu-id="f7400-143">prioridade de THREAD \_ \_ normal</span><span class="sxs-lookup"><span data-stu-id="f7400-143">THREAD\_PRIORITY\_NORMAL</span></span>         |
| <span data-ttu-id="f7400-144">6</span><span class="sxs-lookup"><span data-stu-id="f7400-144">6</span></span>             | <span data-ttu-id="f7400-145">\_classe de prioridade normal \_</span><span class="sxs-lookup"><span data-stu-id="f7400-145">NORMAL\_PRIORITY\_CLASS</span></span>        | <span data-ttu-id="f7400-146">prioridade de THREAD \_ \_ normal</span><span class="sxs-lookup"><span data-stu-id="f7400-146">THREAD\_PRIORITY\_NORMAL</span></span>         |
| <span data-ttu-id="f7400-147">7</span><span class="sxs-lookup"><span data-stu-id="f7400-147">7</span></span>             | <span data-ttu-id="f7400-148">ABAIXO \_ da \_ classe de prioridade normal \_</span><span class="sxs-lookup"><span data-stu-id="f7400-148">BELOW\_NORMAL\_PRIORITY\_CLASS</span></span> | <span data-ttu-id="f7400-149">prioridade de THREAD \_ \_ abaixo do \_ normal</span><span class="sxs-lookup"><span data-stu-id="f7400-149">THREAD\_PRIORITY\_BELOW\_NORMAL</span></span>  |
| <span data-ttu-id="f7400-150">8</span><span class="sxs-lookup"><span data-stu-id="f7400-150">8</span></span>             | <span data-ttu-id="f7400-151">ABAIXO \_ da \_ classe de prioridade normal \_</span><span class="sxs-lookup"><span data-stu-id="f7400-151">BELOW\_NORMAL\_PRIORITY\_CLASS</span></span> | <span data-ttu-id="f7400-152">prioridade de THREAD \_ \_ abaixo do \_ normal</span><span class="sxs-lookup"><span data-stu-id="f7400-152">THREAD\_PRIORITY\_BELOW\_NORMAL</span></span>  |
| <span data-ttu-id="f7400-153">9</span><span class="sxs-lookup"><span data-stu-id="f7400-153">9</span></span>             | <span data-ttu-id="f7400-154">\_classe de prioridade ociosa \_</span><span class="sxs-lookup"><span data-stu-id="f7400-154">IDLE\_PRIORITY\_CLASS</span></span>          | <span data-ttu-id="f7400-155">\_prioridade \_ mais baixa da thread</span><span class="sxs-lookup"><span data-stu-id="f7400-155">THREAD\_PRIORITY\_LOWEST</span></span>         |
| <span data-ttu-id="f7400-156">10</span><span class="sxs-lookup"><span data-stu-id="f7400-156">10</span></span>            | <span data-ttu-id="f7400-157">\_classe de prioridade ociosa \_</span><span class="sxs-lookup"><span data-stu-id="f7400-157">IDLE\_PRIORITY\_CLASS</span></span>          | <span data-ttu-id="f7400-158">prioridade de THREAD \_ \_ ociosa</span><span class="sxs-lookup"><span data-stu-id="f7400-158">THREAD\_PRIORITY\_IDLE</span></span>           |



 

<span data-ttu-id="f7400-159">Para desenvolvimento em C++, consulte [**Propriedade Priority de ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_priority).</span><span class="sxs-lookup"><span data-stu-id="f7400-159">For C++ development, see [**Priority Property of ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_priority).</span></span>

<span data-ttu-id="f7400-160">Para desenvolvimento de script, consulte [**TaskSettings. Priority**](tasksettings-priority.md).</span><span class="sxs-lookup"><span data-stu-id="f7400-160">For script development, see [**TaskSettings.Priority**](tasksettings-priority.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f7400-161">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f7400-161">Requirements</span></span>



| <span data-ttu-id="f7400-162">Requisito</span><span class="sxs-lookup"><span data-stu-id="f7400-162">Requirement</span></span> | <span data-ttu-id="f7400-163">Valor</span><span class="sxs-lookup"><span data-stu-id="f7400-163">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f7400-164">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f7400-164">Minimum supported client</span></span><br/> | <span data-ttu-id="f7400-165">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f7400-165">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="f7400-166">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f7400-166">Minimum supported server</span></span><br/> | <span data-ttu-id="f7400-167">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f7400-167">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f7400-168">Confira também</span><span class="sxs-lookup"><span data-stu-id="f7400-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7400-169">Elementos do esquema de Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="f7400-169">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

