---
title: Mapas de patch
description: Mapas de patch
ms.assetid: d0c91001-d19d-439c-9773-78d6228a6642
keywords:
- MIDI (interface digital de instrumento musical), mapeador de MIDI
- MIDI (interface digital de instrumentos musicais), mapeador de MIDI
- Mapeador de MIDI, mapas de patch
- mapas de patch
- Programa MIDI – alterar mensagens
- Mensagens de controlador de volume de MIDI
- programa-alterar mensagens
- mensagens do controlador de volume
- Mapeador de MIDI, mensagens de alteração de programa
- Mapeador de MIDI, mensagens de controlador de volume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e418b0616d9ba9d2c2bcd05ebcb312ba0176ef5c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292094"
---
# <a name="patch-maps"></a><span data-ttu-id="6097e-113">Mapas de patch</span><span class="sxs-lookup"><span data-stu-id="6097e-113">Patch Maps</span></span>

<span data-ttu-id="6097e-114">Cada entrada de mapa de canal pode ter um mapa de patch associado.</span><span class="sxs-lookup"><span data-stu-id="6097e-114">Each channel map entry can have an associated patch map.</span></span> <span data-ttu-id="6097e-115">Mapas de patch afetam as mensagens de alteração de programa MIDI e controlador de volume.</span><span class="sxs-lookup"><span data-stu-id="6097e-115">Patch maps affect MIDI program-change and volume-controller messages.</span></span> <span data-ttu-id="6097e-116">Mensagens de alteração de programa informam um sintetizador para alterar o som do instrumento (patch) para um canal especificado.</span><span class="sxs-lookup"><span data-stu-id="6097e-116">Program-change messages tell a synthesizer to change the instrument sound (patch) for a specified channel.</span></span> <span data-ttu-id="6097e-117">As mensagens do controlador de volume definem o volume para um canal.</span><span class="sxs-lookup"><span data-stu-id="6097e-117">Volume-controller messages set the volume for a channel.</span></span>

<span data-ttu-id="6097e-118">Um mapa de patch tem uma tabela de conversão com uma entrada para cada um dos valores de alteração de programa 128.</span><span class="sxs-lookup"><span data-stu-id="6097e-118">A patch map has a translation table with an entry for each of the 128 program-change values.</span></span> <span data-ttu-id="6097e-119">Cada mapa de patch especifica o seguinte:</span><span class="sxs-lookup"><span data-stu-id="6097e-119">Each patch map specifies the following:</span></span>

-   <span data-ttu-id="6097e-120">Um programa de destino-alterar valor.</span><span class="sxs-lookup"><span data-stu-id="6097e-120">A destination program-change value.</span></span>
-   <span data-ttu-id="6097e-121">Um volume escalar.</span><span class="sxs-lookup"><span data-stu-id="6097e-121">A volume scalar.</span></span> <span data-ttu-id="6097e-122">(Para obter mais informações, consulte [o volume escalar](the-volume-scalar.md).)</span><span class="sxs-lookup"><span data-stu-id="6097e-122">(For more information, see [The Volume Scalar](the-volume-scalar.md).)</span></span>
-   <span data-ttu-id="6097e-123">Um mapa de chave opcional.</span><span class="sxs-lookup"><span data-stu-id="6097e-123">An optional key map.</span></span> <span data-ttu-id="6097e-124">(Para obter mais informações, consulte [mapas de chaves](key-maps.md).)</span><span class="sxs-lookup"><span data-stu-id="6097e-124">(For more information, see [Key Maps](key-maps.md).)</span></span>

<span data-ttu-id="6097e-125">Quando as mensagens de alteração de programa são recebidas pelo mapeador de MIDI, o valor de alteração do programa de destino é substituído pelo valor de alteração de programa na mensagem.</span><span class="sxs-lookup"><span data-stu-id="6097e-125">When program-change messages are received by the MIDI Mapper, the destination program-change value is substituted for the program-change value in the message.</span></span> <span data-ttu-id="6097e-126">Por exemplo, se o programa de destino-alterar o valor da alteração de programa 16 for 18, o mapeador de MIDI modificará a mensagem de alteração do programa MIDI, conforme mostrado na ilustração a seguir.</span><span class="sxs-lookup"><span data-stu-id="6097e-126">For example, if the destination program-change value for program-change 16 is 18, the MIDI Mapper modifies the MIDI program-change message as shown in the following illustration.</span></span>

![imagem do Mapeador MIDI](images/mmap-a03.gif)

 

 




