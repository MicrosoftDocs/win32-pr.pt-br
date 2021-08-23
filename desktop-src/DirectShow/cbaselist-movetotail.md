---
description: O método MoveToTail divide a lista e anexa a parte da cabeça à parte final de outra lista.
ms.assetid: f5cefe7c-075c-433b-9ece-aa10217344fa
title: Método CBaseList.MoveToTail (Wxlist.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.MoveToTail
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8ae7ab918c8c4ef707b2754f8b1ba1f8f3e76265a6b8ac0b252e765de2aff1b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016914"
---
# <a name="cbaselistmovetotail-method"></a>Método CBaseList.MoveToTail

O `MoveToTail` método divide a lista e anexa a parte da cabeça à parte final de outra lista.

## <a name="syntax"></a>Sintaxe


```C++
BOOL MoveToTail(
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

*Plist* 
</dt> <dd>

Ponteiro para outra lista.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna **TRUE se** for bem-sucedido ou FALSE **caso** contrário.

## <a name="remarks"></a>Comentários

Esse método divide a lista após a posição especificada pelo *parâmetro pos.* A parte final permanece na lista. A parte da cabeça é anexada à parte final da outra lista.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wxlist.h (incluir Fluxos.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseList**](cbaselist.md)
</dt> </dl>

 

 




