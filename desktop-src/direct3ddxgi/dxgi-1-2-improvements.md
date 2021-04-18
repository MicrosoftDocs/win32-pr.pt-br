---
description: A funcionalidade a seguir foi adicionada no Microsoft DirectX Graphics Infrastructure (DXGI) 1,2.
ms.assetid: E2D8DA99-4EA2-4847-B699-80A6994C66C0
title: Aprimoramentos de DXGI 1.2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bd274918d179bc7adeb8dd132fe604cf56d80f2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105787649"
---
# <a name="dxgi-12-improvements"></a>Aprimoramentos de DXGI 1.2

A funcionalidade a seguir foi adicionada no Microsoft DirectX Graphics Infrastructure (DXGI) 1,2.

## <a name="presentation-enhancements-and-optimizations"></a>Aprimoramentos de apresentação e otimizações

DXGI 1,2 aprimora a apresentação com uma nova cadeia de permuta de flip-Model, proteção de conteúdo, apresentação sem janela e apresentação otimizada onde você especifica retângulos sujos e áreas roladas. A apresentação também é aprimorada com o comportamento de exibição 3D estereoscópico.

Você pode usar a seguinte API DXGI 1,2 para apresentação avançada.

-   [**IDXGIDisplayControl::IsStereoEnabled**](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgidisplaycontrol-isstereoenabled)
-   [**IDXGIDisplayControl::SetStereoEnabled**](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgidisplaycontrol-setstereoenabled)
-   [**IDXGIFactory2::CreateSwapChainForHwnd**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-createswapchainforhwnd)
-   [**IDXGIFactory2::CreateSwapChainForCoreWindow**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcorewindow)
-   [**IDXGIFactory2::CreateSwapChainForComposition**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcomposition)
-   [**IDXGIFactory2::IsWindowedStereoEnabled**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-iswindowedstereoenabled)
-   [**IDXGIFactory2::RegisterStereoStatusWindow**](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-registerstereostatuswindow)
-   [**IDXGIFactory2::RegisterStereoStatusEvent**](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-registerstereostatusevent)
-   [**IDXGIFactory2::UnregisterStereoStatus**](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-unregisterstereostatus)
-   [**IDXGIFactory2::RegisterOcclusionStatusWindow**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-registerocclusionstatuswindow)
-   [**IDXGIFactory2::RegisterOcclusionStatusEvent**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-registerocclusionstatusevent)
-   [**IDXGIFactory2::UnregisterOcclusionStatus**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-unregisterocclusionstatus)
-   [**IDXGIOutput1::GetDisplayModeList1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutput1-getdisplaymodelist1)
-   [**IDXGIOutput1::GetDisplaySurfaceData1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutput1-getdisplaysurfacedata1)
-   [**IDXGIOutput1::FindClosestMatchingMode1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutput1-findclosestmatchingmode1)
-   [**IDXGIResource1::CreateSubresourceSurface**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiresource1-createsubresourcesurface)
-   [**IDXGISurface2:: getResource**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgisurface2-getresource)
-   [**IDXGISwapChain1::GetDesc1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-getdesc1)
-   [**IDXGISwapChain1::GetFullscreenDesc**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-getfullscreendesc)
-   [**IDXGISwapChain1:: GetHwnd**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-gethwnd)
-   [**IDXGISwapChain1::GetCoreWindow**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-getcorewindow)
-   [**IDXGISwapChain1::Present1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1)
-   [**IDXGISwapChain1::IsTemporaryMonoSupported**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-istemporarymonosupported)
-   [**IDXGISwapChain1::GetRestrictToOutput**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-getrestricttooutput)
-   [**IDXGISwapChain1:: setBackgroundColor**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-setbackgroundcolor)
-   [**IDXGISwapChain1:: getBackgroundColor**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-getbackgroundcolor)
-   [**IDXGISwapChain1:: SetRotation**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-setrotation)
-   [**IDXGISwapChain1:: getrotation**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-getrotation)

Para obter mais informações sobre como usar a API DXGI 1,2 para apresentação avançada, consulte [aprimorando a apresentação com o modelo de flip, retângulos sujos e áreas roladas](dxgi-1-2-presentation-improvements.md).

Para obter informações sobre como determinar se você pode renderizar em estéreo, consulte [renderização no estéreo e notificação sobre o status do estéreo](stereo-rendering-stereo-status-notifying.md).

Para obter informações sobre como determinar alterações no status do oclusão do seu aplicativo, consulte [aguardando um evento quando a renderização é desnecessária](waiting-when-occluded.md).

Para obter informações sobre como os valores de dados são alterados quando você apresenta o conteúdo na tela, consulte [convertendo dados para o espaço de cores](converting-data-color-space.md).

## <a name="desktop-duplication"></a>Duplicação de área de trabalho

O Windows 8 desabilita drivers de espelho padrão do Windows 2000 Display Driver Model (XDDM). DXGI 1,2 fornece a API de duplicação de área de trabalho como uma alternativa. A API de duplicação de desktop fornece acesso remoto à imagem da área de trabalho para cenários de colaboração.

A API de duplicação de desktops consiste nos seguintes métodos.

