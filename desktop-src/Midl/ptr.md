---
title: atributo ptr
description: O atributo \ PTR \ designa um ponteiro como um ponteiro completo.
ms.assetid: a1233a25-b651-4a01-8abf-a64dc9ee168e
keywords:
- MIDL do atributo PTR
topic_type:
- apiref
api_name:
- ptr
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53e9b85be5e9073a272dafd63a2a01ba64f440f90cc5d9c41f44260f235f9ab5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119927416"
---
# <a name="ptr-attribute"></a>atributo ptr

O atributo **\[ PTR \]** designa um ponteiro como um ponteiro completo.

``` syntax
pointer_default(ptr)

typedef [ ptr [ , type-attribute-list ] ] type-specifier declarator-list; 

typedef [ struct | union ]
{
    [ ptr [ , field-attribute-list ] ] type-specifier declarator-list;
    ...
}

[ ptr [ , function-attribute-list ] ] type-specifier ptr-decl function-name(
    [ [ parameter-attribute-list ] ] type-specifier [standard-declarator]
    , ...);

[[ [ function-attribute-list ] ]] type-specifier [[ptr-decl]] function-name(
    [ ptr [[ , parameter-attribute-list ]] ] type-specifier [[standard-declarator]]
    , ...);
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lista de atributos de tipo* 
</dt> <dd>

Especifica um ou mais atributos que se aplicam ao tipo. Atributos de tipo válidos incluem **\[** [**identificador**](handle.md) **\]** , **\[** [**\_ tipo de comutador**](switch-type.md) **\]** , **\[** [**transmissão \_ como**](transmit-as.md) **\]** ; o atributo de ponteiro **\[** [**ref**](ref.md) **\]** , **\[** [**Unique**](unique.md)ou **\[ PTR \]**; e o identificador de contexto de atributos de uso **\[** [**\_**](context-handle.md) **\]** , **\[** [**cadeia de caracteres**](string.md) **\]** e **\[** [**ignorar**](ignore.md) **\]** . Separe vários atributos com vírgulas.

</dd> <dt>

*especificador de tipo* 
</dt> <dd>

Especifica um tipo de [base](midl-base-types.md), [**struct**](struct.md), [**Union**](union.md)ou tipo de [**Enumeração**](enum.md) ou identificador de tipo. Uma especificação de armazenamento opcional pode preceder o *especificador de tipo*.

</dd> <dt>

*padrão-Declarador* 
</dt> <dd>

Especifica um Declarador C padrão, como um identificador, um Declarador de ponteiro ou um Declarador de matriz. Para obter mais informações, consulte [matriz e Sized-Pointer atributos](array-and-sized-pointer-attributes.md), [**matrizes**](arrays-1.md)e [matrizes e ponteiros](/windows/desktop/Rpc/arrays-and-pointers).

</dd> <dt>

*Declarador-lista* 
</dt> <dd>

Especifica os declaradores padrão C, como identificadores, declaradores de ponteiro e declaradores de matriz. Para obter mais informações, consulte [matriz e Sized-Pointer atributos](array-and-sized-pointer-attributes.md), [**matrizes**](arrays-1.md)e [matrizes e ponteiros](/windows/desktop/Rpc/arrays-and-pointers). A *lista de declaradores* consiste em um ou mais declaradores separados por vírgulas. O identificador de nome de parâmetro no Declarador de função é opcional.

</dd> <dt>

*lista de atributos de campo* 
</dt> <dd>

Especifica zero ou mais atributos de campo que se aplicam ao parâmetro de função ou membro da estrutura ou União. Os atributos de campo válidos incluem **\[** [**primeiro \_**](first-is.md) **\]** , **\[** o [**último \_**](last-is.md)é **\]** , **\[** o [**comprimento \_ é**](length-is.md) **\]** , **\[** [**\_ máx**](max-is.md) **\]** ., **\[** o [**tamanho \_ é**](size-is.md) **\]** ; a cadeia de caracteres de atributos de uso **\[** [](string.md) **\]** , **\[** [**ignorar**](ignore.md) **\]** e **\[** o [**\_ identificador de contexto**](context-handle.md) **\]** ; o atributo de ponteiro **\[** [**ref**](ref.md) **\]** , **\[** [**Unique**](unique.md) **\]** ou **\[ PTR \]**; e o **\[** [**\_ tipo de opção**](switch-type.md)de atributo Union **\]** . Separe vários atributos de campo com vírgulas.

</dd> <dt>

*lista de atributos de função* 
</dt> <dd>

Especifica zero ou mais atributos que se aplicam à função. Os atributos de função válidos são **\[** [**retorno de chamada**](callback.md) **\]** , **\[** [**local**](local.md) **\]** ; o atributo de ponteiro **\[** [**ref**](ref.md) **\]** , **\[** [**Unique**](unique.md) **\]** ou **\[ \] PTR**; e a cadeia de caracteres de atributos de uso **\[** [](string.md) **\]** , **\[** [**ignorar**](ignore.md) **\]** e **\[** [**\_ identificador de contexto**](context-handle.md) **\]** .

</dd> <dt>

*declaração de PTR* 
</dt> <dd>

Especifica pelo menos um Declarador de ponteiro ao qual o atributo **\[ PTR \]** se aplica. Um Declarador de ponteiro é o mesmo que o Declarador de ponteiro usado em C; Ele é construído a partir do \* designador, modificadores, como **distante** e o qualificador [**const**](const.md).

</dd> <dt>

*Nome da função* 
</dt> <dd>

Especifica o nome do procedimento remoto.

</dd> <dt>

*lista de atributos de parâmetro* 
</dt> <dd>

Consiste em zero ou mais atributos apropriados para o tipo de parâmetro especificado. Os atributos de parâmetro podem levar os atributos direcionais para [**dentro**](in.md) e para [**fora**](out-idl.md); os atributos de [**campo \_ First são**](first-is.md), [**Last \_ is**](last-is.md), [**length \_ is**](length-is.md), [**Max \_ is**](max-is.md), [**Size \_ is**](size-is.md)e [**switch \_ Type**](switch-type.md); o atributo pointer [**ref**](ref.md), [**Unique**](unique.md)ou **\[ PTR \]**; e o [**\_ identificador de contexto**](context-handle.md) e a cadeia de [**caracteres**](string.md)de uso. O atributo de uso [**ignore**](ignore.md) não pode ser usado como um atributo de parâmetro. Separe vários atributos com vírgulas.

</dd> </dl>

## <a name="remarks"></a>Comentários

O ponteiro completo designado pelo atributo **\[ PTR \]** se aproxima da funcionalidade completa do ponteiro em linguagem C. O ponteiro completo pode ter o valor **NULL** e pode ser alterado durante a chamada de **NULL** para não **NULL**. Armazenamento apontados por ponteiros completos podem ser acessados por outros nomes no aplicativo com suporte a aliases e ciclos. Essa funcionalidade requer mais sobrecarga durante uma chamada de procedimento remoto para identificar os dados referenciados pelo ponteiro, determinar se o valor é **nulo** e descobrir se dois ponteiros apontam para os mesmos dados.

Use ponteiros completos para:

-   Valores de retorno remotos.
-   Ponteiros duplos, quando o tamanho de um parâmetro de saída não é conhecido.
-   Ponteiros **nulos** .

Ponteiros completos (e exclusivos) não podem ser usados para descrever o tamanho de uma matriz ou Union porque esses ponteiros podem ter o valor **NULL**. Essa restrição por MIDL impede um erro que pode ocorrer quando um valor **nulo** é usado como o tamanho.

Referências e ponteiros exclusivos são considerados para não causar alias de dados. Um grafo direcionado obtido por meio de um ponteiro exclusivo ou de referência e seguir somente ponteiros exclusivos ou de referência não contém nenhuma revergência nem ciclos.

Para evitar o alias, todos os valores de ponteiro devem ser obtidos de um ponteiro de entrada da mesma classe de ponteiro. Se mais de um ponteiro apontar para o mesmo local de memória, todos esses ponteiros deverão ser ponteiros completos.

Em alguns casos, ponteiros completos e exclusivos podem ser misturados. Um ponteiro completo pode ser atribuído ao valor de um ponteiro exclusivo, desde que a atribuição não viole as restrições de alteração do valor de um ponteiro exclusivo. No entanto, quando você atribui um ponteiro exclusivo ao valor de um ponteiro completo, pode causar alias.

A combinação de ponteiros completos e exclusivos pode causar alias, conforme demonstrado no exemplo a seguir:

``` syntax
typedef struct 
{ 
    [ptr] short * pdata;          // full pointer  
} GRAPH_NODE_TYPE; 
 
