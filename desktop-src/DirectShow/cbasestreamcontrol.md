---
description: Essa classe implementa a interface IAMStreamControl para Pins de entrada e saída.
ms.assetid: a0ddc2d5-8385-4209-b1c5-9822c30f8a02
title: Classe CBaseStreamControl (Strmctl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseStreamControl
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: eb1d8d747d88a416792d59af79af41c047cb51aa61688aef9d6b105790bbae8d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118157193"
---
# <a name="cbasestreamcontrol-class"></a>Classe CBaseStreamControl

![hierarquia de classe CBaseStreamControl](images/strmctl1.png)

Essa classe implementa a interface [**IAMStreamControl**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol) para Pins de entrada e saída. Ele fornece controle sobre como iniciar e parar um PIN individual no filtro. Um PIN que dá suporte a **IAMStreamControl** deve herdar dessa classe base. Veja a seguir uma declaração típica para um PIN de entrada:

``` syntax
class CMyInputPin : public CBaseInputPin, public CBaseStreamControl
```

Certifique-se de substituir **NonDelegatingQueryInteface** para expor **IAMStreamControl**. Para obter mais informações, consulte [como implementar IUnknown](how-to-implement-iunknown.md).



| Métodos públicos                                                        | Descrição                                                                                          |
|-----------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [**CBaseStreamControl**](cbasestreamcontrol-cbasestreamcontrol.md)   | Método de construtor.                                                                                  |
| [**~ CBaseStreamControl**](cbasestreamcontrol--cbasestreamcontrol.md) | Método destruidor.                                                                                   |
| [**CheckStreamState**](cbasestreamcontrol-checkstreamstate.md)       | Determina se um exemplo de mídia deve ser entregue ou descartado.                                  |
| [**Liberação**](cbasestreamcontrol-flushing.md)                       | Notifica a classe base que o PIN iniciou ou parou a liberação.                                |
| [**NotifyFilterState**](cbasestreamcontrol-notifyfilterstate.md)     | Notifica o PIN quando o estado do filtro é alterado.                                                    |
| [**SetFilterGraph**](cbasestreamcontrol-setfiltergraph.md)           | Especifica o coletor de eventos para eventos de controle de fluxo.                                                  |
| [**Setsynce**](cbasestreamcontrol-setsyncsource.md)             | Notifica a classe base do relógio de referência atual.                                              |
| Métodos IAMStreamControl                                              | Descrição                                                                                          |
| [**GetInfo**](cbasestreamcontrol-getinfo.md)                         | Recupera informações sobre as configurações de controle de fluxo atuais, incluindo os horários de início e de parada. |
| [**StartAt**](cbasestreamcontrol-startat.md)                         | Informa o PIN quando iniciar a entrega de dados.                                                       |
| [**StopAt**](cbasestreamcontrol-stopat.md)                           | Informa o PIN quando parar de entregar dados.                                                        |



 

## <a name="remarks"></a>Comentários

Essa classe requer o PIN e o filtro proprietário para notificar a classe quando vários eventos ocorrem, como o filtro ingressando no grafo ou recebendo um novo relógio de referência. Você deve chamar os seguintes métodos de classe:

-   No método [**IMediaFilter:: Setsincronizate**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) do filtro, chame o método [**CBaseStreamControl:: setsincronizate**](cbasestreamcontrol-setsyncsource.md) . Esse método notifica a classe do relógio de referência atual.
-   No método [**CBaseFilter:: JoinFilterGraph**](cbasefilter-joinfiltergraph.md) do filtro, chame o método [**CBaseStreamControl:: SetFilterGraph**](cbasestreamcontrol-setfiltergraph.md) . esse método fornece à classe um ponteiro para o filtro Graph Manager, para que a classe possa enviar os eventos de controle de fluxo corretos.
-   Sempre que o filtro muda de estado (para em execução, em pausa ou parado), chame o método [**CBaseStreamControl:: NotifyFilterState**](cbasestreamcontrol-notifyfilterstate.md) .
-   Nos métodos [**IPin:: BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) e [**IPin:: EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) do PIN, chame o método [**CBaseStreamControl:: flush**](cbasestreamcontrol-flushing.md) .

A `CBaseStreamControl` classe usa o relógio de referência do grafo de filtro para determinar quais exemplos o filtro deve ser entregue e qual deve descartar. No método [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) do PIN, chame o método [**CBaseStreamControl:: CheckStreamState**](cbasestreamcontrol-checkstreamstate.md) com um ponteiro para o exemplo de mídia de entrada. Se o método retornar o fluxo de valores \_ fluindo, entregue o downstream de exemplo. Caso contrário, descarte-o.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Strmctl. h (incluir Fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



 

 




