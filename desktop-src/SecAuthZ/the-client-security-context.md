---
description: Como todos os processos, um servidor protegido tem um token de acesso primário que descreve seu contexto de segurança.
ms.assetid: 4e6393b2-4a71-49e4-b1e7-f34bf317d60d
title: O contexto do Client Security
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb3d3b4522aa90ade89e2130742346956a396f15
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921044"
---
# <a name="the-client-security-context"></a>O contexto do Client Security

Como todos os [*processos*](/windows/desktop/SecGloss/p-gly), um servidor protegido tem um [*token de acesso primário*](/windows/desktop/SecGloss/p-gly) que descreve seu [*contexto de segurança*](/windows/desktop/SecGloss/s-gly). Quando um cliente se conecta a um servidor protegido, o servidor pode querer executar ações usando o contexto de segurança do cliente em vez do contexto de segurança do servidor. Por exemplo, quando um cliente em uma conversa do intercâmbio de dados dinâmicos (DDE) solicita informações de um servidor DDE, o servidor precisa verificar se o cliente tem permissão de acesso às informações.

Há duas maneiras que um servidor pode agir no contexto de segurança do cliente:

-   Um thread do processo do servidor pode representar o cliente. Nesse caso, o thread do servidor tem um token de [*acesso*](/windows/desktop/SecGloss/a-gly) de representação que identifica o cliente, os grupos do cliente e os [*privilégios*](/windows/desktop/SecGloss/p-gly)do cliente. Para obter mais informações, consulte [representação do cliente](client-impersonation.md).
-   O servidor pode obter as [*credenciais*](/windows/desktop/SecGloss/c-gly) do cliente e registrar o cliente no computador do servidor. Isso cria uma nova [*sessão*](/windows/desktop/SecGloss/s-gly) de logon e produz um token de acesso primário para o cliente. O servidor pode usar o token de acesso do cliente para representar o cliente ou para iniciar um novo processo que é executado no contexto de segurança do cliente. Para obter mais informações, consulte [sessões de logon do cliente](client-logon-sessions.md).

Na maioria dos casos, representar o cliente é suficiente. A representação permite que o servidor Verifique o acesso do cliente a objetos protegíveis, verifique os privilégios do cliente e gere entradas de trilha de auditoria que identifiquem o cliente. Normalmente, um servidor precisa iniciar uma sessão de logon do cliente somente se precisar usar o contexto de segurança do cliente para acessar os recursos da rede.

 

 
