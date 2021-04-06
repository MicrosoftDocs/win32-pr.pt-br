---
description: O gerenciamento de energia do Windows torna os computadores instantaneamente acessíveis aos usuários no toque de um botão ou chave.
ms.assetid: 388dadb9-b722-43f8-ab2b-a9bbd96600a3
title: Gerenciamento de energia do Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8abb3a040f8da8e2deb242a2aa607a9448d31c09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828362"
---
# <a name="windows-power-management"></a>Gerenciamento de energia do Windows

O gerenciamento de energia do Windows torna os computadores instantaneamente acessíveis aos usuários no toque de um botão ou chave. Ele também garante que todos os elementos do sistema — aplicativos, dispositivos e interface do usuário — possam aproveitar os vastos aprimoramentos na tecnologia e nos recursos de gerenciamento de energia.

O sistema operacional Windows usa o hardware de gerenciamento de energia para colocar o computador em um *estado de suspensão* de baixa energia em vez de desligar completamente, para que o sistema possa retomar rapidamente o trabalho. O sistema operacional entrará automaticamente no estado de suspensão quando o computador estiver ocioso ou quando o usuário pressionar um botão para indicar que a sessão de trabalho atual está acima. Para o usuário, o sistema parece estar desativado. Enquanto estiver no estado de suspensão, o processador do computador não está executando o código e nenhum trabalho está sendo realizado para o usuário. No entanto, os eventos no sistema de dispositivos de hardware e o relógio em tempo real podem ser habilitados para fazer com que o sistema saia do estado de suspensão (ou seja, "acordar") e retorne rapidamente ao estado de trabalho.

Quando o computador está no estado de suspensão, o hardware do computador, o sistema e os aplicativos em execução no computador devem ser capazes de responder imediatamente ao comutador de energia, eventos de comunicação e outras ações. Se todos os aplicativos manipulam as transições de estado de energia normalmente, o usuário vai perceber um sistema mais elegante e integrado. Os aplicativos que não tratam essas transições podem falhar quando a energia é desligada e depois, devido à perda de dados ou uma dependência em um dispositivo que pode ter sido removido.

Estes são os benefícios do gerenciamento de energia do Windows:

-   Elimina atrasos de inicialização e desligamento. O computador não precisa executar uma inicialização completa do sistema ao sair do estado de suspensão ou um desligamento completo do sistema quando o usuário inicia o estado de suspensão.
-   Permite que tarefas automatizadas sejam executadas enquanto o computador estiver no estado de suspensão. O Agendador de Tarefas permite que o usuário agende aplicativos para execução; os eventos agendados podem ser executados mesmo quando o sistema está no estado de suspensão. O Agendador de Tarefas usa [temporizadores de espera](/windows/desktop/Sync/waitable-timer-objects) para garantir que o sistema esteja pronto quando o aplicativo estiver agendado para execução. Para obter mais informações, consulte o arquivo de ajuda incluído no Agendador de Tarefas.
-   Habilita o gerenciamento de energia por dispositivo. Os dispositivos que não estão em uso podem economizar energia entrando no estado de suspensão.
-   Melhora a eficiência de energia. A eficiência de energia é particularmente importante em computadores portáteis. A redução do consumo de energia do sistema é convertida diretamente em custos de energia mais longos e vida útil da bateria.
-   Permite que os usuários criem [esquemas de energia](power-schemes.md), definam alarmes e especifiquem opções de bateria por meio do aplicativo opções de energia no painel de controle. O sistema operacional coordena todas as atividades de gerenciamento de energia, com base nas configurações de política de energia. Para obter mais informações, consulte o arquivo de ajuda incluído com o aplicativo de opções de energia.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre o gerenciamento de energia](about-power-management.md)
</dt> <dt>

[Agendador de Tarefas](/windows/desktop/TaskSchd/task-scheduler-start-page)
</dt> </dl>

 

 
