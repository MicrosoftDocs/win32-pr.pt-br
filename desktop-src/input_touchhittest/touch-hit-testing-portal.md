---
title: Teste de colisão de toque
description: Os tópicos desta seção fornecem uma visão geral do suporte para teste de colisão de toque no Windows 8.
ms.assetid: bdd7630c-b2d8-4080-a149-efec018f697d
keywords:
- interação do usuário
- input
- ponteiro
- touch
ms.topic: article
ms.date: 02/07/2020
ms.openlocfilehash: 8cf6d28badb47a176a6feccf166344003faf1de8
ms.sourcegitcommit: 9e389b8e39616dcef8f7ff4bc53d945179401478
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/07/2020
ms.locfileid: "103823545"
---
# <a name="touch-hit-testing"></a><span data-ttu-id="d0bea-107">Teste de colisão de toque</span><span class="sxs-lookup"><span data-stu-id="d0bea-107">Touch Hit Testing</span></span>

## <a name="purpose"></a><span data-ttu-id="d0bea-108">Finalidade</span><span class="sxs-lookup"><span data-stu-id="d0bea-108">Purpose</span></span>

<span data-ttu-id="d0bea-109">Os tópicos desta seção fornecem uma visão geral do suporte para teste de colisão de toque no Windows.</span><span class="sxs-lookup"><span data-stu-id="d0bea-109">The topics in this section provide an overview of support for Touch Hit Testing in Windows.</span></span> <span data-ttu-id="d0bea-110">O teste de colisão de toque permite identificar um destino de entrada com base em se a área de conteúdo de um elemento de interface do usuário está dentro da área de contato ou inclui o ponto de contato.</span><span class="sxs-lookup"><span data-stu-id="d0bea-110">Touch Hit Testing lets you identify an input target based on whether the content area of a UI element falls within the contact area or includes the contact point.</span></span>

<span data-ttu-id="d0bea-111">O teste de colisão de toque usa geometria de contato complexa para toda a área de toque em vez de uma única coordenada x-y interpolada.</span><span class="sxs-lookup"><span data-stu-id="d0bea-111">Touch hit testing uses complex contact geometry for the entire touch area rather than a single interpolated x-y coordinate.</span></span> <span data-ttu-id="d0bea-112">O uso de toda a geometria de contato melhora muito a precisão e a precisão quando você está identificando o destino mais provável de entrada por toque.</span><span class="sxs-lookup"><span data-stu-id="d0bea-112">Using the entire contact geometry greatly improves precision and accuracy when you're identifying the most likely target of touch input.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="d0bea-113">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="d0bea-113">In this section</span></span>

| <span data-ttu-id="d0bea-114">Tópico</span><span class="sxs-lookup"><span data-stu-id="d0bea-114">Topic</span></span> | <span data-ttu-id="d0bea-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="d0bea-115">Description</span></span> |
| --- | --- |
| [<span data-ttu-id="d0bea-116">Referência de teste de colisão de toque</span><span class="sxs-lookup"><span data-stu-id="d0bea-116">Touch Hit Testing Reference</span></span>](touchhittest-reference.md)<br/> | <span data-ttu-id="d0bea-117">Os tópicos nesta seção fornecem as especificações de referência para [teste de colisão de toque](touch-hit-testing-portal.md).</span><span class="sxs-lookup"><span data-stu-id="d0bea-117">The topics in this section provide the reference specifications for [Touch Hit Testing](touch-hit-testing-portal.md).</span></span><br/> |

## <a name="developer-audience"></a><span data-ttu-id="d0bea-118">Público de desenvolvedores</span><span class="sxs-lookup"><span data-stu-id="d0bea-118">Developer audience</span></span>

<span data-ttu-id="d0bea-119">As APIs de teste de colisão de toque são projetadas para os desenvolvedores que estão criando estruturas de interface do usuário que fornecem uma experiência de usuários consistente e otimizada para toque em aplicativos de área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="d0bea-119">The Touch Hit Testing APIs are designed for developers who are building UI frameworks that provide a consistent touch-optimized user experience across desktop applications.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d0bea-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d0bea-120">Related topics</span></span>

[<span data-ttu-id="d0bea-121">Interação do usuário</span><span class="sxs-lookup"><span data-stu-id="d0bea-121">User Interaction</span></span>](../user-interaction.md)
