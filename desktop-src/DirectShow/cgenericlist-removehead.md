---
description: O método RemoveHead remove o primeiro item na lista.
ms.assetid: 95902028-d2c2-4c16-9ca6-ef57174a9292
title: Método CGenericList.RemoveHead (Wxlist.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.RemoveHead
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7b374ad6a08aac039de3c7d54ee4403f240fdf6bf9839a5ea2554901de789f11
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119317746"
---
# <a name="cgenericlistremovehead-method"></a>Método CGenericList.RemoveHead

O `RemoveHead` método remove o primeiro item na lista.

## <a name="syntax"></a>Sintaxe


```C++
OBJECT* RemoveHead();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorna um ponteiro para um objeto do tipo **OBJECT** (o tipo de modelo) ou **NULL** se a lista estiver vazia.

## <a name="remarks"></a>Comentários

Esse método exclui o nó de lista, mas não o item que o nó contém.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wxlist.h (incluir Fluxos.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CGenericList**](cgenericlist.md)
</dt> </dl>

 

 




