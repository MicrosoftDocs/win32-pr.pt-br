---
description: Capturar DV para o arquivo
ms.assetid: f7a8bcbb-a744-43c4-a226-354ae2d94df8
title: Capturar DV para o arquivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 713e49eba3016b353362c541ba31ffd6a1ae5de7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104296032"
---
# <a name="capture-dv-to-file"></a><span data-ttu-id="8dcc0-103">Capturar DV para o arquivo</span><span class="sxs-lookup"><span data-stu-id="8dcc0-103">Capture DV to File</span></span>

<span data-ttu-id="8dcc0-104">Esta seção descreve como capturar vídeo digital (DV) de uma câmera DV ou de uma fita VTR.</span><span class="sxs-lookup"><span data-stu-id="8dcc0-104">This section describes how to capture digital video (DV) from a DV camera or from a VTR tape.</span></span>

1.  <span data-ttu-id="8dcc0-105">Crie uma instância do filtro de [Driver MSDV](msdv-driver.md) .</span><span class="sxs-lookup"><span data-stu-id="8dcc0-105">Create an instance of the [MSDV Driver](msdv-driver.md) filter.</span></span> <span data-ttu-id="8dcc0-106">Para obter mais informações, consulte [selecionando um dispositivo de captura](selecting-a-capture-device.md).</span><span class="sxs-lookup"><span data-stu-id="8dcc0-106">For more information, see [Selecting a Capture Device](selecting-a-capture-device.md).</span></span>
2.  <span data-ttu-id="8dcc0-107">Inicialize o construtor de gráficos de captura, conforme descrito em [sobre o construtor de grafo de captura](about-the-capture-graph-builder.md).</span><span class="sxs-lookup"><span data-stu-id="8dcc0-107">Initialize the Capture Graph Builder, as described in [About the Capture Graph Builder](about-the-capture-graph-builder.md).</span></span>
3.  <span data-ttu-id="8dcc0-108">Compile o grafo de captura, dependendo do tipo de arquivo de destino:</span><span class="sxs-lookup"><span data-stu-id="8dcc0-108">Build the capture graph, depending on the target file type:</span></span>
    -   [<span data-ttu-id="8dcc0-109">Capturar um arquivo DV tipo-1</span><span class="sxs-lookup"><span data-stu-id="8dcc0-109">Capture a Type-1 DV File</span></span>](capture-a-type-1-dv-file.md)
    -   [<span data-ttu-id="8dcc0-110">Capturar um arquivo DV tipo-2</span><span class="sxs-lookup"><span data-stu-id="8dcc0-110">Capture a Type-2 DV File</span></span>](capture-a-type-2-dv-file.md)
    -   [<span data-ttu-id="8dcc0-111">Capturar DV para RGB descompactado</span><span class="sxs-lookup"><span data-stu-id="8dcc0-111">Capture DV to Uncompressed RGB</span></span>](capture-dv-to-uncompressed-rgb.md)
4.  <span data-ttu-id="8dcc0-112">Execute o grafo.</span><span class="sxs-lookup"><span data-stu-id="8dcc0-112">Run the graph.</span></span>

<span data-ttu-id="8dcc0-113">A captura de uma fita VTR funciona exatamente como a captura de vídeo ao vivo da câmera, exceto que você deve reproduzir a fita, conforme descrito em [controlando uma camcorder DV](controlling-a-dv-camcorder.md).</span><span class="sxs-lookup"><span data-stu-id="8dcc0-113">Capturing from a VTR tape works just like capturing live video from the camera, except that you must play the tape, as described in [Controlling a DV Camcorder](controlling-a-dv-camcorder.md).</span></span> <span data-ttu-id="8dcc0-114">Para evitar a perda de quadros, execute o grafo primeiro e, em seguida, reproduza a fita.</span><span class="sxs-lookup"><span data-stu-id="8dcc0-114">To avoid losing any frames, run the graph first, and then play the tape.</span></span> <span data-ttu-id="8dcc0-115">Quando terminar de transmitir, pare a fita primeiro e, em seguida, pare o grafo.</span><span class="sxs-lookup"><span data-stu-id="8dcc0-115">When you are done transmitting, stop the tape first and then stop the graph.</span></span>

> [!Note]  
> <span data-ttu-id="8dcc0-116">A camcorder deve estar no modo VTR.</span><span class="sxs-lookup"><span data-stu-id="8dcc0-116">The camcorder must be in VTR mode.</span></span> <span data-ttu-id="8dcc0-117">Consulte [modo de dispositivo](device-mode.md).</span><span class="sxs-lookup"><span data-stu-id="8dcc0-117">See [Device Mode](device-mode.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="8dcc0-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8dcc0-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8dcc0-119">Vídeo digital no DirectShow</span><span class="sxs-lookup"><span data-stu-id="8dcc0-119">Digital Video in DirectShow</span></span>](digital-video-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="8dcc0-120">Tipos-1 vs. tipo-2 arquivos AVI de DV</span><span class="sxs-lookup"><span data-stu-id="8dcc0-120">Type-1 vs. Type-2 DV AVI Files</span></span>](type-1-vs--type-2-dv-avi-files.md)
</dt> <dt>

[<span data-ttu-id="8dcc0-121">Captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="8dcc0-121">Video Capture</span></span>](video-capture.md)
</dt> </dl>

 

 



