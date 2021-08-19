---
title: Usando a camada de depuração para depurar aplicativos
description: Aqui, falamos sobre como habilitar a camada de depuração e alguns dos problemas que você pode evitar usando a camada de depuração.
ms.assetid: 3C2B0A12-FB57-4400-BE39-05ED23F552C7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c6ac5492b96c40b4395b2c501b764c646a8edbb06d3a6386a15cbb2534778d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117912730"
---
# <a name="using-the-debug-layer-to-debug-apps"></a>Usando a camada de depuração para depurar aplicativos

Recomendamos que você use a [camada de depuração](overviews-direct3d-11-devices-layers.md) para depurar seus aplicativos para garantir que eles sejam limpos de erros e avisos. A camada de depuração ajuda você a escrever código Direct3D. Além disso, sua produtividade pode aumentar quando você usa a camada de depuração porque você pode ver imediatamente as causas de erros de renderização obscurecidos ou até mesmo telas pretas em sua origem. A camada de depuração fornece avisos para muitos problemas. Por exemplo, a camada de depuração fornece avisos para esses problemas:

-   Esqueceu de definir uma textura, mas lê-la no sombreador de pixel
-   Profundidade de saída, mas não tem nenhum estado de estêncil de profundidade limitado
-   Falha na criação da textura com INVALIDARG

Aqui, falamos sobre como habilitar a camada [de depuração](overviews-direct3d-11-devices-layers.md) e alguns dos problemas que você pode evitar usando a camada de depuração.

