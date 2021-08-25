---
description: A WCT (Wait Chain Traversal) permite que os depuradores diagnostiquem travamentos e bloqueios do aplicativo.
ms.assetid: d266a663-b101-4936-9574-f6ce223419ae
title: Passagem de cadeia de espera
ms.topic: article
ms.date: 08/10/2020
ms.custom: contperf-fy21q1
ms.openlocfilehash: 695e5298d0f56d0c53afcd146b19b1fc3c6ccf25e4ec12aec7f2b6b74fb64243
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119912306"
---
# <a name="wait-chain-traversal"></a>Passagem de cadeia de espera

A WCT (Wait Chain Traversal) permite que os depuradores diagnostiquem travamentos e bloqueios do aplicativo.

Uma *cadeia de espera* é uma sequência alternada de threads e objetos de sincronização em que cada thread aguarda o objeto a seguir. Cada objeto a seguir é, por sua vez, de Propriedade do thread subsequente na cadeia.

Um thread aguarda um objeto de sincronização do momento em que o thread solicita o objeto até que o thread o tenha adquirido. Esse "bloqueio" pertence a um thread a partir do momento em que o thread o adquire, até que o thread o libere. Em outras palavras, quando o thread 1 está aguardando um bloqueio pertencente ao thread 2, o thread 1 é "aguardando" para o thread 2.

A WCT dá suporte aos seguintes primitivos de sincronização:

- [Chamada de procedimento local avançada (ALPC)](../etw/alpc.md)
- [COM (Component Object Model)](../com/the-component-object-model.md)
- [Seções críticas](../sync/critical-section-objects.md)
- [Mutexes](../sync/mutex-objects.md)
- [SendMessage](/windows/win32/api/winuser/nf-winuser-sendmessage)
- Operações de [espera](../sync/wait-functions.md) em [processos e threads](../procthread/processes-and-threads.md)

Para recuperar a cadeia de espera para um ou mais threads, crie uma sessão WCT usando as funções [OpenThreadWaitChainSession](/windows/desktop/api/Wct/nf-wct-openthreadwaitchainsession) e [GetThreadWaitChain](/windows/desktop/api/Wct/nf-wct-getthreadwaitchain) . As sessões WCT são representadas por um identificador do tipo **HWCT**.

## <a name="sessions-can-be-synchronous-or-asynchronous"></a>As sessões podem ser síncronas ou assíncronas

As sessões síncronas não podem ser canceladas e bloqueiam o thread de chamada até que uma cadeia de espera tenha sido recuperada.

As sessões assíncronas não bloqueiam o thread de chamada e podem ser canceladas pelo aplicativo usando a função [CloseThreadWaitChainSession](/windows/desktop/api/Wct/nf-wct-closethreadwaitchainsession) . Os resultados de operações assíncronas são disponibilizados por meio de uma função de retorno de chamada [WaitChainCallback](/windows/win32/api/wct/nc-wct-pwaitchaincallback) fornecida pelo aplicativo.

Para sessões assíncronas, o chamador pode especificar um ponteiro para uma estrutura de dados de contexto por meio de [GetThreadWaitChain](/windows/desktop/api/Wct/nf-wct-getthreadwaitchain) (esse mesmo ponteiro é passado para a função de retorno de chamada [WaitChainCallback](/windows/win32/api/wct/nc-wct-pwaitchaincallback) ).

A estrutura de dados de contexto é definida pelo usuário e opaca para a WCT. Ele pode ser usado pelo aplicativo para comunicar o contexto entre uma consulta WCT e uma função de retorno de chamada. Normalmente, você passa um identificador de evento por essa estrutura e, quando o retorno de chamada é executado, esse evento é sinalizado e um thread de monitoramento é informado de que a consulta foi concluída.

Consulte [usando a WCT](using-wct.md) para obter um exemplo de percurso de cadeia de espera.

## <a name="related-topics"></a>Tópicos relacionados

[Usando WCT](using-wct.md), [referência WCT](wct-reference.md), [msdn Magazine 2007 julho-Bugslayer: espera de passagem de cadeia](/archive/msdn-magazine/2007/july/bugslayer-wait-chain-traversal)