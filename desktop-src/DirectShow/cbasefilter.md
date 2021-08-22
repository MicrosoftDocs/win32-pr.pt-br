---
description: A classe CBaseFilter é uma classe abstrata para implementar filtros.
ms.assetid: 4610c8d6-9d7d-47ca-b1d5-0a867153a5f6
title: Classe CBaseFilter (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fbffdf47e019494570506dac164735a2471d0617daa190ad74fb3c8910a7dede
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118659627"
---
# <a name="cbasefilter-class"></a>Classe CBaseFilter

![Hierarquia de classes cbasefilter](images/filter01.png)

A `CBaseFilter` classe é uma classe abstrata para implementar filtros. Para implementar um filtro usando essa classe, você deve executar pelo menos as seguintes etapas:

-   Derive uma nova classe de `CBaseFilter` .
-   Inclua variáveis de membro que definem os pinos no filtro. Os pinos devem herdar da [**classe CBasePin.**](cbasepin.md)
-   Substitua o método virtual [**puro CBaseFilter::GetPin**](cbasefilter-getpin.md), que recupera pinos no filtro.
-   Substitua o método virtual [**puro CBaseFilter::GetPinCount,**](cbasefilter-getpincount.md)que recupera o número de pinos.
-   Forneça métodos para gerar, processar ou renderizar exemplos de mídia.

Várias classes base derivam `CBaseFilter` de , incluindo [**CSource**](csource.md), [**CBaseRenderer**](cbaserenderer.md)e [**CTransformFilter**](ctransformfilter.md). Normalmente, é mais fácil implementar um filtro com uma dessas classes especializadas, em vez de usar `CBaseFilter` diretamente.



| Variáveis de membro protegidas                                     | Descrição                                                                                        |
|----------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [**Estado \_ m**](cbasefilter-m-state.md)                        | Estado atual do filtro.                                                                       |
| [**m \_ pClock**](cbasefilter-m-pclock.md)                      | Ponteiro para o relógio de referência do filtro.                                                           |
| [**m \_ tStart**](cbasefilter-m-tstart.md)                      | Tempo de referência que corresponde ao tempo de fluxo 0.                                                  |
| [**m \_ clsid**](cbasefilter-m-clsid.md)                        | CLSID (identificador de classe) do filtro.                                                            |
| [**m \_ pLock**](cbasefilter-m-plock.md)                        | Ponteiro para uma seção crítica usada para serializar alterações de estado.                             |
| [**m \_ pName**](cbasefilter-m-pname.md)                        | Nome do filtro.                                                                                       |
| [**m \_ pGraph**](cbasefilter-m-pgraph.md)                      | Ponteiro para o gerenciador de grafo de filtro.                                                               |
| [**m \_ pSink**](cbasefilter-m-psink.md)                        | Ponteiro para a interface [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) no gerenciador de grafo de filtro.   |
| [**m \_ PinVersion**](cbasefilter-m-pinversion.md)              | Versão atual do conjunto de pinos nesse filtro.                                                 |
| Métodos públicos                                                 | Descrição                                                                                        |
| [**Cbasefilter**](cbasefilter-cbasefilter.md)                 | Método do construtor.                                                                                |
| [**~ CBaseFilter**](cbasefilter--cbasefilter.md)              | Método destruidor.                                                                                 |
| [**StreamTime**](cbasefilter-streamtime.md)                   | Recupera a hora do fluxo atual. Virtual.                                                        |
| [**Isactive**](cbasefilter-isactive.md)                       | Determina se o filtro está ativo no momento (em execução ou em pausa).                             |
| [**IsStopped**](cbasefilter-isstopped.md)                     | Determina se o filtro está parado no momento.                                                |
| [**Notifyevent**](cbasefilter-notifyevent.md)                 | Envia uma notificação de evento para o gerenciador de grafo de filtro.                                           |
| [**GetFilterGraph**](cbasefilter-getfiltergraph.md)           | Recupera um ponteiro para o gerenciador de grafo de filtro.                                                   |
| [**ReconnectPin**](cbasefilter-reconnectpin.md)               | Interrompe uma conexão de pino existente e a reconecta ao mesmo pin, usando um tipo de mídia especificado. |
| [**Getpinversion**](cbasefilter-getpinversion.md)             | Recupera um número de versão para o conjunto de pinos nesse filtro. Virtual.                            |
| [**IncrementPinVersion**](cbasefilter-incrementpinversion.md) | Incrementa o número de versão no conjunto de pinos.                                                  |
| [**Getsetupdata**](cbasefilter-getsetupdata.md)               | Recupera os dados de registro para o filtro. Virtual.                                           |
| Métodos virtuais puros                                           | Descrição                                                                                        |
| [**GetPinCount**](cbasefilter-getpincount.md)                 | Recupera o número de pinos.                                                                      |
| [**Getpin**](cbasefilter-getpin.md)                           | Recupera um pino.                                                                                   |
| Métodos IPersist                                               | Descrição                                                                                        |
| [**Getclassid**](cbasefilter-getclassid.md)                   | Recupera o identificador de classe.                                                                    |
| Métodos IMediaFilter                                           | Descrição                                                                                        |
| [**GetState**](cbasefilter-getstate.md)                       | Recupera o estado do filtro (em execução, parado ou em pausa).                                        |
| [**SetSyncSource**](cbasefilter-setsyncsource.md)             | Define um relógio de referência para o filtro.                                                             |
| [**GetSyncSource**](cbasefilter-getsyncsource.md)             | Recupera o relógio de referência que o filtro está usando.                                            |
| [**Stop**](cbasefilter-stop.md)                               | Interrompe o filtro.                                                                                  |
| [**Pausar**](cbasefilter-pause.md)                             | Pausa o filtro.                                                                                 |
| [**Executar**](cbasefilter-run.md)                                 | Executa o filtro.                                                                                   |
| Métodos IBaseFilter                                            | Descrição                                                                                        |
| [**Enumpins**](cbasefilter-enumpins.md)                       | Enumera os pinos nesse filtro.                                                                |
| [**Findpin**](cbasefilter-findpin.md)                         | Recupera o pino com o identificador especificado.                                                   |
| [**QueryFilterInfo**](cbasefilter-queryfilterinfo.md)         | Recupera informações sobre o filtro.                                                            |
| [**Joinfiltergraph**](cbasefilter-joinfiltergraph.md)         | Notifica o filtro de que ele ingressou ou saiu de um grafo de filtro.                                     |
| [**QueryVendorInfo**](cbasefilter-queryvendorinfo.md)         | Recupera uma cadeia de caracteres que contém informações do fornecedor.                                                  |
| Métodos IAMovieSetup                                           | Descrição                                                                                        |
| [**Registrar**](cbasefilter-register.md)                       | Adiciona o filtro ao registro.                                                                   |
| [**Cancelar o registro**](cbasefilter-unregister.md)                   | Remove o filtro do registro.                                                              |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir Fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



 

 




