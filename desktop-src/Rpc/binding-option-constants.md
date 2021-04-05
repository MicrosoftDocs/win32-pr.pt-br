---
title: Constantes de opção de associação (rpcdce. h)
description: Os aplicativos definem as constantes de opção de associação para controlar como a biblioteca de tempo de execução RPC processa chamadas de procedimento remotas. A tabela a seguir lista cada propriedade de associação e os valores constantes relevantes para as propriedades de associação.
ms.assetid: ff88e05d-b9f3-42ef-a44f-fee9261832c8
topic_type:
- apiref
api_name:
- RPC_C_OPT_BINDING_NONCAUSAL
- RPC_C_OPT_MAX_OPTIONS
- RPC_C_DONT_FAIL
- RPC_C_OPT_SESSION_ID
- RPC_C_OPT_COOKIE_AUTH
- RPC_C_OPT_RESOURCE_TYPE_UUID
- RPC_C_OPT_DONT_LINGER
- RPC_C_OPT_UNIQUE_BINDING
api_location:
- Rpcdce.h
- Rpcdcep.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52152b5ddcc17abe5c698697e30f1f1a512ee4f8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918225"
---
# <a name="binding-option-constants"></a>Constantes de opção de associação

Os aplicativos definem as constantes de opção de associação para controlar como a biblioteca de tempo de execução RPC processa chamadas de procedimento remotas. A tabela a seguir lista cada propriedade de associação e os valores constantes relevantes para as propriedades de associação.

> [!Note]  
> Todas as opções de fila de mensagens (MQ) na tabela a seguir são válidas somente para o Windows 2000. O Windows XP e versões posteriores não oferecem suporte ao enfileiramento de mensagens. Os desenvolvedores não são incentivados a usar o enfileiramento de mensagens.

 



| Constante/valor                                                                                                                                                                                                                                                        | Descrição                                                                                                                                                                                                                                                                                           |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RPC_C_OPT_BINDING_NONCAUSAL"></span><span id="rpc_c_opt_binding_noncausal"></span><dl> <dt>**RPC \_ C \_ \_ BIND Binding \_ NONCAUSAL**</dt> <dt>9</dt> </dl>     | Padrão. Se **for false**, causal chamar ordenação. As chamadas RPC são executadas em ordem estrita de envio. Consulte Observações.<br/> Se **for true**, noncausal chamar ordenação. As chamadas RPC são executadas de forma independente. Consulte Observações.<br/>                                                                        |
| <span id="RPC_C_OPT_MAX_OPTIONS"></span><span id="rpc_c_opt_max_options"></span><dl> <dt>**RPC \_ \_ \_ \_ Opções C opt Max**</dt> <dt>17</dt> </dl>                      | Não é necessário para programas de aplicativo. Usado internamente pela Microsoft.<br/>                                                                                                                                                                                                                         |
| <span id="RPC_C_DONT_FAIL"></span><span id="rpc_c_dont_fail"></span><dl> <dt>**RPC \_ C \_ \_ falha**</dt> em <dt>4</dt> </dl>                                          | Não é necessário para programas de aplicativo. Usado internamente pela Microsoft.<br/>                                                                                                                                                                                                                         |
| <span id="RPC_C_OPT_SESSION_ID"></span><span id="rpc_c_opt_session_id"></span><dl> <dt>**RPC \_ \_ID da \_ sessão \_ de aceitação de C**</dt> <dt>6</dt> </dl>                          | Se **for true**, uma ID de sessão será gerada para cada conexão.<br/>                                                                                                                                                                                                                                |
| <span id="RPC_C_OPT_COOKIE_AUTH"></span><span id="rpc_c_opt_cookie_auth"></span><dl> <dt>**RPC \_ \_Autenticação de \_ Cookie \_ b de consentimento**</dt> <dt>7</dt> </dl>                       | Se **for true**, a autenticação baseada em cookie do lado do cliente será usada para conexões. Um ponteiro para a estrutura do [**\_ \_ \_ \_ \_ descritor de autenticação do cookie de consentimento RPC C**](/windows/desktop/api/Rpcdcep/ns-rpcdcep-rpc_c_opt_cookie_auth_descriptor) é passado como o parâmetro *optionvalue* em [**RpcBindingSetOption**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetoption).<br/> |
| <span id="RPC_C_OPT_RESOURCE_TYPE_UUID"></span><span id="rpc_c_opt_resource_type_uuid"></span><dl> <dt>**RPC \_ \_UUID de \_ \_ tipo \_ de recurso de C opt**</dt> <dt>8</dt> </dl> | Não é necessário para programas de aplicativo. Usado internamente pela Microsoft.<br/>                                                                                                                                                                                                                         |
| <span id="RPC_C_OPT_DONT_LINGER"></span><span id="rpc_c_opt_dont_linger"></span><dl> <dt>**RPC \_ C \_ aceitar \_ não \_ remanescente**</dt> <dt>13</dt> </dl>                      | Se **for true**, forçará o desligamento da Associação depois que o último identificador de associação/identificador de contexto for liberado.<br/>                                                                                                                                                                                |
| <span id="RPC_C_OPT_UNIQUE_BINDING"></span><span id="rpc_c_opt_unique_binding"></span><dl> <dt>**RPC \_ C \_ aceitar \_ \_ associação exclusiva**</dt> <dt>11</dt> </dl>             | Quando definido como **true**, o RPC não reutiliza as conexões existentes. Um identificador de associação exclusivo é aberto para cada conexão e o estado é mantido para cada identificador de associação exclusivo.<br/>                                                                                                               |



