---
description: Verifica se o processo de chamada tem acesso de leitura/gravação a um bloco de memória. Caso contrário, a macro chamará a macro DbgBreak.
ms.assetid: 215f6db9-67b6-47e1-bee1-dc37082ae2b8
title: Macro ValidateReadWritePtr (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ValidateReadWritePtr
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: ec4d1c0440d0747024efadaa441ca062da512283f5a01f29be12b19c0f7c0567
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119755656"
---
# <a name="validatereadwriteptr-macro"></a>Macro ValidateReadWritePtr

Verifica se o processo de chamada tem acesso de leitura/gravação a um bloco de memória. Caso contrário, a macro chamará a macro [**DbgBreak**](dbgbreak.md) .

> [!Note]  
> Esta macro foi preterida. no SDK do Windows para Windows Vista (e posterior), essa macro não faz nada.

 

## <a name="syntax"></a>Sintaxe


```C++
void ValidateReadWritePtr(
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

## <a name="return-value"></a>Valor retornado

Essa macro não retorna um valor.

## <a name="remarks"></a>Comentários

essa macro é ignorada a menos que DEBUG, \_ debug ou VFWROBUST seja definido quando o arquivo de cabeçalho da classe base DirectShow for incluído. Essa macro pode ter um custo de desempenho significativo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Wxdebug. h (incluir Fluxos. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Macros de validação de ponteiro](pointer-validation-macros.md)
</dt> </dl>

 

 




