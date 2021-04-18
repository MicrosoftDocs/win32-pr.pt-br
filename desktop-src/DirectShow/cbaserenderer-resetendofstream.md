---
description: O método ResetEndOfStream redefine os sinalizadores de fim de fluxo.
ms.assetid: 80f6d49b-a825-4c3c-b693-7b1d9298f541
title: Método CBaseRenderer. ResetEndOfStream (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.ResetEndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0269ee2dfafea9265b5eeb82caa4c39f8d91320c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756604"
---
# <a name="cbaserendererresetendofstream-method"></a>Método CBaseRenderer. ResetEndOfStream

O `ResetEndOfStream` método redefine os sinalizadores de fim de fluxo.

## <a name="syntax"></a>Sintaxe


```C++
virtual HRESULT ResetEndOfStream();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Retorna S \_ OK.

## <a name="remarks"></a>Comentários

Esse método limpa a condição de fim de fluxo anterior. Nesse ponto, o filtro pode receber novos dados. Os métodos [**CBaseRenderer:: Stop**](cbaserenderer-stop.md) e [**CBaseRenderer:: BeginFlush**](cbaserenderer-beginflush.md) chamam esse método.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Renbase. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




