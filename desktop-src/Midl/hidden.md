---
title: atributo oculto
description: O atributo \ Hidden \ indica que o item existe, mas não deve ser exibido em um navegador orientado ao usuário.
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
ms.openlocfilehash: 1718351ef84199b60ba720ed2f3569cfa78a0a50
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "105750021"
---
# <a name="hidden-attribute"></a>atributo oculto

O atributo **\[ Hidden \]** indica que o item existe, mas não deve ser exibido em um navegador orientado ao usuário.

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

*elementos* 
</dt> <dd>

Uma das seguintes diretivas: [**coclass**](coclass.md), [**dispinterface**](dispinterface.md), [**interface**](interface.md)ou [**library**](library.md).

</dd> <dt>

*nome do elemento* 
</dt> <dd>

O nome que outros componentes de software podem usar para delinear o elemento atual.

</dd> <dt>

*definições* 
</dt> <dd>

Especifica as instruções que compõem a definição do elemento.

</dd> <dt>

*tipo de função* 
</dt> <dd>

Tipo de retorno da função.

</dd> <dt>

*nome da função* 
</dt> <dd>

Nome usado para invocar a função.

</dd> <dt>

*opcional-lista de parâmetros* 
</dt> <dd>

Zero ou mais parâmetros de função.

</dd> </dl>

## <a name="remarks"></a>Comentários

O atributo **\[ Hidden \]** permite remover membros de sua interface (blindando-os de uso adicional) enquanto mantém a compatibilidade com o código existente. Você pode usar o atributo **\[ \] Hidden** em Propriedades, métodos e as instruções [**coclass**](coclass.md), [**dispinterface**](dispinterface.md), [**interface**](interface.md)e [**library**](library.md) .

Quando especificado para uma biblioteca, o atributo **\[ Hidden \]** impede que toda a biblioteca seja exibida. Esse uso destina-se ao uso com controles. Os hosts precisam criar uma nova biblioteca de tipos que encapsula o controle com propriedades estendidas.

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

[TYPEFLAGS](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[**dispinterface**](dispinterface.md)
</dt> <dt>

[**coclass**](coclass.md)
</dt> <dt>

[Gerando uma biblioteca de tipos com MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**interface**](interface.md)
</dt> <dt>

[**biblioteca**](library.md)
</dt> <dt>

[Sintaxe do arquivo ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Exemplo de arquivo ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> </dl>

 

 