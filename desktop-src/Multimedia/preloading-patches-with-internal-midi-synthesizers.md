---
title: Precarregamento de patches com sintetizadores MIDI internos
description: Precarregamento de patches com sintetizadores MIDI internos
ms.assetid: c200aa91-ab91-48e8-b3b5-8e7f36e511be
keywords:
- MIDI (interface digital de instrumento musical), sintetizadores internos
- MIDI (interface digital de instrumentos musicais), sintetizadores internos
- executando arquivos MIDI, sintetizadores internos
- sintetizadores MIDI internos
- MIDI (interface digital de instrumento musical), patches de pré-carregamento
- MIDI (interface digital de instrumentos musicais), patches de pré-carregamento
- executando arquivos MIDI, caminhos de pré-carregamento
- carregando patches de MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc54eccdaa0a0c9aa16f206e7e036f322b615d96
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103917214"
---
# <a name="preloading-patches-with-internal-midi-synthesizers"></a><span data-ttu-id="1df6c-111">Precarregamento de patches com sintetizadores MIDI internos</span><span class="sxs-lookup"><span data-stu-id="1df6c-111">Preloading Patches with Internal MIDI Synthesizers</span></span>

<span data-ttu-id="1df6c-112">Alguns dispositivos de sintetizador MIDI internos não podem manter todos os seus patches carregados simultaneamente.</span><span class="sxs-lookup"><span data-stu-id="1df6c-112">Some internal MIDI synthesizer devices cannot keep all of their patches loaded simultaneously.</span></span> <span data-ttu-id="1df6c-113">Esses dispositivos devem pré-carregar seus dados de patch.</span><span class="sxs-lookup"><span data-stu-id="1df6c-113">These devices must preload their patch data.</span></span>

<span data-ttu-id="1df6c-114">O Windows fornece as seguintes funções para solicitar que um sintetizador seja pré-carregar e armazene em cache os patches especificados.</span><span class="sxs-lookup"><span data-stu-id="1df6c-114">Windows provides the following functions to request that a synthesizer preload and cache specified patches.</span></span>



| <span data-ttu-id="1df6c-115">Valor</span><span class="sxs-lookup"><span data-stu-id="1df6c-115">Value</span></span>                                                      | <span data-ttu-id="1df6c-116">Significado</span><span class="sxs-lookup"><span data-stu-id="1df6c-116">Meaning</span></span>                                                                                                     |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1df6c-117">**midiOutCachePatches**</span><span class="sxs-lookup"><span data-stu-id="1df6c-117">**midiOutCachePatches**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutcachepatches)         | <span data-ttu-id="1df6c-118">Solicita que um dispositivo sintetizador MIDI interno seja pré-carregamento e armazene em cache os patches Melodic especificados.</span><span class="sxs-lookup"><span data-stu-id="1df6c-118">Requests that an internal MIDI synthesizer device preload and cache specified melodic patches.</span></span>              |
| [<span data-ttu-id="1df6c-119">**midiOutCacheDrumPatches**</span><span class="sxs-lookup"><span data-stu-id="1df6c-119">**midiOutCacheDrumPatches**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutcachedrumpatches) | <span data-ttu-id="1df6c-120">Solicita que um dispositivo sintetizador MIDI interno seja despré-carregamento e armazene em cache os patches de percussão baseados em chave especificados.</span><span class="sxs-lookup"><span data-stu-id="1df6c-120">Requests that an internal MIDI synthesizer device preload and cache specified key-based percussion patches.</span></span> |



 

<span data-ttu-id="1df6c-121">Para obter informações sobre como determinar se um dispositivo específico dá suporte a patches de pré-carregamento, consulte [consultando dispositivos de saída de Midi](querying-midi-output-devices.md).</span><span class="sxs-lookup"><span data-stu-id="1df6c-121">For information on how to determine if a particular device supports preloading patches, see [Querying MIDI Output Devices](querying-midi-output-devices.md).</span></span>

 

 