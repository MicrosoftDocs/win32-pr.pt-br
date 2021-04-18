---
title: Tarefas
description: Uma tarefa é o trabalho agendado que o serviço Agendador de Tarefas executa.
ms.assetid: 24c43834-5731-4b14-9409-7d7cf20b1a71
keywords:
- tarefas Agendador de Tarefas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efbb4ef41915ec70c98b59c9a7ba74c00f283ce6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105810116"
---
# <a name="tasks"></a><span data-ttu-id="be89c-104">Tarefas</span><span class="sxs-lookup"><span data-stu-id="be89c-104">Tasks</span></span>

<span data-ttu-id="be89c-105">Uma tarefa é o trabalho agendado que o serviço Agendador de Tarefas executa.</span><span class="sxs-lookup"><span data-stu-id="be89c-105">A task is the scheduled work that the Task Scheduler service performs.</span></span> <span data-ttu-id="be89c-106">Uma tarefa é composta por diferentes componentes, mas uma tarefa deve conter um gatilho que o Agendador de Tarefas usa para iniciar a tarefa e uma ação que descreve o trabalho que o Agendador de Tarefas executará.</span><span class="sxs-lookup"><span data-stu-id="be89c-106">A task is composed of different components, but a task must contain a trigger that the Task Scheduler uses to start the task and an action that describes what work the Task Scheduler will perform.</span></span>

<span data-ttu-id="be89c-107">Quando uma tarefa é criada, ela é armazenada em uma pasta de tarefas.</span><span class="sxs-lookup"><span data-stu-id="be89c-107">When a task is created, it is stored in a task folder.</span></span> <span data-ttu-id="be89c-108">As pastas de tarefas podem ser acessadas por meio da interface [**ITaskFolder**](/windows/desktop/api/taskschd/nn-taskschd-itaskfolder) ([**TaskFolder**](taskfolder.md) para scripts), e as tarefas podem ser acessadas por meio da interface [**IRegisteredTask**](/windows/desktop/api/taskschd/nn-taskschd-iregisteredtask) ([**RegisteredTask**](registeredtask.md) para scripts) quando elas são criadas.</span><span class="sxs-lookup"><span data-stu-id="be89c-108">Task folders can be accessed through the [**ITaskFolder**](/windows/desktop/api/taskschd/nn-taskschd-itaskfolder) interface ([**TaskFolder**](taskfolder.md) for scripting), and tasks can be accessed through the [**IRegisteredTask**](/windows/desktop/api/taskschd/nn-taskschd-iregisteredtask) interface ([**RegisteredTask**](registeredtask.md) for scripting) when they are created.</span></span> <span data-ttu-id="be89c-109">Você pode alterar as listas de controle de acesso (ACLs) para tarefas e pastas de tarefas a fim de conceder ou negar a determinados usuários e grupos o acesso a uma tarefa ou pasta de tarefas.</span><span class="sxs-lookup"><span data-stu-id="be89c-109">You can change access control lists (ACLs) for tasks and task folders in order to grant or deny certain users and groups access to a task or task folder.</span></span> <span data-ttu-id="be89c-110">Isso pode ser feito usando o método [**IRegisteredTask:: SetSecurityDescriptor**](/windows/desktop/api/taskschd/nf-taskschd-iregisteredtask-setsecuritydescriptor) , o método [**ITaskFolder:: SetSecurityDescriptor**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-setsecuritydescriptor) ou especificando um descritor de segurança quando uma tarefa é registrada usando o método [**RegisterTaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition) ou [**RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) .</span><span class="sxs-lookup"><span data-stu-id="be89c-110">This can be done by using the [**IRegisteredTask::SetSecurityDescriptor**](/windows/desktop/api/taskschd/nf-taskschd-iregisteredtask-setsecuritydescriptor) method, the [**ITaskFolder::SetSecurityDescriptor**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-setsecuritydescriptor) method, or by specifying a security descriptor when a task is registered by using the [**RegisterTaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition) or [**RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) method.</span></span>

