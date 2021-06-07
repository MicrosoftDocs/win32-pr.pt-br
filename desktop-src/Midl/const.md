---
title: atributo const
description: A palavra-chave const modifica o tipo de uma declaração de tipo ou o tipo de um parâmetro de função, impedindo que o valor seja variável.
ms.assetid: 398fab76-93f3-4d5a-9223-1c57c612b2d7
keywords:
- atributo const MIDL
topic_type:
- apiref
api_name:
- const
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7095e29daf18dc111caf37038b06b0beff5245a8
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111387055"
---
# <a name="const-attribute"></a>atributo const

A **palavra-chave const** modifica o tipo de uma declaração de tipo ou o tipo de um parâmetro de função, impedindo que o valor seja variável.

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

*const-type* 
</dt> <dd>

Especifica um inteiro MIDL válido, caractere, cadeia de caracteres ou tipo booliana. Os tipos MIDL válidos incluem [**small**](small.md), [**short**](short.md), [**long**](long.md), [**char**](char-idl.md), **charÂ \** _, _ [*wchar \_ t* *](wchar-t.md), **wchar \_ tÂ \**_, _ [*byte* *](byte.md), **byteÂ \** _, e [_*voidÂ \**_](void.md). Os tipos de inteiro e de caractere podem ser [_ *assinados* *](signed.md) [**ou não assinados.**](unsigned.md)

</dd> <dt>

*identifier* 
</dt> <dd>

Especifica um identificador MIDL válido. Os identificadores MIDL válidos consistem em até 31 caracteres alfanuméricos e/ou sublinhados e devem começar com um caractere alfabético ou sublinhado.

</dd> <dt>

*const-expression* 
</dt> <dd>

Especifica uma expressão, identificador ou constante numérica ou de caractere apropriada para o tipo especificado: literais inteiros constantes ou expressões de inteiro constante para constantes de inteiro; Expressões boolianas que podem ser computadas na compilação para [**tipos boolianas;**](boolean.md) constantes de caractere único para [**tipos char;**](char-idl.md) e constantes de cadeia de caracteres para tipos **\[** [**de cadeia de**](string.md) **\]** caracteres. O [ * *tipo \* voidÂ* _](void.md) pode ser inicializado somente para _*NULL**.

</dd> <dt>

*type-attribute-list* 
</dt> <dd>

Especifica um ou mais atributos que se aplicam ao tipo.

</dd> <dt>

*tipo de ponteiro* 
</dt> <dd>

Especifica um tipo de ponteiro MIDL válido.

</dd> <dt>

*declarator e declarator-list* 
</dt> <dd>

Especifica declaradores C padrão, como identificadores, declaradores de ponteiro e declaradores de matriz. Para obter mais informações, [consulte Matriz e Sized-Pointer atributos](array-and-sized-pointer-attributes.md), [**matrizes**](arrays-1.md)e [matrizes e ponteiros](/windows/desktop/Rpc/arrays-and-pointers). A *lista de declaradores* consiste em um ou mais declaradores, separados por vírgulas. O identificador de nome de parâmetro no declarador de função é opcional.

</dd> <dt>

*function-attr-list* 
</dt> <dd>

Especifica zero ou mais atributos que se aplicam à função. Atributos de função válidos são retorno de chamada , local ; o atributo de ponteiro ref , exclusivo ou ptr ; e a cadeia de caracteres de atributos de uso **\[** [](callback.md) **\]** **\[** [](local.md) **\]** **\[** [](ref.md) **\]** **\[** [](unique.md) **\]** **\[** [](ptr.md) **\]** , **\[** [](string.md) **\]** **\[** [**ignoram**](ignore.md) **\]** e o indicador de **\[** [**\_ contexto**](context-handle.md) **\]** .

</dd> <dt>

*especificador de tipo* 
</dt> <dd>

Especifica um tipo base , [**struct**](struct.md), [**union**](union.md), [**tipo enum**](enum.md) ou identificador de tipo. [ \_](midl-base-types.md) Uma especificação de armazenamento opcional pode *preceder o especificador de tipo*.

