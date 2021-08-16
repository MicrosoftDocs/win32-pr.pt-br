---
title: atributo de byte
description: A palavra-chave byte Especifica um item de dados de 8 bits.
ms.assetid: d6401e05-5498-4d66-8f70-2c794ed26527
keywords:
- MIDL de atributo de byte
topic_type:
- apiref
api_name:
- byte
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a271cc81fe97fb25850bfe4dcb7d2edb55ba3c69805dab17d013bc646768e87f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118384716"
---
# <a name="byte-attribute"></a>atributo de byte

A palavra-chave **byte** especifica um item de dados de 8 bits.

``` syntax
byte identifier-name;
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*nome-do-identificador* 
</dt> <dd>

Especifica um identificador MIDL válido. Os identificadores MIDL válidos consistem em até 31 caracteres alfanuméricos e/ou de sublinhado e devem começar com um caractere alfabético ou de sublinhado.

</dd> </dl>

## <a name="remarks"></a>Comentários

Um item de dados de **byte** não passa por nenhuma conversão para transmissão na rede, uma vez que um tipo de [**caractere**](char-idl.md) pode.

O tipo de **byte** é um dos tipos base da IDL (Interface Definition Language). O tipo de **byte** pode aparecer como um especificador de tipo em declarações [**const**](const.md) , declarações de [**typedef**](typedef.md) , declarações gerais e declaradores de função (como um especificador de tipo de retorno de função e como um especificador de tipo de parâmetro). Para o contexto no qual os especificadores de tipo aparecem, consulte [arquivo de definição de interface (IDL)](interface-definition-idl-file.md).

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

[**typedef**](typedef.md)
</dt> </dl>

 

 




