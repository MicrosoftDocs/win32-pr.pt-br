---
title: Interfaces de gatilho
description: As APIs que são usadas para gerenciar gatilhos variam de acordo com a versão do Agendador de Tarefas. No entanto, em ambos os casos, essas APIs permitem criar novos gatilhos, recuperar e atualizar gatilhos existentes e excluir gatilhos que não são mais necessários.
ms.assetid: 94c11f11-72e2-404f-b396-ab7b1be71942
keywords:
- gatilhos Agendador de Tarefas, interfaces
- disparadores Agendador de Tarefas, interfaces, descritos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5357bb745b43c51707d9571c7582a44c9225a7fe
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104294620"
---
# <a name="trigger-interfaces"></a><span data-ttu-id="e00e6-106">Interfaces de gatilho</span><span class="sxs-lookup"><span data-stu-id="e00e6-106">Trigger Interfaces</span></span>

<span data-ttu-id="e00e6-107">As APIs que são usadas para gerenciar gatilhos variam de acordo com a versão do Agendador de Tarefas.</span><span class="sxs-lookup"><span data-stu-id="e00e6-107">The APIs that are used to manage triggers vary depending on the version of the Task Scheduler.</span></span> <span data-ttu-id="e00e6-108">No entanto, em ambos os casos, essas APIs permitem criar novos gatilhos, recuperar e atualizar gatilhos existentes e excluir gatilhos que não são mais necessários.</span><span class="sxs-lookup"><span data-stu-id="e00e6-108">However, in both cases these APIs enable you to create new triggers, retrieve and update existing triggers, and delete triggers that are no longer required.</span></span>


<span data-ttu-id="e00e6-109">Os aplicativos desenvolvidos usando Agendador de Tarefas 2,0 podem usar objetos e interfaces para criar, recuperar, modificar e excluir os gatilhos de uma tarefa.</span><span class="sxs-lookup"><span data-stu-id="e00e6-109">Applications that are developed using Task Scheduler 2.0 can use objects and interfaces to create, retrieve, modify, and delete the triggers for a task.</span></span>

<span data-ttu-id="e00e6-110">Na ilustração a seguir, uma tarefa especifica uma coleção de gatilhos usando sua propriedade Triggers.</span><span class="sxs-lookup"><span data-stu-id="e00e6-110">In the following illustration, a task specifies a collection of triggers using its Triggers property.</span></span> <span data-ttu-id="e00e6-111">Esta coleção contém uma ou mais APIs de gatilho individuais com cada API especificando um tipo de gatilho específico.</span><span class="sxs-lookup"><span data-stu-id="e00e6-111">This collection contains one or more individual trigger APIs with each API specifying a specific trigger type.</span></span> <span data-ttu-id="e00e6-112">Por exemplo, na ilustração abaixo, a coleção de gatilho contém um gatilho de inicialização, um gatilho de logon e um gatilho diário.</span><span class="sxs-lookup"><span data-stu-id="e00e6-112">For example, in the illustration below the trigger collection contains a boot trigger, logon trigger, and a daily trigger.</span></span>

![interfaces de gatilho do Agendador de tarefas 2,0](images/tsktri4.png)

### <a name="object-apis-for-scripting-development"></a><span data-ttu-id="e00e6-114">APIs de objeto para desenvolvimento de scripts</span><span class="sxs-lookup"><span data-stu-id="e00e6-114">Object APIs for Scripting Development</span></span>

<span data-ttu-id="e00e6-115">Para obter mais informações sobre os métodos e as propriedades dos objetos usados para especificar gatilhos, consulte:</span><span class="sxs-lookup"><span data-stu-id="e00e6-115">For more information about the methods and properties of the objects that are used to specify triggers, see:</span></span>

