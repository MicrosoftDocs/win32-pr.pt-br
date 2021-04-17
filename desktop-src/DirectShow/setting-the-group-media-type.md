---
description: Configurando o tipo de mídia do grupo
ms.assetid: 05f0fdcb-74a4-441e-ac3c-d3d2c1dfee80
title: Configurando o tipo de mídia do grupo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 365bd2171100a9d4bcfc48d70dbeb94d8a6639dd
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105782226"
---
# <a name="setting-the-group-media-type"></a><span data-ttu-id="c7aab-103">Configurando o tipo de mídia do grupo</span><span class="sxs-lookup"><span data-stu-id="c7aab-103">Setting the Group Media Type</span></span>

<span data-ttu-id="c7aab-104">\[Essa API não tem suporte e pode ser alterada ou não estar disponível no futuro.\]</span><span class="sxs-lookup"><span data-stu-id="c7aab-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="c7aab-105">Todos os grupos devem definir um tipo de mídia descompactado, áudio ou vídeo.</span><span class="sxs-lookup"><span data-stu-id="c7aab-105">All groups must define an uncompressed media type, either audio or video.</span></span> <span data-ttu-id="c7aab-106">O tipo de mídia não compactada é o formato que os visualizadores veem ou ouvem durante a reprodução.</span><span class="sxs-lookup"><span data-stu-id="c7aab-106">The uncompressed media type is the format that viewers see or hear during playback.</span></span> <span data-ttu-id="c7aab-107">Normalmente, a saída final estará em um formato compactado.</span><span class="sxs-lookup"><span data-stu-id="c7aab-107">Typically, the final output will be in a compressed format.</span></span> <span data-ttu-id="c7aab-108">Para obter mais informações, consulte [renderizando um projeto](rendering-a-project.md).</span><span class="sxs-lookup"><span data-stu-id="c7aab-108">For more information, see [Rendering a Project](rendering-a-project.md).</span></span>

