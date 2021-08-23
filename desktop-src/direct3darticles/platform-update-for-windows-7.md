---
title: Atualização de plataforma para Windows 7
description: Este tópico descreve as melhorias nos componentes da pilha Windows gráficos do Windows 7 que se tornam disponíveis por meio da Atualização de Plataforma para Windows 7.
ms.assetid: C6DC0D38-E17C-4924-AF7C-6AE74C6C50D1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a577d74613a22a176c038b6c85e53b94f413edbc49d07a886a613ddff5a83b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119627576"
---
# <a name="platform-update-for-windows-7"></a>Atualização de plataforma para Windows 7

Este tópico descreve as melhorias nos componentes da pilha de gráficos Windows 7 que se tornam disponíveis por meio da Atualização de Plataforma [para Windows 7](https://support.microsoft.com/kb/2670838).

Quando instalado no Windows 7, a Atualização de Plataforma para o Windows 7 atualiza Windows 7 com a funcionalidade disponível Windows 8. Por exemplo, esses Windows 8 estão disponíveis com funcionalidade completa:

-   Direct2D 1.1 (incluindo Direct2D efeitos)
-   DirectWrite
-   Windows Imaging Component (WIC)

Eles fornecem funcionalidade parcial:

-   Direct3D 11.1
-   DXGI 1.2

E, por exemplo, esse componente não está disponível:

-   DirectComposition (DComp)

Consulte estes tópicos para obter informações sobre Direct2D, DirectWrite e WIC com a atualização da plataforma:

-   [Novidades no Direct2D para Windows 8 (Windows)](/windows/desktop/Direct2D/what-s-new-in-direct2d-for-windows-8-consumer-preview)
-   [Novidades no DirectWrite para Windows 8 (Windows)](/windows/desktop/DirectWrite/what-s-new-in-directwrite-for-windows-8-consumer-preview)
-   [Novidades do WIC no Windows 8 (Windows)](/previous-versions//hh994467(v=vs.85))

Consulte estes tópicos para obter informações sobre Direct3D e DXGI com a atualização da plataforma:

-   [Recursos D3D11.1](/windows/desktop/direct3d11/direct3d-11-1-features)
-   [Melhorias do DXGI 1.2](/windows/desktop/direct3ddxgi/dxgi-1-2-improvements)

Depois que a atualização da plataforma tiver sido instalada, as interfaces introduzidas no Direct3D11.1 e no DXGI 1.2 estarão disponíveis com funcionalidade parcial. Os recursos desses componentes gráficos estão vinculados diretamente aos componentes de kernel gráficos, drivers gráficos e hardware gráfico. Antes de usar o Direct3D11.1 no Windows 7, familiarizar-se com estas especificações:

-   Windows 8 introduziu o modelo de driver WDDM 1.2, que forneceu melhorias na superfície de API associada para todos os níveis [de recursos](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro). Ao ler a documentação do Direct3D11.1, entenda que novos drivers significam *drivers* WDDM 1.2. Essas versões de driver atualizadas, bem como a maioria dos recursos opcionais expostos por meio do [**CheckFeatureSupport**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-checkfeaturesupport), não estão disponíveis Windows 7. Como não há nenhuma garantia de que esses recursos opcionais estão disponíveis, certifique-se de que seus aplicativos tenham comportamentos de fallback apropriados no caso de a funcionalidade desejada não estar disponível.

    Há uma exceção importante. Vários recursos, como [**PSSetConstantBuffers1**](/windows/desktop/api/d3d11_1/nf-d3d11_1-id3d11devicecontext1-pssetconstantbuffers1) com deslocamentos de buffer constantes, exigem novos drivers para o nível [de](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) recurso 10 e superior, mas são realmente emulados para o nível de recurso 9. Essa emulação está disponível no Windows 7 com a atualização da plataforma. Confira [**OPÇÕES D3D11 \_ FEATURE DATA \_ \_ D3D11 para \_**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_feature_data_d3d11_options) obter mais informações sobre quais recursos são emulados.

-   O Windows 8 modelo de driver WDDM 1.2 dá suporte a uma [](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) nova geração de hardware, exposta por meio do nível de recurso D3D 11.1. Windows 7 com a atualização da plataforma dá suporte apenas ao modelo de driver WDDM 1.1 e, portanto, o suporte ao hardware de nível de recurso 11.1 não está disponível (por meio da atualização da plataforma). No Windows 7 com a atualização da plataforma, [**D3D11CreateDevice**](/windows/desktop/api/d3d11/nf-d3d11-d3d11createdevice) sempre retorna um nível de recurso 11.0 ou inferior, exceto com um dispositivo de referência que pode ser usado para testar um caminho de código 11.1 no Windows 7. Use apenas os recursos disponíveis em seus níveis de recurso de destino, conforme descrito na referência de nível de recurso.
-   Alguns novos métodos introduzidos no DGXI 1.2 não têm suporte total com a Atualização de Plataforma para o Windows 7. Você pode testar a disponibilidade dessas funções chamando-as diretamente e verificando se há um código de erro. Certifique-se de que seus aplicativos Windows 7 com a atualização da plataforma tenham um fallback em funcionamento quando a funcionalidade desejada não estiver disponível. Essas classes de recursos não estão disponíveis na Atualização de Plataforma para Windows 7:

    -   Estéreo
    -   Permutas que não direcionam Hwnds
    -   Notificações de status de oclusão
    -   Duplicação da área de trabalho
    -   Recursos do NT Handle

    Especificamente, as SEGUINTES APIs retornarão ERRO DXGI SEM SUPORTE, CHAMADA INVÁLIDA DE \_ \_ ERRO DXGI, \_ E \_ \_ \_ NOTIMPL ou E \_ INVALIDARG:

    -   [**IDXGIFactory2**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2)::[**CreateSwapChainForCoreWindow**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcorewindow)
    -   [**IDXGIFactory2**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2)::[**CreateSwapChainForComposition**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcomposition)
    -   [**IDXGIFactory2**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2)::[**RegisterStereoStatusWindow**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-registerstereostatuswindow)
    -   [**IDXGIFactory2**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2)::[**RegisterStereoStatusEvent**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-registerstereostatusevent)
    -   [**IDXGIFactory2**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2)::[**UnregisterStereoStatus**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-unregisterstereostatus)
    -   [**IDXGIFactory2**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2)::[**RegisterOcclusionStatusWindow**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-registerocclusionstatuswindow)
    -   [**IDXGIFactory2**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2)::[**RegisterOcclusionStatusEvent**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-registerocclusionstatusevent)
    -   [**IDXGIFactory2**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2)::[**UnregisterOcclusionStatus**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-unregisterocclusionstatus)
    -   [**IDXGISwapChain1**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgiswapchain1)::[**GetCoreWindow**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-getcorewindow)
    -   [**IDXGISwapChain1**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgiswapchain1)::[**SetRotation**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-setrotation)
    -   [**IDXGISwapChain1**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgiswapchain1)::[**GetRotation**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-getrotation)
    -   [**IDXGIOutput1**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgioutput1)::[**DuplicateOutput**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgioutput1-duplicateoutput)
    -   [**IDXGIDevice2**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgidevice2)::[**EnqueueSetEvent**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgidevice2-enqueuesetevent)
    -   [**IDXGIResource1**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgiresource1)::[**CreateSharedHandle**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgiresource1-createsharedhandle)
    -   [**IDXGIFactory2**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2)::[**GetSharedResourceAdapterLuid**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-getsharedresourceadapterluid)
    -   [**ID3D11Device1**](/windows/desktop/api/d3d11_1/nn-d3d11_1-id3d11device1)::[**OpenSharedResource1**](/windows/desktop/api/d3d11_1/nf-d3d11_1-id3d11device1-opensharedresource1)
    -   [**ID3D11Device1**](/windows/desktop/api/d3d11_1/nn-d3d11_1-id3d11device1)::[**OpenSharedResourceByName**](/windows/desktop/api/d3d11_1/nf-d3d11_1-id3d11device1-opensharedresourcebyname)

-   Essas APIs têm diferenças de comportamento, conforme foi feito:
    -   [**IDXGIFactory2**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2)::[**CreateSwapChainForHwnd**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforhwnd) aceita uma estrutura [**\_ DXGI SWAP CHAIN \_ \_ DESC1,**](/windows/desktop/api/dxgi1_2/ns-dxgi1_2-dxgi_swap_chain_desc1) que tem um campo para **Dimensionamento**. [**DXGI \_ NÃO há \_ suporte para SCALING NONE**](/windows/desktop/api/dxgi1_2/ne-dxgi1_2-dxgi_scaling) no Windows 7 com a atualização da plataforma e faz com que **CreateSwapChainForHwnd** retorne UMA CHAMADA INVÁLIDA DO ERRO DXGI quando \_ \_ \_ chamada.
    -   [**IDXGISwapChain1**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgiswapchain1)::[**SetBackgroundColor**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-setbackgroundcolor) só é útil quando definido em uma swapchain usando DXGI \_ SCALING \_ NONE. Seu valor ainda é armazenado e pode ser recuperado, mas não tem nenhum efeito.
    -   [**IDXGIDisplayControl**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgidisplaycontrol)::[**IsStereoEnabled,**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgidisplaycontrol-isstereoenabled) [**IDXGIFactory2**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2)::[**IsWindowedStereoEnabled**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-iswindowedstereoenabled)e [**IDXGISwapChain1**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgiswapchain1)::[**IsTemporaryMonoSupported**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-istemporarymonosupported) **retornam FALSE.**
    -   [**IDXGIOutput1**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgioutput1)::[**GetDisplayModeList1**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgioutput1-getdisplaymodelist1) e **IDXGIOutput1**::[**FindClosestMatchingMode1**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgioutput1-findclosestmatchingmode1) foram adicionados para facilitar os modos de exibição estéreo. Não há suporte para estéreo na Atualização de Plataforma para Windows 7, portanto, esse método é equivalente a [**IDXGIOutput**](/windows/desktop/api/dxgi/nn-dxgi-idxgioutput)::[**FindClosestMatchingMode**](/windows/desktop/api/dxgi/nf-dxgi-idxgioutput-findclosestmatchingmode) como [**DXGI \_ MODE \_ DESC1**](/windows/desktop/api/dxgi1_2/ns-dxgi1_2-dxgi_mode_desc1). Estéreo sempre será FALSE.
    -   [**IDXGIDevice2**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgidevice2)::[**OfferResources**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgidevice2-offerresources) e **IDXGIDevice2**:: Não há suporte para [**ReclaimResources**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgidevice2-reclaimresources) na Atualização de Plataforma para Windows 7. No entanto, o runtime ainda permite que eles sejam chamados e executa a validação de que eles estão sendo usados corretamente em recursos não compartilhados.
    -   [Os dispositivos WARP](/windows/desktop/direct3d11/overviews-direct3d-11-devices-create-warp) só [são compatíveis com](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) o nível de recurso 11.0. Ou seja, dispositivos WARP criados passando [D3D \_ DRIVER \_ TYPE \_ WARP](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_driver_type) no parâmetro *DriverType* [**de D3D11CreateDevice**](/windows/desktop/api/d3d11/nf-d3d11-d3d11createdevice) não são compatíveis com a 11.1 nem com superfícies compartilhadas.
-   Para desenvolvedores que trabalham atualmente em aplicativos no Microsoft Visual Studio 2010 ou anterior usando o sinalizador [**D3D11 \_ CREATE \_ DEVICE \_ DEBUG,**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_create_device_flag) esteja ciente de que as chamadas para [**D3D11CreateDevice**](/windows/desktop/api/d3d11/nf-d3d11-d3d11createdevice) falharão. Isso porque o runtime D3D11.1 agora requer D3D11 \_1SDKLayers.dll em vez de D3D11SDKLayers.dll. Para obter essa nova DLL (D3D111SDKLayers.dll), instale o \_ [SDK](https://dev.windows.com/downloads/windows-8-sdk)do Windows 8 ou [o Visual Studio 2012](https://www.microsoft.com/visualstudio/eng/downloads)ou as ferramentas de depuração remota do Visual Studio 2012. Confira a [documentação da Camada de Depuração](/windows/desktop/direct3d11/overviews-direct3d-11-devices-layers) para obter mais informações.

 

 