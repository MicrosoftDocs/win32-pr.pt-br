---
title: Agendador de Tarefas para desenvolvedores
description: O Agendador de Tarefas permite que você execute automaticamente tarefas rotineiras em um computador escolhido. Agendador de Tarefas faz isso monitorando quaisquer critérios que você escolher (chamados de gatilhos) e executando as tarefas quando esses critérios forem atendidos.
ms.assetid: 15970a51-c139-48b8-b82b-605728d0f386
keywords:
- Agendador de Tarefas para desenvolvedores
- Agendador de Tarefas para desenvolvimento
- Desenvolvendo com Agendador de Tarefas
- Agendador de Tarefas, página do portal
ms.topic: article
ms.date: 10/18/2019
ms.openlocfilehash: dfbfb76145e38003e7c501b98c817f4aaca3ff09
ms.sourcegitcommit: 087843ef08ddcd8bce9ed647b610035925da2b3e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/19/2019
ms.locfileid: "104084135"
---
# <a name="task-scheduler-for-developers"></a><span data-ttu-id="801f9-108">Agendador de Tarefas para desenvolvedores</span><span class="sxs-lookup"><span data-stu-id="801f9-108">Task Scheduler for developers</span></span>

> [!IMPORTANT]
> <span data-ttu-id="801f9-109">Este tópico e os outros tópicos desta seção são para um público de desenvolvedor.</span><span class="sxs-lookup"><span data-stu-id="801f9-109">This topic and the other topics in this section are for a developer audience.</span></span> <span data-ttu-id="801f9-110">Se você estiver querendo usar o componente de Agendador de Tarefas em sua capacidade como administrador ou um profissional de ti, consulte [Agendador de tarefas](/dynamics365/business-central/dev-itpro/developer/devenv-task-scheduler).</span><span class="sxs-lookup"><span data-stu-id="801f9-110">If you're wishing to use the the Task Scheduler component in your capacity as an administrator, or an IT Professional, then see [Task Scheduler](/dynamics365/business-central/dev-itpro/developer/devenv-task-scheduler).</span></span>

## <a name="about-the-task-scheduler"></a><span data-ttu-id="801f9-111">Sobre o Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="801f9-111">About the Task Scheduler</span></span>

<span data-ttu-id="801f9-112">O Agendador de Tarefas permite que você execute automaticamente tarefas rotineiras em um computador escolhido.</span><span class="sxs-lookup"><span data-stu-id="801f9-112">The Task Scheduler enables you to automatically perform routine tasks on a chosen computer.</span></span> <span data-ttu-id="801f9-113">Agendador de Tarefas faz isso monitorando quaisquer critérios que você escolher (chamados de gatilhos) e executando as tarefas quando esses critérios forem atendidos.</span><span class="sxs-lookup"><span data-stu-id="801f9-113">Task Scheduler does this by monitoring whatever criteria you choose (referred to as triggers) and then executing the tasks when those criteria are met.</span></span>

<span data-ttu-id="801f9-114">Você pode usar o Agendador de Tarefas para executar tarefas como iniciar um aplicativo, enviar uma mensagem de email ou mostrar uma caixa de mensagem.</span><span class="sxs-lookup"><span data-stu-id="801f9-114">You can use the Task Scheduler to execute tasks such as starting an application, sending an email message, or showing a message box.</span></span> <span data-ttu-id="801f9-115">As tarefas podem ser agendadas para serem executadas em resposta a esses eventos ou gatilhos.</span><span class="sxs-lookup"><span data-stu-id="801f9-115">Tasks can be scheduled to execute in response to these events, or triggers.</span></span> 

- <span data-ttu-id="801f9-116">Quando ocorre um evento de sistema específico.</span><span class="sxs-lookup"><span data-stu-id="801f9-116">When a specific system event occurs.</span></span>
- <span data-ttu-id="801f9-117">Em um momento específico.</span><span class="sxs-lookup"><span data-stu-id="801f9-117">At a specific time.</span></span>
- <span data-ttu-id="801f9-118">Em um horário específico em um agendamento diário.</span><span class="sxs-lookup"><span data-stu-id="801f9-118">At a specific time on a daily schedule.</span></span>
- <span data-ttu-id="801f9-119">Em um horário específico em um cronograma semanal.</span><span class="sxs-lookup"><span data-stu-id="801f9-119">At a specific time on a weekly schedule.</span></span>
- <span data-ttu-id="801f9-120">Em um horário específico em um agendamento mensal.</span><span class="sxs-lookup"><span data-stu-id="801f9-120">At a specific time on a monthly schedule.</span></span>
- <span data-ttu-id="801f9-121">Em um horário específico em uma agenda mensal de dia da semana.</span><span class="sxs-lookup"><span data-stu-id="801f9-121">At a specific time on a monthly day-of-week schedule.</span></span>
- <span data-ttu-id="801f9-122">Quando o computador entra em um estado ocioso.</span><span class="sxs-lookup"><span data-stu-id="801f9-122">When the computer enters an idle state.</span></span>
- <span data-ttu-id="801f9-123">Quando a tarefa é registrada.</span><span class="sxs-lookup"><span data-stu-id="801f9-123">When the task is registered.</span></span>
- <span data-ttu-id="801f9-124">Quando o sistema é inicializado.</span><span class="sxs-lookup"><span data-stu-id="801f9-124">When the system is booted.</span></span>
- <span data-ttu-id="801f9-125">Quando um usuário faz logon.</span><span class="sxs-lookup"><span data-stu-id="801f9-125">When a user logs on.</span></span>
- <span data-ttu-id="801f9-126">Quando uma sessão de Terminal Server muda de estado.</span><span class="sxs-lookup"><span data-stu-id="801f9-126">When a Terminal Server session changes state.</span></span>

