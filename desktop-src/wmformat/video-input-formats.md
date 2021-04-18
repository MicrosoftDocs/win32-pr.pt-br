---
title: Formatos de entrada de vídeo
description: Formatos de entrada de vídeo
ms.assetid: 0f1ec15d-328e-4c07-bf58-fd4ecb483549
keywords:
- SDK do Windows Media Format, formatos de entrada de vídeo
- ASF (Advanced Systems Format), formatos de entrada de vídeo
- ASF (formato de sistemas avançados), formatos de entrada de vídeo
- formatos de entrada de vídeo
- SDK do Windows Media Format, formatos de vídeo
- ASF (Advanced Systems Format), formatos de vídeo
- ASF (formato de sistemas avançados), formatos de vídeo
- formatos de vídeo
- Codec do Windows Media Video 9, formatos de entrada de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c5113ee3cbd9c9235104f858968db20ebc29e3a
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/25/2020
ms.locfileid: "105781084"
---
# <a name="video-input-formats"></a>Formatos de entrada de vídeo

O gravador aceita os seguintes formatos de vídeo como entrada a ser compactada usando o codec do Windows Media Video 9:

-   WMMEDIASUBTYPE \_ IYUV
-   WMMEDIASUBTYPE \_ I420
-   WMMEDIASUBTYPE \_ YV12
-   WMMEDIASUBTYPE \_ YUY2
-   WMMEDIASUBTYPE \_ UYVY
-   WMMEDIASUBTYPE \_ YVYU
-   WMMEDIASUBTYPE \_ YVU9
-   WMMEDIASUBTYPE \_ RGB32
-   WMMEDIASUBTYPE \_ RGB24
-   WMMEDIASUBTYPE \_ RGB565
-   WMMEDIASUBTYPE \_ RGB555
-   WMMEDIASUBTYPE \_ RGB8

Você sempre deve usar [**IWMWriter:: GetInputFormatCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-getinputformatcount) e [**IWMWriter:: GetInputFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputformat) para enumerar os formatos de entrada disponíveis e obter o objeto de propriedades de mídia de entrada para o formato desejado. Os objetos de propriedades de mídia de entrada de vídeo devem ser alterados para refletir o tamanho do quadro e a taxa de quadros da mídia de entrada.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Identificadores de tipo de mídia**](media-type-identifiers.md)
</dt> <dt>

[**Tipos de mídia**](media-types.md)
</dt> </dl>

 

 




