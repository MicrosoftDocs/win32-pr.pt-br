---
title: Listas
description: Listas
ms.assetid: 89fb4457-307a-4693-94d4-57f57c422d1e
keywords:
- mixers de áudio, controles
- mixers de áudio, listas
- mixers, controles
- mixers, listas
- controles de lista
- Estrutura de MIXERCONTROLDETAILS_BOOLEAN
- Estrutura de MIXERCONTROLDETAILS_LISTTEXT
- controle de seleção única
- controle de seleção múltipla
- controle do mixer
- Multiplexador (MUX)
- MUX (multiplexador)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d475816d7090ee241a1508cc054b12742c4ab27
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104293941"
---
# <a name="lists"></a><span data-ttu-id="f75f7-115">Listas</span><span class="sxs-lookup"><span data-stu-id="f75f7-115">Lists</span></span>

<span data-ttu-id="f75f7-116">Os controles de lista fornecem Estados de seleção única ou seleção múltipla para linhas de áudio complexas.</span><span class="sxs-lookup"><span data-stu-id="f75f7-116">The list controls provide single-select or multiple-select states for complex audio lines.</span></span> <span data-ttu-id="f75f7-117">Esses controles usam a [**estrutura \_ booliana MIXERCONTROLDETAILS**](/previous-versions//dd757295(v=vs.85)) para recuperar e definir propriedades de controle.</span><span class="sxs-lookup"><span data-stu-id="f75f7-117">These controls use the [**MIXERCONTROLDETAILS\_BOOLEAN**](/previous-versions//dd757295(v=vs.85)) structure to retrieve and set control properties.</span></span> <span data-ttu-id="f75f7-118">A estrutura [**MIXERCONTROLDETAILS \_ LISTTEXT**](/previous-versions//dd757296(v=vs.85)) também é usada para recuperar todas as descrições de texto de um controle de vários itens.</span><span class="sxs-lookup"><span data-stu-id="f75f7-118">The [**MIXERCONTROLDETAILS\_LISTTEXT**](/previous-versions//dd757296(v=vs.85)) structure is also used to retrieve all text descriptions of a multiple-item control.</span></span> <span data-ttu-id="f75f7-119">A tabela a seguir descreve os tipos de controles de lista.</span><span class="sxs-lookup"><span data-stu-id="f75f7-119">The following table describes the types of list controls.</span></span>



| <span data-ttu-id="f75f7-120">Control</span><span class="sxs-lookup"><span data-stu-id="f75f7-120">Control</span></span>           | <span data-ttu-id="f75f7-121">Descrição</span><span class="sxs-lookup"><span data-stu-id="f75f7-121">Description</span></span>                                                                                                                                                                                                                                                                      |
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f75f7-122">Seleção única</span><span class="sxs-lookup"><span data-stu-id="f75f7-122">Single-select</span></span>     | <span data-ttu-id="f75f7-123">Restringe a seleção de controle para um item por vez.</span><span class="sxs-lookup"><span data-stu-id="f75f7-123">Restricts the control selection to one item at a time.</span></span> <span data-ttu-id="f75f7-124">Ao contrário do controle Multiplexador, esse controle pode ser usado para controlar mais do que as linhas de origem de áudio.</span><span class="sxs-lookup"><span data-stu-id="f75f7-124">Unlike the multiplexer control, this control can be used to control more than audio source lines.</span></span> <span data-ttu-id="f75f7-125">Por exemplo, você pode usar esse controle para selecionar um filtro de baixa passa de uma lista de filtros com suporte de um dispositivo de mixer.</span><span class="sxs-lookup"><span data-stu-id="f75f7-125">For example, you could use this control to select a low-pass filter from a list of filters supported by a mixer device.</span></span> |
| <span data-ttu-id="f75f7-126">Multiplexador (MUX)</span><span class="sxs-lookup"><span data-stu-id="f75f7-126">Multiplexer (MUX)</span></span> | <span data-ttu-id="f75f7-127">Restringe a seleção de linha a uma linha de origem por vez.</span><span class="sxs-lookup"><span data-stu-id="f75f7-127">Restricts the line selection to one source line at a time.</span></span>                                                                                                                                                                                                                       |
| <span data-ttu-id="f75f7-128">Seleção múltipla</span><span class="sxs-lookup"><span data-stu-id="f75f7-128">Multiple-select</span></span>   | <span data-ttu-id="f75f7-129">Permite que o usuário Selecione vários itens de uma lista simultaneamente.</span><span class="sxs-lookup"><span data-stu-id="f75f7-129">Allows the user to select multiple items from a list simultaneously.</span></span> <span data-ttu-id="f75f7-130">Ao contrário do controle de mixer, o controle de seleção múltipla pode ser usado para controlar mais do que as linhas de origem de áudio.</span><span class="sxs-lookup"><span data-stu-id="f75f7-130">Unlike the mixer control, the multiple-select control can be used to control more than audio source lines.</span></span>                                                                                                  |
| <span data-ttu-id="f75f7-131">Mixagem</span><span class="sxs-lookup"><span data-stu-id="f75f7-131">Mixer</span></span>             | <span data-ttu-id="f75f7-132">Permite que o usuário Selecione linhas de origem de uma lista simultaneamente.</span><span class="sxs-lookup"><span data-stu-id="f75f7-132">Allows the user to select source lines from a list simultaneously.</span></span>                                                                                                                                                                                                               |



 

 

 