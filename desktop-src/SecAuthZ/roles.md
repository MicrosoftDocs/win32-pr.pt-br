---
description: As funções atendem a duas finalidades diferentes no Gerenciador de autorização.
ms.assetid: 6d045ecb-432e-4ba6-b5d2-37db82ab1884
title: Funções
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc65d140faa22c72d098c7a4ba2f13e952b2713f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827339"
---
# <a name="roles"></a>Funções

As funções atendem a duas finalidades diferentes no Gerenciador de autorização. Uma função é um conjunto de tarefas ou operações às quais uma categoria de usuários requer acesso e também um conjunto de usuários e grupos que se ajustam a essa categoria.

-   [Funções como conjuntos de tarefas](#roles-as-sets-of-tasks)
-   [Funções como conjuntos de usuários e grupos](#roles-as-sets-of-users-and-groups)
-   [Tópicos relacionados](#related-topics)

## <a name="roles-as-sets-of-tasks"></a>Funções como conjuntos de tarefas

Uma política de autorização atribui objetos [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) a um objeto [**IAzRole**](/windows/desktop/api/Azroles/nn-azroles-iazrole) para criar conjuntos de tarefas. Todos os usuários e grupos atribuídos a esse objeto **IAzRole** , em seguida, têm permissão para acessar todas as operações contidas por esses objetos **IAzTask** .

Como um objeto [**IAzRole**](/windows/desktop/api/Azroles/nn-azroles-iazrole) representa um conjunto de tarefas e um conjunto de usuários e grupos que têm acesso a essas tarefas, o Gerenciador de autorização fornece uma maneira de criar definições de função que podem ser atribuídas a mais de um objeto **IAzRole** . Um objeto [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) pode conter outros objetos **IAzTask** . Em seguida, você pode usar esse objeto **IAzTask** como uma definição de função, atribuindo-o a um ou mais objetos **IAzRole** . Defina a propriedade [**IsRoleDefinition**](/windows/desktop/api/Azroles/nf-azroles-iaztask-get_isroledefinition) do objeto **IAzTask** como **true** para fazer com que a interface do usuário do snap-in MMC do **Gerenciador de autorização** exiba o objeto **IAzTask** como uma função.

## <a name="roles-as-sets-of-users-and-groups"></a>Funções como conjuntos de usuários e grupos

Atribua usuários e grupos a um objeto [**IAzRole**](/windows/desktop/api/Azroles/nn-azroles-iazrole) para conceder a esses usuários e grupos o acesso às tarefas atribuídas a esse objeto **IAzRole** chamando o método [**AddMember**](/windows/desktop/api/Azroles/nf-azroles-iazrole-addmember) ou [**addmembername**](/windows/desktop/api/Azroles/nf-azroles-iazrole-addmembername) . Atribua grupos de aplicativos existentes, representados por objetos [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) , a um objeto **IAzRole** chamando o método [**AddAppMember**](/windows/desktop/api/Azroles/nf-azroles-iazrole-addappmember) . Todos os usuários e grupos atribuídos ao objeto **IAzRole** têm acesso às tarefas e operações atribuídas a essa função. Para obter mais informações sobre grupos de aplicativos, consulte [usuários e grupos](users-and-groups.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Agrupando tarefas em funções em C++](grouping-tasks-into-roles-in-c--.md)
</dt> <dt>

[Definindo grupos de usuários em C++](defining-groups-of-users-in-c--.md)
</dt> <dt>

[Adicionando usuários a um grupo de aplicativos em C++](adding-users-to-an-application-group-in-c--.md)
</dt> </dl>

 

 



