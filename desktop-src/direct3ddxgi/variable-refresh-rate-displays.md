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
# <a name="variable-refresh-rate-displays"></a><span data-ttu-id="32d5d-103">Exibição da taxa de atualização da variável</span><span class="sxs-lookup"><span data-stu-id="32d5d-103">Variable refresh rate displays</span></span>

<span data-ttu-id="32d5d-104">As exibições da taxa de atualização da variável exigem que a *divisão* seja habilitada, isso também é conhecido como suporte "vsync-off".</span><span class="sxs-lookup"><span data-stu-id="32d5d-104">Variable refresh rate displays require *tearing* to be enabled, this is also known as "vsync-off" support.</span></span>

-   [<span data-ttu-id="32d5d-105">Exibição/vsync da taxa de atualização da variável</span><span class="sxs-lookup"><span data-stu-id="32d5d-105">Variable refresh rate displays/Vsync off</span></span>](#variable-refresh-rate-displaysvsync-off)
-   [<span data-ttu-id="32d5d-106">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="32d5d-106">Related topics</span></span>](#related-topics)

## <a name="variable-refresh-rate-displaysvsync-off"></a><span data-ttu-id="32d5d-107">Exibição/vsync da taxa de atualização da variável</span><span class="sxs-lookup"><span data-stu-id="32d5d-107">Variable refresh rate displays/Vsync off</span></span>

<span data-ttu-id="32d5d-108">O suporte para exibições de taxa de atualização de variável é obtido definindo determinados sinalizadores ao criar e apresentar a cadeia de permuta.</span><span class="sxs-lookup"><span data-stu-id="32d5d-108">Support for variable refresh rate displays is achieved by setting certain flags when creating and presenting the swap chain.</span></span>

<span data-ttu-id="32d5d-109">Para usar esse recurso, os usuários do aplicativo precisam estar em sistemas Windows 10 com [KB3156421](https://support.microsoft.com/kb/3156421) ou a atualização de aniversário instalada.</span><span class="sxs-lookup"><span data-stu-id="32d5d-109">To use this feature, app users need to be on Windows 10 systems with either [KB3156421](https://support.microsoft.com/kb/3156421) or the Anniversary Update installed.</span></span> <span data-ttu-id="32d5d-110">O recurso funciona em todas as versões do Direct3D 11 e 12 usando *o \_ \_ \_ \_ \* efeito de permuta \* dxgi* entre os efeitos de permuta.</span><span class="sxs-lookup"><span data-stu-id="32d5d-110">The feature works on all versions of Direct3D 11 and 12 using \**DXGI\_SWAP\_EFFECT\_FLIP\_\** _ swap effects.</span></span>

<span data-ttu-id="32d5d-111">Para adicionar suporte de vsync para seus aplicativos, você pode consultar uma amostra de execução completa para o Direct3D 12, _ *D3D12Fullscreen*\* (consulte [exemplos de trabalho](../direct3d12/working-samples.md)).</span><span class="sxs-lookup"><span data-stu-id="32d5d-111">To add vsync-off support to your apps, you can refer to a complete running sample for Direct3D 12, _ *D3D12Fullscreen*\* (refer to [Working Samples](../direct3d12/working-samples.md)).</span></span> <span data-ttu-id="32d5d-112">Também há alguns pontos que não são explicitamente chamados no código de exemplo, mas você precisa prestar atenção.</span><span class="sxs-lookup"><span data-stu-id="32d5d-112">There are also a few points not explicitly called out in the sample code but you need to pay attention to.</span></span>

-   <span data-ttu-id="32d5d-113">[**ResizeBuffers**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-resizebuffers) (ou [**ResizeBuffers1**](/windows/desktop/api/DXGI1_4/nf-dxgi1_4-idxgiswapchain3-resizebuffers1)) deve ter o mesmo sinalizador de criação da cadeia de permuta (o \_ sinalizador de cadeia de permuta dxgi \_ \_ \_ permite \_ a divisão) passado para ele como [**presente**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-present) (ou [**Present1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1)).</span><span class="sxs-lookup"><span data-stu-id="32d5d-113">[**ResizeBuffers**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-resizebuffers) (or [**ResizeBuffers1**](/windows/desktop/api/DXGI1_4/nf-dxgi1_4-idxgiswapchain3-resizebuffers1)) must have the same swap chain creation flag (DXGI\_SWAP\_CHAIN\_FLAG\_ALLOW\_TEARING) passed to it as [**Present**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-present) (or [**Present1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1)).</span></span>
-   <span data-ttu-id="32d5d-114">O DXGI \_ presente \_ permitir a \_ divisão só pode ser usado com o intervalo de sincronização 0.</span><span class="sxs-lookup"><span data-stu-id="32d5d-114">DXGI\_PRESENT\_ALLOW\_TEARING can only be used with sync interval 0.</span></span> <span data-ttu-id="32d5d-115">É recomendável sempre passar esse sinalizador de divisão ao usar o intervalo de sincronização 0 se [**CheckFeatureSupport**](/windows/desktop/api/DXGI1_5/nf-dxgi1_5-idxgifactory5-checkfeaturesupport) relatar que a divisão tem suporte *e* o aplicativo estiver em um modo de janela, incluindo o modo de tela inteira sem borda.</span><span class="sxs-lookup"><span data-stu-id="32d5d-115">It is recommended to always pass this tearing flag when using sync interval 0 if [**CheckFeatureSupport**](/windows/desktop/api/DXGI1_5/nf-dxgi1_5-idxgifactory5-checkfeaturesupport) reports that tearing is supported *and* the app is in a windowed mode - including border-less fullscreen mode.</span></span> <span data-ttu-id="32d5d-116">Consulte as constantes do [**dxgi \_ presente**](dxgi-present.md) para obter mais detalhes.</span><span class="sxs-lookup"><span data-stu-id="32d5d-116">Refer to the [**DXGI\_PRESENT**](dxgi-present.md) constants for more details.</span></span>
-   <span data-ttu-id="32d5d-117">Desabilitar o vsync não necessariamente uncap sua taxa de quadros: os desenvolvedores também precisam ter certeza de que as chamadas [**presentes**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-present) não são limitadas por outros eventos de tempo (como o `CompositionTarget::Rendering` evento em um aplicativo baseado em XAML).</span><span class="sxs-lookup"><span data-stu-id="32d5d-117">Disabling vsync does not necessarily uncap your frame rate: developers also need to make sure [**Present**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-present) calls are not throttled by other timing events (such as the `CompositionTarget::Rendering` event in an XAML-based app).</span></span>

<span data-ttu-id="32d5d-118">O código abaixo recapitula algumas partes-chave que você precisa adicionar aos seus aplicativos.</span><span class="sxs-lookup"><span data-stu-id="32d5d-118">The code below recaps a few key pieces you need to add to your apps.</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="32d5d-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="32d5d-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="32d5d-120">Aprimoramentos de DXGI 1,5</span><span class="sxs-lookup"><span data-stu-id="32d5d-120">DXGI 1.5 Improvements</span></span>](dxgi-1-5-improvements.md)
</dt> <dt>

[<span data-ttu-id="32d5d-121">Guia de programação para DXGI</span><span class="sxs-lookup"><span data-stu-id="32d5d-121">Programming Guide for DXGI</span></span>](dx-graphics-dxgi-overviews.md)
</dt> </dl>

 

 
