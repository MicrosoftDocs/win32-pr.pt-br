---
description: 'O método GetPin recupera um PIN. Esse método implementa o método puramente virtual CBaseFilter:: GetPin.'
ms.assetid: 7f30a1ba-8e7b-4bde-9f4d-a85b3a2122e9
title: Método CSource. GetPin (Source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSource.GetPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4c5b7548eca20f9ec6d9e03d0e708ead1b106f543ca8cac108700c64c9352ea3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120087076"
---
# <a name="csourcegetpin-method"></a>Método CSource. GetPin

O `GetPin` método recupera um PIN. Esse método implementa o método puramente virtual [**CBaseFilter:: GetPin**](cbasefilter-getpin.md) .

## <a name="syntax"></a>Sintaxe


```C++
CBasePin* GetPin(
   int n
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*n* 
</dt> <dd>

Número do PIN especificado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna o ponteiro para o objeto [**CBasePin**](cbasepin.md) que implementa o PIN ou **NULL** se o índice estiver fora do intervalo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Source. h (incluir Fluxos. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CSource**](csource.md)
</dt> </dl>

 

 




