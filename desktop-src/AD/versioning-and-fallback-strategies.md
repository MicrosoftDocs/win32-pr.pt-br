---
title: Estratégias de controle de versão e fallback
description: Quando um aplicativo detecta uma atualização parcial usando uma das técnicas anteriores ou lê um conjunto de objetos cuja data de efetivação ainda não foi atingida, o aplicativo deve lidar com a situação normalmente.
ms.assetid: 6a34a783-98fd-406e-a96d-8e2a09a51c2d
ms.tgt_platform: multiple
keywords:
- ANÚNCIO de estratégias de controle de versão e fallback
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45f6383ad06e73457e18dddfac53295a0c16389c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822249"
---
# <a name="versioning-and-fallback-strategies"></a><span data-ttu-id="cbd11-104">Estratégias de controle de versão e fallback</span><span class="sxs-lookup"><span data-stu-id="cbd11-104">Versioning and Fallback Strategies</span></span>

<span data-ttu-id="cbd11-105">Quando um aplicativo detecta uma atualização parcial usando uma das técnicas anteriores ou lê um conjunto de objetos cuja data de efetivação ainda não foi atingida, o aplicativo deve lidar com a situação normalmente.</span><span class="sxs-lookup"><span data-stu-id="cbd11-105">When an application detects a partial update using one of the preceding techniques or reads a set of objects whose effective date has not yet been reached, the application must deal with the situation gracefully.</span></span> <span data-ttu-id="cbd11-106">Para alguns aplicativos, a resposta normal é "retorne" para uma versão anterior dos objetos em questão.</span><span class="sxs-lookup"><span data-stu-id="cbd11-106">For some applications, the graceful response is to "fall back" to a previous version of the objects in question.</span></span> <span data-ttu-id="cbd11-107">Active Directory Domain Services não fornecem um recurso de controle de versão – os aplicativos que desejam esse recurso devem fornecê-lo por conta própria.</span><span class="sxs-lookup"><span data-stu-id="cbd11-107">Active Directory Domain Services do not provide a versioning facility—applications that want this capability must provide it themselves.</span></span> <span data-ttu-id="cbd11-108">As abordagens para controle de versão incluem manter os valores "última boa conhecida" armazenados em cache localmente e armazenar vários conjuntos de objetos no diretório, por exemplo, nos contêineres "antigo", "atual" e "novo".</span><span class="sxs-lookup"><span data-stu-id="cbd11-108">Approaches to versioning include keeping the "last known good" values cached locally and storing multiple sets of objects in the directory, for example, in "old," "current," and "new" containers.</span></span> <span data-ttu-id="cbd11-109">Muitos outros esquemas são possíveis.</span><span class="sxs-lookup"><span data-stu-id="cbd11-109">Many other schemes are possible.</span></span>

<span data-ttu-id="cbd11-110">As implementações devem tomar cuidado para evitar consequências indesejadas.</span><span class="sxs-lookup"><span data-stu-id="cbd11-110">Implementations must take care to avoid unintended consequences.</span></span> <span data-ttu-id="cbd11-111">Uma versão anterior dos objetos deve ser usada somente quando uma atualização parcial é detectada ou os novos objetos ainda não estão "efetivos".</span><span class="sxs-lookup"><span data-stu-id="cbd11-111">An earlier version of objects should be used only when a partial update is detected or the new objects are not yet "effective."</span></span> <span data-ttu-id="cbd11-112">Fazer fallback porque algo no aplicativo "não funciona" pode burlar a intenção de um administrador.</span><span class="sxs-lookup"><span data-stu-id="cbd11-112">Falling back because something in the application "does not work" might circumvent an administrator's intent.</span></span> <span data-ttu-id="cbd11-113">Por exemplo, dois computadores que antes podiam se comunicar podem não conseguir fazê-lo devido a uma alteração na diretiva de protocolo IPsec.</span><span class="sxs-lookup"><span data-stu-id="cbd11-113">For example, two computers that formerly could communicate might find themselves unable to do so because of a change in Internet Protocol security (IPsec) policy.</span></span> <span data-ttu-id="cbd11-114">Se isso for intencional por parte do administrador, os sistemas afetados não devem retornar à política que permitia a comunicação, pois isso seria uma violação de segurança.</span><span class="sxs-lookup"><span data-stu-id="cbd11-114">If this is intentional on the part of the administrator, the affected systems should not fall back to the policy that allowed them to communicate, as this would be a security breach.</span></span>

 

 




