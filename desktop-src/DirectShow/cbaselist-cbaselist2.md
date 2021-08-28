---
description: Construtor CBaseList.CBaseList – método do construtor.
ms.assetid: 2982f53a-c222-4a9d-812a-42897ca4cb5c
title: Construtor CBaseList.CBaseList (Wxlist.h)
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
ms.openlocfilehash: 0b734722371aa80e3c120dde3c6fb629785dfc6cdf9786c7f4ab1cbea87e5559
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016974"
---
# <a name="cbaselistcbaselist-constructor"></a>Construtor CBaseList.CBaseList

Método do construtor.

## <a name="syntax"></a>Sintaxe


```C++
CBaseList(
   TCHAR *pName
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Pname* 
</dt> <dd>

Ponteiro para o nome da lista.

</dd> </dl>

## <a name="remarks"></a>Comentários

Para eficiência, a `CBaseList` classe mantém um cache de nós de lista. Esta versão do construtor usa um tamanho de cache padrão.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wxlist.h (incluir Fluxos.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseList**](cbaselist.md)
</dt> </dl>

 

 




