---
description: Televisão analógica
ms.assetid: 9f2c18ec-3684-42a8-a3df-5f8827b27642
title: Televisão analógica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33af8ba94831afed59d783598dbf6bc0eaee0ec6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087516"
---
# <a name="analog-television"></a><span data-ttu-id="bee5a-103">Televisão analógica</span><span class="sxs-lookup"><span data-stu-id="bee5a-103">Analog Television</span></span>

<span data-ttu-id="bee5a-104">A televisão analógica difere de outros cenários de captura de vídeo de várias maneiras:</span><span class="sxs-lookup"><span data-stu-id="bee5a-104">Analog television differs from other video capture scenarios in several ways:</span></span>

-   <span data-ttu-id="bee5a-105">O cartão sintonizador ajusta-se a um sinal analógico, que é então digitalizado.</span><span class="sxs-lookup"><span data-stu-id="bee5a-105">The tuner card tunes to an analog signal, which is then digitized.</span></span>
-   <span data-ttu-id="bee5a-106">O áudio é transportado no sinal analógico.</span><span class="sxs-lookup"><span data-stu-id="bee5a-106">Audio is carried in the analog signal.</span></span> <span data-ttu-id="bee5a-107">A maneira como o áudio atinge a placa de som varia dependendo do hardware.</span><span class="sxs-lookup"><span data-stu-id="bee5a-107">How the audio reaches the sound card varies depending on the hardware.</span></span>
-   <span data-ttu-id="bee5a-108">O sinal pode conter dados adicionais no intervalo vertical em branco (VBI), como legendas codificadas (CC), teletexto mundial padrão (WST) e serviços de dados estendidos (XDS).</span><span class="sxs-lookup"><span data-stu-id="bee5a-108">The signal may contain additional data in the vertical blanking interval (VBI), such as closed captions (CC), World Standard Teletext (WST), and extended data services (XDS).</span></span>

<span data-ttu-id="bee5a-109">O diagrama a seguir mostra um grafo de filtro típico para visualização de televisão.</span><span class="sxs-lookup"><span data-stu-id="bee5a-109">The following diagram shows a typical filter graph for television preview.</span></span>

![gráfico de televisão analógica](images/vidcap06.png)

-   <span data-ttu-id="bee5a-111">O filtro de [sintonizador de TV](tv-tuner-filter.md) controla o ajuste.</span><span class="sxs-lookup"><span data-stu-id="bee5a-111">The [TV Tuner](tv-tuner-filter.md) filter controls tuning.</span></span>
-   <span data-ttu-id="bee5a-112">O filtro de [áudio de TV](tv-audio-filter.md) controla a decodificação de áudio.</span><span class="sxs-lookup"><span data-stu-id="bee5a-112">The [TV Audio](tv-audio-filter.md) filter controls the audio decoding.</span></span>
-   <span data-ttu-id="bee5a-113">Se o cartão sintonizador tiver mais de uma entrada física, o filtro [Crossbar de vídeo analógico](analog-video-crossbar-filter.md) permitirá que o aplicativo selecione qual entrada é decodificada e renderizada.</span><span class="sxs-lookup"><span data-stu-id="bee5a-113">If the tuner card has more than one physical input, the [Analog Video Crossbar](analog-video-crossbar-filter.md) filter enables the application to select which input is decoded and rendered.</span></span>
-   <span data-ttu-id="bee5a-114">O filtro de [captura de vídeo WDM](wdm-video-capture-filter.md) entrega o fluxo de vídeo digitalizado.</span><span class="sxs-lookup"><span data-stu-id="bee5a-114">The [WDM Video Capture](wdm-video-capture-filter.md) filter delivers the digitized video stream.</span></span>

<span data-ttu-id="bee5a-115">O construtor de grafo de captura insere automaticamente todos os filtros necessários para o upstream a partir do filtro de captura.</span><span class="sxs-lookup"><span data-stu-id="bee5a-115">The Capture Graph Builder automatically inserts any filters that are required upstream from the capture filter.</span></span>

<span data-ttu-id="bee5a-116">Esta seção contém os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="bee5a-116">This section contains the following topics:</span></span>

-   [<span data-ttu-id="bee5a-117">Ajuste de televisão analógica</span><span class="sxs-lookup"><span data-stu-id="bee5a-117">Analog Television Tuning</span></span>](analog-television-tuning.md)
-   [<span data-ttu-id="bee5a-118">Áudio de televisão analógica</span><span class="sxs-lookup"><span data-stu-id="bee5a-118">Analog Television Audio</span></span>](analog-television-audio.md)
-   [<span data-ttu-id="bee5a-119">Legendas e teletextos codificados</span><span class="sxs-lookup"><span data-stu-id="bee5a-119">Closed Captions and Teletext</span></span>](closed-captions-and-teletext.md)

## <a name="related-topics"></a><span data-ttu-id="bee5a-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="bee5a-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bee5a-121">Captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="bee5a-121">Video Capture</span></span>](video-capture.md)
</dt> </dl>

 

 



