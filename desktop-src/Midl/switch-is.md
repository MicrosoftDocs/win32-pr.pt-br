---
title: Atributo switch_is
description: O atributo \ switch \_ is \ especifica a expressão ou o identificador que atua como o discriminante de União que seleciona o membro Union.
ms.assetid: 93552bdf-6a14-47ce-877e-32ed976bb895
keywords:
- switch_is do atributo MIDL
topic_type:
- apiref
api_name:
- switch_is
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c52661c4fa1ebce57011f4424901dd1ec18250f
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103916778"
---
# <a name="switch_is-attribute"></a>a opção \_ é um atributo

O atributo **\[ switch \_ é \]** especifica a expressão ou o identificador que atua como o discriminante de União que seleciona o membro Union.

``` syntax
typedef struct [[ struct-tag ]] 
{
    [ switch_is(limited-expr) [[ , field-attr-list ]] ] union-type-specifier declarator;
    ...
}

[[ [function-attribute-list] ]] type-specifier [[pointer-declarator]] function-name(
    [ switch_is(limited-expr) [[ , param-attr-list ]] ] union-type [[declarator]]
    , ...);
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*struct-tag* 
</dt> <dd>

Especifica uma marca opcional para uma estrutura.

</dd> <dt>

*expr limitado* 
</dt> <dd>

Especifica uma expressão de linguagem C com suporte no MIDL. Quase todas as expressões de linguagem C têm suporte. O compilador MIDL oferece suporte a expressões condicionais, expressões lógicas, expressões relacionais e expressões aritméticas. MIDL não permite invocações de função em expressões e não permite operadores pré e pós-incremento e pré e pós-backup.

</dd> <dt>

*campo – attr-lista* 
</dt> <dd>

Especifica zero ou mais atributos de campo que se aplicam a um membro de União. Os atributos de campo válidos incluem **\[** [**primeiro \_**](first-is.md), **\]** **\[** o [**último \_**](last-is.md)é **\]** , **\[** o [**comprimento \_ é**](length-is.md) **\]** , **\[** [**máx \_**](max-is.md) **\]** ., **\[** o [**tamanho \_ é**](size-is.md) **\]** ; a cadeia de caracteres de atributos de uso **\[** [](string.md) **\]** , **\[** [**ignorar**](ignore.md) **\]** e **\[** o [**\_ identificador de contexto**](context-handle.md) **\]** ; o atributo de ponteiro **\[** [**ref**](ref.md) **\]** , **\[** [**Unique**](unique.md) **\]** ou **\[** [**PTR**](ptr.md) **\]** ; e para os membros que estão em suas próprias uniões, o **\[** [**\_ tipo de alternância**](switch-type.md)de atributo Union **\]** . Separe vários atributos de campo com vírgulas.

</dd> <dt>

*especificador de tipo Union* 
</dt> <dd>

Especifica o identificador de tipo de [**União**](union.md) . Uma especificação de armazenamento opcional pode preceder o *especificador de tipo*.

</dd> <dt>

*Declarador e Declarador-lista* 
</dt> <dd>

Especifica um Declarador C padrão, como um identificador, Declarador de ponteiro e Declarador de matriz. (Os declaradores de função e as declarações de campo de bits não são permitidas em uniões que são transmitidas em chamadas de procedimento remoto. Esses declaradores são permitidos em uniões que não são transmitidas.) Separe vários declaradores com vírgulas.

</dd> <dt>

*lista de atributos de função* 
</dt> <dd>

Especifica zero ou mais atributos que se aplicam à função. Os atributos de função válidos são **\[** [**retorno de chamada**](callback.md) **\]** , **\[** [**local**](local.md) **\]** ; o atributo de ponteiro **\[ ref \]**, **\[ \] Unique** ou **\[ PTR \]**; e a cadeia de **\[ caracteres \]** de atributos de uso, **\[ ignorar \]** e **\[ \_ \] identificador de contexto**.

</dd> <dt>

*especificador de tipo* 
</dt> <dd>

Especifica um [tipo base](midl-base-types.md), [**struct**](struct.md), [**Union**](union.md), tipo de [**Enumeração**](enum.md) ou identificador de tipo. Uma especificação de armazenamento opcional pode preceder o *especificador de tipo*.

</dd> <dt>

*Declarador de ponteiro* 
</dt> <dd>

Especifica zero ou mais declaradores de ponteiro. Um Declarador de ponteiro é o mesmo que o Declarador de ponteiro usado em C; Ele é construído a partir do \* designador, modificadores, como **distante** e o qualificador [**const**](const.md).

</dd> <dt>

*nome da função* 
</dt> <dd>

Especifica o nome do procedimento remoto.

</dd> <dt>

*param-attr-List* 
</dt> <dd>

Especifica zero ou mais atributos apropriados para o tipo de parâmetro especificado. Atributos de parâmetro podem levar os atributos direcionais para **\[ dentro \]** e para **\[ \] fora**, os atributos de campo **\[ primeiro \_ são \]**, **\[ Last \_ is \]**, **\[ length \_ is \]**, **\[ Max \_ is \]**, **\[ Size \_ is \]** e **\[ switch \_ Type \]**; o atributo ponteiro **\[ ref \]**, **\[ Unique \]** ou **\[ PTR \]**; e o **\[ \_ identificador \] de contexto** e a cadeia de **\[ caracteres \]** de uso de atributos de utilização. O atributo de uso **\[ ignore \]** não pode ser usado como um atributo de parâmetro. Separe vários atributos com vírgulas.

</dd> <dt>

*tipo de União* 
</dt> <dd>

Identifica o especificador de tipo [**Union**](union.md) .

</dd> </dl>

## <a name="remarks"></a>Comentários

O discriminante associado à **\[ opção \_ \]** o atributo deve ser definido no mesmo nível lógico que a União:

-   Quando Union é um parâmetro, o discriminante de União deve ser outro parâmetro.
-   Quando Union é um campo de uma estrutura, discriminante deve ser outro campo da mesma estrutura.

A sequência em uma estrutura ou uma lista de parâmetros de função não é significativa. A União pode preceder ou seguir o discriminante.

O atributo **\[ switch \_ é \]** pode aparecer como um atributo de campo ou como um atributo de parâmetro.

## <a name="examples"></a>Exemplos

``` syntax
typedef [switch_type(short)] union _WILLIE_UNION_TYPE 
{ 
    [case(24)] 
        float fMays; 
    [case(25)] 
        double dMcCovey; 
    [default] 
        ; 
} WILLIE_UNION_TYPE; 
 
typedef struct _WINNER_TYPE 
{ 
    [switch_is(sUniformNumber)] WILLIE_UNION_TYPE w; 
    short sUniformNumber; 
} WINNER_TYPE;
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[Tipos base de MIDL](midl-base-types.md)
</dt> <dt>

[**retorno de chamada**](callback.md)
</dt> <dt>

[**const**](const.md)
</dt> <dt>

[**identificador de contexto \_**](context-handle.md)
</dt> <dt>

[Uniões encapsuladas](encapsulated-unions.md)
</dt> <dt>

[**enumera**](enum.md)
</dt> <dt>

[**primeiro \_ é**](first-is.md)
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

[Uniões não encapsuladas](nonencapsulated-unions.md)
</dt> <dt>

[**ptr**](ptr.md)
</dt> <dt>

[**ref**](ref.md)
</dt> <dt>

[**o tamanho \_ é**](size-is.md)
</dt> <dt>

[**Strings**](string.md)
</dt> <dt>

[**struct**](struct.md)
</dt> <dt>

[**tipo de comutador \_**](switch-type.md)
</dt> <dt>

[**unida**](union.md)
</dt> <dt>

[**diferente**](unique.md)
</dt> </dl>

 

 




