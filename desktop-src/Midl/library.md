---
title: atributo library
description: A instrução library contém todas as informações que o compilador MIDL usa para gerar uma biblioteca de tipos.
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
ms.openlocfilehash: 4fc1f836174a57f6edfddd0575a10d40367c061c034369a1582cc8bf8ce17a53
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120086366"
---
# <a name="library-attribute"></a>atributo library

A **instrução** library contém todas as informações que o compilador MIDL usa para gerar uma biblioteca de tipos.

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

*uuid-number* 
</dt> <dd>

Especifica um número de identificação universalmente exclusivo para a biblioteca.

</dd> <dt>

*optional-attribute-list* 
</dt> <dd>

Especifica atributos adicionais que se aplicam à instrução **de biblioteca** inteira. Os atributos que permitem **\[** [**incluem controle**](control.md) **\]** , **\[** [**helpcontext,**](helpcontext.md) **\]** **\[** [**helpfile**](helpfile.md), **\]** **\[** [**helpstring**](helpstring.md), **\]** **\[** [**hidden**](hidden.md) **\]** , **\[** [**lcid,**](lcid.md) **\]** **\[** [**restricted**](restricted.md)e **\]** **\[** [**version**](version.md) **\]** .

</dd> <dt>

*nome da biblioteca* 
</dt> <dd>

O nome pelo qual os componentes de software se referem à **biblioteca**.

</dd> <dt>

*library-definition-statements* 
</dt> <dd>

Uma ou mais instruções MIDL que definem o conteúdo da **biblioteca**.

</dd> </dl>

## <a name="remarks"></a>Comentários

Instruções dentro do bloco de biblioteca podem usar elementos declarados dentro ou fora do bloco de biblioteca. As instruções de biblioteca podem usar esses elementos como tipos base, herdando desses elementos ou simplesmente referenciando-os em uma linha, da seguinte maneira:

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

O compilador MIDL criará uma biblioteca de tipos que inclui definições para cada elemento dentro do bloco de biblioteca, além de definições para todos os elementos definidos fora e referenciados de dentro do bloco de biblioteca.

Para obter informações sobre como gerar uma biblioteca de tipos e os stubs de proxy e os headers de um único arquivo IDL, consulte Gerando uma DLL de proxy e uma biblioteca de tipos de um único arquivo [IDL.](generating-a-proxy-dll-and-a-type-library-from-a-single-idl-file-2.md)

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

[**Controle**](control.md)
</dt> <dt>

[Gerando uma biblioteca de tipos com MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**helpcontext**](helpcontext.md)
</dt> <dt>

[**helpfile**](helpfile.md)
</dt> <dt>

[**helpstring**](helpstring.md)
</dt> <dt>

[**Escondidos**](hidden.md)
</dt> <dt>

[**Lcid**](lcid.md)
</dt> <dt>

[Sintaxe de arquivo ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[**Restrito**](restricted.md)
</dt> <dt>

[**Versão**](version.md)
</dt> </dl>

 

 