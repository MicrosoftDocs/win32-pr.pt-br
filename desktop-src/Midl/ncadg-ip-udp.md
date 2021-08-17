---
title: ncadg_ip_udp atributo
description: A palavra-chave ncadg ip udp identifica a \_ versão do \_ datagrama de TCP/IP como a família de protocolos para o ponto de extremidade. Essa família de protocolos está obsoleta e não deve ser usada em novos aplicativos.
ms.assetid: c9133fcc-6dc2-49da-9c6f-5ce3c51090d5
keywords:
- ncadg_ip_udp atributo MIDL
topic_type:
- apiref
api_name:
- ncadg_ip_udp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f91db32fd7636f956e64dafc0db15efb520e643b435995dd977db7a631a20c78
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067056"
---
# <a name="ncadg_ip_udp-attribute"></a>atributo ncadg \_ ip \_ udp

A **palavra-chave ncadg \_ ip \_ udp** identifica a versão do datagrama de TCP/IP como a família de protocolos para o ponto de extremidade. Essa família de protocolos está obsoleta e não deve ser usada em novos aplicativos.

``` syntax
endpoint("ncadg_ip_udp:server-name[port-name]")
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*server-name* 
</dt> <dd>

Especifica o nome ou o endereço da Internet para o servidor ou host, computador. O nome é uma cadeia de caracteres e pode ser um nome de domínio totalmente qualificado. O endereço da Internet é uma notação de endereço da Internet comum.

</dd> <dt>

*port-name* 
</dt> <dd>

Especifica um número opcional de 16 bits. Valores menores que 1024 geralmente são reservados. Se nenhum valor for especificado, o serviço de mapeamento de ponto de extremidade selecionará um valor *de nome de porta* válido.

</dd> </dl>

## <a name="remarks"></a>Comentários

As seguintes restrições se aplicam aos protocolos de datagram, [**ncadg \_ ipx**](ncadg-ipx.md) e **ncadg \_ ip \_ udp**:

-   Eles não são suportados retornos de chamada. Todas as funções que usam o **\[** [**atributo de retorno de**](callback.md) chamada **\]** falharão.
-   Eles não suportam o uso do [**construtor de tipo**](pipe.md) pipe.

A sintaxe da cadeia de caracteres de porta de transporte TCP/IP, como todas as cadeias de caracteres de porta, é definida independentemente da especificação de IDL. O compilador executa alguma verificação de sintaxe, mas não garante que a especificação do ponto de extremidade está correta. Alguns erros podem ser relatados em tempo de run em vez de em tempo de compilação.

## <a name="examples"></a>Exemplos

``` syntax
[
    uuid(12345678-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncadg_ip_udp:rainier[1404]") 
]
interface iface1
{
    // Interface definition statements.
}

[
    uuid(87654321-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncadg_ip_udp:128.10.2.30[1404]") 
]
interface iface2
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

[**ncalrpc**](ncalrpc.md)
</dt> <dt>

[**ncadg \_ ipx**](ncadg-ipx.md)
</dt> <dt>

[Associação de cadeia de caracteres](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 