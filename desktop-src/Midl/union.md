---
title: atributo Union
description: A palavra-chave Union aparece em funções relacionadas a uniões discriminadas.
ms.assetid: 135a6581-e03e-4b90-9fd8-15690820dbd0
keywords:
- atributo Union MIDL
topic_type:
- apiref
api_name:
- union
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc683472d67775c4a2900695246d5f9ca920ca32
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104498881"
---
# <a name="union-attribute"></a>atributo Union

A palavra-chave **Union** aparece em funções relacionadas a uniões discriminadas.

``` syntax
/* Encapsulated union*/
typedef [[ [type-attribute-list] ]] union [[ struct-name ]] switch (switch-type switch-name) [[ union-name ]] 
{
  C-style-case-list 
  [[ [ field-attribute-list <> ] ]] type-specifier <> declarator-list <>;

        ...
}

/* Non-encapsulated union*/
typedef [switch_type(switch-type) [[ , type-attr-list ]] ] union [[ tag ]] 
{ 
    [ case ( limited-expr-list) ]
  [[ [ field-attribute-list ] ]] type-specifier declarator-list;
  [[ [ default ]
  [[ [ field-attribute-list ] ]] type-specifier declarator-list;
  ]]
}
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lista de atributos de tipo* 
</dt> <dd>

Especifica zero ou mais atributos que se aplicam ao tipo Union. Atributos de tipo válidos incluem **\[** [**tratar**](handle.md) **\]** , **\[** [**transmitir \_ como**](transmit-as.md) **\]** ; o atributo de ponteiro **\[** [**exclusivo**](unique.md) **\]** ou **\[** [**PTR**](ptr.md) **\]** ; e o identificador de contexto de atributos de uso **\[** [**\_**](context-handle.md) **\]** e **\[** [**ignorar**](ignore.md) **\]** . As uniões encapsuladas também podem ter o **\[** [](ref.md) **\]** atributo tipo de ponteiro ref. Separe vários atributos com vírgulas.

</dd> <dt>

*nome do struct* 
</dt> <dd>

Especifica uma marca opcional que nomeia a estrutura gerada pelo compilador MIDL.

</dd> <dt>

*tipo de opção* 
</dt> <dd>

Especifica um tipo [**int**](int.md), [**Char**](char-idl.md), [**enum**](enum.md) ou um identificador que resolve para um desses tipos.

</dd> <dt>

*nome do comutador* 
</dt> <dd>

Especifica o nome da variável do tipo *switch-type* que atua como o discriminante de União.

</dd> <dt>

*nome da União* 
</dt> <dd>

Especifica um identificador opcional que nomeia a União na estrutura, gerada pelo compilador MIDL, que contém a União e o discriminante.

</dd> <dt>

*Estilo C-caixa-lista* 
</dt> <dd>

Lista de "**Case** *const-expr* :"

</dd> <dt>

*lista de expressões limitadas* 
</dt> <dd>

Especifica uma ou mais expressões de linguagem C. O compilador MIDL oferece suporte a expressões condicionais, expressões lógicas, expressões relacionais e expressões aritméticas. MIDL não permite invocações de função em expressões e não permite operadores de incremento e decréscimo. Expressões individuais na lista devem ser separadas por uma vírgula.

</dd> <dt>

*lista de atributos de campo* 
</dt> <dd>

Especifica zero ou mais atributos de campo que se aplicam ao membro da União. Os atributos de campo válidos incluem **\[** [**primeiro \_**](first-is.md), **\]** **\[** o [**último \_**](last-is.md)é **\]** , **\[** o [**comprimento \_ é**](length-is.md) **\]** , **\[** [**máx \_**](max-is.md) **\]** ., **\[** o [**tamanho \_ é**](size-is.md) **\]** ; a cadeia de caracteres de atributos de uso **\[** [](string.md) **\]** , **\[** [**ignorar**](ignore.md) **\]** e **\[** o [**\_ identificador de contexto**](context-handle.md) **\]** ; o atributo de ponteiro **\[** [**exclusivo**](unique.md) **\]** ou **\[** [**PTR**](ptr.md) **\]** ; e, para membros que são uniões não encapsuladas, o **\[** [**\_ tipo de opção**](switch-type.md)de atributo Union **\]** . Uniões não encapsuladas também podem usar o **\[** [](ref.md) **\]** atributo de campo ponteiro de referência. Separe vários atributos de campo com vírgulas.

</dd> <dt>

*especificador de tipo* 
</dt> <dd>

Especifica um [tipo base](midl-base-types.md), [**struct**](struct.md), **Union**, tipo de [**Enumeração**](enum.md) ou identificador de tipo. Uma especificação de armazenamento opcional pode preceder o *especificador de tipo*.

</dd> <dt>

*Declarador-lista* 
</dt> <dd>

Um ou mais declaradores C padrão, como identificadores, declaradores de ponteiro e declaradores de matriz. (Os declaradores de função e as declarações de campo de bits não são permitidas em uniões que são transmitidas em chamadas de procedimento remoto. Exceto quando você usa o switch do compilador MIDL [**/OSF**](-osf.md), esses declaradores são permitidos em uniões que não são transmitidas.) Separe vários declaradores com vírgulas.

</dd> <dt>

*Tags* 
</dt> <dd>

Especifica uma marca opcional.

</dd> </dl>

## <a name="remarks"></a>Comentários

O MIDL dá suporte a dois tipos de uniões discriminadas: [uniões encapsuladas](encapsulated-unions.md) e [unencapsulated Unions](nonencapsulated-unions.md). A União encapsulada é compatível com implementações anteriores do RPC (NCA versão 1). A União não encapsulada elimina algumas das restrições da União encapsulada e fornece um discriminante mais visível do que a União encapsulada.

A União encapsulada é identificada pela palavra-chave [**switch**](switch.md) e pela ausência de outras palavras-chave relacionadas à União.

A União não encapsulada, também conhecida como Union, é identificada pela presença da **\[** [**\_ opção**](switch-is.md) **\]** e **\[** palavras-chave do [**\_ tipo switch**](switch-type.md) **\]** , que identificam o discriminante e seu tipo.

Ao usar **\[** uniões [**in**](in.md), [**out**](out-idl.md) **\]** , lembre-se de que a alteração do valor da opção Union durante a chamada pode fazer com que a chamada remota se comporte de forma diferente de uma chamada local. No retorno, os stubs copiam o parâmetro **\[ in** e **out \]** na memória que já está presente no cliente. Quando o procedimento remoto modifica o valor da opção Union e, consequentemente, altera o tamanho do objeto de dados, os stubs podem substituir a memória válida pelo valor **\[ out \]** . Quando a opção Union altera o objeto de dados de um tipo base para um tipo de ponteiro, os stubs podem substituir a memória válida ao copiar o ponteiro Referent para o local da memória indicado pelo valor **\[ in \]** de um tipo base.

A forma de uniões deve ser idêntica em todas as plataformas para garantir a interconectividade.

## <a name="see-also"></a>Confira também

<dl> <dt>

[Uniões encapsuladas](encapsulated-unions.md)
</dt> <dt>

[Arquivo de definição de interface (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**no**](in.md)
</dt> <dt>

[Uniões não encapsuladas](nonencapsulated-unions.md)
</dt> <dt>

[**fora**](out-idl.md)
</dt> <dt>

[**switch \_ é**](switch-is.md)
</dt> <dt>

[**tipo de comutador \_**](switch-type.md)
</dt> </dl>

 

 




