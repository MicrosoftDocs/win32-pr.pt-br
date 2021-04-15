---
title: O que você pode saber e quando você pode conhecê-lo
description: Os aplicativos que são sensíveis a Estados induzidos por latência devem reconhecer Estados de problemas e tomar as devidas ações.
ms.assetid: d1d0135e-2d67-47dd-82ac-4869203ce85e
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e9a8a6c6def8475946ad5faa63615d17742fbcb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105753665"
---
# <a name="what-can-you-know-and-when-can-you-know-it"></a><span data-ttu-id="315f3-103">O que você pode saber e quando você pode conhecê-lo?</span><span class="sxs-lookup"><span data-stu-id="315f3-103">What Can You Know, and When Can You Know It?</span></span>

<span data-ttu-id="315f3-104">Os aplicativos que são sensíveis a Estados induzidos por latência devem reconhecer Estados de problemas e tomar as devidas ações.</span><span class="sxs-lookup"><span data-stu-id="315f3-104">Applications that are sensitive to latency-induced states must recognize problem states and take appropriate action.</span></span> <span data-ttu-id="315f3-105">Há dois Estados de problema: distorção de versão e atualização parcial.</span><span class="sxs-lookup"><span data-stu-id="315f3-105">There are two problem states: version skew and partial update.</span></span> <span data-ttu-id="315f3-106">A distorção de versão não é detectável examinando o serviço de diretório (Lembre-se do axioma de computação distribuída declarado em [por que Active Directory Domain Services usar esse modelo de replicação](why-active-directory-domain-services-uses-this-replication-model.md)).</span><span class="sxs-lookup"><span data-stu-id="315f3-106">Version skew is not detectable by examining the Directory Service (remember the axiom of distributed computing stated in [Why Active Directory Domain Services Use This Replication Model](why-active-directory-domain-services-uses-this-replication-model.md)).</span></span> <span data-ttu-id="315f3-107">A atualização parcial pode ser detectada adicionando metadados aos objetos que compõem o conjunto relacionado.</span><span class="sxs-lookup"><span data-stu-id="315f3-107">Partial update can be detected by adding metadata to the objects that compose the related set.</span></span> <span data-ttu-id="315f3-108">As sugestões para esses metadados aparecem nas seções subsequentes deste documento.</span><span class="sxs-lookup"><span data-stu-id="315f3-108">Suggestions for such metadata appear in subsequent sections of this document.</span></span> <span data-ttu-id="315f3-109">Há estratégias de prevenção que os aplicativos podem tomar para reduzir a possibilidade de distorção de versão e atualização parcial.</span><span class="sxs-lookup"><span data-stu-id="315f3-109">There are avoidance strategies applications can take to reduce the possibility of both version skew and partial update.</span></span> <span data-ttu-id="315f3-110">Essas estratégias também são discutidas nas seções subsequentes deste documento.</span><span class="sxs-lookup"><span data-stu-id="315f3-110">These strategies are also discussed in subsequent sections of this document.</span></span>

 

 




