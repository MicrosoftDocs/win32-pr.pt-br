---
title: Atributo iid_is
description: O atributo \ iid \_ is\ ponteiro especifica a IID da interface COM apontada por um ponteiro de interface.
ms.assetid: 7fb5eb87-15d8-4717-b79a-e8a81f2f7293
keywords:
- iid_is atributo MIDL
topic_type:
- apiref
api_name:
- iid_is
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74553fdb1e3020d49eca7dfdd219354a4690056c45126b3af208395117ade991
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118383863"
---
# <a name="iid_is-attribute"></a>iid \_ é atributo

O **\[ atributo \_ \] iid is** pointer especifica a IID da interface COM apontada por um ponteiro de interface.

``` syntax
[ iid_is(limited-expression) ]
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*expressão limitada* 
</dt> <dd>

Especifica uma expressão da linguagem C. O compilador MIDL dá suporte a expressões condicionais, expressões lógicas, expressões relacionais e expressões aritméticas. MIDL não permite invocações de função em expressões e não permite operadores de incremento e decremento.

</dd> </dl>

## <a name="remarks"></a>Comentários

Você pode usar **\[ iid \_ está em listas \]** de atributos para parâmetros de função e para membros de estrutura ou união. Os stubs usam o IID para determinar como fazer marshal do ponteiro da interface. Isso é útil para um ponteiro de interface que é digitado como um parâmetro de classe base.

Os arquivos que usam o **\[ atributo iid \_ is \]** devem ser compilados com o compilador MIDL no modo padrão, que não está usando a opção [**/osf.**](-osf.md)

## <a name="examples"></a>Exemplos

``` syntax
HRESULT    CreateInstance( 
    [in] REFIID riid, 
    [out, iid_is(riid)] IUnknown ** ppvObject);
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto**](object.md)
</dt> <dt>

[**Uuid**](uuid.md)
</dt> </dl>

 

 




