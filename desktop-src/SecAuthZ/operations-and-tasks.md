---
description: Uma operação é uma ação de computador de baixo nível.
ms.assetid: d75bc507-3502-417c-af05-cbff807a5778
title: Operações e tarefas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a198d8844a9f34030b8b6a40eba759eed4057119
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105756567"
---
# <a name="operations-and-tasks"></a><span data-ttu-id="a7e41-103">Operações e tarefas</span><span class="sxs-lookup"><span data-stu-id="a7e41-103">Operations and Tasks</span></span>

<span data-ttu-id="a7e41-104">Uma operação é uma ação de computador de baixo nível.</span><span class="sxs-lookup"><span data-stu-id="a7e41-104">An operation is a low-level computer action.</span></span> <span data-ttu-id="a7e41-105">Na API do Gerenciador de autorização, uma operação é representada por um objeto [**IAzOperation**](/windows/desktop/api/Azroles/nn-azroles-iazoperation) .</span><span class="sxs-lookup"><span data-stu-id="a7e41-105">In the Authorization Manager API, an operation is represented by an [**IAzOperation**](/windows/desktop/api/Azroles/nn-azroles-iazoperation) object.</span></span> <span data-ttu-id="a7e41-106">Em geral, as operações são muitos em número e um nível muito baixo para facilitar a administração.</span><span class="sxs-lookup"><span data-stu-id="a7e41-106">In general, operations are too many in number and too low-level to facilitate administration.</span></span> <span data-ttu-id="a7e41-107">Agrupe operações em tarefas para simplificar a administração da política de autorização.</span><span class="sxs-lookup"><span data-stu-id="a7e41-107">Group operations into tasks to simplify administration of authorization policy.</span></span>

<span data-ttu-id="a7e41-108">Uma tarefa é representada por um objeto [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) e pode conter um ou mais objetos [**IAzOperation**](/windows/desktop/api/Azroles/nn-azroles-iazoperation) .</span><span class="sxs-lookup"><span data-stu-id="a7e41-108">A task is represented by an [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) object and can contain one or more [**IAzOperation**](/windows/desktop/api/Azroles/nn-azroles-iazoperation) objects.</span></span> <span data-ttu-id="a7e41-109">Um objeto **IAzTask** também pode conter outros objetos **IAzTask** , para que as tarefas possam ser aninhadas.</span><span class="sxs-lookup"><span data-stu-id="a7e41-109">An **IAzTask** object can also contain other **IAzTask** objects, so that tasks can be nested.</span></span> <span data-ttu-id="a7e41-110">Para facilitar a administração, um objeto **IAzTask** deve representar uma tarefa que um usuário real deseja executar.</span><span class="sxs-lookup"><span data-stu-id="a7e41-110">To facilitate administration, an **IAzTask** object should represent a task that a real user wants to perform.</span></span>

<span data-ttu-id="a7e41-111">O acesso às operações contidas por uma tarefa pode ser qualificado em tempo de execução por um script de regra de negócio associado ao objeto [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) que representa essa tarefa.</span><span class="sxs-lookup"><span data-stu-id="a7e41-111">Access to the operations contained by a task can be qualified at run time by a business rule script associated with the [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) object that represents that task.</span></span> <span data-ttu-id="a7e41-112">Para obter mais informações sobre scripts de regra de negócio, consulte [regras de negócio](business-rules.md).</span><span class="sxs-lookup"><span data-stu-id="a7e41-112">For more information about business rule scripts, see [Business Rules](business-rules.md).</span></span>

<span data-ttu-id="a7e41-113">Um objeto [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) também pode representar uma definição de função definindo sua propriedade [**IsRoleDefinition**](/windows/desktop/api/Azroles/nf-azroles-iaztask-get_isroledefinition) como **true**.</span><span class="sxs-lookup"><span data-stu-id="a7e41-113">An [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) object can also represent a role definition by setting its [**IsRoleDefinition**](/windows/desktop/api/Azroles/nf-azroles-iaztask-get_isroledefinition) property to **TRUE**.</span></span> <span data-ttu-id="a7e41-114">A interface do usuário do snap-in MMC do **Gerenciador de autorização** exibe esse objeto **IAzTask** como uma função.</span><span class="sxs-lookup"><span data-stu-id="a7e41-114">The **Authorization Manager** MMC snap-in user interface then displays that **IAzTask** object as a role.</span></span> <span data-ttu-id="a7e41-115">Para obter mais informações sobre definições de função, consulte [funções](roles.md).</span><span class="sxs-lookup"><span data-stu-id="a7e41-115">For more information about role definitions, see [Roles](roles.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a7e41-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a7e41-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a7e41-117">Definindo operações em C++</span><span class="sxs-lookup"><span data-stu-id="a7e41-117">Defining Operations in C++</span></span>](defining-operations-in-c--.md)
</dt> <dt>

[<span data-ttu-id="a7e41-118">Agrupando operações em tarefas em C++</span><span class="sxs-lookup"><span data-stu-id="a7e41-118">Grouping Operations into Tasks in C++</span></span>](grouping-operations-into-tasks-in-c--.md)
</dt> <dt>

[<span data-ttu-id="a7e41-119">Agrupando tarefas em funções em C++</span><span class="sxs-lookup"><span data-stu-id="a7e41-119">Grouping Tasks into Roles in C++</span></span>](grouping-tasks-into-roles-in-c--.md)
</dt> <dt>

[<span data-ttu-id="a7e41-120">Usuários e grupos</span><span class="sxs-lookup"><span data-stu-id="a7e41-120">Users and Groups</span></span>](users-and-groups.md)
</dt> </dl>

 

 



