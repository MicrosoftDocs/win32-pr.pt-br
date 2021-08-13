---
title: ncacn_nb_tcp atributo
description: A palavra-chave tcp ncacn nb é usada para identificar o TCP sobre NetBIOS como a família de protocolo \_ para o ponto de \_ extremidade. Essa família de protocolos está obsoleta e não deve ser usada em novos aplicativos.
ms.assetid: 3633842c-d1f5-46d9-866e-e54f31415ea5
keywords:
- ncacn_nb_tcp atributo MIDL
topic_type:
- apiref
api_name:
- ncacn_nb_tcp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 683be3c986c81feb270d5d502f3da0f56a65d78973c60e4b664c2e4bd75e0494
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118642161"
---
# <a name="ncacn_nb_tcp-attribute"></a>Atributo \_ tcp ncacn \_ nb

A **palavra-chave \_ \_ tcp ncacn nb** é usada para identificar o TCP sobre NetBIOS como a família de protocolo para o ponto de extremidade. Essa família de protocolos está obsoleta e não deve ser usada em novos aplicativos.

``` syntax
endpoint("ncacn_nb_tcp:[port-name]")
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
    endpoint("ncacn_nb_tcp:[100]") 
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

[**ncacn \_ nb \_ nb**](ncacn-nb-nb.md)
</dt> <dt>

[**ncacn \_ np**](ncacn-np.md)
</dt> <dt>

[**ncacn \_ spx**](ncacn-spx.md)
</dt> <dt>

[**ncalrpc**](ncalrpc.md)
</dt> <dt>

[**associação de cadeia de caracteres**](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 