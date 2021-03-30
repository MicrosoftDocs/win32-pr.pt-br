---
title: Mapas de chaves
description: Mapas de chaves
ms.assetid: 5d0367b0-bbf1-4a4b-98b2-dbca6f2f8b0c
keywords:
- MIDI (interface digital de instrumento musical), mapeador de MIDI
- MIDI (interface digital de instrumentos musicais), mapeador de MIDI
- Mapeador de MIDI, mapas de chave
- mapas de chaves
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffafd99e6d813f12c388b633997980b7a58d62dc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916123"
---
# <a name="key-maps"></a><span data-ttu-id="89b74-107">Mapas de chaves</span><span class="sxs-lookup"><span data-stu-id="89b74-107">Key Maps</span></span>

<span data-ttu-id="89b74-108">Cada entrada na tabela de tradução do mapa de patches pode ter um mapa de chaves associado.</span><span class="sxs-lookup"><span data-stu-id="89b74-108">Each entry in the patch-map translation table can have an associated key map.</span></span> <span data-ttu-id="89b74-109">Os mapas principais afetam as mensagens de observação, de observação e de aftertouch de chave de telefonia.</span><span class="sxs-lookup"><span data-stu-id="89b74-109">Key maps affect note-on, note-off, and polyphonic-key-aftertouch messages.</span></span> <span data-ttu-id="89b74-110">Um mapa de chaves tem uma tabela de conversão com uma entrada para cada um dos valores de chave MIDI 128.</span><span class="sxs-lookup"><span data-stu-id="89b74-110">A key map has a translation table with an entry for each of the 128 MIDI key values.</span></span> <span data-ttu-id="89b74-111">Por exemplo, se a entrada para o valor de chave 60 for 72, o mapeador de MIDI modificará as mensagens de observação em MIDI, conforme mostrado na ilustração a seguir.</span><span class="sxs-lookup"><span data-stu-id="89b74-111">For example, if the entry for key value 60 is 72, the MIDI Mapper modifies MIDI note-on messages as shown in the following illustration.</span></span>

![imagem do Mapeador MIDI](images/mmap-a06.gif)

<span data-ttu-id="89b74-113">Mapas de chave são úteis com sintetizadores que têm instrumentos de percussão baseados em chave com um som de percussão específico atribuído a cada chave.</span><span class="sxs-lookup"><span data-stu-id="89b74-113">Key maps are useful with synthesizers that have key-based percussion instruments with a particular percussion sound assigned to each key.</span></span> <span data-ttu-id="89b74-114">Mapas de chave geralmente são atribuídos ao primeiro patch no mapa de patches nos canais de percussão (10 e 16).</span><span class="sxs-lookup"><span data-stu-id="89b74-114">Key maps are usually assigned to the first patch in the patch maps on the percussion channels (10 and 16).</span></span>

 

 




