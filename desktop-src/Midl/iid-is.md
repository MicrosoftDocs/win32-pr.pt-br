---
title: Atributo iid_is
description: O atributo \ IID \_ é \ pointer especifica o IID da interface com apontada por um ponteiro de interface.
ms.assetid: 7fb5eb87-15d8-4717-b79a-e8a81f2f7293
keywords:
- iid_is do atributo MIDL
topic_type:
- apiref
api_name:
- iid_is
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e94c6f46a6828e81817e45ff6eb6eb8245b00a61
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104006376"
---
# <a name="iid_is-attribute"></a>IID \_ é atributo

O **\[ IID \_ é \]** um atributo de ponteiro especifica o IID da interface com apontada por um ponteiro de interface.

``` syntax
[ iid_is(limited-expression) ]
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*expressão limitada* 
</dt> <dd>

Especifica uma expressão de linguagem C. O compilador MIDL oferece suporte a expressões condicionais, expressões lógicas, expressões relacionais e expressões aritméticas. MIDL não permite invocações de função em expressões e não permite operadores de incremento e decréscimo.

</dd> </dl>

## <a name="remarks"></a>Comentários

Você pode usar o **\[ IID \_ \]** em listas de atributos para parâmetros de função e para membros de estrutura ou União. Os stubs usam o IID para determinar como realizar marshaling do ponteiro de interface. Isso é útil para um ponteiro de interface que é digitado como um parâmetro de classe base.

Os arquivos que usam o **\[ IID \_ é \]** o atributo devem ser compilados com o compilador MIDL no modo padrão, que não está usando a opção [**/OSF**](-osf.md)

## <a name="examples"></a>Exemplos

``` syntax
HRESULT    CreateInstance( 
    [in] REFIID riid, 
    [out, iid_is(riid)] IUnknown ** ppvObject);
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[**objeto**](object.md)
</dt> <dt>

[**personalizado**](uuid.md)
</dt> </dl>

 

 




