---
description: Verifica se o processo de chamada tem acesso de leitura a um bloco de memória. Caso não seja, a macro chamará a macro DbgBreak.
ms.assetid: 1a70e4e5-e144-4cfe-b6be-c0a70aac9ada
title: Macro ValidateReadPtr (Wxdebug.h)
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
ms.openlocfilehash: caf429437d284a27e4cda830b51e4512375310f2d466a597e58c394a2fea551f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119501626"
---
# <a name="validatereadptr-macro"></a>Macro ValidateReadPtr

Verifica se o processo de chamada tem acesso de leitura a um bloco de memória. Caso não seja, a macro chamará a macro [**DbgBreak.**](dbgbreak.md)

> [!Note]  
> Essa macro foi preterida. No SDK Windows para Windows Vista (e posterior), essa macro não faz nada.

 

## <a name="syntax"></a>Sintaxe


```C++
void ValidateReadPtr(
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

 

 




