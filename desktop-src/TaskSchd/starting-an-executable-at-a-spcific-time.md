---
title: Iniciando um executável em um horário específico
description: Escrever uma tarefa que inicia um executável em um horário específico é feito definindo um gatilho de tempo e uma ação executável.
ms.assetid: a45a403d-5a54-4648-b517-41e01a0745c9
keywords:
- Exemplos de Agendador de Tarefas Agendador de Tarefas, gatilho de tempo
- Exemplos de Agendador de Tarefas Agendador de Tarefas, iniciando um executável
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62276568f7c626935d8c5c518d51f58ad0a58b5c313e780ec5651067af625068
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119059954"
---
# <a name="starting-an-executable-at-a-specific-time"></a>Iniciando um executável em um horário específico

Escrever uma tarefa que inicia um executável em um horário específico é feito definindo um gatilho de tempo e uma ação executável.

## <a name="start-boundary"></a>Limite de início

É importante observar que um gatilho de tempo é diferente de outros gatilhos baseados em tempo, pois é acionado quando o gatilho é ativado por seu limite inicial. Outros gatilhos baseados em tempo são ativados pelo limite inicial, mas não começam a executar suas ações (nesse caso, iniciando um executável) até que uma data agendada seja atingida.

## <a name="time-trigger-examples"></a>Exemplos de gatilho de tempo

os exemplos a seguir iniciam Bloco de notas 30 segundos depois que a tarefa é ativada:

-   [Exemplo de gatilho de tempo (C++)](time-trigger-example--c---.md)
-   [Exemplo de gatilho de tempo (script)](time-trigger-example--scripting-.md)
-   [Exemplo de gatilho de tempo (XML)](time-trigger-example--xml-.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando o Agendador de Tarefas](using-the-task-scheduler.md)
</dt> </dl>

 

 




