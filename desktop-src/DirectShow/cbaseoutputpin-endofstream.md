---
description: 'O método EndOfStream notifica o PIN de que nenhum dado adicional é esperado. Esse método implementa o método IPin:: EndOfStream.'
ms.assetid: 5c3b5f90-4194-4d65-9f1a-55edf327e3b3
title: Método CBaseOutputPin. EndOfStream (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.EndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e1cd903e811dbcd000ba202fc86c0fcb41bf221b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105755365"
---
# <a name="cbaseoutputpinendofstream-method"></a>Método CBaseOutputPin. EndOfStream

O `EndOfStream` método notifica o PIN de que nenhum dado adicional é esperado. Esse método implementa o método [**IPin:: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT EndOfStream();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Retorna E \_ inesperado.

## <a name="remarks"></a>Comentários

Esse método só deve ser chamado em Pins de entrada, portanto a implementação de **CBaseOutputPin** retorna E \_ inesperada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseOutputPin**](cbaseoutputpin.md)
</dt> </dl>

 

 




