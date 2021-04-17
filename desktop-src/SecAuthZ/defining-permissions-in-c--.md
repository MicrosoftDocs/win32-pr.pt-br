---
description: Instruções para usar a API do Gerenciador de autorização para definir permissões em C++ criando um repositório de política de autorização.
ms.assetid: 8a3bf625-7973-4905-a63c-e42e6682b7c2
title: Definindo permissões em C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc398d811f44b69dbde8d30f135fd4f30a552bbf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105751167"
---
# <a name="defining-permissions-in-c"></a>Definindo permissões em C++

No Gerenciador de autorização, você define quais usuários têm acesso a quais recursos de aplicativo Criando um repositório de política de autorização.

Para obter informações sobre como definir permissões com ACLs, consulte [definindo permissões com ACLs em C++](defining-permissions-with-acls-in-c--.md).

**Para definir permissões de acesso**

1.  Crie o repositório onde a política de autorização está definida:<dl>

[Criando um objeto de repositório de política de autorização em C++](creating-an-authorization-policy-store-object-in-c--.md)  
    </dl>
2.  Crie uma seção no repositório de políticas de autorização para um aplicativo específico:<dl>

[Criando um objeto de aplicativo em C++](creating-an-application-object-in-c--.md)  
    </dl>
3.  Defina as operações que o aplicativo implementa para acessar e modificar recursos:<dl>

[Definindo operações em C++](defining-operations-in-c--.md)  
    </dl>
4.  Agrupe operações em tarefas de alto nível que os usuários desejam executar:<dl>

[Agrupando operações em tarefas em C++](grouping-operations-into-tasks-in-c--.md)  
    </dl>
5.  Definir funções que consistem em grupos de tarefas:<dl>

[Agrupando tarefas em funções em C++](grouping-tasks-into-roles-in-c--.md)  
    </dl>Um usuário que é atribuído a uma função tem permissão para executar qualquer tarefa atribuída a essa função.
6.  Crie scripts para qualificar o acesso a tarefas em tempo de execução:<dl>

[Qualificando o acesso com a lógica de negócios em C++](qualifying-access-with-business-logic-in-c--.md)  
    </dl>Esta etapa é opcional.
7.  Definir grupos de usuários:<dl>

[Definindo grupos de usuários em C++](defining-groups-of-users-in-c--.md)  
    </dl>Esses grupos podem ser atribuídos a funções para determinar quais tarefas eles podem executar.
8.  Adicionar usuários a grupos de usuários:<dl>

[Adicionando usuários a um grupo de aplicativos em C++](adding-users-to-an-application-group-in-c--.md)  
    </dl>

 

 



