---
description: O método RemoveTail remove o último item da lista.
ms.assetid: 377af676-8042-430e-87a6-b41c00482a90
title: Método CGenericList. RemoveTail (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.RemoveTail
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ed0b39d72eac68310dacdf2bfdc1d3c28bb35695b3d77230ba37f6fe81c417ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118656151"
---
# <a name="cgenericlistremovetail-method"></a>Método CGenericList. RemoveTail

O `RemoveTail` método remove o último item da lista.

## <a name="syntax"></a>Sintaxe


```C++
OBJECT* RemoveTail();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorna um ponteiro para um objeto do tipo **Object** (o tipo de modelo) ou **NULL** se a lista estiver vazia.

## <a name="remarks"></a>Comentários

Esse método exclui o nó da lista, mas não o item contido no nó.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wxlist. h (incluir Fluxos. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CGenericList**](cgenericlist.md)
</dt> </dl>

 

 




