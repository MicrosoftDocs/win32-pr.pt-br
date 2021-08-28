---
title: ncacn_vns_spp atributo
description: A palavra-chave \_ ncacn vns \_ spp identifica Banyan Vines SPP como a família de protocolo para o ponto de extremidade. Essa família de protocolos está obsoleta e não deve ser usada em novos aplicativos.
ms.assetid: a2aff0a6-2e7e-43e4-a180-f1ddd0456843
keywords:
- ncacn_vns_spp atributo MIDL
topic_type:
- apiref
api_name:
- ncacn_vns_spp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8409e7e9e0bfc01545ac73673f0653c5a4940c65422223233ec5005f5c9fc02
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119560276"
---
# <a name="ncacn_vns_spp-attribute"></a>Atributo ncacn \_ vns \_ spp

A **palavra-chave \_ ncacn vns \_ spp** identifica Banyan Vines SPP como a família de protocolo para o ponto de extremidade. Essa família de protocolos está obsoleta e não deve ser usada em novos aplicativos.

``` syntax
endpoint("ncacn_vns_spp:server-name[port-address]")
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*server-name* 
</dt> <dd>

Especifica o nome do StreetTalk do servidor. O nome é do formato item@group @organization . O item pode ter até 31 caracteres e o grupo e a organização podem ter até 15 caracteres.

</dd> <dt>

*port-name* 
</dt> <dd>

Especifica uma porta SPP Banyan Vines. O intervalo válido para pontos de extremidade estáticos é de 250 a 511.

</dd> </dl>

## <a name="remarks"></a>Comentários

Para usar o protocolo de transporte **\_ ncacn vns \_ spp** em aplicativos distribuídos em execução no Windows 2000, o software cliente Enterprise Banyan apropriado deve ser instalado. Após a instalação, abra **Painel de Controle**, escolha Configuração e Adicionar **e,** em seguida, selecione **Serviços \| RPC do Service Banyan \| para Banyan**. O suporte para clientes de 16 bits requer o software Vines apropriado. Para obter mais informações sobre o produto Enterprise Cliente do Banyan e o software Vines de 16 bits, entre em contato com Banyan.

A sintaxe da cadeia de caracteres de porta de transporte do Banyan Vines SPP, como todas as cadeias de caracteres de porta, é definida independentemente da especificação de IDL. O compilador executa alguma verificação de sintaxe, mas não garante que a especificação do ponto de extremidade está correta. Alguns erros podem ser relatados em tempo de run em vez de em tempo de compilação.

> [!Note]  
> Não há suporte para essa família de protocolos Windows XP.

 

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

[**ncalrpc**](ncalrpc.md)
</dt> <dt>

[**ncadg \_ ipx**](ncadg-ipx.md)
</dt> <dt>

[**ncadg \_ ip \_ udp**](ncadg-ip-udp.md)
</dt> <dt>

[associação de cadeia de caracteres](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 