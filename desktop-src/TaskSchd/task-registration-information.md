---
title: Informações de registro da tarefa
description: As informações de registro fornecem uma maneira de identificar uma tarefa de várias maneiras diferentes. Por exemplo, uma tarefa pode ser identificada pelo autor, como ela foi criada (conhecida como a origem da tarefa) e a data de registro.
ms.assetid: 45c9fa99-2718-4202-8987-4b506bd677e9
keywords:
- Agendador de Tarefas de informações de registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed6c5048e9cbb9b41abcd9052a02371cd575b57c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104291766"
---
# <a name="task-registration-information"></a><span data-ttu-id="d40c3-105">Informações de registro da tarefa</span><span class="sxs-lookup"><span data-stu-id="d40c3-105">Task Registration Information</span></span>

<span data-ttu-id="d40c3-106">As informações de registro fornecem uma maneira de identificar uma tarefa de várias maneiras diferentes.</span><span class="sxs-lookup"><span data-stu-id="d40c3-106">Registration information provides a way to identify a task in several different ways.</span></span> <span data-ttu-id="d40c3-107">Por exemplo, uma tarefa pode ser identificada pelo autor, como ela foi criada (conhecida como a origem da tarefa) e a data de registro.</span><span class="sxs-lookup"><span data-stu-id="d40c3-107">For example, a task can be identified by the author, how it was authored (referred to as the task source), and date of registration.</span></span>

## <a name="using-registration-information"></a><span data-ttu-id="d40c3-108">Usando informações de registro</span><span class="sxs-lookup"><span data-stu-id="d40c3-108">Using Registration Information</span></span>

<span data-ttu-id="d40c3-109">As informações de registro normalmente são especificadas quando a tarefa é criada e, em seguida, usada das seguintes maneiras:</span><span class="sxs-lookup"><span data-stu-id="d40c3-109">Registration information is typically specified when the task is created and then used in the following ways:</span></span>

-   <span data-ttu-id="d40c3-110">Exibido pela interface do usuário do Agendador de Tarefas.</span><span class="sxs-lookup"><span data-stu-id="d40c3-110">Displayed by the Task Scheduler user interface.</span></span>
-   <span data-ttu-id="d40c3-111">Obter ou definir por aplicativos ou scripts do C++.</span><span class="sxs-lookup"><span data-stu-id="d40c3-111">Get or set by C++ applications or scripts.</span></span>
-   <span data-ttu-id="d40c3-112">Em um ambiente corporativo, usado como critério de pesquisa ao enumerar todas as tarefas registradas.</span><span class="sxs-lookup"><span data-stu-id="d40c3-112">In an enterprise environment, used as a search criteria when enumerating over all registered tasks.</span></span>

## <a name="types-of-registration-information"></a><span data-ttu-id="d40c3-113">Tipos de informações de registro</span><span class="sxs-lookup"><span data-stu-id="d40c3-113">Types of Registration Information</span></span>

<span data-ttu-id="d40c3-114">As informações de registro de tarefa são definidas pelas propriedades do objeto [**RegistrationInfo**](registrationinfo.md) para aplicativos de script, as propriedades da interface [**IRegistrationInfo**](/windows/desktop/api/taskschd/nn-taskschd-iregistrationinfo) para aplicativos C++ e os elementos filho do [**elemento RegistrationInfo (TaskType)**](taskschedulerschema-registrationinfo-tasktype-element.md) para leitura ou gravação de XML.</span><span class="sxs-lookup"><span data-stu-id="d40c3-114">Task registration information is defined by the properties of the [**RegistrationInfo**](registrationinfo.md) object for scripting applications, the properties of the [**IRegistrationInfo**](/windows/desktop/api/taskschd/nn-taskschd-iregistrationinfo) interface for C++ applications, and the child elements of the [**RegistrationInfo (taskType) element**](taskschedulerschema-registrationinfo-tasktype-element.md) for reading or writing XML.</span></span>

<span data-ttu-id="d40c3-115">Essas propriedades permitem o acesso aos seguintes tipos de informações de registro:</span><span class="sxs-lookup"><span data-stu-id="d40c3-115">These properties allow access to the following types of registration information:</span></span>

-   <span data-ttu-id="d40c3-116">Autor da tarefa</span><span class="sxs-lookup"><span data-stu-id="d40c3-116">Task Author</span></span>

    <span data-ttu-id="d40c3-117">Agendador de Tarefas define o autor da tarefa quando ela é criada.</span><span class="sxs-lookup"><span data-stu-id="d40c3-117">Task Scheduler sets the author of the task when it is created.</span></span>

-   <span data-ttu-id="d40c3-118">Data de registro da tarefa</span><span class="sxs-lookup"><span data-stu-id="d40c3-118">Task Registration Date</span></span>

    <span data-ttu-id="d40c3-119">Agendador de Tarefas define essa data quando a tarefa é registrada.</span><span class="sxs-lookup"><span data-stu-id="d40c3-119">Task Scheduler sets this date when the task is registered.</span></span>

-   <span data-ttu-id="d40c3-120">Descrição da tarefa</span><span class="sxs-lookup"><span data-stu-id="d40c3-120">Task Description</span></span>

    <span data-ttu-id="d40c3-121">Uma descrição definida pelo usuário que pode incluir quais gatilhos são usados para iniciar a tarefa ou quais ações a tarefa executa.</span><span class="sxs-lookup"><span data-stu-id="d40c3-121">A user-defined description that may include what triggers are used to start the task or what actions the task performs.</span></span>

