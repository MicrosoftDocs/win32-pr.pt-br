---
description: Um aplicativo em execução como um usuário padrão executa operações que exigem privilégios de administrador, iniciando uma tarefa agendada.
ms.assetid: cd7485b3-6be5-4163-9a86-7892dbc59181
title: Modelo de tarefa elevada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27006e32210cfea05de5c2b3b9adf36613dc4f5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297435"
---
# <a name="elevated-task-model"></a>Modelo de tarefa elevada

No modelo de tarefa com privilégios elevados, um aplicativo em execução como usuário padrão executa operações que exigem privilégios de administrador, iniciando uma tarefa agendada.

**Windows Server 2003 e Windows XP:** Não há suporte para o modelo de tarefa privilegiada.

As tarefas não consomem tantos recursos do sistema como serviços, e as tarefas são fechadas automaticamente quando terminarem. Considere o uso desse modelo em vez do [modelo de serviço do sistema operacional](operating-system-service-model.md) , a menos que a compatibilidade com versões anteriores dos sistemas operacionais sejam necessárias.

Para usar uma tarefa para executar operações privilegiadas para um aplicativo de usuário padrão, as seguintes condições devem ser atendidas:

-   A tarefa deve ser definida para executar como **sistema**.
-   O [*descritor de segurança*](/windows/desktop/SecGloss/s-gly) associado à tarefa deve ser configurado para permitir que usuários padrão iniciem a tarefa.
-   O serviço Agendador de tarefas deve estar em execução.

Para obter informações sobre como criar e iniciar tarefas, consulte [Agendador de tarefas](/windows/desktop/TaskSchd/task-scheduler-start-page).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Desenvolvendo aplicativos que exigem privilégios de administrador](developing-applications-that-require-administrator-privilege.md)
</dt> <dt>

[Modelo de agente do administrador](administrator-broker-model.md)
</dt> <dt>

[Modelo de objeto COM do administrador](administrator-com-object-model.md)
</dt> <dt>

[Modelo de serviço do sistema operacional](operating-system-service-model.md)
</dt> </dl>

 

 
