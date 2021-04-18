---
description: O método removeri remove o item na posição especificada.
ms.assetid: 6a6d54ce-7ab3-48dd-8d5d-1315816bcbb9
title: Método CBaseList. Removei (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.RemoveI
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a4511a9867f61596572c959a3d763eb56d862311
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105771870"
---
# <a name="cbaselistremovei-method"></a>Método CBaseList. Removei

O `RemoveI` método remove o item na posição especificada.

## <a name="syntax"></a>Sintaxe


```C++
void* RemoveI(
   POSITION pos
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pos* 
</dt> <dd>

Valor de posição indicando o item a ser removido.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um ponteiro para o item.

## <a name="remarks"></a>Comentários

Esse método exclui o nó da lista, mas não exclui o item contido nesse nó.

Se o *PDV* for **nulo**, o método retornará **NULL**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wxlist. h (incluir fluxos. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseList**](cbaselist.md)
</dt> </dl>

 

 




