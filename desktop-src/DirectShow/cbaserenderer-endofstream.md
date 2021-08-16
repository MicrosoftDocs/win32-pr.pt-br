---
description: O método EndOfStream notifica o filtro de que o PIN de entrada recebeu uma notificação de fim de fluxo.
ms.assetid: bdfd03f9-81e0-4d52-959e-82fd1a67e1c3
title: Método CBaseRenderer. EndOfStream (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.EndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9ff047865aa4f52dee6c03411cddb0c957327851f0f6ca1b7a03f0b6adaacfe5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117822727"
---
# <a name="cbaserendererendofstream-method"></a>Método CBaseRenderer. EndOfStream

O `EndOfStream` método notifica o filtro de que o PIN de entrada recebeu uma notificação de fim de fluxo.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT EndOfStream();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorna S \_ OK.

## <a name="remarks"></a>Comentários

O pino de entrada do filtro chama esse método quando recebe uma notificação de fim de fluxo.

Esse método define o [**sinalizador CBaseRenderer:: m \_ BeOS**](cbaserenderer-m-beos.md) como **true** e chama o método [**CBaseRenderer:: SendEndOfStream**](cbaserenderer-sendendofstream.md) para agendar um evento de [**\_ conclusão de EC**](ec-complete.md) . Se o filtro estiver em pausa e aguardando um exemplo, esse método concluirá a transição de estado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Renbase. h (incluir Fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




