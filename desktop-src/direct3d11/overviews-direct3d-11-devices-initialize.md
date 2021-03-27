---
title: Como criar um dispositivo e um contexto imediato
description: Este tópico mostra como inicializar um dispositivo.
ms.assetid: 02a20ada-b3aa-435e-8d66-117a19222f9f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 530f2b9cbc77f5404b4e9e8973d326a8708d6436
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007578"
---
# <a name="how-to-create-a-device-and-immediate-context"></a>Como: criar um dispositivo e um contexto imediato

Este tópico mostra como inicializar um [dispositivo](overviews-direct3d-11-devices-intro.md). Inicializar um [dispositivo](overviews-direct3d-11-devices-intro.md) é uma das primeiras tarefas que seu aplicativo deve concluir antes de você poder renderizar sua cena.

**Para criar um dispositivo e um contexto imediato**

Preencha a estrutura [**\_ desc da \_ cadeia \_ de permuta dxgi**](/windows/desktop/api/dxgi/ns-dxgi-dxgi_swap_chain_desc) com informações sobre formatos e dimensões de buffer. Para obter mais informações, consulte criando uma cadeia de permuta.

O exemplo de código a seguir demonstra como preencher a [**estrutura \_ \_ \_ desc da cadeia de permuta dxgi**](/windows/desktop/api/dxgi/ns-dxgi-dxgi_swap_chain_desc) .


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



Usando a [**estrutura \_ \_ \_ desc da cadeia de permuta dxgi**](/windows/desktop/api/dxgi/ns-dxgi-dxgi_swap_chain_desc) da etapa 1, chame [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain) para inicializar o dispositivo e a cadeia de troca ao mesmo tempo.


```
D3D_FEATURE_LEVEL  FeatureLevelsRequested = D3D_FEATURE_LEVEL_11_0;
UINT               numLevelsRequested = 1;
D3D_FEATURE_LEVEL  FeatureLevelsSupported;

if( FAILED (hr = D3D11CreateDeviceAndSwapChain( NULL, 
                D3D_DRIVER_TYPE_HARDWARE, 
                NULL, 
                0,
                &FeatureLevelsRequested, 
                numFeatureLevelsRequested, 
                D3D11_SDK_VERSION, 
                &sd, 
                &g_pSwapChain, 
                &g_pd3dDevice, 
                &FeatureLevelsSupported,
                &g_pImmediateContext )))
{
    return hr;
}
```



> [!Note]  
> Se você solicitar um dispositivo de [**nível de recurso do D3D de \_ \_ \_ 11 \_ 1**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) em um computador com apenas o tempo de execução do Direct3D 11,0, o [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain) será imediatamente fechado com **E \_ INVALIDARG**. Para solicitar com segurança todos os níveis de recursos possíveis em um computador com o tempo de execução do DirectX 11,0 ou DirectX 11,1, use este código:
>
> <span codelanguage=""></span>
>
> <table>
> <colgroup>
> <col style="width: 100%" />
> </colgroup>
> <tbody>
> <tr class="odd">
> <td><pre><code>const D3D_FEATURE_LEVEL lvl[] = { D3D_FEATURE_LEVEL_11_1, D3D_FEATURE_LEVEL_11_0,
> D3D_FEATURE_LEVEL_10_1, D3D_FEATURE_LEVEL_10_0,
> D3D_FEATURE_LEVEL_9_3, D3D_FEATURE_LEVEL_9_2, D3D_FEATURE_LEVEL_9_1 };
>
> UINT createDeviceFlags = 0;
> #ifdef _DEBUG
> createDeviceFlags |= D3D11_CREATE_DEVICE_DEBUG;
> #endif
>
> ID3D11Device* device = nullptr;
> HRESULT hr = D3D11CreateDeviceAndSwapChain( nullptr, D3D_DRIVER_TYPE_HARDWARE, nullptr, createDeviceFlags, lvl, _countof(lvl), D3D11_SDK_VERSION, &sd, &g_pSwapChain, &g_pd3ddevice, &FeatureLevelsSupported, &g_pImmediateContext );
> if ( hr == E_INVALIDARG )
> {
>     hr = D3D11CreateDeviceAndSwapChain( nullptr, D3D_DRIVER_TYPE_HARDWARE, nullptr, createDeviceFlags, &lvl[1], _countof(lvl) - 1, D3D11_SDK_VERSION, &sd, &g_pSwapChain, &g_pd3ddevice, &FeatureLevelsSupported, &g_pImmediateContext );
> }
>
> if (FAILED(hr))
>     return hr;</code></pre></td>
> </tr>
> </tbody>
> </table> 
>
>  
>
> Crie uma exibição de destino de renderização chamando [**ID3D11Device:: CreateRenderTargetView**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createrendertargetview) e associe o buffer de fundo como um destino de renderização chamando [**ID3D11DeviceContext:: OMSetRenderTargets**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetrendertargets).
>
> <span codelanguage=""></span>
>
> <table>
> <colgroup>
> <col style="width: 100%" />
> </colgroup>
> <tbody>
> <tr class="odd">
> <td><pre><code>ID3D11Texture2D* pBackBuffer;
>
> // Get a pointer to the back buffer
> hr = g_pSwapChain->GetBuffer( 0, __uuidof( ID3D11Texture2D ), 
>                              ( LPVOID* )&pBackBuffer );
>
> // Create a render-target view
> g_pd3dDevice->CreateRenderTargetView( pBackBuffer, NULL,
>                                       &g_pRenderTargetView );
>
> // Bind the view
> g_pImmediateContext->OMSetRenderTargets( 1, &g_pRenderTargetView, NULL );</code></pre></td>
> </tr>
> </tbody>
> </table> 
>
> Crie um visor para definir quais partes do destino de renderização ficarão visíveis. Defina o visor usando a estrutura do [**\_ visor D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_viewport) e defina o visor usando o método [**ID3D11DeviceContext:: RSSetViewports**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-rssetviewports) .
>
> <span codelanguage="ManagedCPlusPlus"></span>
>
> <table>
> <colgroup>
> <col style="width: 100%" />
> </colgroup>
> <thead>
> <tr class="header">
> <th>C++</th>
> </tr>
> </thead>
> <tbody>
> <tr class="odd">
> <td><pre><code>    // Setup the viewport
>     D3D11_VIEWPORT vp;
>     vp.Width = 640;
>     vp.Height = 480;
>     vp.MinDepth = 0.0f;
>     vp.MaxDepth = 1.0f;
>     vp.TopLeftX = 0;
>     vp.TopLeftY = 0;
>     g_pImmediateContext->RSSetViewports( 1, &vp );</code></pre></td>
> </tr>
> </tbody>
> </table> 
>
> ## <a name="related-topics"></a>Tópicos relacionados
>
> <dl> <dt>

[Dispositivos](overviews-direct3d-11-devices.md)
</dt> <dt>

[Como usar o Direct3D 11](how-to-use-direct3d-11.md)
</dt> </dl>
>
>  
>
>  
>