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
# <a name="defining-permissions-in-script"></a><span data-ttu-id="8f960-103">Definindo permissões no script</span><span class="sxs-lookup"><span data-stu-id="8f960-103">Defining Permissions in Script</span></span>

<span data-ttu-id="8f960-104">No Gerenciador de autorização, você define quais usuários têm acesso a quais recursos de aplicativo Criando um repositório de política de autorização.</span><span class="sxs-lookup"><span data-stu-id="8f960-104">In Authorization Manager, you define which users have access to which application resources by creating an authorization policy store.</span></span>

<span data-ttu-id="8f960-105">**Para definir permissões de acesso**</span><span class="sxs-lookup"><span data-stu-id="8f960-105">**To define access permissions**</span></span>

1.  <span data-ttu-id="8f960-106">Crie o repositório onde a política de autorização está definida:</span><span class="sxs-lookup"><span data-stu-id="8f960-106">Create the store where the authorization policy is defined:</span></span><dl>

[<span data-ttu-id="8f960-107">Criando um repositório de política de autorização no script</span><span class="sxs-lookup"><span data-stu-id="8f960-107">Creating an Authorization Policy Store in Script</span></span>](creating-an-authorization-policy-store-object-in-script.md)  
    </dl>
2.  <span data-ttu-id="8f960-108">Crie uma seção no repositório de políticas de autorização para um aplicativo específico:</span><span class="sxs-lookup"><span data-stu-id="8f960-108">Create a section in the authorization policy store for a specific application:</span></span><dl>

[<span data-ttu-id="8f960-109">Criando um objeto de aplicativo no script</span><span class="sxs-lookup"><span data-stu-id="8f960-109">Creating an Application Object in Script</span></span>](creating-an-application-object-in-script.md)  
    </dl>
3.  <span data-ttu-id="8f960-110">Defina as operações que o aplicativo implementa para acessar e modificar recursos:</span><span class="sxs-lookup"><span data-stu-id="8f960-110">Define operations that the application implements to access and modify resources:</span></span><dl>

[<span data-ttu-id="8f960-111">Definindo operações no script</span><span class="sxs-lookup"><span data-stu-id="8f960-111">Defining Operations in Script</span></span>](defining-operations-in-script.md)  
    </dl>
4.  <span data-ttu-id="8f960-112">Agrupe operações em tarefas de alto nível que os usuários desejam executar:</span><span class="sxs-lookup"><span data-stu-id="8f960-112">Group operations into high-level tasks that users want to perform:</span></span><dl>

[<span data-ttu-id="8f960-113">Agrupando operações em tarefas no script</span><span class="sxs-lookup"><span data-stu-id="8f960-113">Grouping Operations into Tasks in Script</span></span>](grouping-operations-into-tasks-in-script.md)  
    </dl>
5.  <span data-ttu-id="8f960-114">Definir funções que consistem em grupos de tarefas:</span><span class="sxs-lookup"><span data-stu-id="8f960-114">Define roles that consist of groups of tasks:</span></span><dl>

[<span data-ttu-id="8f960-115">Agrupando tarefas em funções no script</span><span class="sxs-lookup"><span data-stu-id="8f960-115">Grouping Tasks into Roles in Script</span></span>](grouping-tasks-into-roles-in-script.md)  
    </dl><span data-ttu-id="8f960-116">Um usuário que é atribuído a uma função tem permissão para executar qualquer tarefa atribuída a essa função.</span><span class="sxs-lookup"><span data-stu-id="8f960-116">A user that is assigned to a role has permission to perform any task assigned to that role.</span></span>
6.  <span data-ttu-id="8f960-117">Crie scripts para qualificar o acesso a tarefas em tempo de execução:</span><span class="sxs-lookup"><span data-stu-id="8f960-117">Create scripts to qualify access to tasks at run time:</span></span><dl>

[<span data-ttu-id="8f960-118">Qualificando o acesso com a lógica de negócios no script</span><span class="sxs-lookup"><span data-stu-id="8f960-118">Qualifying Access with Business Logic in Script</span></span>](qualifying-access-with-business-logic-in-script.md)  
    </dl><span data-ttu-id="8f960-119">Esta etapa é opcional.</span><span class="sxs-lookup"><span data-stu-id="8f960-119">This step is optional.</span></span>
7.  <span data-ttu-id="8f960-120">Definir grupos de usuários:</span><span class="sxs-lookup"><span data-stu-id="8f960-120">Define groups of users:</span></span><dl>

[<span data-ttu-id="8f960-121">Definindo grupos de usuários no script</span><span class="sxs-lookup"><span data-stu-id="8f960-121">Defining Groups of Users in Script</span></span>](defining-groups-of-users-in-script.md)  
    </dl><span data-ttu-id="8f960-122">Esses grupos podem ser atribuídos a funções para determinar quais tarefas eles podem executar.</span><span class="sxs-lookup"><span data-stu-id="8f960-122">These groups can then be assigned to roles to determine which tasks they can perform.</span></span>
8.  <span data-ttu-id="8f960-123">Adicionar usuários a grupos de usuários:</span><span class="sxs-lookup"><span data-stu-id="8f960-123">Add users to user groups:</span></span><dl>

[<span data-ttu-id="8f960-124">Adicionando usuários a um grupo de aplicativos no script</span><span class="sxs-lookup"><span data-stu-id="8f960-124">Adding Users to an Application Group in Script</span></span>](adding-users-to-an-application-group-in-script.md)  
    </dl>

 

 



