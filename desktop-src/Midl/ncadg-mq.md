---
title: ncadg_mq atributo
description: A \_ palavra-chave ncadg MQ identifica os serviços de enfileiramento de mensagens da Microsoft (MSMQ) como o protocolo de transporte para o ponto de extremidade. Esse protocolo está obsoleto e não deve ser usado em novos aplicativos.
ms.assetid: 7472fc47-c1f0-4578-8aef-b655505e0563
keywords:
- ncadg_mq do atributo MIDL
topic_type:
- apiref
api_name:
- ncadg_mq
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0164211a267760a533d8d164a76387dbbcfba8a0aad8e4ac6ecaf20ed770708a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067016"
---
# <a name="ncadg_mq-attribute"></a>\_atributo ncadg MQ

A palavra-chave **ncadg \_ MQ** identifica os serviços de enfileiramento de mensagens da Microsoft (MSMQ) como o protocolo de transporte para o ponto de extremidade. Esse protocolo está obsoleto e não deve ser usado em novos aplicativos.

``` syntax
endpoint("ncadg_mq:server-name")
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*nome do servidor* 
</dt> <dd>

Especifica o nome do servidor, ou host, computador. O nome é uma cadeia de caracteres e pode ser um nome de domínio totalmente qualificado.

</dd> </dl>

## <a name="remarks"></a>Comentários

Para usar o protocolo de transporte **ncadg \_ MQ** , os componentes do MSMQ devem ser totalmente instalados e os sistemas cliente e servidor devem estar acessíveis por meio dos protocolos do MQ.

O **protocolo \_ MQ ncadg** não dá suporte a pontos de extremidade dinâmicos ou chamadas de [**difusão**](broadcast.md) . Assim como ocorre com outros protocolos de datagrama, o **ncadg \_ MQ** não oferece suporte a retornos de chamada. qualquer função que use o atributo de [**retorno de chamada**](callback.md) falhará

> [!Note]  
> Não há suporte para essa família de protocolos no WindowsÂ XP.

 

## <a name="examples"></a>Exemplos

A sintaxe do protocolo de fila de mensagens é definida independentemente da especificação de IDL. O compilador MIDL executa alguma verificação de sintaxe, mas não garante que a especificação do ponto de extremidade esteja correta. Alguns erros podem ser relatados em tempo de execução em vez de durante a compilação.

``` syntax
[
    uuid(12345678-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncadg_mq:rainier") 
]
interface iface
{
    // Interface definition statements.
}
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[**difusor**](broadcast.md)
</dt> <dt>

[**retorno de chamada**](callback.md)
</dt> <dt>

[**extremidade**](endpoint.md)
</dt> <dt>

[Arquivo de definição de interface (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**Mensagem**](message.md)
</dt> <dt>

[Enfileiramento de mensagens RPC](/windows/desktop/Rpc/rpc-message-queuing)
</dt> <dt>

[Associação de cadeia de caracteres](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 