---
title: Serviços de Segurança do MSMQ
description: Mensagens RPC síncronas podem usar qualquer um dos recursos de segurança disponíveis no tempo de executar RPC. Confira Segurança para obter mais detalhes.
ms.assetid: 0f4d45c4-7457-4449-8736-e141a95f6930
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f142d83c003f1293556786167222a4e9e88d3912786aa328319efa7fb0ea345d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120019646"
---
# <a name="msmq-security-services"></a>Serviços de Segurança do MSMQ

Mensagens RPC síncronas podem usar qualquer um dos recursos de segurança disponíveis no tempo de executar RPC. Confira [Segurança](security.md) para obter mais detalhes.

Chamadas de mensagem assíncronas \[ [](/windows/desktop/Midl/message) \] não podem usar a segurança RPC porque não há nenhum handshake entre o cliente e o servidor. Na verdade, o servidor pode nem estar em execução no momento da chamada. Para acessar os serviços de segurança fornecidos pelo MSMQ (Message Queuing Services), o aplicativo cliente deve chamar [**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) para controlar o nível de autenticação e privacidade de suas chamadas ao servidor.

O aplicativo de servidor pode chamar [**RpcBindingInqAuthClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) de dentro de uma chamada de procedimento remoto para determinar o nível de segurança para essa chamada. O mapeamento entre constantes de segurança RPC e segurança MSMQ é mostrado na tabela a seguir.



| Nível de segurança RPC                | Descrição                                                                                |
|-----------------------------------|--------------------------------------------------------------------------------------------|
| RPC \_ AUTHN \_ LEVEL \_ NONE           | A chamada não é autenticada ou criptografada.                                                |
| INTEGRIDADE \_ PKT NO NÍVEL \_ \_ DE RPC AUTHN \_ | A chamada é autenticada usando a segurança do MSMQ.                                             |
| RPC \_ AUTHN \_ LEVEL \_ PKT \_ PRIVACY   | A chamada é autenticada e criptografada conforme ela percorre entre a fila do cliente e do servidor. |



 

O servidor também pode forçar a autenticação e a criptografia de chamada chamando [**RpcServerUseProtseqEpEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqepex) e definindo os sinalizadores \_ RPC C \_ MQ \_ AUTHN \_ LEVEL \_ NONE, \_ RPC C \_ \_ MQ AUTHN \_ LEVEL PKT INTEGRITY e \_ \_ RPC C \_ \_ MQ \_ AUTHN \_ LEVEL \_ PKT PRIVACY flags \_ [**\_**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_policy) na estrutura RPC POLICY.

 

 