---
title: ncacn_dnet_nsp atributo
description: A \_ \_ palavra-chave ncacn dnet NSP identifica o DECnet como a família de protocolos para o ponto de extremidade. Esta família de protocolos está obsoleta e não deve ser usada em novos aplicativos.
ms.assetid: 797251c1-c5d3-416b-8bc7-5b83bb7027e6
keywords:
- ncacn_dnet_nsp do atributo MIDL
topic_type:
- apiref
api_name:
- ncacn_dnet_nsp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6312aff15d3bdef85d1e37829d669ce1faa5fbb4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104084525"
---
# <a name="ncacn_dnet_nsp-attribute"></a>\_atributo ncacn dnet \_ NSP

A palavra-chave **ncacn \_ dnet \_ NSP** identifica o DECnet como a família de protocolos para o ponto de extremidade. Esta família de protocolos está obsoleta e não deve ser usada em novos aplicativos.

``` syntax
endpoint("ncacn_dnet_nsp:server-name[port-name]")
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*nome do servidor* 
</dt> <dd>

Especifica o nome ou endereço de Internet para o servidor, ou host, computador. O nome é uma cadeia de caracteres.

</dd> <dt>

*nome da porta* 
</dt> <dd>

Especifica um nome de objeto ou número de objeto DECnet. O nome do objeto pode consistir em até 16 caracteres. Os números de objeto podem ser prefixados pelo sinal de libra ( \# ).

</dd> </dl>

## <a name="remarks"></a>Comentários

A sintaxe da cadeia de caracteres da porta de transporte DECnet, como todas as cadeias de caracteres de porta, é definida independentemente da especificação IDL. O compilador executa alguma verificação de sintaxe, mas não garante que a especificação do ponto de extremidade esteja correta. Alguns erros podem ser relatados em tempo de execução em vez de em tempo de compilação.

> [!Note]  
> Não há suporte para essa família de protocolos no WindowsÂ XP.

 

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

[**extremidade**](endpoint.md)
</dt> <dt>

[**Associação de cadeia de caracteres**](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 