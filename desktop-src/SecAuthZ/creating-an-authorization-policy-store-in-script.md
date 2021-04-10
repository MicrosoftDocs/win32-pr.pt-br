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
ms.openlocfilehash: c0cb35e8e998f95e99193d1dc5e8a74838b7efc7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091124"
---
# <a name="creating-an-authorization-policy-store-in-script"></a><span data-ttu-id="c95e5-103">Criando um repositório de política de autorização no script</span><span class="sxs-lookup"><span data-stu-id="c95e5-103">Creating an Authorization Policy Store in Script</span></span>

<span data-ttu-id="c95e5-104">Crie uma política de autorização antes ou durante a instalação de um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c95e5-104">Create an authorization policy before or during the installation of an application.</span></span>

<span data-ttu-id="c95e5-105">Ao usar a API do Gerenciador de autorização para criar uma política de autorização, siga as instruções fornecidas nos tópicos a seguir.</span><span class="sxs-lookup"><span data-stu-id="c95e5-105">When you use the Authorization Manager API to create an authorization policy, follow the instructions provided in the following topics.</span></span>



| <span data-ttu-id="c95e5-106">Tópico</span><span class="sxs-lookup"><span data-stu-id="c95e5-106">Topic</span></span>                                                                                                                  | <span data-ttu-id="c95e5-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="c95e5-107">Description</span></span>                                                                                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c95e5-108">Criando um objeto de repositório de política de autorização no script</span><span class="sxs-lookup"><span data-stu-id="c95e5-108">Creating an Authorization Policy Store Object in Script</span></span>](creating-an-authorization-policy-store-object-in-script.md) | <span data-ttu-id="c95e5-109">Um repositório de diretivas de autorização contém informações sobre a política de segurança de um aplicativo ou grupo de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="c95e5-109">An authorization policy store contains information about the security policy of an application or group of applications.</span></span>                                                                                                                                       |
| [<span data-ttu-id="c95e5-110">Criando um objeto de aplicativo no script</span><span class="sxs-lookup"><span data-stu-id="c95e5-110">Creating an Application Object in Script</span></span>](creating-an-application-object-in-script.md)                               | <span data-ttu-id="c95e5-111">Para cada aplicativo que usa um repositório de política de autorização, você deve criar um objeto [**IAzApplication**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) e salvá-lo em um repositório de políticas.</span><span class="sxs-lookup"><span data-stu-id="c95e5-111">For each application that uses an authorization policy store, you must create an [**IAzApplication**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) object and save it to a policy store.</span></span>                                                                                                |
| [<span data-ttu-id="c95e5-112">Definindo operações no script</span><span class="sxs-lookup"><span data-stu-id="c95e5-112">Defining Operations in Script</span></span>](defining-operations-in-script.md)                                                     | <span data-ttu-id="c95e5-113">Uma operação é uma função ou um método de baixo nível de um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c95e5-113">An operation is a low-level function or method of an application.</span></span>                                                                                                                                                                                              |
| [<span data-ttu-id="c95e5-114">Agrupando operações em tarefas no script</span><span class="sxs-lookup"><span data-stu-id="c95e5-114">Grouping Operations into Tasks in Script</span></span>](grouping-operations-into-tasks-in-script.md)                               | <span data-ttu-id="c95e5-115">Uma tarefa é uma ação de alto nível que os usuários de um aplicativo precisam concluir.</span><span class="sxs-lookup"><span data-stu-id="c95e5-115">A task is a high-level action that users of an application need to complete.</span></span> <span data-ttu-id="c95e5-116">As tarefas são feitas de operações, que são funções e métodos de nível baixo do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c95e5-116">Tasks are made up of operations, which are low-level functions and methods of the application.</span></span>                                                                                    |
| [<span data-ttu-id="c95e5-117">Agrupando tarefas em funções no script</span><span class="sxs-lookup"><span data-stu-id="c95e5-117">Grouping Tasks into Roles in Script</span></span>](grouping-tasks-into-roles-in-script.md)                                         | <span data-ttu-id="c95e5-118">Uma função representa uma categoria de usuários e as tarefas que esses usuários estão autorizados a executar.</span><span class="sxs-lookup"><span data-stu-id="c95e5-118">A role represents a category of users and the tasks those users are authorized to perform.</span></span>                                                                                                                                                                     |
| [<span data-ttu-id="c95e5-119">Definindo grupos de usuários no script</span><span class="sxs-lookup"><span data-stu-id="c95e5-119">Defining Groups of Users in Script</span></span>](defining-groups-of-users-in-script.md)                                           | <span data-ttu-id="c95e5-120">Um objeto [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) representa um grupo de usuários.</span><span class="sxs-lookup"><span data-stu-id="c95e5-120">An [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) object represents a group of users.</span></span> <span data-ttu-id="c95e5-121">As funções podem ser atribuídas a esse grupo de usuários coletivamente.</span><span class="sxs-lookup"><span data-stu-id="c95e5-121">Roles can then be assigned to this group of users collectively.</span></span> <span data-ttu-id="c95e5-122">Um objeto **IAzApplicationGroup** também pode incluir outros objetos **IAzApplicationGroup** como membros.</span><span class="sxs-lookup"><span data-stu-id="c95e5-122">An **IAzApplicationGroup** object can also include other **IAzApplicationGroup** objects as members.</span></span> |
| [<span data-ttu-id="c95e5-123">Adicionando usuários a um grupo de aplicativos no script</span><span class="sxs-lookup"><span data-stu-id="c95e5-123">Adding Users to an Application Group in Script</span></span>](adding-users-to-an-application-group-in-script.md)                   | <span data-ttu-id="c95e5-124">Um grupo de aplicativos é um grupo de usuários e grupos de usuários.</span><span class="sxs-lookup"><span data-stu-id="c95e5-124">An application group is a group of users and user groups.</span></span> <span data-ttu-id="c95e5-125">Um grupo de aplicativos pode conter outros grupos de aplicativos, para que os grupos de usuários possam ser aninhados.</span><span class="sxs-lookup"><span data-stu-id="c95e5-125">An application group can contain other application groups, so groups of users can be nested.</span></span> <span data-ttu-id="c95e5-126">Um grupo de aplicativos é representado por um objeto [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) .</span><span class="sxs-lookup"><span data-stu-id="c95e5-126">An application group is represented by an [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) object.</span></span>    |



 

 

 



