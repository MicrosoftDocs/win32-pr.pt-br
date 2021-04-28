---
description: '\*Método de construtor de Construtor CBaseList. CBaseList (TCHAR, int).'
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
ms.openlocfilehash: cf745e22ffccb342d945a024760f8c72fdb35ce9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099634"
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



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**Classe CBaseList**](cbaselist.md)
</dt> </dl>

 

 




