---
description: Liberação
ms.assetid: 868218c4-3e1a-4da0-89fa-30a9848da0e8
title: Liberação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e70f610a68b2ca81afff736b3e7402d80e5d5675e429d1715ebebf5b640a362
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118401740"
---
# <a name="flushing"></a>Liberação

Enquanto o grafo de filtro está em execução, quantidades arbitrárias de dados podem ser percorrendo o grafo. Algumas delas podem estar em filas, aguardando para serem entregues. Há ocasiões em que o grafo de filtro precisa remover esses dados pendentes o mais rápido possível e substituí-los por novos dados. Depois de um comando de busca, por exemplo, o filtro de origem gera amostras de uma nova posição na origem. Para minimizar a latência, os filtros downstream devem descartar quaisquer exemplos que foram criados antes do comando de busca. O processo de descartar amostras é chamado de *liberação*. Ele permite que o grafo seja mais responsivo quando os eventos alteram o fluxo de dados normal.

A liberação é tratada de forma ligeiramente diferente pelo modelo de pull do que o modelo de push. Este artigo começa descrevendo o modelo de push; em seguida, ele descreve as diferenças no modelo de pull.

A liberação ocorre em dois estágios.

-   Primeiro, o filtro de origem chama [**IPin:: BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) no pino de entrada do filtro downstream. O filtro downstream começa a rejeitar amostras de upstream. Ele também descarta todos os exemplos que estão mantendo e envia a chamada **BeginFlush** de downstream para o próximo filtro.
-   Quando o filtro de origem está pronto para enviar novos dados, ele chama [**IPin:: EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) no pino de entrada. Isso sinaliza o filtro downstream de que ele pode receber novos exemplos. O filtro downstream envia a chamada **EndFlush** para o próximo filtro.

No método **BeginFlush** , o pino de entrada faz o seguinte:

1.  Chama **BeginFlush** em Pins de entrada downstream.
2.  Rejeita todas as chamadas adicionais que transmitem dados, incluindo **Receive** e **EndOfStream**.
3.  Desbloqueia todos os filtros upstream que estão bloqueados aguardando uma amostra do alocador do filtro. Alguns filtros desconfirmam seus alocadores para essa finalidade.
4.  Sai de qualquer espera que bloqueie o streaming. Por exemplo, os filtros de renderização são bloqueados quando pausados. Eles também bloqueiam quando estão aguardando para renderizar uma amostra no tempo de fluxo correto. O filtro deve desbloquear, de modo que os exemplos enfileirados no upstream possam ser entregues e rejeitados. Essa etapa garante que todos os filtros upstream eventualmente desbloqueiem.

No método **EndFlush** , o pino de entrada faz o seguinte:

1.  Aguarda que todas as amostras em fila sejam descartadas.
2.  Libera todos os dados armazenados em buffer. Às vezes, essa etapa pode ser executada no método **BeginFlush** . No entanto, **BeginFlush** não é sincronizado com o thread de streaming. O filtro não deve processar nem armazenar mais dados entre a chamada para **BeginFlush** e a chamada para **EndFlush**.
3.  Limpa todas as notificações pendentes do EC \_ Complete.
4.  Chama downstream de **liberação** .

Neste ponto, o filtro pode aceitar amostras novamente. Todas as amostras têm a garantia de serem mais recentes do que a liberação.

No modelo de pull, o filtro do analisador inicia a liberação, em vez do filtro de origem. Ele não apenas chama **IPin:: BeginFlush** e **IPin:: EndFlush** no filtro downstream, ele também chama [**IAsyncReader:: BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-beginflush) e [**IAsyncReader:: EndFlush**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-endflush) no pino de *saída* do filtro de origem. Se o filtro de origem tiver solicitações de leitura pendentes, elas serão descartadas.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Liberando dados](flushing-data.md)
</dt> </dl>

 

 