<span data-ttu-id="c7aab-109">Para definir o formato descompactado, crie uma estrutura [**de \_ \_ tipo de mídia am**](/windows/win32/api/strmif/ns-strmif-am_media_type) e preencha-a com o tipo principal apropriado, subtipo e cabeçalho de formato.</span><span class="sxs-lookup"><span data-stu-id="c7aab-109">To set the uncompressed format, create an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure and fill it with the appropriate major type, subtype, and format header.</span></span> <span data-ttu-id="c7aab-110">Para vídeo, aloque uma estrutura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) para o bloco de formato e defina a largura, a altura e a profundidade de bits.</span><span class="sxs-lookup"><span data-stu-id="c7aab-110">For video, allocate a [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure for the format block, and set the width, height, and bit depth.</span></span> <span data-ttu-id="c7aab-111">Para áudio, aloque uma estrutura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) para o bloco de formato e defina a taxa de amostragem, a profundidade de bits e o número de canais.</span><span class="sxs-lookup"><span data-stu-id="c7aab-111">For audio, allocate a [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure for the format block, and set the sample rate, bit depth, and number of channels.</span></span> <span data-ttu-id="c7aab-112">Se você definir apenas o tipo principal, o DES fornecerá padrões razoáveis para os outros valores.</span><span class="sxs-lookup"><span data-stu-id="c7aab-112">If you set just the major type, DES provides reasonable defaults for the other values.</span></span> <span data-ttu-id="c7aab-113">Na prática, você deve definir os valores explicitamente para controlar a saída.</span><span class="sxs-lookup"><span data-stu-id="c7aab-113">In practice, you should set the values explicitly to control the output.</span></span>

<span data-ttu-id="c7aab-114">Depois de inicializar a estrutura do tipo de mídia, chame o método [**IAMTimelineGroup:: SetMediaType**](iamtimelinegroup-setmediatype.md) para definir o tipo de mídia para o grupo.</span><span class="sxs-lookup"><span data-stu-id="c7aab-114">After you initialize the media type structure, call the [**IAMTimelineGroup::SetMediaType**](iamtimelinegroup-setmediatype.md) method to set the media type for the group.</span></span>

<span data-ttu-id="c7aab-115">O exemplo a seguir especifica o vídeo RGB de 16 bits, 320 pixels de largura por 240 pixels de altura:</span><span class="sxs-lookup"><span data-stu-id="c7aab-115">The following example specifies 16-bit RGB video, 320 pixels wide by 240 pixels high:</span></span>


```C++
AM_MEDIA_TYPE mtGroup;  
mtGroup.majortype = MEDIATYPE_Video;
mtGroup.subtype = MEDIASUBTYPE_RGB555;

// Set format headers.
mtGroup.pbFormat = (BYTE*)CoTaskMemAlloc(sizeof(VIDEOINFOHEADER));
if (mtGroup.pbFormat == NULL)
{
    return E_OUTOFMEMORY;
}

VIDEOINFOHEADER *pVideoHeader = (VIDEOINFOHEADER*)mtGroup.pbFormat;
ZeroMemory(pVideoHeader, sizeof(VIDEOINFOHEADER));
pVideoHeader->bmiHeader.biBitCount = 16;
pVideoHeader->bmiHeader.biWidth = 320;
pVideoHeader->bmiHeader.biHeight = 240;
pVideoHeader->bmiHeader.biPlanes = 1;
pVideoHeader->bmiHeader.biSize = sizeof(BITMAPINFOHEADER);
pVideoHeader->bmiHeader.biSizeImage = DIBSIZE(pVideoHeader->bmiHeader);

// Set the format type and size.
mtGroup.formattype = FORMAT_VideoInfo;
mtGroup.cbFormat = sizeof(VIDEOINFOHEADER);

// Set the sample size.
mtGroup.bFixedSizeSamples = TRUE;
mtGroup.lSampleSize = DIBSIZE(pVideoHeader->bmiHeader);

// Now use this media type for the group.
pGroup->SetMediaType(&mtGroup);

// Clean up.
CoTaskMemFree(mtGroup.pbFormat);
```



<span data-ttu-id="c7aab-116">O próximo exemplo especifica um grupo de áudio, definindo o tipo de mídia do grupo como estéreo de 16 bits, 44100 amostras por segundo:</span><span class="sxs-lookup"><span data-stu-id="c7aab-116">The next example specifies an audio group, by setting the group media type to 16-bit stereo, 44100 samples per second:</span></span>


```C++
AM_MEDIA_TYPE mt;  
ZeroMemory(&mt, sizeof(AM_MEDIA_TYPE));

mt.majortype = MEDIATYPE_Audio;
mt.subtype = MEDIASUBTYPE_PCM;
mt.formattype = FORMAT_WaveFormatEx;

// Set format block.
mt.pbFormat = (BYTE*)CoTaskMemAlloc(sizeof(WAVEFORMATEX));
if (mt.pbFormat == NULL)
{
    return E_OUTOFMEMORY;
}
mt.cbFormat = sizeof(WAVEFORMATEX);

// Fill in the WAVEFORMATEX structure.
WAVEFORMATEX *wave = (WAVEFORMATEX*) mt.pbFormat;
wave->wFormatTag = WAVE_FORMAT_PCM;
wave->nChannels = 2;  // Stereo
wave->nSamplesPerSec = 44100;
wave->wBitsPerSample = 16;
wave->nBlockAlign = wave->nChannels * wave->wBitsPerSample/8;
wave->nAvgBytesPerSec = wave->nSamplesPerSec * wave->nBlockAlign; 
wave->cbSize = 0;

hr = pGroup->SetMediaType(&mt);
CoTaskMemFree(mt.pbFormat);
```



<span data-ttu-id="c7aab-117">Você também pode usar a classe [**CMediaType**](cmediatype.md) nas [classes base do DirectShow](directshow-base-classes.md) para gerenciar tipos de mídia.</span><span class="sxs-lookup"><span data-stu-id="c7aab-117">You can also use the [**CMediaType**](cmediatype.md) class in the [DirectShow Base Classes](directshow-base-classes.md) to manage media types.</span></span> <span data-ttu-id="c7aab-118">Ele contém alguns métodos auxiliares úteis e libera automaticamente o bloco de formato.</span><span class="sxs-lookup"><span data-stu-id="c7aab-118">It contains some useful helper methods, and automatically releases the format block.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c7aab-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c7aab-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c7aab-120">Sobre os tipos de mídia</span><span class="sxs-lookup"><span data-stu-id="c7aab-120">About Media Types</span></span>](about-media-types.md)
</dt> <dt>

[<span data-ttu-id="c7aab-121">Construindo uma linha do tempo</span><span class="sxs-lookup"><span data-stu-id="c7aab-121">Constructing a Timeline</span></span>](constructing-a-timeline.md)
</dt> </dl>

 

 
