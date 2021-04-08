---
title: Aninhamento no modo nativo
description: A lista a seguir descreve o que pode estar contido em um grupo que existe em um domínio de modo nativo.
ms.assetid: 7992ef2d-9dcf-4087-b09a-35235b23e499
ms.tgt_platform: multiple
keywords:
- Aninhamento no AD no modo nativo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69dba115bb705fe706a049e85136475c6d5b3a16
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822259"
---
# <a name="nesting-in-native-mode"></a><span data-ttu-id="0712b-104">Aninhamento no modo nativo</span><span class="sxs-lookup"><span data-stu-id="0712b-104">Nesting in Native Mode</span></span>

<span data-ttu-id="0712b-105">A lista a seguir descreve o que pode estar contido em um grupo que existe em um domínio de modo nativo.</span><span class="sxs-lookup"><span data-stu-id="0712b-105">The following list describes what can be contained in a group that exists in a native-mode domain.</span></span> <span data-ttu-id="0712b-106">Essa mesma lista também se aplica a grupos de distribuição em domínios de modo misto.</span><span class="sxs-lookup"><span data-stu-id="0712b-106">This same list also applies to distribution groups in mixed-mode domains.</span></span> <span data-ttu-id="0712b-107">O escopo do grupo determina essas regras de confinamento.</span><span class="sxs-lookup"><span data-stu-id="0712b-107">The scope of the group determines these containment rules.</span></span>

-   <span data-ttu-id="0712b-108">Um grupo universal pode conter outros grupos universais, grupos globais e contas de qualquer domínio dentro da floresta em que esse grupo universal reside.</span><span class="sxs-lookup"><span data-stu-id="0712b-108">A universal group can contain other universal groups, global groups and accounts from any domain within the forest in which this Universal Group resides.</span></span>
-   <span data-ttu-id="0712b-109">Um grupo global pode conter outros grupos globais e contas do mesmo domínio ao qual o grupo pertence.</span><span class="sxs-lookup"><span data-stu-id="0712b-109">A global group can contain other global groups and accounts from the same domain that the group belongs to.</span></span> <span data-ttu-id="0712b-110">Um grupo global não pode conter grupos universais ou qualquer conta ou grupo global de outro domínio.</span><span class="sxs-lookup"><span data-stu-id="0712b-110">A global group cannot contain any universal groups, or any global group or account from another domain.</span></span>
-   <span data-ttu-id="0712b-111">Um grupo de domínio local pode conter grupos universais, grupos globais e contas de qualquer domínio ou floresta.</span><span class="sxs-lookup"><span data-stu-id="0712b-111">A domain local group can contain universal groups, global groups and accounts from any domain or forest.</span></span> <span data-ttu-id="0712b-112">Um grupo de domínio local também pode conter outros grupos locais de domínio do mesmo domínio ao qual o grupo pertence.</span><span class="sxs-lookup"><span data-stu-id="0712b-112">A domain local group can also contain other domain local groups from the same domain that the group belongs to.</span></span> <span data-ttu-id="0712b-113">Um grupo de domínio local não pode conter outros grupos locais de domínio de qualquer outro domínio ou floresta.</span><span class="sxs-lookup"><span data-stu-id="0712b-113">A domain local group cannot contain other domain local groups from any other domain or forest.</span></span>

 

 




