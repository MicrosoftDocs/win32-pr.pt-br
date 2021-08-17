---
description: Os contextos de ativação são visíveis em todo o processo.
ms.assetid: 6eda00d5-9dac-4267-bf61-b481814201f8
title: Threads, procedimentos assíncronos e mensagens de janela
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 529be75a3bc72679f44dfb69196f9487aa4f1de4f3cdbeada4ec89e26f05d646
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119141699"
---
# <a name="using-threads-asynchronous-procedures-and-window-messages"></a>Usando threads, procedimentos assíncronos e mensagens de janela

Os contextos de ativação são visíveis em todo o processo. No entanto, as pilhas de contexto de ativação são por thread e dois threads no mesmo processo podem ter pilhas de ativação diferentes. [**CreateThread**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createthread) coloca automaticamente o contexto de ativação atual na parte superior da pilha de ativação do novo thread. Isso pode facilitar a atualização do código existente para usar componentes lado a lado porque o novo thread pode ser executado imediatamente no contexto de ativação atual.

Chamadas de procedimento assíncrono, retornos de chamada de porta de conclusão e quaisquer outros retornos de chamada em outros threads automaticamente obterão o contexto de ativação da origem. Quando o retorno de chamada é chamado, a pilha de ativação é limpa. Isso significa que seu aplicativo pode usar chamadas de procedimento assíncrono e retornos de chamada sem ativar explicitamente nenhum contexto, pois o gerenciamento de contexto será feito pela infraestrutura subjacente lado a lado. Para tornar outros contextos ativos durante um retorno de chamada ou um novo thread, seu aplicativo pode fazer seu próprio gerenciamento de contexto. Nesse caso, seu programa deve usar a sequência adequada de funções de ativação de contexto de ativação e desativar funções.

Os contextos de ativação são neutros por thread. Ativar um contexto altera apenas a pilha do thread atual e você não pode ativar um contexto entre threads. O thread A não pode forçar um contexto no thread B. As funções da API de contexto de ativação também têm conhecimento de threading.

Quando você usa [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) ou [**PostMessage**](/windows/win32/api/winuser/nf-winuser-postmessagea) para enviar uma mensagem de janela para outro procedimento de janela em seu processo, o contexto de ativação atual é ativado antes que a mensagem seja passada para o procedimento de destino. O contexto de ativação atual acompanha a mensagem. Isso garante que as mensagens que se referem a objetos COM, nomes de DLL ou outros recursos lado a lado retêm suas informações de contexto corretas.

 

 
