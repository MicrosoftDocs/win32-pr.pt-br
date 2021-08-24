---
description: Como todos os processos, um servidor protegido tem um token de acesso primário que descreve seu contexto de segurança.
ms.assetid: 4e6393b2-4a71-49e4-b1e7-f34bf317d60d
title: O contexto de segurança do cliente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af57c11c7b0452003498b88b0be24c880e2875fec459fb80e3cd87ef01bdd493
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119907116"
---
# <a name="the-client-security-context"></a>O contexto de segurança do cliente

Assim como [*todos os*](/windows/desktop/SecGloss/p-gly)processos, um servidor protegido tem um token [*de acesso*](/windows/desktop/SecGloss/p-gly) primário que descreve seu contexto de [*segurança*](/windows/desktop/SecGloss/s-gly). Quando um cliente se conecta a um servidor protegido, o servidor pode querer executar ações usando o contexto de segurança do cliente em vez do contexto de segurança do servidor. Por exemplo, quando um cliente em uma conversa DDE (troca de dados dinâmica) solicita informações de um servidor DDE, o servidor precisa verificar se o cliente tem permissão de acesso às informações.

Há duas maneiras pelas quais um servidor pode agir no contexto de segurança do cliente:

-   Um thread do processo do servidor pode representar o cliente. Nesse caso, o thread do servidor tem um [*token*](/windows/desktop/SecGloss/a-gly) de acesso de representação que identifica o cliente, os grupos do cliente e os privilégios [*do cliente.*](/windows/desktop/SecGloss/p-gly) Para obter mais informações, consulte [Representação de cliente](client-impersonation.md).
-   O servidor pode obter as credenciais do cliente [*e*](/windows/desktop/SecGloss/c-gly) fazer logoff do cliente no computador do servidor. Isso cria uma nova sessão [*de*](/windows/desktop/SecGloss/s-gly) logon e produz um token de acesso primário para o cliente. O servidor pode usar o token de acesso do cliente para representar o cliente ou iniciar um novo processo que é executado no contexto de segurança do cliente. Para obter mais informações, consulte [Sessões de logon do cliente](client-logon-sessions.md).

Na maioria dos casos, representar o cliente é suficiente. A representação permite que o servidor verifique o acesso do cliente a objetos de segurança, verifique os privilégios do cliente e gere entradas de trilha de auditoria que identificam o cliente. Normalmente, um servidor precisa iniciar uma sessão de logon do cliente somente se precisar usar o contexto de segurança do cliente para acessar recursos de rede.

 

 
