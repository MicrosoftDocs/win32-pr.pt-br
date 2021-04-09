---
description: Instruções para usar a API do Gerenciador de autorização para definir permissões no script criando um repositório de política de autorização.
ms.assetid: 114426e8-03a7-41e2-96c9-e2da91aa7d84
title: Definindo permissões no script
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e16f377ffa669da0b686ac28783e9a370efec94d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922309"
---
# <a name="defining-permissions-in-script"></a>Definindo permissões no script

No Gerenciador de autorização, você define quais usuários têm acesso a quais recursos de aplicativo Criando um repositório de política de autorização.

**Para definir permissões de acesso**

1.  Crie o repositório onde a política de autorização está definida:<dl>

[Criando um repositório de política de autorização no script](creating-an-authorization-policy-store-object-in-script.md)  
    </dl>
2.  Crie uma seção no repositório de políticas de autorização para um aplicativo específico:<dl>

[Criando um objeto de aplicativo no script](creating-an-application-object-in-script.md)  
    </dl>
3.  Defina as operações que o aplicativo implementa para acessar e modificar recursos:<dl>

[Definindo operações no script](defining-operations-in-script.md)  
    </dl>
4.  Agrupe operações em tarefas de alto nível que os usuários desejam executar:<dl>

[Agrupando operações em tarefas no script](grouping-operations-into-tasks-in-script.md)  
    </dl>
5.  Definir funções que consistem em grupos de tarefas:<dl>

[Agrupando tarefas em funções no script](grouping-tasks-into-roles-in-script.md)  
    </dl>Um usuário que é atribuído a uma função tem permissão para executar qualquer tarefa atribuída a essa função.
6.  Crie scripts para qualificar o acesso a tarefas em tempo de execução:<dl>

[Qualificando o acesso com a lógica de negócios no script](qualifying-access-with-business-logic-in-script.md)  
    </dl>Esta etapa é opcional.
7.  Definir grupos de usuários:<dl>

[Definindo grupos de usuários no script](defining-groups-of-users-in-script.md)  
    </dl>Esses grupos podem ser atribuídos a funções para determinar quais tarefas eles podem executar.
8.  Adicionar usuários a grupos de usuários:<dl>

[Adicionando usuários a um grupo de aplicativos no script](adding-users-to-an-application-group-in-script.md)  
    </dl>

 

 



