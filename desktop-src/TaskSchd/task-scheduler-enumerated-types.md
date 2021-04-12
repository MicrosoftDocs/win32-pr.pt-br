---
title: Agendador de Tarefas tipos enumerados
description: Lista as enumerações usadas pelas APIs de Agendador de Tarefas.
ms.assetid: 9779d32b-0142-41bb-88e2-df79a3b0c1b2
keywords:
- Agendador de Tarefas Agendador de Tarefas, referência, tipos enumerados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a70c4a939d176516d47f6af8bc0825b414bf1de
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104499191"
---
# <a name="task-scheduler-enumerated-types"></a><span data-ttu-id="b68f7-104">Agendador de Tarefas tipos enumerados</span><span class="sxs-lookup"><span data-stu-id="b68f7-104">Task Scheduler Enumerated Types</span></span>

<span data-ttu-id="b68f7-105">Descreve os tipos enumerados que definem as constantes que são usadas pelas APIs de Agendador de Tarefas.</span><span class="sxs-lookup"><span data-stu-id="b68f7-105">Describes the enumerated types that define the constants that are used by the Task Scheduler APIs.</span></span>


<span data-ttu-id="b68f7-106">Os seguintes tipos enumerados são introduzidos no Agendador de Tarefas 2,0.</span><span class="sxs-lookup"><span data-stu-id="b68f7-106">The following enumerated types are introduced in Task Scheduler 2.0.</span></span>



