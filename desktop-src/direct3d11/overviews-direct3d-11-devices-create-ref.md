---
title: Como criar um dispositivo de referência
description: Este tópico mostra como criar um dispositivo de referência que implementa uma implementação de software altamente precisa do tempo de execução.
ms.assetid: 00d3f5f2-02c6-4ff4-82a9-0726ad4a8cb3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dec5f3834bf1f10027da2a3f3a8e22acdee742b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364287"
---
# <a name="how-to-create-a-reference-device"></a>Como: criar um dispositivo de referência

Este tópico mostra como criar um dispositivo de referência que implementa uma implementação de software altamente precisa do tempo de execução. Para criar um dispositivo de referência, basta especificar que o dispositivo que você está criando usará um driver de referência. Este exemplo cria um dispositivo e uma cadeia de permuta ao mesmo tempo.

**Para criar um dispositivo de referência**

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

    

2.  Solicite um nível de recurso que implemente os recursos de que seu aplicativo precisará. Um dispositivo de referência pode ser criado com êxito para o tempo de execução do Direct3D 11.

    ```
        D3D_FEATURE_LEVEL FeatureLevels = D3D_FEATURE_LEVEL_11_0;
    ```

    

    Veja mais sobre os níveis de recurso na enumeração de [**\_ \_ nível de recurso do D3D**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) .

3.  Crie o dispositivo chamando [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain).


```
    HRESULT hr = S_OK;
    D3D_FEATURE_LEVEL FeatureLevel;

    if( FAILED (hr = D3D11CreateDeviceAndSwapChain( NULL, 
                    D3D_DRIVER_TYPE_REFERENCE,
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



Você precisará fornecer a chamada à API com o tipo de driver de referência da enumeração do [**\_ \_ tipo de driver do D3D**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_driver_type) . Depois que o método for bem sucedido, ele retornará uma interface de cadeia de permuta, uma interface de dispositivo, um ponteiro para o nível de recurso que foi concedido pelo driver e uma interface de contexto imediata.

Para obter informações sobre as limitações de criação de um dispositivo de referência em determinados níveis de recursos, consulte [limitações criando dispositivos de referência e detorção](overviews-direct3d-11-devices-limitations.md). [Como usar o Direct3D 11](how-to-use-direct3d-11.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Dispositivos](overviews-direct3d-11-devices.md)
</dt> <dt>

[Como usar o Direct3D 11](how-to-use-direct3d-11.md)
</dt> </dl>

 

 




