---
title: atributo helpfile
description: O atributo \ HelpFile \ define o nome do arquivo de ajuda para uma biblioteca de tipos. Todos os tipos em uma biblioteca compartilham o mesmo arquivo de ajuda.
ms.assetid: caa248b1-a1a7-4c36-886a-079a66a01907
keywords:
- MIDL do atributo HelpFile
topic_type:
- apiref
api_name:
- helpfile
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0b4283b0285631a710af774d364a01b82c9d44b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103640565"
---
# <a name="helpfile-attribute"></a>atributo helpfile

O atributo **\[ HelpFile \]** define o nome do arquivo de ajuda para uma biblioteca de tipos. Todos os tipos em uma biblioteca compartilham o mesmo arquivo de ajuda.

``` syntax
[
    uuid(uuid-number), 
    helpfile("filename") 
    [, optional-attribute-list]
] 
library 
{
    library statements
};
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*UUID-número* 
</dt> <dd>

Especifica um número de identificação universalmente exclusivo para a [**biblioteca**](library.md).

</dd> <dt>

*nome do arquivo* 
</dt> <dd>

Especifica o nome do arquivo que contém o texto de ajuda.

</dd> <dt>

*lista de atributos opcionais* 
</dt> <dd>

Especifica zero ou mais atributos que o compilador MIDL aplicará à [**biblioteca**](library.md).

</dd> <dt>

*instruções de biblioteca* 
</dt> <dd>

Especifica uma ou mais instruções MIDL que definem a interface da biblioteca.

</dd> </dl>

## <a name="remarks"></a>Comentários

Use as funções **GetDocumentation** nas interfaces **ITypeLib** e **ITypeInfo** para recuperar o nome do arquivo.

## <a name="examples"></a>Exemplos

``` syntax
[
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676),
    helpfile("filename.hlp"),
    lcid(0x0409), 
    version(2.0)
]
library Hello
{
    /* Library definition statements here. */
};
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[**biblioteca**](library.md)
</dt> <dt>

[Sintaxe do arquivo ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Exemplo de arquivo ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Gerando uma biblioteca de tipos com MIDL](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 