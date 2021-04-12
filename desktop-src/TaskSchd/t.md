---
title: T (Agendador de Tarefas)
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: d4c6d7ba-7bca-420d-a4dc-4daea816f99c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2730cdbe3a13456aed0e613a614d43a0e56e6673
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104499209"
---
# <a name="t-task-scheduler"></a><span data-ttu-id="83eaf-103">T (Agendador de Tarefas)</span><span class="sxs-lookup"><span data-stu-id="83eaf-103">T (Task Scheduler)</span></span>

<span data-ttu-id="83eaf-104">A B C D [E](e.md) F G H [i](i.md) J K L M N O [P](p.md) Q R [S](s.md) T U V [W](w.md) X Y Z</span><span class="sxs-lookup"><span data-stu-id="83eaf-104">A B C D [E](e.md) F G H [I](i.md) J K L M N O [P](p.md) Q R [S](s.md) T U V [W](w.md) X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="83eaf-105"><span id="_msb_task_objects_gly"></span><span id="_MSB_TASK_OBJECTS_GLY"></span>**objetos de tarefa**</span><span class="sxs-lookup"><span data-stu-id="83eaf-105"><span id="_msb_task_objects_gly"></span><span id="_MSB_TASK_OBJECTS_GLY"></span>**task objects**</span></span>
</dt> <dd>

<span data-ttu-id="83eaf-106">Instâncias de um objeto que fornece métodos para gerenciar tarefas.</span><span class="sxs-lookup"><span data-stu-id="83eaf-106">Instances of an object that provides methods for managing tasks.</span></span> <span data-ttu-id="83eaf-107">Isso inclui métodos para configuração e recuperação de propriedades; executando, encerrando e excluindo tarefas; e criando novos gatilhos e recuperando gatilhos antigos.</span><span class="sxs-lookup"><span data-stu-id="83eaf-107">This includes methods for setting and retrieving properties; running, terminating, and deleting tasks; and creating new triggers and retrieving old triggers.</span></span>

<span data-ttu-id="83eaf-108">O objeto Task é criado por chamadas para [**IScheduledWorkItem:: CreateTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-createtrigger) e [**IScheduledWorkItem:: gettrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-gettrigger).</span><span class="sxs-lookup"><span data-stu-id="83eaf-108">The task object is created by calls to [**IScheduledWorkItem::CreateTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-createtrigger) and [**IScheduledWorkItem::GetTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-gettrigger).</span></span>

</dd> <dt>

<span data-ttu-id="83eaf-109"><span id="_msb_task_scheduler_objects_gly"></span><span id="_MSB_TASK_SCHEDULER_OBJECTS_GLY"></span>**objetos do Agendador de tarefas**</span><span class="sxs-lookup"><span data-stu-id="83eaf-109"><span id="_msb_task_scheduler_objects_gly"></span><span id="_MSB_TASK_SCHEDULER_OBJECTS_GLY"></span>**task scheduler objects**</span></span>
</dt> <dd>

<span data-ttu-id="83eaf-110">Instâncias de um objeto o representa o serviço Agendador de Tarefas.</span><span class="sxs-lookup"><span data-stu-id="83eaf-110">Instances of an object the represents the Task Scheduler service.</span></span> <span data-ttu-id="83eaf-111">Este objeto dá suporte a duas interfaces: **IUnknown** e [**ITaskScheduler**](/windows/desktop/api/Mstask/nn-mstask-itaskscheduler) (atualmente, as tarefas são o único tipo de itens de trabalho com suporte no serviço Agendador de tarefas).</span><span class="sxs-lookup"><span data-stu-id="83eaf-111">This object supports two interfaces: **IUnknown** and [**ITaskScheduler**](/windows/desktop/api/Mstask/nn-mstask-itaskscheduler) (currently tasks are the only type of work items supported by the Task Scheduler service).</span></span>

<span data-ttu-id="83eaf-112">Os objetos do Agendador de tarefas são criados por chamadas para **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="83eaf-112">Task scheduler objects are created by calls to **CoCreateInstance**.</span></span>

