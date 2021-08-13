---
description: O método addcauda acrescenta outra lista ao final desta lista.
ms.assetid: 996523cd-d9ba-406a-afdf-494d328dc9dd
title: Método CBaseList. addcaudal (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.AddTail
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5663a69d803def2b37f9a1ba677966a5b26a8bfc6f7b6eb1eb98eef85bcd961d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118659149"
---
# <a name="cbaselistaddtail-method"></a>Método CBaseList. addcaudal

O `AddTail` método acrescenta outra lista ao final desta lista.

## <a name="syntax"></a>Sintaxe


```C++
BOOL AddTail(
   CBaseList *pList
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pList* 
</dt> <dd>

Ponteiro para a lista a ser acrescentada.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.

## <a name="remarks"></a>Comentários

Se o método falhar, alguns itens poderão ter sido adicionados à lista.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wxlist. h (incluir Fluxos. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseList**](cbaselist.md)
</dt> </dl>

 

 




