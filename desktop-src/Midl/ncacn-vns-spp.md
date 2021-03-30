---
title: ncacn_vns_spp atributo
description: A \_ \_ palavra-chave ncacn VNS spp identifica Banyan Vines spp como a família de protocolos para o ponto de extremidade. Esta família de protocolos está obsoleta e não deve ser usada em novos aplicativos.
ms.assetid: a2aff0a6-2e7e-43e4-a180-f1ddd0456843
keywords:
- ncacn_vns_spp do atributo MIDL
topic_type:
- apiref
api_name:
- ncacn_vns_spp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84e72cd17ae65fbffc2cef280f15d12ba0ddbdbe
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103640794"
---
# <a name="ncacn_vns_spp-attribute"></a>\_atributo ncacn VNS \_ spp

A palavra-chave **ncacn \_ VNS \_ spp** identifica Banyan Vines spp como a família de protocolos para o ponto de extremidade. Esta família de protocolos está obsoleta e não deve ser usada em novos aplicativos.

``` syntax
endpoint("ncacn_vns_spp:server-name[port-address]")
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*nome do servidor* 
</dt> <dd>

Especifica o nome do StreetTalk do servidor. O nome está no formato item@group @organization . O item pode ter até 31 caracteres de comprimento e o grupo e a organização podem ter até 15 caracteres.

</dd> <dt>

*nome da porta* 
</dt> <dd>

Especifica uma porta Banyan Vines SPP. O intervalo válido para pontos de extremidade estáticos é 250 – 511.

</dd> </dl>

## <a name="remarks"></a>Comentários

Para usar o protocolo de transporte **ncacn \_ VNS \_ spp** em aplicativos distribuídos em execução no Windows 2000, o software Banyan cliente corporativo apropriado deve ser instalado. Após a instalação, abra o **painel de controle**, escolha **configuração e adicionar e**, em seguida, selecione **\| \| serviços de RPC de Banyan para Banyan**. O suporte para clientes de 16 bits requer um software de Vines apropriado. Para obter mais informações sobre o produto de Cliente Corporativo da Banyan e o software de Vines de 16 bits, entre em contato com a Banyan.

A sintaxe da cadeia de caracteres de porta de transporte Banyan Vines SPP, como todas as cadeias de caracteres de porta, é definida independentemente da especificação de IDL. O compilador executa alguma verificação de sintaxe, mas não garante que a especificação do ponto de extremidade esteja correta. Alguns erros podem ser relatados em tempo de execução em vez de em tempo de compilação.

> [!Note]  
> Não há suporte para essa família de protocolos no Windows XP.

 

## <a name="examples"></a>Exemplos

``` syntax
[
    uuid(12345678-1234-1234-1234-123456789ABC), 
    version(1.1), 
    endpoint("ncacn_vns_spp:printer@sdkgrp@company[260]")
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

[**ncalrpc**](ncalrpc.md)
</dt> <dt>

[**ncadg \_ IPX**](ncadg-ipx.md)
</dt> <dt>

[**\_UDP IP \_ ncadg**](ncadg-ip-udp.md)
</dt> <dt>

[Associação de cadeia de caracteres](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 