---
description: O método MoveToHead divide a lista e insere a parte final no cabeçalho de outra lista.
ms.assetid: 46e4f8fe-6707-44c6-9d49-0168b35d2364
title: Método CBaseList. MoveToHead (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.MoveToHead
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 80adec6c8e2f6d42b5cf2cabd3a83a4c3aededa3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105778640"
---
# <a name="cbaselistmovetohead-method"></a>Método CBaseList. MoveToHead

O `MoveToHead` método divide a lista e insere a parte final no cabeçalho de outra lista.

## <a name="syntax"></a>Sintaxe


```C++
BOOL MoveToHead(
   POSITION  pos,
   CBaseList *pList
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pos* 
</dt> <dd>

Indicador de posição que marca a divisão na lista.

</dd> <dt>

*pList* 
</dt> <dd>

Ponteiro para outra lista.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.

## <a name="remarks"></a>Comentários

Esse método divide a lista antes da posição especificada pelo parâmetro *pos* . A parte de cabeçalho permanece na lista. A parte final é inserida no cabeçalho da outra lista.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wxlist. h (incluir fluxos. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseList**](cbaselist.md)
</dt> </dl>

 

 




