---
description: Causa uma exceção de ponto de interrupção e registra a cadeia de caracteres especificada usando a macro DbgLog. Ignorado em compilações de varejo.
ms.assetid: 475810db-692b-4727-9ef1-ece74e9618d0
title: Macro KDbgBreak (Wxdebug. h)
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
ms.openlocfilehash: 9631dc8d956652137810b25ae5923cc1c6927bee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757877"
---
# <a name="kdbgbreak-macro"></a>Macro KDbgBreak

Causa uma exceção de ponto de interrupção e registra a cadeia de caracteres especificada usando a macro [**DbgLog**](dbglog.md) . Ignorado em compilações de varejo.

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

Cadeia de texto.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa macro não retorna um valor.

## <a name="remarks"></a>Comentários

Ao contrário da macro [**DbgBreak**](dbgbreak.md) , essa macro não exibe uma caixa de mensagem solicitando o usuário. Em compilações de depuração, ele automaticamente faz com que ocorra uma exceção de ponto de interrupção.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Wxdebug. h (incluir fluxos. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Macros Assert e Breakpoint](assert-and-breakpoint-macros.md)
</dt> </dl>

 

 




