---
title: Repetindo uma tarefa
description: Agendador de Tarefas pode executar uma tarefa quantas vezes forem disparadas após um gatilho ser acionado.
ms.assetid: 69c60713-134c-4602-9e7b-cc3eea871068
keywords:
- padrão de repetição Agendador de Tarefas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 451b2c2cf7e48c40496ddba95728f435ab494ab7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292496"
---
# <a name="repeating-a-task"></a><span data-ttu-id="4225a-104">Repetindo uma tarefa</span><span class="sxs-lookup"><span data-stu-id="4225a-104">Repeating A Task</span></span>

<span data-ttu-id="4225a-105">Agendador de Tarefas pode executar uma tarefa quantas vezes forem disparadas após um gatilho ser acionado.</span><span class="sxs-lookup"><span data-stu-id="4225a-105">Task Scheduler can run a task any number of times times after a trigger is fired.</span></span> <span data-ttu-id="4225a-106">Para fazer isso, o gatilho define um padrão de repetição que informa Agendador de Tarefas por quanto tempo ele deve continuar a repetir a tarefa e o intervalo de tempo entre cada repetição de tarefa.</span><span class="sxs-lookup"><span data-stu-id="4225a-106">To do this, the trigger defines a repetition pattern that tells Task Scheduler how long it should continue to repeat the task and the time interval between each task repetition.</span></span>

## <a name="repetition-pattern"></a><span data-ttu-id="4225a-107">Padrão de repetição</span><span class="sxs-lookup"><span data-stu-id="4225a-107">Repetition Pattern</span></span>

<span data-ttu-id="4225a-108">A ilustração a seguir mostra um padrão de repetição com uma duração de 60 minutos e um intervalo de 25 minutos.</span><span class="sxs-lookup"><span data-stu-id="4225a-108">The following illustration shows a repetition pattern with a duration of 60 minutes and an interval of 25 minutes.</span></span> <span data-ttu-id="4225a-109">Lembre-se de que, nesse caso, Agendador de Tarefas executa a tarefa quando o gatilho é acionado, ele executa a tarefa novamente após 25 minutos e, em seguida, executa a tarefa novamente após 50 minutos, dependendo da configuração da [**Propriedade StopAtDurationEnd de IRepetitionPattern**](/windows/desktop/api/taskschd/nf-taskschd-irepetitionpattern-get_stopatdurationend) ([**RepetitionPattern. StopAtDurationEnd**](repetitionpattern-stopatdurationend.md) para scripts).</span><span class="sxs-lookup"><span data-stu-id="4225a-109">Be aware that in this case, Task Scheduler runs the task when the trigger is fired, it runs the task again after 25 minutes, then runs the task again after 50 minutes depending on the setting of the [**StopAtDurationEnd property of IRepetitionPattern**](/windows/desktop/api/taskschd/nf-taskschd-irepetitionpattern-get_stopatdurationend) ([**RepetitionPattern.StopAtDurationEnd**](repetitionpattern-stopatdurationend.md) for scripting).</span></span> <span data-ttu-id="4225a-110">Se a propriedade **StopAtDurationEnd** for definida como True, Agendador de tarefas interromperá a última instância da tarefa se ela ainda estiver em execução após 60 minutos.</span><span class="sxs-lookup"><span data-stu-id="4225a-110">If the **StopAtDurationEnd** property is set to True, Task Scheduler stops the last instance of the task if it is still running after 60 minutes.</span></span> <span data-ttu-id="4225a-111">Se a propriedade **StopAtDurationEnd** for definida como false, a última instância da tarefa será executada, independentemente da duração.</span><span class="sxs-lookup"><span data-stu-id="4225a-111">If the **StopAtDurationEnd** property is set to False, the last instance of the task is run regardless of the duration.</span></span>

![padrão de repetição de gatilho](images/repetition-pattern.png)