</dd> <dt>

<span data-ttu-id="83eaf-113"><span id="_msb_task_trigger_objects_gly"></span><span id="_MSB_TASK_TRIGGER_OBJECTS_GLY"></span>**objetos de gatilho de tarefa**</span><span class="sxs-lookup"><span data-stu-id="83eaf-113"><span id="_msb_task_trigger_objects_gly"></span><span id="_MSB_TASK_TRIGGER_OBJECTS_GLY"></span>**task trigger objects**</span></span>
</dt> <dd>

<span data-ttu-id="83eaf-114">Instâncias de um objeto o fornece métodos para configurar e recuperar gatilhos de tarefa.</span><span class="sxs-lookup"><span data-stu-id="83eaf-114">Instances of an object the provides methods for setting and retrieving task triggers.</span></span> <span data-ttu-id="83eaf-115">Este objeto dá suporte a duas interfaces: **IUnknown** e [**ITaskTrigger**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger).</span><span class="sxs-lookup"><span data-stu-id="83eaf-115">This object supports two interfaces: **IUnknown** and [**ITaskTrigger**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger).</span></span>

<span data-ttu-id="83eaf-116">Os objetos de gatilho de tarefa são criados por chamadas para [**IScheduledWorkItem:: CreateTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-createtrigger) e [**IScheduledWorkItem:: gettrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-gettrigger).</span><span class="sxs-lookup"><span data-stu-id="83eaf-116">Task trigger objects are created by calls to [**IScheduledWorkItem::CreateTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-createtrigger) and [**IScheduledWorkItem::GetTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-gettrigger).</span></span>

<span data-ttu-id="83eaf-117">Consulte também: *gatilhos*.</span><span class="sxs-lookup"><span data-stu-id="83eaf-117">See also: *triggers*.</span></span>

</dd> <dt>

<span data-ttu-id="83eaf-118"><span id="_msb_tasks_gly"></span><span id="_MSB_TASKS_GLY"></span>**tarefa**</span><span class="sxs-lookup"><span data-stu-id="83eaf-118"><span id="_msb_tasks_gly"></span><span id="_MSB_TASKS_GLY"></span>**tasks**</span></span>
</dt> <dd>

<span data-ttu-id="83eaf-119">Qualquer item que o Agendador de Tarefas possa executar.</span><span class="sxs-lookup"><span data-stu-id="83eaf-119">Any item that the Task Scheduler can execute.</span></span> <span data-ttu-id="83eaf-120">Esses itens podem incluir qualquer um dos seguintes (conforme suportado pelo sistema operacional no qual a tarefa será executada): aplicativos de® Win32, aplicativos Win16, aplicativos do sistema operacional/2, aplicativos do MS-DOS®, arquivos em lotes ( \* . bat), arquivos de comando ( \* . cmd) ou qualquer tipo de arquivo registrado corretamente.</span><span class="sxs-lookup"><span data-stu-id="83eaf-120">These items may include any of the following (as supported by the operating system on which the task will execute): Win32® applications, Win16 applications, OS/2 applications, MS-DOS® applications, batch files (\*.bat), command files (\*.cmd), or any properly registered file type.</span></span>

</dd> <dt>

<span data-ttu-id="83eaf-121"><span id="_msb_tasks_folder_gly"></span><span id="_MSB_TASKS_FOLDER_GLY"></span>**Pasta tarefas**</span><span class="sxs-lookup"><span data-stu-id="83eaf-121"><span id="_msb_tasks_folder_gly"></span><span id="_MSB_TASKS_FOLDER_GLY"></span>**Tasks folder**</span></span>
</dt> <dd>

<span data-ttu-id="83eaf-122">A pasta que lista todos os arquivos de tarefas (atualmente, tarefas são os únicos itens de trabalho disponíveis).</span><span class="sxs-lookup"><span data-stu-id="83eaf-122">The folder that lists all task files (currently, tasks are the only work items available).</span></span> <span data-ttu-id="83eaf-123">Esses arquivos contêm as informações sobre a tarefa.</span><span class="sxs-lookup"><span data-stu-id="83eaf-123">These files contain the information about the task.</span></span> <span data-ttu-id="83eaf-124">O nome desses arquivos reflete o nome da tarefa.</span><span class="sxs-lookup"><span data-stu-id="83eaf-124">The name of these files reflects the name of the task.</span></span>

