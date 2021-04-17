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
ms.openlocfilehash: 94ce34393ec494f34cce621afc168a4d6bbe4325
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759527"
---
# <a name="validatestringptra-macro"></a>Macro ValidateStringPtrA

Verifica se o processo de chamada tem acesso de leitura a uma cadeia de caracteres ANSI. Caso contrário, a macro chamará a macro [**DbgBreak**](dbgbreak.md) .

> [!Note]  
> Esta macro foi preterida. No SDK do Windows para Windows Vista (e posterior), essa macro não faz nada.

 

## <a name="syntax"></a>Sintaxe


```C++
void ValidateStringPtrA(
   LPCSTR p
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*DTI* 
</dt> <dd>

Ponteiro para uma cadeia de caracteres ANSI terminada em nulo.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa macro não retorna um valor.

## <a name="remarks"></a>Comentários

Essa macro é ignorada a menos que DEBUG, \_ debug ou VFWROBUST seja definido quando o arquivo de cabeçalho da classe base do DirectShow for incluído.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Wxdebug. h (incluir fluxos. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Macros de validação de ponteiro](pointer-validation-macros.md)
</dt> </dl>

 

 




