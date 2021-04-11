---
description: Aceleração de vídeo do DirectX 2,0
ms.assetid: acb73b20-89fa-4a48-be4a-846715a239b0
title: Aceleração de vídeo do DirectX 2,0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec3ae813d3c81ebcf753dcaa273cc9f9149eaab5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164190"
---
# <a name="directx-video-acceleration-20"></a><span data-ttu-id="a28f3-103">Aceleração de vídeo do DirectX 2,0</span><span class="sxs-lookup"><span data-stu-id="a28f3-103">DirectX Video Acceleration 2.0</span></span>

<span data-ttu-id="a28f3-104">A DXVA (aceleração de vídeo do DirectX) é uma API e uma DDI correspondente para usar a aceleração de hardware para acelerar o processamento do codec de vídeo.</span><span class="sxs-lookup"><span data-stu-id="a28f3-104">DirectX Video Acceleration (DXVA) is an API and a corresponding DDI for using hardware-acceleration to speed up video codec processing.</span></span> <span data-ttu-id="a28f3-105">Os codecs de software e os processadores de vídeo de software podem usar o DXVA para descarregar determinadas operações com uso intensivo de CPU para a GPU.</span><span class="sxs-lookup"><span data-stu-id="a28f3-105">Software codecs and software video processors can use DXVA to offload certain CPU-intensive operations to the GPU.</span></span> <span data-ttu-id="a28f3-106">Por exemplo, um decodificador de software pode descarregar a transformação de cosseno discreto inverso (iDCT) para a GPU.</span><span class="sxs-lookup"><span data-stu-id="a28f3-106">For example, a software decoder can offload the inverse discrete cosine transform (iDCT) to the GPU.</span></span>

<span data-ttu-id="a28f3-107">Esta seção contém os seguintes tópicos.</span><span class="sxs-lookup"><span data-stu-id="a28f3-107">This section contains the following topics.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="a28f3-108">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="a28f3-108">In this section</span></span>



| <span data-ttu-id="a28f3-109">Tópico</span><span class="sxs-lookup"><span data-stu-id="a28f3-109">Topic</span></span>                                                                                             | <span data-ttu-id="a28f3-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="a28f3-110">Description</span></span>                                                                                                                                                                                                      |
|---------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a28f3-111">Sobre o DXVA 2,0</span><span class="sxs-lookup"><span data-stu-id="a28f3-111">About DXVA 2.0</span></span>](about-dxva-2-0.md)<br/>                                                   | <span data-ttu-id="a28f3-112">Visão geral do DXVA 2 e sua relação com o DXVA 1.</span><span class="sxs-lookup"><span data-stu-id="a28f3-112">Overview of DXVA 2 and its relation to DXVA 1.</span></span><br/>                                                                                                                                                        |
| [<span data-ttu-id="a28f3-113">Gerenciador de Dispositivos Direct3D</span><span class="sxs-lookup"><span data-stu-id="a28f3-113">Direct3D Device Manager</span></span>](direct3d-device-manager.md)<br/>                                 | <span data-ttu-id="a28f3-114">O Microsoft Direct3D Device Manager permite que dois ou mais objetos compartilhem o mesmo dispositivo Microsoft Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="a28f3-114">The Microsoft Direct3D device manager enables two or more objects to share the same Microsoft Direct3D 9 device.</span></span><br/>                                                                                      |
| [<span data-ttu-id="a28f3-115">Suporte a DXVA 2,0 no DirectShow</span><span class="sxs-lookup"><span data-stu-id="a28f3-115">Supporting DXVA 2.0 in DirectShow</span></span>](supporting-dxva-2-0-in-directshow.md)<br/>             | <span data-ttu-id="a28f3-116">Este tópico descreve como dar suporte a DXVA (DirectX Video Acceleration) 2,0 em um filtro de decodificador do DirectShow.</span><span class="sxs-lookup"><span data-stu-id="a28f3-116">This topic describes how to support DirectX Video Acceleration (DXVA) 2.0 in a DirectShow decoder filter.</span></span><br/>                                                                                             |
| [<span data-ttu-id="a28f3-117">Suporte a DXVA 2,0 no Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a28f3-117">Supporting DXVA 2.0 in Media Foundation</span></span>](supporting-dxva-2-0-in-media-foundation.md)<br/> | <span data-ttu-id="a28f3-118">Este tópico descreve como dar suporte a DXVA (DirectX Video Acceleration) 2,0 em uma Media Foundation transformação (MFT) usando o Direct3D 9</span><span class="sxs-lookup"><span data-stu-id="a28f3-118">This topic describes how to support DirectX Video Acceleration (DXVA) 2.0 in a Media Foundation transform (MFT) using Direct3D 9</span></span><br/>                                                                      |
| [<span data-ttu-id="a28f3-119">Processamento de vídeo de DXVA</span><span class="sxs-lookup"><span data-stu-id="a28f3-119">DXVA Video Processing</span></span>](dxva-video-processing.md)<br/>                                     | <span data-ttu-id="a28f3-120">O processamento de vídeo de DXVA encapsula as funções do hardware de gráficos que são dedicadas ao processamento de imagens de vídeo descompactadas.</span><span class="sxs-lookup"><span data-stu-id="a28f3-120">DXVA video processing encapsulates the functions of the graphics hardware that are devoted to processing uncompressed video images.</span></span> <span data-ttu-id="a28f3-121">Os serviços de processamento de vídeo incluem desentrelaçamento e mixagem de vídeo.</span><span class="sxs-lookup"><span data-stu-id="a28f3-121">Video processing services include deinterlacing and video mixing.</span></span><br/> |
| [<span data-ttu-id="a28f3-122">DXVA-HD</span><span class="sxs-lookup"><span data-stu-id="a28f3-122">DXVA-HD</span></span>](dxva-hd.md)<br/>                                                                 | <span data-ttu-id="a28f3-123">A alta definição da aceleração de vídeo do Microsoft DirectX (DXVA-HD) é uma API para processamento de vídeo acelerado por hardware.</span><span class="sxs-lookup"><span data-stu-id="a28f3-123">Microsoft DirectX Video Acceleration High Definition (DXVA-HD) is an API for hardware-accelerated video processing.</span></span> <br/>                                                                                  |



 

## <a name="related-topics"></a><span data-ttu-id="a28f3-124">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a28f3-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a28f3-125">Guia de programação Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a28f3-125">Media Foundation Programming Guide</span></span>](media-foundation-programming-guide.md)
</dt> <dt>

[<span data-ttu-id="a28f3-126">Especificação de DXVA 1</span><span class="sxs-lookup"><span data-stu-id="a28f3-126">DXVA 1 Specification</span></span>](/windows-hardware/drivers/display/directx-video-acceleration)
</dt> </dl>

 

 
