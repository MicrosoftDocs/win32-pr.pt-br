---
description: Capturando um quadro de cartaz
ms.assetid: 0727a1ed-1bc7-49fc-a288-00283e637a71
title: Capturando um quadro de cartaz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2cf06a10d74bb6c81622ac9bad7a1b770f5dc12
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104456868"
---
# <a name="grabbing-a-poster-frame"></a><span data-ttu-id="93250-103">Capturando um quadro de cartaz</span><span class="sxs-lookup"><span data-stu-id="93250-103">Grabbing a Poster Frame</span></span>

<span data-ttu-id="93250-104">\[Essa API não tem suporte e pode ser alterada ou não estar disponível no futuro.\]</span><span class="sxs-lookup"><span data-stu-id="93250-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="93250-105">Este artigo descreve como exibir um quadro de cartaz de um arquivo de mídia digital, usando o objeto [detector de mídia (MediaDet)](media-detector--mediadet.md) fornecido com os [serviços de edição do DirectShow](directshow-editing-services.md).</span><span class="sxs-lookup"><span data-stu-id="93250-105">This article describes how to display a poster frame from a digital media file, using the [Media Detector (MediaDet)](media-detector--mediadet.md) object provided with [DirectShow Editing Services](directshow-editing-services.md).</span></span>

<span data-ttu-id="93250-106">O detector de mídia é um objeto auxiliar que pode obter informações de formato de um arquivo de origem de mídia.</span><span class="sxs-lookup"><span data-stu-id="93250-106">The Media Detector is a helper object that can get format information from a media source file.</span></span> <span data-ttu-id="93250-107">Ele também pode pegar uma imagem de bitmap de um fluxo de vídeo no arquivo de origem.</span><span class="sxs-lookup"><span data-stu-id="93250-107">It can also grab a bitmap image from a video stream in the source file.</span></span> <span data-ttu-id="93250-108">Supondo que o arquivo seja pesquisável, você pode obter a imagem de qualquer ponto no arquivo.</span><span class="sxs-lookup"><span data-stu-id="93250-108">Assuming the file is seekable, you can obtain the image from any point in the file.</span></span> <span data-ttu-id="93250-109">A imagem retornada sempre está no formato RGB de 24 bits.</span><span class="sxs-lookup"><span data-stu-id="93250-109">The returned image is always in 24-bit RGB format.</span></span>

<span data-ttu-id="93250-110">O detector de mídia não é um filtro e o aplicativo não precisa usar o Gerenciador de gráfico de filtro nem criar um gráfico de filtro.</span><span class="sxs-lookup"><span data-stu-id="93250-110">The Media Detector is not a filter, and the application does not need to use the Filter Graph Manager or create a filter graph.</span></span> <span data-ttu-id="93250-111">Internamente, o detector de mídia cria um gráfico de filtro que contém o [**filtro de apoio de exemplo**](sample-grabber-filter.md).</span><span class="sxs-lookup"><span data-stu-id="93250-111">Internally, the Media Detector creates a filter graph that contains the [**Sample Grabber Filter**](sample-grabber-filter.md).</span></span> <span data-ttu-id="93250-112">Para obter um bitmap, o detector de mídia busca e pausa o gráfico de filtro e, em seguida, recupera o bitmap do filtro de apoio de exemplo.</span><span class="sxs-lookup"><span data-stu-id="93250-112">To get a bitmap, the Media Detector seeks and pauses the filter graph, and then retrieves the bitmap from the Sample Grabber filter.</span></span> <span data-ttu-id="93250-113">O aplicativo se comunica com o detector de mídia por meio da interface [**IMediaDet**](imediadet.md) .</span><span class="sxs-lookup"><span data-stu-id="93250-113">The application communicates with the Media Detector through the [**IMediaDet**](imediadet.md) interface.</span></span> <span data-ttu-id="93250-114">O detector de mídia é um bom exemplo de encapsulamento de um grafo de filtro dentro de um objeto auxiliar, a fim de proteger aplicativos de detalhes relacionados ao grafo.</span><span class="sxs-lookup"><span data-stu-id="93250-114">The Media Detector is a good example of encapsulating a filter graph inside a helper object, in order to shield applications from graph-related details.</span></span>

