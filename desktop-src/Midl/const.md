---
title: atributo const
description: A palavra-chave const modifica o tipo de uma declaração de tipo ou o tipo de um parâmetro de função, impedindo que o valor seja variado.
ms.assetid: 398fab76-93f3-4d5a-9223-1c57c612b2d7
keywords:
- MIDL do atributo const
topic_type:
- apiref
api_name:
- const
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d2980f0f484c838e4f972bbf12fb72173edb3e7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103640516"
---
# <a name="const-attribute"></a>atributo const

A palavra-chave **const** modifica o tipo de uma declaração de tipo ou o tipo de um parâmetro de função, impedindo que o valor seja variado.

``` syntax
const const-type identifier = const-expression ;

[ typedef [ , type-attribute-list ] ] const const-type declarator-list;

[ typedef [ , type-attribute-list ] ] pointer-type const declarator-list;

[ [ function-attr-list ] ] type-specifier [ ptr-decl ] function-name(
    [ [ parameter-attribute-list ] ] ) const; 

const-type [declarator], [ [ parameter-attribute-list ] ] pointer-type const [declarator], ...);
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*tipo const* 
</dt> <dd>

Especifica um inteiro MIDL, caractere, Cadeia de caracteres ou tipo booliano válido. Os tipos de MIDL válidos incluem [**pequeno**](small.md), [**curto**](short.md), [**longo**](long.md), [**Char**](char-idl.md), **charÂ \***, [**WCHAR \_ t**](wchar-t.md), **WCHAR \_ tâ \***, [**byte**](byte.md), **byteÂ \*** e [**voidÂ \***](void.md). O número inteiro e os tipos de caracteres podem ser [**assinados**](signed.md) ou [**não assinados**](unsigned.md).

</dd> <dt>

*identifier* 
</dt> <dd>

Especifica um identificador MIDL válido. Os identificadores MIDL válidos consistem em até 31 caracteres alfanuméricos e/ou de sublinhado e devem começar com um caractere alfabético ou de sublinhado.

</dd> <dt>

*expressão const* 
</dt> <dd>

Especifica uma expressão, um identificador ou uma constante numérica ou de caractere apropriada para o tipo especificado: literais inteiros constantes ou expressões de inteiro constante para constantes de inteiro; Expressões booleanas que podem ser computadas na compilação para tipos [**boolianos**](boolean.md) ; constantes de caractere único para tipos de [**caracteres**](char-idl.md) ; e constantes de cadeia de caracteres para tipos de **\[** [**cadeia de caracteres**](string.md) **\]** . O [**tipo \* voidÂ**](void.md) pode ser inicializado somente como **NULL**.

</dd> <dt>

*lista de atributos de tipo* 
</dt> <dd>

Especifica um ou mais atributos que se aplicam ao tipo.

</dd> <dt>

*tipo de ponteiro* 
</dt> <dd>

Especifica um tipo de ponteiro de MIDL válido.

</dd> <dt>

*Declarador e Declarador-lista* 
</dt> <dd>

Especifica os declaradores padrão C, como identificadores, declaradores de ponteiro e declaradores de matriz. Para obter mais informações, consulte [matriz e Sized-Pointer atributos](array-and-sized-pointer-attributes.md), [**matrizes**](arrays-1.md)e [matrizes e ponteiros](/windows/desktop/Rpc/arrays-and-pointers). A *lista de declaradores* consiste em um ou mais declaradores, separados por vírgulas. O identificador de nome de parâmetro no Declarador de função é opcional.

</dd> <dt>

*função-attr-lista* 
</dt> <dd>

Especifica zero ou mais atributos que se aplicam à função. Os atributos de função válidos são **\[** [**retorno de chamada**](callback.md) **\]** , **\[** [**local**](local.md) **\]** ; o atributo de ponteiro **\[** [**ref**](ref.md) **\]** , **\[** [**Unique**](unique.md) **\]** ou **\[** [**PTR**](ptr.md) **\]** ; e a cadeia de caracteres de atributos de uso **\[** [](string.md) **\]** , **\[** [**ignorar**](ignore.md) **\]** e **\[** [**\_ identificador de contexto**](context-handle.md) **\]** .

</dd> <dt>

*especificador de tipo* 
</dt> <dd>

Especifica um [ \_ tipo base](midl-base-types.md), [**struct**](struct.md), [**Union**](union.md), tipo de [**Enumeração**](enum.md) ou identificador de tipo. Uma especificação de armazenamento opcional pode preceder o *especificador de tipo*.

</dd> <dt>

*declaração de PTR* 
</dt> <dd>

Especifica zero ou mais declaradores de ponteiro. Um Declarador de ponteiro é o mesmo que o Declarador de ponteiro usado em C. Ele é construído a partir do **\*** designador, modificadores, como **distante** e o qualificador **const**.

</dd> <dt>

*nome da função* 
</dt> <dd>

Especifica o nome do procedimento remoto.

</dd> <dt>

*lista de atributos de parâmetro* 
</dt> <dd>

Especifica zero ou mais atributos direcionais, atributos de campo, atributos de uso e atributos de ponteiro apropriados para o tipo de parâmetro especificado. Separe vários atributos com vírgulas.

</dd> </dl>

## <a name="remarks"></a>Comentários

MIDL permite que você declare tipos inteiros, caracteres, cadeias de caracteres e boolianos constantes no corpo da interface do arquivo IDL. As declarações de tipo **const** são reproduzidas no arquivo de cabeçalho gerado como **\# definir** diretivas.

Os compiladores de IDL do DCE não dão suporte a expressões constantes. Portanto, esse recurso não está disponível quando você usa a opção [**/OSF**](-osf.md) do compilador MIDL.

Uma constante definida anteriormente pode ser usada como o valor atribuído de uma constante subsequente. O valor de uma expressão integral constante é convertido automaticamente no respectivo tipo de inteiro de acordo com as regras de conversão C.

O valor de uma constante de caractere deve ser um caractere ASCII com aspas simples. Quando a constante de caractere é o próprio caractere de aspas simples ('), o caractere de barra invertida ( \) deve preceder o caractere de aspas simples, como em \\ '.

O valor de uma constante de cadeia de caracteres deve ser uma cadeia de caracteres entre aspas duplas. Dentro de uma cadeia de caracteres, o caractere de barra invertida ( **\\** ) deve preceder um caractere de aspas duplas literal ( **"** ), como em **\\ "**. Dentro de uma cadeia de caracteres, o caractere de barra invertida ( **\\** ) representa um caractere de escape. Constantes de cadeia de caracteres podem consistir de até 255 caracteres.

O valor **NULL** é o único valor válido para constantes do tipo [**voidÂ \***](void.md). Todos os atributos associados à Declaração **const** são ignorados.

O compilador MIDL não verifica erros de intervalo na inicialização **const** . Por exemplo, quando você especifica "const Short x = 0xFFFFFFFF;", o compilador MIDL não relata um erro e o inicializador é reproduzido no arquivo de cabeçalho gerado.

## <a name="examples"></a>Exemplos

``` syntax
const void *  p1        = NULL; 
const char    my_char1  = 'a'; 
const char    my_char2  = my_char1; 
const wchar_t my_wchar3 = L'a'; 
const wchar_t * pszNote = L"Note"; 
const unsigned short int x = 123; 
 
