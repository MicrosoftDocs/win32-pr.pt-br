---
title: Atributo ncalrpc
description: A palavra-chave ncalrpc identifica a comunicação entre processos local como a família de protocolos para o ponto de extremidade. Essa palavra-chave é um dos nomes de família de protocolo válidos que devem ser usados com o atributo \ endpoint\.
ms.assetid: 0009f794-5c14-4484-9023-cb20c7030dc5
keywords:
- Atributo ncalrpc MIDL
topic_type:
- apiref
api_name:
- ncalrpc
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 481f005a741c6a815572f5861755f52d5921bae89e8bb2d8a3ef757a0fc42d9e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119066996"
---
# <a name="ncalrpc-attribute"></a>Atributo ncalrpc

A **palavra-chave ncalrpc** identifica a comunicação entre processos local como a família de protocolos para o ponto de extremidade. Essa palavra-chave é um dos nomes de família de protocolo válidos que devem ser usados com o atributo **\[** [**de ponto de**](endpoint.md) **\]** extremidade.

``` syntax
endpoint("ncalrpc:[port-name]")
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*port-name* 
</dt> <dd>

Uma cadeia de caracteres que especifica a porta de comunicação (um aplicativo, um serviço ou uma instância de um serviço) que um cliente usa para fazer chamadas de interprocessamento para um servidor. A cadeia de caracteres pode conter até 53 caracteres e não deve conter nenhum caractere de invertida ( \\ ). O nome do computador não deve ser usado com a palavra-chave **ncalrpc.**

</dd> </dl>

## <a name="remarks"></a>Comentários

A sintaxe da cadeia de caracteres da porta interprocess-communication local, como todas as cadeias de caracteres de porta, é definida pela implementação de transporte e é independente da especificação de IDL. O compilador MIDL executa verificação de sintaxe limitada, mas não garante que a especificação do ponto de extremidade está correta. Algumas classes de erros podem ser relatadas em tempo de run em vez de em tempo de compilação.

## <a name="examples"></a>Exemplos

``` syntax
[
    uuid(12345678-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncalrpc:[myapplicationname]") 
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

[Arquivo IDL (definição de interface)](interface-definition-idl-file.md)
</dt> <dt>

[**ncacn \_ em \_ dsp**](ncacn-at-dsp.md)
</dt> <dt>

[**ncacn \_ dnet \_ nsp**](ncacn-dnet-nsp.md)
</dt> <dt>

[**ncacn \_ ip \_ tcp**](ncacn-ip-tcp.md)
</dt> <dt>

[**ncacn \_ nb \_ ipx**](ncacn-nb-ipx.md)
</dt> <dt>

[**ncacn \_ spx**](ncacn-spx.md)
</dt> <dt>

[**ncacn \_ nb \_ nb**](ncacn-nb-nb.md)
</dt> <dt>

[**ncacn \_ nb \_ tcp**](ncacn-nb-tcp.md)
</dt> <dt>

[**ncacn \_ np**](ncacn-np.md)
</dt> <dt>

[**ncacn \_ vns \_ spp**](ncacn-vns-spp.md)
</dt> <dt>

[**ncadg \_ ip \_ udp**](ncadg-ip-udp.md)
</dt> <dt>

[**ncadg \_ ipx**](ncadg-ipx.md)
</dt> <dt>

[Associação de cadeia de caracteres](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 