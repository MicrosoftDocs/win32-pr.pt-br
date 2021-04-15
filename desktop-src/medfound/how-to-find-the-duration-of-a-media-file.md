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
# <a name="how-to-find-the-duration-of-a-media-file"></a>Como localizar a duração de um arquivo de mídia

Para localizar a duração de um arquivo de mídia, execute as seguintes etapas:

1.  Use o [resolvedor de origem](source-resolver.md) para criar uma fonte de mídia que possa analisar o arquivo de mídia.
2.  Chame [**IMFMediaSource:: CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) na origem da mídia. Esse método retorna o descritor de apresentação que descreve o conteúdo do arquivo de mídia.
3.  Consulte o descritor de apresentação do atributo de [ \_ \_ duração de PD MF](mf-pd-duration-attribute.md) chamando o método [**IMFAttributes:: getuint64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64) . O valor do atributo, se presente, é a duração do arquivo em unidades de 100 nanossegundos.


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



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Reprodução de áudio/vídeo](audio-video-playback.md)
</dt> </dl>

 

 



