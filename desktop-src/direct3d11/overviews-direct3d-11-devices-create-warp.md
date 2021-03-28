---
title: Como criar um dispositivo de detorção
description: Este tópico mostra como criar um dispositivo de detorção que implementa um rasterizador de software de alta velocidade.
ms.assetid: 6daf661e-bc24-4b90-83a7-031acb57cf87
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: deda409971d22f46132a1cb9b008d3dd1eb7c407
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104988684"
---
# <a name="how-to-create-a-warp-device"></a>Como: criar um dispositivo de detorção

Este tópico mostra como criar um dispositivo de detorção que implementa um rasterizador de software de alta velocidade. Para criar um dispositivo WARP, basta especificar que o dispositivo que você está criando usará um driver WARP. Este exemplo cria um dispositivo e uma cadeia de permuta ao mesmo tempo.

**Para criar um dispositivo de detorção**

1.  Defina os parâmetros iniciais para uma cadeia de permuta.
    ```
        DXGI_SWAP_CHAIN_DESC sd;
        ZeroMemory( &sd, sizeof( sd ) );
        sd.BufferCount = 1;
        sd.BufferDesc.Width = 640;
        sd.BufferDesc.Height = 480;
        sd.BufferDesc.Format = DXGI_FORMAT_R8G8B8A8_UNORM;
        sd.BufferDesc.RefreshRate.Numerator = 60;
        sd.BufferDesc.RefreshRate.Denominator = 1;
        sd.BufferUsage = DXGI_USAGE_RENDER_TARGET_OUTPUT;
        sd.OutputWindow = g_hWnd;
        sd.SampleDesc.Count = 1;
        sd.SampleDesc.Quality = 0;
        sd.Windowed = TRUE;
    ```

    

2.  Solicite um nível de recurso que implemente os recursos de que seu aplicativo precisará. Um dispositivo WARP pode ser criado com êxito para os níveis de recursos do **\_ nível de recurso D3D \_ \_ 9 \_ 1** até o **nível de recurso do D3D \_ \_ \_ 10 \_ 1** e a partir do Windows 8 para todos os níveis de recurso.

    ```
        D3D_FEATURE_LEVEL FeatureLevels = D3D_FEATURE_LEVEL_10_1;
    ```

    

    Veja mais sobre os níveis de recurso na enumeração de [**\_ \_ nível de recurso do D3D**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) .

3.  Crie o dispositivo chamando [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain).


```
    HRESULT hr = S_OK;
    if( FAILED (hr = D3D11CreateDeviceAndSwapChain( NULL, 
                    D3D_DRIVER_TYPE_WARP,
                    NULL, 
                    0,
                    &FeatureLevels, 
                    1, 
                    D3D11_SDK_VERSION, 
                    &sd, 
                    &g_pSwapChain, 
                    &g_pd3dDevice, 
                    &FeatureLevel,
                    &g_pImmediateContext )))
    {
        return hr;
    }
```



Você precisará fornecer a chamada à API com o tipo de driver WARP da enumeração do [**\_ \_ tipo de driver do D3D**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_driver_type) . Depois que o método for bem sucedido, ele retornará uma interface de cadeia de permuta, uma interface de dispositivo, um ponteiro para o nível de recurso que foi concedido pelo driver e uma interface de contexto imediata.

Para obter informações sobre as limitações de criação de um dispositivo de detorção em determinados níveis de recursos, consulte [limitações criando dispositivos de referência e detorção](overviews-direct3d-11-devices-limitations.md).

## <a name="new-for-windows-8"></a>Novo para o Windows 8

Quando o adaptador de vídeo primário de um computador é o "adaptador de vídeo básico da Microsoft" (adaptador de detorção), esse computador também tem um segundo adaptador. Esse segundo adaptador é o dispositivo somente de renderização que não tem saídas de exibição. Para obter mais informações sobre o dispositivo somente de renderização, consulte [novas informações no Windows 8 sobre como enumerar adaptadores](/windows/desktop/direct3ddxgi/d3d10-graphics-programming-guide-dxgi).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Dispositivos](overviews-direct3d-11-devices.md)
</dt> <dt>

[Como usar o Direct3D 11](how-to-use-direct3d-11.md)
</dt> </dl>

 

 