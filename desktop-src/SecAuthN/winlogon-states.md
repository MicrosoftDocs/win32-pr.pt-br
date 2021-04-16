---
description: O Winlogon mantém o estado da estação de trabalho usado pela GINA para determinar quais ações de autenticação são necessárias.
ms.assetid: e04175c4-bb43-4f76-8ceb-50282a1ebed0
title: Estados do Winlogon
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4d2e4ec690d6bdda15fb8e350969b36e01d5c68
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104563632"
---
# <a name="winlogon-states"></a>Estados do Winlogon

O [*Winlogon*](../secgloss/w-gly.md) mantém o estado da estação de trabalho usado pela [*Gina*](../secgloss/g-gly.md) para determinar quais ações de autenticação são necessárias.

Em qualquer ponto no tempo, o Winlogon está em um dos três Estados:

-   [Estado desconectado](#logged-off-state)
-   [Estado conectado](#logged-on-state)
-   [Estado bloqueado da estação de trabalho](#workstation-locked-state)

Esses três Estados são mostrados na ilustração a seguir.

![Estados do Winlogon](images/winlogonst.png)

## <a name="logged-off-state"></a>Estado de Logged-Off

Quando o Winlogon está no estado conectado, os usuários são solicitados a se identificar e fornecer informações de autenticação. Se um usuário fornecer informações de conta de usuário corretas e nenhuma restrição impedir, o usuário está conectado e um programa shell (como o Windows Explorer) é executado no aplicativo desktop. O Winlogon muda para o estado conectado.

## <a name="logged-on-state"></a>Estado de Logged-On

Quando o Winlogon está no estado conectado, os usuários podem interagir com o Shell, ativar aplicativos adicionais e fazer seu trabalho. Do estado conectado, os usuários podem parar todo o trabalho e fazer logoff ou bloquear suas estações (deixando todo o trabalho em vigor). Se o usuário decidir fazer logoff, o Winlogon encerrará todos os processos associados a essa [*sessão de logon*](../secgloss/l-gly.md) e a estação de trabalho estará disponível para outro usuário. Se, em vez disso, o usuário decidir bloquear a estação de trabalho, o Winlogon será alterado para o estado bloqueado da estação de trabalho.

## <a name="workstation-locked-state"></a>Estado de Workstation-Locked

Quando o Winlogon está no estado de bloqueio de estação de trabalho, uma área de segurança segura é exibida até que o usuário desbloqueie a Workstation fornecendo a mesma identificação e informações de autenticação que o usuário que originalmente fez logon ou até que um administrador Force um logoff. Se a estação de trabalho estiver desbloqueada, o aplicativo desktop será exibido e o trabalho poderá ser retomado. No entanto, se um administrador desbloquear a estação de trabalho (fornecendo as informações de identificação e autenticação de uma conta de administrador), os processos do usuário conectado serão encerrados e o Winlogon será alterado para o estado desconectado.

Várias ações diferentes podem ser executadas em cada um dos Estados do Winlogon. Uma DLL GINA pode implementar ações que não fazem parte do sistema operacional Windows padrão. Por exemplo, um sistema de alta segurança pode bloquear automaticamente uma estação de trabalho a cada 10 minutos e forçar os usuários a se autenticarem.

Para obter informações sobre como criar áreas de trabalho e registrar uma [*seqüência de atenção segura*](../secgloss/s-gly.md) (SAS), consulte [inicializando o Winlogon](initializing-winlogon.md). Para obter informações sobre operações de tempo limite, consulte [suporte para operações de tempo de serviço de caixa de diálogo](supported-dialog-box-service-time-out-operations.md). Para obter informações sobre como enviar mensagens para a GINA enquanto uma caixa de diálogo é exibida, consulte [enviando mensagens para a Gina](sending-messages-to-the-gina.md). Para obter informações sobre as funções de suporte, consulte [funções de suporte do Winlogon](authentication-functions.md).

 

 
