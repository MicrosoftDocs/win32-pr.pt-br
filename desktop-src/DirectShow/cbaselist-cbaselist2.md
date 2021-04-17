---
description: Método de construtor.
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
ms.openlocfilehash: 3afc0a4acf54e186e122f676ac14e9e80aaeafdb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747410"
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



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseList**](cbaselist.md)
</dt> </dl>

 

 




