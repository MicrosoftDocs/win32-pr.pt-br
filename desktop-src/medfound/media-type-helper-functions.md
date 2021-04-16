---
description: As funções a seguir pertencem a objetos de tipo de mídia.
ms.assetid: 7d4f3581-8cb9-4d31-b2f7-c8fbde24cf2a
title: Funções auxiliares de tipo de mídia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7e5edb9748bad8ee16903eb9ff1ada50c1c043b
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104506353"
---
# <a name="media-type-helper-functions"></a>Funções auxiliares de tipo de mídia

As funções a seguir pertencem a objetos de tipo de mídia.



| Função                                                                     | Descrição                                                           |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [**MFAverageTimePerFrameToFrameRate**](/windows/desktop/api/mfapi/nf-mfapi-mfaveragetimeperframetoframerate) | Calcula a taxa de quadros a partir da duração média de um quadro de vídeo. |
| [**MFCalculateImageSize**](/windows/desktop/api/mfapi/nf-mfapi-mfcalculateimagesize)                         | Recupera o tamanho da imagem para um formato de vídeo descompactado.            |
| [**MFCompareFullToPartialMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfcomparefulltopartialmediatype)   | Compara um tipo de mídia completa com um tipo de mídia parcial.                   |
| [**MFCreateMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatemediatype)                               | Cria um tipo de mídia vazio.                                          |
| [**MFFrameRateToAverageTimePerFrame**](/windows/desktop/api/mfapi/nf-mfapi-mfframeratetoaveragetimeperframe) | Converte uma taxa de quadros de vídeo em uma duração de quadro.                    |
| [**MFGetStrideForBitmapInfoHeader**](/windows/desktop/api/mfapi/nf-mfapi-mfgetstrideforbitmapinfoheader)     | Recupera o stride de superfície mínimo para um formato de vídeo.              |
| [**MFIsFormatYUV**](/windows/desktop/api/mfapi/nf-mfapi-mfisformatyuv)                                       | Consulta se um código FOURCC ou um valor **D3DFORMAT** é um formato YUV. |
| [**MFValidateMediaTypeSize**](/windows/desktop/api/mfapi/nf-mfapi-mfvalidatemediatypesize)                   | Valida o tamanho de um buffer para um bloco de formato de vídeo.              |
| [**MFWrapMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfwrapmediatype)                                   | Cria um tipo de mídia que encapsula outro tipo de mídia.                   |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Conversões de tipo de mídia](media-type-conversions.md)
</dt> <dt>

[Tipos de mídia](media-types.md)
</dt> </dl>

 

 



