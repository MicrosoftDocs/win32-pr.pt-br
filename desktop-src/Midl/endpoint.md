---
title: atributo de ponto de extremidade
description: O atributo \ endpoint\ especifica uma porta ou portas conhecidas (pontos de extremidade de comunicação) em que os servidores da interface escutam chamadas.
ms.assetid: b88c5a97-b726-43de-b5b6-649cda60c320
keywords:
- atributo de ponto de extremidade MIDL
topic_type:
- apiref
api_name:
- endpoint
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dea4951a407f09c1407c6e897938460d780e0429e888210e7e1ade392b5e94af
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119383176"
---
# <a name="endpoint-attribute"></a>atributo de ponto de extremidade

O **\[ atributo \] de ponto** de extremidade especifica uma porta ou portas conhecidas (pontos de extremidade de comunicação) em que os servidores da interface escutam chamadas.

``` syntax
endpoint("protocol-sequence:[endpoint-port]" [ , ...] )
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*sequência de protocolo* 
</dt> <dd>

Especifica uma cadeia de caracteres que representa uma combinação válida de um protocolo RPC (como "ncacn"), um protocolo de transporte (como "tcp") e um protocolo de rede (como "ip"). Para ver uma lista de sequências de protocolo válidas, consulte [Constantes de sequência de protocolo.](/windows/desktop/Rpc/protocol-sequence-constants)

</dd> <dt>

*endpoint-port* 
</dt> <dd>

Especifica uma cadeia de caracteres que representa a designação de ponto de extremidade para a família de protocolo especificada. A sintaxe da cadeia de caracteres de porta é específica de cada sequência de protocolo.

</dd> </dl>

## <a name="remarks"></a>Comentários

O atributo de ponto de extremidade especifica uma família de transporte, como o protocolo orientado a conexão TCP/IP, um protocolo orientado a conexão NetBIOS ou o protocolo orientado a conexão de pipe nomeado. **\[ \]** O uso do atributo **\[ de \]** ponto de extremidade é consistente com outros métodos para adicionar um ponto de extremidade e não fornece serviços adicionais ou especiais para o ponto de extremidade; ele simplesmente fornece um atalho para chamar a API.

> [!Note]  
> Especificando um ponto de extremidade no . A definição da interface IDL não restringe o acesso à interface ao ponto de extremidade especificado. Adicionando um ponto de extremidade ao . A definição da interface IDL permite que a interface seja chamada por meio de qualquer ponto de extremidade nesse processo e permite que o ponto de extremidade seja usado para chamar outras interfaces nesse processo.

 

O *valor de sequência de* protocolo determina os valores válidos para a porta de ponto de *extremidade*. O compilador MIDL verifica apenas a sintaxe geral para a *entrada de porta de ponto de* extremidade. Os erros de especificação de porta são relatados pelas bibliotecas em tempo de executar. Para obter informações sobre os valores permitidos para cada sequência de protocolo, consulte [Constantes de sequência de protocolo](/windows/desktop/Rpc/protocol-sequence-constants).

As seguintes sequências de protocolo especificadas pelo DCE não são suportadas pelo compilador MIDL fornecido com o Microsoft RPC: **ncacn \_ osi \_ dna** e **ncadg \_ dds**.

Certifique-se de que você cita corretamente caracteres de invertida nos pontos de extremidade. Esse erro geralmente ocorre quando o ponto de extremidade é um pipe nomeado.

As informações de ponto de extremidade especificadas no arquivo IDL são usadas pelas funções [**RpcServerUseProtseqIf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseprotseqif) e [**RpcServerUseAllProtseqsIf.**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseallprotseqsif)

## <a name="examples"></a>Exemplos

``` syntax
endpoint("ncacn_np:[\\pipe\\rainier]") 

endpoint("ncacn_ip_tcp:[1044]", "ncacn_np:[\\pipe\\shasta]")
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[Arquivo IDL (definição de interface)](interface-definition-idl-file.md)
</dt> <dt>

[**RpcServerUseAllProtseqsIf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseallprotseqsif)
</dt> <dt>

[**RpcServerUseProtseqIf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseprotseqif)
</dt> </dl>

 

 