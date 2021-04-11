---
description: As exibições da taxa de atualização da variável exigem que a divisão seja habilitada, isso também é conhecido como &\# 0034; vsync-off&\# 0034; suporte.
ms.assetid: C5F140DD-5BAF-404A-9253-611831C4D424
title: Exibição da taxa de atualização da variável
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da6e658d84c51a6b51bc32855226194b9c22507e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104163755"
---
# <a name="variable-refresh-rate-displays"></a>Exibição da taxa de atualização da variável

As exibições da taxa de atualização da variável exigem que a *divisão* seja habilitada, isso também é conhecido como suporte "vsync-off".

-   [Exibição/vsync da taxa de atualização da variável](#variable-refresh-rate-displaysvsync-off)
-   [Tópicos relacionados](#related-topics)

## <a name="variable-refresh-rate-displaysvsync-off"></a>Exibição/vsync da taxa de atualização da variável

O suporte para exibições de taxa de atualização de variável é obtido definindo determinados sinalizadores ao criar e apresentar a cadeia de permuta.

Para usar esse recurso, os usuários do aplicativo precisam estar em sistemas Windows 10 com [KB3156421](https://support.microsoft.com/kb/3156421) ou a atualização de aniversário instalada. O recurso funciona em todas as versões do Direct3D 11 e 12 usando *o \_ \_ \_ \_ \* efeito de permuta * dxgi* entre os efeitos de permuta.

Para adicionar suporte de vsync para seus aplicativos, você pode consultar uma amostra de execução completa para o Direct3D 12, _ *D3D12Fullscreen** (consulte [exemplos de trabalho](../direct3d12/working-samples.md)). Também há alguns pontos que não são explicitamente chamados no código de exemplo, mas você precisa prestar atenção.

-   [**ResizeBuffers**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-resizebuffers) (ou [**ResizeBuffers1**](/windows/desktop/api/DXGI1_4/nf-dxgi1_4-idxgiswapchain3-resizebuffers1)) deve ter o mesmo sinalizador de criação da cadeia de permuta (o \_ sinalizador de cadeia de permuta dxgi \_ \_ \_ permite \_ a divisão) passado para ele como [**presente**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-present) (ou [**Present1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1)).
-   O DXGI \_ presente \_ permitir a \_ divisão só pode ser usado com o intervalo de sincronização 0. É recomendável sempre passar esse sinalizador de divisão ao usar o intervalo de sincronização 0 se [**CheckFeatureSupport**](/windows/desktop/api/DXGI1_5/nf-dxgi1_5-idxgifactory5-checkfeaturesupport) relatar que a divisão tem suporte *e* o aplicativo estiver em um modo de janela, incluindo o modo de tela inteira sem borda. Consulte as constantes do [**dxgi \_ presente**](dxgi-present.md) para obter mais detalhes.
-   Desabilitar o vsync não necessariamente uncap sua taxa de quadros: os desenvolvedores também precisam ter certeza de que as chamadas [**presentes**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-present) não são limitadas por outros eventos de tempo (como o `CompositionTarget::Rendering` evento em um aplicativo baseado em XAML).

O código abaixo recapitula algumas partes-chave que você precisa adicionar aos seus aplicativos.

``` syntax
//--------------------------------------------------------------------------------------------------------
// Check Tearing Support
//--------------------------------------------------------------------------------------------------------

// Determines whether tearing support is available for fullscreen borderless windows.

void DXSample::CheckTearingSupport()
{
// Rather than create the 1.5 factory interface directly, we create the 1.4
// interface and query for the 1.5 interface. This will enable the graphics
// debugging tools which might not support the 1.5 factory interface.

    ComPtr<IDXGIFactory4> factory4;
    HRESULT hr = CreateDXGIFactory1(IID_PPV_ARGS(&factory4));
    BOOL allowTearing = FALSE;
    if (SUCCEEDED(hr))
    { 
        ComPtr<IDXGIFactory5> factory5;
        hr = factory4.As(&factory5);
        if (SUCCEEDED(hr))
        {
            hr = factory5->CheckFeatureSupport(DXGI_FEATURE_PRESENT_ALLOW_TEARING, &allowTearing, sizeof(allowTearing));
        }
    }
    m_tearingSupport = SUCCEEDED(hr) && allowTearing;
}

//--------------------------------------------------------------------------------------------------------
// Set up swapchain properly
//--------------------------------------------------------------------------------------------------------

// It is recommended to always use the tearing flag when it is supported.
swapChainDesc.Flags = m_tearingSupport ? DXGI_SWAP_CHAIN_FLAG_ALLOW_TEARING : 0;

//--------------------------------------------------------------------------------------------------------
// Present
//--------------------------------------------------------------------------------------------------------

UINT presentFlags = (m_tearingSupport && m_windowedMode) ? DXGI_PRESENT_ALLOW_TEARING : 0;

// Present the frame.
ThrowIfFailed(m_swapChain->Present(0, presentFlags));
```

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Aprimoramentos de DXGI 1,5](dxgi-1-5-improvements.md)
</dt> <dt>

[Guia de programação para DXGI](dx-graphics-dxgi-overviews.md)
</dt> </dl>

 

 
