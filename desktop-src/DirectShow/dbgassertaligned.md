---
description: Testa se um ponteiro está alinhado a um limite especificado. Caso contrário, essa macro invoca a macro ASSERT. Ignorado em compilações de varejo.
ms.assetid: 4d9ec3a9-7107-45a3-a7aa-28d6e38fa92a
title: Macro DbgAssertAligned (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgAssertAligned
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: 22b357f7f28e9df04ce36636e3972dbadc3036a6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105782201"
---
# <a name="dbgassertaligned-macro"></a>Macro DbgAssertAligned

Testa se um ponteiro está alinhado a um limite especificado. Caso contrário, essa macro invoca a macro [**Assert**](assert.md) . Ignorado em compilações de varejo.

## <a name="syntax"></a>Sintaxe


```C++
void DbgAssertAligned(
    ptr,
    alignment
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ptr* 
</dt> <dd>

Variável de ponteiro.

</dd> <dt>

*sintonia* 
</dt> <dd>

Alinhamento necessário.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa macro não retorna um valor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Wxdebug. h (incluir fluxos. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Macros Assert e Breakpoint](assert-and-breakpoint-macros.md)
</dt> </dl>

 

 




