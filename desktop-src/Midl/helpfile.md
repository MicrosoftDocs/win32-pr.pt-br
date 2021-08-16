---
title: atributo helpfile
description: O atributo \ helpfile\ define o nome do arquivo de Ajuda para uma biblioteca de tipos. Todos os tipos em uma biblioteca compartilham o mesmo arquivo de Ajuda.
ms.assetid: caa248b1-a1a7-4c36-886a-079a66a01907
keywords:
- atributo helpfile MIDL
topic_type:
- apiref
api_name:
- helpfile
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1557d96f35913e5e1ed9b784bedfc430e6c4d77b65954583ca6923e4728af9a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118384015"
---
# <a name="helpfile-attribute"></a>atributo helpfile

O **\[ atributo \] helpfile** define o nome do arquivo de Ajuda para uma biblioteca de tipos. Todos os tipos em uma biblioteca compartilham o mesmo arquivo de Ajuda.

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

*uuid-number* 
</dt> <dd>

Especifica um número de identificação universalmente exclusivo para a [**biblioteca**](library.md).

</dd> <dt>

*Filename* 
</dt> <dd>

Especifica o nome do arquivo que contém o texto da ajuda.

</dd> <dt>

*optional-attribute-list* 
</dt> <dd>

Especifica zero ou mais atributos que o compilador MIDL aplicará à [**biblioteca**](library.md).

</dd> <dt>

*instruções de biblioteca* 
</dt> <dd>

Especifica uma ou mais instruções MIDL que definem a interface de biblioteca.

</dd> </dl>

## <a name="remarks"></a>Comentários

Use as **funções GetDocumentation** nas interfaces **ITypeLib** e **ITypeInfo** para recuperar o nome do arquivo.

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

[**Biblioteca**](library.md)
</dt> <dt>

[Sintaxe de arquivo ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Exemplo de arquivo ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Gerando uma biblioteca de tipos com MIDL](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 