---
title: Funções de grupo
description: Um grupo global contém contas de usuário de um domínio que são agrupados em um nome de conta de grupo.
ms.assetid: 2199258d-bde9-4fdb-b9c1-147616420fbe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7696755cd5f5cbe75de11d386cb238fa3bd5d35d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366536"
---
# <a name="group-functions"></a><span data-ttu-id="6dfcb-103">Funções de grupo</span><span class="sxs-lookup"><span data-stu-id="6dfcb-103">Group Functions</span></span>

<span data-ttu-id="6dfcb-104">Um *grupo global* contém contas de usuário de um domínio que são agrupados em um nome de conta de grupo.</span><span class="sxs-lookup"><span data-stu-id="6dfcb-104">A *global group* contains user accounts from one domain that are grouped together under one group account name.</span></span> <span data-ttu-id="6dfcb-105">Um grupo global pode conter somente Membros (usuários) do domínio em que o grupo global é criado; Ele não pode conter grupos locais.</span><span class="sxs-lookup"><span data-stu-id="6dfcb-105">A global group can contain only members (users) from the domain where the global group is created; it cannot contain local groups.</span></span> <span data-ttu-id="6dfcb-106">Um grupo global está disponível em seu próprio domínio e em qualquer domínio confiante.</span><span class="sxs-lookup"><span data-stu-id="6dfcb-106">A global group is available within its own domain and within any trusting domain.</span></span>

<span data-ttu-id="6dfcb-107">As funções do grupo de gerenciamento de rede controlam grupos globais.</span><span class="sxs-lookup"><span data-stu-id="6dfcb-107">The network management group functions control global groups.</span></span> <span data-ttu-id="6dfcb-108">As funções de grupo são listadas a seguir.</span><span class="sxs-lookup"><span data-stu-id="6dfcb-108">The group functions are listed following.</span></span>



| <span data-ttu-id="6dfcb-109">Função</span><span class="sxs-lookup"><span data-stu-id="6dfcb-109">Function</span></span>                                     | <span data-ttu-id="6dfcb-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="6dfcb-110">Description</span></span>                                                                       |
|----------------------------------------------|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="6dfcb-111">**NetGroupAdd**</span><span class="sxs-lookup"><span data-stu-id="6dfcb-111">**NetGroupAdd**</span></span>](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupadd)           | <span data-ttu-id="6dfcb-112">Cria um grupo global.</span><span class="sxs-lookup"><span data-stu-id="6dfcb-112">Creates a global group.</span></span>                                                           |
| [<span data-ttu-id="6dfcb-113">**NetGroupAddUser**</span><span class="sxs-lookup"><span data-stu-id="6dfcb-113">**NetGroupAddUser**</span></span>](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupadduser)   | <span data-ttu-id="6dfcb-114">Adiciona um usuário a um grupo global existente.</span><span class="sxs-lookup"><span data-stu-id="6dfcb-114">Adds one user to an existing global group.</span></span>                                        |
| [<span data-ttu-id="6dfcb-115">**NetGroupDel**</span><span class="sxs-lookup"><span data-stu-id="6dfcb-115">**NetGroupDel**</span></span>](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupdel)           | <span data-ttu-id="6dfcb-116">Remove um grupo global, independentemente de o grupo ter ou não membros.</span><span class="sxs-lookup"><span data-stu-id="6dfcb-116">Removes a global group whether or not the group has any members.</span></span>                  |
| [<span data-ttu-id="6dfcb-117">**NetGroupDelUser**</span><span class="sxs-lookup"><span data-stu-id="6dfcb-117">**NetGroupDelUser**</span></span>](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupdeluser)   | <span data-ttu-id="6dfcb-118">Remove um nome de usuário de um grupo global.</span><span class="sxs-lookup"><span data-stu-id="6dfcb-118">Removes one user name from a global group.</span></span>                                        |
| [<span data-ttu-id="6dfcb-119">**NetGroupEnum**</span><span class="sxs-lookup"><span data-stu-id="6dfcb-119">**NetGroupEnum**</span></span>](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupenum)         | <span data-ttu-id="6dfcb-120">Lista todos os grupos globais em um servidor.</span><span class="sxs-lookup"><span data-stu-id="6dfcb-120">Lists all global groups on a server.</span></span>                                              |
| [<span data-ttu-id="6dfcb-121">**NetGroupGetInfo**</span><span class="sxs-lookup"><span data-stu-id="6dfcb-121">**NetGroupGetInfo**</span></span>](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupgetinfo)   | <span data-ttu-id="6dfcb-122">Retorna informações sobre um determinado grupo global.</span><span class="sxs-lookup"><span data-stu-id="6dfcb-122">Returns information about a particular global group.</span></span>                              |
| [<span data-ttu-id="6dfcb-123">**NetGroupGetUsers**</span><span class="sxs-lookup"><span data-stu-id="6dfcb-123">**NetGroupGetUsers**</span></span>](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupgetusers) | <span data-ttu-id="6dfcb-124">Lista todos os membros de um determinado grupo global.</span><span class="sxs-lookup"><span data-stu-id="6dfcb-124">Lists all members of a particular global group.</span></span>                                   |
| [<span data-ttu-id="6dfcb-125">**NetGroupSetInfo**</span><span class="sxs-lookup"><span data-stu-id="6dfcb-125">**NetGroupSetInfo**</span></span>](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupsetinfo)   | <span data-ttu-id="6dfcb-126">Define informações gerais sobre um grupo global.</span><span class="sxs-lookup"><span data-stu-id="6dfcb-126">Sets general information about a global group.</span></span>                                    |
| [<span data-ttu-id="6dfcb-127">**NetGroupSetUsers**</span><span class="sxs-lookup"><span data-stu-id="6dfcb-127">**NetGroupSetUsers**</span></span>](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupsetusers) | <span data-ttu-id="6dfcb-128">Atribui membros a um novo grupo global; substitui os membros de um grupo existente.</span><span class="sxs-lookup"><span data-stu-id="6dfcb-128">Assigns members to a new global group; replaces the members of an existing group.</span></span> |



 

