---
title: Métodos (IManipulationProcessor)
description: Esta seção contém os métodos para a interface IManipulationProcessor.
ms.assetid: 33736f79-cb61-449c-80b9-1358db2621e9
keywords:
- Windows Touch, interface IManipulationProcessor
- Windows Touch, métodos de interface
- manipulações, interface IManipulationProcessor
- Interface IManipulationProcessor, métodos
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 995a848e18b8308d46ceda717bf7eec291953505
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104369131"
---
# <a name="methods-imanipulationprocessor"></a><span data-ttu-id="43611-107">Métodos (IManipulationProcessor)</span><span class="sxs-lookup"><span data-stu-id="43611-107">Methods (IManipulationProcessor)</span></span>

<span data-ttu-id="43611-108">Esta seção contém os métodos para a interface [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) .</span><span class="sxs-lookup"><span data-stu-id="43611-108">This section contains the methods for the [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) interface.</span></span>

<span data-ttu-id="43611-109">Os métodos a seguir são expostos pela interface [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) .</span><span class="sxs-lookup"><span data-stu-id="43611-109">The following methods are exposed by the [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) interface.</span></span>



| <span data-ttu-id="43611-110">Método</span><span class="sxs-lookup"><span data-stu-id="43611-110">Method</span></span>                                                                      | <span data-ttu-id="43611-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="43611-111">Description</span></span>                                                                              |
|-----------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [<span data-ttu-id="43611-112">**CompleteManipulation**</span><span class="sxs-lookup"><span data-stu-id="43611-112">**CompleteManipulation**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-completemanipulation) | <span data-ttu-id="43611-113">Esse método é chamado quando o desenvolvedor opta por encerrar a manipulação.</span><span class="sxs-lookup"><span data-stu-id="43611-113">This method is called when the developer chooses to end the manipulation.</span></span>                |
| [<span data-ttu-id="43611-114">**GetAngularVelocity**</span><span class="sxs-lookup"><span data-stu-id="43611-114">**GetAngularVelocity**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-getangularvelocity)     | <span data-ttu-id="43611-115">Calcula a velocidade rotacional que o objeto de destino está movendo.</span><span class="sxs-lookup"><span data-stu-id="43611-115">Calculates the rotational velocity that the target object is moving at.</span></span>                  |
| [<span data-ttu-id="43611-116">**GetExpansionVelocity**</span><span class="sxs-lookup"><span data-stu-id="43611-116">**GetExpansionVelocity**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-getexpansionvelocity) | <span data-ttu-id="43611-117">Calcula a taxa em que o objeto de destino está expandindo.</span><span class="sxs-lookup"><span data-stu-id="43611-117">Calculates the rate that the target object is expanding at.</span></span>                              |
| [<span data-ttu-id="43611-118">**GetVelocityX**</span><span class="sxs-lookup"><span data-stu-id="43611-118">**GetVelocityX**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-getvelocityx)                 | <span data-ttu-id="43611-119">Calcula e retorna a velocidade horizontal para o objeto de destino.</span><span class="sxs-lookup"><span data-stu-id="43611-119">Calculates and returns the horizontal velocity for the target object.</span></span>                    |
| [<span data-ttu-id="43611-120">**Getvelocityy**</span><span class="sxs-lookup"><span data-stu-id="43611-120">**GetVelocityY**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-getvelocityy)                 | <span data-ttu-id="43611-121">Calcula e retorna a velocidade vertical.</span><span class="sxs-lookup"><span data-stu-id="43611-121">Calculates and returns the vertical velocity.</span></span>                                            |
| [<span data-ttu-id="43611-122">**ProcessDown**</span><span class="sxs-lookup"><span data-stu-id="43611-122">**ProcessDown**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processdown)                   | <span data-ttu-id="43611-123">Alimenta dados para o processador de manipulação associado a um destino.</span><span class="sxs-lookup"><span data-stu-id="43611-123">Feeds data to the manipulation processor associated with a target.</span></span>                       |
| [<span data-ttu-id="43611-124">**ProcessMove**</span><span class="sxs-lookup"><span data-stu-id="43611-124">**ProcessMove**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processmove)                   | <span data-ttu-id="43611-125">Alimenta dados para o processador de manipulação associado a um destino.</span><span class="sxs-lookup"><span data-stu-id="43611-125">Feeds data to the manipulation processor associated with a target.</span></span>                       |
| [<span data-ttu-id="43611-126">**ProcessUp**</span><span class="sxs-lookup"><span data-stu-id="43611-126">**ProcessUp**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processup)                       | <span data-ttu-id="43611-127">Alimenta dados para o processador de manipulação associado a um destino.</span><span class="sxs-lookup"><span data-stu-id="43611-127">Feeds data to the manipulation processor associated with a target.</span></span>                       |
| [<span data-ttu-id="43611-128">**ProcessDownWithTime**</span><span class="sxs-lookup"><span data-stu-id="43611-128">**ProcessDownWithTime**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processdownwithtime)   | <span data-ttu-id="43611-129">Alimenta dados, incluindo um carimbo de data/hora para o processador de manipulação associado a um destino.</span><span class="sxs-lookup"><span data-stu-id="43611-129">Feeds data including a timestamp to the manipulation processor associated with a target.</span></span> |
| [<span data-ttu-id="43611-130">**ProcessMoveWithTime**</span><span class="sxs-lookup"><span data-stu-id="43611-130">**ProcessMoveWithTime**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processmovewithtime)   | <span data-ttu-id="43611-131">Alimenta dados, incluindo um carimbo de data/hora para o processador de manipulação associado a um destino.</span><span class="sxs-lookup"><span data-stu-id="43611-131">Feeds data including a timestamp to the manipulation processor associated with a target.</span></span> |
| [<span data-ttu-id="43611-132">**ProcessUpWithTime**</span><span class="sxs-lookup"><span data-stu-id="43611-132">**ProcessUpWithTime**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processupwithtime)       | <span data-ttu-id="43611-133">Alimenta dados, incluindo um carimbo de data/hora para o processador de manipulação associado a um destino.</span><span class="sxs-lookup"><span data-stu-id="43611-133">Feeds data including a timestamp to the manipulation processor associated with a target.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="43611-134">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="43611-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="43611-135">**IManipulationProcessor**</span><span class="sxs-lookup"><span data-stu-id="43611-135">**IManipulationProcessor**</span></span>](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor)
</dt> </dl>

 

 