<span data-ttu-id="4225a-113">Se você registrar uma tarefa que contém um gatilho com um intervalo de repetição igual a um minuto e uma duração de repetição igual a quatro minutos, a tarefa será iniciada cinco vezes.</span><span class="sxs-lookup"><span data-stu-id="4225a-113">If you register a task that contains a trigger with a repetition interval equal to one minute and a repetition duration equal to four minutes, the task will be started five times.</span></span> <span data-ttu-id="4225a-114">As cinco repetições podem ser definidas pelo seguinte padrão:</span><span class="sxs-lookup"><span data-stu-id="4225a-114">The five repetitions can be defined by the following pattern:</span></span>

1.  <span data-ttu-id="4225a-115">Uma tarefa é iniciada no início do primeiro minuto.</span><span class="sxs-lookup"><span data-stu-id="4225a-115">A task starts at the beginning of the first minute.</span></span>
2.  <span data-ttu-id="4225a-116">A próxima tarefa é iniciada no final do primeiro minuto.</span><span class="sxs-lookup"><span data-stu-id="4225a-116">The next task starts at the end of the first minute.</span></span>
3.  <span data-ttu-id="4225a-117">A próxima tarefa é iniciada no final do segundo minuto.</span><span class="sxs-lookup"><span data-stu-id="4225a-117">The next task starts at the end of the second minute.</span></span>
4.  <span data-ttu-id="4225a-118">A próxima tarefa começa no final do terceiro minuto.</span><span class="sxs-lookup"><span data-stu-id="4225a-118">The next task starts at the end of the third minute.</span></span>
5.  <span data-ttu-id="4225a-119">A próxima tarefa é iniciada no final do quarto minuto.</span><span class="sxs-lookup"><span data-stu-id="4225a-119">The next task starts at the end of the fourth minute.</span></span>

<span data-ttu-id="4225a-120">**Windows Server 2003, Windows XP e windows 2000:** Se você registrar uma tarefa que contém um gatilho com um intervalo de repetição igual a um minuto e uma duração de repetição igual a quatro minutos, a tarefa será iniciada quatro vezes.</span><span class="sxs-lookup"><span data-stu-id="4225a-120">**Windows Server 2003, Windows XP and Windows 2000:** If you register a task that contains a trigger with a repetition interval equal to one minute and a repetition duration equal to four minutes, the task will be started four times.</span></span>

## <a name="objects-interfaces-and-xml-elements"></a><span data-ttu-id="4225a-121">Objetos, interfaces e elementos XML</span><span class="sxs-lookup"><span data-stu-id="4225a-121">Objects, Interfaces, and XML Elements</span></span>

<span data-ttu-id="4225a-122">Para o desenvolvimento de scripts, o padrão de repetição é definido usando o objeto [**RepetitionPattern**](repetitionpattern.md) .</span><span class="sxs-lookup"><span data-stu-id="4225a-122">For scripting development, the repetition pattern is defined using the [**RepetitionPattern**](repetitionpattern.md) object.</span></span>

<span data-ttu-id="4225a-123">Para o desenvolvimento em C++, o padrão de repetição é definido pela interface [**IRepetitionPattern**](/windows/desktop/api/taskschd/nn-taskschd-irepetitionpattern) .</span><span class="sxs-lookup"><span data-stu-id="4225a-123">For C++ development, the repetition pattern is defined by the [**IRepetitionPattern**](/windows/desktop/api/taskschd/nn-taskschd-irepetitionpattern) interface.</span></span>

<span data-ttu-id="4225a-124">Ao ler ou gravar XML para uma tarefa, o padrão de repetição é especificado no elemento de [**repetição**](taskschedulerschema-repetition-triggerbasetype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="4225a-124">When reading or writing XML for a task, the repetition pattern is specified in the [**Repetition**](taskschedulerschema-repetition-triggerbasetype-element.md) element.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4225a-125">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4225a-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4225a-126">Gatilhos de tarefa</span><span class="sxs-lookup"><span data-stu-id="4225a-126">Task Triggers</span></span>](task-triggers.md)
</dt> </dl>

 

 




