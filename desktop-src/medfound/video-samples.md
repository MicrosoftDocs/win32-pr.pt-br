---
description: Exemplos de vídeo
ms.assetid: 1ee2ad6f-5e84-45ba-9849-cd3bd8e7eb29
title: Exemplos de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3883b3a62cd907c89dd46d14681e28ad9a4d4d94653a9f04a9097707d22cff9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972595"
---
# <a name="video-samples"></a>Exemplos de vídeo

O objeto de exemplo de vídeo é uma implementação especializada da [](enhanced-video-renderer.md) interface [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) para uso com o EVR (Renderador de Vídeo Aprimorado). Para criar uma instância desse objeto, chame a [**função MFCreateVideoSampleFromSurface.**](/windows/desktop/api/evr/nc-evr-mfcreatevideosamplefromsurface) A função leva um ponteiro para uma superfície Direct3D e retorna um ponteiro para a interface **IMFSample.** Os seguintes tipos de objetos devem alocar amostras usando esta função:

-   Presentadores EVR personalizados. Um apresentador aloca exemplos de vídeo e os envia para o método [**IMFTransform::P rocessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) do mixer. Para obter mais informações, [consulte How to Write an EVR Presenter](how-to-write-an-evr-presenter.md).

-   Decodificadores de vídeo que suportam aceleração de vídeo. Para obter mais informações, consulte [Suporte ao DXVA 2.0 no Media Foundation](supporting-dxva-2-0-in-media-foundation.md).

O objeto de exemplo de vídeo implementa as seguintes interfaces:

-   [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

-   [**IMFDesiredSample**](/windows/desktop/api/evr/nn-evr-imfdesiredsample)

-   [**IMFTrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample)

Se o parâmetro *pUnkSurface* [**de MFCreateVideoSampleFromSurface**](/windows/desktop/api/evr/nc-evr-mfcreatevideosamplefromsurface) for não **NULL,** o exemplo de vídeo resultante conterá um único buffer de mídia que encapsula a superfície direct3D. Esse objeto de buffer tem funcionalidade limitada:

-   O método [**IMFMediaBuffer::Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) do buffer retorna E \_ NOTIMPL.

-   O buffer não implementa a interface [**IMF2DBuffer.**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer)

A única maneira de acessar a superfície do buffer é chamar [**IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice)usando o identificador de serviço MR \_ BUFFER \_ SERVICE.

Se o *parâmetro pUnkSurface* for **NULL,** o exemplo de vídeo será criado sem buffers de mídia. Para adicionar um buffer ao exemplo, faça o seguinte:

1.  Crie uma superfície direct3D.

2.  Crie um buffer de superfície chamando [**MFCreateDXSurfaceBuffer.**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatedxsurfacebuffer) Para obter mais informações, consulte [DirectX Surface Buffer](directx-surface-buffer.md).

3.  Adicione o buffer ao exemplo chamando [**IMFSample::AddBuffer**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-addbuffer).

Use essa abordagem se precisar que a memória da superfície seja acessível por meio da interface [**IMF2DBuffer.**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Buffers de mídia](media-buffers.md)
</dt> <dt>

[Exemplos de mídia](media-samples.md)
</dt> </dl>

 

 
