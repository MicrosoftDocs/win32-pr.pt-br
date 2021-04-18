---
description: O método addantes insere uma lista antes da posição especificada.
ms.assetid: a4c0dbec-64a0-445b-95e5-000603cc0264
title: Método CBaseList. AddBefore (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.AddBefore
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6a3c25b2dd545b3e6698404bf00f82d1086bfb81
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751913"
---
# <a name="cbaselistaddbefore-method"></a>Método CBaseList. AddBefore

O `AddBefore` método insere uma lista antes da posição especificada.

## <a name="syntax"></a>Sintaxe


```C++
BOOL AddBefore(
   POSITION  pos,
   CBaseList *pList
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pos* 
</dt> <dd>

Posição antes da qual inserir a lista.

</dd> <dt>

*pList* 
</dt> <dd>

Ponteiro para a lista a ser inserida.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retornará **true** se for bem-sucedido. Caso contrário, retornará **false**.

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

 

 




