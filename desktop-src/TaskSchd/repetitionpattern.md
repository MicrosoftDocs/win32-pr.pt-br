---
title: Objeto RepetitionPattern
description: Objeto de script que define com que frequência a tarefa é executada e por quanto tempo o padrão de repetição é repetido depois que a tarefa é iniciada.
ms.assetid: a4e63da7-78ab-46a9-9b55-8460355753cf
keywords:
- disparadores Agendador de Tarefas, objeto de padrão de repetição
- padrão de repetição Agendador de Tarefas, objeto
- Agendador de Tarefas de objeto RepetitionPattern
- Agendador de Tarefas de objeto RepetitionPattern, descrito
topic_type:
- apiref
api_name:
- RepetitionPattern
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84b88588238c9a7e4158fe21bca8904bf6f39b51
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454899"
---
# <a name="repetitionpattern-object"></a><span data-ttu-id="462b1-107">Objeto RepetitionPattern</span><span class="sxs-lookup"><span data-stu-id="462b1-107">RepetitionPattern object</span></span>

<span data-ttu-id="462b1-108">Objeto de script que define com que frequência a tarefa é executada e por quanto tempo o padrão de repetição é repetido depois que a tarefa é iniciada.</span><span class="sxs-lookup"><span data-stu-id="462b1-108">Scripting object that defines how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span>

## <a name="members"></a><span data-ttu-id="462b1-109">Membros</span><span class="sxs-lookup"><span data-stu-id="462b1-109">Members</span></span>

<span data-ttu-id="462b1-110">O objeto **RepetitionPattern** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="462b1-110">The **RepetitionPattern** object has these types of members:</span></span>

-   [<span data-ttu-id="462b1-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="462b1-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="462b1-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="462b1-112">Properties</span></span>

<span data-ttu-id="462b1-113">O objeto **RepetitionPattern** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="462b1-113">The **RepetitionPattern** object has these properties.</span></span>



| <span data-ttu-id="462b1-114">Propriedade</span><span class="sxs-lookup"><span data-stu-id="462b1-114">Property</span></span>                                                                    | <span data-ttu-id="462b1-115">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="462b1-115">Access type</span></span>           | <span data-ttu-id="462b1-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="462b1-116">Description</span></span>                                                                                                                                        |
|:----------------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="462b1-117">**Duration**</span><span class="sxs-lookup"><span data-stu-id="462b1-117">**Duration**</span></span>](repetitionpattern-duration.md)<br/>                   | <span data-ttu-id="462b1-118">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="462b1-118">Read/write</span></span><br/> | <span data-ttu-id="462b1-119">Obtém ou define por quanto tempo o padrão é repetido.</span><span class="sxs-lookup"><span data-stu-id="462b1-119">Gets or sets how long the pattern is repeated.</span></span><br/>                                                                                          |
| [<span data-ttu-id="462b1-120">**Intervalo**</span><span class="sxs-lookup"><span data-stu-id="462b1-120">**Interval**</span></span>](repetitionpattern-interval.md)<br/>                   | <span data-ttu-id="462b1-121">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="462b1-121">Read/write</span></span><br/> | <span data-ttu-id="462b1-122">Obtém ou define o período de tempo entre cada reinicialização da tarefa.</span><span class="sxs-lookup"><span data-stu-id="462b1-122">Gets or sets the amount of time between each restart of the task.</span></span><br/>                                                                       |
| [<span data-ttu-id="462b1-123">**StopAtDurationEnd**</span><span class="sxs-lookup"><span data-stu-id="462b1-123">**StopAtDurationEnd**</span></span>](repetitionpattern-stopatdurationend.md)<br/> | <span data-ttu-id="462b1-124">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="462b1-124">Read/write</span></span><br/> | <span data-ttu-id="462b1-125">Obtém ou define um valor booliano que indica se uma instância em execução da tarefa é interrompida no final da duração do padrão de repetição.</span><span class="sxs-lookup"><span data-stu-id="462b1-125">Gets or sets a Boolean value that indicates if a running instance of the task is stopped at the end of the repetition pattern duration.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="462b1-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="462b1-126">Remarks</span></span>

<span data-ttu-id="462b1-127">Se você especificar uma duração de repetição para uma tarefa, também deverá especificar o intervalo de repetição.</span><span class="sxs-lookup"><span data-stu-id="462b1-127">If you specify a repetition duration for a task, you must also specify the repetition interval.</span></span>

