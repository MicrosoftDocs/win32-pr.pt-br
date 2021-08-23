---
description: Cada serviço é executado no contexto de segurança de uma conta de usuário.
ms.assetid: a0e48918-6957-4288-a188-d65198b38c16
title: Contas de usuário de serviço
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6053a4f870b2a49923d802f7cb5f2a45b786d63314d1010773c3e8f58627bec2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118888543"
---
# <a name="service-user-accounts"></a>Contas de usuário de serviço

Cada serviço é executado no contexto de segurança de uma conta de usuário. O nome de usuário e a senha de uma conta são especificados pela [**função CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) no momento em que o serviço é instalado. O nome de usuário e a senha podem ser alterados usando a [**função ChangeServiceConfig.**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) Você pode usar a [**função QueryServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfiga) para obter o nome de usuário (mas não a senha) associado a um objeto de serviço. O SCM (gerenciador de controle de serviço) carrega automaticamente o perfil do usuário.

Ao iniciar um serviço, o SCM faz o login na conta associada ao serviço. Se o logoff for bem-sucedido, o sistema produzirá um token de acesso e o anexa ao novo processo de serviço. Esse token identifica o processo de serviço em todas as interações subsequentes com objetos de segurança (objetos que têm um descritor de segurança associado a eles). Por exemplo, se o serviço tentar abrir um handle para um pipe, o sistema comparará o token de acesso do serviço com o descritor de segurança do pipe antes de conceder acesso.

O SCM não mantém as senhas das contas de usuário do serviço. Se uma senha tiver expirado, o logon falhará e o serviço falhará ao iniciar. O administrador do sistema que atribui contas aos serviços pode criar contas com senhas que nunca expiram. O administrador também pode gerenciar contas com senhas que expiram usando um programa de configuração [de](service-configuration-programs.md) serviço para alterar periodicamente as senhas.

Se um serviço precisar reconhecer outro serviço antes de compartilhar suas informações, o segundo serviço poderá usar a mesma conta que o primeiro serviço ou pode ser executado em uma conta que pertence a um alias reconhecido pelo primeiro serviço. Os serviços que precisam ser executados de maneira distribuída pela rede devem ser executados em contas de todo o domínio.

Você pode especificar uma das seguintes contas especiais em vez de especificar uma conta de usuário para o serviço:

-   [LocalService](localservice-account.md)
-   [NetworkService](networkservice-account.md)
-   [LocalSystem](localsystem-account.md)

 

 



