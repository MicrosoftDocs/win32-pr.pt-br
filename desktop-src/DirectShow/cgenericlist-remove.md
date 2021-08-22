---
description: O método Remove remove o item na posição especificada.
ms.assetid: a7b8f6fb-f13a-4c24-aa18-463446602e29
title: Método CGenericList.Remove (Wxlist.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.Remove
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 40b00d0772f391978fa6e581623446c67c2f37deabb1737e2602d7da7382fbaf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119317756"
---
# <a name="cgenericlistremove-method"></a>Método CGenericList.Remove

O `Remove` método remove o item na posição especificada.

## <a name="syntax"></a>Sintaxe


```C++
OBJECT* Remove(
   POSITION pos
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pos* 
</dt> <dd>

Valor POSITION que indica o item a ser removido.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um ponteiro para um objeto do tipo **OBJECT** (o tipo de modelo).

## <a name="remarks"></a>Comentários

Esse método exclui o nó da lista, mas não exclui o item contido nesse nó.

Se *pos* for **NULL,** o método retornará **NULL.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wxlist.h (incluir Fluxos.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CGenericList**](cgenericlist.md)
</dt> </dl>

 

 




