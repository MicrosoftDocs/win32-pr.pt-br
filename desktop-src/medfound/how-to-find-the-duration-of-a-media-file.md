---
description: Como localizar a duração de um arquivo de mídia.
ms.assetid: 88ecde0c-328f-4ca7-9d26-836e4df06563
title: Como localizar a duração de um arquivo de mídia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8915e52e97a4532b1d174166ec2863e26d18e34a
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104506344"
---
# <a name="how-to-find-the-duration-of-a-media-file"></a><span data-ttu-id="89781-103">Como localizar a duração de um arquivo de mídia</span><span class="sxs-lookup"><span data-stu-id="89781-103">How to Find the Duration of a Media File</span></span>

<span data-ttu-id="89781-104">Para localizar a duração de um arquivo de mídia, execute as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="89781-104">To find the duration of a media file, perform the following steps:</span></span>

1.  <span data-ttu-id="89781-105">Use o [resolvedor de origem](source-resolver.md) para criar uma fonte de mídia que possa analisar o arquivo de mídia.</span><span class="sxs-lookup"><span data-stu-id="89781-105">Use the [Source Resolver](source-resolver.md) to create a media source that can parse the media file.</span></span>
2.  <span data-ttu-id="89781-106">Chame [**IMFMediaSource:: CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) na origem da mídia.</span><span class="sxs-lookup"><span data-stu-id="89781-106">Call [**IMFMediaSource::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) on the media source.</span></span> <span data-ttu-id="89781-107">Esse método retorna o descritor de apresentação que descreve o conteúdo do arquivo de mídia.</span><span class="sxs-lookup"><span data-stu-id="89781-107">This method returns presentation descriptor that describes the contents of the media file.</span></span>
3.  <span data-ttu-id="89781-108">Consulte o descritor de apresentação do atributo de [ \_ \_ duração de PD MF](mf-pd-duration-attribute.md) chamando o método [**IMFAttributes:: getuint64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64) .</span><span class="sxs-lookup"><span data-stu-id="89781-108">Query the presentation descriptor for the [MF\_PD\_DURATION](mf-pd-duration-attribute.md) attribute by calling the [**IMFAttributes::GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64) method.</span></span> <span data-ttu-id="89781-109">O valor do atributo, se presente, é a duração do arquivo em unidades de 100 nanossegundos.</span><span class="sxs-lookup"><span data-stu-id="89781-109">The value of the attribute, if present, is the file duration in 100-nanosecond units.</span></span>


```C++
HRESULT GetSourceDuration(IMFMediaSource *pSource, MFTIME *pDuration)
{
    *pDuration = 0;

    IMFPresentationDescriptor *pPD = NULL;

    HRESULT hr = pSource->CreatePresentationDescriptor(&pPD);
    if (SUCCEEDED(hr))
    {
        hr = pPD->GetUINT64(MF_PD_DURATION, (UINT64*)pDuration);
        pPD->Release();
    }
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="89781-110">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="89781-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="89781-111">Reprodução de áudio/vídeo</span><span class="sxs-lookup"><span data-stu-id="89781-111">Audio/Video Playback</span></span>](audio-video-playback.md)
</dt> </dl>

 

 



