---
description: Avalia uma expressão e causa uma exceção de ponto de interrupção se a expressão for FALSE. O texto da expressão, o nome do arquivo de origem e o número de linha são registrados usando a macro DbgLog. Ignorado em builds de varejo.
ms.assetid: fd116403-df23-490f-b3a8-b2a8bf2b4a5f
title: Macro KASSERT (Wxdebug.h)
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
ms.openlocfilehash: a1eb6738ea3e9d4535bf9f8291dc71349d67bb51d143b6bc73e83290f36657cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117817053"
---
# <a name="kassert-macro"></a>Macro KASSERT

Avalia uma expressão e causa uma exceção de ponto de interrupção se a expressão for **FALSE.** O texto da expressão, o nome do arquivo de origem e o número de linha são registrados usando a [**macro DbgLog.**](dbglog.md) Ignorado em builds de varejo.

## <a name="syntax"></a>Sintaxe


```C++
void KASSERT(
    cond
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Cond* 
</dt> <dd>

Expressão para avaliar.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Essa macro não retorna um valor.

## <a name="remarks"></a>Comentários

Ao contrário das macros [**ASSERT**](assert.md) e [**EXECUTE \_ ASSERT,**](execute-assert.md) essa macro não exibe uma caixa de mensagem solicitando o usuário. Em builds de depuração, se a expressão for **FALSE**, a macro fará com que ocorra automaticamente uma exceção de ponto de interrupção.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Wxdebug.h (incluir Fluxos.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Macros assert e breakpoint](assert-and-breakpoint-macros.md)
</dt> </dl>

 

 




