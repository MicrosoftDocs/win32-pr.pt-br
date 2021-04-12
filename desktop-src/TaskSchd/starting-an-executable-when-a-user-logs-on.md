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
# <a name="starting-an-executable-when-a-user-logs-on"></a>Iniciando um executável quando um usuário faz logon

Gravar uma tarefa que inicia um executável quando um usuário faz logon é feito definindo um gatilho de logon e uma ação executável.

## <a name="logon-trigger"></a>Gatilho de logon

Os gatilhos de logon são ativados pelo limite inicial, mas não iniciam o executável até que um usuário especificado faça logon. Você pode especificar o gatilho de logon para iniciar quando um determinado usuário fizer logon especificando o usuário na propriedade [**userid**](/windows/desktop/api/taskschd/nf-taskschd-ilogontrigger-get_userid) da interface [**ILogonTrigger**](/windows/desktop/api/taskschd/nn-taskschd-ilogontrigger) ([**LogonTrigger**](logontrigger.md) para scripts).

## <a name="logontrigger-examples"></a>Exemplos de LogonTrigger

Os exemplos a seguir iniciam o bloco de notas depois que um usuário faz logon.

-   [Exemplo de gatilho de logon (script)](logon-trigger-example--scripting-.md)
-   [Exemplo de gatilho de logon (C++)](logon-trigger-example--c---.md)
-   [Exemplo de gatilho de logon (XML)](logon-trigger-example--xml-.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando o Agendador de Tarefas](using-the-task-scheduler.md)
</dt> </dl>

 

 




