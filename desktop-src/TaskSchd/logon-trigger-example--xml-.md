---
title: Exemplo de gatilho de logon (XML)
description: O XML neste exemplo define uma tarefa que inicia o bloco de notas quando um usuário faz logon.
ms.assetid: c1cce95f-7558-489e-b092-c82d55b42165
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d66766ce4cae33c3526ac9d30071ff2082ddc1f2
ms.sourcegitcommit: 40dd8501397fc79a643deb528c6c57ac2e9726ce
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/24/2020
ms.locfileid: "104365430"
---
# <a name="logon-trigger-example-xml"></a><span data-ttu-id="6cbca-103">Exemplo de gatilho de logon (XML)</span><span class="sxs-lookup"><span data-stu-id="6cbca-103">Logon Trigger Example (XML)</span></span>

<span data-ttu-id="6cbca-104">O XML neste exemplo define uma tarefa que inicia o bloco de notas quando um usuário faz logon.</span><span class="sxs-lookup"><span data-stu-id="6cbca-104">The XML in this example defines a task that starts Notepad when a user logs on.</span></span>

<span data-ttu-id="6cbca-105">Para registrar uma tarefa que é definida em XML, você pode usar a função [**ITaskFolder:: RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) ([**TaskFolder. RegisterTask**](taskfolder-registertask.md) para scripts) ou a ferramenta de linha de comando Schtasks.exe.</span><span class="sxs-lookup"><span data-stu-id="6cbca-105">To register a task that is defined in XML, you can use either the [**ITaskFolder::RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) function ([**TaskFolder.RegisterTask**](taskfolder-registertask.md) for scripting) or the Schtasks.exe command-line tool.</span></span> <span data-ttu-id="6cbca-106">Se você usar a ferramenta de Schtasks.exe (localizada no diretório C: \\ Windows \\ System32), poderá usar o comando a seguir para registrar a tarefa: **SCHTASKS/CREATE/XML** *<path to the XML file containing the task definition>* **/TN** *<task name>* .</span><span class="sxs-lookup"><span data-stu-id="6cbca-106">If you use the Schtasks.exe tool (located in the C:\\Windows\\System32 directory), then you can use the following command to register the task: **schtasks /create /XML** *<path to the XML file containing the task definition>* **/tn** *<task name>*.</span></span>

## <a name="to-define-a-task-to-start-notepad-on-system-boot"></a><span data-ttu-id="6cbca-107">Para definir uma tarefa para iniciar o bloco de notas na inicialização do sistema</span><span class="sxs-lookup"><span data-stu-id="6cbca-107">To define a task to start Notepad on system boot</span></span>

<span data-ttu-id="6cbca-108">O exemplo de XML a seguir mostra como definir uma tarefa com uma única ação de execução (iniciando o bloco de notas), um único gatilho de logon que inicia a tarefa quando um usuário faz logon e várias outras configurações de tarefa que afetam o modo como a tarefa é manipulada pelo Agendador de Tarefas.</span><span class="sxs-lookup"><span data-stu-id="6cbca-108">The following XML example shows how to define a task with a single execution action (starting Notepad), a single logon trigger that starts the task when a user logs on, and several other task settings that affect how the task is handled by Task Scheduler.</span></span>

> [!Note]  
> <span data-ttu-id="6cbca-109">Defina o valor do elemento **userid** como um nome de usuário no computador em que a tarefa está registrada.</span><span class="sxs-lookup"><span data-stu-id="6cbca-109">Set the value of the **UserId** element to a user name on the computer on which the task is registered.</span></span>

 


