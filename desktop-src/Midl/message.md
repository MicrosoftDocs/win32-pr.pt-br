---
title: atributo de mensagem
description: O atributo \ Message \ indica que a chamada de procedimento remoto deve ser tratada como uma mensagem do cliente para o servidor.
ms.assetid: ec616bf5-a845-4e7e-9f39-20947d2074f7
keywords:
- MIDL de atributo de mensagem
topic_type:
- apiref
api_name:
- message
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 964f8dfd8652547bdf5bef25d1abe9acde8189a2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104454020"
---
# <a name="message-attribute"></a>atributo de mensagem

O atributo **\[ Message \]** indica que a chamada de procedimento remoto deve ser tratada como uma mensagem do cliente para o servidor.

``` syntax
[message, optional-attribute-list] void function-name(
    [in, optional-parameter-attributes] param-name,. . .);
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lista de atributos opcionais* 
</dt> <dd>

Outros atributos que se aplicam à função. Somente os **\[** atributos [**local**](local.md) **\]** , **\[** [**Nocode**](nocode.md) **\]** , **\[** [**Code**](code.md)**\]** e **\[** [**Optimize**](optimize.md) **\]** podem ser usados com o atributo **\[ Message \]** .

</dd> <dt>

*nome da função* 
</dt> <dd>

O nome da função, conforme definido no arquivo IDL.

</dd> <dt>

*atributos de parâmetro opcionais* 
</dt> <dd>

Zero ou mais atributos MIDL que serão aplicados ao parâmetro.

</dd> <dt>

*nome do parâmetro* 
</dt> <dd>

O nome do parâmetro, conforme definido no arquivo IDL.

</dd> </dl>

## <a name="remarks"></a>Comentários

Como mensagens do cliente, as chamadas de procedimento remoto com o atributo **\[ Message \]** são entregues ao servidor de forma assíncrona pelo transporte de enfileiramento de mensagens do [**ncadg \_ MQ**](ncadg-mq.md) . Você pode indicar o sistema de mensagens de modo síncrono especificando o protocolo de transporte **ncadg \_ MQ** sem usar o atributo **\[ \] Message** .

Ao especificar o sistema de mensagens de modo assíncrono, o atributo **\[ Message \]** permite que o cliente faça a chamada de procedimento remoto e retorne imediatamente, mesmo quando o aplicativo do servidor não está respondendo. Se o servidor de destino não estiver disponível, a chamada será armazenada até que o servidor fique disponível.

Além disso, o sistema de mensagens em modo assíncrono permite controlar as propriedades da fila de recebimento do servidor. Consulte [**RpcBindingSetOption**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingsetoption) para obter mais informações sobre como selecionar a qualidade do serviço, a prioridade da chamada e o tempo de vida da chamada para o processo do servidor.

As restrições a seguir também se aplicam ao atributo **\[ Message \]** :

-   O enfileiramento de mensagens da Microsoft deve ser implementado nos sistemas cliente e servidor e os sistemas devem ser visíveis uns aos outros, conforme determinado pelo escopo da instalação da fila de mensagens.
-   A associação deve usar pontos de extremidade bem conhecidos e o protocolo de transporte [**ncadg \_ MQ**](ncadg-mq.md) .
-   A função não pode conter parâmetros de saída ou um tipo de retorno diferente de [**void**](void.md). Observe que a última restrição torna o atributo de **\[ mensagem \]** inadequado para métodos de interface com (Object), neste momento. A próxima versão do MIDL permitirá que as funções de **\[ mensagem \]** retornem o status de erro \_ \_ t ou HRESULT.
-   Qualquer interface que contenha pelo menos uma chamada de **\[ mensagem \]** deve ser registrada chamando [**RpcServerRegisterIf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterif) ou [**RpcServerRegisterIfEx**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterifex) antes [**de chamar RpcServerUseProtseqEpEx (ncadg \_ MQ)**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseprotseqepex). Caso contrário, as chamadas que estavam aguardando na fila para o servidor serão lidas antes da interface ser registrada e as chamadas falharão.

## <a name="examples"></a>Exemplos

``` syntax
[message] void DisplayString(
    [in, string] char * p1);
 
[message] void VarDataArray(
    [in, size_is(iSize)] ARRAY_TYPE lpMyArray,
    [in] int iSize,
    [in] unsigned long ulChksum);
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[**auto-completar**](code.md)
</dt> <dt>

[**local**](local.md)
</dt> <dt>

[**ncadg \_ MQ**](ncadg-mq.md)
</dt> <dt>

[**Nocode**](nocode.md)
</dt> <dt>

[**formato**](optimize.md)
</dt> <dt>

[Enfileiramento de mensagens RPC](/windows/desktop/Rpc/rpc-message-queuing)
</dt> <dt>

[**RpcBindingSetOption**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingsetoption)
</dt> <dt>

[**RpcBindingInqOption**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindinginqoption)
</dt> <dt>

[**void**](void.md)
</dt> </dl>

 

 