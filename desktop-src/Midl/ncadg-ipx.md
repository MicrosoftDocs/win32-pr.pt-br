---
title: ncadg_ipx atributo
description: A palavra-chave \_ ncadg ipx identifica IPX como a família de protocolo para o ponto de extremidade. Essa família de protocolos está obsoleta e não deve ser usada em novos aplicativos.
ms.assetid: 6b136eb9-4e18-43ff-993b-a2ad005273f1
keywords:
- ncadg_ipx atributo MIDL
topic_type:
- apiref
api_name:
- ncadg_ipx
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dbca1ef3cb5f51e54fe8b95aa16326c6438903ff9717258edea9fac491eebafa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067046"
---
# <a name="ncadg_ipx-attribute"></a>Atributo ncadg \_ ipx

A **palavra-chave \_ ncadg ipx** identifica IPX como a família de protocolo para o ponto de extremidade. Essa família de protocolos está obsoleta e não deve ser usada em novos aplicativos.

``` syntax
endpoint("ncadg_ipx:link-address[port-name]")
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*link-address* 
</dt> <dd>

Especifica o servidor host. Isso pode ser uma cadeia de caracteres (o nome do servidor) ou um número hexadecimal de 20 dígitos que consiste no endereço de rede do servidor host (8 dígitos) concatenado com o endereço do nó (12 dígitos). Consulte Comentários para obter instruções sobre como obter o endereço de rede e o endereço do nó. Uma **cadeia de** caracteres NULL especifica o computador local.

</dd> <dt>

*port-name* 
</dt> <dd>

Especifica um número opcional de 16 bits que representa o endereço do soquete. Os valores podem variar de 1 a 65535. Quando nenhum valor é especificado, o serviço de mapeamento de ponto de extremidade seleciona um valor *de nome de porta* válido.

</dd> </dl>

## <a name="remarks"></a>Comentários

As seguintes restrições se aplicam aos protocolos de datagram, **ncadg \_ ipx** e [**ncadg \_ ip \_ udp**](ncadg-ip-udp.md):

-   Eles não são suportados retornos de chamada. Todas as funções que usam o **\[** [**atributo de retorno de**](callback.md) chamada **\]** falharão.
-   Eles não suportam o uso do [**construtor de tipo**](pipe.md) pipe.

Ao usar o **transporte \_ ipx ncadg,** o nome do servidor é exatamente o mesmo que o nome Windows servidor de 32 bits. No entanto, como os nomes são distribuídos usando protocolos Novell, eles devem estar em conformidade com as convenções de nomenu da Novell. Se um nome de servidor não for um nome Válido da Novell, os servidores não poderão criar pontos de extremidade com o **transporte \_ ipx ncadg.** Veja a seguir uma lista parcial de caracteres proibidos em nomes de servidor Novell:

" \* + . / : ; < = > ? \[ \] \\ \|

O **transporte \_ ipx ncadg** é suportado pela versão do NWLink fornecida com o MS Client 3.0.

Os aplicativos Windows cliente de 16 bits que usam o transporte **\_ ipx ncadg** exigem que o arquivo Nwipxspx.dll ser instalado para ser executado no subsistema WOW. Contate a Novell para obter esse arquivo.

Para obter os endereços de rede e de nó, use o utilitário **de verificação** da Novell ou o **IPXGetInternetAddress** da API definido pela Novell. No Windows, você também pode obter esses endereços com o **comando ipxroute config.**

A sintaxe da cadeia de caracteres de porta de transporte TCP/IP, como todas as cadeias de caracteres de porta, é definida independentemente da especificação de IDL. O compilador executa alguma verificação de sintaxe, mas não garante que a especificação do ponto de extremidade está correta. Alguns erros podem ser relatados em tempo de run em vez de em tempo de compilação.

> [!Note]  
> Não há suporte para essa família de protocolos no Windows XP.

 

## <a name="examples"></a>Exemplos

``` syntax
[
    uuid(12345678-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncadg_ipx:[1000]") 
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

[**ncacn \_ vns \_ spp**](ncacn-vns-spp.md)
</dt> <dt>

[**ncalrpc**](ncalrpc.md)
</dt> <dt>

[**ncadg \_ ip \_ udp**](ncadg-ip-udp.md)
</dt> <dt>

[associação de cadeia de caracteres](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 