---
title: ncacn_nb_ipx atributo
description: A palavra-chave \_ ncacn nb \_ ipx identifica NetBIOS sobre IPX como a família de protocolo para o ponto de extremidade. Essa família de protocolos está obsoleta e não deve ser usada em novos aplicativos.
ms.assetid: 641471d4-eba4-4d4a-a3fe-1e40b3751e38
keywords:
- ncacn_nb_ipx atributo MIDL
topic_type:
- apiref
api_name:
- ncacn_nb_ipx
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c8be67485d86a6094e2a41c01d5e0cf78cdabe5e251a3ab9ae046a47ed05d6d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118642217"
---
# <a name="ncacn_nb_ipx-attribute"></a>Atributo ncacn \_ nb \_ ipx

A **palavra-chave \_ ncacn nb \_ ipx** identifica NetBIOS sobre IPX como a família de protocolo para o ponto de extremidade. Essa família de protocolos está obsoleta e não deve ser usada em novos aplicativos.

``` syntax
endpoint("ncacn_nb_ipx:[port-name]")
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*port-name* 
</dt> <dd>

Especifica um valor opcional de 8 bits que varia de 1 a 254. Valores menores que 0x20 são reservados. Se o *valor de nome da* porta não for especificado, o serviço de mapeamento de ponto de extremidade selecionará o valor da porta.

</dd> </dl>

## <a name="remarks"></a>Comentários

A sintaxe da cadeia de caracteres de porta NetBIOS, como todas as cadeias de caracteres de porta, é definida pela implementação de transporte e é independente da especificação de IDL. O compilador MIDL executa verificação de sintaxe limitada, mas não garante que a especificação do ponto de extremidade está correta. Algumas classes de erros podem ser relatadas em tempo de run em vez de em tempo de compilação.

> [!Note]  
> Não há suporte para essa família de protocolos no Windows XP.

 

## <a name="examples"></a>Exemplos

``` syntax
[
    uuid(12345678-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncacn_nb_ipx:[100]") 
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

[**ncacn \_ ip \_ tcp**](ncacn-ip-tcp.md)
</dt> <dt>

[**ncacn \_ nb \_ tcp**](ncacn-nb-tcp.md)
</dt> <dt>

[**ncacn \_ nb \_ nb**](ncacn-nb-nb.md)
</dt> <dt>

[**ncacn \_ em \_ dsp**](ncacn-at-dsp.md)
</dt> <dt>

[**ncacn \_ spx**](ncacn-spx.md)
</dt> <dt>

[**ncacn \_ np**](ncacn-np.md)
</dt> <dt>

[**ncalrpc**](ncalrpc.md)
</dt> <dt>

[**ncadg \_ ip \_ udp**](ncadg-ip-udp.md)
</dt> <dt>

[**ncadg \_ ipx**](ncadg-ipx.md)
</dt> <dt>

[**associação de cadeia de caracteres**](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 