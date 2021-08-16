---
description: Verifica se o processo de chamada tem acesso de gravação a um bloco de memória. Caso não seja, a macro chamará a macro DbgBreak.
ms.assetid: efbb5ca6-0289-487d-b55a-f85b38d0515a
title: Macro ValidateWritePtr (Wxdebug.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ValidateWritePtr
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: f20739093692977b2560de465b916cac12aeb67e2dbf9a6b9488ef8cd61f544f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119072120"
---
# <a name="validatewriteptr-macro"></a>Macro ValidateWritePtr

Verifica se o processo de chamada tem acesso de gravação a um bloco de memória. Caso não seja, a macro chamará a macro [**DbgBreak.**](dbgbreak.md)

> [!Note]  
> Essa macro foi preterida. No SDK Windows para Windows Vista (e posterior), essa macro não faz nada.

 

## <a name="syntax"></a>Sintaxe


```C++
void ValidateWritePtr(
   const void *p,
         UINT cb
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*P* 
</dt> <dd>

Ponteiro para um bloco de memória.

</dd> <dt>

*Cb* 
</dt> <dd>

Tamanho do bloco de memória, em bytes.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Essa macro não retorna um valor.

## <a name="remarks"></a>Comentários

Essa macro é ignorada, a menos que DEBUG, DEBUG ou VFWROBUST seja definido quando o arquivo de DirectShow de classe \_ base for incluído. Essa macro pode ter um custo de desempenho significativo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Wxdebug.h (incluir Fluxos.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Macros de validação de ponteiro](pointer-validation-macros.md)
</dt> </dl>

 

 




