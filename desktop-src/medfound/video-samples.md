---
description: Exemplos de vídeo
ms.assetid: 1ee2ad6f-5e84-45ba-9849-cd3bd8e7eb29
title: Exemplos de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 239fecd0947271627abc7fc50ed16f6a7c682b84
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827792"
---
# <a name="video-samples"></a>Exemplos de vídeo

O objeto de exemplo de vídeo é uma implementação especializada da interface [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) para uso com o [processador de vídeo avançado](enhanced-video-renderer.md) (EVR). Para criar uma instância desse objeto, chame a função [**MFCreateVideoSampleFromSurface**](/windows/desktop/api/evr/nc-evr-mfcreatevideosamplefromsurface) . A função usa um ponteiro para uma superfície do Direct3D e retorna um ponteiro para a interface **IMFSample** . Os seguintes tipos de objetos devem alocar amostras usando essa função:

-   Apresentadores de EVR personalizados. Um apresentador aloca amostras de vídeo e as envia para o método [**IMFTransform::P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) do mixer. Para obter mais informações, consulte [como escrever um apresentador EVR](how-to-write-an-evr-presenter.md).

-   Decodificadores de vídeo que dão suporte à aceleração de vídeo. Para obter mais informações, consulte [dando suporte a DXVA 2,0 em Media Foundation](supporting-dxva-2-0-in-media-foundation.md).

O objeto de exemplo de vídeo implementa as seguintes interfaces:

-   [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

-   [**IMFDesiredSample**](/windows/desktop/api/evr/nn-evr-imfdesiredsample)

-   [**IMFTrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample)

Se o parâmetro *pUnkSurface* de [**MFCreateVideoSampleFromSurface**](/windows/desktop/api/evr/nc-evr-mfcreatevideosamplefromsurface) for não **nulo**, o exemplo de vídeo resultante conterá um único buffer de mídia que encapsula a superfície do Direct3D. Esse objeto de buffer tem funcionalidade limitada:

-   O método [**IMFMediaBuffer:: Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) do buffer retorna E \_ NOTIMPL.

-   O buffer não implementa a interface [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) .

A única maneira de acessar a superfície do buffer é chamar [**IMFGetService:: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice), usando o serviço de buffer do Service Identifier Mr \_ \_ .

Se o parâmetro *pUnkSurface* for **NULL**, o exemplo de vídeo será criado com zero buffers de mídia. Para adicionar um buffer ao exemplo, faça o seguinte:

1.  Crie uma superfície do Direct3D.

2.  Crie um buffer de superfície chamando [**MFCreateDXSurfaceBuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatedxsurfacebuffer). Para obter mais informações, consulte [buffer de superfície DirectX](directx-surface-buffer.md).

3.  Adicione o buffer ao exemplo chamando [**IMFSample:: addbuffer**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-addbuffer).

Use essa abordagem se você precisar que a memória da superfície seja acessível por meio da interface [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Buffers de mídia](media-buffers.md)
</dt> <dt>

[Amostras de mídia](media-samples.md)
</dt> </dl>

 

 
