---
title: wchar_t atributo
description: A \_ palavra-chave WCHAR t designa um tipo de caractere largo.
ms.assetid: e21b2587-909a-4e2b-8c6d-6cc570bf509f
keywords:
- wchar_t do atributo MIDL
topic_type:
- apiref
api_name:
- wchar_t
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0be9af276a8f87fe5ee7a4dfeb499b864de92f4
ms.sourcegitcommit: 686cb805bed0e89573fc68d145809f50c6b0e6d5
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/13/2020
ms.locfileid: "104007204"
---
# <a name="wchar_t-attribute"></a>atributo do WCHAR \_ t

A palavra-chave **WCHAR \_ t** designa um tipo de caractere largo.

``` syntax
wchar_t identifier-name;
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*nome-do-identificador* 
</dt> <dd>

Especifica um identificador MIDL válido. Os identificadores MIDL válidos consistem em até 31 caracteres alfanuméricos e/ou de sublinhado e devem começar com um caractere alfabético ou de sublinhado.

</dd> </dl>

## <a name="remarks"></a>Comentários

O tipo **WCHAR \_ t** é definido pelo MIDL como um objeto de dados [**curto**](short.md) [**não assinado**](unsigned.md) (16 bits).

O compilador MIDL permite redefinição de **WCHAR \_ t**, mas somente se for consistente com a definição anterior.

O tipo de caractere largo é um dos tipos predefinidos de MIDL. O tipo de caractere largo pode aparecer como um especificador de tipo em declarações [**const**](const.md) , declarações de [**typedef**](typedef.md) , declarações gerais e declaradores de função (como um especificador de tipo de retorno de função e como um especificador de tipo de parâmetro). Para o contexto no qual os especificadores de tipo aparecem, consulte [arquivo de definição de interface (IDL)](interface-definition-idl-file.md).

O atributo de **\[ cadeia de caracteres \]** pode ser aplicado a um ponteiro ou matriz do tipo **WCHAR \_ t**.

Use o caractere **L** antes de um caractere ou uma constante de cadeia de caracteres para designar a constante de tipo de caractere largo.

## <a name="see-also"></a>Confira também

<dl> <dt>

[Tipos base de MIDL](midl-base-types.md)
</dt> <dt>

[**char**](char-idl.md)
</dt> <dt>

[**const**](const.md)
</dt> <dt>

[Arquivo de definição de interface (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**short**](short.md)
</dt> <dt>

[**typedef**](typedef.md)
</dt> <dt>

[**não assinados**](unsigned.md)
</dt> </dl>

 

 




