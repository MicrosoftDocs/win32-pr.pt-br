---
description: Buffer de superfície DirectX
ms.assetid: 2c82c023-4436-4f8a-b896-7f4765f989b3
title: Buffer de superfície DirectX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 746cff1489a644fd5c4144c8c0d923f11e5ca4555886e8defbce3b9b26a16a35
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119828266"
---
# <a name="directx-surface-buffer"></a>Buffer de superfície DirectX

O objeto de buffer da superfície DirectX é um buffer de mídia que gerencia uma superfície do Direct3D. Para criar uma instância desse objeto, chame [**MFCreateDXSurfaceBuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatedxsurfacebuffer) e passe um ponteiro para a superfície DirectX. O buffer de superfície do DirectX expõe as seguintes interfaces:

-   [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer)
-   [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer)
-   [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)

Há várias maneiras de acessar a memória da superfície do objeto de buffer:

-   Recomendado: chamar [**IMFGetService:: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) no buffer. Use o **\_ \_ serviço de buffer** do identificador de serviço Mr. O método retorna um ponteiro para a superfície do Direct3D subjacente.
-   Chame [**IMF2DBuffer:: Lock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-lock2d). Esse método chama **IDirect3DSurface9:: LockRect** diretamente na superfície. O método [**IMF2DBuffer:: Unlock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-unlock2d) chama **UnlockRect** na superfície.
-   Chame [**IMFMediaBuffer:: Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock). Em geral, isso não é recomendado, pois força o objeto a copiar a memória da superfície do Direct3D e, em seguida, voltar a usar. O método [**Lock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-lock2d) é mais eficiente.

[**Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) e [**Lock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-lock2d) podem falhar se a superfície subjacente não for bloqueáveis. O buffer de superfície do DirectX implementa esses dois métodos principalmente para componentes que não são projetados para funcionar com superfícies do Direct3D.

O processador de vídeo avançado (EVR) cria buffers de superfície do DirectX quando o decodificador não está configurado para a DXVA (aceleração de vídeo do DirectX). Para obter mais informações, consulte [**IMFVideoSampleAllocator**](/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocator).

### <a name="obtaining-the-direct3d-surface"></a>Obtendo a superfície do Direct3D

Para obter uma superfície do Direct3D de um exemplo de vídeo, faça o seguinte:

1.  Chame [**IMFSample:: GetBufferByIndex**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getbufferbyindex) com um valor de índice igual a zero.
2.  Chame [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) e especifique o identificador do serviço de **\_ \_ buffer do Mr** .

O código a seguir mostra essas etapas:


```C++
HRESULT GetD3DSurfaceFromSample(IMFSample *pSample, IDirect3DSurface9 **ppSurface)
{
    *ppSurface = NULL;

    IMFMediaBuffer *pBuffer = NULL;

    HRESULT hr = pSample->GetBufferByIndex(0, &pBuffer);
    if (SUCCEEDED(hr))
    {
        hr = MFGetService(pBuffer, MR_BUFFER_SERVICE, IID_PPV_ARGS(ppSurface));
        pBuffer->Release();
    }

    return hr;
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Buffers de mídia](media-buffers.md)
</dt> <dt>

[Exemplos de vídeo](video-samples.md)
</dt> </dl>

 

 



