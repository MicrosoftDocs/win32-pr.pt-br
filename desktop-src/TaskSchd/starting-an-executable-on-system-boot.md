---
title: Iniciando um executável na inicialização do sistema
description: Escrever uma tarefa que inicia um executável quando um sistema é inicializado é feito definindo um gatilho de inicialização e uma ação executável.
ms.assetid: 9e2359df-a223-4a0c-9051-01b73a83c1f7
keywords:
- Exemplos de Agendador de Tarefas Agendador de Tarefas, gatilho de inicialização
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7d41c39e9c80d3fc8f14c0bc9b9d9305de38e16
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636594"
---
# <a name="starting-an-executable-on-system-boot"></a>Iniciando um executável na inicialização do sistema

Escrever uma tarefa que inicia um executável quando um sistema é inicializado é feito definindo um gatilho de inicialização e uma ação executável.

## <a name="boot-trigger"></a>Gatilho de inicialização

Os gatilhos de inicialização são ativados pelo limite inicial, mas não iniciam o executável até que o sistema seja inicializado. Você também pode especificar um tempo de atraso no gatilho de inicialização que especifica a quantidade de tempo entre o momento em que o sistema é inicializado e quando a tarefa é iniciada. Isso é definido pela propriedade [**Delay**](/windows/desktop/api/taskschd/nf-taskschd-iboottrigger-get_delay) na interface [**IBootTrigger**](/windows/desktop/api/taskschd/nn-taskschd-iboottrigger) (objeto [**BootTrigger**](boottrigger.md) para scripts).

## <a name="boot-trigger-examples"></a>Exemplos de gatilho de inicialização

Os exemplos a seguir iniciam o bloco de notas depois que o sistema é inicializado:

-   [Exemplo de gatilho de inicialização (script)](boot-trigger-example--scripting-.md)
-   [Exemplo de gatilho de inicialização (C++)](boot-trigger-example--c---.md)
-   [Exemplo de gatilho de inicialização (XML)](boot-trigger-example--xml-.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando o Agendador de Tarefas](using-the-task-scheduler.md)
</dt> </dl>

 

 




