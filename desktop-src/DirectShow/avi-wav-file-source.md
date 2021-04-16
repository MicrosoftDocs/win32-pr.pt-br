---
description: Origem do arquivo AVI/WAV
ms.assetid: b8abf5d8-ba7f-441d-beef-9f85859318d5
title: Origem do arquivo AVI/WAV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef659d880ef570176f94ac91875291ea9d200cf5
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105779244"
---
# <a name="aviwav-file-source"></a><span data-ttu-id="e5fa9-103">Origem do arquivo AVI/WAV</span><span class="sxs-lookup"><span data-stu-id="e5fa9-103">AVI/WAV File Source</span></span>

<span data-ttu-id="e5fa9-104">(Preterido.</span><span class="sxs-lookup"><span data-stu-id="e5fa9-104">(Deprecated.</span></span> <span data-ttu-id="e5fa9-105">Para arquivos AVI e WAV, use a [origem do arquivo (Async)](file-source--async--filter.md) e o [divisor AVI](avi-splitter-filter.md) ou o [analisador Wave](wave-parser-filter.md).)</span><span class="sxs-lookup"><span data-stu-id="e5fa9-105">For AVI and WAV files, use the [File Source (Async)](file-source--async--filter.md) and the [AVI Splitter](avi-splitter-filter.md) or [WAVE Parser](wave-parser-filter.md).)</span></span>

<span data-ttu-id="e5fa9-106">O filtro de origem de arquivo AVI/WAV lê arquivos de origem AVI e WAV e gera os Pins de saída apropriados para o tipo de arquivo.</span><span class="sxs-lookup"><span data-stu-id="e5fa9-106">The AVI/WAV File Source filter reads AVI and WAV source files and generates the appropriate output pins for the file type.</span></span>

<span data-ttu-id="e5fa9-107">Para arquivos WAV, o filtro cria um PIN de saída de áudio, que produz um fluxo de áudio que pode ser conectado a um filtro de renderização de áudio ou ao filtro de transformação de áudio intermediário.</span><span class="sxs-lookup"><span data-stu-id="e5fa9-107">For WAV files, the filter creates an audio output pin, which produces an audio stream that can be connected to an audio rendering filter or intervening audio transform filter.</span></span>

<span data-ttu-id="e5fa9-108">Para arquivos AVI, o filtro cria um pino de saída de vídeo, que produz um fluxo AVI compactado adequado para o filtro de codec AVI e um PIN de saída de áudio, que produz um fluxo de áudio adequado para um filtro de renderização de áudio ou um filtro de transformação de áudio intermediário.</span><span class="sxs-lookup"><span data-stu-id="e5fa9-108">For AVI files, the filter creates a video output pin, which produces a compressed AVI stream suitable for the AVI codec filter, and an audio output pin, which produces an audio stream suitable for an audio rendering filter or an intervening audio transform filter.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e5fa9-109">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e5fa9-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e5fa9-110">Filtros do DirectShow</span><span class="sxs-lookup"><span data-stu-id="e5fa9-110">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



