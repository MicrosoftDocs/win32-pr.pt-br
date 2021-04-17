---
title: Exemplo de gatilho de registro (XML)
description: O XML neste exemplo define uma tarefa que inicia o bloco de notas quando a tarefa é registrada.
ms.assetid: 976b9767-635f-42a6-84f5-7e0203478594
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 09b9193f3b63f21464811609e8f5f19017539ecd
ms.sourcegitcommit: 40dd8501397fc79a643deb528c6c57ac2e9726ce
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/24/2020
ms.locfileid: "105813042"
---
# <a name="registration-trigger-example-xml"></a><span data-ttu-id="fbf9a-103">Exemplo de gatilho de registro (XML)</span><span class="sxs-lookup"><span data-stu-id="fbf9a-103">Registration Trigger Example (XML)</span></span>

<span data-ttu-id="fbf9a-104">O XML neste exemplo define uma tarefa que inicia o bloco de notas quando a tarefa é registrada.</span><span class="sxs-lookup"><span data-stu-id="fbf9a-104">The XML in this example defines a task that starts Notepad when the task is registered.</span></span>

<span data-ttu-id="fbf9a-105">Para registrar uma tarefa que é definida em XML, você pode usar a função [**ITaskFolder:: RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) ([**TaskFolder. RegisterTask**](taskfolder-registertask.md) para scripts) ou a ferramenta de linha de comando Schtasks.exe.</span><span class="sxs-lookup"><span data-stu-id="fbf9a-105">To register a task that is defined in XML, you can use either the [**ITaskFolder::RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) function ([**TaskFolder.RegisterTask**](taskfolder-registertask.md) for scripting) or the Schtasks.exe command-line tool.</span></span> <span data-ttu-id="fbf9a-106">Se você usar a ferramenta de Schtasks.exe (localizada no diretório C: \\ Windows \\ System32), poderá usar o comando a seguir para registrar a tarefa: **SCHTASKS/CREATE/XML** *<path to the XML file containing the task definition>* **/TN** *<task name>* .</span><span class="sxs-lookup"><span data-stu-id="fbf9a-106">If you use the Schtasks.exe tool (located in the C:\\Windows\\System32 directory), then you can use the following command to register the task: **schtasks /create /XML** *<path to the XML file containing the task definition>* **/tn** *<task name>*.</span></span>

> [!Note]  
> <span data-ttu-id="fbf9a-107">Quando uma tarefa com um gatilho de registro é atualizada, a tarefa será executada Depois que a atualização ocorrer.</span><span class="sxs-lookup"><span data-stu-id="fbf9a-107">When a task with a registration trigger is updated, the task will execute after the update occurs.</span></span>

 

## <a name="to-define-a-task-to-start-notepad-on-registration"></a><span data-ttu-id="fbf9a-108">Para definir uma tarefa para iniciar o bloco de notas no registro</span><span class="sxs-lookup"><span data-stu-id="fbf9a-108">To define a task to start Notepad on registration</span></span>

<span data-ttu-id="fbf9a-109">O exemplo de XML a seguir mostra como definir uma tarefa com uma única ação de execução (iniciando bloco de notas), um único gatilho de registro que inicia a tarefa quando ela é registrada e várias outras configurações de tarefa que afetam o modo como a tarefa é manipulada pelo Agendador de Tarefas.</span><span class="sxs-lookup"><span data-stu-id="fbf9a-109">The following XML example shows how to define a task with a single execution action (starting Notepad), a single registration trigger that starts the task when it is registered, and several other task settings that affect how the task is handled by the Task Scheduler.</span></span>

> [!Note]  
> <span data-ttu-id="fbf9a-110">Quando uma tarefa com um gatilho de registro é atualizada, a tarefa será executada Depois que a atualização ocorrer.</span><span class="sxs-lookup"><span data-stu-id="fbf9a-110">When a task with a registration trigger is updated, the task will execute after the update occurs.</span></span>

 


