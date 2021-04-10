---
title: A arquitetura do mapeador de MIDI
description: A arquitetura do mapeador de MIDI
ms.assetid: d08d1442-bf9f-46bb-bd44-f512ff4b6bd5
keywords:
- MIDI (interface digital de instrumento musical), mapeador de MIDI
- MIDI (interface digital de instrumentos musicais), mapeador de MIDI
- Mapeador de MIDI, arquitetura
- Mapeador de MIDI, mapa de instalação
- Mapa de instalação MIDI
- Mapeador de MIDI, mapa de canal
- Mapeador de MIDI, mapas de patch
- Mapeador de MIDI, mapas de chave
- mapa de canal
- mapas de patch
- mapas de chaves
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba337b05fcff1bd0bb0e948e36e7d290eacb9604
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292581"
---
# <a name="the-midi-mapper-architecture"></a><span data-ttu-id="581c6-114">A arquitetura do mapeador de MIDI</span><span class="sxs-lookup"><span data-stu-id="581c6-114">The MIDI Mapper Architecture</span></span>

<span data-ttu-id="581c6-115">O mapeador de MIDI usa um mapa de instalação de MIDI para determinar como converter e redirecionar as mensagens recebidas.</span><span class="sxs-lookup"><span data-stu-id="581c6-115">The MIDI Mapper uses a MIDI setup map to determine how to translate and redirect the messages it receives.</span></span> <span data-ttu-id="581c6-116">Um mapa de instalação de MIDI consiste nos seguintes tipos de mapas.</span><span class="sxs-lookup"><span data-stu-id="581c6-116">A MIDI setup map consists of the following types of maps.</span></span>

-   [<span data-ttu-id="581c6-117">O mapa do canal</span><span class="sxs-lookup"><span data-stu-id="581c6-117">The Channel Map</span></span>](the-channel-map.md)
-   [<span data-ttu-id="581c6-118">Mapas de patch</span><span class="sxs-lookup"><span data-stu-id="581c6-118">Patch Maps</span></span>](patch-maps.md)
-   [<span data-ttu-id="581c6-119">Mapas de chaves</span><span class="sxs-lookup"><span data-stu-id="581c6-119">Key Maps</span></span>](key-maps.md)

<span data-ttu-id="581c6-120">A ilustração a seguir mostra as funções de canal, patch e mapas de chave em um mapa de instalação de MIDI.</span><span class="sxs-lookup"><span data-stu-id="581c6-120">The following illustration shows the roles of channel, patch, and key maps in a MIDI setup map.</span></span>

![as funções de canal, patch e mapas de chave em uma imagem de mapa de instalação Midi](images/mmap-a02.gif)

 

 




