---
title: ncacn_dnet_nsp atributo
description: A palavra-chave ncacn \_ dnet \_ nsp identifica DECnet como a família de protocolo para o ponto de extremidade. Essa família de protocolos está obsoleta e não deve ser usada em novos aplicativos.
ms.assetid: 797251c1-c5d3-416b-8bc7-5b83bb7027e6
keywords:
- ncacn_dnet_nsp atributo MIDL
topic_type:
- apiref
api_name:
- ncacn_dnet_nsp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4fa7448ff9d0cf3946ad3d0293ade19a5c2c0c407ca157d79c2c425f4a8ef6d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118642757"
---
# <a name="ncacn_dnet_nsp-attribute"></a>Atributo ncacn \_ dnet \_ nsp

A **palavra-chave ncacn \_ dnet \_ nsp** identifica DECnet como a família de protocolo para o ponto de extremidade. Essa família de protocolos está obsoleta e não deve ser usada em novos aplicativos.

``` syntax
endpoint("ncacn_dnet_nsp:server-name[port-name]")
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*server-name* 
</dt> <dd>

Especifica o nome ou o endereço da Internet para o servidor ou host, computador. O nome é uma cadeia de caracteres.

</dd> <dt>

*port-name* 
</dt> <dd>

Especifica um nome de objeto DECnet ou um número de objeto. O nome do objeto pode consistir em até 16 caracteres. Os números de objeto podem ser prefixados pelo sinal de peso ( \# ).

</dd> </dl>

## <a name="remarks"></a>Comentários

A sintaxe da cadeia de caracteres de porta de transporte de DECnet, como todas as cadeias de caracteres de porta, é definida independentemente da especificação de IDL. O compilador executa alguma verificação de sintaxe, mas não garante que a especificação do ponto de extremidade está correta. Alguns erros podem ser relatados em tempo de run em vez de em tempo de compilação.

> [!Note]  
> Não há suporte para essa família de protocolos no Windows XP.

 

## <a name="examples"></a>Exemplos

``` syntax
[   
    uuid(12345678-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncacn_dnet_nsp:node[RPC0034501]") 
interface iface
{
    // Interface definition statements.
}

[
    uuid(12345678-1234-1234-1234-123456789ABC), 
    version(1.1), 
    endpoint("ncacn_dnet_nsp:node[#41]") 
] 
interface iface
{
    // Interface definition statements.
}
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Extremidade**](endpoint.md)
</dt> <dt>

[**associação de cadeia de caracteres**](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 