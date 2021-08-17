---
description: A macro REMIND gera um lembrete no tempo de compilação. Essa macro gera uma cadeia de caracteres que inclui a cadeia de caracteres de parâmetro, o nome do arquivo de origem e o número de linha.
ms.assetid: 12043df5-ed68-4980-91aa-7598d8ab1951
title: REMIND (Wxdebug.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- REMIND
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c17ec8fac190cd98803a0dfa85acff015d0ac2c18ce712cc87316dd2dca181bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118952115"
---
# <a name="remind"></a>Lembrar

A `REMIND` macro gera um lembrete no tempo de compilação. Essa macro gera uma cadeia de caracteres que inclui a cadeia de caracteres de parâmetro, o nome do arquivo de origem e o número de linha.

``` syntax
REMIND(strLiteral);
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="strLiteral"></span><span id="strliteral"></span><span id="STRLITERAL"></span>*strLiteral*
</dt> <dd>

Cadeia de caracteres de texto.

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa macro é útil para gerar avisos de tempo de compilação:


```C++
#pragma message (REMIND("TO DO: Add support for IDispatch."))
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wxdebug.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de saída de depuração](debug-output-functions.md)
</dt> </dl>

 

 




