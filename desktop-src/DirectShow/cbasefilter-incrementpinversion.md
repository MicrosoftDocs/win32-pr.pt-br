---
description: O método IncremementPinVersion incrementa o número de versão no conjunto de Pins.
ms.assetid: e1b3ec33-104d-4a12-9b11-f8bea09690a7
title: Método CBaseFilter. IncrementPinVersion (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.IncrementPinVersion
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 53e66ccd5bdd34c4767001403439f4372ff2938a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749265"
---
# <a name="cbasefilterincrementpinversion-method"></a>Método CBaseFilter. IncrementPinVersion

O `IncremementPinVersion` método incrementa o número de versão no conjunto de Pins.

## <a name="syntax"></a>Sintaxe


```C++
void IncrementPinVersion();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Esse método incrementa a variável de membro [**CBaseFilter:: m \_ PinVersion**](cbasefilter-m-pinversion.md) . Se o filtro cria ou destrói Pins dinamicamente, chame esse método sempre que os Pins forem alterados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseFilter**](cbasefilter.md)
</dt> <dt>

[**CBaseFilter::GetPinVersion**](cbasefilter-getpinversion.md)
</dt> </dl>

 

 




