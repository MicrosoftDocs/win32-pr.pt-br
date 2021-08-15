---
title: atributo oculto
description: O atributo \ hidden\ indica que o item existe, mas não deve ser exibido em um navegador orientado pelo usuário.
ms.assetid: bf1f9270-fb93-4421-804e-d56e2c863bbd
keywords:
- atributo oculto MIDL
topic_type:
- apiref
api_name:
- hidden
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a907a608376d9ad13f97427bd7a941b99221a0f14a6fa9fe35944ced10770b66
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118384041"
---
# <a name="hidden-attribute"></a>atributo oculto

O **\[ atributo \]** oculto indica que o item existe, mas não deve ser exibido em um navegador orientado pelo usuário.

``` syntax
[
    other-attributes, 
    hidden
] 
element element-name
{
    definitions
}

[other-attributes, hidden] function-type function-name(optional-parameter-list);
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*outros atributos* 
</dt> <dd>

Zero ou mais atributos MIDL opcionais.

</dd> <dt>

*Elemento* 
</dt> <dd>

Uma das seguintes diretivas: [**coclass**](coclass.md), [**dispinterface,**](dispinterface.md) [**interface**](interface.md)ou [**biblioteca**](library.md).

</dd> <dt>

*element-name* 
</dt> <dd>

O nome que outros componentes de software podem usar para delinear o elemento atual.

</dd> <dt>

*Definições* 
</dt> <dd>

Especifica instruções que comem a definição do elemento.

</dd> <dt>

*tipo de função* 
</dt> <dd>

Tipo de retorno da função.

</dd> <dt>

*Nome da função* 
</dt> <dd>

Nome usado para invocar a função.

</dd> <dt>

*optional-parameter-list* 
</dt> <dd>

Zero ou mais parâmetros de função.

</dd> </dl>

## <a name="remarks"></a>Comentários

O **\[ atributo \]** oculto permite que você remova membros da interface (blindando-os de uso posterior), mantendo a compatibilidade com o código existente. Você pode usar o **\[ atributo \] oculto** em propriedades, métodos e as instruções de [**coclasse**](coclass.md), [**dispinterface,**](dispinterface.md) [**interface**](interface.md)e [**biblioteca.**](library.md)

Quando especificado para uma biblioteca, o **\[ atributo oculto \]** impede que toda a biblioteca seja exibida. Esse uso destina-se ao uso com controles . Os hosts precisam criar uma nova biblioteca de tipos que envolva o controle com propriedades estendidas.

### <a name="flags"></a>Flags

VARFLAG \_ FHIDDEN, FUNCFLAG \_ FHIDDEN, TYPEFLAG \_ FHIDDEN

## <a name="examples"></a>Exemplos

``` syntax
[hidden, vararg] SAFEARRAY (int) SecretFunc(
    [in, out] SAFEARRAY (variant) *varP) ;

[
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676), 
    hidden, 
    version (3.0)
] 
library HiddenLib 
{
    /* Library definition statements here. */
};
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[Typeflags](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[**dispinterface**](dispinterface.md)
</dt> <dt>

[**coclass**](coclass.md)
</dt> <dt>

[Gerando uma biblioteca de tipos com MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**Interface**](interface.md)
</dt> <dt>

[**Biblioteca**](library.md)
</dt> <dt>

[Sintaxe de arquivo ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Exemplo de arquivo ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> </dl>

 

 