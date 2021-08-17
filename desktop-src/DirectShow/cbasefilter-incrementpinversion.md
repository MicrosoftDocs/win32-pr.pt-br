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
ms.openlocfilehash: 01c82a5f506673b6145b468004bbc900d3acdb051f525df20930344137618e72
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117824101"
---
# <a name="cbasefilterincrementpinversion-method"></a>Método CBaseFilter. IncrementPinVersion

O `IncremementPinVersion` método incrementa o número de versão no conjunto de Pins.

## <a name="syntax"></a>Sintaxe


```C++
void IncrementPinVersion();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Esse método incrementa a variável de membro [**CBaseFilter:: m \_ PinVersion**](cbasefilter-m-pinversion.md) . Se o filtro cria ou destrói Pins dinamicamente, chame esse método sempre que os Pins forem alterados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir Fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseFilter**](cbasefilter.md)
</dt> <dt>

[**CBaseFilter::GetPinVersion**](cbasefilter-getpinversion.md)
</dt> </dl>

 

 




