---
description: A macro lembrar gera um lembrete no momento da compilação. Essa macro gera uma cadeia de caracteres que inclui a cadeia de caracteres do parâmetro, o nome do arquivo de origem e o número da linha.
ms.assetid: 12043df5-ed68-4980-91aa-7598d8ab1951
title: LEMBREte (Wxdebug. h)
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
ms.openlocfilehash: 305e5df628244293b643da8882f57dd83041c4c6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105779837"
---
# <a name="remind"></a>-

A `REMIND` macro gera um lembrete no momento da compilação. Essa macro gera uma cadeia de caracteres que inclui a cadeia de caracteres do parâmetro, o nome do arquivo de origem e o número da linha.

``` syntax
REMIND(strLiteral);
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="strLiteral"></span><span id="strliteral"></span><span id="STRLITERAL"></span>*strLiteral*
</dt> <dd>

Cadeia de texto.

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa macro é útil para gerar avisos de tempo de compilação:


```C++
#pragma message (REMIND("TO DO: Add support for IDispatch."))
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wxdebug. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de saída de depuração](debug-output-functions.md)
</dt> </dl>

 

 




