---
title: Atualização de plataforma para o Windows 7
description: Este tópico descreve as melhorias nos componentes da pilha gráfica do Windows 7 que se tornam disponíveis por meio da atualização de plataforma para o Windows 7.
ms.assetid: C6DC0D38-E17C-4924-AF7C-6AE74C6C50D1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49fd1e6e2681673d2bb2bab7a4a6de42f77988eb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103823936"
---
# <a name="platform-update-for-windows-7"></a>Atualização de plataforma para o Windows 7

Este tópico descreve as melhorias nos componentes da pilha gráfica do Windows 7 que se tornam disponíveis por meio da [atualização de plataforma para o Windows 7](https://support.microsoft.com/kb/2670838).

Quando instalado no Windows 7, a atualização da plataforma para o Windows 7 atualiza o Windows 7 com a funcionalidade disponível no Windows 8. Por exemplo, esses componentes do Windows 8 se tornam disponíveis com a funcionalidade completa:

-   Direct2D 1,1 (incluindo efeitos de Direct2D)
-   DirectWrite
-   Windows Imaging Component (WIC)

Eles fornecem funcionalidade parcial:

-   Direct3D 11,1
-   DXGI 1,2

E, por exemplo, este componente não está disponível:

-   DirectComposition (DComp)

Consulte estes tópicos para obter informações sobre Direct2D, DirectWrite e WIC com a atualização de plataforma:

-   [O que há de novo no Direct2D para Windows 8 (Windows)](/windows/desktop/Direct2D/what-s-new-in-direct2d-for-windows-8-consumer-preview)
-   [O que há de novo no DirectWrite para Windows 8 (Windows)](/windows/desktop/DirectWrite/what-s-new-in-directwrite-for-windows-8-consumer-preview)
-   [O que há de novo para o WIC no Windows 8 (Windows)](/previous-versions//hh994467(v=vs.85))

Consulte estes tópicos para obter informações sobre Direct3D e DXGI com a atualização da plataforma:

-   [Recursos do D3D 11.1](/windows/desktop/direct3d11/direct3d-11-1-features)
-   [Aprimoramentos de DXGI 1,2](/windows/desktop/direct3ddxgi/dxgi-1-2-improvements)

Após a instalação da atualização da plataforma, as interfaces introduzidas no Direct3D 11.1 e DXGI 1,2 estarão disponíveis com a funcionalidade parcial. Os recursos desses componentes gráficos estão vinculados diretamente aos componentes de kernel de gráficos, drivers gráficos e hardware de gráficos. Antes de usar o Direct3D 11.1 no Windows 7, familiarize-se com estas especificações:

-   O Windows 8 introduziu o modelo de driver do WDDM 1,2, que forneceu melhorias na superfície da API associada a todos os [níveis de recursos](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro). Ao ler a documentação do Direct3D 11.1, entenda que os *novos drivers* significam drivers WDDM 1,2. Essas versões de driver atualizadas, bem como a maioria dos recursos opcionais expostos por meio do [**CheckFeatureSupport**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-checkfeaturesupport), estão indisponíveis no Windows 7. Como não há nenhuma garantia de que esses recursos opcionais estejam disponíveis, verifique se seus aplicativos têm comportamentos de fallback apropriados caso a funcionalidade desejada não esteja disponível.

    Há uma exceção importante. Vários recursos, como [**PSSetConstantBuffers1**](/windows/desktop/api/d3d11_1/nf-d3d11_1-id3d11devicecontext1-pssetconstantbuffers1) com deslocamentos de buffer constante, exigem novos drivers para o [nível de recurso](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 10 e superior, mas são, na verdade, emulados para o nível de recurso 9. Essa emulação está disponível no Windows 7 com a atualização da plataforma. Consulte [**\_ Opções de \_ \_ D3D11 \_ de dados de recursos do D3D11**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_feature_data_d3d11_options) para obter mais informações sobre quais recursos são emulados.

-   O modelo de driver do Windows 8 WDDM 1,2 dá suporte a uma nova geração de hardware, exposto por meio do [nível de recurso](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) do D3D 11,1. O Windows 7 com a atualização de plataforma dá suporte apenas ao modelo de driver do WDDM 1,1 e, portanto, o suporte de hardware de nível 11,1 não está disponível (por meio da atualização de plataforma). No Windows 7 com a atualização de plataforma, o [**D3D11CreateDevice**](/windows/desktop/api/d3d11/nf-d3d11-d3d11createdevice) sempre retorna um nível de recurso de 11,0 ou inferior, exceto por um dispositivo de referência que pode ser usado para testar um caminho de código 11,1 no Windows 7. Use apenas os recursos disponíveis nos níveis de recurso de destino, conforme descrito na referência de nível de recurso.
-   Alguns novos métodos introduzidos no DGXI 1,2 não têm suporte completo com a atualização de plataforma para o Windows 7. você pode testar a disponibilidade dessas funções chamando-as diretamente e verificando um código de erro. Certifique-se de que seus aplicativos direcionados para o Windows 7 com a atualização de plataforma tenham um fallback no local quando a funcionalidade desejada não estiver disponível. Essas classes de recursos não estão disponíveis na atualização da plataforma para o Windows 7:

    -   Estéreo
    -   Permuta não direcionar para HWNDs
    -   Notificações de status do oclusão
    -   Duplicação de área de trabalho
    -   Recursos de identificador NT

    Especificamente, as APIs a seguir retornarão \_ erro dxgi \_ sem suporte, \_ chamada de erro dxgi \_ inválida \_ , e \_ NOTIMPL ou E \_ INVALIDARG:

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
    -   [**IDXGISwapChain1**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgiswapchain1)::[**getrotation**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-getrotation)
    -   [**IDXGIOutput1**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgioutput1)::[**DuplicateOutput**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgioutput1-duplicateoutput)
    -   [**IDXGIDevice2**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgidevice2)::[**EnqueueSetEvent**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgidevice2-enqueuesetevent)
    -   [**IDXGIResource1**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgiresource1)::[**CreateSharedHandle**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgiresource1-createsharedhandle)
    -   [**IDXGIFactory2**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2)::[**GetSharedResourceAdapterLuid**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-getsharedresourceadapterluid)
    -   [**ID3D11Device1**](/windows/desktop/api/d3d11_1/nn-d3d11_1-id3d11device1)::[**OpenSharedResource1**](/windows/desktop/api/d3d11_1/nf-d3d11_1-id3d11device1-opensharedresource1)
    -   [**ID3D11Device1**](/windows/desktop/api/d3d11_1/nn-d3d11_1-id3d11device1)::[**OpenSharedResourceByName**](/windows/desktop/api/d3d11_1/nf-d3d11_1-id3d11device1-opensharedresourcebyname)

-   Essas APIs têm diferenças de comportamento, conforme observado:
    -   [**IDXGIFactory2**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2)::[**CreateSwapChainForHwnd**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforhwnd) usa uma [**estrutura \_ \_ \_ DESC1 de cadeia de permuta dxgi**](/windows/desktop/api/dxgi1_2/ns-dxgi1_2-dxgi_swap_chain_desc1) , que tem um campo para **dimensionamento**. [**Dxgi \_ Não \_**](/windows/desktop/api/dxgi1_2/ne-dxgi1_2-dxgi_scaling) há suporte para o dimensionamento de nenhum no Windows 7 com a atualização de plataforma e faz com que o **CreateSwapChainForHwnd** retorne a chamada de \_ erro dxgi \_ inválida \_ quando chamada.
    -   [**IDXGISwapChain1**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgiswapchain1)::[**setBackgroundColor**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-setbackgroundcolor) só é útil quando definido em um SwapChain usando o \_ dimensionamento de dxgi \_ nenhum. Seu valor ainda é armazenado e pode ser recuperado, mas não tem nenhum efeito.
    -   [**IDXGIDisplayControl**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgidisplaycontrol)::[**IsStereoEnabled**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgidisplaycontrol-isstereoenabled), [**IDXGIFactory2**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2)::[**IsWindowedStereoEnabled**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-iswindowedstereoenabled)e [**IDXGISwapChain1**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgiswapchain1)::[**IsTemporaryMonoSupported**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-istemporarymonosupported) retorna **false**.
    -   [**IDXGIOutput1**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgioutput1)::[**GetDisplayModeList1**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgioutput1-getdisplaymodelist1) e **IDXGIOutput1**::[**FindClosestMatchingMode1**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgioutput1-findclosestmatchingmode1) foram adicionados para facilitar os modos de exibição de estéreo. O estéreo não tem suporte na atualização da plataforma para o Windows 7, portanto, esse método é equivalente a [**IDXGIOutput**](/windows/desktop/api/dxgi/nn-dxgi-idxgioutput)::[**FindClosestMatchingMode**](/windows/desktop/api/dxgi/nf-dxgi-idxgioutput-findclosestmatchingmode) como [**\_ modo dxgi \_ DESC1**](/windows/desktop/api/dxgi1_2/ns-dxgi1_2-dxgi_mode_desc1). O estéreo será sempre falso.
    -   [**IDXGIDevice2**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgidevice2)::[**OfferResources**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgidevice2-offerresources) e **IDXGIDevice2**::[**ReclaimResources**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgidevice2-reclaimresources) não têm suporte na atualização de plataforma para o Windows 7. No entanto, o tempo de execução ainda permite que eles sejam chamados e executa a validação de que estão sendo usados corretamente em recursos não compartilhados.
    -   Os dispositivos [Warp](/windows/desktop/direct3d11/overviews-direct3d-11-devices-create-warp) só dão suporte ao [nível de recurso](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 11,0. Ou seja, os dispositivos deformados criados pela passagem do [ \_ tipo de driver D3D \_ \_ Warp](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_driver_type) no parâmetro *driverType* de [**D3D11CreateDevice**](/windows/desktop/api/d3d11/nf-d3d11-d3d11createdevice) não dão suporte a 11,1, nem oferecem suporte a superfícies compartilhadas.
-   Para os desenvolvedores que estão trabalhando atualmente em aplicativos no Microsoft Visual Studio 2010 ou anterior usando o sinalizador de [**\_ \_ \_ depuração de dispositivo D3D11 Create**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_create_device_flag) , lembre-se de que as chamadas para [**D3D11CreateDevice**](/windows/desktop/api/d3d11/nf-d3d11-d3d11createdevice) falharão. Isso ocorre porque o tempo de execução do D3D 11.1 agora requer o D3D11 \_1SDKLayers.dll em vez de D3D11SDKLayers.dll. Para obter essa nova DLL (D3D11 \_1SDKLayers.dll), instale o [SDK do Windows 8](https://dev.windows.com/downloads/windows-8-sdk)ou o [Visual Studio 2012](https://www.microsoft.com/visualstudio/eng/downloads)ou as ferramentas de depuração remota do Visual Studio 2012. Consulte a documentação da [camada de depuração](/windows/desktop/direct3d11/overviews-direct3d-11-devices-layers) para obter mais informações.

 

 