-   [Habilitando a camada de depuração](#enabling-the-debug-layer)
-   [Impedindo erros em seu aplicativo com a camada de depuração](#preventing-errors-in-your-app-with-the-debug-layer)
    -   [Não passar ponteiros NULL para o Mapa](#dont-pass-null-pointers-to-map)
    -   [Caixa de origem de limite nos recursos de origem e destino](#confine-source-box-within-source-and-destination-resources)
    -   [Não descarte DiscardResource ou DiscardView](#dont-drop-discardresource-or-discardview)
-   [Tópicos relacionados](#related-topics)

## <a name="enabling-the-debug-layer"></a>Habilitando a camada de depuração

Para habilitar a camada [de depuração](overviews-direct3d-11-devices-layers.md), especifique o sinalizador [**D3D11 \_ CREATE DEVICE \_ \_ DEBUG**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_create_device_flag) no parâmetro *Flags* ao chamar a [**função D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) para criar o dispositivo de renderização. Este código de exemplo mostra como habilitar a camada de depuração quando seu projeto Microsoft Visual Studio está em um build de depuração:


```C++
        UINT creationFlags = D3D11_CREATE_DEVICE_BGRA_SUPPORT;
#if defined(_DEBUG)
        // If the project is in a debug build, enable the debug layer.
        creationFlags |= D3D11_CREATE_DEVICE_DEBUG;
#endif
        // Define the ordering of feature levels that Direct3D attempts to create.
        D3D_FEATURE_LEVEL featureLevels[] =
        {
            D3D_FEATURE_LEVEL_11_1,
            D3D_FEATURE_LEVEL_11_0,
            D3D_FEATURE_LEVEL_10_1,
            D3D_FEATURE_LEVEL_10_0,
            D3D_FEATURE_LEVEL_9_3,
            D3D_FEATURE_LEVEL_9_1
        };

        ComPtr<ID3D11Device> d3dDevice;
        ComPtr<ID3D11DeviceContext> d3dDeviceContext;
        DX::ThrowIfFailed(
            D3D11CreateDevice(
                nullptr,                    // specify nullptr to use the default adapter
                D3D_DRIVER_TYPE_HARDWARE,
                nullptr,                    // specify nullptr because D3D_DRIVER_TYPE_HARDWARE 
                                            // indicates that this function uses hardware
                creationFlags,              // optionally set debug and Direct2D compatibility flags
                featureLevels,
                ARRAYSIZE(featureLevels),
                D3D11_SDK_VERSION,          // always set this to D3D11_SDK_VERSION
                &d3dDevice,
                nullptr,
                &d3dDeviceContext
                )
            );
```



## <a name="preventing-errors-in-your-app-with-the-debug-layer"></a>Impedindo erros em seu aplicativo com a camada de depuração

Se você usar indevidamente a API do Direct3D 11 ou passar parâmetros incorretos, a saída de depuração da camada [de depuração](overviews-direct3d-11-devices-layers.md) relata um erro ou um aviso. Em seguida, você pode corrigir seu erro. Em seguida, vamos ver alguns problemas de codificação que podem causar um comportamento indefinido ou até mesmo o sistema operacional falhar. Você pode capturar e evitar esses problemas usando a camada de depuração.

### <a name="dont-pass-null-pointers-to-map"></a>Não passar ponteiros NULL para o Mapa

Se você passar **NULL** para o *parâmetro pResource* ou *pMappedResource* do método [**ID3D11DeviceContext::Map,**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) o comportamento de **Map** será indefinido. Se você criou um dispositivo que dá suporte apenas à camada [principal,](overviews-direct3d-11-devices-layers.md)os parâmetros inválidos para **Map** poderão falhar no sistema operacional. Se você criou um dispositivo que dá suporte à [camada de depuração](overviews-direct3d-11-devices-layers.md), a saída de depuração relata um erro nessa chamada **de Mapa** inválida.

### <a name="confine-source-box-within-source-and-destination-resources"></a>Caixa de origem de limite nos recursos de origem e destino

Em uma chamada para o [**método ID3D11DeviceContext::CopySubresourceRegion,**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-copysubresourceregion) a caixa de origem deve estar dentro do recurso de origem. Os deslocamentos de destino(x, y e z) permitem que a caixa de origem seja deslocada ao escrever no recurso de destino, mas as dimensões da caixa de origem e os deslocamentos devem estar dentro do tamanho do recurso. Se você tentar copiar fora do recurso de destino ou especificar uma caixa de origem maior que o recurso de origem, o comportamento de **CopySubresourceRegion** será indefinido. Se você criou um dispositivo que dá suporte à camada [de depuração](overviews-direct3d-11-devices-layers.md), a saída de depuração relata um erro nessa chamada **CopySubresourceRegion** inválida. Parâmetros inválidos para **CopySubresourceRegion** causam comportamento indefinido e podem resultar em renderização incorreta, recorte, nenhuma cópia ou até mesmo a remoção do dispositivo de renderização.

### <a name="dont-drop-discardresource-or-discardview"></a>Não descarte DiscardResource ou DiscardView

O runtime descarta uma chamada para [**ID3D11DeviceContext1::D iscardResource**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-discardresource) ou [**ID3D11DeviceContext1::D iscardView,**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-discardview) a menos que você crie o recurso corretamente.

O recurso que você passa para [**ID3D11DeviceContext1::D iscardResource**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-discardresource) deve ter sido criado usando [**D3D11 \_ USAGE \_ DEFAULT**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage) ou [**D3D11 \_ USAGE \_ DYNAMIC, caso**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage)contrário, o runtime descarta a chamada para **DiscardResource**.

O recurso que baseia a exibição que você passa para [**ID3D11DeviceContext1::D iscardView**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-discardview) deve ter sido criado usando [**D3D11 \_ USAGE \_ DEFAULT**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage) ou [**D3D11 \_ USAGE \_ DYNAMIC, caso**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage)contrário, o runtime descarta a chamada para **DiscardView**.

Se você criou um dispositivo que dá suporte à [camada de depuração](overviews-direct3d-11-devices-layers.md), a saída de depuração relata um erro em relação à chamada descartado.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Camadas de software](overviews-direct3d-11-devices-layers.md)
</dt> </dl>

 

 




