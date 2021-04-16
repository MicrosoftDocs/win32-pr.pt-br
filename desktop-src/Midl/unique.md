---
title: atributo exclusivo
description: O atributo \ Unique \ especifica um ponteiro exclusivo.
ms.assetid: 0d668148-e65a-478f-9e47-2528d3caa84c
keywords:
- MIDL de atributo exclusivo
topic_type:
- apiref
api_name:
- unique
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95b839a2abdd546842ef0d33d45a31428af840f7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "105758319"
---
# <a name="unique-attribute"></a>atributo exclusivo

O atributo **\[ exclusivo \]** especifica um ponteiro exclusivo.

``` syntax
pointer_default(unique)

typedef [ unique [[ , type-attribute-list ]] ] type-specifier declarator-list; 

typedef struct-or-union-declarator 
{
    [ unique [[ , field-attribute-list ]] ] type-specifier declarator-list;
    ...}

[ unique [[ , function-attribute-list ]] ] type-specifier ptr-decl function-name(
    [[ [ parameter-attribute-list ] ]] type-specifier [[declarator]]
    , ...);

[[ [ function-attribute-list ] ]] type-specifier [[ptr-decl]] function-name(
    [ unique [[ , parameter-attribute-list ]] ] type-specifier [[declarator]]
    , ...);
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lista de atributos de tipo* 
</dt> <dd>

Especifica um ou mais atributos que se aplicam ao tipo. Atributos de tipo válidos incluem **\[** [**identificador**](handle.md) **\]** , **\[** [**\_ tipo de comutador**](switch-type.md) **\]** , **\[** [**transmissão \_ como**](transmit-as.md) **\]** ; o atributo de ponteiro **\[** [**ref**](ref.md) **\]** , **\[ Unique \]** ou **\[** [**PTR**](ptr.md) **\]** ; e o identificador de contexto de atributos de uso **\[** [**\_**](context-handle.md) **\]** , **\[** [**cadeia de caracteres**](string.md) **\]** e **\[** [**ignorar**](ignore.md) **\]** . Separe vários atributos com vírgulas.

</dd> <dt>

*especificador de tipo* 
</dt> <dd>

Especifica um [tipo base](midl-base-types.md), [**struct**](struct.md), [**Union**](union.md), tipo de [**Enumeração**](enum.md) ou identificador de tipo. Uma especificação de armazenamento opcional pode preceder o *especificador de tipo*.

</dd> <dt>

*Declarador e Declarador-lista* 
</dt> <dd>

Especifica os declaradores padrão C, como identificadores, declaradores de ponteiro e declaradores de matriz. Para obter mais informações, consulte [matriz e Sized-Pointer atributos](array-and-sized-pointer-attributes.md), [**matrizes**](arrays-1.md)e [matrizes e ponteiros](/windows/desktop/Rpc/arrays-and-pointers). A *lista de declaradores* consiste em um ou mais declaradores separados por vírgulas. O identificador de nome de parâmetro no Declarador de função é opcional.

</dd> <dt>

*struct-ou-Union-declaradora* 
</dt> <dd>

Especifica um Declarador [**de MIDL ou**](struct.md) [**Union**](union.md) .

</dd> <dt>

*lista de atributos de campo* 
</dt> <dd>

Especifica zero ou mais atributos de campo que se aplicam ao membro da estrutura, ao membro da União ou ao parâmetro de função. Os atributos de campo válidos incluem **\[** [**primeiro \_**](first-is.md) **\]** , **\[** o [**último \_**](last-is.md)é **\]** , **\[** [**o comprimento \_ é**](length-is.md) **\]** , **\[** [**máx \_**](max-is.md) **\]** ., **\[** o [**tamanho \_ é**](size-is.md) **\]** ; a cadeia de **\[ caracteres \]** de atributos de uso, **\[ ignorar \]** e o **\[ \_ identificador \] de contexto**; o atributo de ponteiro **\[ ref \]**, **\[ Unique \]** ou **\[ PTR \]**; e o **\[ \_ tipo \] de opção** de atributo Union. Separe vários atributos de campo com vírgulas.

</dd> <dt>

*lista de atributos de função* 
</dt> <dd>

Especifica zero ou mais atributos que se aplicam à função. Os atributos de função válidos são **\[** [**retorno de chamada**](callback.md) **\]** , **\[** [**local**](local.md) **\]** ; o atributo de ponteiro **\[ ref \]**, **\[ \] Unique** ou **\[ PTR \]**; e a cadeia de **\[ caracteres \]** de atributos de uso, **\[ ignorar \]** e **\[ \_ \] identificador de contexto**.

</dd> <dt>

*declaração de PTR* 
</dt> <dd>

Especifica pelo menos um Declarador de ponteiro ao qual o atributo **\[ exclusivo \]** se aplica. Um Declarador de ponteiro é o mesmo que o Declarador de ponteiro usado em C; Ele é construído a partir do \* designador, modificadores, como **distante** e o qualificador [**const**](const.md).

</dd> <dt>

*nome da função* 
</dt> <dd>

Especifica o nome do procedimento remoto.

</dd> <dt>

*lista de atributos de parâmetro* 
</dt> <dd>

Consiste em zero ou mais atributos apropriados para o tipo de parâmetro especificado. Os atributos de parâmetro podem levar os atributos direcionais para **\[ \] dentro** e para **\[ fora \]**; os atributos do campo **\[ primeiro \_ são \]**, **\[ Last \_ is \]**, **\[ length \_ is \]**, **\[ Max \_ is \]**, **\[ Size \_ is \]** e **\[ switch \_ Type \]**; o atributo pointer **\[ ref \]**, **Unique** ou [**PTR**](ptr.md); e o **\[ \_ identificador \] de contexto** de atributos de uso e a cadeia de **\[ caracteres \]**. O atributo de uso **\[ ignore \]** não pode ser usado como um atributo de parâmetro. Separe vários atributos com vírgulas.

</dd> </dl>

## <a name="remarks"></a>Comentários

Os atributos de ponteiro podem ser aplicados como um atributo de tipo; como um atributo de campo que se aplica a um membro de estrutura, um membro de União ou um parâmetro; ou como um atributo de função que se aplica ao tipo de retorno da função. O atributo pointer também pode aparecer com a **\[** palavra-chave [**\_ default do ponteiro**](pointer-default.md) **\]** .

Um ponteiro exclusivo tem as seguintes características:

-   Pode ter o valor **NULL**.
-   Pode ser alterado durante uma chamada de **NULL** para não **NULL**, de não **NULL** para **NULL** ou de um valor não **nulo** para outro.
-   Pode alocar nova memória no cliente. Quando o ponteiro exclusivo muda de **nulo** para não **nulo**, os dados retornados do servidor são gravados no novo armazenamento.
-   Pode usar a memória existente no cliente sem alocar nova memória. Quando um ponteiro exclusivo é alterado durante uma chamada de um valor não **nulo** para outro, o ponteiro é considerado para apontar para um objeto de dados do mesmo tipo. Os dados retornados do servidor são gravados no armazenamento existente especificado pelo valor do ponteiro exclusivo antes da chamada.
-   Pode órfão na memória do cliente. A memória referenciada por um ponteiro exclusivo não **nulo** pode nunca ser liberada se o ponteiro exclusivo mudar para **NULL** durante uma chamada e o cliente não tiver outro meio de desreferenciar o armazenamento.
-   Não causa alias. Como o armazenamento apontado por um ponteiro de referência, o armazenamento apontado por um ponteiro exclusivo não pode ser acessado de nenhum outro nome na função.

Os stubs chamam as funções de gerenciamento de memória fornecidas pelo usuário para [**\_ \_ alocar**](/windows/desktop/Rpc/the-midl-user-allocate-function) o usuário MIDL e o [**usuário de MIDL \_ \_ livres**](/windows/desktop/Rpc/the-midl-user-free-function) para alocar e desalocar a memória necessária para ponteiros exclusivos e seus referents.

As seguintes restrições se aplicam a ponteiros exclusivos:

-   O atributo **\[ exclusivo \]** não pode ser aplicado a parâmetros de identificador de associação ( [**identificador \_ t**](handle-t.md)) e a parâmetros de identificador de contexto.
-   O atributo **\[ exclusivo \]** não pode ser aplicado a parâmetros de ponteiro de **\[** [](out-idl.md) **\]** nível superior somente de saída (parâmetros que têm apenas o atributo direcional **\[ \] out** ).
-   Por padrão, os ponteiros de nível superior nas listas de parâmetros são **\[** [](ref.md) **\]** ponteiros de referência. Isso é verdadeiro mesmo que a interface especifique **o \_ padrão de ponteiro (exclusivo)**. Os parâmetros de nível superior nas listas de parâmetros devem ser especificados com o atributo **\[ exclusivo \]** como um ponteiro exclusivo.
-   Ponteiros exclusivos não podem ser usados para descrever o tamanho de um ARM de matriz ou de União porque ponteiros exclusivos podem ter o valor **NULL**. Essa restrição impede o erro que resulta se um valor **nulo** é usado como o tamanho da matriz ou o tamanho de União de braço.

## <a name="examples"></a>Exemplos

``` syntax
pointer_default(unique) 
 
typedef [unique, string] unsigned char * MY_STRING_TYPE; 
 
[unique] char * MyFunction([in, out, unique] long * plNumber);
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

[**lidar com \_ t**](handle-t.md)
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

[\_alocar usuário de MIDL \_](/windows/desktop/Rpc/the-midl-user-allocate-function)
</dt> <dt>

[usuário de MIDL \_ \_ gratuito](/windows/desktop/Rpc/the-midl-user-free-function)
</dt> <dt>

[**fora**](out-idl.md)
</dt> <dt>

[**padrão de ponteiro \_**](pointer-default.md)
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
</dt> </dl>

 

 