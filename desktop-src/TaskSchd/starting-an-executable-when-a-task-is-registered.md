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
# <a name="starting-an-executable-when-a-task-is-registered"></a>Iniciando um executável quando uma tarefa é registrada

A gravação de uma tarefa que inicia um executável quando uma tarefa é registrada é feita pela definição de um gatilho de registro e uma ação executável.

## <a name="registration-trigger"></a>Gatilho de registro

Os gatilhos de registro iniciam uma tarefa assim que ela é registrada. Você também pode especificar um atraso para o gatilho de registro, que inicia uma tarefa após uma quantidade específica de tempo (o atraso) depois que a tarefa é registrada. O atraso é especificado na propriedade [**Delay**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationtrigger-get_delay) da interface [**IRegistrationTrigger**](/windows/desktop/api/taskschd/nn-taskschd-iregistrationtrigger) ([**RegistrationTrigger**](registrationtrigger.md) para scripts).

> [!Note]  
> Quando uma tarefa com um gatilho de registro é atualizada, a tarefa será executada Depois que a atualização ocorrer.

 

## <a name="registration-trigger-examples"></a>Exemplos de gatilho de registro

Os exemplos a seguir iniciam o bloco de notas quando uma tarefa é registrada:

-   [Exemplo de gatilho de registro (script)](registration-trigger-example--scripting-.md)
-   [Exemplo de gatilho de registro (C++)](registration-trigger-example--c---.md)
-   [Exemplo de gatilho de registro (XML)](registration-trigger-example--xml-.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando o Agendador de Tarefas](using-the-task-scheduler.md)
</dt> </dl>

 

 




