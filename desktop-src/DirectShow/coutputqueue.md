---
description: A classe COutputQueue implementa uma fila para fornecer amostras de mídia.
ms.assetid: da35bdac-fdc2-4b38-8253-547a19213cce
title: Classe COutputQueue (Outputq. h)
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
ms.openlocfilehash: cd6167402abd36db8f436f6e27b18213642f010b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105812842"
---
# <a name="coutputqueue-class"></a>Classe COutputQueue

![coutputqueue](images/oput01.png)

A `COutputQueue` classe implementa uma fila para fornecer amostras de mídia.

Essa classe permite que um pino de saída entregue amostras de forma assíncrona. Os exemplos são colocados em uma fila e um thread de trabalho os entrega ao PIN de entrada. A fila também pode manter mensagens de controle que indicam um novo segmento, uma notificação de fim de fluxo ou uma operação de liberação.

Para usar essa classe, crie um objeto **COutputQueue** para cada pino de saída no filtro. No método do Construtor, especifique o pino de entrada conectado a esse pino de saída. Usando essa classe, o pino de saída não chama métodos diretamente no pino de entrada. Em vez disso, ele chama os métodos correspondentes no `COutputQueue` , conforme mostrado na tabela a seguir.



| Método PIN                                                            | Método COutputQueue                                     |
|-----------------------------------------------------------------------|---------------------------------------------------------|
| [**IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush)                           | [**BeginFlush**](coutputqueue-beginflush.md)           |
| [**IPin:: EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush)                               | [**EndFlush**](coutputqueue-endflush.md)               |
| [**IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream)                         | [**Electric**](coutputqueue-eos.md)                         |
| [**IPin::NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment)                           | [**NewSegment**](coutputqueue-newsegment.md)           |
| [**IMemInputPin:: receber**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive)                 | [**Recebe**](coutputqueue-receive.md)                 |
| [**IMemInputPin::ReceiveMultiple**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple) | [**ReceiveMultiple**](coutputqueue-receivemultiple.md) |



 

Opcionalmente, você pode configurar o `COutputQueue` objeto para entregar amostras de forma síncrona, sem um thread de trabalho. O objeto também pode decidir em tempo de execução se um thread de trabalho deve ser usado, com base nas características do pino de entrada. Para obter mais informações, consulte [**COutputQueue:: COutputQueue**](coutputqueue-coutputqueue.md).



| Variáveis de membro protegido                                   | Descrição                                                                                              |
|--------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [**\_pPin m**](coutputqueue-m-ppin.md)                       | Ponteiro para a interface [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) do pino de entrada.                                               |
| [**\_pInputPin m**](coutputqueue-m-pinputpin.md)             | Ponteiro para a interface [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) do pino de entrada.                               |
| [**\_bBatchExact m**](coutputqueue-m-bbatchexact.md)         | Sinalizador que especifica se o objeto fornece amostras em lotes exatos.                                |
| [**\_lBatchSize m**](coutputqueue-m-lbatchsize.md)           | Tamanho do lote.                                                                                              |
| [**lista de m \_**](coutputqueue-m-list.md)                       | Fila de exemplo de mídia.                                                                                      |
| [**\_hSem m**](coutputqueue-m-hsem.md)                       | Identificador para um semáforo, usado pelo thread para aguardar exemplos.                                           |
| [**\_evFlushComplete m**](coutputqueue-m-evflushcomplete.md) | Evento que sinaliza quando uma operação de liberação é concluída.                                                  |
| [**\_hThread m**](coutputqueue-m-hthread.md)                 | Identificador para o thread de trabalho.                                                                             |
| [**\_ppSamples m**](coutputqueue-m-ppsamples.md)             | Matriz de amostras de tamanho [**COutputQueue:: m \_ lBatchSize**](coutputqueue-m-lbatchsize.md).               |
| [**\_nBatched m**](coutputqueue-m-nbatched.md)               | Número de amostras atualmente em lote e aguardando processamento.                                             |
| [**\_lWaiting m**](coutputqueue-m-lwaiting.md)               | Sinalizador que tem um valor diferente de zero quando o thread está aguardando um exemplo.                                   |
| [**\_bFlushing m**](coutputqueue-m-bflushing.md)             | Sinalizador que especifica se o objeto está executando uma operação de liberação.                                  |
| [**\_bTerminate m**](coutputqueue-m-bterminate.md)           | Sinalizador que especifica se o thread deve ser encerrado.                                                 |
| [**\_bSendAnyway m**](coutputqueue-m-bsendanyway.md)         | Sinalizador para substituir o processamento em lotes.                                                                       |
| [**m \_ hr**](coutputqueue-m-hr.md)                           | Valor **HRESULT** que indica se o objeto aceitará amostras.                                 |
| [**\_hEventPop m**](coutputqueue-m-heventpop.md)             | Evento que é sinalizado sempre que o objeto remove um exemplo da fila.                              |
| Métodos Protegidos                                            | Descrição                                                                                              |
| [**InitialThreadProc**](coutputqueue-initialthreadproc.md)  | Chama o método [**COutputQueue:: ThreadProc**](coutputqueue-threadproc.md) quando o thread é criado. |
| [**ThreadProc**](coutputqueue-threadproc.md)                | Recupera amostras da fila e as entrega ao PIN de entrada.                                     |
| [**Isqueueed**](coutputqueue-isqueued.md)                    | Determina se o objeto está usando um thread de trabalho para fornecer exemplos.                               |
| [**QueueSample**](coutputqueue-queuesample.md)              | Enfileira um exemplo de mídia ou uma mensagem de controle.                                                                |
| [**IsSpecialSample**](coutputqueue-isspecialsample.md)      | Determina se os dados em fila são uma mensagem de controle.                                                     |
| [**FreeSamples**](coutputqueue-freesamples.md)              | Libera todos os exemplos pendentes.                                                                               |
| [**NotifyThread**](coutputqueue-notifythread.md)            | Notifica o thread de que a fila contém dados.                                                        |
| Métodos públicos                                               | Descrição                                                                                              |
| [**COutputQueue**](coutputqueue-coutputqueue.md)            | Método de construtor.                                                                                      |
| [**~ COutputQueue**](coutputqueue--coutputqueue.md)          | Método destruidor.                                                                                       |
| [**BeginFlush**](coutputqueue-beginflush.md)                | Inicia uma operação de liberação.                                                                                |
| [**EndFlush**](coutputqueue-endflush.md)                    | Finaliza uma operação de liberação.                                                                                  |
| [**Electric**](coutputqueue-eos.md)                              | Fornece uma chamada de fim de fluxo para o pino de entrada.                                                         |
| [**SendAnyway**](coutputqueue-sendanyway.md)                | Entrega quaisquer exemplos pendentes.                                                                            |
| [**NewSegment**](coutputqueue-newsegment.md)                | Entrega um novo segmento ao pino de entrada.                                                                 |
| [**Recebe**](coutputqueue-receive.md)                      | Entrega um exemplo de mídia para o pino de entrada.                                                                |
| [**ReceiveMultiple**](coutputqueue-receivemultiple.md)      | Entrega um lote de amostras de mídia para o pino de entrada.                                                      |
| [**Redefinir**](coutputqueue-reset.md)                          | Redefine o objeto para que ele possa receber mais dados.                                                      |
| [**IsIdle**](coutputqueue-isidle.md)                        | Determina se o objeto está aguardando dados.                                                       |
| [**SetPopEvent**](coutputqueue-setpopevent.md)              | Especifica um evento que é sinalizado sempre que o objeto remove um exemplo da fila.                 |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Outputq. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



 

 