-   [<span data-ttu-id="e00e6-116">**TaskDefinition**</span><span class="sxs-lookup"><span data-stu-id="e00e6-116">**TaskDefinition**</span></span>](taskdefinition.md)
-   [<span data-ttu-id="e00e6-117">**Disparador**</span><span class="sxs-lookup"><span data-stu-id="e00e6-117">**TriggerCollection**</span></span>](triggercollection.md)
-   [<span data-ttu-id="e00e6-118">**Of**</span><span class="sxs-lookup"><span data-stu-id="e00e6-118">**Trigger**</span></span>](trigger.md)
-   [<span data-ttu-id="e00e6-119">**BootTrigger**</span><span class="sxs-lookup"><span data-stu-id="e00e6-119">**BootTrigger**</span></span>](boottrigger.md)
-   [<span data-ttu-id="e00e6-120">**DailyTrigger**</span><span class="sxs-lookup"><span data-stu-id="e00e6-120">**DailyTrigger**</span></span>](dailytrigger.md)
-   [<span data-ttu-id="e00e6-121">**EventTrigger**</span><span class="sxs-lookup"><span data-stu-id="e00e6-121">**EventTrigger**</span></span>](eventtrigger.md)
-   [<span data-ttu-id="e00e6-122">**IdleTrigger**</span><span class="sxs-lookup"><span data-stu-id="e00e6-122">**IdleTrigger**</span></span>](idletrigger.md)
-   [<span data-ttu-id="e00e6-123">**LogonTrigger**</span><span class="sxs-lookup"><span data-stu-id="e00e6-123">**LogonTrigger**</span></span>](logontrigger.md)
-   [<span data-ttu-id="e00e6-124">**MonthlyDOWTrigger**</span><span class="sxs-lookup"><span data-stu-id="e00e6-124">**MonthlyDOWTrigger**</span></span>](monthlydowtrigger.md)
-   [<span data-ttu-id="e00e6-125">**MonthlyTrigger**</span><span class="sxs-lookup"><span data-stu-id="e00e6-125">**MonthlyTrigger**</span></span>](monthlytrigger.md)
-   [<span data-ttu-id="e00e6-126">**RegistrationTrigger**</span><span class="sxs-lookup"><span data-stu-id="e00e6-126">**RegistrationTrigger**</span></span>](registrationtrigger.md)
-   [<span data-ttu-id="e00e6-127">**TimeTrigger**</span><span class="sxs-lookup"><span data-stu-id="e00e6-127">**TimeTrigger**</span></span>](timetrigger.md)
-   [<span data-ttu-id="e00e6-128">**WeeklyTrigger**</span><span class="sxs-lookup"><span data-stu-id="e00e6-128">**WeeklyTrigger**</span></span>](weeklytrigger.md)

### <a name="interfaces-apis-for-c-development"></a><span data-ttu-id="e00e6-129">APIs de interfaces para desenvolvimento em C++</span><span class="sxs-lookup"><span data-stu-id="e00e6-129">Interfaces APIs for C++ Development</span></span>

<span data-ttu-id="e00e6-130">Para obter mais informações sobre os métodos e as propriedades das interfaces usadas para especificar gatilhos, consulte:</span><span class="sxs-lookup"><span data-stu-id="e00e6-130">For more information about the methods and properties of the interfaces that are used to specify triggers, see:</span></span>

-   [<span data-ttu-id="e00e6-131">**ITaskDefinition**</span><span class="sxs-lookup"><span data-stu-id="e00e6-131">**ITaskDefinition**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition)
-   [<span data-ttu-id="e00e6-132">**ITriggerCollection**</span><span class="sxs-lookup"><span data-stu-id="e00e6-132">**ITriggerCollection**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-itriggercollection)
-   [<span data-ttu-id="e00e6-133">**ITrigger**</span><span class="sxs-lookup"><span data-stu-id="e00e6-133">**ITrigger**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-itrigger)
-   [<span data-ttu-id="e00e6-134">**IBootTrigger**</span><span class="sxs-lookup"><span data-stu-id="e00e6-134">**IBootTrigger**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-iboottrigger)
-   [<span data-ttu-id="e00e6-135">**IDailyTrigger**</span><span class="sxs-lookup"><span data-stu-id="e00e6-135">**IDailyTrigger**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-idailytrigger)
-   [<span data-ttu-id="e00e6-136">**IEventTrigger**</span><span class="sxs-lookup"><span data-stu-id="e00e6-136">**IEventTrigger**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-ieventtrigger)
-   [<span data-ttu-id="e00e6-137">**IIdleTrigger**</span><span class="sxs-lookup"><span data-stu-id="e00e6-137">**IIdleTrigger**</span></span>](/windows/win32/api/taskschd/nn-taskschd-iidletrigger)
-   [<span data-ttu-id="e00e6-138">**ILogonTrigger**</span><span class="sxs-lookup"><span data-stu-id="e00e6-138">**ILogonTrigger**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-ilogontrigger)
-   [<span data-ttu-id="e00e6-139">**IMonthlyDOWTrigger**</span><span class="sxs-lookup"><span data-stu-id="e00e6-139">**IMonthlyDOWTrigger**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-imonthlydowtrigger)
-   [<span data-ttu-id="e00e6-140">**IMonthlyTrigger**</span><span class="sxs-lookup"><span data-stu-id="e00e6-140">**IMonthlyTrigger**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-imonthlytrigger)
-   [<span data-ttu-id="e00e6-141">**IRegistrationTrigger**</span><span class="sxs-lookup"><span data-stu-id="e00e6-141">**IRegistrationTrigger**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-iregistrationtrigger)
-   [<span data-ttu-id="e00e6-142">**ITimeTrigger**</span><span class="sxs-lookup"><span data-stu-id="e00e6-142">**ITimeTrigger**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-itimetrigger)
-   [<span data-ttu-id="e00e6-143">**IWeeklyTrigger**</span><span class="sxs-lookup"><span data-stu-id="e00e6-143">**IWeeklyTrigger**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-iweeklytrigger)

