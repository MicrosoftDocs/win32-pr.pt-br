---
description: O método GetCurrentSample recupera o exemplo atual.
ms.assetid: cfdc66e3-7d32-47b7-87f6-99dd9513c93b
title: Método CBaseRenderer. GetCurrentSample (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.GetCurrentSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5ffe3cdf95d5ab248956e670c04572140fa4621fff5b0cb5183f9a7cbd9b837e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117822717"
---
# <a name="cbaserenderergetcurrentsample-method"></a>Método CBaseRenderer. GetCurrentSample

O `GetCurrentSample` método recupera o exemplo atual.

## <a name="syntax"></a>Sintaxe


```C++
virtual IMediaSample* GetCurrentSample();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorna um ponteiro para a interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) do exemplo, ou **NULL** se nenhum exemplo estiver disponível.

## <a name="remarks"></a>Comentários

A menos que o método retorne **NULL**, o método chama **AddRef** no ponteiro [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) antes de retorná-lo. O chamador deve liberar o ponteiro. (Por implicação, você deve atribuir o valor de retorno a uma variável, para que você possa liberá-lo mais tarde.)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Renbase. h (incluir Fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




