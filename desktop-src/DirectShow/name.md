---
description: A macro de nome gera uma cadeia de caracteres somente depuração.
ms.assetid: 5cb9f803-dd2b-4055-bdcc-e754ef5fa505
title: NOME (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NAME
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9fa3d9c7e343dcbc8c6959a1ead025cafb3e4722382d7fd61c085bcff05347ec
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120107676"
---
# <a name="name"></a>NOME

A macro de **nome** gera uma cadeia de caracteres somente depuração.

``` syntax
NAME(strLiteral);
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="strLiteral"></span><span id="strliteral"></span><span id="STRLITERAL"></span>*strLiteral*
</dt> <dd>

Cadeia de texto.

</dd> </dl>

## <a name="remarks"></a>Comentários

Em compilações de depuração, essa macro é equivalente à macro de **texto** . Em compilações de varejo, ele é resolvido para (TCHAR \* ) **NULL**. Essa macro é útil ao declarar o nome de um objeto que deriva da classe [**CBaseObject**](cbaseobject.md) .


```C++
pObject = new CBaseObject(NAME("My Object"));
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wxdebug. h (incluir Fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de saída de depuração](debug-output-functions.md)
</dt> </dl>

 

 




