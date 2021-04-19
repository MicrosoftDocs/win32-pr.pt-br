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
ms.openlocfilehash: 6e12da02ffbce99b29d324c1166b3d4cdf2265c6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752899"
---
# <a name="cbaserendererendofstream-method"></a>Método CBaseRenderer. EndOfStream

O `EndOfStream` método notifica o filtro de que o PIN de entrada recebeu uma notificação de fim de fluxo.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT EndOfStream();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Retorna S \_ OK.

## <a name="remarks"></a>Comentários

O pino de entrada do filtro chama esse método quando recebe uma notificação de fim de fluxo.

Esse método define o [**sinalizador CBaseRenderer:: m \_ BeOS**](cbaserenderer-m-beos.md) como **true** e chama o método [**CBaseRenderer:: SendEndOfStream**](cbaserenderer-sendendofstream.md) para agendar um evento de [**\_ conclusão de EC**](ec-complete.md) . Se o filtro estiver em pausa e aguardando um exemplo, esse método concluirá a transição de estado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Renbase. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




