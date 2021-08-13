---
title: atributo personalizado
description: O atributo \ custom\ cria um atributo definido pelo usuário.
ms.assetid: 63c93eca-c9c1-4c14-9f46-aa78b01d9ff8
keywords:
- atributo personalizado MIDL
topic_type:
- apiref
api_name:
- custom
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ace6a558da428da07a432653391e0e48b7a5545bb1a83eb40d9c950abfa9d9aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118643665"
---
# <a name="custom-attribute"></a>atributo personalizado

O **\[ atributo \]** personalizado cria um atributo definido pelo usuário.

``` syntax
[custom(attribute-id, attribute-value),attribute-list] element-type element-name
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*attribute-id* 
</dt> <dd>

O GUID do atributo personalizado.

</dd> <dt>

*atributo-valor* 
</dt> <dd>

O valor que o atributo contém. O valor deve ser aquele que pode ser colocado em um tipo VARIANT.

</dd> <dt>

*lista de atributos* 
</dt> <dd>

Outros atributos, como **\[** [**uuid**](uuid.md) **\]** e **\[** [**helpstring,**](helpstring.md) **\]** que se aplicam a esse elemento.

</dd> <dt>

*tipo de elemento* 
</dt> <dd>

O tipo de elemento ao qual o atributo personalizado se aplica. Pode ser uma instrução de biblioteca, informações de tipo, uma variável, uma função ou um parâmetro. Não é possível usar um atributo personalizado em um membro de uma coclasse.

</dd> <dt>

*element-name* 
</dt> <dd>

O nome do elemento.

</dd> </dl>

## <a name="remarks"></a>Comentários

Use o **\[ atributo \]** personalizado para definir seu próprio atributo. Por exemplo, você pode criar um atributo com valor de cadeia de caracteres que fornece o ProgID para uma classe.

Para recuperar um valor de atributo personalizado, chame um dos seguintes:

-   ITypeLib2::GetCustData(rguid, pvarVal)
-   ITypeInfo2::GetCustData(rguid, pvarVal)
-   ITypeInfo2::GetFuncCustData(index, rguid, pvarVal)
-   ITypeInfo2::GetVarCustData(index, rguid, pvarval)
-   ITypeInfo2::GetParamCustData(indexFunc, indexParam, rguid, pvarVal)

## <a name="see-also"></a>Confira também

<dl> <dt>

[Gerando uma biblioteca de tipos com MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**helpstring**](helpstring.md)
</dt> <dt>

[**Biblioteca**](library.md)
</dt> <dt>

[Exemplo de arquivo ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Sintaxe de arquivo ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[**Uuid**](uuid.md)
</dt> </dl>

 

 