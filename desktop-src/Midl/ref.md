---
title: atributo ref
description: O atributo \ ref \ identifica um ponteiro de referência. Ele é usado simplesmente para representar um nível de indireção.
ms.assetid: db4ff938-0f38-4f77-bb65-f728ffd609e0
keywords:
- MIDL do atributo ref
topic_type:
- apiref
api_name:
- ref
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82bc5762eea78b3ce73ab3db58e9bb567b051675
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103823698"
---
# <a name="ref-attribute"></a>atributo ref

O atributo **\[ ref \]** identifica um ponteiro de referência. Ele é usado simplesmente para representar um nível de indireção.

``` syntax
pointer_default(ref)

typedef [ ref [[ , type-attribute-list ]] ] type-specifier declarator-list; 

typedef [ struct | union ] 
{
    [ ref [[ , field-attribute-list ]] ] type-specifier declarator-list;
    ...}

[[ [ function-attribute-list ] ]] type-specifier [[ptr-decl]] function-name(
    [ ref [[ , parameter-attribute-list ]] ] type-specifier [[standard-declarator]]
    , ...);
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lista de atributos de tipo* 
</dt> <dd>

Especifica um ou mais atributos que se aplicam ao tipo. Atributos de tipo válidos incluem **\[** [**identificador**](handle.md) **\]** , **\[** [**\_ tipo de comutador**](switch-type.md) **\]** , **\[** [**transmissão \_ como**](transmit-as.md) **\]** ; os atributos de ponteiro **\[ ref \]**, **\[** [**Unique**](unique.md) **\]** ou **\[** [**PTR**](ptr.md) **\]** ; e o identificador de contexto de atributos de uso **\[** [**\_**](context-handle.md) **\]** , **\[** [**cadeia de caracteres**](string.md) **\]** e **\[** [**ignorar**](ignore.md) **\]** . Separe vários atributos com vírgulas.

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

Especifica zero ou mais atributos de campo que se aplicam à estrutura, ao membro de União ou ao parâmetro de função. Os atributos de campo válidos incluem **\[** [**primeiro \_**](first-is.md) **\]** , **\[** o [**último \_**](last-is.md)é **\]** , **\[** o [**comprimento \_ é**](length-is.md) **\]** , **\[** [**\_ máx**](max-is.md) **\]** ., **\[** o [**tamanho \_ é**](size-is.md) **\]** ; a cadeia de caracteres de atributos de uso **\[** [](string.md) **\]** , **\[** [**ignorar**](ignore.md) **\]** e **\[** o [**\_ identificador de contexto**](context-handle.md) **\]** ; o atributo de ponteiro **\[ ref \]**, **\[** [**Unique**](unique.md) **\]** ou **\[** [**PTR**](ptr.md) **\]** ; e o **\[** [**\_ tipo de opção**](switch-type.md)de atributo Union **\]** . Separe vários atributos de campo com vírgulas.

</dd> <dt>

*lista de atributos de função* 
</dt> <dd>

Especifica zero ou mais atributos que se aplicam à função. Os atributos de função válidos são **\[** [**retorno de chamada**](callback.md) **\]** , **\[** [**local**](local.md) **\]** ; o atributo de ponteiro **\[ \] ref**, **\[** [**Unique**](unique.md) **\]** ou **\[** [**PTR**](ptr.md) **\]** ; e a cadeia de caracteres de atributos de uso **\[** [](string.md) **\]** , **\[** [**ignorar**](ignore.md) **\]** e **\[** [**\_ identificador de contexto**](context-handle.md) **\]** .

</dd> <dt>

*declaração de PTR* 
</dt> <dd>

Especifica pelo menos um Declarador de ponteiro ao qual o atributo **\[ ref \]** se aplica. Um Declarador de ponteiro é o mesmo que o Declarador de ponteiro usado em C; Ele é construído a partir do \* designador, modificadores, como **distante** e o qualificador [**const**](const.md).

</dd> <dt>

*nome da função* 
</dt> <dd>

Especifica o nome do procedimento remoto.

</dd> <dt>

*lista de atributos de parâmetro* 
</dt> <dd>

Consiste em zero ou mais atributos apropriados para o tipo de parâmetro especificado. Os atributos de parâmetro podem levar os atributos direcionais para **\[** [**dentro**](in.md) **\]** e para **\[** [**fora**](out-idl.md) **\]** ; os atributos do campo **\[** [**primeiro \_ são**](first-is.md), **\]** **\[** [**Last \_ is**](last-is.md) **\]** , **\[** [**length \_ is**](length-is.md), **\]** **\[** [**Max \_ is**](max-is.md), **\]** **\[** [**Size \_ is**](size-is.md) **\]** e **\[** [**switch \_ Type**](switch-type.md) **\]** ; o atributo pointer **\[ \] ref**, **\[** [**Unique**](unique.md) **\]** ou **\[** [**PTR**](ptr.md) **\]** ; e o identificador de contexto de atributos de uso e a **\[** [**\_**](context-handle.md) **\]** cadeia de **\[** [**caracteres**](string.md) **\]** . O atributo de uso **\[** [**ignore**](ignore.md) **\]** não pode ser usado como um atributo de parâmetro. Separe vários atributos com vírgulas.

</dd> </dl>

## <a name="remarks"></a>Comentários

Um atributo de ponteiro pode ser aplicado como um atributo de tipo, como um atributo de campo que se aplica a um membro de estrutura, membro de União ou parâmetro; ou como um atributo de função que se aplica ao tipo de retorno da função. O atributo pointer também pode aparecer com a **\[** palavra-chave [**\_ default do ponteiro**](pointer-default.md) **\]** .

Um ponteiro de referência tem as seguintes características:

-   Sempre aponta para o armazenamento válido; Nunca tem o valor **NULL**. Um ponteiro de referência sempre pode ser desreferenciado.
-   Nunca muda durante uma chamada. Um ponteiro de referência sempre aponta para o mesmo armazenamento no cliente antes e depois da chamada.
-   Não aloca uma nova memória no cliente. Os dados retornados do servidor são gravados no armazenamento existente especificado pelo valor do ponteiro de referência antes da chamada.
-   Não causa alias. O armazenamento apontado por um ponteiro de referência não pode ser acessado de nenhum outro nome na função.

Um ponteiro de referência não pode ser usado como o tipo de um ponteiro retornado por uma função.

Se nenhum atributo for especificado para um parâmetro de ponteiro de nível superior, ele será tratado como um ponteiro de referência.

## <a name="examples"></a>Exemplos

``` syntax
[unique] char * GetFirstName( 
    [in, ref] char * pszFullName);
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Storage**](arrays-1.md)
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

[**fora**](out-idl.md)
</dt> <dt>

[**ptr**](ptr.md)
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

 

 