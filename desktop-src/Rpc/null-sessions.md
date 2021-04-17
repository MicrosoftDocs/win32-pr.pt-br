---
title: Sessões nulas
description: Às vezes, uma chamada que chega na sessão nula pode aparecer como uma chamada autenticada.
ms.assetid: 5d113d20-c7af-4fb3-ba17-d0715671f290
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68fe0542d86dd2e6b903a08834293d6cc2f09828
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104453700"
---
# <a name="null-sessions"></a>Sessões nulas

Às vezes, uma chamada que chega na sessão nula pode aparecer como uma chamada autenticada. Especificamente, chamar a função [**RpcBindingInqAuthClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) retorna o nível de autenticação e o provedor de segurança usados para a chamada. Esta operação não significa que a chamada não estava em uma sessão nula. Os dois problemas são ortogonal. No Microsoft Windows 2000, uma chamada de procedimento remoto pode tentar representar um chamador e verificar as permissões após a representação. No Microsoft Windows XP, é mais rápido chamar a função [**RpcServerInqCallAttributes**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcserverinqcallattributesa) e verificar o sinalizador **NullSession** .

Existe outra diferença relevante entre o Windows 2000 e o Windows XP. Se apenas o \_ \_ \_ sinalizador permitir somente segurança \_ for especificado, as chamadas na sessão nula passarão pelo Windows 2000. No Windows XP, com o ajuste geral das configurações de segurança padrão, quando esse sinalizador é especificado, as chamadas na sessão nula são rejeitadas com acesso negado. No entanto, mesmo com o RPC \_ se \_ permitir \_ \_ sinalizador somente seguro, o RPC não garante o nível de privilégio do usuário que está chamando. Todas as verificações RPC são que o usuário tem credenciais válidas. É possível que o usuário que está chamando esteja usando a conta de convidado ou outras contas com poucos privilégios. Verifique se o servidor não assume alto privilégio depois de RPC \_ se \_ permitir \_ \_ somente seguro for usado.

 

 




