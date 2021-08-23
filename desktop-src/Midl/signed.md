---
title: atributo signed
description: A palavra-chave signed indica o bit mais significativo de uma variável de inteiro representa um bit de sinal em vez de um bit de dados.
ms.assetid: 6116089a-647e-485b-8f79-9c9267aa4810
keywords:
- atributo assinado MIDL
topic_type:
- apiref
api_name:
- signed
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f3db15bc46d6d8ab3ec108c648d094ebf706d9286a8c4b0a823fa409e118e3d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118641325"
---
# <a name="signed-attribute"></a>atributo signed

A **palavra-chave** signed indica o bit mais significativo de uma variável de inteiro representa um bit de sinal em vez de um bit de dados.

``` syntax
[[ signed ]] type-qualifier [[ int ]]identifier-name;
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*type-qualifier* 
</dt> <dd>

Pode ser qualquer um [**de char**](char-idl.md), [**wchar \_ t**](wchar-t.md), [**long**](long.md), [**short**](short.md)e [**small.**](small.md)

</dd> <dt>

*identifier-name* 
</dt> <dd>

Especifica um identificador MIDL válido. Os identificadores MIDL válidos consistem em até 31 caracteres alfanuméricos e/ou sublinhados e devem começar com um caractere alfabético ou sublinhado.

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa palavra-chave é opcional e pode ser usada com qualquer um dos tipos de caractere e inteiro [**char**](char-idl.md), [**wchar \_ t**](wchar-t.md), [**long**](long.md), [**short**](short.md)e [**small**](small.md). Opcionalmente, você pode incluir a palavra-chave [**int**](int.md) após os qualificadores de tipo **long,** **short** e **small.**

Quando você usa os tipos char [**,**](char-idl.md)character e integer do com opção do compilador MIDL [](unsigned.md) que aparecem no arquivo IDL sem palavras-chave de sinal explícitas podem aparecer com as palavras-chave assinadas ou não assinadas no arquivo de título gerado.  Para evitar confusão, especifique o sinal dos tipos inteiro e caractere.

## <a name="see-also"></a>Confira também

<dl> <dt>

[Tipos base MIDL](midl-base-types.md)
</dt> <dt>

[**/char**](-char.md)
</dt> <dt>

[Arquivo IDL (definição de interface)](interface-definition-idl-file.md)
</dt> <dt>

[**INT**](int.md)
</dt> <dt>

[**long**](long.md)
</dt> <dt>

[**short**](short.md)
</dt> <dt>

[**Pequeno**](small.md)
</dt> <dt>

[**Unsigned**](unsigned.md)
</dt> <dt>

[**wchar \_ t**](wchar-t.md)
</dt> </dl>

 

 




