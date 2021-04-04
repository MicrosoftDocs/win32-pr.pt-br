---
title: Autenticação mútua em aplicativos RPC
description: Os serviços RPC podem usar pontos de conexão de serviço para publicar por conta própria ou podem usar as APIs do serviço de nomes RPC (RpcNs).
ms.assetid: 9f575aef-0a4b-4e1b-8ea9-5f40e6c3d9c7
ms.tgt_platform: multiple
keywords:
- Autenticação mútua no AD de aplicativos RPC
- Active Directory, usando, autenticação mútua, RPC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05a8591056293c916205b5b600c1b1a061d169f0
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "103823647"
---
# <a name="mutual-authentication-in-rpc-applications"></a>Autenticação mútua em aplicativos RPC

Os serviços RPC podem usar pontos de conexão de serviço para publicar por conta própria ou podem usar as APIs do serviço de nomes RPC (RpcNs). Este tópico discute como executar a autenticação mútua com um serviço RPC que se publica usando as APIs do serviço de nomes RPC (RpcNs).

**Para registrar um SPN no diretório**

1.  Chame a função [**DsGetSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna) para compor um SPN (nome da entidade de serviço) para o serviço.
2.  Chame a função [**DsWriteAccountSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna) para registrar o SPN na conta de serviço ou conta de computador em cujo contexto o serviço será executado.

**Para registrar um serviço com o serviço de cadastramento de RPC**

1.  Verifique se os SPNs apropriados estão registrados na conta sob a qual o serviço está sendo executado. Para obter mais informações, consulte [tarefas de manutenção de conta de logon](logon-account-maintenance-tasks.md).
2.  Chame a função [**RpcServerRegisterAuthInfo**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterauthinfo) para registrar o SPN de serviço com o serviço de autenticação RPC e especifique o **RPC \_ C \_ Authn \_ GSS \_ Negotiate** como o serviço de autenticação a ser usado.

Para obter mais informações sobre como executar a autenticação mútua em um serviço RPC, consulte [escrevendo um servidor SSPI autenticado](/windows/desktop/Rpc/writing-an-authenticated-sspi-server).

**Para autenticar o serviço do cliente**

1.  Extraia o nome do host da Associação RPC.
2.  Redija o SPN para o serviço chamando a função [**DsMakeSpn**](/windows/desktop/api/Dsparse/nf-dsparse-dsmakespna) com a classe de serviço, o nome do host DNS e o nome do serviço; Esse é o nome distinto do ponto de conexão no caso de RpcNs.

    Para obter mais informações sobre como compor um SPN para um serviço de RpcNs, consulte [composição de SPNs para um serviço de RpcNs](composing-spns-for-an-rpcns-service.md).

3.  Configure uma estrutura [**de \_ \_ QoS de segurança RPC**](/windows/desktop/api/rpcdce/ns-rpcdce-rpc_security_qos) para solicitar autenticação mútua.
4.  Chame a função [**RpcBindingSetAuthInfoEx**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa) para definir os dados de autenticação para a associação RPC. O cliente deve solicitar pelo menos **a \_ \_ integridade de \_ pkt do \_ nível \_ de autenticação RPC C** para garantir que as comunicações não tenham sido adulteradas. Para aumentar a segurança, o cliente deve especificar a **privacidade do PCT do \_ nível de \_ autenticação \_ \_ \_ RPC C** para solicitar a criptografia.
5.  Execute a chamada RPC.

Para obter mais informações sobre como executar a autenticação mútua em um cliente RPC, consulte [escrevendo um cliente SSPI autenticado](/windows/desktop/Rpc/writing-an-authenticated-sspi-client).

**Para autenticar o cliente do serviço**

1.  Chame a função [**RpcBindingInqAuthClient**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindinginqauthclient) para verificar os parâmetros de autenticação especificados pelo cliente. Se o cliente não tiver solicitado o nível de autenticação desejado, rejeite a chamada. Lembre-se de que um serviço RPC deve verificar o nível de autenticação, o serviço de autenticação e a identidade do cliente em cada chamada para garantir que o cliente tenha sido autenticado corretamente.
2.  Chame a função [**RpcImpersonateClient**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcimpersonateclient) para representar o cliente.
3.  Execute a operação solicitada.
4.  Chame a função [**RpcRevertToSelf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcreverttoself) para reverter para o contexto de segurança do serviço.

Para obter mais informações sobre a representação do cliente RPC, consulte [representação do cliente](/windows/desktop/Rpc/client-impersonation).

Para obter mais informações, consulte:

-   [Publicando com o serviço de nomes RPC (RpcNs)](publishing-with-the-rpc-name-service-rpcns.md)
-   [Noções básicas de segurança RPC](/windows/desktop/Rpc/rpc-security-essentials)

 

 