<span data-ttu-id="462b1-128">Se você registrar uma tarefa que contém um gatilho com um intervalo de repetição igual a um minuto e uma duração de repetição igual a quatro minutos, a tarefa será iniciada cinco vezes.</span><span class="sxs-lookup"><span data-stu-id="462b1-128">If you register a task that contains a trigger with a repetition interval equal to one minute and a repetition duration equal to four minutes, the task will be launched five times.</span></span> <span data-ttu-id="462b1-129">As cinco repetições podem ser definidas pelo padrão a seguir.</span><span class="sxs-lookup"><span data-stu-id="462b1-129">The five repetitions can be defined by the following pattern.</span></span>

1.  <span data-ttu-id="462b1-130">Uma tarefa é iniciada no início do primeiro minuto.</span><span class="sxs-lookup"><span data-stu-id="462b1-130">A task starts at the beginning of the first minute.</span></span>
2.  <span data-ttu-id="462b1-131">A próxima tarefa é iniciada no final do primeiro minuto.</span><span class="sxs-lookup"><span data-stu-id="462b1-131">The next task starts at the end of the first minute.</span></span>
3.  <span data-ttu-id="462b1-132">A próxima tarefa é iniciada no final do segundo minuto.</span><span class="sxs-lookup"><span data-stu-id="462b1-132">The next task starts at the end of the second minute.</span></span>
4.  <span data-ttu-id="462b1-133">A próxima tarefa começa no final do terceiro minuto.</span><span class="sxs-lookup"><span data-stu-id="462b1-133">The next task starts at the end of the third minute.</span></span>
5.  <span data-ttu-id="462b1-134">A próxima tarefa é iniciada no final do quarto minuto.</span><span class="sxs-lookup"><span data-stu-id="462b1-134">The next task starts at the end of the fourth minute.</span></span>

<span data-ttu-id="462b1-135">**Windows Server 2003, Windows XP e windows 2000:** Se você registrar uma tarefa que contém um gatilho com um intervalo de repetição igual a um minuto e uma duração de repetição igual a quatro minutos, a tarefa será iniciada quatro vezes.</span><span class="sxs-lookup"><span data-stu-id="462b1-135">**Windows Server 2003, Windows XP and Windows 2000:** If you register a task that contains a trigger with a repetition interval equal to one minute and a repetition duration equal to four minutes, the task will be launched four times.</span></span>

<span data-ttu-id="462b1-136">Ao ler ou gravar XML em uma tarefa, o padrão de repetição é especificado usando o elemento de [**repetição**](taskschedulerschema-repetition-triggerbasetype-element.md) do esquema de Agendador de tarefas.</span><span class="sxs-lookup"><span data-stu-id="462b1-136">When reading or writing XML for a task, the repetition pattern is specified using the [**Repetition**](taskschedulerschema-repetition-triggerbasetype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="examples"></a><span data-ttu-id="462b1-137">Exemplos</span><span class="sxs-lookup"><span data-stu-id="462b1-137">Examples</span></span>

<span data-ttu-id="462b1-138">Para obter mais informações e código de exemplo para essa propriedade, consulte [exemplo de gatilho diário (script)](daily-trigger-example--scripting-.md).</span><span class="sxs-lookup"><span data-stu-id="462b1-138">For more information and example code for this property, see [Daily Trigger Example (Scripting)](daily-trigger-example--scripting-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="462b1-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="462b1-139">Requirements</span></span>



| <span data-ttu-id="462b1-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="462b1-140">Requirement</span></span> | <span data-ttu-id="462b1-141">Valor</span><span class="sxs-lookup"><span data-stu-id="462b1-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="462b1-142">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="462b1-142">Minimum supported client</span></span><br/> | <span data-ttu-id="462b1-143">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="462b1-143">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="462b1-144">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="462b1-144">Minimum supported server</span></span><br/> | <span data-ttu-id="462b1-145">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="462b1-145">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="462b1-146">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="462b1-146">Type library</span></span><br/>             | <dl> <span data-ttu-id="462b1-147"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="462b1-147"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="462b1-148">DLL</span><span class="sxs-lookup"><span data-stu-id="462b1-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="462b1-149"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="462b1-149"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="462b1-150">Confira também</span><span class="sxs-lookup"><span data-stu-id="462b1-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="462b1-151">Objetos Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="462b1-151">Task Scheduler Objects</span></span>](task-scheduler-objects.md)
</dt> <dt>

[<span data-ttu-id="462b1-152">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="462b1-152">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





