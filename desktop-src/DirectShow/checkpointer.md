---
description: Verifica se um ponteiro é NULL. Se o ponteiro for NULL, a função ou o método no qual a macro aparece retornará o valor especificado.
ms.assetid: eca73fbf-5fd8-4b76-af06-ca0c22510b55
title: Macro CheckPointer (Wxdebug.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CheckPointer
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: ef1fa2370def45321958862ebaf3ded341b13f45ddae1ecafdc4a17e937aca08
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119999286"
---
# <a name="checkpointer-macro"></a>Macro CheckPointer

Verifica se um ponteiro é **NULL.** Se o ponteiro for **NULL,** a função ou o método no qual a macro aparece retornará o valor especificado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT CheckPointer(
    p,
    ret
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*P* 
</dt> <dd>

Ponteiro para verificar.

</dd> <dt>

*Ret* 
</dt> <dd>

Valor que a função ou método retornará se *p* for **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valor retornado

A função ao redor *retornará ret* se *p* for **NULL.** Caso contrário, a macro não faz com que a função ao redor retorne.

## <a name="examples"></a>Exemplos


```
HRESULT MyFunction(VOID *pSomeParameter)
{
    // Return E_INVALIDARG if pSomeParameter is NULL.
    CheckPointer(pSomeParameter, E_INVALIDARG)

    // Rest of the function (not shown).
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Wxdebug.h (incluir Fluxos.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Macros de validação de ponteiro](pointer-validation-macros.md)
</dt> </dl>

 

 




