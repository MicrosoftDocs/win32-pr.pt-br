---
title: Constantes de opção de associação (Rpcdce.h)
description: Os aplicativos configuram as constantes de opção de associação para controlar como a biblioteca em tempo de executar RPC processa chamadas de procedimento remoto. A tabela a seguir lista cada propriedade de associação e os valores constantes relevantes para as propriedades de associação.
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
ms.openlocfilehash: 147d36cf66bb3a45add61b8639ccd3fada31856e72fce8c1f96d7a021e1d5e95
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120023116"
---
# <a name="binding-option-constants"></a>Constantes de opção de associação

Os aplicativos configuram as constantes de opção de associação para controlar como a biblioteca em tempo de executar RPC processa chamadas de procedimento remoto. A tabela a seguir lista cada propriedade de associação e os valores constantes relevantes para as propriedades de associação.

> [!Note]  
> Todas as opções de fila de mensagens (MQ) na tabela a seguir são válidas somente Windows 2000. Windows O XP e as versões posteriores não são suportados com en ensuamento de mensagens. Os desenvolvedores não são desencorajados a usar o enxuamento de mensagens.

 



| Constante/valor                                                                                                                                                                                                                                                        | Descrição                                                                                                                                                                                                                                                                                           |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RPC_C_OPT_BINDING_NONCAUSAL"></span><span id="rpc_c_opt_binding_noncausal"></span><dl> <dt>**RPC \_ C \_ OPT \_ BINDING \_ NONCAUSAL**</dt> <dt>9</dt> </dl>     | Padrão. Se **FALSE**, ordenação de chamada causal. Chamadas RPC são executadas em ordem estrita de envio. Consulte Observações.<br/> Se **TRUE,** ordenação de chamada não truncada. As chamadas RPC são executadas independentemente. Consulte Observações.<br/>                                                                        |
| <span id="RPC_C_OPT_MAX_OPTIONS"></span><span id="rpc_c_opt_max_options"></span><dl> <dt>**RPC \_ C \_ OPT \_ MAX \_ OPTIONS**</dt> <dt>17</dt> </dl>                      | Não é necessário para programas de aplicativo. Usado internamente pela Microsoft.<br/>                                                                                                                                                                                                                         |
| <span id="RPC_C_DONT_FAIL"></span><span id="rpc_c_dont_fail"></span><dl> <dt>**RPC \_ C \_ DONT \_ FAIL**</dt> <dt>4</dt> </dl>                                          | Não é necessário para programas de aplicativo. Usado internamente pela Microsoft.<br/>                                                                                                                                                                                                                         |
| <span id="RPC_C_OPT_SESSION_ID"></span><span id="rpc_c_opt_session_id"></span><dl> <dt>**RPC \_ C \_ OPT \_ SESSION \_ ID**</dt> <dt>6</dt> </dl>                          | Se **TRUE**, uma ID de sessão será gerada para cada conexão.<br/>                                                                                                                                                                                                                                |
| <span id="RPC_C_OPT_COOKIE_AUTH"></span><span id="rpc_c_opt_cookie_auth"></span><dl> <dt>**RPC \_ C \_ OPT \_ COOKIE \_ AUTH**</dt> <dt>7</dt> </dl>                       | Se **TRUE**, a autenticação baseada em cookie do lado do cliente será usada para conexões. Um ponteiro para a estrutura [**\_ RPC C \_ OPT COOKIE \_ \_ AUTH \_ DESCRIPTOR**](/windows/desktop/api/Rpcdcep/ns-rpcdcep-rpc_c_opt_cookie_auth_descriptor) é passado como o parâmetro *OptionValue* em [**RpcBindingSetOption**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetoption).<br/> |
| <span id="RPC_C_OPT_RESOURCE_TYPE_UUID"></span><span id="rpc_c_opt_resource_type_uuid"></span><dl> <dt>**RPC \_ C \_ OPT RESOURCE TYPE \_ \_ \_ UUID**</dt> <dt>8</dt> </dl> | Não é necessário para programas de aplicativo. Usado internamente pela Microsoft.<br/>                                                                                                                                                                                                                         |
| <span id="RPC_C_OPT_DONT_LINGER"></span><span id="rpc_c_opt_dont_linger"></span><dl> <dt>**RPC \_ C \_ OPT \_ DONT \_ LINGER**</dt> <dt>13</dt> </dl>                      | Se **TRUE**, force o desligamento da associação após a última alça de associação/o alça de contexto nele ser liberado.<br/>                                                                                                                                                                                |
| <span id="RPC_C_OPT_UNIQUE_BINDING"></span><span id="rpc_c_opt_unique_binding"></span><dl> <dt>**RPC \_ C \_ OPT \_ UNIQUE \_ BINDING**</dt> <dt>11</dt> </dl>             | Quando definido como **true,** o RPC não reutiliza as conexões existentes. Um alça de associação exclusivo é aberto para cada conexão e o estado é mantido para cada alça de associação exclusiva.<br/>                                                                                                               |



## <a name="remarks"></a>Comentários

Por padrão, a biblioteca em tempo de execução RPC executa as chamadas em um determinado alça de associação de cada thread de um aplicativo em ordem estrita de envio. Isso não garante que chamadas de threads diferentes no mesmo alça de associação sejam serializadas. Aplicativos multithread devem serializar suas chamadas RPC. Se esse comportamento for muito restritivo, você poderá habilitar a ordenação nãoncausal. Quando você faz isso, a biblioteca em tempo de execução RPC executa chamadas independentemente. Ele não impõe nenhuma ordenação em seu envio.

Um exemplo de um aplicativo que pode achar a ordenação não tncausal útil é um programa multithread cujos threads fazem chamadas no mesmo alça de associação. Da mesma forma, um programa que usa várias chamadas assíncronas em um alçamento de associação encontrará uma opção conveniente de ordenação não tínusal. Outro exemplo pode ser um programa de proxy da Internet que usa um único thread para lidar com solicitações para vários clientes. Em cada um desses casos, seria extremamente restritivo tentar serializar as chamadas de procedimento remoto.

A **opção RPC \_ C OPT \_ \_ DONT \_ LINGER** pode ser definida somente em alças de associação que usam as sequências de protocolo **ncalrpc** ou **ncacn \_ \** _ . Ele não pode ser usado em sequências de protocolo _*ncadg. \_ \**_ A [função _ *RpcBindingSetOption* *](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetoption) com essa opção deve ser chamada em um alçamento de associação no qual pelo menos uma chamada RPC foi feita. Se nenhuma chamada RPC tiver sido feita no alçamento de associação, **RPC \_ S WRONG KIND OF \_ \_ \_ \_ BINDING** será retornado da chamada de função **RpcBindingSetOption.** A opção entra em vigor para toda a associação, independentemente de quantas alças de associação estão anexadas à associação. Como ele é verificado antes que a associação seja destruída, ela pode ser definida a qualquer momento antes que o alça de associação seja fechado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                                                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                                                                 |
| Cabeçalho<br/>                   | <dl> <dt>Rpcdce.h; </dt> <dt>Rpcdcep.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**RpcBindingSetOption**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetoption)
</dt> <dt>

[**RpcBindingInqOption**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqoption)
</dt> <dt>

[Gerenciando conjuntos de conexões de rede (associações)](managing-network-connection-sets-associations-.md)
</dt> </dl>

 

 





