---
title: ncacn_nb_nb atributo
description: A \_ \_ palavra-chave NB do ncacn NB identifica NetBEUI sobre NetBIOS como a família de protocolos para o ponto de extremidade. Esta família de protocolos está obsoleta e não deve ser usada em novos aplicativos.
ms.assetid: 8bab2784-44ba-4356-85c1-5bd17e75d6a8
keywords:
- ncacn_nb_nb do atributo MIDL
topic_type:
- apiref
api_name:
- ncacn_nb_nb
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84a2ea48bc1472d69c2247f227b94193326927481838894e24efbce9e09afc87
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118642144"
---
# <a name="ncacn_nb_nb-attribute"></a>\_ \_ atributo NB do ncacn NB

A palavra-chave **\_ \_ NB do ncacn NB** identifica NetBEUI sobre NetBIOS como a família de protocolos para o ponto de extremidade. Esta família de protocolos está obsoleta e não deve ser usada em novos aplicativos.

``` syntax
endpoint("ncacn_nb_nb:[port-name]")
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*nome da porta* 
</dt> <dd>

Especifica um valor opcional de 8 bits que varia de 1 a 255. Valores menores que 0x20 são reservados. Se o valor de *Port-Name* não for especificado, o serviço de mapeamento de ponto de extremidade selecionará o valor da porta.

</dd> </dl>

## <a name="remarks"></a>Comentários

A sintaxe da cadeia de caracteres de porta NetBIOS, como todas as cadeias de porta, é definida pela implementação de transporte e é independente da especificação de IDL. O compilador MIDL executa uma verificação de sintaxe limitada, mas não garante que a especificação do ponto de extremidade esteja correta. Algumas classes de erros podem ser relatadas em tempo de execução em vez de em tempo de compilação.

> [!Note]  
> Não há suporte para essa família de protocolos no WindowsÂ XP.

 

## <a name="examples"></a>Exemplos

``` syntax
[
    uuid(12345678-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncacn_nb_nb:[100]") 
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

[**\_TCP IP \_ ncacn**](ncacn-ip-tcp.md)
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

 

 