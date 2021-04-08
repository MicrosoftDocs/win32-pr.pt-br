---
description: Cada serviço é executado no contexto de segurança de uma conta de usuário.
ms.assetid: a0e48918-6957-4288-a188-d65198b38c16
title: Contas de usuário de serviço
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54c72f332b8eddbc5b5929718b6688f75e226e59
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103836969"
---
# <a name="service-user-accounts"></a>Contas de usuário de serviço

Cada serviço é executado no contexto de segurança de uma conta de usuário. O nome de usuário e a senha de uma conta são especificados pela função [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) no momento em que o serviço é instalado. O nome de usuário e a senha podem ser alterados usando a função [**ChangeServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) . Você pode usar a função [**QueryServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfiga) para obter o nome de usuário (mas não a senha) associado a um objeto de serviço. O SCM (Gerenciador de controle de serviço) carrega automaticamente o perfil do usuário.

Ao iniciar um serviço, o SCM faz logon na conta associada ao serviço. Se o logon for bem-sucedido, o sistema produzirá um token de acesso e o anexará ao novo processo de serviço. Esse token identifica o processo de serviço em todas as interações subsequentes com objetos protegíveis (objetos que têm um descritor de segurança associado a eles). Por exemplo, se o serviço tentar abrir um identificador para um pipe, o sistema compara o token de acesso do serviço com o descritor de segurança do pipe antes de conceder acesso.

O SCM não mantém as senhas das contas de usuário de serviço. Se uma senha estiver expirada, o logon falhará e o serviço não será iniciado. O administrador do sistema que atribui contas aos serviços pode criar contas com senhas que nunca expiram. O administrador também pode gerenciar contas com senhas que expiram usando um [programa de configuração de serviço](service-configuration-programs.md) para alterar periodicamente as senhas.

Se um serviço precisar reconhecer outro serviço antes de compartilhar suas informações, o segundo serviço poderá usar a mesma conta que o primeiro serviço ou pode ser executado em uma conta que pertence a um alias que é reconhecido pelo primeiro serviço. Os serviços que precisam ser executados de maneira distribuída pela rede devem ser executados em contas de todo o domínio.

Você pode especificar uma das seguintes contas especiais em vez de especificar uma conta de usuário para o serviço:

-   [LocalService](localservice-account.md)
-   [NetworkService](networkservice-account.md)
-   [LocalSystem](localsystem-account.md)

 

 



