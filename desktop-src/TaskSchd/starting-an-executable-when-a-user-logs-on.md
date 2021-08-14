---
title: Iniciando um executável quando um usuário faz login
description: Escrever uma tarefa que inicia um executável quando um usuário faz logon é feito definindo um gatilho de logon e uma ação executável.
ms.assetid: 0c5912aa-913d-42ce-a01b-b1359b49bb2f
keywords:
- Agendador de Tarefas exemplos Agendador de Tarefas , gatilho de logon
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5bd7cfc8412e33df47841cf33d2a4950061d39d77fbe76d3b896b5d220b04b8a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118132118"
---
# <a name="starting-an-executable-when-a-user-logs-on"></a>Iniciando um executável quando um usuário faz login

Escrever uma tarefa que inicia um executável quando um usuário faz logon é feito definindo um gatilho de logon e uma ação executável.

## <a name="logon-trigger"></a>Gatilho de logon

Os gatilhos de logon são ativados pelo limite inicial, mas não iniciam o executável até que um usuário especificado faça logon. Você pode especificar o gatilho de logon para iniciar quando um determinado usuário faz logon especificando o usuário na propriedade [**UserId**](/windows/desktop/api/taskschd/nf-taskschd-ilogontrigger-get_userid) da interface [**ILogonTrigger**](/windows/desktop/api/taskschd/nn-taskschd-ilogontrigger) ([**LogonTrigger**](logontrigger.md) para script).

## <a name="logontrigger-examples"></a>Exemplos de LogonTrigger

Os exemplos a seguir começam Bloco de notas depois que um usuário faz logo on.

-   [Exemplo de gatilho de logon (script)](logon-trigger-example--scripting-.md)
-   [Exemplo de gatilho de logon (C++)](logon-trigger-example--c---.md)
-   [Exemplo de gatilho de logon (XML)](logon-trigger-example--xml-.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando o Agendador de Tarefas](using-the-task-scheduler.md)
</dt> </dl>

 

 




