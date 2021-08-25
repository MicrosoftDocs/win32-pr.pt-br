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
ms.openlocfilehash: 64e833ef495ace41a9dcd1614b69e4a081befce0e429fa7aad800a73ce490439
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119916386"
---
# <a name="cbasepinisstopped-method"></a>Método CBasePin. IsStopped

O `IsStopped` método determina se o filtro que contém este pin é interrompido.

## <a name="syntax"></a>Sintaxe


```C++
BOOL IsStopped();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retornará **true** se o filtro for interrompido. Caso contrário, retornará **false**.

## <a name="remarks"></a>Comentários

Não chame esse método de dentro do método do construtor **CBasePin** , pois o filtro pode ainda não ter sido inicializado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir Fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBasePin**](cbasepin.md)
</dt> </dl>

 

 




