---
description: Um aplicativo em execução como um usuário padrão executa operações que exigem privilégio de administrador iniciando uma tarefa agendada.
ms.assetid: cd7485b3-6be5-4163-9a86-7892dbc59181
title: Modelo de tarefa com elevação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08aa485c47983760cc260a97cb52b58316a0d87bd4083d3ed09e72032f8fc7a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119672316"
---
# <a name="elevated-task-model"></a>Modelo de tarefa com elevação

No modelo de tarefa com privilégios elevados, um aplicativo em execução como um usuário padrão executa operações que exigem privilégio de administrador iniciando uma tarefa agendada.

**Windows Server 2003 e Windows XP:** Não há suporte para o modelo de tarefa com elevação.

As tarefas não consomem tantos recursos do sistema quanto serviços e as tarefas são automaticamente próximas quando concluídas. Considere usar esse modelo em vez do Modelo de [Serviço do Sistema](operating-system-service-model.md) Operacional, a menos que seja necessária compatibilidade com versões anteriores com sistemas operacionais anteriores.

Para usar uma tarefa para executar operações privilegiadas para um aplicativo de usuário padrão, as seguintes condições devem ser atendidas:

-   A tarefa deve ser definida para ser executado como **SYSTEM**.
-   O [*descritor de segurança*](/windows/desktop/SecGloss/s-gly) associado à tarefa deve ser configurado para permitir que os usuários padrão iniciem a tarefa.
-   O serviço agendador de tarefas deve estar em execução.

Para obter informações sobre como criar e iniciar tarefas, [consulte Agendador de Tarefas](/windows/desktop/TaskSchd/task-scheduler-start-page).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Desenvolvendo aplicativos que exigem privilégios de administrador](developing-applications-that-require-administrator-privilege.md)
</dt> <dt>

[Modelo do Agente de Administrador](administrator-broker-model.md)
</dt> <dt>

[Modelo de objeto COM do administrador](administrator-com-object-model.md)
</dt> <dt>

[Modelo de serviço do sistema operacional](operating-system-service-model.md)
</dt> </dl>

 

 
