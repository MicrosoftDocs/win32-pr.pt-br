---
title: Recursos do Direct3D 11,2
description: A funcionalidade a seguir foi adicionada no Direct3D 11,2, que está incluído com Windows 8.1, Windows RT 8,1 e Windows Server 2012 R2.
ms.assetid: 2A2D9BBB-F53A-4187-A25B-F4E58C896EE2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 299b720bfb91297043c8e7d76beb50067eb64e17
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104967195"
---
# <a name="direct3d-112-features"></a>Recursos do Direct3D 11,2

A funcionalidade a seguir foi adicionada no Direct3D 11,2, que está incluído com Windows 8.1, Windows RT 8,1 e Windows Server 2012 R2.

-   [Recursos em ladrilho](#tiled-resources)
    -   [Verifique o suporte a recursos de ladrilho](#check-tiled-resources-support)
-   [Suporte estendido para dispositivos WARP](#extended-support-for-warp-devices)
-   [Anotar comandos gráficos](#annotate-graphics-commands)
-   [Vinculação de sombreador HLSL](#hlsl-shader-linking)
    -   [Grafo de vinculação de função (FLG)](#function-linking-graph-flg)
-   [Compilador HLSL de caixa de entrada](#inbox-hlsl-compiler)
-   [Tópicos relacionados](#related-topics)

## <a name="tiled-resources"></a>Recursos em ladrilho

O Direct3D 11,2 permite que você crie recursos com sublados que podem ser considerados como recursos lógicos grandes que usam pequenas quantidades de memória física. Os recursos por lado são úteis (por exemplo) com o terreno em jogos e a interface do usuário do aplicativo.

Os recursos em ladrilho são criados especificando-se o sinalizador de [**\_ \_ \_ lado diverso do recurso D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) . Para trabalhar com recurso de lado, use estas APIs:

-   [**ID3D11Device2::GetResourceTiling**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11device2-getresourcetiling)
-   [**ID3D11DeviceContext2::UpdateTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetiles)
-   [**ID3D11DeviceContext2::UpdateTileMappings**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetilemappings)
-   [**ID3D11DeviceContext2::CopyTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytiles)
-   [**ID3D11DeviceContext2::CopyTileMappings**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytilemappings)
-   [**ID3D11DeviceContext2::ResizeTilePool**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-resizetilepool)
-   [**ID3D11DeviceContext2::TiledResourceBarrier**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-tiledresourcebarrier)
-   **D3D11 \_ \_Recurso \_ de depuração desabilitar o \_ \_ \_ \_ rastreamento \_ e \_** o sinalizador de validação de mapeamento de recursos com [ **ID3D11Debug:: SetFeatureMask**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11debug-setfeaturemask)

Para obter mais informações sobre recursos de lado, consulte [recursos em ladrilho](tiled-resources.md).

### <a name="check-tiled-resources-support"></a>Verifique o suporte a recursos de ladrilho

Antes de usar os recursos ao lado do ladrilho, você precisa descobrir se o dispositivo dá suporte a recursos de lado. Veja como você verifica o suporte para os recursos do lado do xadrez:


```C++
HRESULT hr = D3D11CreateDevice(
    nullptr,                    // Specify nullptr to use the default adapter.
    D3D_DRIVER_TYPE_HARDWARE,   // Create a device using the hardware graphics driver.
    0,                          // Should be 0 unless the driver is D3D_DRIVER_TYPE_SOFTWARE.
    creationFlags,              // Set debug and Direct2D compatibility flags.
    featureLevels,              // List of feature levels this app can support.
    ARRAYSIZE(featureLevels),   // Size of the list above.
    D3D11_SDK_VERSION,          // Always set this to D3D11_SDK_VERSION for Windows Store apps.
    &device,                    // Returns the Direct3D device created.
    &m_d3dFeatureLevel,         // Returns feature level of device created.
    &context                    // Returns the device immediate context.
    );

if (SUCCEEDED(hr))
{
    D3D11_FEATURE_DATA_D3D11_OPTIONS1 featureData;
    DX::ThrowIfFailed(
        device->CheckFeatureSupport(D3D11_FEATURE_D3D11_OPTIONS1, &featureData, sizeof(featureData))
        );

    m_tiledResourcesTier = featureData.TiledResourcesTier;
}
```



## <a name="extended-support-for-warp-devices"></a>Suporte estendido para dispositivos WARP

O Direct3D 11,2 estende o suporte para dispositivos [Warp](overviews-direct3d-11-devices-create-warp.md) , que você cria passando o [**tipo de driver do D3D \_ \_ \_ Warp**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_driver_type) no parâmetro *driverType* de [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice). O processador de software WARP no Direct3D 11,2 adiciona suporte completo para o [nível de recurso](overviews-direct3d-11-devices-downlevel-intro.md) do Direct3D 11 \_ 1, incluindo os [recursos de lado](#tiled-resources), [**IDXGIDevice3:: Trim**](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-idxgidevice3-trim), superfícies BCN compartilhadas, minblend e o padrão de mapa. O suporte [duplo](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_doubles) em sombreadores HLSL também foi habilitado junto com o suporte para a MSAA de 16x.

## <a name="annotate-graphics-commands"></a>Anotar comandos gráficos

O Direct3D 11,2 permite anotar comandos gráficos com estas APIs:

-   [**ID3D11DeviceContext2::IsAnnotationEnabled**](/windows/desktop/api/d3d11_2/nf-d3d11_2-id3d11devicecontext2-isannotationenabled)
-   [**ID3D11DeviceContext2::BeginEventInt**](/windows/desktop/api/d3d11_2/nf-d3d11_2-id3d11devicecontext2-begineventint)
-   [**ID3D11DeviceContext2::SetMarkerInt**](/windows/desktop/api/d3d11_2/nf-d3d11_2-id3d11devicecontext2-setmarkerint)
-   [**ID3D11DeviceContext2:: endEvent**](/windows/desktop/api/d3d11_2/nf-d3d11_2-id3d11devicecontext2-endevent)

## <a name="hlsl-shader-linking"></a>Vinculação de sombreador HLSL

Windows 8.1 adiciona compilação separada e vinculação de sombreadores HLSL, que permite aos programadores de gráficos criar funções HLSL pré-compiladas, empacotá-las em bibliotecas e vinculá-las a sombreadores completos em tempo de execução. Isso é essencialmente um equivalente à compilação, às bibliotecas e à vinculação separadas do C/C++, e permite aos programadores compor código HLSL pré-compilado quando mais informações estiverem disponíveis para finalizar a computação. Para obter mais informações sobre como usar a vinculação de sombreador, consulte [usando a vinculação de sombreador](/windows/desktop/direct3dhlsl/using-shader-linking).

Conclua estas etapas para criar um sombreador final usando vinculação dinâmica em tempo de execução.

**Para criar e usar a vinculação de sombreador**

1.  Crie um objeto vinculador [**ID3D11Linker**](/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11linker) , que representa um contexto de vinculação. Um contexto único não pode ser usado para produzir vários sombreadores; um contexto de vinculação é usado para produzir um único sombreador e, em seguida, o contexto de vinculação é Descartado.
2.  Use [**D3DLoadModule**](/windows/desktop/api/d3dcompiler/nf-d3dcompiler-d3dloadmodule) para carregar e definir bibliotecas de seus blobs de biblioteca.
3.  Use [**D3DLoadModule**](/windows/desktop/api/d3dcompiler/nf-d3dcompiler-d3dloadmodule) para carregar e definir um blob de sombreador de entrada ou criar um [sombreador FLG](#function-linking-graph-flg).
4.  Use [**ID3D11Module**](/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11module)::[**CreateInstance**](/windows/desktop/api/D3D11Shader/nf-d3d11shader-id3d11module-createinstance) para criar objetos [**ID3D11ModuleInstance**](/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11moduleinstance) e, em seguida, chame funções nesses objetos para reassociar recursos a seus slots finais.
5.  Adicione as bibliotecas ao vinculador e, em seguida, chame [**ID3D11Linker**](/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11linker)::[**link**](/windows/desktop/api/D3D11Shader/nf-d3d11shader-id3d11linker-link) para produzir o código de byte do sombreador final que pode ser carregado e usado no tempo de execução, assim como um sombreador totalmente pré-compilado e vinculado.

### <a name="function-linking-graph-flg"></a>Grafo de vinculação de função (FLG)

Windows 8.1 também adiciona o grafo de vinculação de função (FLG). Você pode usar FLG para construir sombreadores que consistem em uma sequência de invocações de função pré-compiladas que passam valores entre si. Ao usar o FLG, não há necessidade de escrever HLSL e invocar o compilador HLSL. Em vez disso, a estrutura do sombreador é especificada programaticamente usando chamadas à API do C++. Os nós FLG representam assinaturas de entrada e saída e invocações de funções de biblioteca pré-compiladas. A ordem de registro dos nós de chamada de função define a sequência de invocações. O nó de assinatura de entrada deve ser especificado primeiro, enquanto o nó de assinatura de saída deve ser especificado por último. As bordas FLG definem como os valores são passados de um nó para outro. Os tipos de dados dos valores passados devem ser os mesmos; Não há nenhuma conversão implícita de tipo. As regras Shape e swizzling seguem o comportamento de HLSL e os valores só podem ser passados para frente nessa sequência. Para obter informações sobre a API do FLG, consulte [**ID3D11FunctionLinkingGraph**](/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11functionlinkinggraph).

## <a name="inbox-hlsl-compiler"></a>Compilador HLSL de caixa de entrada

O compilador HLSL agora é a caixa de entrada no Windows 8.1 e posterior. Agora, a maioria das APIs para a programação de sombreador pode ser usada em aplicativos da Windows Store criados para Windows 8.1 e posterior. Muitas APIs para programação de sombreador não puderam ser usadas em aplicativos da Windows Store criados para o Windows 8; as páginas de referência para essas APIs foram marcadas com uma observação. Mas algumas APIs de sombreador (por exemplo, [**D3DCompileFromFile**](/windows/desktop/direct3dhlsl/d3dcompilefromfile)) ainda podem ser usadas apenas para desenvolver aplicativos da Windows Store, e não em aplicativos que você envia para a Windows Store; as páginas de referência para essas APIs ainda são marcadas com uma observação.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[O que há de novo no Direct3D 11](dx-graphics-overviews-introduction.md)
</dt> </dl>

 

 