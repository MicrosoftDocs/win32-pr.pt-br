---
title: atributo Ncalrpc
description: A palavra-chave Ncalrpc identifica a comunicação entre processos local como a família de protocolos para o ponto de extremidade. Essa palavra-chave é um dos nomes de família de protocolos válidos que devem ser usados com o atributo \ Endpoint \.
ms.assetid: 0009f794-5c14-4484-9023-cb20c7030dc5
keywords:
- Ncalrpc do atributo MIDL
topic_type:
- apiref
api_name:
- ncalrpc
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f20ae9e347303288868eeb16758736047fecc1b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103917270"
---
# <a name="ncalrpc-attribute"></a>atributo Ncalrpc

A palavra-chave **Ncalrpc** identifica a comunicação entre processos local como a família de protocolos para o ponto de extremidade. Essa palavra-chave é um dos nomes de família de protocolos válidos que devem ser usados com o atributo de **\[** [**ponto de extremidade**](endpoint.md) **\]** .

``` syntax
endpoint("ncalrpc:[port-name]")
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*nome da porta* 
</dt> <dd>

Uma cadeia de caracteres que especifica a porta de comunicação (um aplicativo, um serviço ou uma instância de um serviço) que um cliente usa para fazer chamadas entre processos em um servidor. A cadeia de caracteres pode conter até 53 caracteres e não deve conter nenhuma barra invertida ( \) caracteres. O nome do computador não deve ser usado com a palavra-chave **Ncalrpc** .

</dd> </dl>

## <a name="remarks"></a>Comentários

A sintaxe da cadeia de caracteres da porta de comunicação entre processos local, como todas as cadeias de porta, é definida pela implementação do transporte e é independente da especificação de IDL. O compilador MIDL executa uma verificação de sintaxe limitada, mas não garante que a especificação do ponto de extremidade esteja correta. Algumas classes de erros podem ser relatadas em tempo de execução em vez de em tempo de compilação.

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

[**extremidade**](endpoint.md)
</dt> <dt>

[Arquivo de definição de interface (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**ncacn \_ no \_ DSP**](ncacn-at-dsp.md)
</dt> <dt>

[**ncacn \_ dnet \_ NSP**](ncacn-dnet-nsp.md)
</dt> <dt>

[**\_TCP IP \_ ncacn**](ncacn-ip-tcp.md)
</dt> <dt>

[**IPX do ncacn \_ NB \_**](ncacn-nb-ipx.md)
</dt> <dt>

[**ncacn \_ SPX**](ncacn-spx.md)
</dt> <dt>

[**ncacn \_ NB NB \_**](ncacn-nb-nb.md)
</dt> <dt>

[**ncacn \_ NB \_ TCP**](ncacn-nb-tcp.md)
</dt> <dt>

[**ncacn \_ NP**](ncacn-np.md)
</dt> <dt>

[**ncacn \_ VNS \_ spp**](ncacn-vns-spp.md)
</dt> <dt>

[**\_UDP IP \_ ncadg**](ncadg-ip-udp.md)
</dt> <dt>

[**ncadg \_ IPX**](ncadg-ipx.md)
</dt> <dt>

[Associação de cadeia de caracteres](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 