---
title: Iniciando um executável quando uma tarefa é registrada
description: A gravação de uma tarefa que inicia um executável quando uma tarefa é registrada é feita pela definição de um gatilho de registro e uma ação executável.
ms.assetid: 426fa79d-7f0d-42fb-a8c4-15981d13be71
keywords:
- Exemplos de Agendador de Tarefas Agendador de Tarefas, gatilho de registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8036b8bdff807ded582279e0ba7675bc2160811
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916385"
---
# <a name="starting-an-executable-when-a-task-is-registered"></a><span data-ttu-id="7a41d-104">Iniciando um executável quando uma tarefa é registrada</span><span class="sxs-lookup"><span data-stu-id="7a41d-104">Starting an Executable When a Task is Registered</span></span>

<span data-ttu-id="7a41d-105">A gravação de uma tarefa que inicia um executável quando uma tarefa é registrada é feita pela definição de um gatilho de registro e uma ação executável.</span><span class="sxs-lookup"><span data-stu-id="7a41d-105">Writing a task that starts an executable when a task is registered is done by defining a registration trigger and an executable action.</span></span>

## <a name="registration-trigger"></a><span data-ttu-id="7a41d-106">Gatilho de registro</span><span class="sxs-lookup"><span data-stu-id="7a41d-106">Registration Trigger</span></span>

<span data-ttu-id="7a41d-107">Os gatilhos de registro iniciam uma tarefa assim que ela é registrada.</span><span class="sxs-lookup"><span data-stu-id="7a41d-107">Registration triggers start a task as soon as it is registered.</span></span> <span data-ttu-id="7a41d-108">Você também pode especificar um atraso para o gatilho de registro, que inicia uma tarefa após uma quantidade específica de tempo (o atraso) depois que a tarefa é registrada.</span><span class="sxs-lookup"><span data-stu-id="7a41d-108">You can also specify a delay for the registration trigger, which starts a task after a specific amount of time (the delay) after the task is registered.</span></span> <span data-ttu-id="7a41d-109">O atraso é especificado na propriedade [**Delay**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationtrigger-get_delay) da interface [**IRegistrationTrigger**](/windows/desktop/api/taskschd/nn-taskschd-iregistrationtrigger) ([**RegistrationTrigger**](registrationtrigger.md) para scripts).</span><span class="sxs-lookup"><span data-stu-id="7a41d-109">The delay is specified in the [**Delay**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationtrigger-get_delay) property of the [**IRegistrationTrigger**](/windows/desktop/api/taskschd/nn-taskschd-iregistrationtrigger) interface ([**RegistrationTrigger**](registrationtrigger.md) for scripting).</span></span>

> [!Note]  
> <span data-ttu-id="7a41d-110">Quando uma tarefa com um gatilho de registro é atualizada, a tarefa será executada Depois que a atualização ocorrer.</span><span class="sxs-lookup"><span data-stu-id="7a41d-110">When a task with a registration trigger is updated, the task will execute after the update occurs.</span></span>

 

## <a name="registration-trigger-examples"></a><span data-ttu-id="7a41d-111">Exemplos de gatilho de registro</span><span class="sxs-lookup"><span data-stu-id="7a41d-111">Registration Trigger Examples</span></span>

<span data-ttu-id="7a41d-112">Os exemplos a seguir iniciam o bloco de notas quando uma tarefa é registrada:</span><span class="sxs-lookup"><span data-stu-id="7a41d-112">The following examples start Notepad when a task is registered:</span></span>

-   [<span data-ttu-id="7a41d-113">Exemplo de gatilho de registro (script)</span><span class="sxs-lookup"><span data-stu-id="7a41d-113">Registration Trigger Example (Scripting)</span></span>](registration-trigger-example--scripting-.md)
-   [<span data-ttu-id="7a41d-114">Exemplo de gatilho de registro (C++)</span><span class="sxs-lookup"><span data-stu-id="7a41d-114">Registration Trigger Example (C++)</span></span>](registration-trigger-example--c---.md)
-   [<span data-ttu-id="7a41d-115">Exemplo de gatilho de registro (XML)</span><span class="sxs-lookup"><span data-stu-id="7a41d-115">Registration Trigger Example (XML)</span></span>](registration-trigger-example--xml-.md)

## <a name="related-topics"></a><span data-ttu-id="7a41d-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7a41d-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7a41d-117">Usando o Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="7a41d-117">Using the Task Scheduler</span></span>](using-the-task-scheduler.md)
</dt> </dl>

 

 




