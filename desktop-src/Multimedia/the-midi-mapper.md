---
title: O mapeador de MIDI
description: O mapeador de MIDI
ms.assetid: 92cffc67-b4a4-4807-94d2-02fbbdba5abf
keywords:
- Multimídia do Windows, mapeador de MIDI
- multimídia, mapeador de MIDI
- áudio de multimídia, mapeador de MIDI
- áudio, mapeador de MIDI
- MIDI (interface digital de instrumento musical), mapeador de MIDI
- MIDI (interface digital de instrumentos musicais), mapeador de MIDI
- Mapeador de MIDI, sobre
- Mapeador de MIDI, origem
- Mapeador de MIDI, destino
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3b360148c994c0ee6434fdf097ca5f393b23d49
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005344"
---
# <a name="the-midi-mapper"></a><span data-ttu-id="9e1af-112">O mapeador de MIDI</span><span class="sxs-lookup"><span data-stu-id="9e1af-112">The MIDI Mapper</span></span>

<span data-ttu-id="9e1af-113">Os serviços de patch padrão do mapeador de MIDI fornecem reprodução de arquivo MIDI independente de dispositivo para aplicativos.</span><span class="sxs-lookup"><span data-stu-id="9e1af-113">The MIDI Mapper's standard patch services provide device-independent MIDI file playback for applications.</span></span> <span data-ttu-id="9e1af-114">O mapeador de MIDI pode ser usado com o sequenciador MIDI MCI ou com serviços de saída MIDI de nível baixo.</span><span class="sxs-lookup"><span data-stu-id="9e1af-114">The MIDI Mapper can be used with the MCI MIDI sequencer or with low-level MIDI output services.</span></span>

<span data-ttu-id="9e1af-115">A menos que declarado de outra forma, todas as referências a números de canal de MIDI usam os números de canal lógico de 1 a 16.</span><span class="sxs-lookup"><span data-stu-id="9e1af-115">Unless stated otherwise, all references to MIDI channel numbers use the logical channel numbers 1 through 16.</span></span> <span data-ttu-id="9e1af-116">Esses números de canal lógico correspondem aos números de canal físico de 0 a 15 que, na verdade, fazem parte da mensagem MIDI.</span><span class="sxs-lookup"><span data-stu-id="9e1af-116">These logical channel numbers correspond to the physical channel numbers 0 through 15 that are actually part of the MIDI message.</span></span> <span data-ttu-id="9e1af-117">Todas as referências a valores de chave e alteração de programa MIDI usam os valores físicos de 0 a 127.</span><span class="sxs-lookup"><span data-stu-id="9e1af-117">All references to MIDI program-change and key values use the physical values 0 through 127.</span></span> <span data-ttu-id="9e1af-118">Todos os números são decimais, a menos que sejam precedidos pelo prefixo "0x"; nesse caso, eles são hexadecimais.</span><span class="sxs-lookup"><span data-stu-id="9e1af-118">All numbers are decimal unless preceded by "0x" prefix, in which case they are hexadecimal.</span></span>

<span data-ttu-id="9e1af-119">Na discussão do mapeador de MIDI, o termo *origem* se refere ao lado de entrada do mapeador de Midi.</span><span class="sxs-lookup"><span data-stu-id="9e1af-119">In the discussion of the MIDI Mapper, the term *source* refers to the input side of the MIDI Mapper.</span></span> <span data-ttu-id="9e1af-120">O termo *destino* refere-se ao lado de saída do mapeador de Midi.</span><span class="sxs-lookup"><span data-stu-id="9e1af-120">The term *destination* refers to the output side of the MIDI Mapper.</span></span> <span data-ttu-id="9e1af-121">Por exemplo, um canal de origem é o canal MIDI de uma mensagem enviada para o mapeador de MIDI, e um canal de destino é o canal MIDI de uma mensagem enviada do Mapeador MIDI para um dispositivo de saída.</span><span class="sxs-lookup"><span data-stu-id="9e1af-121">For example, a source channel is the MIDI channel of a message sent to the MIDI Mapper, and a destination channel is the MIDI channel of a message sent from the MIDI Mapper to an output device.</span></span>

-   [<span data-ttu-id="9e1af-122">O mapeador de MIDI e o Windows</span><span class="sxs-lookup"><span data-stu-id="9e1af-122">The MIDI Mapper and Windows</span></span>](the-midi-mapper-and-windows.md)
-   [<span data-ttu-id="9e1af-123">A arquitetura do mapeador de MIDI</span><span class="sxs-lookup"><span data-stu-id="9e1af-123">The MIDI Mapper Architecture</span></span>](the-midi-mapper-architecture.md)
-   [<span data-ttu-id="9e1af-124">O mapa do canal</span><span class="sxs-lookup"><span data-stu-id="9e1af-124">The Channel Map</span></span>](the-channel-map.md)
-   [<span data-ttu-id="9e1af-125">Mapas de patch</span><span class="sxs-lookup"><span data-stu-id="9e1af-125">Patch Maps</span></span>](patch-maps.md)
-   [<span data-ttu-id="9e1af-126">O volume escalar</span><span class="sxs-lookup"><span data-stu-id="9e1af-126">The Volume Scalar</span></span>](the-volume-scalar.md)
-   [<span data-ttu-id="9e1af-127">Mapas de chaves</span><span class="sxs-lookup"><span data-stu-id="9e1af-127">Key Maps</span></span>](key-maps.md)
-   [<span data-ttu-id="9e1af-128">Resumo de mensagens de mapas e MIDI</span><span class="sxs-lookup"><span data-stu-id="9e1af-128">Summary of Maps and MIDI Messages</span></span>](summary-of-maps-and-midi-messages.md)

 

 




