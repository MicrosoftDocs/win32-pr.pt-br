---
title: Agendador de Tarefas tipos enumerados 2,0
description: Descreve os tipos enumerados que definem as constantes que são usadas pelas APIs Agendador de Tarefas 2,0.
ms.assetid: d59f017e-df32-4826-954d-9ba338282d0d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db410564ab97f0477ecac8aeda2b54b8fd655d62
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104294632"
---
# <a name="task-scheduler-20-enumerated-types"></a><span data-ttu-id="12b36-103">Agendador de Tarefas tipos enumerados 2,0</span><span class="sxs-lookup"><span data-stu-id="12b36-103">Task Scheduler 2.0 Enumerated Types</span></span>

<span data-ttu-id="12b36-104">Descreve os tipos enumerados que definem as constantes que são usadas pelas APIs Agendador de Tarefas 2,0.</span><span class="sxs-lookup"><span data-stu-id="12b36-104">Describes the enumerated types that define the constants that are used by the Task Scheduler 2.0 APIs.</span></span>


<span data-ttu-id="12b36-105">Os seguintes tipos enumerados são introduzidos no Agendador de Tarefas 2,0.</span><span class="sxs-lookup"><span data-stu-id="12b36-105">The following enumerated types are introduced in Task Scheduler 2.0.</span></span>



