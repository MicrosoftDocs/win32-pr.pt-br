---
description: Os contextos de ativação são visíveis durante todo o processo.
ms.assetid: 6eda00d5-9dac-4267-bf61-b481814201f8
title: Threads, procedimentos assíncronos e mensagens de janela
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e615eb9795ba32bcf4bd227a4933e890e9b89055
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826994"
---
# <a name="using-threads-asynchronous-procedures-and-window-messages"></a>Usando threads, procedimentos assíncronos e mensagens de janela

Os contextos de ativação são visíveis durante todo o processo. As pilhas de contexto de ativação são, no entanto, por thread, e dois threads no mesmo processo podem ter diferentes pilhas de ativação. [**CreateThread**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createthread) coloca automaticamente o contexto de ativação atual na parte superior da pilha de ativação do novo thread. Isso pode facilitar a atualização do código existente para usar componentes lado a lado, pois o novo thread pode ser executado imediatamente no contexto de ativação atual.

Chamadas de procedimento assíncronos, retornos de chamada de porta de conclusão e quaisquer outros retornos de chamada em outros threads obtêm automaticamente o contexto de ativação da origem. Quando o retorno de chamada é chamado, a pilha de ativação é limpa. Isso significa que seu aplicativo pode usar chamadas de procedimento assíncronos e retornos de chamada sem ativar explicitamente quaisquer contextos porque o gerenciamento de contexto será feito pela infraestrutura lado a lado subjacente. Para fazer com que outros contextos sejam ativados durante um retorno de chamada ou novo thread, seu aplicativo pode fazer seu próprio gerenciamento de contexto. Nesse caso, o programa deve usar a sequência adequada de contexto de ativação ativar funções e desativar funções.

Os contextos de ativação são de thread neutro. Ativar um contexto apenas altera a pilha do thread atual e você não pode ativar um contexto entre threads. O thread A não pode forçar um contexto para o thread B. As funções da API de contexto de ativação também têm reconhecimento de Threading.

Quando você usa [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) ou a [**mensagem de ismessage**](/windows/win32/api/winuser/nf-winuser-postmessagea) para enviar uma mensagem de janela para outro procedimento de janela em seu processo, o contexto de ativação atual é ativado antes que a mensagem seja passada para o procedimento de destino. O contexto de ativação atual acompanha a mensagem. Isso garante que as mensagens que se referem a objetos COM, nomes de DLL ou outros recursos lado a lado retenham suas informações de contexto corretas.

 

 
