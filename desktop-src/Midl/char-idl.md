---
title: atributo Char
description: A palavra-chave Char especifica um item de dados de 8 bits.
ms.assetid: 3c9ba8bb-5aea-4166-acf6-b251377e5384
keywords:
- atributo Char MIDL
topic_type:
- apiref
api_name:
- char
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1eab719f6f8ea6e21ccc5b389b12a66b617d5773
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103823356"
---
# <a name="char-attribute"></a>atributo Char

A palavra-chave **Char** especifica um item de dados de 8 bits.

``` syntax
char identifier-name;
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*nome-do-identificador* 
</dt> <dd>

Especifica um identificador MIDL válido. Os identificadores MIDL válidos consistem em até 31 caracteres alfanuméricos e/ou de sublinhado e devem começar com um caractere alfabético ou de sublinhado.

</dd> </dl>

## <a name="remarks"></a>Comentários

A palavra-chave **Char** identifica um item de dados que tem 8 bits. Para o compilador MIDL, um **Char** não é assinado por padrão e é sinônimo de **Char** [**não assinado**](unsigned.md) .

Nesta versão do Microsoft RPC, as tabelas de conversão de caracteres que convertem entre ASCII e EBCDIC são criadas nas bibliotecas de tempo de execução e não podem ser alteradas pelo usuário.

O tipo **Char** é um dos tipos base da IDL (Interface Definition Language). O tipo **Char** pode aparecer como um especificador de tipo em declarações [**const**](const.md) , declarações de [**typedef**](typedef.md) , declarações gerais e declaradores de função (como um especificador de tipo de retorno de função e um especificador de tipo de parâmetro). Para o contexto no qual os especificadores de tipo aparecem, consulte [arquivo de definição de interface (IDL)](interface-definition-idl-file.md).

Os compiladores de IDL do DCE não aceitam a palavra-chave [**assinaled**](signed.md) aplicada a tipos de **caracteres** . Portanto, esse recurso não está disponível quando você usa a opção [**/OSF**](-osf.md) do compilador MIDL.

## <a name="see-also"></a>Confira também

<dl> <dt>

[Tipos base de MIDL](midl-base-types.md)
</dt> <dt>

[**minuciosa**](byte.md)
</dt> <dt>

[**/Char**](-char.md)
</dt> <dt>

[**const**](const.md)
</dt> <dt>

[Arquivo de definição de interface (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**/osf**](-osf.md)
</dt> <dt>

[**inteiro**](signed.md)
</dt> <dt>

[**Strings**](string.md)
</dt> <dt>

[**typedef**](typedef.md)
</dt> <dt>

[**não assinados**](unsigned.md)
</dt> <dt>

[**WCHAR \_ t**](wchar-t.md)
</dt> </dl>

 

 




