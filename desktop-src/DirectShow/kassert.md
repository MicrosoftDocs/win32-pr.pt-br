---
description: Avalia uma expressão e causa uma exceção de ponto de interrupção se a expressão for falsa. O texto da expressão, o nome do arquivo de origem e o número da linha são registrados usando a macro DbgLog. Ignorado em compilações de varejo.
ms.assetid: fd116403-df23-490f-b3a8-b2a8bf2b4a5f
title: Macro KASSERT (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KASSERT
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: f797e60a6175a86f2c1c9d675e9607a48a58c14a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757248"
---
# <a name="kassert-macro"></a>Macro KASSERT

Avalia uma expressão e causa uma exceção de ponto de interrupção se a expressão for **falsa**. O texto da expressão, o nome do arquivo de origem e o número da linha são registrados usando a macro [**DbgLog**](dbglog.md) . Ignorado em compilações de varejo.

## <a name="syntax"></a>Sintaxe


```C++
void KASSERT(
    cond
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*condicional* 
</dt> <dd>

Expressão para avaliar.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa macro não retorna um valor.

## <a name="remarks"></a>Comentários

Ao contrário das macros [**Assert e**](assert.md) [**Execute \_ Assert**](execute-assert.md) , essa macro não exibe uma caixa de mensagem solicitando o usuário. Em compilações de depuração, se a expressão for **false**, a macro automaticamente fará com que uma exceção de ponto de interrupção ocorra.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Wxdebug. h (incluir fluxos. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Macros Assert e Breakpoint](assert-and-breakpoint-macros.md)
</dt> </dl>

 

 




