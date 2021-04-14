---
title: Localidade temporal
description: A localidade temporal é uma estratégia de prevenção que reduz a janela para atualizações parciais.
ms.assetid: 8f454087-46cb-4fa6-b83a-65b2393029c3
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ceecff05d031875178b6192e7c633f70e4c91c50
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104453494"
---
# <a name="temporal-locality"></a><span data-ttu-id="0e348-103">Localidade temporal</span><span class="sxs-lookup"><span data-stu-id="0e348-103">Temporal Locality</span></span>

<span data-ttu-id="0e348-104">A *localidade temporal* é uma estratégia de prevenção que reduz a janela para atualizações parciais.</span><span class="sxs-lookup"><span data-stu-id="0e348-104">*Temporal locality* is an avoidance strategy that reduces the window for partial updates.</span></span> <span data-ttu-id="0e348-105">A replicação de alterações de uma determinada réplica de origem prossegue em ordem crescente de USN.</span><span class="sxs-lookup"><span data-stu-id="0e348-105">Replication of changes from a given source replica proceeds in ascending USN order.</span></span> <span data-ttu-id="0e348-106">As gravações que ocorrem em conjunto junto no tempo terão USNs que estão "perto" entre si e serão propagadas junto em tempo.</span><span class="sxs-lookup"><span data-stu-id="0e348-106">Writes that occur close together in time will have USNs that are "near" each other, and will be propagated close together in time.</span></span> <span data-ttu-id="0e348-107">Os aplicativos que criam ou atualizam vários objetos relacionados devem gravar os objetos o mais próximo possível do tempo possível.</span><span class="sxs-lookup"><span data-stu-id="0e348-107">Applications that create or update multiple, related objects should write the objects as close together in time as possible.</span></span> <span data-ttu-id="0e348-108">Por exemplo, o aplicativo pode reunir toda a entrada necessária do usuário e aplicá-la ao diretório quando o usuário clicar em um botão "aplicar".</span><span class="sxs-lookup"><span data-stu-id="0e348-108">For example, the application could gather all necessary input from the user and apply it to the directory when the user clicks an "Apply" button.</span></span>

<span data-ttu-id="0e348-109">A localidade temporal também reduz as chances de resolução de colisão introduzindo inconsistências dentro do objeto.</span><span class="sxs-lookup"><span data-stu-id="0e348-109">Temporal locality also reduces the odds of collision resolution introducing intra-object inconsistencies.</span></span>

 

 




