---
description: A classe CSourceStream fornece um pino de saída para a classe de filtro CSource.
ms.assetid: 5ccfb129-93e2-4773-9398-5f59f2914ba7
title: Classe CSourceStream (Source.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0f7563cabff97626ac45a150e9a763033d9ce9261e5ae528e83d174e35d4f0d9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119428776"
---
# <a name="csourcestream-class"></a>Classe CSourceStream

![Hierarquia de classes csourcestream](images/source02.png)

A **classe CSourceStream** fornece um pino de saída para a [**classe de filtro CSource.**](csource.md)

Para obter informações sobre como usar essa classe, consulte [**CSource**](csource.md). Essa classe herda a [**classe CAMThread,**](camthread.md) que fornece um thread de trabalho para transmitir dados do pino. A **classe CSourceStream** implementa os seguintes métodos auxiliares para enviar solicitações para o thread:

-   [**CSourceStream::Exit**](csourcestream-exit.md)
-   [**CSourceStream::Init**](csourcestream-init.md)
-   [**CSourceStream::P ause**](csourcestream-pause.md)
-   [**CSourceStream::Run**](csourcestream-run.md)
-   [**CSourceStream::Stop**](csourcestream-stop.md)

A primeira solicitação para o thread deve ser [**Init**](csourcestream-init.md). A [**solicitação**](csourcestream-exit.md) Exit encerra o thread. Na prática, não é necessário chamar nenhum desses métodos diretamente, porque os métodos [**CSourceStream::Active**](csourcestream-active.md) e [**CSourceStream::Inactive**](csourcestream-inactive.md) do pino os chamam conforme necessário.

A classe também fornece vários métodos de "manipulador":

-   [**CSourceStream::OnThreadCreate**](csourcestream-onthreadcreate.md)
-   [**CSourceStream::OnThreadDestroy**](csourcestream-onthreaddestroy.md)
-   [**CSourceStream::OnThreadStartPlay**](csourcestream-onthreadstartplay.md)

Eles não fazem nada na classe base, mas a classe derivada pode substituí-las.



| Variáveis de membro protegidas                                             | Descrição                                                                                                                       |
|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [**m \_ pFilter**](csourcestream-m-pfilter.md)                          | Ponteiro para o filtro que contém esse pino.                                                                                     |
| Métodos Protegidos                                                      | Descrição                                                                                                                       |
| [**OnThreadCreate**](csourcestream-onthreadcreate.md)                 | Chamado quando o thread de streaming é inicializado. Virtual.                                                                         |
| [**OnThreadDestroy**](csourcestream-onthreaddestroy.md)               | Chamado quando o thread de streaming está prestes a sair. Virtual.                                                                       |
| [**OnThreadStartPlay**](csourcestream-onthreadstartplay.md)           | Chamado no início do método [**CSourceStream::D oBufferProcessingLoop.**](csourcestream-dobufferprocessingloop.md) Virtual. |
| [**Ativo**](csourcestream-active.md)                                 | Notifica o pino de que o filtro agora está ativo.                                                                                   |
| [**Inativo**](csourcestream-inactive.md)                             | Notifica o pino de que o filtro não está mais ativo.                                                                             |
| [**Getrequest**](csourcestream-getrequest.md)                         | Aguarda a próxima solicitação de thread.                                                                                                |
| [**CheckRequest**](csourcestream-checkrequest.md)                     | Verifica se há uma solicitação de thread, sem bloqueio.                                                                            |
| [**Threadproc**](csourcestream-threadproc.md)                         | Procedimento de thread. Virtual.                                                                                                        |
| [**DoBufferProcessingLoop**](csourcestream-dobufferprocessingloop.md) | Gera dados de mídia e os entrega para o pin de entrada downstream. Virtual.                                                        |
| [**Checkmediatype**](csourcestream-checkmediatype.md)                 | Determina se o pin aceita um tipo de mídia específico. Virtual.                                                                     |
| [**Getmediatype**](csourcestream-getmediatype.md)                     | Recupera um tipo de mídia preferencial. Virtual.                                                                                        |
| Métodos públicos                                                         | Descrição                                                                                                                       |
| [**Csourcestream**](csourcestream-csourcestream.md)                   | Método do construtor.                                                                                                               |
| [**~ CSourceStream**](csourcestream--csourcestream.md)                | Método destruidor. Virtual.                                                                                                       |
| [**Init**](csourcestream-init.md)                                     | Inicializa o thread de streaming.                                                                                                 |
| [**Fechar**](csourcestream-exit.md)                                     | Sinaliza o thread de streaming para sair.                                                                                             |
| [**Executar**](csourcestream-run.md)                                       | Sinaliza o thread de streaming a ser executado.                                                                                              |
| [**Pausar**](csourcestream-pause.md)                                   | Sinaliza o thread de streaming para se tornar ativo.                                                                                    |
| [**Stop**](csourcestream-stop.md)                                     | Sinaliza o thread de streaming para parar.                                                                                             |
| Métodos virtuais puros                                                   | Descrição                                                                                                                       |
| [**FillBuffer**](csourcestream-fillbuffer.md)                         | Preenche um exemplo de mídia com dados.                                                                                                   |
| Métodos IPin                                                           | Descrição                                                                                                                       |
| [**Queryid**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid)                                        | Recupera um identificador para o pino.                                                                                              |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Source.h (incluir Fluxos.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Escrevendo filtros de origem](writing-source-filters.md)
</dt> </dl>

 

 




