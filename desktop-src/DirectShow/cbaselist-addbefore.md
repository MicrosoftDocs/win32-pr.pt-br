---
description: O método AddBefore insere uma lista antes da posição especificada.
ms.assetid: a4c0dbec-64a0-445b-95e5-000603cc0264
title: Método CBaseList.AddBefore (Wxlist.h)
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
ms.openlocfilehash: 2b4f85536b6a9372f164f596f96758a503096dbb0a5e5ed55adab42bc406b053
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016964"
---
# <a name="cbaselistaddbefore-method"></a>Método CBaseList.AddBefore

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

*Plist* 
</dt> <dd>

Ponteiro para a lista a ser inserida.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará **TRUE** se for bem-sucedido. Caso contrário, **retornará FALSE.**

## <a name="remarks"></a>Comentários

Os indicadores de posição existentes, incluindo o especificado no parâmetro *pos,* permanecem válidos. Se o método falhar, alguns dos itens poderão ter sido adicionados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wxlist.h (incluir Fluxos.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseList**](cbaselist.md)
</dt> </dl>

 

 




