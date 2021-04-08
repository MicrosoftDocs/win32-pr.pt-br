---
description: Digite-1 vs.
ms.assetid: 3f1cf981-f678-46a6-9784-ffb389438b6d
title: Tipos-1 vs. tipo-2 arquivos AVI de DV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0000b81e94e25749b5590287145a88a28280e16d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103921920"
---
# <a name="type-1-vs-type-2-dv-avi-files"></a><span data-ttu-id="6ebed-103">Tipos-1 vs. tipo-2 arquivos AVI de DV</span><span class="sxs-lookup"><span data-stu-id="6ebed-103">Type-1 vs. Type-2 DV AVI Files</span></span>

<span data-ttu-id="6ebed-104">Câmeras de DV produzem áudio-vídeo intercalado; cada quadro de vídeo também contém as informações de áudio.</span><span class="sxs-lookup"><span data-stu-id="6ebed-104">DV cameras produce interleaved audio-video; each frame of video also contains the audio information.</span></span> <span data-ttu-id="6ebed-105">Se você salvar dados DV em um arquivo AVI, terá uma opção:</span><span class="sxs-lookup"><span data-stu-id="6ebed-105">If you save DV data to an AVI file, you have a choice:</span></span>

-   <span data-ttu-id="6ebed-106">Armazene os dados intercalados como um fluxo no arquivo AVI.</span><span class="sxs-lookup"><span data-stu-id="6ebed-106">Store the interleaved data as one stream in the AVI file.</span></span> <span data-ttu-id="6ebed-107">Isso é conhecido como um arquivo de tipo 1.</span><span class="sxs-lookup"><span data-stu-id="6ebed-107">This is known as a type-1 file.</span></span>
-   <span data-ttu-id="6ebed-108">Divida os dados intercalados em fluxos de áudio e vídeo separados.</span><span class="sxs-lookup"><span data-stu-id="6ebed-108">Split the interleaved data into separate audio and video streams.</span></span> <span data-ttu-id="6ebed-109">Isso é conhecido como um arquivo de tipo 2.</span><span class="sxs-lookup"><span data-stu-id="6ebed-109">This is known as a type-2 file.</span></span>

<span data-ttu-id="6ebed-110">Para captura de vídeo, em que a taxa de transferência máxima é crucial, é melhor usar um arquivo Type-1, pois os arquivos de tipo 2 contêm dados de áudio redundantes.</span><span class="sxs-lookup"><span data-stu-id="6ebed-110">For video capture, where maximum throughput is crucial, it is better to use a type-1 file, because type-2 files carry redundant audio data.</span></span> <span data-ttu-id="6ebed-111">(O fluxo de vídeo ainda tem os dados de áudio.</span><span class="sxs-lookup"><span data-stu-id="6ebed-111">(The video stream still has the audio data.</span></span> <span data-ttu-id="6ebed-112">O áudio é simplesmente ocultado ao rotular o fluxo como vídeo.) Além disso, gravar um arquivo de tipo 2 requer um tempo de processador adicional para dividir o fluxo intercalado.</span><span class="sxs-lookup"><span data-stu-id="6ebed-112">The audio is simply hidden by labeling the stream as video.) Also, writing a type-2 file requires some additional processor time to split the interleaved stream.</span></span>

<span data-ttu-id="6ebed-113">Por outro lado, os arquivos Type-1 são menos eficientes para a edição em tempo real.</span><span class="sxs-lookup"><span data-stu-id="6ebed-113">On the other hand, type-1 files are less efficient for real-time editing.</span></span> <span data-ttu-id="6ebed-114">O aplicativo deve extrair o áudio do fluxo intercalado, fazer as edições e intercalar os dados novamente.</span><span class="sxs-lookup"><span data-stu-id="6ebed-114">The application must extract the audio from the interleaved stream, make the edits, and interleave the data again.</span></span> <span data-ttu-id="6ebed-115">Além disso, o formato Type-1 não é compatível com o Microsoft® Video for Windows® (VFW).</span><span class="sxs-lookup"><span data-stu-id="6ebed-115">Also, the type-1 format is not compatible with Microsoft® Video for Windows® (VFW).</span></span> <span data-ttu-id="6ebed-116">O DirectShow pode lidar com os dois tipos de arquivos.</span><span class="sxs-lookup"><span data-stu-id="6ebed-116">DirectShow can handle both types of files.</span></span>

<span data-ttu-id="6ebed-117">Um arquivo de tipo 2 pode ser convertido para o tipo 1 usando o filtro [DV Muxer](dv-muxer-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="6ebed-117">A type-2 file can be converted to type-1 using the [DV Muxer](dv-muxer-filter.md) filter.</span></span> <span data-ttu-id="6ebed-118">Um arquivo Type-1 pode ser convertido para o tipo 2 usando o filtro de [Splitter de DV](dv-splitter-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="6ebed-118">A type-1 file can be converted to type-2 using the [DV Splitter](dv-splitter-filter.md) filter.</span></span> <span data-ttu-id="6ebed-119">O diagrama a seguir ilustra a diferença entre os dois formatos.</span><span class="sxs-lookup"><span data-stu-id="6ebed-119">The following diagram illustrates the difference between the two formats.</span></span>

![conversão entre o tipo-1 e o tipo-2 DV](images/dv-filters3.png)

## <a name="related-topics"></a><span data-ttu-id="6ebed-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6ebed-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6ebed-122">Vídeo digital no DirectShow</span><span class="sxs-lookup"><span data-stu-id="6ebed-122">Digital Video in DirectShow</span></span>](digital-video-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="6ebed-123">Dados de DV no formato de arquivo AVI</span><span class="sxs-lookup"><span data-stu-id="6ebed-123">DV Data in the AVI File Format</span></span>](dv-data-in-the-avi-file-format.md)
</dt> </dl>

 

 



