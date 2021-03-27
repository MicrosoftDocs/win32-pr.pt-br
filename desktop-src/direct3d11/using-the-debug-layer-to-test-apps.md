---
title: Usando a camada de depuração para depurar aplicativos
description: Aqui, falamos sobre como habilitar a camada de depuração e alguns dos problemas que você pode evitar usando a camada de depuração.
ms.assetid: 3C2B0A12-FB57-4400-BE39-05ED23F552C7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aaa3f4748da6893470e3bb6631c4228ec1ae3d48
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635127"
---
# <a name="using-the-debug-layer-to-debug-apps"></a>Usando a camada de depuração para depurar aplicativos

Recomendamos que você use a [camada de depuração](overviews-direct3d-11-devices-layers.md) para depurar seus aplicativos a fim de garantir que eles estejam com limpeza de erros e avisos. A camada de depuração ajuda a escrever código Direct3D. Além disso, sua produtividade pode aumentar quando você usa a camada de depuração, pois você pode ver imediatamente as causas de erros de renderização obscuras ou até mesmo de telas pretas em sua origem. A camada de depuração fornece avisos para muitos problemas. Por exemplo, a camada de depuração fornece avisos para esses problemas:

-   Esqueceu de definir uma textura, mas lê-la no sombreador de pixel
-   Profundidade de saída, mas não há limite de estado de estêncil de profundidade
-   Falha na criação de textura com INVALIDARG

Aqui, falamos sobre como habilitar a [camada de depuração](overviews-direct3d-11-devices-layers.md) e alguns dos problemas que você pode evitar usando a camada de depuração.

-   [Habilitando a camada de depuração](#enabling-the-debug-layer)
-   [Impedindo erros em seu aplicativo com a camada de depuração](#preventing-errors-in-your-app-with-the-debug-layer)
    -   [Não passar ponteiros nulos para o mapa](#dont-pass-null-pointers-to-map)
    -   [Caixa restringir origem nos recursos de origem e de destino](#confine-source-box-within-source-and-destination-resources)
    -   [Não remova DiscardResource ou DiscardView](#dont-drop-discardresource-or-discardview)
-   [Tópicos relacionados](#related-topics)

## <a name="enabling-the-debug-layer"></a>Habilitando a camada de depuração

Para habilitar a [camada de depuração](overviews-direct3d-11-devices-layers.md), especifique o sinalizador de [**depuração do \_ \_ dispositivo \_ D3D11 Create**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_create_device_flag) no parâmetro *flags* ao chamar a função [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) para criar o dispositivo de renderização. Este código de exemplo mostra como habilitar a camada de depuração quando seu projeto de Microsoft Visual Studio está em uma compilação de depuração:


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

Se você indevidamente a API do Direct3D 11 ou passar parâmetros inválidos, a saída de depuração da [camada de depuração](overviews-direct3d-11-devices-layers.md) relatará um erro ou um aviso. Em seguida, você pode corrigir o erro. Em seguida, examinaremos alguns problemas de codificação que podem causar um comportamento indefinido ou até mesmo o sistema operacional a falhar. Você pode detectar e evitar esses problemas usando a camada de depuração.

### <a name="dont-pass-null-pointers-to-map"></a>Não passar ponteiros nulos para o mapa

Se você passar **NULL** para o parâmetro *PreSource* ou *pMappedResource* do método [**ID3D11DeviceContext:: map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) , o comportamento do **mapa** será indefinido. Se você criou um dispositivo que dá suporte apenas à [camada principal](overviews-direct3d-11-devices-layers.md), os parâmetros inválidos para **mapear** podem travar o sistema operacional. Se você criou um dispositivo que dá suporte à [camada de depuração](overviews-direct3d-11-devices-layers.md), a saída de depuração relatará um erro nessa chamada de **mapa** inválida.

### <a name="confine-source-box-within-source-and-destination-resources"></a>Caixa restringir origem nos recursos de origem e de destino

Em uma chamada para o método [**ID3D11DeviceContext:: CopySubresourceRegion**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-copysubresourceregion) , a caixa Source deve estar dentro do recurso de origem. Os deslocamentos de destino, (x, y e z) permitem que a caixa de origem seja deslocada ao gravar no recurso de destino, mas as dimensões da caixa de origem e dos deslocamentos devem estar dentro do tamanho do recurso. Se você tentar copiar fora do recurso de destino ou especificar uma caixa de origem que seja maior do que o recurso de origem, o comportamento de **CopySubresourceRegion** será indefinido. Se você criou um dispositivo que dá suporte à [camada de depuração](overviews-direct3d-11-devices-layers.md), a saída de depuração relatará um erro nessa chamada **CopySubresourceRegion** inválida. Parâmetros inválidos para **CopySubresourceRegion** causam comportamento indefinido e podem resultar em renderização incorreta, recorte, sem cópia ou até mesmo a remoção do dispositivo de renderização.

### <a name="dont-drop-discardresource-or-discardview"></a>Não remova DiscardResource ou DiscardView

O tempo de execução descarta uma chamada para [**ID3D11DeviceContext1::D iscardresource**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-discardresource) ou [**ID3D11DeviceContext1::D iscardview**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-discardview) , a menos que você crie o recurso corretamente.

O recurso que você passa para [**ID3D11DeviceContext1::D iscardresource**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-discardresource) deve ter sido criado usando [**D3D11 \_ uso \_ padrão**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage) ou o [**uso de D3D11 \_ \_ dinâmico**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage), caso contrário, o tempo de execução descartará a chamada para **DiscardResource**.

O recurso que se baseia no modo de exibição que você passa para [**ID3D11DeviceContext1::D iscardview**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-discardview) deve ter sido criado usando [**D3D11 \_ uso \_ padrão**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage) ou o [**uso de D3D11 \_ \_ dinâmico**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage), caso contrário, o tempo de execução descartará a chamada para **DiscardView**.

Se você criou um dispositivo que dá suporte à [camada de depuração](overviews-direct3d-11-devices-layers.md), a saída de depuração relatará um erro em relação à chamada descartada.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Camadas de software](overviews-direct3d-11-devices-layers.md)
</dt> </dl>

 

 




