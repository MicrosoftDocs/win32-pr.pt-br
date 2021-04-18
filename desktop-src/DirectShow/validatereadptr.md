---
description: Verifica se o processo de chamada tem acesso de leitura a um bloco de memória. Caso contrário, a macro chamará a macro DbgBreak.
ms.assetid: 1a70e4e5-e144-4cfe-b6be-c0a70aac9ada
title: Macro ValidateReadPtr (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ValidateReadPtr
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: aa8093ecbd428cafbf1266179b1489cac0d69c4d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105787124"
---
# <a name="validatereadptr-macro"></a>Macro ValidateReadPtr

Verifica se o processo de chamada tem acesso de leitura a um bloco de memória. Caso contrário, a macro chamará a macro [**DbgBreak**](dbgbreak.md) .

> [!Note]  
> Esta macro foi preterida. No SDK do Windows para Windows Vista (e posterior), essa macro não faz nada.

 

## <a name="syntax"></a>Sintaxe


```C++
void ValidateReadPtr(
   const void *p,
         UINT cb
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*DTI* 
</dt> <dd>

Ponteiro para um bloco de memória.

</dd> <dt>

*CB* 
</dt> <dd>

Tamanho do bloco de memória, em bytes.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa macro não retorna um valor.

## <a name="remarks"></a>Comentários

Essa macro é ignorada a menos que DEBUG, \_ debug ou VFWROBUST seja definido quando o arquivo de cabeçalho da classe base do DirectShow for incluído. Essa macro pode ter um custo de desempenho significativo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Wxdebug. h (incluir fluxos. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Macros de validação de ponteiro](pointer-validation-macros.md)
</dt> </dl>

 

 




