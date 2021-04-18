---
description: O método addapós insere uma lista após a posição especificada.
ms.assetid: c2a2e599-0a83-4eb0-aceb-c483f153ba7e
title: Método CBaseList. AddAfter (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.AddAfter
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4fdab54a124986b462e0ef592bba888e27c09b53
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749848"
---
# <a name="cbaselistaddafter-method"></a>Método CBaseList. AddAfter

O `AddAfter` método insere uma lista após a posição especificada.

## <a name="syntax"></a>Sintaxe


```C++
BOOL AddAfter(
   POSITION  pos,
   CBaseList *pList
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pos* 
</dt> <dd>

Posição após a qual inserir a lista.

</dd> <dt>

*pList* 
</dt> <dd>

Ponteiro para a lista a ser inserida.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.

## <a name="remarks"></a>Comentários

Os indicadores de posição existentes, incluindo aquele especificado no parâmetro *pos* , permanecem válidos. Se o método falhar, alguns dos itens podem ter sido adicionados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wxlist. h (incluir fluxos. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseList**](cbaselist.md)
</dt> </dl>

 

 




