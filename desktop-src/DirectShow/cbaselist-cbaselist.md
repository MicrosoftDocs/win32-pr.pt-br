---
description: Método de construtor.
ms.assetid: 2d48cb66-45d2-4d2d-ba7e-ae759b6d2aa4
title: Construtor CBaseList. CBaseList (TCHAR *, INT) (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.CBaseList
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9c947c8ffa6b61f919d03470b386ffa82945f3b2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105778641"
---
# <a name="cbaselistcbaselisttchar-int-constructor"></a>Construtor CBaseList. CBaseList (TCHAR \* , int)

Método de construtor.

## <a name="syntax"></a>Sintaxe


```C++
CBaseList(
   TCHAR *pName,
   INT   iItems
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pName* 
</dt> <dd>

Ponteiro para o nome da lista.

</dd> <dt>

*iItems* 
</dt> <dd>

Tamanho do cache do nó.

</dd> </dl>

## <a name="remarks"></a>Comentários

Para eficiência, a `CBaseList` classe mantém um cache de nós de lista. Se você souber aproximadamente quantos itens a lista manterá, use esta versão do construtor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wxlist. h (incluir fluxos. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseList**](cbaselist.md)
</dt> </dl>

 

 




