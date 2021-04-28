---
description: Construtor de CBaseList. CBaseList-método de construtor.
ms.assetid: 2982f53a-c222-4a9d-812a-42897ca4cb5c
title: Construtor CBaseList. CBaseList (Wxlist. h)
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
ms.openlocfilehash: 66aad24fe2d5176c684d4d78be27833e3be2f909
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096323"
---
# <a name="cbaselistcbaselist-constructor"></a>Construtor CBaseList. CBaseList

Método de construtor.

## <a name="syntax"></a>Sintaxe


```C++
CBaseList(
   TCHAR *pName
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pName* 
</dt> <dd>

Ponteiro para o nome da lista.

</dd> </dl>

## <a name="remarks"></a>Comentários

Para eficiência, a `CBaseList` classe mantém um cache de nós de lista. Esta versão do construtor usa um tamanho de cache padrão.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wxlist. h (incluir fluxos. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**Classe CBaseList**](cbaselist.md)
</dt> </dl>

 

 




