---
description: Causa uma exceção de ponto de interrupção e registra a cadeia de caracteres especificada usando a macro DbgLog. Ignorado em builds de varejo.
ms.assetid: 475810db-692b-4727-9ef1-ece74e9618d0
title: Macro KDbgBreak (Wxdebug.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KDbgBreak
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: 3339e69bb10876fe326f5960e6012849664fdbfcb4fe06fffd4029e6170af8b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118952355"
---
# <a name="kdbgbreak-macro"></a>Macro KDbgBreak

Causa uma exceção de ponto de interrupção e registra a cadeia de caracteres especificada usando a [**macro DbgLog.**](dbglog.md) Ignorado em builds de varejo.

## <a name="syntax"></a>Sintaxe


```C++
void KDbgBreak(
    strLiteral
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*strLiteral* 
</dt> <dd>

Cadeia de caracteres de texto.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Essa macro não retorna um valor.

## <a name="remarks"></a>Comentários

Ao contrário [**da macro DbgBreak,**](dbgbreak.md) essa macro não exibe uma caixa de mensagem solicitando o usuário. Em builds de depuração, isso faz com que ocorra automaticamente uma exceção de ponto de interrupção.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Wxdebug.h (incluir Fluxos.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Macros assert e breakpoint](assert-and-breakpoint-macros.md)
</dt> </dl>

 

 




