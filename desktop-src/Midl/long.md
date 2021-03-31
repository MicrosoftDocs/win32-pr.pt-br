---
title: atributo longo
description: A palavra-chave Long designa um inteiro de 32 bits.
ms.assetid: 5619e482-e3c3-4898-a70b-afd337d2749a
keywords:
- MIDL de atributo longo
topic_type:
- apiref
api_name:
- long
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47ea9af3bfac85ff375f6d5433b4e9f3ed37d8f7
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103916721"
---
# <a name="long-attribute"></a>atributo longo

A palavra-chave **Long** designa um inteiro de 32 bits.

``` syntax
[ signed | unsigned ] long [ int ] declarator-list;
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Declarador-lista* 
</dt> <dd>

Especifica um ou mais declaradores C padrão, como identificadores, declaradores de ponteiro e declaradores de matriz. (Os declaradores de função e as declarações de campo de bits não são permitidas em estruturas que são transmitidas em chamadas de procedimento remoto. Esses declaradores são permitidos em estruturas que não são transmitidas.) Separe vários declaradores com vírgulas.

</dd> </dl>

## <a name="remarks"></a>Comentários

A palavra-chave **Long** pode ser precedida por uma palavra-chave [**assinada**](signed.md) ou pela palavra-chave [**não**](unsigned.md)assinada. A palavra-chave [**int**](int.md) é opcional e pode ser omitida. Para o compilador MIDL, um inteiro longo é assinado por padrão e é sinônimo de **int Long assinado**. Em plataformas de 32 bits, **Long** é sinônimo de **int**.

O tipo inteiro **longo** é um dos tipos base da linguagem IDL. O tipo inteiro **longo** pode aparecer como um especificador de tipo em declarações [**const**](const.md) , declarações de [**typedef**](typedef.md) , declarações gerais e declaradores de função (como um especificador de tipo de retorno de função e como um especificador de tipo de parâmetro). Para o contexto no qual os especificadores de tipo aparecem, consulte [arquivo de definição de interface (IDL)](interface-definition-idl-file.md).

## <a name="see-also"></a>Confira também

<dl> <dt>

[**const**](const.md)
</dt> <dt>

[Tipos base de MIDL](midl-base-types.md)
</dt> <dt>

[**Hyper**](hyper.md)
</dt> <dt>

[**INT**](int.md)
</dt> <dt>

[**short**](short.md)
</dt> <dt>

[**inteiro**](signed.md)
</dt> <dt>

[**menores**](small.md)
</dt> <dt>

[**typedef**](typedef.md)
</dt> <dt>

[**não assinados**](unsigned.md)
</dt> </dl>

 

 




