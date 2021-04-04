---
title: Determinando a associação de um usuário ou grupo em um grupo
description: O método IADs. IsMember pode ser usado para determinar se um objeto é membro de um grupo.
ms.assetid: c7168781-4ae4-4ce3-8d8a-2eefc7def62b
ms.tgt_platform: multiple
keywords:
- Determinando a associação de um usuário ou grupo em um AD do grupo
- grupos de anúncios, determinando a associação de um usuário ou grupo em um grupo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b520146079fdfaa5fa1adc99975b3b25d2e78c05
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104007327"
---
# <a name="determining-a-users-or-groups-membership-in-a-group"></a><span data-ttu-id="009bb-105">Determinando a associação de um usuário ou grupo em um grupo</span><span class="sxs-lookup"><span data-stu-id="009bb-105">Determining a User's or Group's Membership in a Group</span></span>

<span data-ttu-id="009bb-106">O método [**IADs. IsMember**](/windows/desktop/api/iads/nf-iads-iadsgroup-ismember) pode ser usado para determinar se um objeto é membro de um grupo.</span><span class="sxs-lookup"><span data-stu-id="009bb-106">The [**IADsGroup.IsMember**](/windows/desktop/api/iads/nf-iads-iadsgroup-ismember) method can be used to determine if an object is a member of a group.</span></span> <span data-ttu-id="009bb-107">Esse método retornará **true** se o objeto especificado for um membro direto do grupo, ou seja, a propriedade de membro do grupo contiver o objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="009bb-107">This method returns **TRUE** if the specified object is a direct member of the group, that is, the group's member property contains the specified object.</span></span>

<span data-ttu-id="009bb-108">Um grupo pode conter outros grupos.</span><span class="sxs-lookup"><span data-stu-id="009bb-108">A group can contain other groups.</span></span> <span data-ttu-id="009bb-109">O método [**IADs. IsMember**](/windows/desktop/api/iads/nf-iads-iadsgroup-ismember) não verifica recursivamente os membros dos grupos em sua Propriedade Member, os grupos dentro desses grupos e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="009bb-109">The [**IADsGroup.IsMember**](/windows/desktop/api/iads/nf-iads-iadsgroup-ismember) method does not recursively verify the members of groups in its member property, groups within those groups, and so on.</span></span> <span data-ttu-id="009bb-110">Para verificar recursivamente se um objeto é membro de um grupo, enumere os grupos na Propriedade do membro, verifique os membros desses grupos para ver se o objeto é um membro e se esses grupos contêm outros grupos, verifique seus membros e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="009bb-110">To recursively verify that an object is a member of a group, enumerate the groups in the member property, verify the members of those groups to see if the object is a member, and if those groups contain other groups, check their members, and so on.</span></span>

> [!Note]  
> <span data-ttu-id="009bb-111">Como os grupos podem ser aninhados, a associação de grupo pode ter loops.</span><span class="sxs-lookup"><span data-stu-id="009bb-111">Since groups can be nested, group membership may have loops.</span></span> <span data-ttu-id="009bb-112">Qualquer script que enumere muitos grupos deve manter uma lista interna de grupos para encerrar a recursão se um grupo já tiver sido visitado.</span><span class="sxs-lookup"><span data-stu-id="009bb-112">Any script that enumerates over many groups should keep an internal list of groups to end recursion if a group has already been visited.</span></span>

 

 

 