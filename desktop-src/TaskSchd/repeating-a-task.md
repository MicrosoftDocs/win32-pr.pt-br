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
# <a name="repeating-a-task"></a>Repetindo uma tarefa

Agendador de Tarefas pode executar uma tarefa quantas vezes forem disparadas após um gatilho ser acionado. Para fazer isso, o gatilho define um padrão de repetição que informa Agendador de Tarefas por quanto tempo ele deve continuar a repetir a tarefa e o intervalo de tempo entre cada repetição de tarefa.

## <a name="repetition-pattern"></a>Padrão de repetição

A ilustração a seguir mostra um padrão de repetição com uma duração de 60 minutos e um intervalo de 25 minutos. Lembre-se de que, nesse caso, Agendador de Tarefas executa a tarefa quando o gatilho é acionado, ele executa a tarefa novamente após 25 minutos e, em seguida, executa a tarefa novamente após 50 minutos, dependendo da configuração da [**Propriedade StopAtDurationEnd de IRepetitionPattern**](/windows/desktop/api/taskschd/nf-taskschd-irepetitionpattern-get_stopatdurationend) ([**RepetitionPattern. StopAtDurationEnd**](repetitionpattern-stopatdurationend.md) para scripts). Se a propriedade **StopAtDurationEnd** for definida como True, Agendador de tarefas interromperá a última instância da tarefa se ela ainda estiver em execução após 60 minutos. Se a propriedade **StopAtDurationEnd** for definida como false, a última instância da tarefa será executada, independentemente da duração.

![padrão de repetição de gatilho](images/repetition-pattern.png)

Se você registrar uma tarefa que contém um gatilho com um intervalo de repetição igual a um minuto e uma duração de repetição igual a quatro minutos, a tarefa será iniciada cinco vezes. As cinco repetições podem ser definidas pelo seguinte padrão:

1.  Uma tarefa é iniciada no início do primeiro minuto.
2.  A próxima tarefa é iniciada no final do primeiro minuto.
3.  A próxima tarefa é iniciada no final do segundo minuto.
4.  A próxima tarefa começa no final do terceiro minuto.
5.  A próxima tarefa é iniciada no final do quarto minuto.

**Windows Server 2003, Windows XP e windows 2000:** Se você registrar uma tarefa que contém um gatilho com um intervalo de repetição igual a um minuto e uma duração de repetição igual a quatro minutos, a tarefa será iniciada quatro vezes.

## <a name="objects-interfaces-and-xml-elements"></a>Objetos, interfaces e elementos XML

Para o desenvolvimento de scripts, o padrão de repetição é definido usando o objeto [**RepetitionPattern**](repetitionpattern.md) .

Para o desenvolvimento em C++, o padrão de repetição é definido pela interface [**IRepetitionPattern**](/windows/desktop/api/taskschd/nn-taskschd-irepetitionpattern) .

Ao ler ou gravar XML para uma tarefa, o padrão de repetição é especificado no elemento de [**repetição**](taskschedulerschema-repetition-triggerbasetype-element.md) .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Gatilhos de tarefa](task-triggers.md)
</dt> </dl>

 

 