> [!Note]  
> <span data-ttu-id="be89c-111">Se a conta do sistema local tiver acesso negado a um arquivo de tarefa ou pasta de tarefas, o serviço de Agendador de Tarefas poderá produzir resultados inesperados.</span><span class="sxs-lookup"><span data-stu-id="be89c-111">If the Local System account is denied access to a task file or task folder, then the Task Scheduler service can produce unexpected results.</span></span>

 

## <a name="components-of-a-task"></a><span data-ttu-id="be89c-112">Componentes de uma tarefa</span><span class="sxs-lookup"><span data-stu-id="be89c-112">Components of a Task</span></span>

<span data-ttu-id="be89c-113">A ilustração a seguir mostra os componentes da tarefa.</span><span class="sxs-lookup"><span data-stu-id="be89c-113">The following illustration shows the task components.</span></span>

![componentes da tarefa](images/taskcomponents.png)

<span data-ttu-id="be89c-115">A lista a seguir contém uma breve descrição de cada componente de tarefa:</span><span class="sxs-lookup"><span data-stu-id="be89c-115">The following list contains a brief description of each task component:</span></span>

-   <span data-ttu-id="be89c-116">Gatilhos: Agendador de Tarefas usa gatilhos de evento ou baseados em tempo para saber quando iniciar uma tarefa.</span><span class="sxs-lookup"><span data-stu-id="be89c-116">Triggers: Task Scheduler uses event or time-based triggers to know when to start a task.</span></span> <span data-ttu-id="be89c-117">Cada tarefa pode especificar um ou mais gatilhos para iniciar a tarefa.</span><span class="sxs-lookup"><span data-stu-id="be89c-117">Every task can specify one or more triggers to start the task.</span></span>

    <span data-ttu-id="be89c-118">Para obter mais informações sobre gatilhos, consulte [disparadores de tarefas](task-triggers.md).</span><span class="sxs-lookup"><span data-stu-id="be89c-118">For more information about triggers, see [Task Triggers](task-triggers.md).</span></span>

-   <span data-ttu-id="be89c-119">Ações: essas são as ações, o trabalho real, que é executado pela tarefa.</span><span class="sxs-lookup"><span data-stu-id="be89c-119">Actions: These are the actions, the actual work, that is performed by the task.</span></span> <span data-ttu-id="be89c-120">Cada tarefa pode especificar uma ou mais ações para concluir seu trabalho.</span><span class="sxs-lookup"><span data-stu-id="be89c-120">Every task can specify one or more actions to complete its work.</span></span>

    <span data-ttu-id="be89c-121">Para obter mais informações sobre ações, consulte [ações de tarefas](task-actions.md).</span><span class="sxs-lookup"><span data-stu-id="be89c-121">For more information about actions, see [Task Actions](task-actions.md).</span></span>

