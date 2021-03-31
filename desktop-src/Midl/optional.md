---
title: atributo opcional
description: O atributo \ optional \ especifica um parâmetro opcional para uma função de membro.
ms.assetid: 683e5c9e-5b25-4beb-99ce-cfae4fee4ea6
keywords:
- atributo opcional MIDL
topic_type:
- apiref
api_name:
- optional
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b446cf2a7a14e5909d2c99d41fd918147d23c6f1
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103823752"
---
# <a name="optional-attribute"></a>atributo opcional

O atributo **\[ opcional \]** especifica um parâmetro opcional para uma função de membro.

``` syntax
return-type function-name([optional [, other-attributes]] parameter-type parameter-name)
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*tipo de retorno* 
</dt> <dd>

Especifica o tipo de retorno da função.

</dd> <dt>

*nome da função* 
</dt> <dd>

Especifica o nome da função, conforme definido no arquivo IDL.

</dd> <dt>

*outros atributos* 
</dt> <dd>

Zero ou mais atributos MIDL opcionais.

</dd> <dt>

*tipo de parâmetro* 
</dt> <dd>

O tipo de dados do parâmetro opcional.

</dd> <dt>

*nome do parâmetro* 
</dt> <dd>

Especifica o nome do parâmetro opcional.

</dd> </dl>

## <a name="remarks"></a>Comentários

O atributo **\[ opcional \]** será válido somente se o parâmetro for do tipo **Variant** ou **Variant** Â \* .

O compilador MIDL aceita a seguinte ordenação de parâmetro (da esquerda para a direita):

1.  Parâmetros necessários (parâmetros que não têm os atributos **\[** [**DefaultValue**](defaultvalue.md) **\]** ou **\[ optional \]** ),
2.  Parâmetros opcionais com ou sem o **\[** [](defaultvalue.md) **\]** atributo DefaultValue,
3.  Parâmetros com o atributo **\[ opcional \]** e sem o **\[** atributo [**DefaultValue**](defaultvalue.md) **\]** ,
4.  **\[** parâmetro [**LCID**](lcid.md) **\]** , se houver,
5.  **\[**[**retval**](retval.md) **\]** meter

Você não pode aplicar o atributo **\[ opcional \]** a um parâmetro que também tenha os **\[** atributos [**LCID**](lcid.md) **\]** ou **\[** [**retval**](retval.md) **\]** .

## <a name="examples"></a>Exemplos

``` syntax
HRESULT MyFunc([in, optional] VARIANT Param1, 
               [out, optional] VARIANT Param2)
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[**ValorPadrão**](defaultvalue.md)
</dt> <dt>

[Gerando uma biblioteca de tipos com MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**LCID**](lcid.md)
</dt> <dt>

[Exemplo de arquivo ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Sintaxe do arquivo ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[**retval**](retval.md)
</dt> </dl>

 

 