---
title: atributo arrays
description: Matrizes são coleções homogêneas de dados acessados por um índice ou número de elemento.
ms.assetid: 375fb795-8f18-45b7-898c-99f1273746d8
keywords:
- atributo arrays MIDL
topic_type:
- apiref
api_name:
- arrays
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57682252c36284a89a3fb659c69446902c3d0181cbf82d494b200b5769e087e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117808274"
---
# <a name="arrays-attribute"></a>atributo arrays

Matrizes são coleções homogêneas de dados acessados por um índice ou número de elemento.

``` syntax
typedef [ [type-attr-list] ] type-specifier [pointer-decl] array-declarator;

typedef [ [type-attr-list] ] struct [ tag ] 
{
    [ [ field-attribute-list ] ] type-specifier [pointer-decl] array-declarator;
    ...
};

typedef [ [type-attr-list] ] union [ tag ] 
{
    [ case (limited-expression [ , ... ] ) ]
  [ [ field-attribute-list ] ] type-specifier [pointer-decl] array-declarator;
  [ [ default ]
  [ [ field-attribute-list ] ] type-specifier [pointer-decl] array-declarator;
  ]
};

[[ [function-attribute-list] ]] type-specifier [[pointer-decl]] function-name(
        [[ [param-attr-list] ]] type-specifier [[pointer-decl]] array-declarator
        , ...);
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*type-attr-list* 
</dt> <dd>

Especifica zero ou mais atributos que se aplicam ao tipo. Os atributos de tipo [**válidos \[ \]**](handle.md)incluem handle , switch [**\[ \_ type \]**](switch-type.md), [**\[ transmit \_ \] as**](transmit-as.md); o atributo de ponteiro [**\[ ref \]**](ref.md), [**\[ unique \]**](unique.md)ou ptr ; [**\[ \]**](string.md) [**\[ \]**](ignore.md) [**\[ \_ \]**](context-handle.md)e o [**\[ identificador \]**](ptr.md)de contexto de atributos de uso , cadeia de caracteres e ignorar . Separe vários atributos com vírgulas.

</dd> <dt>

*especificador de tipo* 
</dt> <dd>

Especifica o identificador de tipo, o tipo base, [**o struct**](struct.md), [**a união**](union.md)ou [**o tipo de enum.**](enum.md) A especificação de tipo pode incluir uma especificação de armazenamento opcional.

</dd> <dt>

*pointer-decl* 
</dt> <dd>

Especifica zero ou mais declaradores de ponteiro. Um declarador de ponteiro é o mesmo que o declarador de ponteiro usado em C, construído do **\* *_ designator,*** modificadores como _ far e o qualificador [**const**](const.md).

</dd> <dt>

*array-declarator* 
</dt> <dd>

Especifica o nome da matriz, seguido por um dos seguintes constructos **\[ \]** para cada dimensão da matriz: " ", " **\[\*\]** ", " **\[** _const1_ *_\]_* ", ou " **\[** _lower... superior_ *_\]_* " em que *inferior* *e superior* são valores constantes que representam os limites inferior e superior. A constante *inferior* deve ser avaliada como zero.

</dd> <dt>

*Tag* 
</dt> <dd>

Especifica uma marca opcional para a estrutura ou a união.

</dd> <dt>

*field-attribute-list* 
</dt> <dd>

Especifica zero ou mais atributos de campo que se aplicam à estrutura, membro de união ou parâmetro de função. [**\[ \]**](string.md) [**\[ \_ \]**](switch-type.md) [**\[ \_ \]**](last-is.md) [**\[ \_ \]**](length-is.md) [**\[ \_ \]**](max-is.md) [**\[ \_ \]**](size-is.md) [**\[ \]**](ref.md) [**\[ \]**](unique.md) [**\[ \]**](ignore.md) [**\[ \]**](ptr.md) [**\[ Os atributos de campo válidos incluem primeiro é , o último é , o comprimento é , max é , o tamanho é ; a cadeia de caracteres de atributos de uso e ignoram ; os atributos de ponteiro ref , unique e ptr ; e o tipo de comutador de atributo de união . \_ \]**](first-is.md) Separe vários atributos de campo com vírgulas. Observe que, dos atributos listados acima, **\[ primeiro \_ é \]**, **\[ o último \_ é \]** e [**\[ ignore \]**](ignore.md) não são válidos para uniões.

</dd> <dt>

*expressão limitada* 
</dt> <dd>

Especifica uma expressão da linguagem C. O compilador MIDL dá suporte a expressões condicionais, expressões lógicas, expressões relacionais e expressões aritméticas. MIDL não permite invocações de função em expressões e não permite operadores de incremento e decremento.

</dd> <dt>

*function-attribute-list* 
</dt> <dd>

Especifica zero ou mais atributos que se aplicam à função. Os atributos de função válidos são [**\[ retorno \]**](callback.md)de chamada , [**\[ local \]**](local.md); o atributo de ponteiro [**\[ \] ref**](ref.md), [**\[ exclusivo \]**](unique.md)ou [**\[ ptr \]**](ptr.md); [**\[ \_ \]**](context-handle.md) [**\[ \]**](string.md)e a cadeia de caracteres de atributos de uso e o alça de contexto .

</dd> <dt>

*Nome da função* 
</dt> <dd>

Especifica o nome do procedimento remoto.

</dd> <dt>

*param-attr-list* 
</dt> <dd>

Especifica os atributos direcionais e um ou mais atributos de campo opcionais que se aplicam ao parâmetro de matriz. Atributos de campo válidos [**\[ \_ incluem \] max é**](max-is.md), size [**\[ \_ é \]**](size-is.md), length [**\[ \_ é \]**](length-is.md), first [**\[ \_ is \]**](first-is.md)e last [**\[ \_ is \]**](last-is.md).

</dd> </dl>

## <a name="remarks"></a>Comentários

As matrizes em MIDL usam um estilo semelhante a , mas não exatamente o mesmo que C e C++. Para obter mais informações, consulte [Matrizes MIDL](midl-arrays.md).

## <a name="see-also"></a>Confira também

<dl> <dt>

[**retorno de chamada**](callback.md)
</dt> <dt>

[**const**](const.md)
</dt> <dt>

[**alça de \_ contexto**](context-handle.md)
</dt> <dt>

[**Enum**](enum.md)
</dt> <dt>

[**primeiro \_ é**](first-is.md)
</dt> <dt>

[**Lidar com**](handle.md)
</dt> <dt>

[Arquivo IDL (definição de interface)](interface-definition-idl-file.md)
</dt> <dt>

[**Ignorar**](ignore.md)
</dt> <dt>

[**o último \_ é**](last-is.md)
</dt> <dt>

[**length \_ é**](length-is.md)
</dt> <dt>

[**Local**](local.md)
</dt> <dt>

[**max \_ é**](max-is.md)
</dt> <dt>

[**ptr**](ptr.md)
</dt> <dt>

[**ref**](ref.md)
</dt> <dt>

[**size \_ é**](size-is.md)
</dt> <dt>

[**string**](string.md)
</dt> <dt>

[**Struct**](struct.md)
</dt> <dt>

[**tipo \_ switch**](switch-type.md)
</dt> <dt>

[**transmitir \_ como**](transmit-as.md)
</dt> <dt>

[**União**](union.md)
</dt> <dt>

[**Único**](unique.md)
</dt> </dl>

 

 




