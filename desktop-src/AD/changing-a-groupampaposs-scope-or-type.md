---
title: Alterando o escopo ou tipo de um grupo
description: Este tópico mostra como alterar o escopo ou o tipo de um grupo em domínios de modo nativo.
ms.assetid: bdae7bc9-072a-4063-9562-8e0fcb1b7937
ms.tgt_platform: multiple
keywords:
- grupos de anúncios, alterando o escopo ou tipo de um grupo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f65c64b4a2dafe4bf6c0e65463ef16e0270c0be3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103634804"
---
# <a name="changing-a-groups-scope-or-type"></a><span data-ttu-id="28886-104">Alterando o escopo ou tipo de um grupo</span><span class="sxs-lookup"><span data-stu-id="28886-104">Changing a Group's Scope or Type</span></span>

<span data-ttu-id="28886-105">A alteração de um escopo ou tipo de grupo não é permitida em domínios de modo misto.</span><span class="sxs-lookup"><span data-stu-id="28886-105">Changing a group scope or type is not allowed in mixed-mode domains.</span></span> <span data-ttu-id="28886-106">No entanto, as seguintes conversões são permitidas em domínios de modo nativo:</span><span class="sxs-lookup"><span data-stu-id="28886-106">However, the following conversions are allowed in native-mode domains:</span></span>

<span data-ttu-id="28886-107">Grupo global para grupo universal: isso só será permitido se o grupo global não for membro de outro grupo global.</span><span class="sxs-lookup"><span data-stu-id="28886-107">Global group to universal group: This is only allowed if the global group is not a member of another global group.</span></span>

<span data-ttu-id="28886-108">Grupo de domínio local para grupo universal: o grupo local de domínio que está sendo convertido não pode conter outro grupo de domínio local.</span><span class="sxs-lookup"><span data-stu-id="28886-108">Domain local group to universal group: The domain local group being converted cannot contain another domain local group.</span></span>

<span data-ttu-id="28886-109">Grupo universal para grupo local global ou de domínio: para conversão para grupo global, o grupo universal que está sendo convertido não pode conter usuários ou grupos globais de outro domínio.</span><span class="sxs-lookup"><span data-stu-id="28886-109">Universal group to global or domain local group: For conversion to global group, the universal group being converted cannot contain users or global groups from another domain.</span></span> <span data-ttu-id="28886-110">Para conversão para grupo de domínio local, o grupo universal que está sendo convertido não pode ser membro de um grupo universal ou de um grupo de domínio local de outro domínio.</span><span class="sxs-lookup"><span data-stu-id="28886-110">For conversion to domain local group, the universal group being converted cannot be a member of any universal group or a domain local group from another domain.</span></span>

<span data-ttu-id="28886-111">No modo nativo, um tipo de grupo pode ser convertido livremente entre grupos de segurança e grupos de distribuição.</span><span class="sxs-lookup"><span data-stu-id="28886-111">In native mode, a group type can be converted freely between security groups and distribution groups.</span></span>

<span data-ttu-id="28886-112">Lembre-se de que, se um grupo for usado para definir o controle de acesso, alterar o escopo ou o tipo poderá afetar as ACEs (entradas de controle de acesso) que contêm esse grupo.</span><span class="sxs-lookup"><span data-stu-id="28886-112">Be aware that if a group is used to set access control, changing the scope or type can affect the access control entries (ACEs) that contain that group.</span></span> <span data-ttu-id="28886-113">O sistema de segurança irá ignorar ACEs que contêm grupos que não são grupos de segurança.</span><span class="sxs-lookup"><span data-stu-id="28886-113">The security system will ignore ACEs that contain groups that are not security groups.</span></span>

 

 




