---
description: Verifica se o processo de chamada tem acesso de leitura a uma cadeia de caracteres ANSI. Caso contrário, a macro chamará a macro DbgBreak.
ms.assetid: 44be67f8-9896-4360-82de-083a5f28a3d0
title: Macro ValidateStringPtrA (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ValidateStringPtrA
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: 26a0e000f5b2b8de645924300eb650a05a66a4b57c16c5eda3f124e7bc0903a8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119432096"
---
# <a name="validatestringptra-macro"></a>Macro ValidateStringPtrA

Verifica se o processo de chamada tem acesso de leitura a uma cadeia de caracteres ANSI. Caso contrário, a macro chamará a macro [**DbgBreak**](dbgbreak.md) .

> [!Note]  
> Esta macro foi preterida. no SDK do Windows para Windows Vista (e posterior), essa macro não faz nada.

 

## <a name="syntax"></a>Sintaxe


```C++
void ValidateStringPtrA(
   LPCSTR p
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*p* 
</dt> <dd>

Ponteiro para uma cadeia de caracteres ANSI terminada em nulo.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Essa macro não retorna um valor.

## <a name="remarks"></a>Comentários

essa macro é ignorada a menos que DEBUG, \_ debug ou VFWROBUST seja definido quando o arquivo de cabeçalho da classe base DirectShow for incluído.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Wxdebug. h (incluir Fluxos. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Macros de validação de ponteiro](pointer-validation-macros.md)
</dt> </dl>

 

 




