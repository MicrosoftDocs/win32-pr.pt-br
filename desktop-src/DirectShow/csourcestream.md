---
description: A classe CSourceStream fornece um pino de saída para a classe de filtro CSource.
ms.assetid: 5ccfb129-93e2-4773-9398-5f59f2914ba7
title: Classe CSourceStream (Source. h)
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
ms.openlocfilehash: 36b9085df8c15e765c751be8b5fcdfd4f4a02140
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105779545"
---
# <a name="csourcestream-class"></a>Classe CSourceStream

![hierarquia de classe CSourceStream](images/source02.png)

A classe **CSourceStream** fornece um pino de saída para a classe de filtro [**CSource**](csource.md) .

Para obter informações sobre como usar essa classe, consulte [**CSource**](csource.md). Essa classe herda a classe [**CAMThread**](camthread.md) , que fornece um thread de trabalho para streaming de dados do PIN. A classe **CSourceStream** implementa os seguintes métodos auxiliares para enviar solicitações para o thread:

-   [**CSourceStream:: sair**](csourcestream-exit.md)
-   [**CSourceStream:: init**](csourcestream-init.md)
-   [**CSourceStream::P ause**](csourcestream-pause.md)
-   [**CSourceStream:: Run**](csourcestream-run.md)
-   [**CSourceStream:: Stop**](csourcestream-stop.md)

A primeira solicitação para o thread deve ser [**init**](csourcestream-init.md). A solicitação de [**saída**](csourcestream-exit.md) encerra o thread. Na prática, não é necessário chamar qualquer um desses métodos diretamente, porque os métodos [**CSourceStream:: active**](csourcestream-active.md) e [**CSourceStream:: Inactive**](csourcestream-inactive.md) do PIN os chamam conforme necessário.

A classe também fornece vários métodos "Handler":

-   [**CSourceStream::OnThreadCreate**](csourcestream-onthreadcreate.md)
-   [**CSourceStream::OnThreadDestroy**](csourcestream-onthreaddestroy.md)
-   [**CSourceStream::OnThreadStartPlay**](csourcestream-onthreadstartplay.md)

Eles não fazem nada na classe base, mas a classe derivada pode substituí-los.



| Variáveis de membro protegido                                             | Descrição                                                                                                                       |
|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [**\_pFilter m**](csourcestream-m-pfilter.md)                          | Ponteiro para o filtro que contém este pin.                                                                                     |
| Métodos Protegidos                                                      | Descrição                                                                                                                       |
| [**OnThreadCreate**](csourcestream-onthreadcreate.md)                 | Chamado quando o thread de streaming é inicializado. VirtuaisLUNs.                                                                         |
| [**OnThreadDestroy**](csourcestream-onthreaddestroy.md)               | Chamado quando o thread de streaming está prestes a sair. VirtuaisLUNs.                                                                       |
| [**OnThreadStartPlay**](csourcestream-onthreadstartplay.md)           | Chamado no início do método [**CSourceStream::D obufferprocessingloop**](csourcestream-dobufferprocessingloop.md) . VirtuaisLUNs. |
| [**Activo**](csourcestream-active.md)                                 | Notifica o PIN de que o filtro está ativo agora.                                                                                   |
| [**Inativo**](csourcestream-inactive.md)                             | Notifica o PIN de que o filtro não está mais ativo.                                                                             |
| [**GetRequest**](csourcestream-getrequest.md)                         | Aguarda a próxima solicitação de thread.                                                                                                |
| [**CheckRequest**](csourcestream-checkrequest.md)                     | Verifica se há uma solicitação de thread, sem bloqueio.                                                                            |
| [**ThreadProc**](csourcestream-threadproc.md)                         | Procedimento de thread. VirtuaisLUNs.                                                                                                        |
| [**DoBufferProcessingLoop**](csourcestream-dobufferprocessingloop.md) | Gera dados de mídia e os entrega para o pino de entrada downstream. VirtuaisLUNs.                                                        |
| [**CheckMediaType**](csourcestream-checkmediatype.md)                 | Determina se o PIN aceita um tipo de mídia específico. VirtuaisLUNs.                                                                     |
| [**GetMediaType**](csourcestream-getmediatype.md)                     | Recupera um tipo de mídia preferencial. VirtuaisLUNs.                                                                                        |
| Métodos públicos                                                         | Descrição                                                                                                                       |
| [**CSourceStream**](csourcestream-csourcestream.md)                   | Método de construtor.                                                                                                               |
| [**~ CSourceStream**](csourcestream--csourcestream.md)                | Método destruidor. VirtuaisLUNs.                                                                                                       |
| [**Init**](csourcestream-init.md)                                     | Inicializa o thread de streaming.                                                                                                 |
| [**Fechar**](csourcestream-exit.md)                                     | Sinaliza o thread de streaming para sair.                                                                                             |
| [**Executar**](csourcestream-run.md)                                       | Sinaliza o thread de streaming a ser executado.                                                                                              |
| [**Pausar**](csourcestream-pause.md)                                   | Sinaliza o thread de streaming para se tornar ativo.                                                                                    |
| [**Stop**](csourcestream-stop.md)                                     | Sinaliza o thread de streaming para parar.                                                                                             |
| Métodos virtuais puros                                                   | Descrição                                                                                                                       |
| [**FillBuffer**](csourcestream-fillbuffer.md)                         | Preenche um exemplo de mídia com dados.                                                                                                   |
| Métodos IPin                                                           | Descrição                                                                                                                       |
| [**QueryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid)                                        | Recupera um identificador para o PIN.                                                                                              |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Source. h (incluir fluxos. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Gravando filtros de origem](writing-source-filters.md)
</dt> </dl>

 

 




