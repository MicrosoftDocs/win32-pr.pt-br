---
description: Sobre a API de transcodificação
ms.assetid: 54733364-f10c-4c1d-9800-75e283ba4be4
title: Sobre a API de transcodificação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30d2d49a33a97bbb538888173db78705061583ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104571069"
---
# <a name="about-the-transcode-api"></a><span data-ttu-id="e5d28-103">Sobre a API de transcodificação</span><span class="sxs-lookup"><span data-stu-id="e5d28-103">About the Transcode API</span></span>

<span data-ttu-id="e5d28-104">O diagrama a seguir mostra como a API de transcodificação está relacionada ao restante do pipeline de codificação de Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="e5d28-104">The following diagram shows how the transcode API relates to the rest of the Media Foundation encoding pipeline.</span></span>

![um diagrama que mostra a API de transcodificação.](images/encoding08.png)

<span data-ttu-id="e5d28-106">O pipeline de codificação contém os seguintes objetos de processamento de dados:</span><span class="sxs-lookup"><span data-stu-id="e5d28-106">The encoding pipeline contains the following data-processing objects:</span></span>

-   <span data-ttu-id="e5d28-107">Origem da mídia</span><span class="sxs-lookup"><span data-stu-id="e5d28-107">Media source</span></span>
-   <span data-ttu-id="e5d28-108">Decodificador</span><span class="sxs-lookup"><span data-stu-id="e5d28-108">Decoder</span></span>
-   <span data-ttu-id="e5d28-109">Redimensionador de vídeo ou reamostrador de áudio</span><span class="sxs-lookup"><span data-stu-id="e5d28-109">Video resizer or audio resampler</span></span>
-   <span data-ttu-id="e5d28-110">Codificador</span><span class="sxs-lookup"><span data-stu-id="e5d28-110">Encoder</span></span>
-   <span data-ttu-id="e5d28-111">Coletor de mídia</span><span class="sxs-lookup"><span data-stu-id="e5d28-111">Media sink</span></span>

<span data-ttu-id="e5d28-112">O redimensionador de vídeo será necessário somente se o tamanho do vídeo de saída diferir da origem.</span><span class="sxs-lookup"><span data-stu-id="e5d28-112">The video resizer is needed only if the size of the output video differs from the source.</span></span> <span data-ttu-id="e5d28-113">O reamostrador de áudio será necessário somente se o áudio precisar ser reamostrado antes da codificação.</span><span class="sxs-lookup"><span data-stu-id="e5d28-113">The audio resampler is needed only if the audio needs to be resampled before encoding.</span></span> <span data-ttu-id="e5d28-114">O par de decodificador/codificador é necessário para transcodificação, mas não para remuxing.</span><span class="sxs-lookup"><span data-stu-id="e5d28-114">The decoder/encoder pair is required for transcoding, but not for remuxing.</span></span>

<span data-ttu-id="e5d28-115">A *topologia* de codificação é o conjunto de objetos de pipeline (origem, decodificador, redimensionador, reamostrador, codificador e coletor de mídia), além dos pontos de conexão entre eles.</span><span class="sxs-lookup"><span data-stu-id="e5d28-115">The encoding *topology* is the set of pipeline objects (source, decoder, resizer, resampler, encoder, and media sink), plus the connection points between them.</span></span> <span data-ttu-id="e5d28-116">Para obter mais informações sobre topologias, consulte [topologias](topologies.md).</span><span class="sxs-lookup"><span data-stu-id="e5d28-116">For more information about topologies, see [Topologies](topologies.md).</span></span>

<span data-ttu-id="e5d28-117">Componentes diferentes são responsáveis por criar os vários objetos de pipeline:</span><span class="sxs-lookup"><span data-stu-id="e5d28-117">Different components are responsible for creating the various pipeline objects:</span></span>

-   <span data-ttu-id="e5d28-118">O aplicativo normalmente usa o [resolvedor de origem](source-resolver.md) para criar a origem da mídia.</span><span class="sxs-lookup"><span data-stu-id="e5d28-118">The application typically uses the [Source Resolver](source-resolver.md) to create the media source.</span></span>
-   <span data-ttu-id="e5d28-119">A [sessão de mídia](media-session.md) carrega e configura o decodificador, o redimensionador de vídeo e o reamostrador de áudio.</span><span class="sxs-lookup"><span data-stu-id="e5d28-119">The [Media Session](media-session.md) loads and configures the decoder, video resizer, and audio resampler.</span></span> <span data-ttu-id="e5d28-120">Internamente, ele usa o carregador de topologia para fazer isso (consulte [**IMFTopoLoader**](/windows/desktop/api/mfidl/nn-mfidl-imftopoloader)).</span><span class="sxs-lookup"><span data-stu-id="e5d28-120">Internally, it uses the topology loader to do this (see [**IMFTopoLoader**](/windows/desktop/api/mfidl/nn-mfidl-imftopoloader)).</span></span>
-   <span data-ttu-id="e5d28-121">A API de transcodificação carrega e configura o codificador e o coletor de mídia.</span><span class="sxs-lookup"><span data-stu-id="e5d28-121">The transcode API loads and configures the encoder and the media sink.</span></span>

<span data-ttu-id="e5d28-122">Os aplicativos avançados podem configurar o codificador e o coletor de mídia diretamente, em vez de usar a API de transcodificação.</span><span class="sxs-lookup"><span data-stu-id="e5d28-122">Advanced applications can configure the encoder and the media sink directly, rather than using the transcode API.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e5d28-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e5d28-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e5d28-124">API de transcodificação</span><span class="sxs-lookup"><span data-stu-id="e5d28-124">Transcode API</span></span>](transcode-api.md)
</dt> <dt>

[<span data-ttu-id="e5d28-125">Usando a API de transcodificação</span><span class="sxs-lookup"><span data-stu-id="e5d28-125">Using the Transcode API</span></span>](fast-transcode-objects.md)
</dt> </dl>

 

 