<span data-ttu-id="93250-115">O detector de mídia opera em dois modos.</span><span class="sxs-lookup"><span data-stu-id="93250-115">The Media Detector operates in two modes.</span></span> <span data-ttu-id="93250-116">Ao criá-lo pela primeira vez, o detector de mídia está no modo de "coleta de informações".</span><span class="sxs-lookup"><span data-stu-id="93250-116">When you first create it, the Media Detector is in "information gathering" mode.</span></span> <span data-ttu-id="93250-117">Você pode especificar o nome de um arquivo de mídia e obter informações sobre cada um dos fluxos no arquivo, como o tipo de formato, a taxa de quadros ou a duração.</span><span class="sxs-lookup"><span data-stu-id="93250-117">You can specify the name of a media file and get information about each of the streams in the file, such as the format type, the frame rate, or the duration.</span></span> <span data-ttu-id="93250-118">Se o arquivo contiver um fluxo de vídeo, você poderá alternar o detector de mídia no modo "captura de bitmap" e recuperar os bitmaps da origem.</span><span class="sxs-lookup"><span data-stu-id="93250-118">If the file contains a video stream, you can switch the Media Detector into "bitmap grab" mode and retrieve bitmaps from the source.</span></span> <span data-ttu-id="93250-119">No entanto, depois de fazer isso, você não pode alternar o detector de mídia de volta para seu modo original; Ele é anexado permanentemente a esse fluxo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="93250-119">However, once you do so, you cannot switch the Media Detector back to its original mode; it is permanently attached to that video stream.</span></span> <span data-ttu-id="93250-120">Para trabalhar com outro fluxo ou outro arquivo, você deve criar uma nova instância do detector de mídia.</span><span class="sxs-lookup"><span data-stu-id="93250-120">To work with another stream or another file, you must create a new instance of the Media Detector.</span></span>

> [!Note]  
> <span data-ttu-id="93250-121">Os exemplos de código neste tutorial usam a classe **CComPtr** do ATL, que gerencia automaticamente as contagens de referência.</span><span class="sxs-lookup"><span data-stu-id="93250-121">The code examples in this tutorial use the ATL **CComPtr** class, which automatically manages reference counts.</span></span> <span data-ttu-id="93250-122">Se você preferir usar ponteiros de interface brutos, lembre-se de liberar todas as interfaces quando terminar.</span><span class="sxs-lookup"><span data-stu-id="93250-122">If you prefer to use raw interface pointers, remember to release every interface when you are done with it.</span></span> <span data-ttu-id="93250-123">Além disso, para resumir, os exemplos de código omitem grande parte da verificação de erros que um aplicativo deve executar.</span><span class="sxs-lookup"><span data-stu-id="93250-123">Also, for brevity the code examples omit much of the error checking that an application should perform.</span></span> <span data-ttu-id="93250-124">No código de trabalho, sempre verifique valores **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="93250-124">In working code, always check **HRESULT** values.</span></span>

 

<span data-ttu-id="93250-125">Este tutorial contém as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="93250-125">This tutorial contains the following steps:</span></span>

-   [<span data-ttu-id="93250-126">Etapa 1: criar o Windows Framework</span><span class="sxs-lookup"><span data-stu-id="93250-126">Step 1: Create the Windows Framework</span></span>](step-1--create-the-windows-framework.md)
-   [<span data-ttu-id="93250-127">Etapa 2: adicionar um comando de menu para pegar um quadro de cartaz</span><span class="sxs-lookup"><span data-stu-id="93250-127">Step 2: Add a Menu Command to Grab a Poster Frame</span></span>](step-2--add-a-menu-command-to-grab-a-poster-frame.md)
-   [<span data-ttu-id="93250-128">Etapa 3: implementar a função Frame-Grabbing</span><span class="sxs-lookup"><span data-stu-id="93250-128">Step 3: Implement the Frame-Grabbing Function</span></span>](step-3--implement-the-frame-grabbing-function.md)
-   [<span data-ttu-id="93250-129">Etapa 4: desenhar o bitmap na área do cliente</span><span class="sxs-lookup"><span data-stu-id="93250-129">Step 4: Draw the Bitmap on the Client Area</span></span>](step-4--draw-the-bitmap-on-the-client-area.md)

## <a name="related-topics"></a><span data-ttu-id="93250-130">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="93250-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="93250-131">Usando os serviços de edição do DirectShow</span><span class="sxs-lookup"><span data-stu-id="93250-131">Using DirectShow Editing Services</span></span>](using-directshow-editing-services.md)
</dt> </dl>

 

 