-   [**IDXGIOutput1::D uplicateOutput**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutput1-duplicateoutput)
-   [**IDXGIOutputDuplication:: GetDesc**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-getdesc)
-   [**IDXGIOutputDuplication::AcquireNextFrame**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-acquirenextframe)
-   [**IDXGIOutputDuplication::GetFrameDirtyRects**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-getframedirtyrects)
-   [**IDXGIOutputDuplication::GetFrameMoveRects**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-getframemoverects)
-   [**IDXGIOutputDuplication::GetFramePointerShape**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-getframepointershape)
-   [**IDXGIOutputDuplication::MapDesktopSurface**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-mapdesktopsurface)
-   [**IDXGIOutputDuplication::UnMapDesktopSurface**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-unmapdesktopsurface)
-   [**IDXGIOutputDuplication::ReleaseFrame**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-releaseframe)

Para obter mais informações sobre como usar a API de duplicação de área de trabalho, consulte [API de duplicação de área de trabalho](desktop-dup-api.md).

## <a name="improved-usage-of-shared-resources-and-synchronized-events"></a>Uso aprimorado de recursos compartilhados e eventos sincronizados

Nas versões anteriores do Windows, os aplicativos usam sondagem contínua para determinar se a GPU (unidade de processamento gráfico) terminou de processar comandos arbitrários. DXGI 1,2 permite que um aplicativo enfileirar um evento para um dispositivo DXGI. Em seguida, o aplicativo pode aguardar o dispositivo DXGI sinalizar o evento para determinar que a GPU concluiu a execução de todos os comandos de renderização. DXGI 1,2 permite que vários dispositivos compartilhem um recurso por meio de um identificador NT.

Você pode usar a seguinte API de DXGI 1,2 e a API Direct3D 11,1 para compartilhar recursos e sincronizar eventos.

-   [**IDXGIDevice2:: EnqueueSetEvent**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgidevice2-enqueuesetevent)
-   [**IDXGIResource1::CreateSharedHandle**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiresource1-createsharedhandle)
-   [**IDXGIFactory2::GetSharedResourceAdapterLuid**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-getsharedresourceadapterluid)
-   [**ID3D11Device1::OpenSharedResource1**](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11device1-opensharedresource1)
-   [**ID3D11Device1::OpenSharedResourceByName**](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11device1-opensharedresourcebyname)
-   [**D3D11 \_ \_ \_ dishared \_ NTHANDLE de recursos**](/windows/win32/api/d3d11/ne-d3d11-d3d11_resource_misc_flag)

## <a name="offer-the-video-memory-of-resources"></a>Oferecer a memória de vídeo dos recursos

DXGI 1,2 permite que um aplicativo ofereça a memória de vídeo de seus recursos com baixa sobrecarga. Ao oferecer a memória de vídeo, o sistema operacional pode liberar a memória de vídeo.

Esse recurso DXGI 1,2 consiste nos seguintes métodos.

-   [**IDXGIDevice2:: OfferResources**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgidevice2-offerresources)
-   [**IDXGIDevice2:: ReclaimResources**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgidevice2-reclaimresources)

Você pode usar o método [**ID3D11Debug:: SetFeatureMask**](/windows/win32/api/d3d11sdklayers/nf-d3d11sdklayers-id3d11debug-setfeaturemask) para definir sinalizadores de máscara de recurso que depurem o comportamento dos métodos [**IDXGIDevice2:: OfferResources**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgidevice2-offerresources) e [**IDXGIDevice2:: ReclaimResources**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgidevice2-reclaimresources) em seu aplicativo.

## <a name="gpu-preemption-at-finer-granularity-levels-for-wddm-12-driver-model"></a>Preempção de GPU em níveis de granularidade mais definados para o modelo de driver do WDDM 1,2

Começando com o modelo de driver do Windows Display Driver Model (WDDM) 1,2, o Agendador do WDDM pode apropriar a execução de tarefas de aplicativos da GPU em níveis de granularidade mais definados. DXGI 1,2 permite que você determine os níveis de granularidade de preempção da GPU.

Esse recurso DXGI 1,2 consiste no método a seguir.

-   [**IDXGIAdapter2::GetDesc2**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiadapter2-getdesc2)

## <a name="debugging-apis"></a>APIs de depuração

O SDK do Windows 8 fornece recursos adicionais de depuração. Você pode usar as seguintes APIs DXGI de Dxgidebug.dll para depurar seu aplicativo:

-   [**DXGIGetDebugInterface**](/windows/desktop/api/DXGIDebug/nf-dxgidebug-dxgigetdebuginterface)
-   [**IDXGIDebug**](/windows/desktop/api/DXGIDebug/nn-dxgidebug-idxgidebug)
-   [**IDXGIInfoQueue**](/windows/desktop/api/DXGIDebug/nn-dxgidebug-idxgiinfoqueue)

Para acessar o [**DXGIGetDebugInterface**](/windows/desktop/api/DXGIDebug/nf-dxgidebug-dxgigetdebuginterface), chame a função [**GetModuleHandle**](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulehandlea) para obter Dxgidebug.dll e a função [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para obter o endereço de **DXGIGetDebugInterface**. Em seguida, você pode chamar **DXGIGetDebugInterface** para obter a interface [**IDXGIDebug**](/windows/desktop/api/DXGIDebug/nn-dxgidebug-idxgidebug) ou [**IDXGIInfoQueue**](/windows/desktop/api/DXGIDebug/nn-dxgidebug-idxgiinfoqueue) .

Para obter informações sobre como depurar aplicativos DirectX remotamente, consulte [Depurando aplicativos DirectX remotamente](../direct3dtools/debugging-directx-apps-remotely.md).

## <a name="related-topics"></a>Tópicos relacionados

[Guia de programação para DXGI](dx-graphics-dxgi-overviews.md)
