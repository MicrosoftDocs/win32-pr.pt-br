---
title: Waveform-Audio tipos de dados de entrada
description: Waveform-Audio tipos de dados de entrada
ms.assetid: dfedcb93-edfb-4a25-8445-95d4aee55734
keywords:
- áudio de onda, tipos de dados de entrada
- Wave-interface de áudio, tipos de dados de entrada
- gravando áudio de onda, tipos de dados de entrada
- Identificador de HWAVEIN
- Estrutura WAVEFORMATEX
- Estrutura WAVEHDR
- Estrutura WAVEINCAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39a8d37869224fe2ce677e2b8b952030ca6e021f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104007479"
---
# <a name="waveform-audio-input-data-types"></a><span data-ttu-id="268ce-110">Waveform-Audio tipos de dados de entrada</span><span class="sxs-lookup"><span data-stu-id="268ce-110">Waveform-Audio Input Data Types</span></span>

<span data-ttu-id="268ce-111">Os tipos de dados a seguir são definidos para funções de entrada de formato wave-áudio.</span><span class="sxs-lookup"><span data-stu-id="268ce-111">The following data types are defined for waveform-audio input functions.</span></span>



| <span data-ttu-id="268ce-112">Tipo</span><span class="sxs-lookup"><span data-stu-id="268ce-112">Type</span></span>                                 | <span data-ttu-id="268ce-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="268ce-113">Description</span></span>                                                                                                                                                     |
|--------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="268ce-114">**HWAVEIN**</span><span class="sxs-lookup"><span data-stu-id="268ce-114">**HWAVEIN**</span></span>                          | <span data-ttu-id="268ce-115">Identificador de um dispositivo de entrada de wave-áudio aberto.</span><span class="sxs-lookup"><span data-stu-id="268ce-115">Handle of an open waveform-audio input device.</span></span>                                                                                                                  |
| [<span data-ttu-id="268ce-116">**WAVEFORMATEX**</span><span class="sxs-lookup"><span data-stu-id="268ce-116">**WAVEFORMATEX**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) | <span data-ttu-id="268ce-117">Estrutura que especifica os formatos de dados com suporte por um dispositivo de entrada de wave-áudio específico.</span><span class="sxs-lookup"><span data-stu-id="268ce-117">Structure that specifies the data formats supported by a particular waveform-audio input device.</span></span> <span data-ttu-id="268ce-118">Essa estrutura também é usada para dispositivos de saída de wave-áudio.</span><span class="sxs-lookup"><span data-stu-id="268ce-118">This structure is also used for waveform-audio output devices.</span></span> |
| [<span data-ttu-id="268ce-119">**WAVEHDR**</span><span class="sxs-lookup"><span data-stu-id="268ce-119">**WAVEHDR**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr)           | <span data-ttu-id="268ce-120">Estrutura usada como um cabeçalho para um bloco de dados de entrada de forma de onda-áudio.</span><span class="sxs-lookup"><span data-stu-id="268ce-120">Structure used as a header for a block of waveform-audio input data.</span></span> <span data-ttu-id="268ce-121">Essa estrutura também é usada para dispositivos de saída de wave-áudio.</span><span class="sxs-lookup"><span data-stu-id="268ce-121">This structure is also used for waveform-audio output devices.</span></span>                             |
| [<span data-ttu-id="268ce-122">**WAVEINCAPS**</span><span class="sxs-lookup"><span data-stu-id="268ce-122">**WAVEINCAPS**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-waveincaps)     | <span data-ttu-id="268ce-123">Estrutura usada para consultar os recursos de um dispositivo de entrada de áudio de onda específico.</span><span class="sxs-lookup"><span data-stu-id="268ce-123">Structure used to inquire about the capabilities of a particular waveform-audio input device.</span></span>                                                                   |



 

## <a name="related-topics"></a><span data-ttu-id="268ce-124">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="268ce-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="268ce-125">Gravando áudio de onda</span><span class="sxs-lookup"><span data-stu-id="268ce-125">Recording Waveform Audio</span></span>](recording-waveform-audio.md)
</dt> </dl>

 

 