| <span data-ttu-id="b68f7-107">Enumeração</span><span class="sxs-lookup"><span data-stu-id="b68f7-107">Enumeration</span></span>                                                                  | <span data-ttu-id="b68f7-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="b68f7-108">Description</span></span>                                                                                                      |
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b68f7-109">**\_tipo de ação da tarefa \_**</span><span class="sxs-lookup"><span data-stu-id="b68f7-109">**TASK\_ACTION\_TYPE**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_action_type)                               | <span data-ttu-id="b68f7-110">Define o tipo de ações que uma tarefa pode executar.</span><span class="sxs-lookup"><span data-stu-id="b68f7-110">Defines the type of actions that a task can perform.</span></span>                                                             |
| [<span data-ttu-id="b68f7-111">**compatibilidade de tarefas \_**</span><span class="sxs-lookup"><span data-stu-id="b68f7-111">**TASK\_COMPATIBILITY**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_compatibility)                            | <span data-ttu-id="b68f7-112">Define quais versões do Agendador de Tarefas ou o comando AT com o qual a tarefa é compatível.</span><span class="sxs-lookup"><span data-stu-id="b68f7-112">Defines what versions of Task Scheduler or the AT command that the task is compatible with.</span></span>                      |
| [<span data-ttu-id="b68f7-113">**criação de tarefa \_**</span><span class="sxs-lookup"><span data-stu-id="b68f7-113">**TASK\_CREATION**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_creation)                                       | <span data-ttu-id="b68f7-114">Define como o serviço de Agendador de Tarefas cria, atualiza ou desabilita a tarefa.</span><span class="sxs-lookup"><span data-stu-id="b68f7-114">Defines how the Task Scheduler service creates, updates, or disables the task.</span></span>                                   |
| [<span data-ttu-id="b68f7-115">**\_sinalizadores de enumeração de tarefa \_**</span><span class="sxs-lookup"><span data-stu-id="b68f7-115">**TASK\_ENUM\_FLAGS**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_enum_flags)                                 | <span data-ttu-id="b68f7-116">Define como o Agendador de Tarefas enumera por meio de tarefas registradas.</span><span class="sxs-lookup"><span data-stu-id="b68f7-116">Defines how the Task Scheduler enumerates through registered tasks.</span></span>                                              |
| [<span data-ttu-id="b68f7-117">**\_política de instâncias de tarefas \_**</span><span class="sxs-lookup"><span data-stu-id="b68f7-117">**TASK\_INSTANCES\_POLICY**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_instances_policy)                     | <span data-ttu-id="b68f7-118">Define como o Agendador de Tarefas trata as instâncias existentes da tarefa quando ele inicia uma nova instância da tarefa.</span><span class="sxs-lookup"><span data-stu-id="b68f7-118">Defines how the Task Scheduler handles existing instances of the task when it starts a new instance of the task.</span></span> |
| [<span data-ttu-id="b68f7-119">**TIPO de logon da tarefa \_**</span><span class="sxs-lookup"><span data-stu-id="b68f7-119">**TASK\_LOGON TYPE**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_logon_type)                                  | <span data-ttu-id="b68f7-120">Define qual técnica de logon é necessária para executar uma tarefa.</span><span class="sxs-lookup"><span data-stu-id="b68f7-120">Defines what logon technique is required to run a task.</span></span>                                                          |
| [<span data-ttu-id="b68f7-121">**TIPO de PROCESSTOKENSID de tarefa \_**</span><span class="sxs-lookup"><span data-stu-id="b68f7-121">**TASK\_PROCESSTOKENSID TYPE**</span></span>](/windows/win32/api/taskschd/ne-taskschd-task_processtokensid_type)              | <span data-ttu-id="b68f7-122">Define os tipos de SID de processo que podem ser usados pelas tarefas.</span><span class="sxs-lookup"><span data-stu-id="b68f7-122">Defines the types of process SID that can used by tasks.</span></span>                                                         |
| [<span data-ttu-id="b68f7-123">**\_sinalizadores de execução de tarefa \_**</span><span class="sxs-lookup"><span data-stu-id="b68f7-123">**TASK\_RUN\_FLAGS**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_run_flags)                                   | <span data-ttu-id="b68f7-124">Define como uma tarefa é executada.</span><span class="sxs-lookup"><span data-stu-id="b68f7-124">Defines how a task is run.</span></span>                                                                                       |
| [<span data-ttu-id="b68f7-125">**\_tipo de runlevel de tarefa \_**</span><span class="sxs-lookup"><span data-stu-id="b68f7-125">**TASK\_RUNLEVEL\_TYPE**</span></span>](/windows/win32/api/taskschd/ne-taskschd-task_runlevel_type)                           | <span data-ttu-id="b68f7-126">Define sinalizadores de elevação de LUA que especificam com que nível de privilégio a tarefa será executada.</span><span class="sxs-lookup"><span data-stu-id="b68f7-126">Defines LUA elevation flags that specify with what privilege level the task will be run.</span></span>                         |
| [<span data-ttu-id="b68f7-127">**\_tipo de \_ alteração de estado da sessão de tarefa \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b68f7-127">**TASK\_SESSION\_STATE\_CHANGE\_TYPE**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_session_state_change_type) | <span data-ttu-id="b68f7-128">Define os tipos de Terminal Server alteração de estado de sessão que você pode usar para disparar uma tarefa a ser iniciada.</span><span class="sxs-lookup"><span data-stu-id="b68f7-128">Defines what kinds of Terminal Server session state change you can use to trigger a task to start.</span></span>               |
| [<span data-ttu-id="b68f7-129">**estado da tarefa \_**</span><span class="sxs-lookup"><span data-stu-id="b68f7-129">**TASK\_STATE**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_state)                                            | <span data-ttu-id="b68f7-130">Define os diferentes Estados em que uma tarefa registrada pode estar.</span><span class="sxs-lookup"><span data-stu-id="b68f7-130">Defines the different states that a registered task can be in.</span></span>                                                   |
| [<span data-ttu-id="b68f7-131">**Gatilho de tarefa \_ \_ TYPE2**</span><span class="sxs-lookup"><span data-stu-id="b68f7-131">**TASK\_TRIGGER\_TYPE2**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_trigger_type2)                                  | <span data-ttu-id="b68f7-132">Define o tipo de gatilhos que podem ser usados pelas tarefas.</span><span class="sxs-lookup"><span data-stu-id="b68f7-132">Defines the type of triggers that can be used by tasks.</span></span>                                                          |



 


> [!WARNING]
> <span data-ttu-id="b68f7-133">As enumerações Agendador de Tarefas 1,0 estão disponíveis apenas nos sistemas operacionais Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="b68f7-133">The Task Scheduler 1.0 enumerations are available only in Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="b68f7-134">Eles foram preteridos no Windows Vista e podem ser removidos completamente no futuro.</span><span class="sxs-lookup"><span data-stu-id="b68f7-134">They are deprecated as of Windows Vista and may be removed completely in the future.</span></span> <span data-ttu-id="b68f7-135">Use as enumerações Agendador de Tarefas 2,0 listadas acima em vez disso.</span><span class="sxs-lookup"><span data-stu-id="b68f7-135">Please use the Task Scheduler 2.0 enumerations listed above instead.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="b68f7-136">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b68f7-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b68f7-137">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="b68f7-137">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="b68f7-138">Referência de Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="b68f7-138">Task Scheduler Reference</span></span>](task-scheduler-reference.md)
</dt> </dl>

 

 




