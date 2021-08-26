---
title: Iniciando um executável quando uma tarefa é registrada
description: A escrita de uma tarefa que inicia um executável quando uma tarefa é registrada é feita definindo um gatilho de registro e uma ação executável.
ms.assetid: 426fa79d-7f0d-42fb-a8c4-15981d13be71
keywords:
- Agendador de Tarefas exemplos Agendador de Tarefas , gatilho de registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6a051c820a1099828ae0ee123e4241ec42d6edbb23ce9e98275057b5903dfbc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120033946"
---
# <a name="starting-an-executable-when-a-task-is-registered"></a>Iniciando um executável quando uma tarefa é registrada

A escrita de uma tarefa que inicia um executável quando uma tarefa é registrada é feita definindo um gatilho de registro e uma ação executável.

## <a name="registration-trigger"></a>Gatilho de registro

Os gatilhos de registro iniciam uma tarefa assim que ela é registrada. Você também pode especificar um atraso para o gatilho de registro, que inicia uma tarefa após um período específico (o atraso) após o registro da tarefa. O atraso é especificado na propriedade [**Delay**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationtrigger-get_delay) da interface [**IRegistrationTrigger**](/windows/desktop/api/taskschd/nn-taskschd-iregistrationtrigger) ([**RegistrationTrigger**](registrationtrigger.md) para script).

> [!Note]  
> Quando uma tarefa com um gatilho de registro for atualizada, a tarefa será executada depois que a atualização ocorrer.

 

## <a name="registration-trigger-examples"></a>Exemplos de gatilho de registro

Os exemplos a seguir começam Bloco de notas quando uma tarefa é registrada:

-   [Exemplo de gatilho de registro (script)](registration-trigger-example--scripting-.md)
-   [Exemplo de gatilho de registro (C++)](registration-trigger-example--c---.md)
-   [Exemplo de gatilho de registro (XML)](registration-trigger-example--xml-.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando o Agendador de Tarefas](using-the-task-scheduler.md)
</dt> </dl>

 

 




