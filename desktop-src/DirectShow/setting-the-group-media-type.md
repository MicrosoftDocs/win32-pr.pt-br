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
# <a name="setting-the-group-media-type"></a>Configurando o tipo de mídia do grupo

\[Essa API não tem suporte e pode ser alterada ou não estar disponível no futuro.\]

Todos os grupos devem definir um tipo de mídia descompactado, áudio ou vídeo. O tipo de mídia não compactada é o formato que os visualizadores veem ou ouvem durante a reprodução. Normalmente, a saída final estará em um formato compactado. Para obter mais informações, consulte [renderizando um projeto](rendering-a-project.md).

Para definir o formato descompactado, crie uma estrutura [**de \_ \_ tipo de mídia am**](/windows/win32/api/strmif/ns-strmif-am_media_type) e preencha-a com o tipo principal apropriado, subtipo e cabeçalho de formato. Para vídeo, aloque uma estrutura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) para o bloco de formato e defina a largura, a altura e a profundidade de bits. Para áudio, aloque uma estrutura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) para o bloco de formato e defina a taxa de amostragem, a profundidade de bits e o número de canais. Se você definir apenas o tipo principal, o DES fornecerá padrões razoáveis para os outros valores. Na prática, você deve definir os valores explicitamente para controlar a saída.

Depois de inicializar a estrutura do tipo de mídia, chame o método [**IAMTimelineGroup:: SetMediaType**](iamtimelinegroup-setmediatype.md) para definir o tipo de mídia para o grupo.

O exemplo a seguir especifica o vídeo RGB de 16 bits, 320 pixels de largura por 240 pixels de altura:


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



O próximo exemplo especifica um grupo de áudio, definindo o tipo de mídia do grupo como estéreo de 16 bits, 44100 amostras por segundo:


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



Você também pode usar a classe [**CMediaType**](cmediatype.md) nas [classes base do DirectShow](directshow-base-classes.md) para gerenciar tipos de mídia. Ele contém alguns métodos auxiliares úteis e libera automaticamente o bloco de formato.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre os tipos de mídia](about-media-types.md)
</dt> <dt>

[Construindo uma linha do tempo](constructing-a-timeline.md)
</dt> </dl>

 

 
