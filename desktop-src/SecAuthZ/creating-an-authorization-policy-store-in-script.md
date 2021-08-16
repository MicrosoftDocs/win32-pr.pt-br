---
description: Instruções para usar a API do Gerenciador de autorização para criar um repositório de política de autorização no script.
ms.assetid: bd9a995a-4195-4da4-a194-472448a0cb08
title: Criando um repositório de política de autorização no script
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: cbe8bf5457f36cdb71577ae13c2cc226115d4c968436c84b72ca8e90a3446be9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117782532"
---
# <a name="creating-an-authorization-policy-store-in-script"></a>Criando um repositório de política de autorização no script

Crie uma política de autorização antes ou durante a instalação de um aplicativo.

Ao usar a API do Gerenciador de autorização para criar uma política de autorização, siga as instruções fornecidas nos tópicos a seguir.



| Tópico                                                                                                                  | Descrição                                                                                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Criando um objeto de repositório de política de autorização no script](creating-an-authorization-policy-store-object-in-script.md) | Um repositório de diretivas de autorização contém informações sobre a política de segurança de um aplicativo ou grupo de aplicativos.                                                                                                                                       |
| [Criando um objeto de aplicativo no script](creating-an-application-object-in-script.md)                               | Para cada aplicativo que usa um repositório de política de autorização, você deve criar um objeto [**IAzApplication**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) e salvá-lo em um repositório de políticas.                                                                                                |
| [Definindo operações no script](defining-operations-in-script.md)                                                     | Uma operação é uma função ou um método de baixo nível de um aplicativo.                                                                                                                                                                                              |
| [Agrupando operações em tarefas no script](grouping-operations-into-tasks-in-script.md)                               | Uma tarefa é uma ação de alto nível que os usuários de um aplicativo precisam concluir. As tarefas são feitas de operações, que são funções e métodos de nível baixo do aplicativo.                                                                                    |
| [Agrupando tarefas em funções no script](grouping-tasks-into-roles-in-script.md)                                         | Uma função representa uma categoria de usuários e as tarefas que esses usuários estão autorizados a executar.                                                                                                                                                                     |
| [Definindo grupos de usuários no script](defining-groups-of-users-in-script.md)                                           | Um objeto [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) representa um grupo de usuários. As funções podem ser atribuídas a esse grupo de usuários coletivamente. Um objeto **IAzApplicationGroup** também pode incluir outros objetos **IAzApplicationGroup** como membros. |
| [Adicionando usuários a um grupo de aplicativos no script](adding-users-to-an-application-group-in-script.md)                   | Um grupo de aplicativos é um grupo de usuários e grupos de usuários. Um grupo de aplicativos pode conter outros grupos de aplicativos, para que os grupos de usuários possam ser aninhados. Um grupo de aplicativos é representado por um objeto [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) .    |



 

 

 



