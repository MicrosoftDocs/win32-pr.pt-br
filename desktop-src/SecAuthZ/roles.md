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
# <a name="roles"></a><span data-ttu-id="e697a-103">Funções</span><span class="sxs-lookup"><span data-stu-id="e697a-103">Roles</span></span>

<span data-ttu-id="e697a-104">As funções atendem a duas finalidades diferentes no Gerenciador de autorização.</span><span class="sxs-lookup"><span data-stu-id="e697a-104">Roles serve two different purposes in Authorization Manager.</span></span> <span data-ttu-id="e697a-105">Uma função é um conjunto de tarefas ou operações às quais uma categoria de usuários requer acesso e também um conjunto de usuários e grupos que se ajustam a essa categoria.</span><span class="sxs-lookup"><span data-stu-id="e697a-105">A role is a set of tasks or operations to which a category of users requires access, and it is also a set of users and groups that fit into that category.</span></span>

-   [<span data-ttu-id="e697a-106">Funções como conjuntos de tarefas</span><span class="sxs-lookup"><span data-stu-id="e697a-106">Roles as Sets of Tasks</span></span>](#roles-as-sets-of-tasks)
-   [<span data-ttu-id="e697a-107">Funções como conjuntos de usuários e grupos</span><span class="sxs-lookup"><span data-stu-id="e697a-107">Roles as Sets of Users and Groups</span></span>](#roles-as-sets-of-users-and-groups)
-   [<span data-ttu-id="e697a-108">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e697a-108">Related topics</span></span>](#related-topics)

## <a name="roles-as-sets-of-tasks"></a><span data-ttu-id="e697a-109">Funções como conjuntos de tarefas</span><span class="sxs-lookup"><span data-stu-id="e697a-109">Roles as Sets of Tasks</span></span>

<span data-ttu-id="e697a-110">Uma política de autorização atribui objetos [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) a um objeto [**IAzRole**](/windows/desktop/api/Azroles/nn-azroles-iazrole) para criar conjuntos de tarefas.</span><span class="sxs-lookup"><span data-stu-id="e697a-110">An authorization policy assigns [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) objects to an [**IAzRole**](/windows/desktop/api/Azroles/nn-azroles-iazrole) object to create sets of tasks.</span></span> <span data-ttu-id="e697a-111">Todos os usuários e grupos atribuídos a esse objeto **IAzRole** , em seguida, têm permissão para acessar todas as operações contidas por esses objetos **IAzTask** .</span><span class="sxs-lookup"><span data-stu-id="e697a-111">All users and groups assigned to that **IAzRole** object then have permission to access all operations contained by those **IAzTask** objects.</span></span>

<span data-ttu-id="e697a-112">Como um objeto [**IAzRole**](/windows/desktop/api/Azroles/nn-azroles-iazrole) representa um conjunto de tarefas e um conjunto de usuários e grupos que têm acesso a essas tarefas, o Gerenciador de autorização fornece uma maneira de criar definições de função que podem ser atribuídas a mais de um objeto **IAzRole** .</span><span class="sxs-lookup"><span data-stu-id="e697a-112">Because an [**IAzRole**](/windows/desktop/api/Azroles/nn-azroles-iazrole) object represents both a set of tasks and a set of users and groups that have access to those tasks, Authorization Manager provides a way to create role definitions that can be assigned to more than one **IAzRole** object.</span></span> <span data-ttu-id="e697a-113">Um objeto [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) pode conter outros objetos **IAzTask** .</span><span class="sxs-lookup"><span data-stu-id="e697a-113">An [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) object can contain other **IAzTask** objects.</span></span> <span data-ttu-id="e697a-114">Em seguida, você pode usar esse objeto **IAzTask** como uma definição de função, atribuindo-o a um ou mais objetos **IAzRole** .</span><span class="sxs-lookup"><span data-stu-id="e697a-114">You can then use that **IAzTask** object as a role definition by assigning it to one or more **IAzRole** objects.</span></span> <span data-ttu-id="e697a-115">Defina a propriedade [**IsRoleDefinition**](/windows/desktop/api/Azroles/nf-azroles-iaztask-get_isroledefinition) do objeto **IAzTask** como **true** para fazer com que a interface do usuário do snap-in MMC do **Gerenciador de autorização** exiba o objeto **IAzTask** como uma função.</span><span class="sxs-lookup"><span data-stu-id="e697a-115">Set the [**IsRoleDefinition**](/windows/desktop/api/Azroles/nf-azroles-iaztask-get_isroledefinition) property of the **IAzTask** object to **TRUE** to cause the **Authorization Manager** MMC snap-in user interface to display the **IAzTask** object as a role.</span></span>

## <a name="roles-as-sets-of-users-and-groups"></a><span data-ttu-id="e697a-116">Funções como conjuntos de usuários e grupos</span><span class="sxs-lookup"><span data-stu-id="e697a-116">Roles as Sets of Users and Groups</span></span>

<span data-ttu-id="e697a-117">Atribua usuários e grupos a um objeto [**IAzRole**](/windows/desktop/api/Azroles/nn-azroles-iazrole) para conceder a esses usuários e grupos o acesso às tarefas atribuídas a esse objeto **IAzRole** chamando o método [**AddMember**](/windows/desktop/api/Azroles/nf-azroles-iazrole-addmember) ou [**addmembername**](/windows/desktop/api/Azroles/nf-azroles-iazrole-addmembername) .</span><span class="sxs-lookup"><span data-stu-id="e697a-117">Assign users and groups to an [**IAzRole**](/windows/desktop/api/Azroles/nn-azroles-iazrole) object to grant those users and groups access to the tasks assigned to that **IAzRole** object by calling the [**AddMember**](/windows/desktop/api/Azroles/nf-azroles-iazrole-addmember) or [**AddMemberName**](/windows/desktop/api/Azroles/nf-azroles-iazrole-addmembername) method.</span></span> <span data-ttu-id="e697a-118">Atribua grupos de aplicativos existentes, representados por objetos [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) , a um objeto **IAzRole** chamando o método [**AddAppMember**](/windows/desktop/api/Azroles/nf-azroles-iazrole-addappmember) .</span><span class="sxs-lookup"><span data-stu-id="e697a-118">Assign existing application groups, represented by [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) objects, to an **IAzRole** object by calling the [**AddAppMember**](/windows/desktop/api/Azroles/nf-azroles-iazrole-addappmember) method.</span></span> <span data-ttu-id="e697a-119">Todos os usuários e grupos atribuídos ao objeto **IAzRole** têm acesso às tarefas e operações atribuídas a essa função.</span><span class="sxs-lookup"><span data-stu-id="e697a-119">All users and groups assigned to the **IAzRole** object have access to the tasks and operations assigned to that role.</span></span> <span data-ttu-id="e697a-120">Para obter mais informações sobre grupos de aplicativos, consulte [usuários e grupos](users-and-groups.md).</span><span class="sxs-lookup"><span data-stu-id="e697a-120">For more information about application groups, see [Users and Groups](users-and-groups.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e697a-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e697a-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e697a-122">Agrupando tarefas em funções em C++</span><span class="sxs-lookup"><span data-stu-id="e697a-122">Grouping Tasks into Roles in C++</span></span>](grouping-tasks-into-roles-in-c--.md)
</dt> <dt>

[<span data-ttu-id="e697a-123">Definindo grupos de usuários em C++</span><span class="sxs-lookup"><span data-stu-id="e697a-123">Defining Groups of Users in C++</span></span>](defining-groups-of-users-in-c--.md)
</dt> <dt>

[<span data-ttu-id="e697a-124">Adicionando usuários a um grupo de aplicativos em C++</span><span class="sxs-lookup"><span data-stu-id="e697a-124">Adding Users to an Application Group in C++</span></span>](adding-users-to-an-application-group-in-c--.md)
</dt> </dl>

 

 



