---
description: Verifica se um ponteiro é nulo. Se o ponteiro for nulo, a função ou o método no qual a macro aparece retornará o valor especificado.
ms.assetid: eca73fbf-5fd8-4b76-af06-ca0c22510b55
title: Macro do ponto de verificação (Wxdebug. h)
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
ms.openlocfilehash: 04f442303e520ef758a3576d21c2df810ef26fb2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748200"
---
# <a name="checkpointer-macro"></a>Macro do ponto de verificação

Verifica se um ponteiro é **nulo**. Se o ponteiro for **nulo**, a função ou o método no qual a macro aparece retornará o valor especificado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT CheckPointer(
    p,
    ret
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*DTI* 
</dt> <dd>

Ponteiro para verificar.

</dd> <dt>

*RET* 
</dt> <dd>

Valor que a função ou método retorna se *p* for **nulo**.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

A função ao redor retornará *RET* se *p* for **NULL**. Caso contrário, a macro não fará com que a função ao redor seja retornada.

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
| parâmetro<br/> | <dl> <dt>Wxdebug. h (incluir fluxos. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Macros de validação de ponteiro](pointer-validation-macros.md)
</dt> </dl>

 

 




