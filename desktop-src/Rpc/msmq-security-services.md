---
title: Serviços de segurança MSMQ
description: As mensagens RPC síncronas podem usar qualquer um dos recursos de segurança disponíveis no tempo de execução RPC. Consulte segurança para obter mais detalhes.
ms.assetid: 0f4d45c4-7457-4449-8736-e141a95f6930
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffd2e12cd9f32a571088de769adb079327caab9b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084716"
---
# <a name="msmq-security-services"></a>Serviços de segurança MSMQ

As mensagens RPC síncronas podem usar qualquer um dos recursos de segurança disponíveis no tempo de execução RPC. Consulte [segurança](security.md) para obter mais detalhes.

Chamadas de mensagens assíncronas \[ [](/windows/desktop/Midl/message) \] não podem usar a segurança RPC porque não há handshake entre cliente e servidor. Na verdade, o servidor pode nem mesmo estar em execução no momento da chamada. Para acessar os serviços de segurança fornecidos pelo MSMQ (serviços de enfileiramento de mensagens), o aplicativo cliente deve chamar [**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) para controlar o nível de autenticação e privacidade de suas chamadas para o servidor.

O aplicativo de servidor pode chamar [**RpcBindingInqAuthClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) de dentro de uma chamada de procedimento remoto para determinar o nível de segurança para essa chamada. O mapeamento entre as constantes de segurança RPC e a segurança do MSMQ é mostrado na tabela a seguir.



| Nível de segurança RPC                | Descrição                                                                                |
|-----------------------------------|--------------------------------------------------------------------------------------------|
| \_ \_ nenhum nível de autenticação \_ RPC           | A chamada não é autenticada ou criptografada.                                                |
| \_integridade de pkt do nível de autenticação RPC \_ \_ \_ | A chamada é autenticada usando a segurança do MSMQ.                                             |
| \_privacidade do PCT no nível de autenticação RPC \_ \_ \_   | A chamada é autenticada e criptografada à medida que ela viaja entre a fila do cliente e do servidor. |



 

O servidor também pode forçar a chamada de autenticação e criptografia chamando [**RpcServerUseProtseqEpEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqepex) e Configurando o RPC \_ c \_ MQ \_ authtemplate \_ nível \_ None, RPC \_ c \_ MQ \_ Authn \_ nível de autenticação do \_ PCT \_ e \_ sinalizadores de privacidade de \_ \_ \_ \_ pkt do MQ \_ de [**\_**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_policy) RPC c.

 

 