<span data-ttu-id="83eaf-125">Você pode recuperar o local da pasta tarefas do registro obtendo dados para o seguinte valor:</span><span class="sxs-lookup"><span data-stu-id="83eaf-125">You can retrieve the location of the Tasks folder from the registry by getting data for the following value:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         SchedulingAgent
            TasksFolder
```

</dd> <dt>

<span data-ttu-id="83eaf-126"><span id="_msb_triggers_gly"></span><span id="_MSB_TRIGGERS_GLY"></span>**gatilhos**</span><span class="sxs-lookup"><span data-stu-id="83eaf-126"><span id="_msb_triggers_gly"></span><span id="_MSB_TRIGGERS_GLY"></span>**triggers**</span></span>
</dt> <dd>

<span data-ttu-id="83eaf-127">Um conjunto de critérios que, quando atendidos, fará com que uma tarefa seja executada.</span><span class="sxs-lookup"><span data-stu-id="83eaf-127">A set of criteria that, when met, will cause a task to be executed.</span></span> <span data-ttu-id="83eaf-128">O Agendador de Tarefas fornece gatilhos baseados em tempo e eventos que podem especificar horários de início da tarefa, critérios de repetição e outros parâmetros.</span><span class="sxs-lookup"><span data-stu-id="83eaf-128">Task Scheduler provides time-based and event-based triggers that can specify task start times, repetition criteria, and other parameters.</span></span>

</dd> <dt>

<span data-ttu-id="83eaf-129"><span id="_msb_trigger_strings_gly"></span><span id="_MSB_TRIGGER_STRINGS_GLY"></span>**cadeias de caracteres de gatilho**</span><span class="sxs-lookup"><span data-stu-id="83eaf-129"><span id="_msb_trigger_strings_gly"></span><span id="_MSB_TRIGGER_STRINGS_GLY"></span>**trigger strings**</span></span>
</dt> <dd>

<span data-ttu-id="83eaf-130">Uma cadeia de caracteres que descreve o gatilho.</span><span class="sxs-lookup"><span data-stu-id="83eaf-130">A string that describes the trigger.</span></span> <span data-ttu-id="83eaf-131">Essa cadeia de caracteres é criada pelo serviço de Agendador de Tarefas e aparece na interface do usuário do Agendador de Tarefas em um formato semelhante a "at 14h todos os dias, começando em 5/11/97".</span><span class="sxs-lookup"><span data-stu-id="83eaf-131">This string is created by the Task Scheduler service, and appears in the Task Scheduler user interface in a form similar to "At 2PM every day, starting 5/11/97."</span></span>

</dd> <dt>

<span data-ttu-id="83eaf-132"><span id="_msb_trigger_structures_gly"></span><span id="_MSB_TRIGGER_STRUCTURES_GLY"></span>**estruturas de gatilho**</span><span class="sxs-lookup"><span data-stu-id="83eaf-132"><span id="_msb_trigger_structures_gly"></span><span id="_MSB_TRIGGER_STRUCTURES_GLY"></span>**trigger structures**</span></span>
</dt> <dd>

<span data-ttu-id="83eaf-133">A estrutura do [**\_ gatilho de tarefa**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) usada ao configurar ou recuperar os critérios que definem o gatilho.</span><span class="sxs-lookup"><span data-stu-id="83eaf-133">The [**TASK\_TRIGGER**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) structure used when setting or retrieving the criteria that defines the trigger.</span></span> <span data-ttu-id="83eaf-134">Os critérios incluem quando o gatilho será acionado e o tipo do gatilho.</span><span class="sxs-lookup"><span data-stu-id="83eaf-134">The criteria includes when the trigger will fire, and the type of the trigger.</span></span>

</dd> </dl>

 

 