-   <span data-ttu-id="d40c3-122">Documentação da tarefa</span><span class="sxs-lookup"><span data-stu-id="d40c3-122">Task Documentation</span></span>

    <span data-ttu-id="d40c3-123">Documentação fornecida pelo usuário que é necessária para a tarefa.</span><span class="sxs-lookup"><span data-stu-id="d40c3-123">User-supplied documentation that is needed by the task.</span></span>

-   <span data-ttu-id="d40c3-124">Descritor de segurança da tarefa</span><span class="sxs-lookup"><span data-stu-id="d40c3-124">Task Security Descriptor</span></span>

    <span data-ttu-id="d40c3-125">Um descritor de segurança fornecido pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="d40c3-125">A user-supplied security descriptor.</span></span>

-   <span data-ttu-id="d40c3-126">Origem da tarefa</span><span class="sxs-lookup"><span data-stu-id="d40c3-126">Task Source</span></span>

    <span data-ttu-id="d40c3-127">Informações fornecidas pelo usuário que descrevem de onde a tarefa foi originada.</span><span class="sxs-lookup"><span data-stu-id="d40c3-127">User-supplied information that describes where the task originated from.</span></span> <span data-ttu-id="d40c3-128">Por exemplo, uma tarefa pode se originar de um componente, serviço, aplicativo ou usuário.</span><span class="sxs-lookup"><span data-stu-id="d40c3-128">For example, a task may originate from a component, service, application, or user.</span></span>

-   <span data-ttu-id="d40c3-129">URI da tarefa</span><span class="sxs-lookup"><span data-stu-id="d40c3-129">Task URI</span></span>

    <span data-ttu-id="d40c3-130">Um URI (Uniform Resource Identifier) para a tarefa.</span><span class="sxs-lookup"><span data-stu-id="d40c3-130">A uniform resource identifier (URI) for the task.</span></span>

-   <span data-ttu-id="d40c3-131">Versão da Tarefa</span><span class="sxs-lookup"><span data-stu-id="d40c3-131">Task Version</span></span>

    <span data-ttu-id="d40c3-132">Informações fornecidas pelo usuário que são usadas quando há várias versões de uma tarefa.</span><span class="sxs-lookup"><span data-stu-id="d40c3-132">User-supplied information that is used when multiple versions of a task exist.</span></span>

-   <span data-ttu-id="d40c3-133">Texto XML</span><span class="sxs-lookup"><span data-stu-id="d40c3-133">XML Text</span></span>

    <span data-ttu-id="d40c3-134">Uma versão formatada em XML das informações de registro.</span><span class="sxs-lookup"><span data-stu-id="d40c3-134">An XML-formatted version of the registration information.</span></span> <span data-ttu-id="d40c3-135">Observe que você pode definir ou modificar as informações de registro diretamente por meio desse XML e as propriedades apropriadas de objeto e de interface serão atualizadas de acordo.</span><span class="sxs-lookup"><span data-stu-id="d40c3-135">Note that you can set or modify the registration information directly through this XML and the appropriate object and interface properties will be updated accordingly.</span></span>

## <a name="registering-tasks"></a><span data-ttu-id="d40c3-136">Registrando tarefas</span><span class="sxs-lookup"><span data-stu-id="d40c3-136">Registering Tasks</span></span>

<span data-ttu-id="d40c3-137">Uma tarefa pode ser registrada depois que as definições de tarefa são criadas e as informações de registro e os valores de configuração são fornecidos pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="d40c3-137">A task can be registered after the task definitions are created and registration information and setting values are supplied by the user.</span></span> <span data-ttu-id="d40c3-138">Uma tarefa é registrada usando o método [**TaskFolder. RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) para aplicativos de script ou o método [**ITaskFolder:: RegisterTaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition) para aplicativos C++.</span><span class="sxs-lookup"><span data-stu-id="d40c3-138">A task is registered using the [**TaskFolder.RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) method for scripting applications or the [**ITaskFolder::RegisterTaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition) method for C++ applications.</span></span> <span data-ttu-id="d40c3-139">Se você quiser registrar uma tarefa usando XML para definir a tarefa, use o método [**TaskFolder. RegisterTask**](taskfolder-registertask.md) para aplicativos de script e o método [**ITaskFolder:: RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) para aplicativos C++.</span><span class="sxs-lookup"><span data-stu-id="d40c3-139">If you want to register a task using XML to define the task, you use the [**TaskFolder.RegisterTask**](taskfolder-registertask.md) method for scripting applications and the [**ITaskFolder::RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) method for C++ applications.</span></span>

<span data-ttu-id="d40c3-140">Nos métodos mencionados acima, você pode especificar o contexto de segurança para executar a tarefa.</span><span class="sxs-lookup"><span data-stu-id="d40c3-140">In the methods mentioned above, you can specify the security context to run the task.</span></span> <span data-ttu-id="d40c3-141">Você precisa ser um administrador no sistema para agendar trabalhos para serem executados em contextos diferentes do seu próprio.</span><span class="sxs-lookup"><span data-stu-id="d40c3-141">You have to be an administrator on the system to schedule jobs to run under contexts other than your own.</span></span> <span data-ttu-id="d40c3-142">Para obter mais informações sobre os contextos de segurança para executar tarefas, consulte [contextos de segurança para tarefas em execução](security-contexts-for-running-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="d40c3-142">For more information on the security contexts to run tasks, see [Security Contexts for Running Tasks](security-contexts-for-running-tasks.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d40c3-143">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d40c3-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d40c3-144">Sobre o Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="d40c3-144">About The Task Scheduler</span></span>](about-the-task-scheduler.md)
</dt> <dt>

[<span data-ttu-id="d40c3-145">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="d40c3-145">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 




