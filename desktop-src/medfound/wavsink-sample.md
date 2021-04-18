---
description: Exemplo de WavSink
ms.assetid: 9e1af25f-d55c-45db-8c76-abf814e16700
title: Exemplo de WavSink
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e96ecca551b6ea3e6837f211f0afcb34818d635
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105781377"
---
# <a name="wavsink-sample"></a><span data-ttu-id="3b783-103">Exemplo de WavSink</span><span class="sxs-lookup"><span data-stu-id="3b783-103">WavSink Sample</span></span>

<span data-ttu-id="3b783-104">Mostra como implementar um coletor de mídia personalizado no Microsoft Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="3b783-104">Shows how to implement a custom media sink in Microsoft Media Foundation.</span></span> <span data-ttu-id="3b783-105">O exemplo implementa um coletor de arquivo que grava áudio PCM não compactado em um arquivo. wav.</span><span class="sxs-lookup"><span data-stu-id="3b783-105">The sample implements an archive sink that writes uncompressed PCM audio to a .wav file.</span></span>

## <a name="apis-demonstrated"></a><span data-ttu-id="3b783-106">APIs demonstradas</span><span class="sxs-lookup"><span data-stu-id="3b783-106">APIs Demonstrated</span></span>

<span data-ttu-id="3b783-107">Este exemplo demonstra as seguintes interfaces de Media Foundation:</span><span class="sxs-lookup"><span data-stu-id="3b783-107">This sample demonstrates the following Media Foundation interfaces:</span></span>

-   [<span data-ttu-id="3b783-108">**IMFClockStateSink**</span><span class="sxs-lookup"><span data-stu-id="3b783-108">**IMFClockStateSink**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink)
-   [<span data-ttu-id="3b783-109">**IMFFinalizableMediaSink**</span><span class="sxs-lookup"><span data-stu-id="3b783-109">**IMFFinalizableMediaSink**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imffinalizablemediasink)
-   [<span data-ttu-id="3b783-110">**IMFMediaSink**</span><span class="sxs-lookup"><span data-stu-id="3b783-110">**IMFMediaSink**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink)
-   [<span data-ttu-id="3b783-111">**IMFMediaTypeHandler**</span><span class="sxs-lookup"><span data-stu-id="3b783-111">**IMFMediaTypeHandler**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler)
-   [<span data-ttu-id="3b783-112">**IMFStreamSink**</span><span class="sxs-lookup"><span data-stu-id="3b783-112">**IMFStreamSink**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink)

## <a name="usage"></a><span data-ttu-id="3b783-113">Uso</span><span class="sxs-lookup"><span data-stu-id="3b783-113">Usage</span></span>

<span data-ttu-id="3b783-114">O exemplo de WavSink contém dois projetos do Visual Studio:</span><span class="sxs-lookup"><span data-stu-id="3b783-114">The WavSink sample contains two Visual Studio projects:</span></span>

-   <span data-ttu-id="3b783-115">WavSink. vcproj cria uma biblioteca estática que contém a implementação do coletor de mídia.</span><span class="sxs-lookup"><span data-stu-id="3b783-115">WavSink.vcproj builds a static library that contains the media sink implementation.</span></span>
-   <span data-ttu-id="3b783-116">WriteWavFile. vcproj cria um aplicativo de console que usa o coletor de mídia para produzir um arquivo. wav.</span><span class="sxs-lookup"><span data-stu-id="3b783-116">WriteWavFile.vcproj builds a console application that uses the media sink to produce a .wav file.</span></span> <span data-ttu-id="3b783-117">Este aplicativo é vinculado à biblioteca criada pelo projeto WavSink.</span><span class="sxs-lookup"><span data-stu-id="3b783-117">This application links to the library created by the WavSink project.</span></span>

## <a name="requirements"></a><span data-ttu-id="3b783-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3b783-118">Requirements</span></span>



| <span data-ttu-id="3b783-119">Produto</span><span class="sxs-lookup"><span data-stu-id="3b783-119">Product</span></span>                                                        | <span data-ttu-id="3b783-120">Versão</span><span class="sxs-lookup"><span data-stu-id="3b783-120">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="3b783-121">SDK do Windows</span><span class="sxs-lookup"><span data-stu-id="3b783-121">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="3b783-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="3b783-122">Windows 7</span></span> |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="3b783-123">Baixando o exemplo</span><span class="sxs-lookup"><span data-stu-id="3b783-123">Downloading the Sample</span></span>

<span data-ttu-id="3b783-124">Este exemplo está disponível no [repositório GitHub de exemplos clássicos do Windows](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/wavsink).</span><span class="sxs-lookup"><span data-stu-id="3b783-124">This sample is available in the [Windows classic samples github repository](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/wavsink).</span></span>

## <a name="related-topics"></a><span data-ttu-id="3b783-125">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3b783-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3b783-126">Exemplos de SDK do Media Foundation</span><span class="sxs-lookup"><span data-stu-id="3b783-126">Media Foundation SDK Samples</span></span>](media-foundation-sdk-samples.md)
</dt> <dt>

[<span data-ttu-id="3b783-127">Coletores de mídia</span><span class="sxs-lookup"><span data-stu-id="3b783-127">Media Sinks</span></span>](media-sinks.md)
</dt> </dl>

 

 



