---
title: Controlando a autenticação do cliente
description: O melhor método para autenticar um cliente é instalar uma função de retorno de chamada de segurança usando a função RpcServerRegisterIf2 ou RpcServerRegisterIfEx; aceita uma função de retorno de chamada de segurança como um argumento.
ms.assetid: 3e858a71-9190-44a3-bc63-08cfbd02d443
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb00a03740d99b137f97b085525e4c7232483dc15db487daf486ad51560b4427
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118931233"
---
# <a name="controlling-client-authentication"></a>Controlando a autenticação do cliente

O melhor método para autenticar um cliente é instalar uma função de retorno de chamada de segurança usando a [**função RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2) ou [**RpcServerRegisterIfEx;**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex) aceita uma função de retorno de chamada de segurança como um argumento. Quando a função de retorno de chamada de segurança for chamada, faça as verificações necessárias. Os atributos na conexão, a identidade do chamador ou ambos podem ser verificados. Para verificar os atributos de uma conexão, chame a [**função RpcServerInqCallAttributes**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcserverinqcallattributesa) [**ou RpcBindingInqAuthClient.**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) Isso permite a filtragem de clientes que não são autenticados, clientes que usam um provedor de segurança específico ou clientes que não usam proteção forte o suficiente (como privacidade).

Para permitir o acesso a um subconjunto dos usuários autenticados, use [**RpcGetAuthorizationContextForClient**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcgetauthorizationcontextforclient). Essa função retorna um contexto de cliente Authz que pode ser usado para fazer verificações de acesso muito sofisticadas. Por exemplo, esse método pode ser usado para permitir o acesso somente aos vice-presidentes em uma organização durante o horário comercial normal e ao CEO durante qualquer hora usando os serviços do Active Directory para mapear um nome de usuário para seu título. O usuário pode ser personificado e seu nome é obtido. Depois que sua identidade for conhecida, todas as verificações desejadas poderão ser feitas.

 

 