## <a name="task-scheduler-10-trigger-interfaces"></a><span data-ttu-id="e00e6-144">Agendador de Tarefas interfaces de gatilho 1,0</span><span class="sxs-lookup"><span data-stu-id="e00e6-144">Task Scheduler 1.0 Trigger Interfaces</span></span>

<span data-ttu-id="e00e6-145">Os aplicativos existentes que são desenvolvidos usando Agendador de Tarefas 1,0 podem usar os métodos que estão disponíveis nas interfaces Agendador de Tarefas 1,0 para criar, recuperar, modificar e excluir os gatilhos de um [*item de trabalho*](w.md).</span><span class="sxs-lookup"><span data-stu-id="e00e6-145">Existing applications that are developed using Task Scheduler 1.0 can use the methods that are available from the Task Scheduler 1.0 interfaces to create, retrieve, modify, and delete the triggers for a [*work item*](w.md).</span></span> <span data-ttu-id="e00e6-146">No entanto, observe que todas as interfaces, enumerações e estruturas do Agendador de Tarefas 1,0 são obsoletas e não devem ser usadas para o desenvolvimento de novos aplicativos.</span><span class="sxs-lookup"><span data-stu-id="e00e6-146">However, note that all Task Scheduler 1.0 interfaces, enumerations, and structures are obsolete and should not be used for the development of new applications.</span></span>

<span data-ttu-id="e00e6-147">As duas interfaces que são usadas para fazer isso são mostradas na ilustração a seguir.</span><span class="sxs-lookup"><span data-stu-id="e00e6-147">The two interfaces that are used to do this are shown in the following illustration.</span></span> <span data-ttu-id="e00e6-148">A interface [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) é usada para gerenciar todos os gatilhos associados a um item de trabalho (esse gerenciamento inclui a criação de um novo disparador para o item de trabalho).</span><span class="sxs-lookup"><span data-stu-id="e00e6-148">The [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) interface is used to manage all the triggers that are associated with a work item (such management includes creating a new trigger for the work item).</span></span> <span data-ttu-id="e00e6-149">A interface [**ITaskTrigger**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger) é usada para gerenciar um gatilho específico.</span><span class="sxs-lookup"><span data-stu-id="e00e6-149">The [**ITaskTrigger**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger) interface is used to manage a specific trigger.</span></span>

![interfaces de gatilho do Agendador de tarefas 1,0](images/tsktri2.png)

<span data-ttu-id="e00e6-151">A interface [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) fornece métodos para criar um novo gatilho para um item de trabalho, recuperando o número de gatilhos associados a um item de trabalho, recuperando as [*estruturas de gatilho*](t.md) associadas ao item de trabalho, recuperando [*cadeias de caracteres de gatilho*](t.md) associadas ao item de trabalho e para excluir gatilhos.</span><span class="sxs-lookup"><span data-stu-id="e00e6-151">The [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) interface provides methods for creating a new trigger for a work item, retrieving the number of triggers that are associated with a work item, retrieving the [*trigger structures*](t.md) that are associated with the work item, retrieving [*trigger strings*](t.md) that are associated with the work item, and for deleting triggers.</span></span>

<span data-ttu-id="e00e6-152">Depois que o objeto de gatilho estiver disponível, você poderá usar a interface [**ITaskTrigger**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger) para recuperar a estrutura do gatilho e a cadeia de caracteres do gatilho e definir os critérios usados para acionar o gatilho.</span><span class="sxs-lookup"><span data-stu-id="e00e6-152">Once the trigger object is available, you can use the [**ITaskTrigger**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger) interface to retrieve the trigger structure and the string of the trigger and to set the criteria that is used to fire the trigger.</span></span> <span data-ttu-id="e00e6-153">Essa interface é usada somente quando você está trabalhando com um [*objeto de gatilho de tarefa*](t.md).</span><span class="sxs-lookup"><span data-stu-id="e00e6-153">This interface is used only when you are working with a [*task trigger object*](t.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e00e6-154">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e00e6-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e00e6-155">Gatilhos de tarefa</span><span class="sxs-lookup"><span data-stu-id="e00e6-155">Task Triggers</span></span>](task-triggers.md)
</dt> <dt>

[<span data-ttu-id="e00e6-156">Tipos de gatilho</span><span class="sxs-lookup"><span data-stu-id="e00e6-156">Trigger Types</span></span>](trigger-types.md)
</dt> <dt>

[<span data-ttu-id="e00e6-157">Estruturas de gatilho</span><span class="sxs-lookup"><span data-stu-id="e00e6-157">Trigger Structures</span></span>](trigger-structures.md)
</dt> </dl>

 

 