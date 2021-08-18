---
title: atributo não assinado
description: A palavra-chave não assinada indica que o bit mais significativo de uma variável de inteiro representa um bit de dados em vez de um bit assinado.
ms.assetid: bfcc6bec-895e-45e1-b162-b79651662aa6
keywords:
- atributo não assinado MIDL
topic_type:
- apiref
api_name:
- unsigned
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 383a8fc0379ca81abb9ad0a88edab8750661bdfa429e32e7e91d193aa0fd2938
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146169"
---
# <a name="unsigned-attribute"></a>atributo não assinado

A palavra-chave **não assinada** indica que o bit mais significativo de uma variável de inteiro representa um bit de dados em vez de um bit assinado.

``` syntax
[[ unsigned ]] type-qualifier [[ int ]]identifier-name;
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*type-qualifier* 
</dt> <dd>

Pode ser qualquer [**Char**](char-idl.md), [**WCHAR \_ t**](wchar-t.md), [**Long**](long.md), [**int**](int.md), [**Short**](short.md)e [**Small**](small.md).

</dd> <dt>

*nome-do-identificador* 
</dt> <dd>

Especifica um identificador MIDL válido. Os identificadores MIDL válidos consistem em até 31 caracteres alfanuméricos e/ou de sublinhado e devem começar com um caractere alfabético ou de sublinhado.

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa palavra-chave é opcional e pode ser usada com qualquer um dos tipos de caractere e inteiro [**Char**](char-idl.md), [**WCHAR \_ t**](wchar-t.md), [**Long**](long.md), [**Short**](short.md)e [**Small**](small.md). Opcionalmente, você pode incluir a palavra-chave [**int**](int.md) após os qualificadores de tipo **longo**, **curto** e **pequeno**.

Quando você usa o [**/Char**](-char.md)do compilador de MIDL, os tipos de caractere e inteiro que aparecem no arquivo IDL sem palavras-chave de sinal explícitos podem aparecer com a palavra-chave [**assinada**](signed.md) ou **não** assinado no arquivo de cabeçalho gerado. Para evitar confusão, especifique o sinal dos tipos inteiro e de caractere.

## <a name="see-also"></a>Confira também

<dl> <dt>

[Tipos base de MIDL](midl-base-types.md)
</dt> <dt>

[**char**](char-idl.md)
</dt> <dt>

[**/Char**](-char.md)
</dt> <dt>

[Arquivo de definição de interface (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**INT**](int.md)
</dt> <dt>

[**long**](long.md)
</dt> <dt>

[**short**](short.md)
</dt> <dt>

[**inteiro**](signed.md)
</dt> <dt>

[**menores**](small.md)
</dt> <dt>

[**WCHAR \_ t**](wchar-t.md)
</dt> </dl>

 

 