typedef struct 
{ 
    [unique] graph_node * left;   // unique pointer  
    [unique] graph_node * right;  // unique pointer 
} TREE_NODE_TYPE; 
 
// application code: 
short a = 5; 
TREE_NODE_TYPE * t; 
GRAPH_NODE_TYPE g, h; 
 
g.pdata = h.pdata = &a; 
t->left = &g; 
t->right = &h; 
// t->left->pdata == t->right->pdata == &a
```

Embora "t->Left" e "t->Right" apontem para locais de memória exclusivos, "t->Left->pData" e "t->Right – >pData" têm alias. Por esse motivo, os algoritmos de suporte a alias devem seguir todos os ponteiros (incluindo ponteiros exclusivos e de referência) que podem eventualmente atingir um ponteiro completo.

## <a name="examples"></a>Exemplos

``` syntax
pointer_default(ptr) 
 
typedef [ptr, string] unsigned char * MY_STRING_TYPE; 
 
[ptr] char * MyFunction([in, out, unique] long * plNumber);
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[**matrizes**](arrays-1.md)
</dt> <dt>

[Matrizes e ponteiros](/windows/desktop/Rpc/arrays-and-pointers)
</dt> <dt>

[Atributos de matriz e de Sized-Pointer](array-and-sized-pointer-attributes.md)
</dt> <dt>

[Tipos base de MIDL](midl-base-types.md)
</dt> <dt>

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

[**padrão de ponteiro \_**](pointer-default.md)
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

 

 