```XML
<?xml version="1.0" ?>
<!--
This sample schedules a task to start notepad.exe when
the task is registered.
-->
<Task xmlns="http://schemas.microsoft.com/windows/2004/02/mit/task">
    <RegistrationInfo>
        <Date>2005-10-11T13:21:17-08:00</Date>
        <Author>AuthorName</Author>
        <Version>1.0.0</Version>
        <Description>Task starts after registration.</Description>
    </RegistrationInfo>
    <Triggers>
        <RegistrationTrigger>
        </RegistrationTrigger>
    </Triggers>
    <Principals>
        <Principal>
            <UserId>Administrator</UserId>
            <LogonType>InteractiveToken</LogonType>
        </Principal>
    </Principals>
    <Settings>
        <Enabled>true</Enabled>
        <AllowStartOnDemand>true</AllowStartOnDemand>
        <AllowHardTerminate>true</AllowHardTerminate>
    </Settings>
    <Actions>
        <Exec>
            <Command>notepad.exe</Command>
        </Exec>
    </Actions>
</Task>
```



## <a name="taskscheduler-schema-elements"></a><span data-ttu-id="fbf9a-111">Elementos do esquema TaskScheduler</span><span class="sxs-lookup"><span data-stu-id="fbf9a-111">TaskScheduler Schema Elements</span></span>

<span data-ttu-id="fbf9a-112">Aqui estão alguns elementos importantes para ter em mente ao usar este exemplo.</span><span class="sxs-lookup"><span data-stu-id="fbf9a-112">Here are some important elements to keep in mind when using this example.</span></span>

-   <span data-ttu-id="fbf9a-113">[**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md): contém informações de registro sobre a tarefa.</span><span class="sxs-lookup"><span data-stu-id="fbf9a-113">[**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md): Contains registration information about the task.</span></span>
-   <span data-ttu-id="fbf9a-114">[**Triggers**](taskschedulerschema-triggers-tasktype-element.md): define o gatilho que inicia a tarefa.</span><span class="sxs-lookup"><span data-stu-id="fbf9a-114">[**Triggers**](taskschedulerschema-triggers-tasktype-element.md): Defines the trigger that starts the task.</span></span>
-   <span data-ttu-id="fbf9a-115">[**RegistrationTrigger**](taskschedulerschema-registrationtrigger-triggergroup-element.md): define o gatilho de registro.</span><span class="sxs-lookup"><span data-stu-id="fbf9a-115">[**RegistrationTrigger**](taskschedulerschema-registrationtrigger-triggergroup-element.md): Defines the registration trigger.</span></span> <span data-ttu-id="fbf9a-116">Nesse caso, somente dois elementos filho são usados: os limites inicial e final que especificam quando o gatilho é ativado e desativado.</span><span class="sxs-lookup"><span data-stu-id="fbf9a-116">In this case, only two child elements are used: the start and end boundaries that specify when the trigger is activated and deactivated.</span></span>
-   <span data-ttu-id="fbf9a-117">[**Principal**](taskschedulerschema-principal-principaltype-element.md): define o contexto de segurança em que uma tarefa é executada.</span><span class="sxs-lookup"><span data-stu-id="fbf9a-117">[**Principal**](taskschedulerschema-principal-principaltype-element.md): Defines the security context that a task runs under.</span></span>
-   <span data-ttu-id="fbf9a-118">[**Configurações**](taskschedulerschema-settings-tasktype-element.md): define as configurações de tarefa que o Agendador de tarefas usa para executar a tarefa.</span><span class="sxs-lookup"><span data-stu-id="fbf9a-118">[**Settings**](taskschedulerschema-settings-tasktype-element.md): Defines the task settings that the Task Scheduler uses to perform the task.</span></span>
-   <span data-ttu-id="fbf9a-119">[**Ações**](taskschedulerschema-actions-tasktype-element.md): define as ações que a tarefa executa.</span><span class="sxs-lookup"><span data-stu-id="fbf9a-119">[**Actions**](taskschedulerschema-actions-tasktype-element.md): Defines the actions the task performs.</span></span> <span data-ttu-id="fbf9a-120">Nesse caso, executar o bloco de notas.</span><span class="sxs-lookup"><span data-stu-id="fbf9a-120">In this case, running Notepad.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fbf9a-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="fbf9a-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fbf9a-122">Usando o Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="fbf9a-122">Using the Task Scheduler</span></span>](using-the-task-scheduler.md)
</dt> </dl>

 

 