| <span data-ttu-id="12b36-106">Enumeração</span><span class="sxs-lookup"><span data-stu-id="12b36-106">Enumeration</span></span>                                                                  | <span data-ttu-id="12b36-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="12b36-107">Description</span></span>                                                                                                      |
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="12b36-108">**\_tipo de ação da tarefa \_**</span><span class="sxs-lookup"><span data-stu-id="12b36-108">**TASK\_ACTION\_TYPE**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_action_type)                               | <span data-ttu-id="12b36-109">Define o tipo de ações que uma tarefa pode executar.</span><span class="sxs-lookup"><span data-stu-id="12b36-109">Defines the type of actions that a task can perform.</span></span>                                                             |
| [<span data-ttu-id="12b36-110">**compatibilidade de tarefas \_**</span><span class="sxs-lookup"><span data-stu-id="12b36-110">**TASK\_COMPATIBILITY**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_compatibility)                            | <span data-ttu-id="12b36-111">Define quais versões do Agendador de Tarefas ou o comando AT com o qual a tarefa é compatível.</span><span class="sxs-lookup"><span data-stu-id="12b36-111">Defines what versions of Task Scheduler or the AT command that the task is compatible with.</span></span>                      |
| [<span data-ttu-id="12b36-112">**criação de tarefa \_**</span><span class="sxs-lookup"><span data-stu-id="12b36-112">**TASK\_CREATION**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_creation)                                       | <span data-ttu-id="12b36-113">Define como o serviço de Agendador de Tarefas cria, atualiza ou desabilita a tarefa.</span><span class="sxs-lookup"><span data-stu-id="12b36-113">Defines how the Task Scheduler service creates, updates, or disables the task.</span></span>                                   |
| [<span data-ttu-id="12b36-114">**\_sinalizadores de enumeração de tarefa \_**</span><span class="sxs-lookup"><span data-stu-id="12b36-114">**TASK\_ENUM\_FLAGS**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_enum_flags)                                 | <span data-ttu-id="12b36-115">Define como o Agendador de Tarefas enumera por meio de tarefas registradas.</span><span class="sxs-lookup"><span data-stu-id="12b36-115">Defines how the Task Scheduler enumerates through registered tasks.</span></span>                                              |
| [<span data-ttu-id="12b36-116">**\_política de instâncias de tarefas \_**</span><span class="sxs-lookup"><span data-stu-id="12b36-116">**TASK\_INSTANCES\_POLICY**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_instances_policy)                     | <span data-ttu-id="12b36-117">Define como o Agendador de Tarefas trata as instâncias existentes da tarefa quando ele inicia uma nova instância da tarefa.</span><span class="sxs-lookup"><span data-stu-id="12b36-117">Defines how the Task Scheduler handles existing instances of the task when it starts a new instance of the task.</span></span> |
| [<span data-ttu-id="12b36-118">**TIPO de logon da tarefa \_**</span><span class="sxs-lookup"><span data-stu-id="12b36-118">**TASK\_LOGON TYPE**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_logon_type)                                  | <span data-ttu-id="12b36-119">Define qual técnica de logon é necessária para executar uma tarefa.</span><span class="sxs-lookup"><span data-stu-id="12b36-119">Defines what logon technique is required to run a task.</span></span>                                                          |
| [<span data-ttu-id="12b36-120">**\_tipo de PROCESSTOKENSID de tarefa \_**</span><span class="sxs-lookup"><span data-stu-id="12b36-120">**TASK\_PROCESSTOKENSID\_TYPE**</span></span>](/windows/win32/api/taskschd/ne-taskschd-task_processtokensid_type)             | <span data-ttu-id="12b36-121">Define os tipos de SID de processo que podem ser usados pelas tarefas.</span><span class="sxs-lookup"><span data-stu-id="12b36-121">Defines the types of process SID that can be used by tasks.</span></span>                                                      |
| [<span data-ttu-id="12b36-122">**\_sinalizadores de execução de tarefa \_**</span><span class="sxs-lookup"><span data-stu-id="12b36-122">**TASK\_RUN\_FLAGS**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_run_flags)                                   | <span data-ttu-id="12b36-123">Define como uma tarefa é executada.</span><span class="sxs-lookup"><span data-stu-id="12b36-123">Defines how a task is run.</span></span>                                                                                       |
| [<span data-ttu-id="12b36-124">**\_tipo de runlevel de tarefa \_**</span><span class="sxs-lookup"><span data-stu-id="12b36-124">**TASK\_RUNLEVEL\_TYPE**</span></span>](/windows/win32/api/taskschd/ne-taskschd-task_runlevel_type)                           | <span data-ttu-id="12b36-125">Define sinalizadores de elevação de LUA que especificam com que nível de privilégio a tarefa será executada.</span><span class="sxs-lookup"><span data-stu-id="12b36-125">Defines LUA elevation flags that specify with what privilege level the task will be run.</span></span>                         |
| [<span data-ttu-id="12b36-126">**\_tipo de \_ alteração de estado da sessão de tarefa \_ \_**</span><span class="sxs-lookup"><span data-stu-id="12b36-126">**TASK\_SESSION\_STATE\_CHANGE\_TYPE**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_session_state_change_type) | <span data-ttu-id="12b36-127">Define os tipos de Terminal Server alteração de estado de sessão que você pode usar para disparar uma tarefa a ser iniciada.</span><span class="sxs-lookup"><span data-stu-id="12b36-127">Defines what kinds of Terminal Server session state change you can use to trigger a task to start.</span></span>               |
| [<span data-ttu-id="12b36-128">**estado da tarefa \_**</span><span class="sxs-lookup"><span data-stu-id="12b36-128">**TASK\_STATE**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_state)                                            | <span data-ttu-id="12b36-129">Define os diferentes Estados em que uma tarefa registrada pode estar.</span><span class="sxs-lookup"><span data-stu-id="12b36-129">Defines the different states that a registered task can be in.</span></span>                                                   |
| [<span data-ttu-id="12b36-130">**Gatilho de tarefa \_ \_ TYPE2**</span><span class="sxs-lookup"><span data-stu-id="12b36-130">**TASK\_TRIGGER\_TYPE2**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_trigger_type2)                                  | <span data-ttu-id="12b36-131">Define o tipo de gatilhos que podem ser usados pelas tarefas.</span><span class="sxs-lookup"><span data-stu-id="12b36-131">Defines the type of triggers that can be used by tasks.</span></span>                                                          |



 

## <a name="related-topics"></a><span data-ttu-id="12b36-132">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="12b36-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="12b36-133">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="12b36-133">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="12b36-134">Referência de Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="12b36-134">Task Scheduler Reference</span></span>](task-scheduler-reference.md)
</dt> </dl>

 

 




