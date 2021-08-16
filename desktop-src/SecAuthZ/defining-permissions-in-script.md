---
description: Instruções para usar a API do Gerenciador de Autorização para definir permissões em Script criando um armazenamento de política de autorização.
ms.assetid: 114426e8-03a7-41e2-96c9-e2da91aa7d84
title: Definindo permissões no script
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 772c55f453a68e3bf1a4933abc4beb7cf3d65380b3bcf5d2e2c4af2832173b73
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117782097"
---
# <a name="defining-permissions-in-script"></a>Definindo permissões no script

No Gerenciador de Autorização, você define quais usuários têm acesso a quais recursos de aplicativo criando um armazenamento de política de autorização.

**Para definir permissões de acesso**

1.  Crie o armazenamento em que a política de autorização está definida:<dl>

[Criando um armazenamento de política de autorização no script](creating-an-authorization-policy-store-object-in-script.md)  
    </dl>
2.  Crie uma seção no armazenamento de política de autorização para um aplicativo específico:<dl>

[Criando um objeto de aplicativo no script](creating-an-application-object-in-script.md)  
    </dl>
3.  Defina operações que o aplicativo implementa para acessar e modificar recursos:<dl>

[Definindo operações no script](defining-operations-in-script.md)  
    </dl>
4.  Agrupar operações em tarefas de alto nível que os usuários querem executar:<dl>

[Agrupando operações em tarefas no script](grouping-operations-into-tasks-in-script.md)  
    </dl>
5.  Defina funções que consistem em grupos de tarefas:<dl>

[Agrupando tarefas em funções no script](grouping-tasks-into-roles-in-script.md)  
    </dl>Um usuário atribuído a uma função tem permissão para executar qualquer tarefa atribuída a essa função.
6.  Crie scripts para qualificar o acesso às tarefas em tempo de executar:<dl>

[Qualificando o acesso com lógica de negócios no script](qualifying-access-with-business-logic-in-script.md)  
    </dl>Esta etapa é opcional.
7.  Defina grupos de usuários:<dl>

[Definindo grupos de usuários no script](defining-groups-of-users-in-script.md)  
    </dl>Esses grupos podem ser atribuídos a funções para determinar quais tarefas eles podem executar.
8.  Adicionar usuários a grupos de usuários:<dl>

[Adicionando usuários a um grupo de aplicativos no script](adding-users-to-an-application-group-in-script.md)  
    </dl>

 

 



