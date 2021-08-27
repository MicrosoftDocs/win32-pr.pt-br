---
description: 'O método EndFlush termina uma operação de liberação. Implementa o método IPin:: EndFlush.'
ms.assetid: d4110eb4-26c5-4312-b33f-4af31e1bf2ae
title: Método CBaseInputPin. EndFlush (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.EndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fba4c82679ebe96827cd45c9045080fb354cdab25eb562523869e97d533c5f2a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120056346"
---
# <a name="cbaseinputpinendflush-method"></a>Método CBaseInputPin. EndFlush

O `EndFlush` método encerra uma operação de liberação. Implementa o método [**IPin:: EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT EndFlush();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorna S \_ OK.

## <a name="remarks"></a>Comentários

Esse método define o sinalizador [**CBaseInputPin:: m \_ BFlushing**](cbaseinputpin-m-bflushing.md) como **true**, o que permite que o método [**CBaseInputPin:: Receive**](cbaseinputpin-receive.md) aceite amostras.

A classe derivada deve substituir esse método e executar as seguintes etapas:

1.  Libere todos os dados armazenados em buffer e aguarde a descartação de todas as amostras em fila.
2.  Desmarque todas as notificações pendentes do [**EC \_ Complete**](ec-complete.md) .
3.  Chame o método da classe base.
4.  Chame [**IPin:: EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) em Pins de entrada downstream. Se o PIN ainda não tiver entregue nenhuma amostra de mídia downstream, você poderá ignorar esta etapa. Se os Pins de saída derivarem da classe [**CBaseOutputPin**](cbaseoutputpin.md) , você poderá chamar o método [**CBaseOutputPin::D eliverendflush**](cbaseoutputpin-deliverendflush.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir Fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseInputPin**](cbaseinputpin.md)
</dt> </dl>

 

 




