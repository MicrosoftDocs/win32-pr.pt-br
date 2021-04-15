---
description: Componentes de filtro do VMR
ms.assetid: 86fd8d6f-a742-457d-bb30-d04542431a0a
title: Componentes de filtro do VMR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b597f6ac1b52f81ddc26d18e3fe0c6d16bae9515
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104506013"
---
# <a name="vmr-filter-components"></a><span data-ttu-id="1b299-103">Componentes de filtro do VMR</span><span class="sxs-lookup"><span data-stu-id="1b299-103">VMR Filter Components</span></span>

<span data-ttu-id="1b299-104">O VMR emprega um design modular que permite aos aplicativos configurá-lo para vários cenários de renderização diferentes.</span><span class="sxs-lookup"><span data-stu-id="1b299-104">The VMR employs a modular design that enables applications to configure it for many different rendering scenarios.</span></span> <span data-ttu-id="1b299-105">Dependendo de sua configuração, o VMR contém de dois a cinco subcomponentes (além de seus PINs de entrada).</span><span class="sxs-lookup"><span data-stu-id="1b299-105">Depending on its configuration, the VMR contains from two to five subcomponents (in addition to its input pins).</span></span>

![VMR no modo de janela com vários fluxos](images/vmr-multiple-streams.png)

<span data-ttu-id="1b299-107">**Mixer:** O Mixer é um objeto COM responsável por misturar vários fluxos.</span><span class="sxs-lookup"><span data-stu-id="1b299-107">**Mixer:** The mixer is a COM object responsible for mixing multiple streams.</span></span> <span data-ttu-id="1b299-108">O desentrelaçamento também ocorre dentro do mixer.</span><span class="sxs-lookup"><span data-stu-id="1b299-108">Deinterlacing also occurs inside the mixer.</span></span> <span data-ttu-id="1b299-109">O Mixer é carregado pelo VMR quando vários fluxos de entrada são detectados ou quando o vídeo de entrada é entrelaçado.</span><span class="sxs-lookup"><span data-stu-id="1b299-109">The mixer is loaded by the VMR when multiple input streams are detected, or when the input video is interlaced.</span></span> <span data-ttu-id="1b299-110">O mixer coleta informações sobre cada fluxo de entrada e classifica os fluxos na ordem Z correta.</span><span class="sxs-lookup"><span data-stu-id="1b299-110">The mixer collects information about each input stream and sorts the streams into the correct Z-order.</span></span> <span data-ttu-id="1b299-111">Ele é responsável por determinar quando cada PIN de entrada recebe um exemplo e para instruir o compositor da imagem no momento adequado para executar a mistura real.</span><span class="sxs-lookup"><span data-stu-id="1b299-111">It is responsible for determining when each input pin receives a sample, and for instructing the image compositor at the proper time to perform the actual blending.</span></span> <span data-ttu-id="1b299-112">O mixer também calcula o carimbo de data/hora a ser aplicado a cada imagem de saída.</span><span class="sxs-lookup"><span data-stu-id="1b299-112">The mixer also calculates the time stamp to be applied to each output image.</span></span> <span data-ttu-id="1b299-113">Quando o aplicativo está fornecendo um bitmap a ser exibido na parte superior da imagem compostada, o Mixer é responsável por garantir que o bitmap seja exibido na parte superior, mesmo que a ordem Z dos fluxos de entrada seja modificada.</span><span class="sxs-lookup"><span data-stu-id="1b299-113">When the application is supplying a bitmap to be displayed on top of the composited image, the mixer is responsible for ensuring that the bitmap is displayed on top even if the Z-order of the input streams is modified.</span></span>

<span data-ttu-id="1b299-114">**Compositor da imagem:** O compositor da imagem é um objeto COM que executa a mistura real dos fluxos de entrada em uma única superfície do DirectDraw ou do Direct3D fornecida pelo alocador de dados.</span><span class="sxs-lookup"><span data-stu-id="1b299-114">**Image Compositor:** The Image Compositor is a COM object that performs the actual blending of the input streams onto a single DirectDraw or Direct3D surface provided by the allocator-presenter.</span></span> <span data-ttu-id="1b299-115">O VMR fornece um compositor de imagem padrão que permite que os aplicativos executem efeitos de mesclagem alfa 2-D.</span><span class="sxs-lookup"><span data-stu-id="1b299-115">The VMR provides a default image compositor that enables applications to perform 2-D alpha-blending effects.</span></span> <span data-ttu-id="1b299-116">Os aplicativos podem fornecer um compositor de imagem personalizada para habilitar outros efeitos 2D e 3, como aplicar texturas a partes da imagem, mesclagem alfa por pixel, mapeando a imagem para objetos de 3D ou movendo-D e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="1b299-116">Applications can provide a custom image compositor to enable other 2-D and 3-D effects, such as applying textures to portions of the image, per-pixel alpha blending, mapping the image to stationary or moving 3-D objects, and so on.</span></span>

<span data-ttu-id="1b299-117">**Alocador-apresentador:** O alocador-Presenter é um objeto COM que aloca o objeto DirectDraw ou Direct3D e manipula a comunicação com a placa gráfica.</span><span class="sxs-lookup"><span data-stu-id="1b299-117">**Allocator-Presenter:** The allocator-presenter is a COM object that allocates the DirectDraw or Direct3D object and handles the communication with the graphics card.</span></span> <span data-ttu-id="1b299-118">O desenho pode ser executado como um flip ou como um blit.</span><span class="sxs-lookup"><span data-stu-id="1b299-118">The drawing can be performed either as a flip or as a blit.</span></span> <span data-ttu-id="1b299-119">Você pode conectar seu próprio apresentador de alocador para criar e controlar o objeto DirectDraw ou Direct3D e/ou para obter acesso aos bits de vídeo no momento da apresentação.</span><span class="sxs-lookup"><span data-stu-id="1b299-119">You can plug in your own allocator-presenter in order to create and control the DirectDraw or Direct3D object, and/or to obtain access to the video bits at presentation time.</span></span>

<span data-ttu-id="1b299-120">**Gerenciador de janelas:** O Gerenciador de janelas é usado apenas no modo de janela.</span><span class="sxs-lookup"><span data-stu-id="1b299-120">**Window Manager:** The Window Manager is used only in windowed mode.</span></span> <span data-ttu-id="1b299-121">O Gerenciador de janelas dá suporte às interfaces herdadas [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) e [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) para compatibilidade com versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="1b299-121">The Window Manager supports the legacy [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) and [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) interfaces for backward-compatibility.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1b299-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1b299-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1b299-123">Sobre o processamento de mixagem de vídeo</span><span class="sxs-lookup"><span data-stu-id="1b299-123">About the Video Mixing Render</span></span>](about-the-video-mixing-render.md)
</dt> </dl>

 

 



