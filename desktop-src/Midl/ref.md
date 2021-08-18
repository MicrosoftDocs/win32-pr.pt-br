---
title: atributo ref
description: O atributo \ ref\ identifica um ponteiro de referência. Ele é usado simplesmente para representar um nível de indcisão.
ms.assetid: db4ff938-0f38-4f77-bb65-f728ffd609e0
keywords:
- atributo ref MIDL
topic_type:
- apiref
api_name:
- ref
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 916556bdee83817f512c2d86eef2d768c3f6dbddf06b39408da5c25a2ba10ed2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013664"
---
# <a name="ref-attribute"></a>atributo ref

O **\[ atributo ref \]** identifica um ponteiro de referência. Ele é usado simplesmente para representar um nível de indcisão.

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

*type-attribute-list* 
</dt> <dd>

Especifica um ou mais atributos que se aplicam ao tipo. Os atributos de tipo válidos incluem **\[** [**handle**](handle.md), **\]** switch type , transmit **\[** [**\_**](switch-type.md) **\]** **\[** [**\_ as**](transmit-as.md); **\]** **\[ \]** **\[** [](unique.md) **\]** **\[** [](ptr.md) **\]** **\[** [**\_**](context-handle.md) **\]** **\[** [](string.md) **\]** **\[** [](ignore.md) **\]** os atributos de ponteiro ref , unique ou ptr ; e o identificador de contexto de atributos de uso , cadeia de caracteres e ignorar . Separe vários atributos com vírgulas.

</dd> <dt>

*especificador de tipo* 
</dt> <dd>

Especifica um [tipo base](midl-base-types.md), [**struct**](struct.md), [**union**](union.md)ou tipo [**de enum**](enum.md) ou identificador de tipo. Uma especificação de armazenamento opcional pode *preceder o especificador de tipo*.

</dd> <dt>

*standard-declarator* 
</dt> <dd>

Especifica um declarador C padrão, como um identificador, um declarador de ponteiro ou um declarador de matriz. Para obter mais informações, [consulte Matriz e Sized-Pointer atributos](array-and-sized-pointer-attributes.md), [**matrizes**](arrays-1.md)e [Matrizes e Ponteiros](/windows/desktop/Rpc/arrays-and-pointers).

</dd> <dt>

*declarator-list* 
</dt> <dd>

Especifica declaradores C padrão, como identificadores, declaradores de ponteiro e declaradores de matriz. Para obter mais informações, [consulte Matriz e Sized-Pointer atributos](array-and-sized-pointer-attributes.md), [**matrizes**](arrays-1.md)e [Matrizes e Ponteiros](/windows/desktop/Rpc/arrays-and-pointers). A *lista de declaradores* consiste em um ou mais declaradores separados por vírgulas. O identificador de nome de parâmetro no declarador de função é opcional.

</dd> <dt>

*field-attribute-list* 
</dt> <dd>

Especifica zero ou mais atributos de campo que se aplicam à estrutura, membro da união ou parâmetro de função. Os atributos de campo válidos incluem primeiro é , o último é , o comprimento é , max é , o tamanho é ; a cadeia de caracteres de atributos de uso , ignora e o identificador de contexto ; o atributo de ponteiro **\[** [**\_**](first-is.md) **\]** **\[** [**\_**](last-is.md) **\]** **\[** [**\_**](length-is.md) **\]** **\[** [**\_**](max-is.md) **\]** **\[** [**\_**](size-is.md) **\]** **\[** [](string.md) **\]** **\[** [](ignore.md) **\]** **\[** [**\_**](context-handle.md) **\]** **\[ ref \]**, exclusivo **\[** [](unique.md) **\]** **\[** [](ptr.md) **\]** **\[** [**\_**](switch-type.md) **\]** ou ptr ; e o tipo de comutador de atributo de união . Separe vários atributos de campo com vírgulas.

</dd> <dt>

*function-attribute-list* 
</dt> <dd>

