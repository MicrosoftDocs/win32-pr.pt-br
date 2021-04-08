---
title: atributo string
description: O atributo \ String \ indica que a matriz char-dimensional, WCHAR \_ t, Byte (ou equivalente) ou o ponteiro para tal matriz deve ser tratado como uma cadeia de caracteres.
ms.assetid: 379cd59e-7540-4188-9b5c-6c25a8928999
keywords:
- atributo de cadeia de caracteres MIDL
topic_type:
- apiref
api_name:
- string
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae2bd3c56bcf09d1c47343f903653e9d83113b1d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103917254"
---
# <a name="string-attribute"></a>atributo string

O atributo **\[ \] String** indica que a matriz [**Char**](char-idl.md)-dimensional, [**WCHAR \_ t**](wchar-t.md), [**byte**](byte.md) (ou equivalente) ou o ponteiro para tal matriz deve ser tratado como uma cadeia de caracteres. A cadeia de caracteres também pode ser uma matriz (ou um ponteiro para uma matriz) de construções cujos campos são todos do tipo **byte**.

``` syntax
typedef [ string [[ , type-attribute-list ]] ] type-specifier declarator-list; 

typedef [ struct | union ] 
{
    [ string [[ , field-attribute-list ]] ] type-specifier declarator-list;
    ...
};

[ string [[ , function-attribute-list ]] ] type-specifier ptr-decl function-name(
  [[ [ parameter-attribute-list ] ]] type-specifier [[standard-declarator]]
  , ...);

[[ [ function-attribute-list ] ]] type-specifier [[ptr-decl]] function-name(
    [ string [[ , parameter-attribute-list ]] ] type-specifier [[standard-declarator]]
  , ...);
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lista de atributos de tipo* 
</dt> <dd>

Especifica um ou mais atributos que se aplicam a um tipo. Atributos de tipo válidos incluem **\[** [**identificador**](handle.md) **\]** , **\[** [**\_ tipo de comutador**](switch-type.md) **\]** , **\[** [**transmissão \_ como**](transmit-as.md) **\]** ; o atributo de ponteiro **\[** [**ref**](ref.md) **\]** , **\[** [**Unique**](unique.md) **\]** ou **\[** [**PTR**](ptr.md) **\]** ; e o identificador de contexto de atributos de uso **\[** [**\_**](context-handle.md) **\]** , **\[ cadeia de \] caracteres** e **\[** [**ignorar**](ignore.md) **\]** . Separe vários atributos com vírgulas.

</dd> <dt>

*especificador de tipo* 
</dt> <dd>

Especifica um [tipo de base](midl-base-types.md), tipo de [**struct**](struct.md) ou identificador de tipo. Uma especificação de armazenamento opcional pode preceder o *especificador de tipo*.

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

Especifica zero ou mais atributos de campo que se aplicam à estrutura, ao membro de União ou ao parâmetro de função. Os dois atributos de campo válidos são **\[** [**\_ Max**](max-is.md) **\]** e **\[** [**Size \_ é**](size-is.md) **\]** ; a cadeia de **\[ caracteres \]** de atributos de uso, **\[ ignorar \]** e o **\[ \_ identificador \] de contexto**, o atributo de ponteiro **\[** [**ref**](ref.md) **\]** , **\[ Unique \]** ou **\[** [**PTR**](ptr.md) **\]** , e o **\[ \_ tipo \] de opção** de atributo Union. Separe vários atributos de campo com vírgulas.

</dd> <dt>

*lista de atributos de função* 
</dt> <dd>

Especifica zero ou mais atributos que se aplicam à função. Os atributos de função válidos são **\[** [**retorno de chamada**](callback.md) **\]** , **\[** [**local**](local.md) **\]** ; o atributo de ponteiro **\[ ref \]**, **\[ \] Unique** ou **\[ PTR \]**; e a cadeia de **\[ caracteres \]** de atributos de uso, **\[ ignorar \]** e **\[ \_ \] identificador de contexto**.

</dd> <dt>

*declaração de PTR* 
</dt> <dd>

Especifica um Declarador de ponteiro opcional ao qual o atributo de **\[ cadeia de caracteres \]** se aplica. Um Declarador de ponteiro é o mesmo que o Declarador de ponteiro usado em C; Ele é construído a partir do \* designador, modificadores, como **distante** e o qualificador [**const**](const.md).

</dd> <dt>

*nome da função* 
</dt> <dd>

Especifica o nome do procedimento remoto.

</dd> <dt>

*lista de atributos de parâmetro* 
</dt> <dd>

Consiste em zero ou mais atributos apropriados para o tipo de parâmetro especificado. Os atributos de parâmetro podem levar os atributos direcionais para **\[ dentro \]** e para **\[ \] fora**; o campo máximo de atributos **\[** [**\_ é**](max-is.md) **\]** e o **\[** [**tamanho \_ é**](size-is.md) **\]** ; o atributo de ponteiro **\[ ref \]**, **\[ Unique \]** ou **\[ PTR \]**; e o **\[ \_ identificador \] de contexto** e a cadeia de **\[ caracteres \]** de atributos de uso. O atributo de uso **\[ ignore \]** não pode ser usado como um atributo de parâmetro. Separe vários atributos com vírgulas.

</dd> </dl>

## <a name="remarks"></a>Comentários

Se o atributo de **\[ cadeia de \] caracteres** for usado com uma matriz cujos limites são determinados em tempo de execução, você também deverá especificar que um **\[ tamanho \_ é \]** ou **\[ Max \_ é \]** o atributo, como no exemplo a seguir:

``` syntax
/* a string that can hold up to MAX_STRING_LENGTH characters */
typedef [string, max_is(MAX_STRING_LENGTH)] char line[];
```

O atributo de **\[ \] cadeia de caracteres** não pode ser usado com atributos que especificam o intervalo de elementos transmitidos, como **\[ First \_ é \]**, **\[ Last \_ is \]** e **\[ length \_ is \]**.

Quando usado em matrizes multidimensionais, o atributo de **\[ cadeia de caracteres \]** se aplica à matriz mais à direita.

Para definir uma cadeia de caracteres contada, não use o atributo de **\[ cadeia de caracteres \]** . Use uma matriz de caracteres ou um ponteiro baseado em caractere, como o seguinte:

``` syntax
typedef struct 
{ 
    unsigned short size; 
    unsigned short length; 
    [size_is(size), length_is(length)] char string[*]; 
} counted_string;
```

O atributo **\[ String \]** especifica que o stub deve usar um método fornecido por linguagem para determinar o comprimento das cadeias de caracteres.

Ao declarar cadeias de caracteres em C, você deve alocar espaço para um caractere extra que marque o final da cadeia de caracteres.

## <a name="examples"></a>Exemplos

``` syntax
/* a string type that can hold up to 80 characters */ 
typedef [string] char line[81]; 
 
HRESULT Proc1([in, string] char * pszName);
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Storage**](arrays-1.md)
</dt> <dt>

[Tipos base de MIDL](midl-base-types.md)
</dt> <dt>

[**retorno de chamada**](callback.md)
</dt> <dt>

[**char**](char-idl.md)
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

[**ptr**](ptr.md)
</dt> <dt>

[**ref**](ref.md)
</dt> <dt>

[**o tamanho \_ é**](size-is.md)
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
</dt> <dt>

[**WCHAR \_ t**](wchar-t.md)
</dt> </dl>

 

 