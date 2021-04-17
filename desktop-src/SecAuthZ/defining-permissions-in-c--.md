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
# <a name="defining-permissions-in-c"></a><span data-ttu-id="5a6a8-103">Definindo permissões em C++</span><span class="sxs-lookup"><span data-stu-id="5a6a8-103">Defining Permissions in C++</span></span>

<span data-ttu-id="5a6a8-104">No Gerenciador de autorização, você define quais usuários têm acesso a quais recursos de aplicativo Criando um repositório de política de autorização.</span><span class="sxs-lookup"><span data-stu-id="5a6a8-104">In Authorization Manager, you define which users have access to which application resources by creating an authorization policy store.</span></span>

<span data-ttu-id="5a6a8-105">Para obter informações sobre como definir permissões com ACLs, consulte [definindo permissões com ACLs em C++](defining-permissions-with-acls-in-c--.md).</span><span class="sxs-lookup"><span data-stu-id="5a6a8-105">For information about defining permissions with ACLs, see [Defining Permissions with ACLs in C++](defining-permissions-with-acls-in-c--.md).</span></span>

<span data-ttu-id="5a6a8-106">**Para definir permissões de acesso**</span><span class="sxs-lookup"><span data-stu-id="5a6a8-106">**To define access permissions**</span></span>

1.  <span data-ttu-id="5a6a8-107">Crie o repositório onde a política de autorização está definida:</span><span class="sxs-lookup"><span data-stu-id="5a6a8-107">Create the store where the authorization policy is defined:</span></span><dl>

[<span data-ttu-id="5a6a8-108">Criando um objeto de repositório de política de autorização em C++</span><span class="sxs-lookup"><span data-stu-id="5a6a8-108">Creating an Authorization Policy Store Object in C++</span></span>](creating-an-authorization-policy-store-object-in-c--.md)  
    </dl>
2.  <span data-ttu-id="5a6a8-109">Crie uma seção no repositório de políticas de autorização para um aplicativo específico:</span><span class="sxs-lookup"><span data-stu-id="5a6a8-109">Create a section in the authorization policy store for a specific application:</span></span><dl>

[<span data-ttu-id="5a6a8-110">Criando um objeto de aplicativo em C++</span><span class="sxs-lookup"><span data-stu-id="5a6a8-110">Creating an Application Object in C++</span></span>](creating-an-application-object-in-c--.md)  
    </dl>
3.  <span data-ttu-id="5a6a8-111">Defina as operações que o aplicativo implementa para acessar e modificar recursos:</span><span class="sxs-lookup"><span data-stu-id="5a6a8-111">Define operations that the application implements to access and modify resources:</span></span><dl>

[<span data-ttu-id="5a6a8-112">Definindo operações em C++</span><span class="sxs-lookup"><span data-stu-id="5a6a8-112">Defining Operations in C++</span></span>](defining-operations-in-c--.md)  
    </dl>
4.  <span data-ttu-id="5a6a8-113">Agrupe operações em tarefas de alto nível que os usuários desejam executar:</span><span class="sxs-lookup"><span data-stu-id="5a6a8-113">Group operations into high-level tasks that users want to perform:</span></span><dl>

[<span data-ttu-id="5a6a8-114">Agrupando operações em tarefas em C++</span><span class="sxs-lookup"><span data-stu-id="5a6a8-114">Grouping Operations into Tasks in C++</span></span>](grouping-operations-into-tasks-in-c--.md)  
    </dl>
5.  <span data-ttu-id="5a6a8-115">Definir funções que consistem em grupos de tarefas:</span><span class="sxs-lookup"><span data-stu-id="5a6a8-115">Define roles that consist of groups of tasks:</span></span><dl>

[<span data-ttu-id="5a6a8-116">Agrupando tarefas em funções em C++</span><span class="sxs-lookup"><span data-stu-id="5a6a8-116">Grouping Tasks into Roles in C++</span></span>](grouping-tasks-into-roles-in-c--.md)  
    </dl><span data-ttu-id="5a6a8-117">Um usuário que é atribuído a uma função tem permissão para executar qualquer tarefa atribuída a essa função.</span><span class="sxs-lookup"><span data-stu-id="5a6a8-117">A user that is assigned to a role has permission to perform any task assigned to that role.</span></span>
6.  <span data-ttu-id="5a6a8-118">Crie scripts para qualificar o acesso a tarefas em tempo de execução:</span><span class="sxs-lookup"><span data-stu-id="5a6a8-118">Create scripts to qualify access to tasks at run time:</span></span><dl>

[<span data-ttu-id="5a6a8-119">Qualificando o acesso com a lógica de negócios em C++</span><span class="sxs-lookup"><span data-stu-id="5a6a8-119">Qualifying Access with Business Logic in C++</span></span>](qualifying-access-with-business-logic-in-c--.md)  
    </dl><span data-ttu-id="5a6a8-120">Esta etapa é opcional.</span><span class="sxs-lookup"><span data-stu-id="5a6a8-120">This step is optional.</span></span>
7.  <span data-ttu-id="5a6a8-121">Definir grupos de usuários:</span><span class="sxs-lookup"><span data-stu-id="5a6a8-121">Define groups of users:</span></span><dl>

[<span data-ttu-id="5a6a8-122">Definindo grupos de usuários em C++</span><span class="sxs-lookup"><span data-stu-id="5a6a8-122">Defining Groups of Users in C++</span></span>](defining-groups-of-users-in-c--.md)  
    </dl><span data-ttu-id="5a6a8-123">Esses grupos podem ser atribuídos a funções para determinar quais tarefas eles podem executar.</span><span class="sxs-lookup"><span data-stu-id="5a6a8-123">These groups can then be assigned to roles to determine which tasks they can perform.</span></span>
8.  <span data-ttu-id="5a6a8-124">Adicionar usuários a grupos de usuários:</span><span class="sxs-lookup"><span data-stu-id="5a6a8-124">Add users to user groups:</span></span><dl>

[<span data-ttu-id="5a6a8-125">Adicionando usuários a um grupo de aplicativos em C++</span><span class="sxs-lookup"><span data-stu-id="5a6a8-125">Adding Users to an Application Group in C++</span></span>](adding-users-to-an-application-group-in-c--.md)  
    </dl>

 

 