<span data-ttu-id="6dfcb-129">Ao chamar a função [**NetGroupAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupadd) para criar um grupo global, você deve fornecer um nome de grupo.</span><span class="sxs-lookup"><span data-stu-id="6dfcb-129">When you call the [**NetGroupAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupadd) function to create a global group, you must supply a group name.</span></span> <span data-ttu-id="6dfcb-130">Inicialmente, um novo grupo não tem nenhum membro.</span><span class="sxs-lookup"><span data-stu-id="6dfcb-130">Initially, a new group has no members.</span></span>

<span data-ttu-id="6dfcb-131">As contas de usuário pertencem automaticamente aos usuários do domínio do grupo global especial.</span><span class="sxs-lookup"><span data-stu-id="6dfcb-131">User accounts automatically belong to the special global group Domain Users.</span></span> <span data-ttu-id="6dfcb-132">A associação a esse grupo é controlada indiretamente pelas funções [**NetUserAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuseradd), [**NetUserDel**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserdel)e [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) .</span><span class="sxs-lookup"><span data-stu-id="6dfcb-132">Membership in this group is indirectly controlled by the [**NetUserAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuseradd), [**NetUserDel**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserdel), and [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) functions.</span></span>

<span data-ttu-id="6dfcb-133">As informações de conta de grupo global estão disponíveis nos seguintes níveis:</span><span class="sxs-lookup"><span data-stu-id="6dfcb-133">Global group account information is available at the following levels:</span></span>

-   [<span data-ttu-id="6dfcb-134">**Informações do grupo \_ \_ 0**</span><span class="sxs-lookup"><span data-stu-id="6dfcb-134">**GROUP\_INFO\_0**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-group_info_0)
-   [<span data-ttu-id="6dfcb-135">**Informações do grupo \_ \_ 1**</span><span class="sxs-lookup"><span data-stu-id="6dfcb-135">**GROUP\_INFO\_1**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-group_info_1)
-   [<span data-ttu-id="6dfcb-136">**Informações do grupo \_ \_ 2**</span><span class="sxs-lookup"><span data-stu-id="6dfcb-136">**GROUP\_INFO\_2**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-group_info_2)
-   [<span data-ttu-id="6dfcb-137">**Informações do grupo \_ \_ 3**</span><span class="sxs-lookup"><span data-stu-id="6dfcb-137">**GROUP\_INFO\_3**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-group_info_3)
-   [<span data-ttu-id="6dfcb-138">**Informações do grupo \_ \_ 1002**</span><span class="sxs-lookup"><span data-stu-id="6dfcb-138">**GROUP\_INFO\_1002**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-group_info_1002)
-   [<span data-ttu-id="6dfcb-139">**Informações do grupo \_ \_ 1005**</span><span class="sxs-lookup"><span data-stu-id="6dfcb-139">**GROUP\_INFO\_1005**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-group_info_1005)

<span data-ttu-id="6dfcb-140">Os níveis 1002 e 1005 são válidos somente para a função [**NetGroupSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupsetinfo) .</span><span class="sxs-lookup"><span data-stu-id="6dfcb-140">The 1002 and 1005 levels are valid only for the [**NetGroupSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupsetinfo) function.</span></span>

<span data-ttu-id="6dfcb-141">As informações do membro do grupo global estão disponíveis no seguinte nível de informação:</span><span class="sxs-lookup"><span data-stu-id="6dfcb-141">Global group member information is available at the following information level:</span></span>

-   [<span data-ttu-id="6dfcb-142">**Informações de usuários do grupo \_ \_ \_ 0**</span><span class="sxs-lookup"><span data-stu-id="6dfcb-142">**GROUP\_USERS\_INFO\_0**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-group_users_info_0)

<span data-ttu-id="6dfcb-143">Para obter mais informações, consulte funções de [grupo local](local-group-functions.md)de gerenciamento de rede.</span><span class="sxs-lookup"><span data-stu-id="6dfcb-143">For more information, see the network management [Local Group Functions](local-group-functions.md).</span></span>

<span data-ttu-id="6dfcb-144">Se estiver programando para Active Directory, você poderá chamar determinados métodos ADSI (interface do serviço de Active Directory) para obter a mesma funcionalidade que pode obter ao chamar as funções do grupo de gerenciamento de rede.</span><span class="sxs-lookup"><span data-stu-id="6dfcb-144">If you are programming for Active Directory, you may be able to call certain Active Directory Service Interface (ADSI) methods to achieve the same functionality you can achieve by calling the network management group functions.</span></span> <span data-ttu-id="6dfcb-145">Para obter mais informações, consulte [**IADs**](/windows/desktop/api/iads/nn-iads-iadsgroup).</span><span class="sxs-lookup"><span data-stu-id="6dfcb-145">For more information, see [**IADsGroup**](/windows/desktop/api/iads/nn-iads-iadsgroup).</span></span>

 

 