## <a name="remarks"></a>Comentários

Por padrão, a biblioteca de tempo de execução RPC executa as chamadas em um determinado identificador de ligação de cada thread de um aplicativo em ordem estrita de envio. Isso não garante que as chamadas de threads diferentes no mesmo identificador de ligação sejam serializadas. Os aplicativos multissegmentados devem serializar suas chamadas RPC. Se esse comportamento for muito restritivo, você poderá habilitar a ordenação noncausal. Quando você faz isso, a biblioteca de tempo de execução RPC executa chamadas de forma independente. Ele impõe nenhuma ordem no envio.

Um exemplo de um aplicativo que pode encontrar a ordenação de noncausal útil é um programa multithread cujos threads fazem chamadas no mesmo identificador de ligação. Da mesma forma, um programa que usa várias chamadas assíncronas em um identificador de ligação encontrará noncausal a ordenação de uma opção conveniente. Outro exemplo pode ser um programa de proxy da Internet que usa um único thread para lidar com solicitações para vários clientes. Em cada um desses casos, seria extremamente restritivo tentar serializar as chamadas de procedimento remoto.

A opção **RPC \_ C opt não \_ \_ \_ persistente** pode ser definida somente em identificadores de associação que usam as sequências de protocolo **Ncalrpc** ou **ncacn \_ \** _. Ele não pode ser usado em sequências de protocolo _*ncadg \_ \**_ . A função [_ *RpcBindingSetOption* *](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetoption) com essa opção deve ser chamada em um identificador de associação no qual pelo menos uma chamada RPC foi feita. Se nenhuma chamada RPC tiver sido feita no identificador de associação, **o \_ \_ \_ tipo \_ de \_ Associação RPC S incorreto** será retornado da chamada de função **RpcBindingSetOption** . A opção entra em vigor para toda a associação, independentemente de quantos identificadores de associação são anexados à associação. Como ela é verificada antes de a associação ser destruída, ela pode ser definida a qualquer momento antes que o identificador de associação seja fechado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                                                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                                                                 |
| Cabeçalho<br/>                   | <dl> <dt>Rpcdce. h; </dt> <dt>Rpcdcep. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**RpcBindingSetOption**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetoption)
</dt> <dt>

[**RpcBindingInqOption**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqoption)
</dt> <dt>

[Gerenciando conjuntos de conexões de rede (associações)](managing-network-connection-sets-associations-.md)
</dt> </dl>

 

 