```XML
<?xml version="1.0" ?>
<!--
This sample schedules a task to start notepad.exe when a user logs on.
-->
<Task xmlns="http://schemas.microsoft.com/windows/2004/02/mit/task">
    <RegistrationInfo>
        <Date>2005-10-11T13:21:17-08:00</Date>
        <Author>AuthorName</Author>
        <Version>1.0.0</Version>
        <Description>Starts Notepad when a specified user logs on.</Description>
    </RegistrationInfo>
    <Triggers>
        <LogonTrigger>
            <StartBoundary>2005-10-11T13:21:17-08:00</StartBoundary>
            <EndBoundary>2006-01-01T00:00:00-08:00</EndBoundary>
            <Enabled>true</Enabled>
            <UserId>DOMAIN_NAME\UserName</UserId>
        </LogonTrigger>
    </Triggers>
    <Principals>
        <Principal>
            <GroupId>Builtin\Administrators</GroupId>
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



## <a name="taskscheduler-schema-elements"></a><span data-ttu-id="6cbca-110">Elementos do esquema TaskScheduler</span><span class="sxs-lookup"><span data-stu-id="6cbca-110">TaskScheduler Schema Elements</span></span>

<span data-ttu-id="6cbca-111">Veja a seguir alguns elementos importantes para ter em mente ao usar este exemplo:</span><span class="sxs-lookup"><span data-stu-id="6cbca-111">The following are some important elements to keep in mind when using this example:</span></span>

-   <span data-ttu-id="6cbca-112">[**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md): contém informações de registro sobre a tarefa.</span><span class="sxs-lookup"><span data-stu-id="6cbca-112">[**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md): Contains registration information about the task.</span></span>
-   <span data-ttu-id="6cbca-113">[**Triggers**](taskschedulerschema-triggers-tasktype-element.md): define o gatilho que inicia a tarefa.</span><span class="sxs-lookup"><span data-stu-id="6cbca-113">[**Triggers**](taskschedulerschema-triggers-tasktype-element.md): Defines the trigger that starts the task.</span></span>
-   <span data-ttu-id="6cbca-114">[**LogonTrigger**](taskschedulerschema-logontrigger-triggergroup-element.md): define o gatilho de logon.</span><span class="sxs-lookup"><span data-stu-id="6cbca-114">[**LogonTrigger**](taskschedulerschema-logontrigger-triggergroup-element.md): Defines the logon trigger.</span></span> <span data-ttu-id="6cbca-115">Nesse caso, três elementos filho são usados: os limites inicial e final que especificam quando o gatilho é ativado e desativado e o elemento [**userid**](taskschedulerschema-userid-logontriggertype-element.md) que o identificador do usuário.</span><span class="sxs-lookup"><span data-stu-id="6cbca-115">In this case, three child elements are used: the start and end boundaries that specify when the trigger is activated and deactivated, and the [**UserId**](taskschedulerschema-userid-logontriggertype-element.md) element that identifier of the user.</span></span> <span data-ttu-id="6cbca-116">A tarefa é iniciada quando esse usuário faz logon no computador.</span><span class="sxs-lookup"><span data-stu-id="6cbca-116">The task is started when this user logs on to the computer..</span></span>
-   <span data-ttu-id="6cbca-117">[**Principal**](taskschedulerschema-principal-principaltype-element.md): define o contexto de segurança em que uma tarefa é executada.</span><span class="sxs-lookup"><span data-stu-id="6cbca-117">[**Principal**](taskschedulerschema-principal-principaltype-element.md): Defines the security context that a task runs under.</span></span>
-   <span data-ttu-id="6cbca-118">[**Configurações**](taskschedulerschema-settings-tasktype-element.md): define as configurações de tarefa que o Agendador de tarefas usa para executar a tarefa.</span><span class="sxs-lookup"><span data-stu-id="6cbca-118">[**Settings**](taskschedulerschema-settings-tasktype-element.md): Defines the task settings that the Task Scheduler uses to perform the task.</span></span>
-   <span data-ttu-id="6cbca-119">[**Ações**](taskschedulerschema-actions-tasktype-element.md): define as ações que a tarefa executa.</span><span class="sxs-lookup"><span data-stu-id="6cbca-119">[**Actions**](taskschedulerschema-actions-tasktype-element.md): Defines the actions the task performs.</span></span> <span data-ttu-id="6cbca-120">Nesse caso, executar o bloco de notas.</span><span class="sxs-lookup"><span data-stu-id="6cbca-120">In this case, running Notepad.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6cbca-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6cbca-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6cbca-122">Usando o Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="6cbca-122">Using the Task Scheduler</span></span>](using-the-task-scheduler.md)
</dt> </dl>

 

 




