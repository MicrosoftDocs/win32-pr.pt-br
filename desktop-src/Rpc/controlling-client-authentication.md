---
title: Controlando a autenticação do cliente
description: O melhor método para autenticar um cliente é instalar uma função de retorno de chamada de segurança usando a função RpcServerRegisterIf2 ou RpcServerRegisterIfEx; aceita uma função de retorno de chamada de segurança como um argumento.
ms.assetid: 3e858a71-9190-44a3-bc63-08cfbd02d443
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3508e99b351cd57fb67a3727710b60562ffe25dc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822562"
---
# <a name="controlling-client-authentication"></a>Controlando a autenticação do cliente

O melhor método para autenticar um cliente é instalar uma função de retorno de chamada de segurança usando a função [**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2) ou [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex) ; aceita uma função de retorno de chamada de segurança como um argumento. Quando a função de retorno de chamada de segurança for chamada, faça as verificações necessárias. Os atributos na conexão, identidade do chamador ou ambos, podem ser verificados. Para verificar os atributos de uma conexão, chame a função [**RpcServerInqCallAttributes**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcserverinqcallattributesa) ou [**RpcBindingInqAuthClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) . Isso permite a filtragem de clientes que não são autenticados, clientes que usam um provedor de segurança específico ou clientes que não usam proteção suficientemente forte (como privacidade).

Para permitir o acesso a um subconjunto de usuários autenticados, use [**RpcGetAuthorizationContextForClient**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcgetauthorizationcontextforclient). Essa função retorna um contexto de cliente AuthZ que pode ser usado para fazer verificações de acesso muito sofisticadas. Por exemplo, esse método pode ser usado para permitir o acesso somente ao presidentes em uma organização durante o horário comercial normal e ao CEO durante qualquer hora usando os serviços Active Directory para mapear um nome de usuário para seu título. O usuário pode ser representado e seu nome obtido. Depois que sua identidade for conhecida, quaisquer verificações desejadas poderão ser feitas.

 

 




