---
description: Interfaces de renderização e captura de áudio
ms.assetid: 79b42ffd-703a-4a7c-bb2d-5cfc2fbeb16c
title: Interfaces de renderização e captura de áudio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f941c1220f1adc06a686d702e9db21095a8cb7e6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105812856"
---
# <a name="audio-capture-and-rendering-interfaces"></a><span data-ttu-id="53f62-103">Interfaces de renderização e captura de áudio</span><span class="sxs-lookup"><span data-stu-id="53f62-103">Audio Capture and Rendering Interfaces</span></span>

<span data-ttu-id="53f62-104">Essas interfaces dão suporte à captura e renderização de áudio no DirectShow</span><span class="sxs-lookup"><span data-stu-id="53f62-104">These interfaces support audio capture and rendering in DirectShow</span></span>



| <span data-ttu-id="53f62-105">Interface</span><span class="sxs-lookup"><span data-stu-id="53f62-105">Interface</span></span>                                              | <span data-ttu-id="53f62-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="53f62-106">Description</span></span>                                                                                                                                               |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="53f62-107">**IAMAudioInputMixer**</span><span class="sxs-lookup"><span data-stu-id="53f62-107">**IAMAudioInputMixer**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamaudioinputmixer)       | <span data-ttu-id="53f62-108">Acesse as entradas analógicas na placa de som do sistema e ajuste as características, como mono ou estéreo, nível de mixagem, nível panorâmico, intensidade, agudo e baixo.</span><span class="sxs-lookup"><span data-stu-id="53f62-108">Access the analog inputs on the system's sound card and adjust characteristics, such as mono or stereo, mix level, pan level, loudness, treble, and bass.</span></span> |
| [<span data-ttu-id="53f62-109">**IAMAudioRendererStats**</span><span class="sxs-lookup"><span data-stu-id="53f62-109">**IAMAudioRendererStats**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamaudiorendererstats) | <span data-ttu-id="53f62-110">Obtenha informações estatísticas de desempenho sobre o processamento de áudio.</span><span class="sxs-lookup"><span data-stu-id="53f62-110">Get statistical performance information about audio renderering.</span></span>                                                                                          |
| [<span data-ttu-id="53f62-111">**IAMBufferNegotiation**</span><span class="sxs-lookup"><span data-stu-id="53f62-111">**IAMBufferNegotiation**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iambuffernegotiation)   | <span data-ttu-id="53f62-112">Controle como o filtro de captura de áudio aloca buffers.</span><span class="sxs-lookup"><span data-stu-id="53f62-112">Control how the audio capture filter allocates buffers.</span></span>                                                                                                   |
| [<span data-ttu-id="53f62-113">**IAMClockSlave**</span><span class="sxs-lookup"><span data-stu-id="53f62-113">**IAMClockSlave**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamclockslave)                 | <span data-ttu-id="53f62-114">Controle a tolerância de um processador de áudio quando ele corresponde a taxas com outro relógio.</span><span class="sxs-lookup"><span data-stu-id="53f62-114">Control the tolerance of an audio renderer when it matches rates with another clock.</span></span>                                                                      |
| [<span data-ttu-id="53f62-115">**IAMDirectSound**</span><span class="sxs-lookup"><span data-stu-id="53f62-115">**IAMDirectSound**</span></span>](/previous-versions/windows/desktop/api/Amaudio/nn-amaudio-iamdirectsound)               | <span data-ttu-id="53f62-116">Permite que um aplicativo especifique qual janela tem o foco para controlar a reprodução de áudio DirectSound.</span><span class="sxs-lookup"><span data-stu-id="53f62-116">Enables an application to specify which window has focus for controlling DirectSound audio playback.</span></span>                                                      |
| [<span data-ttu-id="53f62-117">**IAMResourceControl**</span><span class="sxs-lookup"><span data-stu-id="53f62-117">**IAMResourceControl**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamresourcecontrol)       | <span data-ttu-id="53f62-118">Mantenha um recurso de dispositivo de áudio antes que ele seja necessário.</span><span class="sxs-lookup"><span data-stu-id="53f62-118">Hold an audio device resource before it is needed.</span></span>                                                                                                        |
| [<span data-ttu-id="53f62-119">**IAMStreamConfig**</span><span class="sxs-lookup"><span data-stu-id="53f62-119">**IAMStreamConfig**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig)             | <span data-ttu-id="53f62-120">Consulte e defina o formato de saída do filtro de captura.</span><span class="sxs-lookup"><span data-stu-id="53f62-120">Query and set the capture filter's output format.</span></span>                                                                                                         |
| [<span data-ttu-id="53f62-121">**IBasicAudio**</span><span class="sxs-lookup"><span data-stu-id="53f62-121">**IBasicAudio**</span></span>](/windows/desktop/api/Control/nn-control-ibasicaudio)                     | <span data-ttu-id="53f62-122">Defina o volume e o saldo de saída de áudio.</span><span class="sxs-lookup"><span data-stu-id="53f62-122">Set audio output volume and balance.</span></span>                                                                                                                      |



 

## <a name="related-topics"></a><span data-ttu-id="53f62-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="53f62-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="53f62-124">Interfaces</span><span class="sxs-lookup"><span data-stu-id="53f62-124">Interfaces</span></span>](interfaces.md)
</dt> </dl>

 

 



