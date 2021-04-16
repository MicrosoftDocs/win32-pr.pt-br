---
description: A classe CBaseFilter é uma classe abstrata para a implementação de filtros.
ms.assetid: 4610c8d6-9d7d-47ca-b1d5-0a867153a5f6
title: Classe CBaseFilter (Amfilter. h)
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
ms.openlocfilehash: fe032d0614b1067c9351b643d457a718b4917a8b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750680"
---
# <a name="cbasefilter-class"></a>Classe CBaseFilter

![hierarquia de classe CBaseFilter](images/filter01.png)

A `CBaseFilter` classe é uma classe abstrata para a implementação de filtros. Para implementar um filtro usando essa classe, você deve executar pelo menos as seguintes etapas:

-   Derive uma nova classe de `CBaseFilter` .
-   Inclua variáveis de membro que definam os Pins no filtro. Os Pins devem herdar da classe [**CBasePin**](cbasepin.md) .
-   Substitua o método virtual puro [**CBaseFilter:: GetPin**](cbasefilter-getpin.md), que recupera Pins no filtro.
-   Substitua o método virtual puro [**CBaseFilter:: GetPinCount**](cbasefilter-getpincount.md), que recupera o número de Pins.
-   Forneça métodos para gerar, processar ou renderizar amostras de mídia.

Várias classes base derivam de `CBaseFilter` , incluindo [**CSource**](csource.md), [**CBaseRenderer**](cbaserenderer.md)e [**CTransformFilter**](ctransformfilter.md). Geralmente, é mais fácil implementar um filtro com uma dessas classes especializadas, em vez de usar `CBaseFilter` diretamente.



| Variáveis de membro protegido                                     | Descrição                                                                                        |
|----------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [**\_estado m**](cbasefilter-m-state.md)                        | Estado atual do filtro.                                                                       |
| [**\_pClock m**](cbasefilter-m-pclock.md)                      | Ponteiro para o relógio de referência do filtro.                                                           |
| [**\_tStart m**](cbasefilter-m-tstart.md)                      | Tempo de referência que corresponde ao tempo de fluxo 0.                                                  |
| [**CLSID do m \_**](cbasefilter-m-clsid.md)                        | Identificador de classe (CLSID) do filtro.                                                            |
| [**\_pLock m**](cbasefilter-m-plock.md)                        | Ponteiro para uma seção crítica que é usada para serializar alterações de estado.                             |
| [**\_pname m**](cbasefilter-m-pname.md)                        | Nome do filtro.                                                                                       |
| [**\_pGraph m**](cbasefilter-m-pgraph.md)                      | Ponteiro para o Gerenciador de gráfico de filtro.                                                               |
| [**\_pSink m**](cbasefilter-m-psink.md)                        | Ponteiro para a interface [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) no Gerenciador do grafo de filtro.   |
| [**\_PinVersion m**](cbasefilter-m-pinversion.md)              | Versão atual do conjunto de Pins neste filtro.                                                 |
| Métodos públicos                                                 | Descrição                                                                                        |
| [**CBaseFilter**](cbasefilter-cbasefilter.md)                 | Método de construtor.                                                                                |
| [**~ CBaseFilter**](cbasefilter--cbasefilter.md)              | Método destruidor.                                                                                 |
| [**Fluxo de transmissão**](cbasefilter-streamtime.md)                   | Recupera a hora atual do fluxo. VirtuaisLUNs.                                                        |
| [**IsActive**](cbasefilter-isactive.md)                       | Determina se o filtro está ativo no momento (em execução ou em pausa).                             |
| [**IsStopped**](cbasefilter-isstopped.md)                     | Determina se o filtro está parado no momento.                                                |
| [**NotifyEvent**](cbasefilter-notifyevent.md)                 | Envia uma notificação de eventos para o Gerenciador do grafo de filtro.                                           |
| [**GetFilterGraph**](cbasefilter-getfiltergraph.md)           | Recupera um ponteiro para o Gerenciador de gráfico de filtro.                                                   |
| [**ReconnectPin**](cbasefilter-reconnectpin.md)               | Interrompe uma conexão de PIN existente e a reconecta ao mesmo PIN, usando um tipo de mídia especificado. |
| [**GetPinVersion**](cbasefilter-getpinversion.md)             | Recupera um número de versão para o conjunto de Pins neste filtro. VirtuaisLUNs.                            |
| [**IncrementPinVersion**](cbasefilter-incrementpinversion.md) | Incrementa o número de versão no conjunto de Pins.                                                  |
| [**GetSetupData**](cbasefilter-getsetupdata.md)               | Recupera os dados de registro para o filtro. VirtuaisLUNs.                                           |
| Métodos virtuais puros                                           | Descrição                                                                                        |
| [**GetPinCount**](cbasefilter-getpincount.md)                 | Recupera o número de Pins.                                                                      |
| [**GetPin**](cbasefilter-getpin.md)                           | Recupera um PIN.                                                                                   |
| Métodos IPersist                                               | Descrição                                                                                        |
| [**GetClassID**](cbasefilter-getclassid.md)                   | Recupera o identificador de classe.                                                                    |
| Métodos IMediaFilter                                           | Descrição                                                                                        |
| [**GetState**](cbasefilter-getstate.md)                       | Recupera o estado do filtro (em execução, parado ou pausado).                                        |
| [**Setsynce**](cbasefilter-setsyncsource.md)             | Define um relógio de referência para o filtro.                                                             |
| [**Getsync**](cbasefilter-getsyncsource.md)             | Recupera o relógio de referência que o filtro está usando.                                            |
| [**Stop**](cbasefilter-stop.md)                               | Interrompe o filtro.                                                                                  |
| [**Pausar**](cbasefilter-pause.md)                             | Pausa o filtro.                                                                                 |
| [**Executar**](cbasefilter-run.md)                                 | Executa o filtro.                                                                                   |
| Métodos IBaseFilter                                            | Descrição                                                                                        |
| [**EnumPins**](cbasefilter-enumpins.md)                       | Enumera os Pins neste filtro.                                                                |
| [**FindPin**](cbasefilter-findpin.md)                         | Recupera o PIN com o identificador especificado.                                                   |
| [**QueryFilterInfo**](cbasefilter-queryfilterinfo.md)         | Recupera informações sobre o filtro.                                                            |
| [**JoinFilterGraph**](cbasefilter-joinfiltergraph.md)         | Notifica o filtro de que ele ingressou ou saiu de um grafo de filtro.                                     |
| [**QueryVendorInfo**](cbasefilter-queryvendorinfo.md)         | Recupera uma cadeia de caracteres que contém informações do fornecedor.                                                  |
| Métodos IAMovieSetup                                           | Descrição                                                                                        |
| [**Registrar**](cbasefilter-register.md)                       | Adiciona o filtro ao registro.                                                                   |
| [**Cancelar o registro**](cbasefilter-unregister.md)                   | Remove o filtro do registro.                                                              |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



 

 




