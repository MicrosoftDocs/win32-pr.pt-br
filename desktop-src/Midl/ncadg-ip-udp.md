---
title: ncadg_ip_udp atributo
description: A \_ \_ palavra-chave UDP IP ncadg identifica a versão do datagrama do TCP/IP como a família de protocolos para o ponto de extremidade. Esta família de protocolos está obsoleta e não deve ser usada em novos aplicativos.
ms.assetid: c9133fcc-6dc2-49da-9c6f-5ce3c51090d5
keywords:
- ncadg_ip_udp do atributo MIDL
topic_type:
- apiref
api_name:
- ncadg_ip_udp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 173ccd0b81eb5fa7d84a6fa4d2821162b852303d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104084488"
---
# <a name="ncadg_ip_udp-attribute"></a>\_atributo UDP de IP ncadg \_

A palavra-chave **\_ \_ UDP IP ncadg** identifica a versão do datagrama do TCP/IP como a família de protocolos para o ponto de extremidade. Esta família de protocolos está obsoleta e não deve ser usada em novos aplicativos.

``` syntax
endpoint("ncadg_ip_udp:server-name[port-name]")
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*nome do servidor* 
</dt> <dd>

Especifica o nome ou endereço de Internet para o servidor, ou host, computador. O nome é uma cadeia de caracteres e pode ser um nome de domínio totalmente qualificado. O endereço da Internet é uma notação de endereço da Internet comum.

</dd> <dt>

*nome da porta* 
</dt> <dd>

Especifica um número opcional de 16 bits. Valores menores que 1024 geralmente são reservados. Se nenhum valor for especificado, o serviço de mapeamento de ponto de extremidade selecionará um valor *de nome de porta* válido.

</dd> </dl>

## <a name="remarks"></a>Comentários

As restrições a seguir se aplicam aos protocolos de datagrama, [**ncadg \_ IPX**](ncadg-ipx.md) e **ncadg \_ IP \_ UDP**:

-   Eles não oferecem suporte a retornos de chamada. Qualquer função que use o atributo de **\[** [**retorno de chamada**](callback.md) **\]** falhará.
-   Eles não dão suporte ao uso do construtor de tipo de [**pipe**](pipe.md) .

A sintaxe da cadeia de caracteres da porta de transporte TCP/IP, como todas as cadeias de caracteres de porta, é definida independentemente da especificação IDL. O compilador executa alguma verificação de sintaxe, mas não garante que a especificação do ponto de extremidade esteja correta. Alguns erros podem ser relatados em tempo de execução em vez de em tempo de compilação.

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

[**ncalrpc**](ncalrpc.md)
</dt> <dt>

[**ncadg \_ IPX**](ncadg-ipx.md)
</dt> <dt>

[Associação de cadeia de caracteres](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 