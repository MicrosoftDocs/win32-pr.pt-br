---
description: A macro de observação envia uma cadeia de caracteres para o local de saída de depuração. Ignorado em compilações de varejo.
ms.assetid: 8b85861a-b4d6-4cc6-9ac9-77d06f173869
title: Observação (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NOTE
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0becacba37f3f474577c36a694539de77795f1c19ccf3b1655cb80370be9e297
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120050916"
---
# <a name="note"></a>OBSERVAÇÃO

A `NOTE` macro envia uma cadeia de caracteres para o local de saída de depuração. Ignorado em compilações de varejo.

``` syntax
NOTE(
    pFormat
);

NOTEn(
    pFormat,
    arg1 ... arg5
);
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="pFormat"></span><span id="pformat"></span><span id="PFORMAT"></span>*pFormat*
</dt> <dd>

Uma cadeia de caracteres de formato de estilo printf.

</dd> <dt>

<span id="arg1arg5"></span><span id="ARG1ARG5"></span>*arg1*–*arg5*
</dt> <dd>

Argumentos adicionais para a cadeia de caracteres de formato. O número de argumentos deve corresponder ao nome da macro. Por exemplo, **NOTE1** usa um argumento e **NOTE5** usa cinco argumentos.

</dd> </dl>

## <a name="remarks"></a>Comentários

Essas macros são variantes da macro [**DbgLog**](dbglog.md) . Eles geram mensagens de rastreamento de LOG de nível 5 \_ .

## <a name="example"></a>Exemplo


```C++
NOTE("Warning, failed to created graph.");
NOTE2("Width: %d, Height: %d", width, height);
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

 

 




