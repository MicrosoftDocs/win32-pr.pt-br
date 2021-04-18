---
title: Sobre o Agendador de Tarefas
description: O serviço Agendador de Tarefas permite que você execute tarefas automatizadas em um computador escolhido.
ms.assetid: 13816b8b-3090-4d17-86bb-8e632ca0cd37
keywords:
- Agendador de Tarefas Agendador de Tarefas, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6022546550efe32504dd0a3d12c94163e78214f6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105760321"
---
# <a name="about-the-task-scheduler"></a>Sobre o Agendador de Tarefas

O serviço Agendador de Tarefas permite que você execute tarefas automatizadas em um computador escolhido. Com esse serviço, você pode agendar qualquer programa para ser executado em um horário conveniente para você ou quando ocorrer um evento específico. O Agendador de Tarefas monitora os critérios de tempo ou de evento que você escolhe e executa a tarefa quando esses critérios são atendidos.

## <a name="where-task-scheduler-is-installed"></a>Onde o Agendador de Tarefas está instalado

O Agendador de Tarefas é instalado automaticamente com vários sistemas operacionais da Microsoft.

O Agendador de Tarefas 1,0 é instalado com os sistemas operacionais Windows Server 2003, Windows XP e Windows 2000.

O Agendador de Tarefas 2,0 é instalado com o Windows Vista e o Windows Server 2008.

A API Agendador de Tarefas 2,0 deve ser usada no desenvolvimento de aplicativos que usam o serviço Agendador de Tarefas no Windows Vista. Para obter mais informações, consulte [referência de Agendador de tarefas](task-scheduler-reference.md).

Agendador de Tarefas é iniciado toda vez que o sistema operacional é iniciado. Ele pode ser executado por meio da GUI (interface gráfica do usuário) do Agendador de Tarefas ou por meio da API do Agendador de Tarefas descrita neste SDK.

## <a name="information-about-tasks"></a>Informações sobre tarefas

As tarefas são o componente principal do Agendador de Tarefas. Para obter informações sobre quais tarefas são e quais são seus componentes, consulte os seguintes tópicos:

-   [Tarefas](tasks.md)
-   [Ações de tarefas](task-actions.md)
-   [Gatilhos de tarefa](task-triggers.md)
-   [Informações de registro da tarefa](task-registration-information.md)
-   [Condições de ociosidade da tarefa](task-idle-conditions.md)
-   [Contextos de segurança para tarefas](security-contexts-for-running-tasks.md)
-   [Repetindo uma tarefa](repeating-a-task.md)
-   [Manutenção automática](task-maintenence.md)

Para obter mais informações e exemplos sobre como usar as interfaces de Agendador de Tarefas, os objetos de script e o XML, consulte [usando o Agendador de tarefas](using-the-task-scheduler.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Agendador de Tarefas](task-scheduler-start-page.md)
</dt> </dl>

 

 




