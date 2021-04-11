---
title: Enumerações de contexto de interação
description: Os tópicos nesta seção fornecem as especificações de referência para enumerações de contexto de interação.
ms.assetid: 0B8D9A5F-F7CF-42B0-A320-77D44445CC24
keywords:
- interação do usuário
- input
- ponteiro
- touch
- mouse
- caneta
- caneta
ms.topic: article
ms.date: 02/06/2020
ms.openlocfilehash: cebab2a0b7879d0dff71704cb808c42155484408
ms.sourcegitcommit: 6b8d5058d02daacad4d2ed7830da63b63a509586
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/07/2020
ms.locfileid: "104084329"
---
# <a name="interaction-context-enumerations"></a><span data-ttu-id="87f18-110">Enumerações de contexto de interação</span><span class="sxs-lookup"><span data-stu-id="87f18-110">Interaction Context Enumerations</span></span>

<span data-ttu-id="87f18-111">Os tópicos nesta seção fornecem as especificações de referência para enumerações de [contexto de interação](interaction-context-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="87f18-111">The topics in this section provide the reference specifications for [Interaction Context](interaction-context-portal.md) enumerations.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="87f18-112">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="87f18-112">In this section</span></span>

| <span data-ttu-id="87f18-113">Tópico</span><span class="sxs-lookup"><span data-stu-id="87f18-113">Topic</span></span> | <span data-ttu-id="87f18-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="87f18-114">Description</span></span> |
|---|---|
| [<span data-ttu-id="87f18-115">**\_sinalizadores de slide cruzado \_**</span><span class="sxs-lookup"><span data-stu-id="87f18-115">**CROSS\_SLIDE\_FLAGS**</span></span>](/windows/win32/api/interactioncontext/ne-interactioncontext-cross_slide_flags)<br/> | <span data-ttu-id="87f18-116">Especifica o estado da interação entre slides.</span><span class="sxs-lookup"><span data-stu-id="87f18-116">Specifies the state of the cross-slide interaction.</span></span><br/> |
| [<span data-ttu-id="87f18-117">**\_limite de slide cruzado \_**</span><span class="sxs-lookup"><span data-stu-id="87f18-117">**CROSS\_SLIDE\_THRESHOLD**</span></span>](/windows/win32/api/interactioncontext/ne-interactioncontext-cross_slide_threshold)<br/> | <span data-ttu-id="87f18-118">Especifica os limites de comportamento entre slides.</span><span class="sxs-lookup"><span data-stu-id="87f18-118">Specifies the cross-slide behavior thresholds.</span></span><br/> |
| [<span data-ttu-id="87f18-119">**\_parâmetro inércia**</span><span class="sxs-lookup"><span data-stu-id="87f18-119">**INERTIA\_PARAMETER**</span></span>](/windows/win32/api/interactioncontext/ne-interactioncontext-inertia_parameter)<br/> | <span data-ttu-id="87f18-120">Especifica os valores de inércia para uma manipulação (translação, rotação, dimensionamento).</span><span class="sxs-lookup"><span data-stu-id="87f18-120">Specifies the inertia values for a manipulation (translation, rotation, scaling).</span></span><br/> |
| [<span data-ttu-id="87f18-121">**\_sinalizadores de configuração de interação \_**</span><span class="sxs-lookup"><span data-stu-id="87f18-121">**INTERACTION\_CONFIGURATION\_FLAGS**</span></span>](/windows/win32/api/interactioncontext/ne-interactioncontext-interaction_configuration_flags)<br/> | <span data-ttu-id="87f18-122">Especifica as interações a serem habilitadas ao configurar um objeto de [contexto de interação](interaction-context-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="87f18-122">Specifies the interactions to enable when configuring an [Interaction Context](interaction-context-portal.md) object.</span></span><br/> |
| [<span data-ttu-id="87f18-123">**\_propriedade de contexto de interação \_**</span><span class="sxs-lookup"><span data-stu-id="87f18-123">**INTERACTION\_CONTEXT\_PROPERTY**</span></span>](/windows/win32/api/interactioncontext/ne-interactioncontext-interaction_context_property)<br/> | <span data-ttu-id="87f18-124">Especifica as propriedades do objeto de [contexto de interação](interaction-context-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="87f18-124">Specifies properties of the [Interaction Context](interaction-context-portal.md) object.</span></span> <br/> |
| [<span data-ttu-id="87f18-125">**sinalizadores de interação \_**</span><span class="sxs-lookup"><span data-stu-id="87f18-125">**INTERACTION\_FLAGS**</span></span>](/windows/win32/api/interactioncontext/ne-interactioncontext-interaction_flags)<br/> | <span data-ttu-id="87f18-126">Especifica o estado de uma interação.</span><span class="sxs-lookup"><span data-stu-id="87f18-126">Specifies the state of an interaction.</span></span><br/> |
| [<span data-ttu-id="87f18-127">**ID de interação \_**</span><span class="sxs-lookup"><span data-stu-id="87f18-127">**INTERACTION\_ID**</span></span>](/windows/win32/api/interactioncontext/ne-interactioncontext-interaction_id)<br/> | <span data-ttu-id="87f18-128">Especifica os Estados de interação usados para configurar um objeto de [contexto de interação](interaction-context-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="87f18-128">Specifies the interaction states used for configuring an [Interaction Context](interaction-context-portal.md) object.</span></span> <span data-ttu-id="87f18-129">As interações podem ser estáticas (contato único sem manipulação, como toque, toque duplo, toque com o botão direito, pressionar e manter pressionado) ou dinâmico (um ou mais contatos com manipulação, como tradução, rotação ou dimensionamento).</span><span class="sxs-lookup"><span data-stu-id="87f18-129">Interactions can be static (single contact with no manipulation, such as tap, double tap, right tap, press and hold) or dynamic (one or more contacts with manipulation, such as translation, rotation, or scaling).</span></span><br/> |
| [<span data-ttu-id="87f18-130">**Estado de interação \_**</span><span class="sxs-lookup"><span data-stu-id="87f18-130">**INTERACTION\_STATE**</span></span>](/windows/win32/api/interactioncontext/ne-interactioncontext-interaction_state)<br/> | <span data-ttu-id="87f18-131">Especifica o estado do objeto de [contexto de interação](interaction-context-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="87f18-131">Specifies the state of the [Interaction Context](interaction-context-portal.md) object.</span></span><br/> |
| [<span data-ttu-id="87f18-132">**Estado dos trilhos de manipulação \_ \_**</span><span class="sxs-lookup"><span data-stu-id="87f18-132">**MANIPULATION\_RAILS\_STATE**</span></span>](/windows/win32/api/interactioncontext/ne-interactioncontext-manipulation_rails_state)<br/> | <span data-ttu-id="87f18-133">Especifica os Estados do trilho para uma interação.</span><span class="sxs-lookup"><span data-stu-id="87f18-133">Specifies the rail states for an interaction.</span></span><br/> |
| [<span data-ttu-id="87f18-134">**\_parâmetro de roda do mouse \_**</span><span class="sxs-lookup"><span data-stu-id="87f18-134">**MOUSE\_WHEEL\_PARAMETER**</span></span>](/windows/win32/api/interactioncontext/ne-interactioncontext-mouse_wheel_parameter)<br/> | <span data-ttu-id="87f18-135">Especifica as manipulações que podem ser mapeadas para a rotação da roda do mouse.</span><span class="sxs-lookup"><span data-stu-id="87f18-135">Specifies the manipulations that can be mapped to mouse wheel rotation.</span></span><br/> |

## <a name="related-topics"></a><span data-ttu-id="87f18-136">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="87f18-136">Related topics</span></span>

[<span data-ttu-id="87f18-137">Referência de contexto de interação</span><span class="sxs-lookup"><span data-stu-id="87f18-137">Interaction Context Reference</span></span>](interaction-context-reference.md)
