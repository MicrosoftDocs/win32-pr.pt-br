---
title: atributo hyper
description: A palavra-chave hyper indica um inteiro de 64 bits que pode ser declarado como assinado ou não assinado.
ms.assetid: cadcacc7-8eea-4ce2-b69f-98a1d8bafeaa
keywords:
- atributo hyper MIDL
topic_type:
- apiref
api_name:
- hyper
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44f202890d2d81dcd7916f29c0330bf8e7093a7cf189e7b76a8af64dd2f0d0a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119895256"
---
# <a name="hyper-attribute"></a>atributo hyper

A **palavra-chave hyper** indica um inteiro de 64 bits que pode ser declarado como assinado ou não assinado.

``` syntax
[ signed | unsigned ] hyper [ int ] declarator-list;
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*declarator-list* 
</dt> <dd>

Especifica um ou mais declaradores C padrão, como identificadores, declaradores de ponteiro e declaradores de matriz. (Declaradores de função e declarações de campo de bits não são permitidos em estruturas transmitidas em chamadas de procedimento remoto. Esses declaradores são permitidos em estruturas que não são transmitidas.) Separe vários declaradores com vírgulas.

</dd> </dl>

## <a name="remarks"></a>Comentários

O **tipo** hyper é um dos tipos base da IDL (linguagem de definição de interface). O **tipo hyper** pode aparecer como um especificador de tipo em declarações [**const,**](const.md) declarações [**typedef,**](typedef.md) declarações gerais e declaradores de função (como um especificador de tipo de retorno de função e como um especificador de tipo de parâmetro). Para o contexto no qual os especificadores de tipo aparecem, consulte [Arquivo de definição de interface (IDL).](interface-definition-idl-file.md)

> [!Note]  
> Para plataformas de 16 bits, o compilador MIDL substitui os hiper inteiros sem sinal por **\_ midl uhyper**. Isso permite que interfaces com hiper inteiros sem sinal sejam definidas em plataformas que não suportam diretamente inteiros de 64 bits. **O \_ uhyper MIDL** é definido nos arquivos de header RPC.

 

## <a name="see-also"></a>Confira também

<dl> <dt>

[Tipos base MIDL](midl-base-types.md)
</dt> <dt>

[**const**](const.md)
</dt> <dt>

[Arquivo IDL (definição de interface)](interface-definition-idl-file.md)
</dt> <dt>

[**Typedef**](typedef.md)
</dt> </dl>

 

 




