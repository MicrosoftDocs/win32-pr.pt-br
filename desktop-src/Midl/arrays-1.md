---
title: atributo de matrizes
description: As matrizes são coleções homogêneas de dados acessados por um índice ou número de elemento.
ms.assetid: 375fb795-8f18-45b7-898c-99f1273746d8
keywords:
- atributo de matrizes MIDL
topic_type:
- apiref
api_name:
- arrays
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e189eb1784a4ff24b799c7a4d4482d0f56b20e3
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "105758785"
---
# <a name="arrays-attribute"></a>atributo de matrizes

As matrizes são coleções homogêneas de dados acessados por um índice ou número de elemento.

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

*tipo-attr-List* 
</dt> <dd>

Especifica zero ou mais atributos que se aplicam ao tipo. Atributos de tipo válidos [**\[ incluem \] identificador**](handle.md), [**\[ \_ tipo \] de comutador**](switch-type.md), [**\[ transmissão \_ como \]**](transmit-as.md); o atributo de ponteiro [**\[ ref \]**](ref.md), [**\[ Unique \]**](unique.md)ou [**\[ PTR \]**](ptr.md); e o [**\[ \_ identificador \] de contexto**](context-handle.md)de atributos de uso, Cadeia de [**\[ caracteres \]**](string.md)e [**\[ ignorar \]**](ignore.md). Separe vários atributos com vírgulas.

</dd> <dt>

*especificador de tipo* 
</dt> <dd>

Especifica o identificador de tipo, tipo base, [**struct**](struct.md), [**União**](union.md)ou tipo de [**Enumeração**](enum.md) . A especificação de tipo pode incluir uma especificação de armazenamento opcional.

</dd> <dt>

*ponteiro-decl* 
</dt> <dd>

Especifica zero ou mais declaradores de ponteiro. Um Declarador de ponteiro é o mesmo que o Declarador de ponteiro usado em C, construído a partir do **\*** designador, modificadores como **distante** e o qualificador [**const**](const.md).

</dd> <dt>

*Declarador de matriz* 
</dt> <dd>

Especifica o nome da matriz, seguido por uma das seguintes construções para cada dimensão da matriz: "**\[ \]**", " **\[\*\]** ", "**\[ ***Const1*** \]**" ou "**\[ ***Lower...*** Upper \]**"onde *Lower* e *Upper* são valores constantes que representam os limites inferior e superior. A constante *inferior* deve ser avaliada como zero.

</dd> <dt>

*Tags* 
</dt> <dd>

Especifica uma marca opcional para a estrutura ou União.

</dd> <dt>

*lista de atributos de campo* 
</dt> <dd>

Especifica zero ou mais atributos de campo que se aplicam à estrutura, ao membro de União ou ao parâmetro de função. Os atributos de campo válidos incluem [**\[ primeiro \_ \]**](first-is.md), o [**\[ último \_ \]**](last-is.md)é [**\[ \]**](ptr.md) [**\[ \]**](ref.md) [**\[ \]**](unique.md) [**\[ \_ , comprimento é \]**](length-is.md), [**\[ máximo \_ é \]**](max-is.md), [**\[ tamanho, a cadeia de \_ caracteres de atributos de uso e ignore; os atributos de ponteiro ref, Unique e PTR; e o tipo de opção de atributo Union. \]**](size-is.md) [**\[ \_ \]**](switch-type.md) [**\[ \]**](string.md) [**\[ \]**](ignore.md) Separe vários atributos de campo com vírgulas. Observe que os atributos listados acima, **\[ primeiro \_ é \]**, **\[ último \_ \]** são e [**\[ ignorar \]**](ignore.md) não são válidos para uniões.

</dd> <dt>

*expressão limitada* 
</dt> <dd>

Especifica uma expressão de linguagem C. O compilador MIDL oferece suporte a expressões condicionais, expressões lógicas, expressões relacionais e expressões aritméticas. MIDL não permite invocações de função em expressões e não permite operadores de incremento e decréscimo.

</dd> <dt>

*lista de atributos de função* 
</dt> <dd>

Especifica zero ou mais atributos que se aplicam à função. Os atributos de função válidos são [**\[ retorno de \] chamada**](callback.md), [**\[ local \]**](local.md); o atributo de ponteiro [**\[ ref \]**](ref.md), [**\[ Unique \]**](unique.md)ou [**\[ PTR \]**](ptr.md); e a cadeia de [**\[ caracteres \]**](string.md)de atributos de uso e o [**\[ \_ identificador \] de contexto**](context-handle.md).

</dd> <dt>

*nome da função* 
</dt> <dd>

Especifica o nome do procedimento remoto.

</dd> <dt>

*param-attr-List* 
</dt> <dd>

Especifica os atributos direcionais e um ou mais atributos de campo opcionais que se aplicam ao parâmetro de matriz. Os atributos de campo válidos incluem [**\[ Max \_ is \]**](max-is.md), [**\[ Size \_ \] is**](size-is.md), [**\[ length \_ is \]**](length-is.md), [**\[ First \_ is \]**](first-is.md)e [**\[ Last \_ is \]**](last-is.md).

</dd> </dl>

## <a name="remarks"></a>Comentários

As matrizes no MIDL usam um estilo semelhante a, mas não exatamente igual a C e C++. Para obter mais informações, consulte [matrizes de MIDL](midl-arrays.md).

## <a name="see-also"></a>Confira também

<dl> <dt>

[**retorno de chamada**](callback.md)
</dt> <dt>

[**const**](const.md)
</dt> <dt>

[**identificador de contexto \_**](context-handle.md)
</dt> <dt>

[**enumera**](enum.md)
</dt> <dt>

[**primeiro \_ é**](first-is.md)
</dt> <dt>

[**processamento**](handle.md)
</dt> <dt>

[Arquivo de definição de interface (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**ignorar**](ignore.md)
</dt> <dt>

[**último \_ é**](last-is.md)
</dt> <dt>

[**comprimento \_ é**](length-is.md)
</dt> <dt>

[**local**](local.md)
</dt> <dt>

[**máximo \_ é**](max-is.md)
</dt> <dt>

[**ptr**](ptr.md)
</dt> <dt>

[**ref**](ref.md)
</dt> <dt>

[**o tamanho \_ é**](size-is.md)
</dt> <dt>

[**string**](string.md)
</dt> <dt>

[**struct**](struct.md)
</dt> <dt>

[**tipo de comutador \_**](switch-type.md)
</dt> <dt>

[**transmitir \_ como**](transmit-as.md)
</dt> <dt>

[**unida**](union.md)
</dt> <dt>

[**diferente**](unique.md)
</dt> </dl>

 

 




