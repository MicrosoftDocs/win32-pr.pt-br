---
title: atributo do Hyper
description: A palavra-chave Hyper indica um inteiro de 64 bits que pode ser declarado como assinado ou não assinado.
ms.assetid: cadcacc7-8eea-4ce2-b69f-98a1d8bafeaa
keywords:
- MIDL do atributo do Hyper
topic_type:
- apiref
api_name:
- hyper
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57da7c0d54e5b9ffcd47f76b22825d13b0a8cff9
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103638425"
---
# <a name="hyper-attribute"></a>atributo do Hyper

A palavra-chave **Hyper** indica um inteiro de 64 bits que pode ser declarado como assinado ou não assinado.

``` syntax
[ signed | unsigned ] hyper [ int ] declarator-list;
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Declarador-lista* 
</dt> <dd>

Especifica um ou mais declaradores C padrão, como identificadores, declaradores de ponteiro e declaradores de matriz. (Os declaradores de função e as declarações de campo de bits não são permitidas em estruturas que são transmitidas em chamadas de procedimento remoto. Esses declaradores são permitidos em estruturas que não são transmitidas.) Separe vários declaradores com vírgulas.

</dd> </dl>

## <a name="remarks"></a>Comentários

O tipo de **Hyper** é um dos tipos base da IDL (Interface Definition Language). O tipo de **Hyper** pode aparecer como um especificador de tipo em declarações [**const**](const.md) , declarações de [**typedef**](typedef.md) , declarações gerais e declaradores de função (como um especificador de tipo de retorno de função e como um especificador de tipo de parâmetro). Para o contexto no qual os especificadores de tipo aparecem, consulte [arquivo de definição de interface (IDL)](interface-definition-idl-file.md).

> [!Note]  
> Para plataformas de 16 bits, o compilador MIDL substitui o Hyper inteiros não assinados por **MIDL \_ uhyper**. Isso permite que as interfaces com inteiros de Hyper não assinados sejam definidas em plataformas que não dão suporte diretamente a inteiros de 64 bits. O **MIDL \_ uhyper** é definido nos arquivos de cabeçalho RPC.

 

## <a name="see-also"></a>Consulte também

<dl> <dt>

[Tipos base de MIDL](midl-base-types.md)
</dt> <dt>

[**const**](const.md)
</dt> <dt>

[Arquivo de definição de interface (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**typedef**](typedef.md)
</dt> </dl>

 

 