typedef [string] const char *LPCSTR; 
 
HRESULT GetName([out] wchar_t * const pszName );
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Storage**](arrays-1.md)
</dt> <dt>

[Tipos base de MIDL](midl-base-types.md)
</dt> <dt>

[**Boolean**](boolean.md)
</dt> <dt>

[**minuciosa**](byte.md)
</dt> <dt>

[**retorno de chamada**](callback.md)
</dt> <dt>

[**char**](char-idl.md)
</dt> <dt>

[**identificador de contexto \_**](context-handle.md)
</dt> <dt>

[**enumera**](enum.md)
</dt> <dt>

[Arquivo de definição de interface (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**ignorar**](ignore.md)
</dt> <dt>

[**local**](local.md)
</dt> <dt>

[**Longas**](long.md)
</dt> <dt>

[**/osf**](-osf.md)
</dt> <dt>

[**ptr**](ptr.md)
</dt> <dt>

[**ref**](ref.md)
</dt> <dt>

[**short**](short.md)
</dt> <dt>

[**inteiro**](signed.md)
</dt> <dt>

[**menores**](small.md)
</dt> <dt>

[**string**](string.md)
</dt> <dt>

[**struct**](struct.md)
</dt> <dt>

[**unida**](union.md)
</dt> <dt>

[**diferente**](unique.md)
</dt> <dt>

[**não assinados**](unsigned.md)
</dt> <dt>

[**void**](void.md)
</dt> <dt>

[**WCHAR \_ t**](wchar-t.md)
</dt> </dl>

 

 