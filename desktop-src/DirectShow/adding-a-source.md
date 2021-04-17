---
description: Adicionando uma fonte
ms.assetid: 8c5d1050-a696-4a5d-be68-806420d0cd78
title: Adicionando uma fonte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee583cd8971c183f2e03b92f68e2d6ba555c41db
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105749647"
---
# <a name="adding-a-source"></a><span data-ttu-id="72dae-103">Adicionando uma fonte</span><span class="sxs-lookup"><span data-stu-id="72dae-103">Adding a Source</span></span>

<span data-ttu-id="72dae-104">\[Essa API não tem suporte e pode ser alterada ou não estar disponível no futuro.\]</span><span class="sxs-lookup"><span data-stu-id="72dae-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="72dae-105">Crie um objeto de origem da mesma maneira que cria outros objetos de linha do tempo.</span><span class="sxs-lookup"><span data-stu-id="72dae-105">Create a source object the same way you create other timeline objects.</span></span> <span data-ttu-id="72dae-106">Antes de inseri-lo na linha do tempo, no entanto, você deve especificar pelo menos as propriedades a seguir na origem.</span><span class="sxs-lookup"><span data-stu-id="72dae-106">Before inserting it into the timeline, however, you must specify at least the following properties on the source.</span></span>

-   <span data-ttu-id="72dae-107">Os horários de início e de término, em relação à linha do tempo.</span><span class="sxs-lookup"><span data-stu-id="72dae-107">The start and stop times, relative to the timeline.</span></span> <span data-ttu-id="72dae-108">Chame o método [**IAMTimelineObj:: SetStartStop**](iamtimelineobj-setstartstop.md) .</span><span class="sxs-lookup"><span data-stu-id="72dae-108">Call the [**IAMTimelineObj::SetStartStop**](iamtimelineobj-setstartstop.md) method.</span></span>
-   <span data-ttu-id="72dae-109">O arquivo de mídia a ser usado como origem.</span><span class="sxs-lookup"><span data-stu-id="72dae-109">The media file to use as a source.</span></span> <span data-ttu-id="72dae-110">Chame o método [**IAMTimelineSrc:: Setmedianame**](iamtimelinesrc-setmedianame.md) com uma cadeia de caracteres largo representando o nome do arquivo.</span><span class="sxs-lookup"><span data-stu-id="72dae-110">Call the [**IAMTimelineSrc::SetMediaName**](iamtimelinesrc-setmedianame.md) method with a wide-character string representing the name of the file.</span></span>
-   <span data-ttu-id="72dae-111">Os horários de início e de término da mídia, que são relativos ao arquivo original.</span><span class="sxs-lookup"><span data-stu-id="72dae-111">The media start and stop times, which are relative to the original file.</span></span> <span data-ttu-id="72dae-112">Chame o método [**IAMTimelineSrc:: SetMediaTimes**](iamtimelinesrc-setmediatimes.md) .</span><span class="sxs-lookup"><span data-stu-id="72dae-112">Call the [**IAMTimelineSrc::SetMediaTimes**](iamtimelinesrc-setmediatimes.md) method.</span></span> <span data-ttu-id="72dae-113">Para obter mais informações sobre os tempos de mídia, consulte [tempo em serviços de edição do DirectShow](time-in-directshow-editing-services.md).</span><span class="sxs-lookup"><span data-stu-id="72dae-113">For more information about media times, see [Time in DirectShow Editing Services](time-in-directshow-editing-services.md).</span></span>

<span data-ttu-id="72dae-114">No exemplo a seguir, o clipe de origem inicia quatro segundos no arquivo.</span><span class="sxs-lookup"><span data-stu-id="72dae-114">In the following example, the source clip starts four seconds into the file.</span></span> <span data-ttu-id="72dae-115">A duração da mídia é de 10 segundos, duas vezes o comprimento da duração da linha do tempo, o que significa que a fonte será reproduzida em duas vezes a velocidade normal.</span><span class="sxs-lookup"><span data-stu-id="72dae-115">The media duration is 10 seconds, twice the length of the timeline duration, meaning the source will play at twice normal speed.</span></span> <span data-ttu-id="72dae-116">As unidades de constante são definidas como 10 milhões (10 ^ 7) e são iguais a um segundo.</span><span class="sxs-lookup"><span data-stu-id="72dae-116">The constant UNITS is defined as 10000000 (10^7) and equals one second.</span></span>


```C++
pSourceObj->SetStartStop(0, 50000000)
BSTR bstrFile = SysAllocStringLen(OLESTR("C:\\example.avi"), 15);
pSource->SetMediaName(bstrFile); 
SysFreeString(bstrFile);
pSource->SetMediaTimes(40000000, 140000000);
```



> [!Note]  
> <span data-ttu-id="72dae-117">Atualmente, o DES não pode renderizar simultaneamente mais de 75 fontes que foram compactadas com codecs do VCM (Gerenciador de compactação de vídeo).</span><span class="sxs-lookup"><span data-stu-id="72dae-117">Currently, DES cannot simultaneously render more than 75 sources that were compressed with Video Compression Manager (VCM) codecs.</span></span> <span data-ttu-id="72dae-118">Além disso, se o projeto como um todo contiver mais de 75 fontes, você deverá usar a reconexão dinâmica ou o DES não poderá visualizar o projeto.</span><span class="sxs-lookup"><span data-stu-id="72dae-118">Also, if the project as a whole contains more than 75 such sources, you must use dynamic reconnection or DES cannot preview the project.</span></span> <span data-ttu-id="72dae-119">Para obter mais informações, consulte [**IRenderEngine:: SetDynamicReconnectLevel**](irenderengine-setdynamicreconnectlevel.md).</span><span class="sxs-lookup"><span data-stu-id="72dae-119">For more information, see [**IRenderEngine::SetDynamicReconnectLevel**](irenderengine-setdynamicreconnectlevel.md).</span></span>

 

<span data-ttu-id="72dae-120">Para obter mais informações sobre fontes, consulte [trabalhando com fontes](working-with-sources.md).</span><span class="sxs-lookup"><span data-stu-id="72dae-120">For more information about sources, see [Working with Sources](working-with-sources.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="72dae-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="72dae-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="72dae-122">Construindo uma linha do tempo</span><span class="sxs-lookup"><span data-stu-id="72dae-122">Constructing a Timeline</span></span>](constructing-a-timeline.md)
</dt> </dl>

 

 



