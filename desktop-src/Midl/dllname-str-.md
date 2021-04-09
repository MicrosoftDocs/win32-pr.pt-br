---
title: atributo DllName (Str)
description: O atributo \ DllName \ define o nome da DLL que contém os pontos de entrada para um módulo.
ms.assetid: dbf062ce-9dcc-4cc6-b7cd-cdc5945e399b
keywords:
- o atributo DllName (Str) MIDL
topic_type:
- apiref
api_name:
- dllname(str)
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 990d277db855c2988021d19a0a756c49454546f7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104007533"
---
# <a name="dllnamestr-attribute"></a>atributo DllName (Str)

O atributo **\[ DllName \]** define o nome da dll que contém os pontos de entrada para um módulo.

``` syntax
[
    uuid(uuid-number), 
    dllname("filename")
    [, optional-attribute-list]
]
module modulename
{
    elementlist
};
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*UUID-número* 
</dt> <dd>

Especifica um número de identificação universalmente exclusivo para o [**módulo**](module.md).

</dd> <dt>

*nome do arquivo* 
</dt> <dd>

Especifica uma cadeia de caracteres terminada em nulo que contém o caminho completo para o arquivo dll.

</dd> <dt>

*lista de atributos opcionais* 
</dt> <dd>

Especifica uma lista de zero ou mais atributos de interface MIDL.

</dd> <dt>

*ModuleName* 
</dt> <dd>

Especifica o nome que outros componentes de software podem usar para se referir ao módulo.

</dd> <dt>

*elementolist* 
</dt> <dd>

Especifica uma ou mais instruções de definição de elemento de módulo.

</dd> </dl>

## <a name="remarks"></a>Comentários

O atributo **\[ DllName \]** é necessário em um módulo.

## <a name="examples"></a>Exemplos

``` syntax
[
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676),
    helpstring("A meaningful comment"),   
    dllname("HANDY.DLL")
] 
module HandyStuff
{
    /* Module content definitions */
};
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[**modulo**](module.md)
</dt> <dt>

[**inicial**](entry.md)
</dt> <dt>

[Sintaxe do arquivo ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Exemplo de arquivo ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Gerando uma biblioteca de tipos com MIDL](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 