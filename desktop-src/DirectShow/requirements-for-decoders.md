---
description: Requisitos para decodificadores
ms.assetid: 149aea20-0d37-4b1c-a098-8446c4088ce1
title: Requisitos para decodificadores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 461120bec88636e4c015c2e319d855571e8ac1b8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104456557"
---
# <a name="requirements-for-decoders"></a><span data-ttu-id="9d6a8-103">Requisitos para decodificadores</span><span class="sxs-lookup"><span data-stu-id="9d6a8-103">Requirements for Decoders</span></span>

<span data-ttu-id="9d6a8-104">Os decodificadores que fornecem amostras para o VMR devem observar as seguintes regras:</span><span class="sxs-lookup"><span data-stu-id="9d6a8-104">Decoders that deliver samples to the VMR must observe the following rules:</span></span>

-   <span data-ttu-id="9d6a8-105">Deve haver um quadro de subimagem entregue ao VMR para cada quadro de vídeo.</span><span class="sxs-lookup"><span data-stu-id="9d6a8-105">There should be one subpicture frame delivered to the VMR for each video frame.</span></span> <span data-ttu-id="9d6a8-106">Os dois quadros devem ter os mesmos carimbos de data/hora.</span><span class="sxs-lookup"><span data-stu-id="9d6a8-106">The two frames should have the same time stamps.</span></span>
-   <span data-ttu-id="9d6a8-107">Se a subimagem não tiver sido alterada, use o \_ sinalizador am gbf \_ NOTASYNCPOINT no método [**IMemAllocator:: GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) para forçar o alocador a retornar um buffer que contém o último quadro entregue ao VMR.</span><span class="sxs-lookup"><span data-stu-id="9d6a8-107">If the subpicture has not changed, use the AM\_GBF\_NOTASYNCPOINT flag in the [**IMemAllocator::GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) method to force the allocator to return a buffer containing the last frame delivered to the VMR.</span></span> <span data-ttu-id="9d6a8-108">Basta colocar um novo carimbo de data/hora no exemplo e entregá-lo ao VMR novamente.</span><span class="sxs-lookup"><span data-stu-id="9d6a8-108">Just put a new time stamp on the sample and deliver it to the VMR again.</span></span> <span data-ttu-id="9d6a8-109">Se a fama da subimagem estiver em branco, você ainda deverá entregá-la.</span><span class="sxs-lookup"><span data-stu-id="9d6a8-109">If the subpicture fame is blank, you should still deliver it.</span></span> <span data-ttu-id="9d6a8-110">O VMR detectará o quadro vazio e não o mesclará com o vídeo.</span><span class="sxs-lookup"><span data-stu-id="9d6a8-110">The VMR will detect the empty frame and not blend it with the video.</span></span> <span data-ttu-id="9d6a8-111">Esse teste é executado pelo chip VGA e não afeta o desempenho da reprodução.</span><span class="sxs-lookup"><span data-stu-id="9d6a8-111">This test is performed by the VGA chip and does not affect the playback performance.</span></span>
-   <span data-ttu-id="9d6a8-112">Todos os exemplos, exceto para transmissões ao vivo, devem ter carimbos de hora de início e parada válidos anexados.</span><span class="sxs-lookup"><span data-stu-id="9d6a8-112">All samples, except for live streams, must have valid start and stop time stamps attached.</span></span> <span data-ttu-id="9d6a8-113">(O DVD não é um fluxo ao vivo.)</span><span class="sxs-lookup"><span data-stu-id="9d6a8-113">(DVD is not a live stream.)</span></span>
-   <span data-ttu-id="9d6a8-114">Os carimbos de data/hora de exemplo de mídia devem ser contíguos</span><span class="sxs-lookup"><span data-stu-id="9d6a8-114">The media sample time stamps must be contiguous</span></span>
-   <span data-ttu-id="9d6a8-115">O decodificador deve se identificar como compatível com o VMR para uso por construtores de grafo.</span><span class="sxs-lookup"><span data-stu-id="9d6a8-115">The decoder must identify itself as VMR-capable for use by graph builders.</span></span>
-   <span data-ttu-id="9d6a8-116">O fluxo de subimagem agora deve conter valores Alfa inseridos por pixel.</span><span class="sxs-lookup"><span data-stu-id="9d6a8-116">The subpicture stream should now contain embedded per-pixel alpha values.</span></span> <span data-ttu-id="9d6a8-117">O tipo de superfície ARGB4444 é ideal para subimagems.</span><span class="sxs-lookup"><span data-stu-id="9d6a8-117">The ARGB4444 surface type is ideal for subpictures.</span></span>
-   <span data-ttu-id="9d6a8-118">Não assuma que o stride da subimagem seja igual à largura da superfície.</span><span class="sxs-lookup"><span data-stu-id="9d6a8-118">Do not assume that the stride of the subpicture is the same as the surface width.</span></span> <span data-ttu-id="9d6a8-119">Isso nem sempre acontece com o VMR.</span><span class="sxs-lookup"><span data-stu-id="9d6a8-119">This is not always the case with the VMR.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9d6a8-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9d6a8-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9d6a8-121">Sobre a aceleração de vídeo do DirectX</span><span class="sxs-lookup"><span data-stu-id="9d6a8-121">About DirectX Video Acceleration</span></span>](about-directx-video-acceleration.md)
</dt> </dl>

 

 



