---
title: Sessões nulas
description: Às vezes, uma chamada que chega na sessão nula pode aparecer como uma chamada autenticada.
ms.assetid: 5d113d20-c7af-4fb3-ba17-d0715671f290
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5476a49513019fe15afa4a30beae08104533a6621a84c4e0d1de4e9f315275ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120019556"
---
# <a name="null-sessions"></a>Sessões nulas

Às vezes, uma chamada que chega na sessão nula pode aparecer como uma chamada autenticada. Especificamente, chamar a função [**RpcBindingInqAuthClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) retorna o nível de autenticação e o provedor de segurança usados para a chamada. Esta operação não significa que a chamada não estava em uma sessão nula. Os dois problemas são ortogonal. no Microsoft Windows 2000, uma chamada de procedimento remoto pode tentar representar um chamador e verificar as permissões após a representação. no Microsoft Windows XP, é mais rápido chamar a função [**RpcServerInqCallAttributes**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcserverinqcallattributesa) e verificar o sinalizador **NullSession** .

existe outra diferença relevante entre Windows 2000 e Windows XP. se apenas o \_ \_ \_ sinalizador permitir somente segurança \_ for especificado, as chamadas na sessão nula passarão pelo Windows 2000. no Windows XP, com o ajuste geral das configurações de segurança padrão, quando esse sinalizador é especificado, as chamadas na sessão nula são rejeitadas com acesso negado. No entanto, mesmo com o RPC \_ se \_ permitir \_ \_ sinalizador somente seguro, o RPC não garante o nível de privilégio do usuário que está chamando. Todas as verificações RPC são que o usuário tem credenciais válidas. É possível que o usuário que está chamando esteja usando a conta de convidado ou outras contas com poucos privilégios. Verifique se o servidor não assume alto privilégio depois de RPC \_ se \_ permitir \_ \_ somente seguro for usado.

 

 




