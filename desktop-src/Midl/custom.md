---
title: atributo personalizado
description: O atributo \ custom \ cria um atributo definido pelo usuário.
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
ms.openlocfilehash: ef7c4210091cc028d7724cb40724f22a91eb7d74
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "105768735"
---
# <a name="custom-attribute"></a>atributo personalizado

O atributo **\[ personalizado \]** cria um atributo definido pelo usuário.

``` syntax
[custom(attribute-id, attribute-value),attribute-list] element-type element-name
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ID do atributo* 
</dt> <dd>

O GUID do atributo personalizado.

</dd> <dt>

*atributo-valor* 
</dt> <dd>

O valor que o atributo mantém. O valor deve ser um que possa ser colocado em um tipo VARIANT.

</dd> <dt>

*lista de atributos* 
</dt> <dd>

Outros atributos, como **\[** [**UUID**](uuid.md) **\]** e **\[** [**HelpString**](helpstring.md) **\]** , que se aplicam a esse elemento.

</dd> <dt>

*tipo de elemento* 
</dt> <dd>

O tipo de elemento ao qual o atributo personalizado se aplica. Isso pode ser uma instrução de biblioteca, informações de tipo, uma variável, uma função ou um parâmetro. Você não pode usar um atributo personalizado em um membro de uma coclass.

</dd> <dt>

*nome do elemento* 
</dt> <dd>

O nome do elemento.

</dd> </dl>

## <a name="remarks"></a>Comentários

Use o atributo **\[ personalizado \]** para definir seu próprio atributo. Por exemplo, você pode criar um atributo com valor de cadeia de caracteres que forneça a ProgID para uma classe.

Para recuperar um valor de atributo personalizado, chame um dos seguintes:

-   ITypeLib2::GetCustData(rguid, pvarVal)
-   ITypeInfo2::GetCustData(rguid, pvarVal)
-   ITypeInfo2:: GetFuncCustData (index, rguid, pvarVal)
-   ITypeInfo2:: GetVarCustData (index, rguid, pvarVal)
-   ITypeInfo2::GetParamCustData(indexFunc, indexParam, rguid, pvarVal)

## <a name="see-also"></a>Confira também

<dl> <dt>

[Gerando uma biblioteca de tipos com MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**helpstring**](helpstring.md)
</dt> <dt>

[**biblioteca**](library.md)
</dt> <dt>

[Exemplo de arquivo ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Sintaxe do arquivo ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[**personalizado**](uuid.md)
</dt> </dl>

 

 