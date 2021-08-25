---
description: O método EndOfStream notifica o filtro de que nenhum dado adicional é esperado do pino de entrada.
ms.assetid: b8fc3976-e3d4-4f16-82b0-3900ad6a740c
title: Método CTransformFilter. EndOfStream (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.EndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ade419666b1df36e851d5d945e14d9035c1377145cecd472244c9178758f45f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119907626"
---
# <a name="ctransformfilterendofstream-method"></a>Método CTransformFilter. EndOfStream

O `EndOfStream` método notifica o filtro de que nenhum dado adicional é esperado do pino de entrada.

## <a name="syntax"></a>Sintaxe


```C++
virtual HRESULT EndOfStream();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorna S \_ OK ou outro valor **HRESULT** .

## <a name="remarks"></a>Comentários

O método [**CTransformInputPin:: EndOfStream**](ctransforminputpin-endofstream.md) do pino de entrada chama esse método. Esse método entrega o downstream de notificação de fim de fluxo. Se a classe derivada usar um thread de trabalho para fornecer amostras de mídia, ela deverá substituir esse método e enfileirar a notificação de fim de fluxo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Transfrm. h (incluir Fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CTransformFilter**](ctransformfilter.md)
</dt> </dl>

 

 




