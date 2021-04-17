---
description: O método NotifyEvent envia uma notificação de evento para o Gerenciador do grafo de filtro.
ms.assetid: 79587b72-4152-4443-9fde-c2746bf06191
title: Método CBaseFilter. NotifyEvent (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.NotifyEvent
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 49fa689262d8f9b584c93a4b0485bbeaaacbf9a4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748827"
---
# <a name="cbasefilternotifyevent-method"></a>Método CBaseFilter. NotifyEvent

O `NotifyEvent` método envia uma notificação de evento para o Gerenciador do grafo de filtro.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT NotifyEvent(
   long     EventCode,
   LONG_PTR EventParam1,
   LONG_PTR EventParam2
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*EventCode* 
</dt> <dd>

Código de notificação de eventos.

</dd> <dt>

*EventParam1* 
</dt> <dd>

Primeiro parâmetro do evento.

</dd> <dt>

*EventParam2* 
</dt> <dd>

Segundo parâmetro do evento.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor **HRESULT** . Os valores possíveis incluem os da tabela a seguir.



| Código de retorno                                                                               | Descrição                                                                                            |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_falso**</dt> </dl>   | O Gerenciador do grafo de filtro não está aceitando notificações de eventos.<br/>                              |
| <dl> <dt>**S \_ OK**</dt> </dl>      | Êxito.<br/>                                                                                    |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl> | O filtro não tem um ponteiro para a interface [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) .<br/> |



 

## <a name="remarks"></a>Comentários

Para obter uma lista de códigos de notificação e valores de parâmetros, consulte [códigos de notificação de eventos](event-notification-codes.md).

Na classe base, se o código do evento for EC \_ Complete, o método definirá o parâmetro *EventParam2* como um ponteiro para a interface [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) do filtro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseFilter**](cbasefilter.md)
</dt> </dl>

 

 




