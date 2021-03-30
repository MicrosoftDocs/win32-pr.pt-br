---
title: Removendo membros de grupos em um domínio
description: Você pode remover usuários, grupos ou contatos de grupos.
ms.assetid: 036f2882-7da9-4293-87a0-a087235b212f
ms.tgt_platform: multiple
keywords:
- grupos de anúncios, removendo membros de grupos em um domínio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ab7600d98e75447c55fd84d783ff5263fc63bde
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "103640386"
---
# <a name="removing-members-from-groups-in-a-domain"></a><span data-ttu-id="98235-104">Removendo membros de grupos em um domínio</span><span class="sxs-lookup"><span data-stu-id="98235-104">Removing Members from Groups in a Domain</span></span>

<span data-ttu-id="98235-105">Você pode remover usuários, grupos ou contatos de grupos.</span><span class="sxs-lookup"><span data-stu-id="98235-105">You can remove users, groups, or contacts from groups.</span></span> <span data-ttu-id="98235-106">O atributo **Member** do objeto **Group** contém todos os membros diretos do grupo.</span><span class="sxs-lookup"><span data-stu-id="98235-106">The **member** attribute of the **group** object contains all direct members of the group.</span></span>

<span data-ttu-id="98235-107">A maneira mais simples de remover um membro de um grupo é chamar o método [**IADs. Remove**](/windows/desktop/api/iads/nf-iads-iadsgroup-remove) na interface [**IADs**](/windows/desktop/api/iads/nn-iads-iadsgroup) do objeto de grupo do qual você deseja remover membros.</span><span class="sxs-lookup"><span data-stu-id="98235-107">The simplest way to remove a member from a group is to call the [**IADsGroup.Remove**](/windows/desktop/api/iads/nf-iads-iadsgroup-remove) method on the [**IADsGroup**](/windows/desktop/api/iads/nn-iads-iadsgroup) interface of the group object you want to remove members from.</span></span>

 

 