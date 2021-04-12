---
title: Iniciando um executável quando um usuário faz logon
description: Gravar uma tarefa que inicia um executável quando um usuário faz logon é feito definindo um gatilho de logon e uma ação executável.
ms.assetid: 0c5912aa-913d-42ce-a01b-b1359b49bb2f
keywords:
- Exemplos de Agendador de Tarefas Agendador de Tarefas, gatilho de logon
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ffa758546dbd08b6ccf27412f38891589cb9643
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104363643"
---
# <a name="starting-an-executable-when-a-user-logs-on"></a><span data-ttu-id="f08ef-104">Iniciando um executável quando um usuário faz logon</span><span class="sxs-lookup"><span data-stu-id="f08ef-104">Starting an Executable When a User Logs On</span></span>

<span data-ttu-id="f08ef-105">Gravar uma tarefa que inicia um executável quando um usuário faz logon é feito definindo um gatilho de logon e uma ação executável.</span><span class="sxs-lookup"><span data-stu-id="f08ef-105">Writing a task that starts an executable when a user logs on is done by defining a logon trigger and an executable action.</span></span>

## <a name="logon-trigger"></a><span data-ttu-id="f08ef-106">Gatilho de logon</span><span class="sxs-lookup"><span data-stu-id="f08ef-106">Logon Trigger</span></span>

<span data-ttu-id="f08ef-107">Os gatilhos de logon são ativados pelo limite inicial, mas não iniciam o executável até que um usuário especificado faça logon.</span><span class="sxs-lookup"><span data-stu-id="f08ef-107">Logon triggers are activated by their start boundary but they do not start the executable until a specified user logs on.</span></span> <span data-ttu-id="f08ef-108">Você pode especificar o gatilho de logon para iniciar quando um determinado usuário fizer logon especificando o usuário na propriedade [**userid**](/windows/desktop/api/taskschd/nf-taskschd-ilogontrigger-get_userid) da interface [**ILogonTrigger**](/windows/desktop/api/taskschd/nn-taskschd-ilogontrigger) ([**LogonTrigger**](logontrigger.md) para scripts).</span><span class="sxs-lookup"><span data-stu-id="f08ef-108">You can specify the logon trigger to start when a certain user logs on by specifying the user in the [**UserId**](/windows/desktop/api/taskschd/nf-taskschd-ilogontrigger-get_userid) property of the [**ILogonTrigger**](/windows/desktop/api/taskschd/nn-taskschd-ilogontrigger) interface ([**LogonTrigger**](logontrigger.md) for scripting).</span></span>

## <a name="logontrigger-examples"></a><span data-ttu-id="f08ef-109">Exemplos de LogonTrigger</span><span class="sxs-lookup"><span data-stu-id="f08ef-109">LogonTrigger Examples</span></span>

<span data-ttu-id="f08ef-110">Os exemplos a seguir iniciam o bloco de notas depois que um usuário faz logon.</span><span class="sxs-lookup"><span data-stu-id="f08ef-110">The following examples start Notepad after a user logs on.</span></span>

-   [<span data-ttu-id="f08ef-111">Exemplo de gatilho de logon (script)</span><span class="sxs-lookup"><span data-stu-id="f08ef-111">Logon Trigger Example (Scripting)</span></span>](logon-trigger-example--scripting-.md)
-   [<span data-ttu-id="f08ef-112">Exemplo de gatilho de logon (C++)</span><span class="sxs-lookup"><span data-stu-id="f08ef-112">Logon Trigger Example (C++)</span></span>](logon-trigger-example--c---.md)
-   [<span data-ttu-id="f08ef-113">Exemplo de gatilho de logon (XML)</span><span class="sxs-lookup"><span data-stu-id="f08ef-113">Logon Trigger Example (XML)</span></span>](logon-trigger-example--xml-.md)

## <a name="related-topics"></a><span data-ttu-id="f08ef-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f08ef-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f08ef-115">Usando o Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="f08ef-115">Using the Task Scheduler</span></span>](using-the-task-scheduler.md)
</dt> </dl>

 

 




