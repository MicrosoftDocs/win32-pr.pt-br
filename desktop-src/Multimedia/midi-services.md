---
title: Serviços MIDI
description: Serviços MIDI
ms.assetid: 884066c2-6927-4f5b-902b-8baef9a4a0d7
keywords:
- Multimídia do Windows, serviços MIDI
- multimídia, serviços de MIDI
- áudio de multimídia, serviços de MIDI
- áudio, serviços de MIDI
- MIDI (interface digital de instrumento musical), serviços de MIDI
- MIDI (interface digital de instrumentos musicais), serviços de MIDI
- Serviços de MIDI, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc412ddec21245e9682a2a2e79e3f8031d2a6918
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104365959"
---
# <a name="midi-services"></a><span data-ttu-id="8762d-110">Serviços MIDI</span><span class="sxs-lookup"><span data-stu-id="8762d-110">MIDI Services</span></span>

<span data-ttu-id="8762d-111">A maioria dos aplicativos poderá usar o sequenciador MIDI MCI ou buffers de fluxo (e a função [**midiStreamOut**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout) ) para implementar toda a funcionalidade de Midi de que precisam.</span><span class="sxs-lookup"><span data-stu-id="8762d-111">Most applications will be able to use the MCI MIDI sequencer or stream buffers (and the [**midiStreamOut**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout) function) to implement all the MIDI functionality they need.</span></span> <span data-ttu-id="8762d-112">Os desenvolvedores de MIDI sérios, aqueles que produzem ferramentas de criação de MIDI ou de sequenciamento, podem usar uma combinação dos recursos de fluxo e dos serviços de MIDI ou usar apenas os serviços de MIDI.</span><span class="sxs-lookup"><span data-stu-id="8762d-112">Serious MIDI developers — those producing MIDI authoring or sequencing tools — can use either a combination of the stream capabilities and the MIDI services or use only the MIDI services.</span></span> <span data-ttu-id="8762d-113">Os tópicos a seguir fornecem informações gerais sobre como usar os serviços MIDI.</span><span class="sxs-lookup"><span data-stu-id="8762d-113">The following topics provides general information about using the MIDI services.</span></span>

-   [<span data-ttu-id="8762d-114">Consultando dispositivos MIDI</span><span class="sxs-lookup"><span data-stu-id="8762d-114">Querying MIDI Devices</span></span>](querying-midi-devices.md)
-   [<span data-ttu-id="8762d-115">Abrindo e fechando drivers de dispositivo</span><span class="sxs-lookup"><span data-stu-id="8762d-115">Opening and Closing Device Drivers</span></span>](opening-and-closing-device-drivers.md)
-   [<span data-ttu-id="8762d-116">Alocando e preparando blocos de dados MIDI</span><span class="sxs-lookup"><span data-stu-id="8762d-116">Allocating and Preparing MIDI Data Blocks</span></span>](allocating-and-preparing-midi-data-blocks.md)
-   [<span data-ttu-id="8762d-117">Gerenciando blocos de dados MIDI</span><span class="sxs-lookup"><span data-stu-id="8762d-117">Managing MIDI Data Blocks</span></span>](managing-midi-data-blocks.md)
-   [<span data-ttu-id="8762d-118">Solicitando formatos de hora</span><span class="sxs-lookup"><span data-stu-id="8762d-118">Requesting Time Formats</span></span>](requesting-time-formats.md)
-   [<span data-ttu-id="8762d-119">Tratamento de erros com funções MIDI</span><span class="sxs-lookup"><span data-stu-id="8762d-119">Handling Errors with MIDI Functions</span></span>](handling-errors-with-midi-functions.md)

 

 