-   <span data-ttu-id="be89c-122">Entidades: as entidades definem o contexto de segurança no qual a tarefa é executada.</span><span class="sxs-lookup"><span data-stu-id="be89c-122">Principals: Principals define the security context in which the task is run.</span></span> <span data-ttu-id="be89c-123">Por exemplo, uma entidade de segurança pode definir um usuário ou grupo de usuários específico que possa executar a tarefa.</span><span class="sxs-lookup"><span data-stu-id="be89c-123">For example, a principal might define a specific user or user group that can run the task.</span></span>

    <span data-ttu-id="be89c-124">Para obter mais informações sobre entidades, consulte [contextos de segurança para tarefas](security-contexts-for-running-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="be89c-124">For more information about principals, see [Security Contexts for Tasks](security-contexts-for-running-tasks.md).</span></span>

-   <span data-ttu-id="be89c-125">Configurações: essas são as configurações que o Agendador de Tarefas usa para executar a tarefa em relação às condições que são externas à própria tarefa.</span><span class="sxs-lookup"><span data-stu-id="be89c-125">Settings: These are the settings that the Task Scheduler uses to run the task with respect to conditions that are external to the task itself.</span></span> <span data-ttu-id="be89c-126">Por exemplo, essas configurações podem especificar a prioridade da tarefa em relação a outras tarefas, se várias instâncias da tarefa podem ser executadas, como a tarefa é tratada quando o computador está em uma condição ociosa e outras condições.</span><span class="sxs-lookup"><span data-stu-id="be89c-126">For example, these settings can specify the priority of the task with respect to other tasks, whether multiple instances of the task can be run, how the task is handled when the computer is in an idle condition, and other conditions.</span></span>

    <span data-ttu-id="be89c-127">Para obter mais informações sobre configurações de tarefas, consulte [**ITaskSettings**](/windows/desktop/api/taskschd/nn-taskschd-itasksettings) ([**TaskSettings**](tasksettings.md) for Scripting).</span><span class="sxs-lookup"><span data-stu-id="be89c-127">For more information about task settings, see [**ITaskSettings**](/windows/desktop/api/taskschd/nn-taskschd-itasksettings) ([**TaskSettings**](tasksettings.md) for scripting).</span></span>

    > [!Note]  
    > <span data-ttu-id="be89c-128">Por padrão, uma tarefa será interrompida em 72 horas depois de começar a ser executada.</span><span class="sxs-lookup"><span data-stu-id="be89c-128">By default, a task will be stopped 72 hours after it starts to run.</span></span> <span data-ttu-id="be89c-129">Você pode alterar isso alterando a configuração [**ExecutionTimeLimit**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_executiontimelimit) .</span><span class="sxs-lookup"><span data-stu-id="be89c-129">You can change this by changing the [**ExecutionTimeLimit**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_executiontimelimit) setting.</span></span>

     

-   <span data-ttu-id="be89c-130">Informações de registro: são informações administrativas que são coletadas quando a tarefa é registrada.</span><span class="sxs-lookup"><span data-stu-id="be89c-130">Registration Information: This is administrative information that is gathered when the task is registered.</span></span> <span data-ttu-id="be89c-131">Por exemplo, essas informações descrevem o autor da tarefa, a data em que a tarefa foi registrada, uma descrição XML da tarefa e outras informações.</span><span class="sxs-lookup"><span data-stu-id="be89c-131">For example, this information describes the author of the task, the date when the task was registered, an XML description of the task, and other information.</span></span>

    <span data-ttu-id="be89c-132">Para obter mais informações sobre informações de registro de tarefas, consulte [informações de registro da tarefa](task-registration-information.md).</span><span class="sxs-lookup"><span data-stu-id="be89c-132">For more information about task registration information, see [Task Registration Information](task-registration-information.md).</span></span>

-   <span data-ttu-id="be89c-133">Dados: essa é uma documentação adicional sobre a tarefa fornecida pelo autor da tarefa.</span><span class="sxs-lookup"><span data-stu-id="be89c-133">Data: This is additional documentation about the task that is supplied by the author of the task.</span></span> <span data-ttu-id="be89c-134">Por exemplo, esses dados podem conter ajuda XML que pode ser usada pelos usuários quando eles executam a tarefa.</span><span class="sxs-lookup"><span data-stu-id="be89c-134">For example, this data may contain XML Help that can be used by users when they run the task.</span></span>

## <a name="task-apis"></a><span data-ttu-id="be89c-135">APIs de tarefa</span><span class="sxs-lookup"><span data-stu-id="be89c-135">Task APIs</span></span>

<span data-ttu-id="be89c-136">O Agendador de Tarefas 2,0 fornece dois conjuntos de APIs: um conjunto de interfaces e objetos de script para Agendador de Tarefas 2,0.</span><span class="sxs-lookup"><span data-stu-id="be89c-136">Task Scheduler 2.0 provides two sets of APIs: a set of scripting objects and interfaces for Task Scheduler 2.0.</span></span> <span data-ttu-id="be89c-137">Para obter mais informações, consulte [referência de Agendador de tarefas](task-scheduler-reference.md).</span><span class="sxs-lookup"><span data-stu-id="be89c-137">For more information, see [Task Scheduler Reference](task-scheduler-reference.md).</span></span>

<span data-ttu-id="be89c-138">A compatibilidade de tarefas, que é definida por meio da propriedade de [**compatibilidade**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_compatibility) , só deve ser definida como compatibilidade de tarefas \_ \_ v1 se uma tarefa precisar ser acessada ou modificada de um computador com Windows XP, Windows Server 2003 ou Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="be89c-138">Task compatibility, which is set through the [**Compatibility**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_compatibility) property, should only be set to TASK\_COMPATIBILITY\_V1 if a task must be accessed or modified from a Windows XP, Windows Server 2003, or Windows 2000 computer.</span></span> <span data-ttu-id="be89c-139">Caso contrário, é recomendável que você use a Agendador de Tarefas a compatibilidade 2,0 porque ela tem mais recursos.</span><span class="sxs-lookup"><span data-stu-id="be89c-139">Otherwise, it is recommended that you use Task Scheduler 2.0 compatibility because it has more features.</span></span>

<span data-ttu-id="be89c-140">A partir do Agendador de Tarefas 2,0, a interface [**o ITaskService**](/windows/desktop/api/taskschd/nn-taskschd-itaskservice) ([**TaskService**](taskservice.md) para scripts) é usada como um ponto de partida para criar tarefas em pastas especificadas.</span><span class="sxs-lookup"><span data-stu-id="be89c-140">Starting with Task Scheduler 2.0, the [**ITaskService**](/windows/desktop/api/taskschd/nn-taskschd-itaskservice) interface ([**TaskService**](taskservice.md) for scripting) is used as a starting point to create tasks in specified folders.</span></span> <span data-ttu-id="be89c-141">A interface [**ITaskDefinition**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition) ([**TaskDefinition**](taskdefinition.md) para scripts) é usada para manter todos os componentes de uma tarefa, como as configurações, as ações e os gatilhos.</span><span class="sxs-lookup"><span data-stu-id="be89c-141">The [**ITaskDefinition**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition) interface ([**TaskDefinition**](taskdefinition.md) for scripting) is used to hold all the components of a task, such as the settings, actions, and triggers.</span></span> <span data-ttu-id="be89c-142">As APIs [**ITaskTrigger**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger), [**IAction**](/windows/desktop/api/taskschd/nn-taskschd-iaction)e [**ITaskSettings**](/windows/desktop/api/taskschd/nn-taskschd-itasksettings) fornecem propriedades que são usadas para definir os outros componentes da tarefa.</span><span class="sxs-lookup"><span data-stu-id="be89c-142">The [**ITaskTrigger**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger), [**IAction**](/windows/desktop/api/taskschd/nn-taskschd-iaction), and [**ITaskSettings**](/windows/desktop/api/taskschd/nn-taskschd-itasksettings) APIs provide properties that are then used to define the other components of the task.</span></span> <span data-ttu-id="be89c-143">Agendador de Tarefas 1,0 fornece a interface [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) , que tem suporte apenas para compatibilidade com versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="be89c-143">Task Scheduler 1.0 provides the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface, which is supported only for backward compatibility.</span></span>

<span data-ttu-id="be89c-144">Para scripts, as interfaces de Agendador de Tarefas são mapeadas para objetos de script que têm nomes, propriedades e métodos semelhantes.</span><span class="sxs-lookup"><span data-stu-id="be89c-144">For scripting, the Task Scheduler interfaces map to scripting objects that have the similar names, properties, and methods.</span></span> <span data-ttu-id="be89c-145">Por exemplo, o objeto de script [**TaskService**](taskservice.md) tem as mesmas propriedades e métodos que a interface [**o ITaskService**](/windows/desktop/api/taskschd/nn-taskschd-itaskservice) .</span><span class="sxs-lookup"><span data-stu-id="be89c-145">For example, the [**TaskService**](taskservice.md) scripting object has the same properties and methods as the [**ITaskService**](/windows/desktop/api/taskschd/nn-taskschd-itaskservice) interface.</span></span>

<span data-ttu-id="be89c-146">Para obter mais informações e exemplos sobre como usar as interfaces de Agendador de Tarefas, os objetos de script e o XML, consulte [usando o Agendador de tarefas](using-the-task-scheduler.md).</span><span class="sxs-lookup"><span data-stu-id="be89c-146">For more information and examples about how to use the Task Scheduler interfaces, scripting objects, and XML, see [Using the Task Scheduler](using-the-task-scheduler.md).</span></span>

### <a name="task-scheduler-10-tasks"></a><span data-ttu-id="be89c-147">Agendador de Tarefas tarefas 1,0</span><span class="sxs-lookup"><span data-stu-id="be89c-147">Task Scheduler 1.0 Tasks</span></span>

<span data-ttu-id="be89c-148">Uma tarefa Agendador de Tarefas 1,0 é qualquer tipo de aplicativo ou de arquivo que o Agendador de Tarefas possa executar.</span><span class="sxs-lookup"><span data-stu-id="be89c-148">A Task Scheduler 1.0 task is any application or file type that the Task Scheduler can execute.</span></span> <span data-ttu-id="be89c-149">Eles podem incluir qualquer um dos seguintes (conforme suportado pelo sistema operacional no qual a tarefa será executada): aplicativos Win32, aplicativos Win16, aplicativos do sistema operacional/2, aplicativos do MS-DOS, arquivos em lotes ( \* . bat), arquivos de comando ( \* . cmd) ou qualquer tipo de arquivo registrado corretamente.</span><span class="sxs-lookup"><span data-stu-id="be89c-149">These may include any of the following (as supported by the operating system on which the task will execute): Win32 applications, Win16 applications, OS/2 applications, MS-DOS applications, batch files (\*.bat), command files (\*.cmd), or any properly registered file type.</span></span>

<span data-ttu-id="be89c-150">Os dados que descrevem uma tarefa são mantidos em um arquivo de tarefa armazenado na pasta tarefas agendadas.</span><span class="sxs-lookup"><span data-stu-id="be89c-150">Data that describes a task is kept in a task file that is stored in the Scheduled Tasks folder.</span></span> <span data-ttu-id="be89c-151">Para obter mais informações, consulte [*pasta tarefas agendadas*](s.md).</span><span class="sxs-lookup"><span data-stu-id="be89c-151">For more information, see [*Scheduled Tasks folder*](s.md).</span></span> <span data-ttu-id="be89c-152">O nome desses arquivos de tarefas inclui o nome da tarefa, seguido por uma extensão de nome de arquivo. Job.</span><span class="sxs-lookup"><span data-stu-id="be89c-152">The name of these task files include the name of the task, followed by a .job file name extension.</span></span>

<span data-ttu-id="be89c-153">Para obter mais informações sobre como adicionar Agendador de Tarefas tarefas 1,0, consulte [adicionando itens de trabalho](adding-work-items.md).</span><span class="sxs-lookup"><span data-stu-id="be89c-153">For more information about adding Task Scheduler 1.0 tasks, see [Adding Work Items](adding-work-items.md).</span></span>

<span data-ttu-id="be89c-154">Para obter mais informações sobre como enumerar por meio de tarefas Agendador de Tarefas 1,0, consulte [enumerando tarefas](enumerating-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="be89c-154">For more information about enumerating through Task Scheduler 1.0 tasks, see [Enumerating Tasks](enumerating-tasks.md).</span></span>

<span data-ttu-id="be89c-155">Para um computador com Windows Server 2003, Windows XP ou Windows 2000 para criar, monitorar ou controlar tarefas em um computador com Windows Vista, as seguintes operações devem ser concluídas no computador com Windows Vista e o usuário que está chamando o método [**ITaskScheduler:: SetTargetComputer**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-settargetcomputer) deve ser membro do grupo Administradores no computador remoto do Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="be89c-155">For a Windows Server 2003, Windows XP, or Windows 2000 computer to create, monitor, or control tasks on a Windows Vista computer, the following operations should be completed on the Windows Vista computer, and the user who is calling the [**ITaskScheduler::SetTargetComputer**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-settargetcomputer) method must be a member of the Administrators group on the remote Windows Vista computer.</span></span>

<span data-ttu-id="be89c-156">**Para habilitar a exceção "compartilhar arquivos e impressoras" no firewall do Windows**</span><span class="sxs-lookup"><span data-stu-id="be89c-156">**To enable the "Share File and Printers" exception in Windows Firewall**</span></span>

1.  <span data-ttu-id="be89c-157">Clique em **Iniciar** e em **Painel de Controle**.</span><span class="sxs-lookup"><span data-stu-id="be89c-157">Click **Start**, and then click **Control Panel**.</span></span>
2.  <span data-ttu-id="be89c-158">No **painel de controle**, clique em **exibição clássica** e clique duas vezes no ícone **Firewall do Windows** .</span><span class="sxs-lookup"><span data-stu-id="be89c-158">In **Control Panel**, click **Classic View** and then double-click the **Windows Firewall** icon.</span></span>
3.  <span data-ttu-id="be89c-159">Na janela **Firewall do Windows** , clique na guia **exceções** e selecione caixa de seleção de **exceção de compartilhamento de arquivos e impressoras** .</span><span class="sxs-lookup"><span data-stu-id="be89c-159">In the **Windows Firewall** window, click the **Exceptions** tab and select **File and Printer Sharing exception** check box.</span></span>

<span data-ttu-id="be89c-160">**Para habilitar o serviço "registro remoto"**</span><span class="sxs-lookup"><span data-stu-id="be89c-160">**To enable the "Remote Registry" service**</span></span>

-   <span data-ttu-id="be89c-161">Abra uma janela de prompt de comando e digite o seguinte comando: **net start "registro remoto"**.</span><span class="sxs-lookup"><span data-stu-id="be89c-161">Open a Command Prompt window and enter the following command: **net start "Remote Registry"**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="be89c-162">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="be89c-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="be89c-163">Sobre o Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="be89c-163">About the Task Scheduler</span></span>](about-the-task-scheduler.md)
</dt> <dt>

[<span data-ttu-id="be89c-164">Gatilhos de tarefa</span><span class="sxs-lookup"><span data-stu-id="be89c-164">Task Triggers</span></span>](task-triggers.md)
</dt> <dt>

[<span data-ttu-id="be89c-165">Ações de tarefas</span><span class="sxs-lookup"><span data-stu-id="be89c-165">Task Actions</span></span>](task-actions.md)
</dt> <dt>

[<span data-ttu-id="be89c-166">**ITaskDefinition**</span><span class="sxs-lookup"><span data-stu-id="be89c-166">**ITaskDefinition**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition)
</dt> <dt>

[<span data-ttu-id="be89c-167">**TaskDefinition**</span><span class="sxs-lookup"><span data-stu-id="be89c-167">**TaskDefinition**</span></span>](taskdefinition.md)
</dt> <dt>

[<span data-ttu-id="be89c-168">**O ITaskService**</span><span class="sxs-lookup"><span data-stu-id="be89c-168">**ITaskService**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-itaskservice)
</dt> <dt>

[<span data-ttu-id="be89c-169">**TaskService**</span><span class="sxs-lookup"><span data-stu-id="be89c-169">**TaskService**</span></span>](taskservice.md)
</dt> </dl>

 

 




