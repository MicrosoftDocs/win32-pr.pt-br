---
title: Sobre o Agendador de Tarefas
description: O Agendador de Tarefas serviço permite que você execute tarefas automatizadas em um computador escolhido.
ms.assetid: 13816b8b-3090-4d17-86bb-8e632ca0cd37
keywords:
- Agendador de Tarefas Agendador de Tarefas , sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dca865fe98ffb56f2bb6e9310e31d38bdaa804a63da07e486bbc89a0cd9ebcdf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120072706"
---
# <a name="about-the-task-scheduler"></a>Sobre o Agendador de Tarefas

O Agendador de Tarefas serviço permite que você execute tarefas automatizadas em um computador escolhido. Com esse serviço, você pode agendar qualquer programa para ser executado em um momento conveniente para você ou quando ocorrer um evento específico. O Agendador de Tarefas monitora o tempo ou os critérios de evento escolhidos e, em seguida, executa a tarefa quando esses critérios são atendidos.

## <a name="where-task-scheduler-is-installed"></a>Onde Agendador de Tarefas está instalado

O Agendador de Tarefas é instalado automaticamente com vários sistemas operacionais da Microsoft.

Agendador de Tarefas 1.0 é instalado com os sistemas operacionais Windows Server 2003, Windows XP e Windows 2000.

Agendador de Tarefas 2.0 é instalado com Windows Vista e Windows Server 2008.

A API Agendador de Tarefas 2.0 deve ser usada no desenvolvimento de aplicativos que usam o serviço Agendador de Tarefas no Windows Vista. Para obter mais informações, [consulte Agendador de Tarefas Referência de](task-scheduler-reference.md).

Agendador de Tarefas é iniciado sempre que o sistema operacional é iniciado. Ele pode ser executado por meio Agendador de Tarefas GUI (interface gráfica do usuário) ou por meio da API de Agendador de Tarefas descrita neste SDK.

## <a name="information-about-tasks"></a>Informações sobre tarefas

As tarefas são o componente principal do Agendador de Tarefas. Para obter informações sobre o que são tarefas e quais são seus componentes, consulte os seguintes tópicos:

-   [Tarefas](tasks.md)
-   [Ações de tarefa](task-actions.md)
-   [Gatilhos de tarefa](task-triggers.md)
-   [Informações de registro de tarefa](task-registration-information.md)
-   [Condições ociosas da tarefa](task-idle-conditions.md)
-   [Contextos de segurança para tarefas](security-contexts-for-running-tasks.md)
-   [Repetindo uma tarefa](repeating-a-task.md)
-   [Manutenção Automática](task-maintenence.md)

Para obter mais informações e exemplos sobre como usar as interfaces Agendador de Tarefas, objetos de script e XML, consulte Usando o [Agendador de Tarefas](using-the-task-scheduler.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Agendador de Tarefas](task-scheduler-start-page.md)
</dt> </dl>

 

 




