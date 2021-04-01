---
title: Fluxos de áudio e vídeo
description: Fluxos de áudio e vídeo
ms.assetid: 809e5bb6-2bc4-4022-9117-a2be5418d7d1
keywords:
- SDK do Windows Media Format, fluxos de áudio
- ASF (Advanced Systems Format), fluxos de áudio
- ASF (formato de sistemas avançados), fluxos de áudio
- SDK do Windows Media Format, fluxos de vídeo
- ASF (Advanced Systems Format), fluxos de vídeo
- ASF (formato de sistemas avançados), fluxos de vídeo
- SDK do Windows Media Format, fluxos
- ASF (Advanced Systems Format), fluxos
- ASF (formato de sistemas avançados), fluxos
- fluxos de áudio, sobre
- fluxos de vídeo, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d72eb46a6fb19129da2b9a841eab1710da47013
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005449"
---
# <a name="audio-and-video-streams"></a><span data-ttu-id="563aa-114">Fluxos de áudio e vídeo</span><span class="sxs-lookup"><span data-stu-id="563aa-114">Audio and Video Streams</span></span>

<span data-ttu-id="563aa-115">Os tipos mais comuns de fluxos usados em arquivos criados com o Windows Media Format SDK são fluxos de áudio e vídeo.</span><span class="sxs-lookup"><span data-stu-id="563aa-115">The most common types of streams used in files created by using the Windows Media Format SDK are audio and video streams.</span></span> <span data-ttu-id="563aa-116">Representações digitais de dados de áudio e vídeo são complexas e ocupam grandes quantidades de memória.</span><span class="sxs-lookup"><span data-stu-id="563aa-116">Digital representations of audio and video data are complex and take up large amounts of memory.</span></span> <span data-ttu-id="563aa-117">Na maioria das circunstâncias, áudio e vídeo são compactados antes de serem adicionados a um arquivo ASF.</span><span class="sxs-lookup"><span data-stu-id="563aa-117">Under most circumstances, both audio and video are compressed before being added to an ASF file.</span></span> <span data-ttu-id="563aa-118">A compactação é realizada usando um compactador/descompactador (codec).</span><span class="sxs-lookup"><span data-stu-id="563aa-118">Compression is accomplished using a compressor/decompressor (codec).</span></span>

<span data-ttu-id="563aa-119">Vários codecs de mídia do Windows estão incluídos neste SDK e fornecem uma compactação de qualidade excelente para mídia digital.</span><span class="sxs-lookup"><span data-stu-id="563aa-119">Several Windows Media codecs are included with this SDK, and they provide excellent quality compression for digital media.</span></span> <span data-ttu-id="563aa-120">Para obter mais informações sobre os codecs de mídia do Windows, consulte [recursos de codec](codec-features.md).</span><span class="sxs-lookup"><span data-stu-id="563aa-120">For more information about the Windows Media codecs, see [Codec Features](codec-features.md).</span></span> <span data-ttu-id="563aa-121">Muitos outros codecs estão disponíveis de várias fontes.</span><span class="sxs-lookup"><span data-stu-id="563aa-121">Many other codecs are available from various sources.</span></span> <span data-ttu-id="563aa-122">Você pode usar quaisquer codecs que desejar ao criar arquivos ASF, mas somente os codecs do Windows Media são diretamente suportados pelos objetos deste SDK.</span><span class="sxs-lookup"><span data-stu-id="563aa-122">You can use whatever codecs you like when creating ASF files, but only the Windows Media codecs are directly supported by the objects of this SDK.</span></span> <span data-ttu-id="563aa-123">Para usar outros codecs, você deve compactar amostras e passá-las para o objeto do gravador como dados arbitrários.</span><span class="sxs-lookup"><span data-stu-id="563aa-123">To use other codecs, you must compress samples and pass them to the writer object as arbitrary data.</span></span>

<span data-ttu-id="563aa-124">A distinção mais importante entre fluxos de áudio ou vídeo e fluxos arbitrários é que os fluxos que contêm dados de áudio ou vídeo do Windows Media são validados pelos objetos do SDK do Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="563aa-124">The most important distinction between audio or video streams and arbitrary streams is that streams containing Windows Media audio or video data are validated by the objects of the Windows Media Format SDK.</span></span> <span data-ttu-id="563aa-125">Os fluxos de dados arbitrários não são validados automaticamente e devem ser verificados quanto à integridade pelo seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="563aa-125">Arbitrary data streams are not validated automatically, and should be checked for integrity by your application.</span></span>

<span data-ttu-id="563aa-126">As propriedades de um fluxo de áudio ou vídeo são descritas no perfil usado para criar o arquivo.</span><span class="sxs-lookup"><span data-stu-id="563aa-126">The properties of an audio or video stream are described in the profile used to create the file.</span></span>

## <a name="related-topics"></a><span data-ttu-id="563aa-127">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="563aa-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="563aa-128">**Fluxos arbitrários**</span><span class="sxs-lookup"><span data-stu-id="563aa-128">**Arbitrary Streams**</span></span>](arbitrary-streams.md)
</dt> <dt>

[<span data-ttu-id="563aa-129">**Recursos de arquivo ASF**</span><span class="sxs-lookup"><span data-stu-id="563aa-129">**ASF File Features**</span></span>](asf-file-features.md)
</dt> <dt>

[<span data-ttu-id="563aa-130">**Trabalhando com perfis**</span><span class="sxs-lookup"><span data-stu-id="563aa-130">**Working with Profiles**</span></span>](working-with-profiles.md)
</dt> </dl>

 

 




