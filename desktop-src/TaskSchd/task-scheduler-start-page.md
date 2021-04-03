---
title: Agendador de Tarefas para desenvolvedores
description: O Agendador de Tarefas permite que você execute automaticamente tarefas rotineiras em um computador escolhido. Agendador de Tarefas faz isso monitorando quaisquer critérios que você escolher (chamados de gatilhos) e executando as tarefas quando esses critérios forem atendidos.
ms.assetid: 15970a51-c139-48b8-b82b-605728d0f386
keywords:
- Agendador de Tarefas para desenvolvedores
- Agendador de Tarefas para desenvolvimento
- Desenvolvendo com Agendador de Tarefas
- Agendador de Tarefas, página do portal
ms.topic: article
ms.date: 10/18/2019
ms.openlocfilehash: dfbfb76145e38003e7c501b98c817f4aaca3ff09
ms.sourcegitcommit: 087843ef08ddcd8bce9ed647b610035925da2b3e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/19/2019
ms.locfileid: "104084135"
---
# <a name="task-scheduler-for-developers"></a>Agendador de Tarefas para desenvolvedores

> [!IMPORTANT]
> Este tópico e os outros tópicos desta seção são para um público de desenvolvedor. Se você estiver querendo usar o componente de Agendador de Tarefas em sua capacidade como administrador ou um profissional de ti, consulte [Agendador de tarefas](/dynamics365/business-central/dev-itpro/developer/devenv-task-scheduler).

## <a name="about-the-task-scheduler"></a>Sobre o Agendador de Tarefas

O Agendador de Tarefas permite que você execute automaticamente tarefas rotineiras em um computador escolhido. Agendador de Tarefas faz isso monitorando quaisquer critérios que você escolher (chamados de gatilhos) e executando as tarefas quando esses critérios forem atendidos.

Você pode usar o Agendador de Tarefas para executar tarefas como iniciar um aplicativo, enviar uma mensagem de email ou mostrar uma caixa de mensagem. As tarefas podem ser agendadas para serem executadas em resposta a esses eventos ou gatilhos. 

- Quando ocorre um evento de sistema específico.
- Em um momento específico.
- Em um horário específico em um agendamento diário.
- Em um horário específico em um cronograma semanal.
- Em um horário específico em um agendamento mensal.
- Em um horário específico em uma agenda mensal de dia da semana.
- Quando o computador entra em um estado ocioso.
- Quando a tarefa é registrada.
- Quando o sistema é inicializado.
- Quando um usuário faz logon.
- Quando uma sessão de Terminal Server muda de estado.

## <a name="developers"></a>Desenvolvedores

O Agendador de Tarefas fornece APIs nesses formulários.

- Agendador de Tarefas 2,0: interfaces e objetos são fornecidos para C++ e para desenvolvimento de scripts, respectivamente.
- Agendador de Tarefas 1,0: as interfaces são fornecidas para desenvolvimento em C++.

## <a name="run-time-requirements"></a>Requisitos de tempo de execução

O Agendador de Tarefas requer os seguintes sistemas operacionais.

- Agendador de Tarefas 2,0: o cliente requer o Windows Vista ou superior. O servidor requer o Windows Server 2008 ou superior.
- Agendador de Tarefas 1,0: o cliente requer o Windows Vista ou o Windows XP. O servidor requer o Windows Server 2008 ou o Windows Server 2003.

## <a name="in-this-section"></a>Nesta seção

| Tópico | Descrição |
|-|-|
| [O que há de novo no Agendador de Tarefas](what-s-new-in-task-scheduler.md) | Resumo da nova funcionalidade introduzida pelo Agendador de Tarefas. |
| [Sobre o Agendador de Tarefas](about-the-task-scheduler.md) | Informações conceituais gerais sobre a API de Agendador de Tarefas. |
| [Usando o Agendador de Tarefas](using-the-task-scheduler.md) | Exemplos de código que mostram como usar as APIs de Agendador de Tarefas. |
| [Referência de Agendador de Tarefas](task-scheduler-reference.md) | Informações de referência detalhadas para APIs de Agendador de Tarefas e o esquema de Agendador de Tarefas. |