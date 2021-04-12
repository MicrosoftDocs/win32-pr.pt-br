---
title: atributo pequeno
description: A palavra-chave Small designa um número inteiro de 8 bits.
ms.assetid: 368e8836-1baa-4547-a62b-f34ac38bbdb2
keywords:
- MIDL de atributo pequeno
topic_type:
- apiref
api_name:
- small
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5a0f106f1be1ba6d0acabf877b5dbefab3eaff6
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104364693"
---
# <a name="small-attribute"></a>atributo pequeno

A palavra-chave **Small** designa um número inteiro de 8 bits.

``` syntax
small identifier-name;
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*nome-do-identificador* 
</dt> <dd>

Especifica um identificador MIDL válido. Os identificadores MIDL válidos consistem em até 31 caracteres alfanuméricos e/ou de sublinhado e devem começar com um caractere alfabético ou de sublinhado.

</dd> </dl>

## <a name="remarks"></a>Comentários

A palavra-chave **Small** pode ser precedida por uma palavra-chave [**assinada**](signed.md) ou pela palavra-chave [**não**](unsigned.md)assinada. A palavra-chave [**int**](int.md) é opcional e pode ser omitida. Para o compilador MIDL, um pequeno inteiro é **assinado** por padrão e é sinônimo de **int pequeno assinado**.

O tipo inteiro **pequeno** é um dos tipos base da linguagem IDL. O tipo inteiro **pequeno** pode aparecer como um especificador de tipo em declarações [**const**](const.md) , declarações de [**typedef**](typedef.md) , declarações gerais e declaradores de função (como um especificador de tipo de retorno de função e como um especificador de tipo de parâmetro). Para o contexto no qual os especificadores de tipo aparecem, consulte [arquivo de definição de interface (IDL)](interface-definition-idl-file.md).

O sinal do tipo **pequeno** pode ser modificado pela opção de compilador MIDL [**/Char**](-char.md). Para evitar confusão, especifique o sinal do tipo de inteiro com as palavras-chave [**assinadas**](signed.md) e [**não assinadas**](unsigned.md).

## <a name="see-also"></a>Confira também

<dl> <dt>

[**/Char**](-char.md)
</dt> <dt>

[**const**](const.md)
</dt> <dt>

[Arquivo de definição de interface (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**int**](int.md)
</dt> <dt>

[**Longas**](long.md)
</dt> <dt>

[**short**](short.md)
</dt> <dt>

[**inteiro**](signed.md)
</dt> <dt>

[**não assinados**](unsigned.md)
</dt> <dt>

[**typedef**](typedef.md)
</dt> </dl>

 

 




