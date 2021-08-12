---
description: As exibições de taxa de atualização variável exigem a habilitação da operação, isso também é conhecido como &\# 0034;vsync-off&\# 0034; suporte.
ms.assetid: C5F140DD-5BAF-404A-9253-611831C4D424
title: A taxa de atualização variável é exibida
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 349592ce49d1008f6337b53c7f524ac7303907f75cd99205fe79bf55988b934b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118288919"
---
# <a name="variable-refresh-rate-displays"></a>A taxa de atualização variável é exibida

As exibições de  taxa de atualização de variável exigem a habilitação da operação. Isso também é conhecido como suporte a "vsync-off".

-   [A taxa de atualização variável é exibida/Vsync desligada](#variable-refresh-rate-displaysvsync-off)
-   [Tópicos relacionados](#related-topics)

## <a name="variable-refresh-rate-displaysvsync-off"></a>A taxa de atualização variável é exibida/Vsync desligada

O suporte para exibições de taxa de atualização variável é obtido definindo determinados sinalizadores ao criar e apresentar a cadeia de permuta.

Para usar esse recurso, os usuários do aplicativo precisam estar em sistemas Windows 10 com [o KB3156421](https://support.microsoft.com/kb/3156421) ou a Atualização de Aniversário instalada. O recurso funciona em todas as versões do Direct3D 11 e 12 usando efeitos de permuta DE FLIP **DXGI \_ SWAP \_ \_ \_ \* EFFECT.**

Para adicionar suporte vsync-off aos seus [aplicativos,](../direct3d12/working-samples.md)você pode consultar um exemplo de execução completo para Direct3D 12, **D3D12Fullscreen** (consulte Amostras de trabalho). Também há alguns pontos não explicitamente chamados no código de exemplo, mas você precisa prestar atenção.

-   [**ResizeBuffers**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-resizebuffers) (ou [**ResizeBuffers1**](/windows/desktop/api/DXGI1_4/nf-dxgi1_4-idxgiswapchain3-resizebuffers1)) deve ter o mesmo sinalizador de criação de cadeia de permuta (SINALIZADOR DE CADEIA DE PERMUTA DXGI ALLOW TEARING) passado para ele como \_ \_ \_ \_ \_ [**Present**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-present) (ou [**Present1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1)).
-   DXGI \_ PRESENT \_ ALLOW \_ TEARING só pode ser usado com o intervalo de sincronização 0. É recomendável sempre passar esse sinalizador de descompasso ao usar o intervalo  de sincronização 0 se [**CheckFeatureSupport**](/windows/desktop/api/DXGI1_5/nf-dxgi1_5-idxgifactory5-checkfeaturesupport) relata que há suporte para a replicação e o aplicativo está em um modo de janela , incluindo o modo de tela inteira sem borda. Consulte as constantes [**DXGI \_ PRESENT**](dxgi-present.md) para obter mais detalhes.
-   Desabilitar o vsync não necessariamente desacapta sua [](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-present) taxa de quadros: os desenvolvedores também precisam garantir que as chamadas presentes não sejam controladas por outros eventos de tempo (como o evento em um aplicativo baseado em `CompositionTarget::Rendering` XAML).

O código a seguir recapitula algumas partes principais que você precisa adicionar aos seus aplicativos.

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

[Melhorias do DXGI 1.5](dxgi-1-5-improvements.md)
</dt> <dt>

[Guia de programação para DXGI](dx-graphics-dxgi-overviews.md)
</dt> </dl>

 

 
