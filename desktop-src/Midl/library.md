---
title: atributo de biblioteca
description: A instrução Library contém todas as informações que o compilador MIDL usa para gerar uma biblioteca de tipos.
ms.assetid: d73acb17-abe4-4c31-a264-a131d1f9fa51
keywords:
- atributo de biblioteca MIDL
topic_type:
- apiref
api_name:
- library
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 100c901c6b5d86ed3420d51e459627bdb5b461b8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "105753460"
---
# <a name="library-attribute"></a>atributo de biblioteca

A instrução **library** contém todas as informações que o compilador MIDL usa para gerar uma biblioteca de tipos.

``` syntax
[
    uuid(uuid-number), 
    [, optional-attribute-list]
] 
library library-name
{ 
    library-definition-statements
}
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*UUID-número* 
</dt> <dd>

Especifica um número de identificação universalmente exclusivo para a biblioteca.

</dd> <dt>

*lista de atributos opcionais* 
</dt> <dd>

Especifica atributos adicionais que se aplicam a toda a instrução da **biblioteca** . Os atributos permitidos incluem **\[** [**controle**](control.md) **\]** , **\[** [**HelpContext**](helpcontext.md) **\]** , **\[** [**HelpFile**](helpfile.md) **\]** , **\[** [**HelpString**](helpstring.md) **\]** , **\[** [**Hidden**](hidden.md) **\]** , **\[** [**LCID**](lcid.md) **\]** , **\[** [**Restricted**](restricted.md) **\]** e **\[** [**version**](version.md) **\]** .

</dd> <dt>

*nome da biblioteca* 
</dt> <dd>

O nome pelo qual os componentes de software se referem à **biblioteca**.

</dd> <dt>

*bibliotecas-definição-instruções* 
</dt> <dd>

Uma ou mais instruções MIDL que definem o conteúdo da **biblioteca**.

</dd> </dl>

## <a name="remarks"></a>Comentários

As instruções dentro do bloco de biblioteca podem usar elementos que são declarados dentro ou fora do bloco de biblioteca. As instruções de biblioteca podem usar esses elementos como tipos base, herdando desses elementos ou simplesmente fazendo referência a eles em uma linha, da seguinte maneira:

``` syntax
interface MyFace 
{
    // Interface definition statements
};

[
    // library attributes
] 
library
{
    interface MyFace;

    // Other library definition statements.
};
```

O compilador MIDL criará uma biblioteca de tipos que inclui definições para cada elemento dentro do bloco de biblioteca, além de definições para quaisquer elementos definidos fora e referenciados de dentro do bloco de biblioteca.

Para obter informações sobre como gerar uma biblioteca de tipos e stubs de proxy e cabeçalhos de um único arquivo IDL, consulte [gerando uma DLL de proxy e uma biblioteca de tipos de um único arquivo IDL](generating-a-proxy-dll-and-a-type-library-from-a-single-idl-file-2.md).

## <a name="examples"></a>Exemplos

``` syntax
[
    uuid(12345678-1234-1234-1234-123456789ABC), 
    helpstring("Hello 2.0 Type Library"), 
    lcid(0x0409), 
    version(2.0)
] 
library Hello 
{
    /* Library definition statements */
};
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[Conteúdo de uma biblioteca de tipos](/previous-versions/windows/desktop/automat/contents-of-a-type-library)
</dt> <dt>

[**controlo**](control.md)
</dt> <dt>

[Gerando uma biblioteca de tipos com MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**helpcontext**](helpcontext.md)
</dt> <dt>

[**helpfile**](helpfile.md)
</dt> <dt>

[**helpstring**](helpstring.md)
</dt> <dt>

[**oculto**](hidden.md)
</dt> <dt>

[**LCID**](lcid.md)
</dt> <dt>

[Sintaxe do arquivo ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[**Restricted**](restricted.md)
</dt> <dt>

[**Versão**](version.md)
</dt> </dl>

 

 