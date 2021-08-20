---
title: atributo long
description: A palavra-chave long designa um inteiro de 32 bits.
ms.assetid: 5619e482-e3c3-4898-a70b-afd337d2749a
keywords:
- atributo long MIDL
topic_type:
- apiref
api_name:
- long
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9493aea9a669e9ac14882e9a230e217e74c7236a68c3bb924ddbbaad7e4b93ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117806711"
---
# <a name="long-attribute"></a>atributo long

A **palavra-chave** long designa um inteiro de 32 bits.

``` syntax
[ signed | unsigned ] long [ int ] declarator-list;
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*declarator-list* 
</dt> <dd>

Especifica um ou mais declaradores C padrão, como identificadores, declaradores de ponteiro e declaradores de matriz. (Declaradores de função e declarações de campo de bits não são permitidos em estruturas transmitidas em chamadas de procedimento remoto. Esses declaradores são permitidos em estruturas que não são transmitidas.) Separe vários declaradores com vírgulas.

</dd> </dl>

## <a name="remarks"></a>Comentários

A **palavra-chave long** pode ser precedida pela palavra-chave [**signed**](signed.md) ou pela palavra-chave [**unsigned**](unsigned.md). A [**palavra-chave int**](int.md) é opcional e pode ser omitida. Para o compilador MIDL, um inteiro longo é assinado por padrão e é sinônimo de **long int assinado.** Em plataformas de 32 bits, **long** é sinônimo de **int**.

O **tipo** inteiro longo é um dos tipos base da linguagem IDL. O **tipo** inteiro longo pode aparecer como um especificador de tipo em declarações [**const,**](const.md) declarações [**typedef,**](typedef.md) declarações gerais e declaradores de função (como um especificador de tipo de retorno de função e como um especificador de tipo de parâmetro). Para o contexto no qual os especificadores de tipo aparecem, consulte [Arquivo de definição de interface (IDL).](interface-definition-idl-file.md)

## <a name="see-also"></a>Confira também

<dl> <dt>

[**const**](const.md)
</dt> <dt>

[Tipos base MIDL](midl-base-types.md)
</dt> <dt>

[**Hyper**](hyper.md)
</dt> <dt>

[**INT**](int.md)
</dt> <dt>

[**short**](short.md)
</dt> <dt>

[**Assinado**](signed.md)
</dt> <dt>

[**Pequeno**](small.md)
</dt> <dt>

[**Typedef**](typedef.md)
</dt> <dt>

[**Unsigned**](unsigned.md)
</dt> </dl>

 

 




