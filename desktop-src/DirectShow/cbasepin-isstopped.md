---
description: O método IsStopped determina se o filtro que contém esse PIN é interrompido.
ms.assetid: ffeac352-2f9b-44be-a8e8-7e9238d0b18e
title: Método CBasePin. IsStopped (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.IsStopped
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4185c02b396f7d0d570081ba1401e0ec9e301d46
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751505"
---
# <a name="cbasepinisstopped-method"></a>Método CBasePin. IsStopped

O `IsStopped` método determina se o filtro que contém este pin é interrompido.

## <a name="syntax"></a>Sintaxe


```C++
BOOL IsStopped();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Retornará **true** se o filtro for interrompido. Caso contrário, retornará **false**.

## <a name="remarks"></a>Comentários

Não chame esse método de dentro do método do construtor **CBasePin** , pois o filtro pode ainda não ter sido inicializado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBasePin**](cbasepin.md)
</dt> </dl>

 

 




