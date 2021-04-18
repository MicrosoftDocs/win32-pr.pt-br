---
title: Para buscar marcadores
description: Para buscar marcadores
ms.assetid: 2d5efebf-dcbd-4fb8-933e-cc6d3a99adf8
keywords:
- ASF (Advanced Systems Format), buscando marcadores
- ASF (formato de sistemas avançados), buscando marcadores
- ASF (Advanced Systems Format), leitores assíncronos
- ASF (formato de sistemas avançados), leitores assíncronos
- ASF (Advanced Systems Format), marcadores
- ASF (formato de sistemas avançados), marcadores
- leitores assíncronos, buscando marcadores
- leitores assíncronos, marcadores
- marcadores, buscando
- marcadores, leitores assíncronos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a16cb4fef99a5c735a12f03f8d2e962d6caf9c2a
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/25/2020
ms.locfileid: "105807882"
---
# <a name="to-seek-to-markers"></a><span data-ttu-id="ff03a-113">Para buscar marcadores</span><span class="sxs-lookup"><span data-stu-id="ff03a-113">To Seek to Markers</span></span>

<span data-ttu-id="ff03a-114">Um marcador é um local nomeado em um arquivo ASF.</span><span class="sxs-lookup"><span data-stu-id="ff03a-114">A marker is a named location in an ASF file.</span></span> <span data-ttu-id="ff03a-115">Você só pode iniciar a reprodução do local de um marcador usando o leitor assíncrono.</span><span class="sxs-lookup"><span data-stu-id="ff03a-115">You can only start playback from the location of a marker by using the asynchronous reader.</span></span> <span data-ttu-id="ff03a-116">Você pode começar a reprodução em um marcador seguindo estas etapas.</span><span class="sxs-lookup"><span data-stu-id="ff03a-116">You can begin playback at a marker by following these steps.</span></span>

1.  <span data-ttu-id="ff03a-117">Chame **IWMReader:: QueryInterface** para obter um ponteiro para a interface [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) .</span><span class="sxs-lookup"><span data-stu-id="ff03a-117">Call **IWMReader::QueryInterface** to obtain a pointer to the [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) interface.</span></span>
2.  <span data-ttu-id="ff03a-118">Recupere o número total de marcadores no arquivo chamando [**IWMHeaderInfo:: GetMarkerCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getmarkercount).</span><span class="sxs-lookup"><span data-stu-id="ff03a-118">Retrieve the total number of markers in the file by calling [**IWMHeaderInfo::GetMarkerCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getmarkercount).</span></span>
3.  <span data-ttu-id="ff03a-119">Faça um loop pelos marcadores, usando a contagem de marcadores recuperada na etapa 2.</span><span class="sxs-lookup"><span data-stu-id="ff03a-119">Loop through the markers, using the marker count retrieved in step 2.</span></span> <span data-ttu-id="ff03a-120">Recupere o nome e a hora de cada marcador chamando [**IWMHeaderInfo:: Getmarkr**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getmarker) para cada.</span><span class="sxs-lookup"><span data-stu-id="ff03a-120">Retrieve the name and time of each marker by calling [**IWMHeaderInfo::GetMarker**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getmarker) for each.</span></span> <span data-ttu-id="ff03a-121">Salve o índice do marcador desejado.</span><span class="sxs-lookup"><span data-stu-id="ff03a-121">Save the index of the desired marker.</span></span>
4.  <span data-ttu-id="ff03a-122">Chame **IWMReader:: QueryInterface** para obter um ponteiro para a interface [**IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2) .</span><span class="sxs-lookup"><span data-stu-id="ff03a-122">Call **IWMReader::QueryInterface** to obtain a pointer to the [**IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2) interface.</span></span>
5.  <span data-ttu-id="ff03a-123">Especifique o marcador no qual iniciar a reprodução chamando [**IWMReaderAdvanced2:: StartAtMarker**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-startatmarker).</span><span class="sxs-lookup"><span data-stu-id="ff03a-123">Specify the marker at which to start playback by calling [**IWMReaderAdvanced2::StartAtMarker**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-startatmarker).</span></span> <span data-ttu-id="ff03a-124">Você deve passar o índice do marcador desejado, que você salvou na etapa 3.</span><span class="sxs-lookup"><span data-stu-id="ff03a-124">You must pass the index of the desired marker, which you saved in step 3.</span></span>
6.  <span data-ttu-id="ff03a-125">Manipule os exemplos como faria normalmente em sua implementação do método [**IWMReaderCallback:: onsample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample) .</span><span class="sxs-lookup"><span data-stu-id="ff03a-125">Handle the samples as you normally would in your implementation of the [**IWMReaderCallback::OnSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample) method.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ff03a-126">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ff03a-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ff03a-127">**Marcadores**</span><span class="sxs-lookup"><span data-stu-id="ff03a-127">**Markers**</span></span>](markers.md)
</dt> <dt>

[<span data-ttu-id="ff03a-128">**Lendo arquivos com o leitor assíncrono**</span><span class="sxs-lookup"><span data-stu-id="ff03a-128">**Reading Files with the Asynchronous Reader**</span></span>](reading-files-with-the-asynchronous-reader.md)
</dt> <dt>

[<span data-ttu-id="ff03a-129">**Trabalhando com índices**</span><span class="sxs-lookup"><span data-stu-id="ff03a-129">**Working with Indexes**</span></span>](working-with-indexes.md)
</dt> </dl>

 

 




