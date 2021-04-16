---
title: ncacn_nb_ipx atributo
description: A \_ \_ palavra-chave IPX do ncacn NB identifica o NetBIOS sobre IPX como a família de protocolos para o ponto de extremidade. Esta família de protocolos está obsoleta e não deve ser usada em novos aplicativos.
ms.assetid: 641471d4-eba4-4d4a-a3fe-1e40b3751e38
keywords:
- ncacn_nb_ipx do atributo MIDL
topic_type:
- apiref
api_name:
- ncacn_nb_ipx
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 156b5c460c4cc8638640e7eb3500ec9a7a9fa0b0
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "105750263"
---
# <a name="ncacn_nb_ipx-attribute"></a>\_ \_ atributo IPX do ncacn NB

A palavra-chave **\_ \_ IPX do ncacn NB** identifica o NetBIOS sobre IPX como a família de protocolos para o ponto de extremidade. Esta família de protocolos está obsoleta e não deve ser usada em novos aplicativos.

``` syntax
endpoint("ncacn_nb_ipx:[port-name]")
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*nome da porta* 
</dt> <dd>

Especifica um valor opcional de 8 bits que varia de 1 a 254. Valores menores que 0x20 são reservados. Se o valor de *Port-Name* não for especificado, o serviço de mapeamento de ponto de extremidade selecionará o valor da porta.

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
    endpoint("ncacn_nb_ipx:[100]") 
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

[**ncacn \_ NB NB \_**](ncacn-nb-nb.md)
</dt> <dt>

[**ncacn \_ no \_ DSP**](ncacn-at-dsp.md)
</dt> <dt>

[**ncacn \_ SPX**](ncacn-spx.md)
</dt> <dt>

[**ncacn \_ NP**](ncacn-np.md)
</dt> <dt>

[**ncalrpc**](ncalrpc.md)
</dt> <dt>

[**\_UDP IP \_ ncadg**](ncadg-ip-udp.md)
</dt> <dt>

[**ncadg \_ IPX**](ncadg-ipx.md)
</dt> <dt>

[**Associação de cadeia de caracteres**](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 