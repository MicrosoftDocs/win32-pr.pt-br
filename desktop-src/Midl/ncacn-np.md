---
title: ncacn_np atributo
description: A \_ palavra-chave ncacn NP identifica pipes nomeados como a família de protocolos para o ponto de extremidade.
ms.assetid: 02961bb8-faf0-42e5-b134-dd2983e6d146
keywords:
- ncacn_np do atributo MIDL
topic_type:
- apiref
api_name:
- ncacn_np
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84634e6bb5d2b634439be767ad44749291cffe11
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103640958"
---
# <a name="ncacn_np-attribute"></a>\_atributo ncacn NP

A palavra-chave **ncacn \_ NP** identifica pipes nomeados como a família de protocolos para o ponto de extremidade.

``` syntax
endpoint("ncacn_np:server-name[\\pipe\\pipe-name]")
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*nome do servidor* 
</dt> <dd>

Opcional. Especifica o nome do servidor. Caracteres de barra invertida são opcionais.

</dd> <dt>

*nome do pipe* 
</dt> <dd>

Especifica um nome de pipe válido. Um nome de pipe válido é uma cadeia de caracteres que contém identificadores separados por caracteres de barra invertida. O primeiro identificador deve ser [**pipe**](pipe.md). Cada identificador deve ser separado por dois caracteres de barra invertida.

</dd> </dl>

## <a name="remarks"></a>Comentários

Um servidor cria uma instância de um pipe nomeado que está disponível para qualquer cliente. Quando um cliente tenta se conectar, a instância existente é associada a esse cliente. Antes que outro cliente possa se conectar, o servidor deve criar outra instância do pipe nomeado. Se um cliente tentar se associar ao servidor antes que a nova instância seja criada, a chamada de associação, [**RpcBindingFromStringBinding**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingfromstringbinding), poderá falhar com a mensagem de erro o servidor RPC está \_ \_ \_ muito \_ ocupado. Portanto, você precisa garantir que o aplicativo cliente manipule o caso em que o servidor está muito ocupado para aceitar uma conexão. O cliente deve repetir automaticamente, solicitar um curso de ação ao usuário ou falhar normalmente.

A sintaxe da cadeia de caracteres de porta de pipe nomeado, como todas as cadeias de caracteres de porta, é definida pela implementação de transporte e é independente da especificação de IDL. O compilador MIDL executa uma verificação de sintaxe limitada, mas não garante que a especificação do ponto de extremidade esteja correta. Algumas classes de erros podem ser relatadas em tempo de execução em vez de em tempo de compilação.

## <a name="examples"></a>Exemplos

``` syntax
[
    uuid(12345678-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncacn_np:[\\pipe\\stove\\hat]") 
] 
interface iface1
{
    // Interface definition statements.
}

[
    uuid(87654321-4000-2006-0000-20000000001b), 
    version(1.1), 
    endpoint("ncacn_np:\\\\myotherserver[\\pipe\\corncob]") 
] 
interface iface2
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

[**ncacn \_ VNS \_ spp**](ncacn-vns-spp.md)
</dt> <dt>

[**ncalrpc**](ncalrpc.md)
</dt> <dt>

[**ncadg \_ IPX**](ncadg-ipx.md)
</dt> <dt>

[**\_UDP IP \_ ncadg**](ncadg-ip-udp.md)
</dt> <dt>

[**Associação de cadeia de caracteres**](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 