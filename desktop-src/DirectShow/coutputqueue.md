---
description: A classe COutputQueue implementa uma fila para fornecer exemplos de mídia.
ms.assetid: da35bdac-fdc2-4b38-8253-547a19213cce
title: Classe COutputQueue (Outputq.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8911c7261af0bf2e140a551b0146b7764cd541368898e6d3905f5dee2eaa4c53
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119813427"
---
# <a name="coutputqueue-class"></a>Classe COutputQueue

![Coutputqueue](images/oput01.png)

A `COutputQueue` classe implementa uma fila para fornecer exemplos de mídia.

Essa classe permite que um pino de saída entregue amostras de forma assíncrona. Os exemplos são colocados em uma fila e um thread de trabalho os entrega ao pino de entrada. A fila também pode conter mensagens de controle que indicam um novo segmento, uma notificação de fim de fluxo ou uma operação de liberação.

Para usar essa classe, crie um **objeto COutputQueue** para cada pino de saída no filtro. No método do construtor, especifique o pino de entrada conectado a esse pino de saída. Usando essa classe, o pino de saída não chama métodos diretamente no pino de entrada. Em vez disso, ele chama métodos correspondentes em `COutputQueue` , conforme mostrado na tabela a seguir.



| Método Pin                                                            | Método COutputQueue                                     |
|-----------------------------------------------------------------------|---------------------------------------------------------|
| [**IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush)                           | [**Beginflush**](coutputqueue-beginflush.md)           |
| [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush)                               | [**Endflush**](coutputqueue-endflush.md)               |
| [**IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream)                         | [**Eos**](coutputqueue-eos.md)                         |
| [**IPin::NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment)                           | [**Newsegment**](coutputqueue-newsegment.md)           |
| [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive)                 | [**Receber**](coutputqueue-receive.md)                 |
| [**IMemInputPin::ReceiveMultiple**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple) | [**ReceiveMultiple**](coutputqueue-receivemultiple.md) |



 

Opcionalmente, você pode configurar o objeto para entregar amostras de forma `COutputQueue` síncrona, sem um thread de trabalho. O objeto também pode decidir em tempo de executar se deve usar um thread de trabalho, com base nas características do pino de entrada. Para obter mais informações, [**consulte COutputQueue::COutputQueue**](coutputqueue-coutputqueue.md).



| Variáveis de membro protegidas                                   | Descrição                                                                                              |
|--------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [**m \_ pPin**](coutputqueue-m-ppin.md)                       | Ponteiro para a interface [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) do pino de entrada.                                               |
| [**m \_ pInputPin**](coutputqueue-m-pinputpin.md)             | Ponteiro para a interface [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) do pino de entrada.                               |
| [**m \_ bBatchExact**](coutputqueue-m-bbatchexact.md)         | Sinalizador que especifica se o objeto fornece amostras em lotes exatos.                                |
| [**m \_ lBatchSize**](coutputqueue-m-lbatchsize.md)           | Tamanho do lote.                                                                                              |
| [**m \_ List**](coutputqueue-m-list.md)                       | Fila de exemplo de mídia.                                                                                      |
| [**m \_ hSem**](coutputqueue-m-hsem.md)                       | Lidar com um semáforo, usado pelo thread para aguardar exemplos.                                           |
| [**m \_ evFlushComplete**](coutputqueue-m-evflushcomplete.md) | Evento que sinaliza quando uma operação de liberação é concluída.                                                  |
| [**m \_ hThread**](coutputqueue-m-hthread.md)                 | Lidar com o thread de trabalho.                                                                             |
| [**m \_ ppSamples**](coutputqueue-m-ppsamples.md)             | Matriz de exemplos de tamanho [**COutputQueue::m \_ lBatchSize**](coutputqueue-m-lbatchsize.md).               |
| [**m \_ nBatched**](coutputqueue-m-nbatched.md)               | Número de amostras atualmente em lote e aguardando processamento.                                             |
| [**m \_ lWaiting**](coutputqueue-m-lwaiting.md)               | Sinalizador que tem um valor que não é zero quando o thread está aguardando um exemplo.                                   |
| [**m \_ bFlushing**](coutputqueue-m-bflushing.md)             | Sinalizador que especifica se o objeto está executando uma operação de liberação.                                  |
| [**m \_ bTerminate**](coutputqueue-m-bterminate.md)           | Sinalizador que especifica se o thread deve ser encerrado.                                                 |
| [**m \_ bSendAnyway**](coutputqueue-m-bsendanyway.md)         | Sinalizador para substituir o processamento em lotes.                                                                       |
| [**m \_ hr**](coutputqueue-m-hr.md)                           | **Valor HRESULT** que indica se o objeto aceitará exemplos.                                 |
| [**m \_ hEventPop**](coutputqueue-m-heventpop.md)             | Evento que é sinalizado sempre que o objeto remove um exemplo da fila.                              |
| Métodos Protegidos                                            | Descrição                                                                                              |
| [**InitialThreadProc**](coutputqueue-initialthreadproc.md)  | Chama o [**método COutputQueue::ThreadProc**](coutputqueue-threadproc.md) quando o thread é criado. |
| [**Threadproc**](coutputqueue-threadproc.md)                | Recupera exemplos da fila e os entrega ao pino de entrada.                                     |
| [**IsQueued**](coutputqueue-isqueued.md)                    | Determina se o objeto está usando um thread de trabalho para fornecer amostras.                               |
| [**QueueSample**](coutputqueue-queuesample.md)              | Enfile um exemplo de mídia ou mensagem de controle.                                                                |
| [**IsSpecialSample**](coutputqueue-isspecialsample.md)      | Determina se os dados na fila são uma mensagem de controle.                                                     |
| [**FreeSamples**](coutputqueue-freesamples.md)              | Libera todos os exemplos pendentes.                                                                               |
| [**NotifyThread**](coutputqueue-notifythread.md)            | Notifica o thread de que a fila contém dados.                                                        |
| Métodos públicos                                               | Descrição                                                                                              |
| [**Coutputqueue**](coutputqueue-coutputqueue.md)            | Método do construtor.                                                                                      |
| [**~COutputQueue**](coutputqueue--coutputqueue.md)          | Método destruidor.                                                                                       |
| [**Beginflush**](coutputqueue-beginflush.md)                | Inicia uma operação de liberação.                                                                                |
| [**Endflush**](coutputqueue-endflush.md)                    | Encerra uma operação de liberação.                                                                                  |
| [**Eos**](coutputqueue-eos.md)                              | Fornece uma chamada de fim de fluxo para o pino de entrada.                                                         |
| [**SendAnyway**](coutputqueue-sendanyway.md)                | Fornece exemplos pendentes.                                                                            |
| [**Newsegment**](coutputqueue-newsegment.md)                | Fornece um novo segmento para o pino de entrada.                                                                 |
| [**Receber**](coutputqueue-receive.md)                      | Fornece um exemplo de mídia para o pino de entrada.                                                                |
| [**ReceiveMultiple**](coutputqueue-receivemultiple.md)      | Fornece um lote de exemplos de mídia para o pino de entrada.                                                      |
| [**Redefinir**](coutputqueue-reset.md)                          | Redefine o objeto para que ele possa receber mais dados.                                                      |
| [**IsIdle**](coutputqueue-isidle.md)                        | Determina se o objeto está aguardando dados.                                                       |
| [**SetPopEvent**](coutputqueue-setpopevent.md)              | Especifica um evento que é sinalizado sempre que o objeto remove um exemplo da fila.                 |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Outputq. h (incluir Fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



 

 




