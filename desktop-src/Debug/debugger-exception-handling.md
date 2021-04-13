---
description: A manipulação do sistema de exceções de modo de usuário fornece suporte para depuradores sofisticados.
ms.assetid: c45a7dc6-e6b2-4fc4-9522-12d96893f4c7
title: Manipulação de exceção do depurador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6aff6d566e8798aaf4f3113ce6d8f44a3bc71ba
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104456880"
---
# <a name="debugger-exception-handling"></a>Manipulação de exceção do depurador

A manipulação do sistema de exceções de modo de usuário fornece suporte para depuradores sofisticados. Se o processo no qual ocorre uma exceção estiver sendo depurado, o sistema gerará um evento de depuração. Se o depurador estiver usando a função [**WaitForDebugEvent**](/windows/win32/api/debugapi/nf-debugapi-waitfordebugevent) , o evento Debug fará com que essa função retorne com um ponteiro para uma estrutura de [**\_ eventos de depuração**](/windows/win32/api/minwinbase/ns-minwinbase-debug_event) . Essa estrutura contém o processo e os identificadores de thread que o depurador pode usar para acessar o registro de contexto do thread. A estrutura também contém uma estrutura de [**\_ \_ informações de depuração de exceção**](/windows/win32/api/minwinbase/ns-minwinbase-exception_debug_info) que inclui uma cópia do registro de exceção.

Quando o sistema está procurando um manipulador de exceção, ele faz duas tentativas de notificar o depurador de um processo. A primeira tentativa de notificação fornece ao depurador uma oportunidade para manipular o ponto de interrupção ou exceções de etapa única. Isso é conhecido como *notificação de primeira chance*. O usuário pode emitir comandos do depurador para manipular o ambiente do processo antes de qualquer manipulador de exceção ser executado. A segunda tentativa de notificar o depurador ocorrerá somente se o sistema não conseguir encontrar um manipulador de exceção baseado em quadro que manipule a exceção. Isso é conhecido como *notificação de última chance*. Se o depurador não tratar a exceção após a notificação de última chance, o sistema encerrará o processo que está sendo depurado.

Em cada tentativa de notificação, o depurador usa a função [**ContinueDebugEvent**](/windows/win32/api/debugapi/nf-debugapi-continuedebugevent) para retornar o controle ao sistema. Antes de retornar o controle, o depurador pode manipular a exceção e modificar o estado do thread conforme apropriado ou pode optar por não lidar com a exceção. Usando **ContinueDebugEvent**, o depurador pode indicar que ele tratou a exceção; nesse caso, o estado da máquina é restaurado e a execução do thread continua no ponto em que a exceção ocorreu. O depurador também pode indicar que ele não trata a exceção, o que faz com que o sistema continue sua pesquisa por um manipulador de exceção.

 

 
