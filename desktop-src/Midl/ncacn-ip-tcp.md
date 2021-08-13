---
title: ncacn_ip_tcp atributo
description: A \_ \_ palavra-chave TCP IP NCACN identifica TCP/IP como a família de protocolos para o ponto de extremidade.
ms.assetid: 8142c667-9a5f-4066-a36d-1bb5ce551d21
keywords:
- ncacn_ip_tcp do atributo MIDL
topic_type:
- apiref
api_name:
- ncacn_ip_tcp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c34ba0a872af79245469818121761a38d356316b53a31743f9ebf2cd66f72325
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118642219"
---
# <a name="ncacn_ip_tcp-attribute"></a>\_atributo TCP de IP ncacn \_

A palavra-chave **\_ \_ TCP IP ncacn** identifica TCP/IP como a família de protocolos para o ponto de extremidade.

``` syntax
endpoint("ncacn_ip_tcp:server-name[port-name]")
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*nome do servidor* 
</dt> <dd>

Especifica o nome ou endereço de Internet para o servidor, ou host, computador. O nome é uma cadeia de caracteres. O endereço da Internet é uma notação de endereço da Internet comum.

</dd> <dt>

*nome da porta* 
</dt> <dd>

Especifica um número opcional de 16 bits. Valores menores que 1024 geralmente são reservados. Se nenhum valor for especificado, o serviço de mapeamento de ponto de extremidade selecionará um valor *de nome de porta* válido.

</dd> </dl>

## <a name="remarks"></a>Comentários

A sintaxe da cadeia de caracteres da porta de transporte TCP/IP, como todas as cadeias de caracteres de porta, é definida independentemente da especificação IDL. O compilador executa alguma verificação de sintaxe, mas não garante que a especificação do ponto de extremidade esteja correta. Alguns erros podem ser relatados em tempo de execução em vez de em tempo de compilação.

## <a name="examples"></a>Exemplos

``` syntax
[   
    uuid(12345678-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncacn_ip_tcp:rainier[1404]") 
]
interface iface
{
    // Interface definition statements.
}

 
endpoint("ncacn_ip_tcp:128.10.2.30[1404]")
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[**extremidade**](endpoint.md)
</dt> <dt>

[Arquivo de definição de interface (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**ncacn \_ NB \_ TCP**](ncacn-nb-tcp.md)
</dt> <dt>

[**ncacn \_ NP**](ncacn-np.md)
</dt> <dt>

[**ncacn \_ SPX**](ncacn-spx.md)
</dt> <dt>

[**ncalrpc**](ncalrpc.md)
</dt> <dt>

[**Associação de cadeia de caracteres**](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 