---
title: Como criar uma cadeia de permuta
description: Este tópico mostra como criar uma cadeia de permuta que encapsula dois ou mais buffers usados para renderização e exibição.
ms.assetid: 0e290b37-0807-42c7-9e50-fd2db6affb14
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71ef97b261d9831c451c8a81bfc1f4d9d13b1cd423ac28f38de4b90c1d4ae100
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118530568"
---
# <a name="how-to-create-a-swap-chain"></a>Como criar uma cadeia de permuta

Este tópico mostra como criar uma cadeia de permuta que encapsula dois ou mais buffers usados para renderização e exibição. Normalmente, eles contêm um buffer frontal que é apresentado ao dispositivo de exibição e um buffer de fundo que serve como o destino de renderização. Depois que o contexto imediato for feito a renderização para o buffer de fundo, a cadeia de permuta apresentará o buffer de fundo, alternando os dois buffers.

A cadeia de permuta define várias características de renderização, incluindo:

-   O tamanho da área de renderização.
-   A taxa de atualização de exibição.
-   O modo de exibição.
-   O formato da superfície.

Defina as características da cadeia de permuta preenchendo uma estrutura [**\_ DXGI SWAP CHAIN \_ \_ DESC**](/windows/desktop/api/dxgi/ns-dxgi-dxgi_swap_chain_desc) e inicializando uma interface [**IDXGISwapChain.**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain) Inicialize uma cadeia de permuta chamando [**IDXGIFactory::CreateSwapChain**](/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-createswapchain) ou [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain).

## <a name="create-a-device-and-a-swap-chain"></a>Criar um dispositivo e uma cadeia de permuta

Para inicializar um dispositivo e uma cadeia de permuta, use uma das duas funções a seguir:

-   Use [**a função D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain) quando quiser inicializar a cadeia de permuta ao mesmo tempo que a inicialização do dispositivo. Essa geralmente é a opção mais fácil.

-   Use a [**função D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) quando você já tiver criado uma cadeia de permuta usando [**IDXGIFactory::CreateSwapChain**](/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-createswapchain).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Dispositivos](overviews-direct3d-11-devices.md)
</dt> <dt>

[Como usar o Direct3D 11](how-to-use-direct3d-11.md)
</dt> </dl>

 

 