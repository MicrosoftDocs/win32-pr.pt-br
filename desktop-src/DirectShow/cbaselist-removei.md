---
description: O método RemoveI remove o item na posição especificada.
ms.assetid: 6a6d54ce-7ab3-48dd-8d5d-1315816bcbb9
title: Método CBaseList.RemoveI (Wxlist.h)
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
ms.openlocfilehash: ac3277f30e959e42cf2fd2d1aeeb13f81cb17515abb8434a8ae13406d244aaec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117823733"
---
# <a name="cbaselistremovei-method"></a>Método CBaseList.RemoveI

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

Valor POSITION que indica o item a ser removido.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um ponteiro para o item.

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

[**Classe CBaseList**](cbaselist.md)
</dt> </dl>

 

 




