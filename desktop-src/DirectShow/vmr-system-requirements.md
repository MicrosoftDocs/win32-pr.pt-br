---
description: Requisitos do sistema do VMR
ms.assetid: fd50b312-73f0-4c68-a8b1-3497d958bc8f
title: Requisitos do sistema do VMR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99d54d6d1604c3e514f3ceef379eaba4a8fa1ee1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170263"
---
# <a name="vmr-system-requirements"></a><span data-ttu-id="96b89-103">Requisitos do sistema do VMR</span><span class="sxs-lookup"><span data-stu-id="96b89-103">VMR System Requirements</span></span>

<span data-ttu-id="96b89-104">O VMR usa exclusivamente os recursos de processamento de gráficos do cartão de vídeo do computador; o VMR não executa nenhuma mistura ou renderização de vídeo usando o processador do host, pois isso afetaria muito a taxa de quadros e a qualidade do vídeo que está sendo exibido.</span><span class="sxs-lookup"><span data-stu-id="96b89-104">The VMR uses the graphics-processing capabilities of the computer's display card exclusively; the VMR does not perform any blending or rendering of video using the host processor, because to do so would greatly impact the frame rate and quality of the video being displayed.</span></span> <span data-ttu-id="96b89-105">Ao aproveitar os novos recursos oferecidos pelo VMR, particularmente mesclagem de vários fluxos de vídeo e/ou imagens de aplicativos, o desempenho geral obtido é altamente dependente dos recursos da placa gráfica que está sendo usada no computador.</span><span class="sxs-lookup"><span data-stu-id="96b89-105">When taking advantage of the new features offered by the VMR, particularly blending of multiple video streams and/or application images, the overall performance obtained is highly dependent on the capabilities of the graphics card being used on the computer.</span></span> <span data-ttu-id="96b89-106">As placas gráficas que executam bem com o VMR têm o seguinte suporte de hardware interno:</span><span class="sxs-lookup"><span data-stu-id="96b89-106">Graphics cards that perform well with the VMR have the following hardware support built into them:</span></span>

-   <span data-ttu-id="96b89-107">Suporte para superfícies de textura de Direct3D e "sem energia de 2".</span><span class="sxs-lookup"><span data-stu-id="96b89-107">Support for YUV and "non-power of 2" Direct3D texture surfaces.</span></span>
-   <span data-ttu-id="96b89-108">A capacidade de StretchBlt das superfícies de YUV para RGB do DirectDraw.</span><span class="sxs-lookup"><span data-stu-id="96b89-108">The ability to StretchBlt from YUV to RGB DirectDraw surfaces.</span></span>
-   <span data-ttu-id="96b89-109">Pelo menos 16MB de memória de vídeo se vários fluxos de vídeo forem mesclados juntos.</span><span class="sxs-lookup"><span data-stu-id="96b89-109">At least 16MB of video memory if multiple video streams are to be blended together.</span></span> <span data-ttu-id="96b89-110">A quantidade real de memória necessária depende do tamanho da imagem dos fluxos de vídeo e da resolução do modo de exibição que está sendo usado.</span><span class="sxs-lookup"><span data-stu-id="96b89-110">The actual amount of memory required is dependent on the image size of the video streams and resolution of the display mode being used.</span></span>
-   <span data-ttu-id="96b89-111">Suporte para uma sobreposição RGB ou a capacidade de misturar para uma superfície de sobreposição YUV.</span><span class="sxs-lookup"><span data-stu-id="96b89-111">Support for an RGB overlay or the ability to blend to a YUV overlay surface.</span></span>
-   <span data-ttu-id="96b89-112">Vídeo acelerado por hardware (suporte para aceleração de vídeo do DirectX) decodificação.</span><span class="sxs-lookup"><span data-stu-id="96b89-112">Hardware-accelerated video (support for DirectX Video Acceleration) decoding.</span></span>
-   <span data-ttu-id="96b89-113">Taxas de preenchimento de pixel alto.</span><span class="sxs-lookup"><span data-stu-id="96b89-113">High pixel fill rates.</span></span>

> [!Note]  
> <span data-ttu-id="96b89-114">O VMR requer que o monitor do sistema seja definido para uma profundidade de cor de pelo menos 16 bits.</span><span class="sxs-lookup"><span data-stu-id="96b89-114">The VMR requires that the system monitor be set for a color depth of at least 16 bits.</span></span> <span data-ttu-id="96b89-115">O VMR não poderá ser colocado em um estado de execução se o monitor estiver definido para 256 cores.</span><span class="sxs-lookup"><span data-stu-id="96b89-115">The VMR cannot be put into a run state if the monitor is set for 256 colors.</span></span> <span data-ttu-id="96b89-116">Além disso, algumas placas de vídeo não podem executar operações de Direct3D quando a exibição é definida como 24 bits por pixel.</span><span class="sxs-lookup"><span data-stu-id="96b89-116">Also, some video cards cannot perform Direct3D operations when the display is set to 24 bits per pixel.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="96b89-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="96b89-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="96b89-118">Sobre o processamento de mixagem de vídeo</span><span class="sxs-lookup"><span data-stu-id="96b89-118">About the Video Mixing Render</span></span>](about-the-video-mixing-render.md)
</dt> </dl>

 

 



