---
title: atributo assinado
description: A palavra-chave signed indica que o bit mais significativo de uma variável de inteiro representa um bit de sinal em vez de um bit de dados.
ms.assetid: 6116089a-647e-485b-8f79-9c9267aa4810
keywords:
- MIDL de atributo assinado
topic_type:
- apiref
api_name:
- signed
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 500b87c849f31082a036d605db0947650e914bed
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103823102"
---
# <a name="signed-attribute"></a>atributo assinado

A palavra-chave **signed** indica que o bit mais significativo de uma variável de inteiro representa um bit de sinal em vez de um bit de dados.

``` syntax
[[ signed ]] type-qualifier [[ int ]]identifier-name;
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*type-qualifier* 
</dt> <dd>

Pode ser qualquer [**Char**](char-idl.md), [**WCHAR \_ t**](wchar-t.md), [**Long**](long.md), [**Short**](short.md)e [**Small**](small.md).

</dd> <dt>

*nome-do-identificador* 
</dt> <dd>

Especifica um identificador MIDL válido. Os identificadores MIDL válidos consistem em até 31 caracteres alfanuméricos e/ou de sublinhado e devem começar com um caractere alfabético ou de sublinhado.

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa palavra-chave é opcional e pode ser usada com qualquer um dos tipos de caractere e inteiro [**Char**](char-idl.md), [**WCHAR \_ t**](wchar-t.md), [**Long**](long.md), [**Short**](short.md)e [**Small**](small.md). Opcionalmente, você pode incluir a palavra-chave [**int**](int.md) após os qualificadores de tipo **longo**, **curto** e **pequeno**.

Quando você usa os tipos [**Char**](char-idl.md), Character e Integer do compilador MIDL que aparecem no arquivo IDL sem palavras-chave de sinal explícitos podem aparecer com as palavras-chave assinadas ou [**não**](unsigned.md) **assinados** no arquivo de cabeçalho gerado. Para evitar confusão, especifique o sinal dos tipos inteiro e de caractere.

## <a name="see-also"></a>Confira também

<dl> <dt>

[Tipos base de MIDL](midl-base-types.md)
</dt> <dt>

[**/Char**](-char.md)
</dt> <dt>

[Arquivo de definição de interface (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**INT**](int.md)
</dt> <dt>

[**Longas**](long.md)
</dt> <dt>

[**short**](short.md)
</dt> <dt>

[**menores**](small.md)
</dt> <dt>

[**não assinados**](unsigned.md)
</dt> <dt>

[**WCHAR \_ t**](wchar-t.md)
</dt> </dl>

 

 




