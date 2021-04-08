---
description: Parâmetros de mídia
ms.assetid: 48b2bc2e-897d-4aa9-8a50-c2855a17dca5
title: Parâmetros de mídia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce9276a3d38b9176458299bfd1a47057cac6236e
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "103837616"
---
# <a name="media-parameters"></a><span data-ttu-id="d7e67-103">Parâmetros de mídia</span><span class="sxs-lookup"><span data-stu-id="d7e67-103">Media Parameters</span></span>

<span data-ttu-id="d7e67-104">Os parâmetros de mídia permitem que um aplicativo configure as propriedades de um objeto de forma que elas sejam alteradas com o passar do tempo de forma matematicamente determinística.</span><span class="sxs-lookup"><span data-stu-id="d7e67-104">Media parameters enable an application to configure an object's properties so that they change over time in a mathematically deterministic way.</span></span>

<span data-ttu-id="d7e67-105">Por exemplo, suponha que um engenheiro de som esteja misturando uma fita mestre digital e queira aplicar um pequeno atraso a uma seção vocal para preencher o som.</span><span class="sxs-lookup"><span data-stu-id="d7e67-105">For example, suppose that a sound engineer is mixing a digital master tape and wants to apply a slight delay to a vocal section, to fill out the sound.</span></span> <span data-ttu-id="d7e67-106">O efeito será dissonante se o atraso for recortado abruptamente.</span><span class="sxs-lookup"><span data-stu-id="d7e67-106">The effect will be jarring if the delay cuts in abruptly.</span></span> <span data-ttu-id="d7e67-107">Em vez disso, o efeito deve começar de 100% seco (sem atraso) e a mistura úmida/seca deve aumentar gradualmente até atingir o nível desejado.</span><span class="sxs-lookup"><span data-stu-id="d7e67-107">Instead, the effect should begin 100 percent dry (no delay), and the wet/dry mix should increase gradually until it reaches the desired level.</span></span> <span data-ttu-id="d7e67-108">Além disso, essa transição deve seguir uma curva suave ou uma progressão linear.</span><span class="sxs-lookup"><span data-stu-id="d7e67-108">Moreover, this transition should follow a smooth curve or linear progression.</span></span> <span data-ttu-id="d7e67-109">Para dar suporte a esse cenário, um DMO pode expor as seguintes interfaces:</span><span class="sxs-lookup"><span data-stu-id="d7e67-109">To support this scenario, a DMO can expose the following interfaces:</span></span>

-   <span data-ttu-id="d7e67-110">[**IMediaParamInfo**](/previous-versions/windows/desktop/api/Medparam/nn-medparam-imediaparaminfo) contém métodos para descobrir informações sobre as propriedades com suporte.</span><span class="sxs-lookup"><span data-stu-id="d7e67-110">[**IMediaParamInfo**](/previous-versions/windows/desktop/api/Medparam/nn-medparam-imediaparaminfo) contains methods for discovering information about the supported properties.</span></span> <span data-ttu-id="d7e67-111">Normalmente, o cliente chamará esses métodos antes de começar a transmitir dados.</span><span class="sxs-lookup"><span data-stu-id="d7e67-111">Typically, the client will call these methods before it begins to stream data.</span></span>
-   <span data-ttu-id="d7e67-112">[**IMediaParams**](/previous-versions/windows/desktop/api/Medparam/nn-medparam-imediaparams) contêm métodos para definir as curvas que um parâmetro seguirá durante o streaming.</span><span class="sxs-lookup"><span data-stu-id="d7e67-112">[**IMediaParams**](/previous-versions/windows/desktop/api/Medparam/nn-medparam-imediaparams) contain methods for setting the curves that a parameter will follow during streaming.</span></span>

<span data-ttu-id="d7e67-113">Essas interfaces são projetadas principalmente para DMOs, mas qualquer objeto pode dar suporte a elas.</span><span class="sxs-lookup"><span data-stu-id="d7e67-113">These interfaces are designed primarily for DMOs, but any object can support them.</span></span> <span data-ttu-id="d7e67-114">Nesta seção, o *parâmetro* Term refere-se a qualquer propriedade que ofereça suporte a essas duas interfaces.</span><span class="sxs-lookup"><span data-stu-id="d7e67-114">Within this section, the term *parameter* refers to any property that supports these two interfaces.</span></span>

<span data-ttu-id="d7e67-115">Esta seção contém os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="d7e67-115">This section contains the following topics:</span></span>

-   [<span data-ttu-id="d7e67-116">Curvas de parâmetro</span><span class="sxs-lookup"><span data-stu-id="d7e67-116">Parameter Curves</span></span>](parameter-curves.md)
-   [<span data-ttu-id="d7e67-117">Informações de parâmetro</span><span class="sxs-lookup"><span data-stu-id="d7e67-117">Parameter Information</span></span>](parameter-information.md)
-   [<span data-ttu-id="d7e67-118">Segmentos de envelope</span><span class="sxs-lookup"><span data-stu-id="d7e67-118">Envelope Segments</span></span>](envelope-segments.md)
-   [<span data-ttu-id="d7e67-119">Calculando valores de parâmetro</span><span class="sxs-lookup"><span data-stu-id="d7e67-119">Calculating Parameter Values</span></span>](calculating-parameter-values.md)

## <a name="related-topics"></a><span data-ttu-id="d7e67-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d7e67-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d7e67-121">Objetos de mídia do DirectX</span><span class="sxs-lookup"><span data-stu-id="d7e67-121">DirectX Media Objects</span></span>](directx-media-objects.md)
</dt> </dl>

 

 