Especifica zero ou mais atributos que se aplicam à função. Atributos de função válidos são retorno de chamada , local ; o atributo de ponteiro **\[** [](callback.md) **\]** **\[** [](local.md) **\]** **\[ \] ref**, exclusivo ou **\[** [](unique.md) **\]** **\[** [**ptr**](ptr.md); **\]** **\[** [](string.md) **\]** **\[** [](ignore.md) **\]** **\[** [**\_**](context-handle.md) **\]** e a cadeia de caracteres de atributos de uso , ignoram e o indicador de contexto .

</dd> <dt>

*ptr-decl* 
</dt> <dd>

Especifica pelo menos um declarador de ponteiro ao qual o **\[ atributo ref \]** se aplica. Um declarador de ponteiro é o mesmo que o declarador de ponteiro usado em C; ele é construído a partir do \* designador, modificadores como **distante** e o qualificador [**const**](const.md).

</dd> <dt>

*Nome da função* 
</dt> <dd>

Especifica o nome do procedimento remoto.

</dd> <dt>

*parameter-attribute-list* 
</dt> <dd>

Consiste em zero ou mais atributos apropriados para o tipo de parâmetro especificado. Os atributos de parâmetro podem levar os atributos direcionais para dentro e para fora ; os atributos de campo primeiro são , o último é , o comprimento é , max é , o tamanho é e o tipo de opção ; o atributo de ponteiro **\[** [](in.md) **\]** **\[** [](out-idl.md) **\]** **\[** [**\_**](first-is.md) **\]** **\[** [**\_**](last-is.md) **\]** **\[** [**\_**](length-is.md) **\]** **\[** [**\_**](max-is.md) **\]** **\[** [**\_**](size-is.md) **\]** **\[** [**\_**](switch-type.md) **\]** **\[ ref, \]** **\[** [**exclusivo**](unique.md) **\]** **\[** [](ptr.md) **\]** **\[** [**\_**](context-handle.md) **\]** **\[** [](string.md) **\]** ou ptr ; e o identificador de contexto de atributos de uso e a cadeia de caracteres . O atributo de **\[** [**uso ignore**](ignore.md) **\]** não pode ser usado como um atributo de parâmetro. Separe vários atributos com vírgulas.

</dd> </dl>

## <a name="remarks"></a>Comentários

Um atributo de ponteiro pode ser aplicado como um atributo de tipo, como um atributo de campo que se aplica a um membro de estrutura, membro de união ou parâmetro; ou como um atributo de função que se aplica ao tipo de retorno de função. O atributo de ponteiro também pode aparecer com a **\[** [**palavra-chave \_ padrão do**](pointer-default.md) **\]** ponteiro.

Um ponteiro de referência tem as seguintes características:

-   Sempre aponta para um armazenamento válido; nunca tem o valor **NULL.** Um ponteiro de referência sempre pode ser desreferenciado.
-   Nunca muda durante uma chamada. Um ponteiro de referência sempre aponta para o mesmo armazenamento no cliente antes e depois da chamada.
-   Não aloca nova memória no cliente. Os dados retornados do servidor são gravados no armazenamento existente especificado pelo valor do ponteiro de referência antes da chamada.
-   Não causa alias. Armazenamento apontado por um ponteiro de referência não pode ser alcançado de nenhum outro nome na função.

Um ponteiro de referência não pode ser usado como o tipo de um ponteiro retornado por uma função.

Se nenhum atributo for especificado para um parâmetro de ponteiro de nível superior, ele será tratado como um ponteiro de referência.

## <a name="examples"></a>Exemplos

``` syntax
[unique] char * GetFirstName( 
    [in, ref] char * pszFullName);
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[**matrizes**](arrays-1.md)
</dt> <dt>

[Matrizes e ponteiros](/windows/desktop/Rpc/arrays-and-pointers)
</dt> <dt>

[Atributos de matriz e Sized-Pointer dados](array-and-sized-pointer-attributes.md)
</dt> <dt>

[Tipos base MIDL](midl-base-types.md)
</dt> <dt>

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

[**out**](out-idl.md)
</dt> <dt>

[**ptr**](ptr.md)
</dt> <dt>

[**size \_ é**](size-is.md)
</dt> <dt>

[**String**](string.md)
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

 

 