---
description: O próximo método recupera a próxima posição na lista.
ms.assetid: ba9753b0-c82e-4772-84a7-e9982de3b8ad
title: Método CBaseList. Next (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.Next
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f8a09ec91191437fbfb851ce92824b118a5440ca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105769248"
---
# <a name="cbaselistnext-method"></a>Método CBaseList. Next

O `Next` método recupera a próxima posição na lista.

## <a name="syntax"></a>Sintaxe


```C++
POSITION Next(
   POSITION pos
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pos* 
</dt> <dd>

Valor da posição.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna o indicador de posição que segue a posição especificada pelo *PDV*.

## <a name="remarks"></a>Comentários

Se *pos* for a última posição na lista, o método retornará **NULL**. Se o *PDV* for **nulo**, o método retornará a primeira posição na lista.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wxlist. h (incluir fluxos. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseList**](cbaselist.md)
</dt> </dl>

 

 




