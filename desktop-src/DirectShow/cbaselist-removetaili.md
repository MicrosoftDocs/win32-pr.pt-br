---
description: O método RemoveTailI remove o último item na lista.
ms.assetid: 3e9f88a5-a681-4494-8977-d9a6ec62a849
title: Método CBaseList.RemoveTailI (Wxlist.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.RemoveTailI
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c10f7acbb73fe2024308117c8548e789696ee65914aa698dc0478a900846e77d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119341626"
---
# <a name="cbaselistremovetaili-method"></a>Método CBaseList.RemoveTailI

O `RemoveTailI` método remove o último item na lista.

## <a name="syntax"></a>Sintaxe


```C++
void* RemoveTailI();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorna um ponteiro para o item ou **NULL** se a lista estiver vazia.

## <a name="remarks"></a>Comentários

Esse método exclui o nó de lista, mas não o item contido no nó.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wxlist.h (incluir Fluxos.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseList**](cbaselist.md)
</dt> </dl>

 

 




