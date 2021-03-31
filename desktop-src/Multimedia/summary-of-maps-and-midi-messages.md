---
title: Resumo de mensagens de mapas e MIDI
description: Resumo de mensagens de mapas e MIDI
ms.assetid: cd0ec7b0-2ba1-4e75-b85c-f5b95ac9dfeb
keywords:
- MIDI (interface digital de instrumento musical), mapeador de MIDI
- MIDI (interface digital de instrumentos musicais), mapeador de MIDI
- Mapeador de MIDI, mapa de canal
- Mapeador de MIDI, mapas de patch
- Mapeador de MIDI, mapas de chave
- mapa de canal
- mapas de patch
- mapas de chaves
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddd962f848343ea493204d494943a99eedcc56a5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636836"
---
# <a name="summary-of-maps-and-midi-messages"></a><span data-ttu-id="58bd3-111">Resumo de mensagens de mapas e MIDI</span><span class="sxs-lookup"><span data-stu-id="58bd3-111">Summary of Maps and MIDI Messages</span></span>

<span data-ttu-id="58bd3-112">A seguir estão os bytes de status para mensagens MIDI e os tipos de mapa que afetam cada mensagem.</span><span class="sxs-lookup"><span data-stu-id="58bd3-112">Following are the status bytes for MIDI messages and the map types that affect each message.</span></span>



| <span data-ttu-id="58bd3-113">Status de MIDI</span><span class="sxs-lookup"><span data-stu-id="58bd3-113">MIDI status</span></span> | <span data-ttu-id="58bd3-114">Description</span><span class="sxs-lookup"><span data-stu-id="58bd3-114">Description</span></span>               | <span data-ttu-id="58bd3-115">Tipos de mapa</span><span class="sxs-lookup"><span data-stu-id="58bd3-115">Map types</span></span>                |
|-------------|---------------------------|--------------------------|
| <span data-ttu-id="58bd3-116">0x80-0x8F</span><span class="sxs-lookup"><span data-stu-id="58bd3-116">0x80-0x8F</span></span>   | <span data-ttu-id="58bd3-117">Anotação desativada</span><span class="sxs-lookup"><span data-stu-id="58bd3-117">Note off</span></span>                  | <span data-ttu-id="58bd3-118">Mapas de canal, mapas de chaves</span><span class="sxs-lookup"><span data-stu-id="58bd3-118">Channel maps, key maps</span></span>   |
| <span data-ttu-id="58bd3-119">0x90-0x9F</span><span class="sxs-lookup"><span data-stu-id="58bd3-119">0x90-0x9F</span></span>   | <span data-ttu-id="58bd3-120">Observe o </span><span class="sxs-lookup"><span data-stu-id="58bd3-120">Note on</span></span>                   | <span data-ttu-id="58bd3-121">Mapas de canal, mapas de chaves</span><span class="sxs-lookup"><span data-stu-id="58bd3-121">Channel maps, key maps</span></span>   |
| <span data-ttu-id="58bd3-122">0xA0-0xAF</span><span class="sxs-lookup"><span data-stu-id="58bd3-122">0xA0-0xAF</span></span>   | <span data-ttu-id="58bd3-123">Aftertouch de chave de telefonia</span><span class="sxs-lookup"><span data-stu-id="58bd3-123">Polyphonic-key aftertouch</span></span> | <span data-ttu-id="58bd3-124">Mapas de canal, mapas de chaves</span><span class="sxs-lookup"><span data-stu-id="58bd3-124">Channel maps, key maps</span></span>   |
| <span data-ttu-id="58bd3-125">0xB0-0xBF</span><span class="sxs-lookup"><span data-stu-id="58bd3-125">0xB0-0xBF</span></span>   | <span data-ttu-id="58bd3-126">Alteração de controle</span><span class="sxs-lookup"><span data-stu-id="58bd3-126">Control change</span></span>            | <span data-ttu-id="58bd3-127">Mapas de canal, mapas de patch</span><span class="sxs-lookup"><span data-stu-id="58bd3-127">Channel maps, patch maps</span></span> |
| <span data-ttu-id="58bd3-128">0xC0-0xCF</span><span class="sxs-lookup"><span data-stu-id="58bd3-128">0xC0-0xCF</span></span>   | <span data-ttu-id="58bd3-129">Alteração do programa</span><span class="sxs-lookup"><span data-stu-id="58bd3-129">Program change</span></span>            | <span data-ttu-id="58bd3-130">Mapas de canal, mapas de patch</span><span class="sxs-lookup"><span data-stu-id="58bd3-130">Channel maps, patch maps</span></span> |
| <span data-ttu-id="58bd3-131">0xD0-0xDF</span><span class="sxs-lookup"><span data-stu-id="58bd3-131">0xD0-0xDF</span></span>   | <span data-ttu-id="58bd3-132">Aftertouch de canal</span><span class="sxs-lookup"><span data-stu-id="58bd3-132">Channel aftertouch</span></span>        | <span data-ttu-id="58bd3-133">Mapas de canal</span><span class="sxs-lookup"><span data-stu-id="58bd3-133">Channel maps</span></span>             |
| <span data-ttu-id="58bd3-134">0xE0-0xEF</span><span class="sxs-lookup"><span data-stu-id="58bd3-134">0xE0-0xEF</span></span>   | <span data-ttu-id="58bd3-135">Alteração de curvatura de densidade</span><span class="sxs-lookup"><span data-stu-id="58bd3-135">Pitch-bend change</span></span>         | <span data-ttu-id="58bd3-136">Mapas de canal</span><span class="sxs-lookup"><span data-stu-id="58bd3-136">Channel maps</span></span>             |
| <span data-ttu-id="58bd3-137">0xF0-0xFF</span><span class="sxs-lookup"><span data-stu-id="58bd3-137">0xF0-0xFF</span></span>   | <span data-ttu-id="58bd3-138">Sistema</span><span class="sxs-lookup"><span data-stu-id="58bd3-138">System</span></span>                    | <span data-ttu-id="58bd3-139">Não mapeado</span><span class="sxs-lookup"><span data-stu-id="58bd3-139">Not mapped</span></span>               |



 

-   <span data-ttu-id="58bd3-140">Os quatro bits de ordem superior representam o valor de status.</span><span class="sxs-lookup"><span data-stu-id="58bd3-140">The high-order four bits represent the status value.</span></span> <span data-ttu-id="58bd3-141">Os quatro bits de ordem inferior representam as informações do canal.</span><span class="sxs-lookup"><span data-stu-id="58bd3-141">The low-order four bits represent the channel information.</span></span>
-   <span data-ttu-id="58bd3-142">Mapas de patch afetam apenas o controlador 7 (volume principal).</span><span class="sxs-lookup"><span data-stu-id="58bd3-142">Patch maps affect only controller 7 (main volume).</span></span>
-   <span data-ttu-id="58bd3-143">As mensagens do sistema são enviadas para todos os dispositivos listados em um mapa de canal.</span><span class="sxs-lookup"><span data-stu-id="58bd3-143">System messages are sent to all devices listed in a channel map.</span></span>

 

 




