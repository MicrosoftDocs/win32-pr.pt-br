---
description: trabalhando com tipos de mídia DMO
ms.assetid: 1aaf7554-1a5f-439a-afb1-a031607e1a1e
title: trabalhando com tipos de mídia DMO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48a75d7eb65e92a89d5d413d8cc04a7dbb9f1891d6b23a9cc3c1242fbae46f1c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119100909"
---
# <a name="working-with-dmo-media-types"></a>trabalhando com tipos de mídia DMO

os tipos de mídia de entrada e saída usados pelo codec DMOs são definidos usando a estrutura [**de \_ \_ tipo de mídia DMO**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) . essa estrutura é idêntica ao [**tipo de \_ mídia \_ do WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type), que é definido no Windows media Format SDK e no [**\_ \_ tipo de mídia AM**](/windows/win32/api/strmif/ns-strmif-am_media_type), que é definido no Microsoft DirectShow®. Dependendo do seu aplicativo, você pode usar variáveis definidas como qualquer um desses três tipos. É seguro converter um ponteiro para uma das estruturas de tipo de mídia como outra. Por exemplo:


```
    DMO_MEDIA_TYPE MediaType;
    WM_MEDIA_TYPE* pMedia = NULL;
    pMedia = (WM_MEDIA_TYPE*)&MediaType;
```



Os tipos de formato usados pelos codecs geralmente são limitados aos descritos pelas estruturas **VIDEOINFOHEADER** e **WAVEFORMATEX** . Para sua conveniência, constantes para esses tipos de formato são incluídas no arquivo de cabeçalho wmcodecconst. h. Os nomes das constantes são WMCFORMAT \_ VIDEOINFO e WMCFORMAT \_ WaveFormatEx, respectivamente. Os codecs de áudio podem funcionar com a estrutura **WAVEFORMATEXTENSIBLE** em algumas circunstâncias e devem ser usados em outros. no entanto, **DMO \_ tipo de mídia \_ . formattype** é definido com o mesmo valor que é para **WAVEFORMATEX**. Para obter mais informações sobre como usar o **WAVEFORMATEXTENSIBLE**, consulte [usando High-Definition áudio](usinghighdefinitionaudio.md).

> [!Note]  
>    Você deve incluir a estrutura de tipo de formato usada como a saída do codificador em qualquer contêiner usado para armazenar os dados compactados. Os decodificadores exigem a estrutura de formato original para descompactar o conteúdo. além dos membros da estrutura, os tipos de vídeo e áudio de mídia compactados Windows exigem informações de formato adicionais, que são acrescentadas à estrutura. Para obter mais informações, consulte [trabalhando com áudio](workingwithaudio.md) e [trabalhando com vídeo](workingwithvideo.md).

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Trabalhando com codec DMOs](workingwithcodecdmos.md)
</dt> </dl>

 

 