</dd> <dt>

*ptr-decl* 
</dt> <dd>

Especifica zero ou mais declaradores de ponteiro. Um declarador de ponteiro é o mesmo que o declarador de ponteiro usado em C. Ele é construído do **\* *designador _ , modificadores*** como _ far e o qualificador **const**.

</dd> <dt>

*function-name* 
</dt> <dd>

Especifica o nome do procedimento remoto.

</dd> <dt>

*parameter-attribute-list* 
</dt> <dd>

Especifica zero ou mais atributos direcionais, atributos de campo, atributos de uso e atributos de ponteiro apropriados para o tipo de parâmetro especificado. Separe vários atributos com vírgulas.

</dd> </dl>

## <a name="remarks"></a>Comentários

MIDL permite declarar inteiro constante, caractere, cadeia de caracteres e tipos boolianas no corpo da interface do arquivo IDL. **As** declarações de tipo Const são reproduzidas no arquivo de header gerado como **\# diretivas de** definição.

Os compiladores de IDL de DCE não são suportados por expressões constantes. Portanto, esse recurso não está disponível quando você usa a opção [**/osf do**](-osf.md) compilador MIDL.

Uma constante definida anteriormente pode ser usada como o valor atribuído de uma constante subsequente. O valor de uma expressão integral constante é convertido automaticamente no respectivo tipo inteiro de acordo com as regras de conversão C.

O valor de uma constante de caractere deve ser um caractere ASCII entre aspas simples. Quando a constante de caractere é o próprio caractere de aspas simples ('), o caractere de faixa invertida ( ) deve preceder o caractere de aspas \\ simples, como \\ em '.

O valor de uma constante de cadeia de caracteres deve ser uma cadeia de caracteres entre aspas duplas. Em uma cadeia de caracteres, o caractere de linha invertida ( ) deve preceder um caractere de aspas duplas literais **\\** ( **"** ), como **\\ em "**. Em uma cadeia de caracteres, o caractere de faixa invertida ( **\\** ) representa um caractere de escape. Constantes de cadeia de caracteres podem consistir em até 255 caracteres.

O valor **NULL** é o único valor válido para constantes do tipo [ * *voidÂ \** _](void.md). Todos os atributos associados à declaração _ *const** são ignorados.

O compilador MIDL não verifica se há erros de intervalo na **inicialização const.** Por exemplo, quando você especifica "const short x = 0xFFFFFFFF;", o compilador MIDL não relata um erro e o inicializador é reproduzido no arquivo de header gerado.

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

[**Matrizes**](arrays-1.md)
</dt> <dt>

[Tipos base MIDL](midl-base-types.md)
</dt> <dt>

[**Boolean**](boolean.md)
</dt> <dt>

[**Byte**](byte.md)
</dt> <dt>

[**retorno de chamada**](callback.md)
</dt> <dt>

[**Char**](char-idl.md)
</dt> <dt>

[**alça de \_ contexto**](context-handle.md)
</dt> <dt>

[**Enum**](enum.md)
</dt> <dt>

[Arquivo IDL (definição de interface)](interface-definition-idl-file.md)
</dt> <dt>

[**Ignorar**](ignore.md)
</dt> <dt>

[**Local**](local.md)
</dt> <dt>

[**Longas**](long.md)
</dt> <dt>

[**/osf**](-osf.md)
</dt> <dt>

[**ptr**](ptr.md)
</dt> <dt>

[**ref**](ref.md)
</dt> <dt>

[**Curto**](short.md)
</dt> <dt>

[**Assinado**](signed.md)
</dt> <dt>

[**Pequeno**](small.md)
</dt> <dt>

[**String**](string.md)
</dt> <dt>

[**Struct**](struct.md)
</dt> <dt>

[**União**](union.md)
</dt> <dt>

[**unique**](unique.md)
</dt> <dt>

[**Unsigned**](unsigned.md)
</dt> <dt>

[**Vazio**](void.md)
</dt> <dt>

[**wchar \_ t**](wchar-t.md)
</dt> </dl>

 

 