## <a name="developers"></a><span data-ttu-id="801f9-127">Desenvolvedores</span><span class="sxs-lookup"><span data-stu-id="801f9-127">Developers</span></span>

<span data-ttu-id="801f9-128">O Agendador de Tarefas fornece APIs nesses formulários.</span><span class="sxs-lookup"><span data-stu-id="801f9-128">The Task Scheduler provides APIs in these forms.</span></span>

- <span data-ttu-id="801f9-129">Agendador de Tarefas 2,0: interfaces e objetos são fornecidos para C++ e para desenvolvimento de scripts, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="801f9-129">Task Scheduler 2.0: interfaces and objects are provided for C++, and for scripting development, respectively.</span></span>
- <span data-ttu-id="801f9-130">Agendador de Tarefas 1,0: as interfaces são fornecidas para desenvolvimento em C++.</span><span class="sxs-lookup"><span data-stu-id="801f9-130">Task Scheduler 1.0: interfaces are provided for C++ development.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="801f9-131">Requisitos de tempo de execução</span><span class="sxs-lookup"><span data-stu-id="801f9-131">Run-time requirements</span></span>

<span data-ttu-id="801f9-132">O Agendador de Tarefas requer os seguintes sistemas operacionais.</span><span class="sxs-lookup"><span data-stu-id="801f9-132">The Task Scheduler requires the following operating systems.</span></span>

- <span data-ttu-id="801f9-133">Agendador de Tarefas 2,0: o cliente requer o Windows Vista ou superior.</span><span class="sxs-lookup"><span data-stu-id="801f9-133">Task Scheduler 2.0: Client requires Windows Vista, or above.</span></span> <span data-ttu-id="801f9-134">O servidor requer o Windows Server 2008 ou superior.</span><span class="sxs-lookup"><span data-stu-id="801f9-134">Server requires Windows Server 2008, or above.</span></span>
- <span data-ttu-id="801f9-135">Agendador de Tarefas 1,0: o cliente requer o Windows Vista ou o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="801f9-135">Task Scheduler 1.0: Client requires Windows Vista, or Windows XP.</span></span> <span data-ttu-id="801f9-136">O servidor requer o Windows Server 2008 ou o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="801f9-136">Server requires Windows Server 2008, or Windows Server 2003.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="801f9-137">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="801f9-137">In this section</span></span>

| <span data-ttu-id="801f9-138">Tópico</span><span class="sxs-lookup"><span data-stu-id="801f9-138">Topic</span></span> | <span data-ttu-id="801f9-139">Descrição</span><span class="sxs-lookup"><span data-stu-id="801f9-139">Description</span></span> |
|-|-|
| [<span data-ttu-id="801f9-140">O que há de novo no Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="801f9-140">What's new in Task Scheduler</span></span>](what-s-new-in-task-scheduler.md) | <span data-ttu-id="801f9-141">Resumo da nova funcionalidade introduzida pelo Agendador de Tarefas.</span><span class="sxs-lookup"><span data-stu-id="801f9-141">Summary of new functionality introduced by the Task Scheduler.</span></span> |
| [<span data-ttu-id="801f9-142">Sobre o Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="801f9-142">About the Task Scheduler</span></span>](about-the-task-scheduler.md) | <span data-ttu-id="801f9-143">Informações conceituais gerais sobre a API de Agendador de Tarefas.</span><span class="sxs-lookup"><span data-stu-id="801f9-143">General conceptual information about the Task Scheduler API.</span></span> |
| [<span data-ttu-id="801f9-144">Usando o Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="801f9-144">Using the Task Scheduler</span></span>](using-the-task-scheduler.md) | <span data-ttu-id="801f9-145">Exemplos de código que mostram como usar as APIs de Agendador de Tarefas.</span><span class="sxs-lookup"><span data-stu-id="801f9-145">Code examples that show how to use the Task Scheduler APIs.</span></span> |
| [<span data-ttu-id="801f9-146">Referência de Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="801f9-146">Task Scheduler reference</span></span>](task-scheduler-reference.md) | <span data-ttu-id="801f9-147">Informações de referência detalhadas para APIs de Agendador de Tarefas e o esquema de Agendador de Tarefas.</span><span class="sxs-lookup"><span data-stu-id="801f9-147">Detailed reference information for Task Scheduler APIs and the Task Scheduler schema.</span></span> |