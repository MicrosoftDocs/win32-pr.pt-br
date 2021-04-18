---
title: ncacn_spx atributo
description: A \_ palavra-chave ncacn SPX identifica SPX como a família de protocolos para o ponto de extremidade. Esta família de protocolos está obsoleta e não deve ser usada em novos aplicativos.
ms.assetid: 45e93e25-e84d-4242-80b0-c4b61e80f716
keywords:
- ncacn_spx do atributo MIDL
topic_type:
- apiref
api_name:
- ncacn_spx
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09d27cc746df906ff6b1a3290e41d860c76dc362
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "105764674"
---
# <a name="ncacn_spx-attribute"></a>\_atributo ncacn SPX

A palavra-chave **ncacn \_ SPX** identifica SPX como a família de protocolos para o ponto de extremidade. Esta família de protocolos está obsoleta e não deve ser usada em novos aplicativos.

``` syntax
endpoint("ncacn_spx:link-address[port-name]")
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Endereço de link* 
</dt> <dd>

Especifica o servidor host. Pode ser uma cadeia de caracteres (o nome do servidor) ou um número hexadecimal de 20 dígitos que consiste no endereço de rede do servidor host (8 dígitos) concatenado com o endereço do nó (12 dígitos). Consulte comentários para obter instruções sobre como obter o endereço de rede e o endereço do nó. Uma cadeia de caracteres **nula** especifica o computador local.

</dd> <dt>

*nome da porta* 
</dt> <dd>

Especifica um número opcional de 16 bits que representa o endereço do soquete. Os valores podem variar de 1 a 65.535. Quando nenhum valor é especificado, o serviço de mapeamento de ponto de extremidade seleciona um valor *de nome de porta* válido.

</dd> </dl>

## <a name="remarks"></a>Comentários

Quando você usa o transporte **ncacn \_ SPX** , o nome do servidor é exatamente o mesmo que o nome do Windows de 32 bits. No entanto, como os nomes são distribuídos usando protocolos Novell, eles devem estar em conformidade com as convenções de nomenclatura da Novell. Se um nome de servidor não for um nome Novell válido, os servidores não poderão criar pontos de extremidade com o transporte **ncacn \_ SPX** . A seguir está uma lista parcial de caracteres proibidos em nomes de servidor Novell:

" \* + . / : ; < = >? \[ \] \\ \|

O transporte **ncacn \_ SPX** não é compatível com a versão do NWLink fornecida com o MS Client 3,0.

aplicativos cliente do Windows de 16 bits que usam o transporte **ncacn \_ SPX** exigem que o arquivo Nwipxspx.dll ser instalado para ser executado no subsistema WOW. Contate a Novell para obter esse arquivo.

> [!Note]  
> Para obter os endereços de rede e nó, use o utilitário **ComCheck** do Novell ou a API definida pela Novell **IPXGetInternetAddress**. No Windows, você também pode obter esses endereços com o comando **ipxroute config** .

 

A sintaxe da cadeia de caracteres da porta de transporte SPX, como todas as cadeias de caracteres de porta, é definida independentemente da especificação IDL. O compilador executa alguma verificação de sintaxe, mas não garante que a especificação do ponto de extremidade esteja correta. Alguns erros podem ser relatados em tempo de execução em vez de em tempo de compilação.

## <a name="examples"></a>Exemplos

``` syntax
[
    uuid(12345678-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncacn_spx:[1000]") 
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

[**\_UDP IP \_ ncadg**](ncadg-ip-udp.md)
</dt> <dt>

[Associação de cadeia de caracteres](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 