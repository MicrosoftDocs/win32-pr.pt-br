---
title: Enumerando Membros em um grupo
description: Saiba mais sobre como enumerar Membros em um grupo de Azure Active Directory. Os membros de um grupo são armazenados em um atributo com vários valores chamado membro.
ms.assetid: 28cafdbe-e599-4b1d-a384-264f41d81c79
ms.tgt_platform: multiple
keywords:
- Enumerando Membros em um grupo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 916b988cd26ee4df59eaf27cc5ffd690bca1458a
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407419"
---
# <a name="enumerating-members-in-a-group"></a><span data-ttu-id="da848-105">Enumerando Membros em um grupo</span><span class="sxs-lookup"><span data-stu-id="da848-105">Enumerating Members in a Group</span></span>

<span data-ttu-id="da848-106">Os membros de um grupo são armazenados em um atributo com vários valores chamado **membro**.</span><span class="sxs-lookup"><span data-stu-id="da848-106">The members of a group are stored in a multi-value attribute called **member**.</span></span> <span data-ttu-id="da848-107">Para grupos com uma associação de tamanho pequeno e médio, use o método [**IADs. Members**](/windows/desktop/api/iads/nf-iads-iadsgroup-members) para obter um ponteiro para um objeto [**IADsMembers**](/windows/desktop/api/iads/nn-iads-iadsmembers) que contém a lista de todos os membros.</span><span class="sxs-lookup"><span data-stu-id="da848-107">For groups with a small to medium-sized membership, use the [**IADsGroup.Members**](/windows/desktop/api/iads/nf-iads-iadsgroup-members) method to get a pointer to an [**IADsMembers**](/windows/desktop/api/iads/nn-iads-iadsmembers) object that contains the list of all members.</span></span> <span data-ttu-id="da848-108">Em seguida, use o [**IADsMembers:: get \_ \_ NewEnum**](/windows/desktop/api/iads/nf-iads-iadsmembers-get__newenum) para obter um objeto Enumerator que você pode usar para enumerar os membros.</span><span class="sxs-lookup"><span data-stu-id="da848-108">Then use the [**IADsMembers::get\_\_NewEnum**](/windows/desktop/api/iads/nf-iads-iadsmembers-get__newenum) to get an enumerator object that you can use to enumerate the members.</span></span>

<span data-ttu-id="da848-109">Se a associação de grupo prevista for 1000 ou mais membros, use a variação para recuperar os usuários um intervalo por vez.</span><span class="sxs-lookup"><span data-stu-id="da848-109">If the anticipated group membership will be 1000 or more members, use ranging to retrieve users one range at a time.</span></span> <span data-ttu-id="da848-110">Para obter mais informações sobre como usar variando para enumerar Membros, consulte [enumerando grupos que contêm muitos membros](enumerating-groups-that-contain-many-members.md).</span><span class="sxs-lookup"><span data-stu-id="da848-110">For more information about using ranging to enumerate members, see [Enumerating Groups That Contain Many Members](enumerating-groups-that-contain-many-members.md).</span></span>

 

 