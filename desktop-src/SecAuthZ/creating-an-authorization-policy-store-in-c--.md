---
description: Instruções para usar a API do Gerenciador de autorização para criar um repositório de política de autorização em C++.
ms.assetid: a350f25a-7cda-4879-82d1-151a3da7d8ec
title: Criando um repositório de política de autorização em C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90eeb30fd1e66bc69760f8bf3d714419fe818dbda06c1b8e2eb059aeb579ca74
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117782522"
---
# <a name="creating-an-authorization-policy-store-in-c"></a>Criando um repositório de política de autorização em C++

Crie uma política de autorização antes ou durante a instalação de um aplicativo.

Ao usar a API do Gerenciador de autorização para criar uma política de autorização, siga as instruções fornecidas nos tópicos a seguir.



| Tópico                                                                                                            | Descrição                                                                                                                                                                                                                                               |
|------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Criando um objeto de repositório de política de autorização em C++](creating-an-authorization-policy-store-object-in-c--.md) | Um repositório de diretivas de autorização contém informações sobre a política de segurança de um aplicativo ou grupo de aplicativos. As informações incluem os aplicativos, as operações, as tarefas, os usuários e os grupos de usuários associados à loja.              |
| [Criando um objeto de aplicativo em C++](creating-an-application-object-in-c--.md)                               | Um repositório de diretivas de autorização contém informações de política de autorização para um ou mais aplicativos. Para cada aplicativo que usa esse repositório de políticas, você deve criar um objeto [**IAzApplication**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) e salvá-lo em um repositório de políticas. |
| [Definindo operações em C++](defining-operations-in-c--.md)                                                     | No Gerenciador de autorização, uma operação é uma função ou um método de baixo nível de um aplicativo.                                                                                                                                                               |
| [Agrupando operações em tarefas em C++](grouping-operations-into-tasks-in-c--.md)                               | No Gerenciador de autorização, uma tarefa é uma ação de alto nível que os usuários de um aplicativo precisam concluir. As tarefas são feitas de operações, que são funções e métodos de nível baixo do aplicativo.                                                     |
| [Agrupando tarefas em funções em C++](grouping-tasks-into-roles-in-c--.md)                                         | No Gerenciador de autorização, uma função representa uma categoria de usuários e as tarefas que esses usuários estão autorizados a executar.                                                                                                                                      |
| [Definindo grupos de usuários em C++](defining-groups-of-users-in-c--.md)                                           | No Gerenciador de autorização, um objeto [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) representa um grupo de usuários. As funções podem ser atribuídas a esse grupo de usuários coletivamente.                                                                       |
| [Adicionando usuários a um grupo de aplicativos em C++](adding-users-to-an-application-group-in-c--.md)                   | No Gerenciador de autorização, um grupo de aplicativos é um grupo de usuários e grupos de usuários. Um grupo de aplicativos pode conter outros grupos de aplicativos, para que os grupos de usuários possam ser aninhados.                                                                          |



 

 

 



