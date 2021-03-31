---
title: atributo de ponto de extremidade
description: O atributo \ Endpoint \ especifica uma porta conhecida ou portas (pontos de extremidade de comunicação) nos quais os servidores da interface escutam chamadas.
ms.assetid: b88c5a97-b726-43de-b5b6-649cda60c320
keywords:
- MIDL do atributo de ponto de extremidade
topic_type:
- apiref
api_name:
- endpoint
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4383df496a791859f7249766f0dbb59266d28e93
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103823688"
---
# <a name="endpoint-attribute"></a>atributo de ponto de extremidade

O atributo **\[ Endpoint \]** especifica uma porta ou portas conhecidas (pontos de extremidade de comunicação) nos quais os servidores da interface escutam chamadas.

``` syntax
endpoint("protocol-sequence:[endpoint-port]" [ , ...] )
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*sequência de protocolos* 
</dt> <dd>

Especifica uma cadeia de caracteres que representa uma combinação válida de um protocolo RPC (como "ncacn"), um protocolo de transporte (como "TCP") e um protocolo de rede (como "IP"). Para obter uma lista de sequências de protocolo válidas, consulte [constantes de sequência de protocolo](/windows/desktop/Rpc/protocol-sequence-constants).

</dd> <dt>

*ponto de extremidade-porta* 
</dt> <dd>

Especifica uma cadeia de caracteres que representa a designação do ponto de extremidade para a família de protocolos especificada. A sintaxe da cadeia de caracteres de porta é específica para cada sequência de protocolo.

</dd> </dl>

## <a name="remarks"></a>Comentários

O atributo **\[ Endpoint \]** especifica uma família de transporte, como o protocolo orientado a conexões TCP/IP, um protocolo orientado a conexões NetBIOS ou o protocolo orientado a conexão de pipe nomeado. O uso do atributo de **\[ ponto de extremidade \]** é consistente com outros métodos para adicionar um ponto de extremidade e não fornece serviços adicionais ou especiais para o ponto de extremidade; ele simplesmente fornece um atalho para chamar a API.

> [!Note]  
> Especificar um ponto de extremidade no. A definição da interface IDL não restringe o acesso à interface para o ponto de extremidade especificado. Adicionando um ponto de extremidade ao. A definição de interface IDL permite que a interface seja chamada por meio de qualquer ponto de extremidade nesse processo e permite que o ponto de extremidade seja usado para chamar outras interfaces nesse processo.

 

O valor de *sequência de protocolo* determina os valores válidos para a porta do *ponto de extremidade*. O compilador MIDL verifica apenas a sintaxe geral para a entrada de *porta do ponto de extremidade* . Os erros de especificação de porta são relatados pelas bibliotecas de tempo de execução. Para obter informações sobre os valores permitidos para cada sequência de protocolo, consulte as [constantes de sequência de protocolo](/windows/desktop/Rpc/protocol-sequence-constants).

As seguintes sequências de protocolo especificadas pelo DCE não são suportadas pelo compilador MIDL fornecido com o Microsoft RPC: **ncacn \_ OSI \_ DNA** e **ncadg \_ DDS**.

Certifique-se de ter digitado corretamente caracteres de barra invertida em pontos de extremidade. Esse erro geralmente ocorre quando o ponto de extremidade é um pipe nomeado.

As informações de ponto de extremidade especificadas no arquivo IDL são usadas pelas funções de tempo de execução RPC [**RpcServerUseProtseqIf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseprotseqif) e [**RpcServerUseAllProtseqsIf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseallprotseqsif).

## <a name="examples"></a>Exemplos

``` syntax
endpoint("ncacn_np:[\\pipe\\rainier]") 

endpoint("ncacn_ip_tcp:[1044]", "ncacn_np:[\\pipe\\shasta]")
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[Arquivo de definição de interface (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**RpcServerUseAllProtseqsIf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseallprotseqsif)
</dt> <dt>

[**RpcServerUseProtseqIf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseprotseqif)
</dt> </dl>

 

 