---
title: Visão geral das camadas
description: Descreve os conceitos básicos das camadas direct2D.
ms.assetid: 22d161fb-8470-49cc-a523-309f90643ea9
keywords:
- Direct2D, camadas
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: ac68ba25d1e8f35c5a41daec4d7a5295235a5d98
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549181"
---
# <a name="layers-overview"></a>Visão geral das camadas

Esta visão geral descreve os conceitos básicos do uso de camadas direct2D. Ele contém as seguintes seções:

-   [O que são camadas?](#what-are-layers)
-   [Camadas no Windows 8 e posterior](#layers-in-windows-8-and-later)
    -   [ID2D1DeviceContext e PushLayer](#id2d1devicecontext-and-pushlayer)
    -   [D2D1 \_ LAYER \_ PARAMETERS1 e D2D1 \_ LAYER \_ OPTIONS1](/windows)
    -   [Modos do Blend](#blend-modes)
    -   [Interoperação](#interoperation)
-   [Criando camadas](#creating-layers)
-   [Limites de conteúdo](#content-bounds)
-   [Máscaras geométricas](#geometric-masks)
-   [Máscaras de opacidade](#opacity-masks)
-   [Alternativas a camadas](#alternatives-to-layers)
-   [Recorte de uma forma arbitrária](#clipping-an-arbitrary-shape)
    -   [Clipes alinhados ao eixo](#axis-aligned-clips)
-   [Tópicos relacionados](#related-topics)

## <a name="what-are-layers"></a>O que são camadas?

Camadas, representadas por [**objetos ID2D1Layer,**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) permitem que um aplicativo manipule um grupo de operações de desenho. Você usa uma camada "esvasada" para um destino de renderização. As operações de desenho subsequentes pelo destino de renderização são direcionadas para a camada. Depois de terminar com a camada, você "pop" a camada do destino de renderização, que compõe o conteúdo da camada de volta para o destino de renderização.

Como pincéis, as camadas são recursos dependentes do dispositivo criados por destinos de renderização. As camadas podem ser usadas em qualquer destino de renderização no mesmo domínio de recurso que contém o destino de renderização que a criou. No entanto, um recurso de camada só pode ser usado por um destino de renderização por vez. Para obter mais informações sobre recursos, consulte a [visão geral de recursos](resources-and-resource-domains.md).

Embora as camadas ofereçam uma poderosa técnica de renderização para produzir efeitos interessantes, o número excessivo de camadas em um aplicativo pode afetar negativamente o desempenho, devido aos vários custos associados ao gerenciamento de camadas e recursos de camada. Por exemplo, há o custo de preencher ou limpar a camada e, em seguida, mesclar novamente, especialmente em hardware de extremidade superior. Em seguida, há o custo de gerenciar os recursos de camada. Se você os realocar com frequência, as interrupções resultantes na GPU serão o problema mais significativo. Ao projetar seu aplicativo, tente maximizar a reutilização de recursos de camada.

## <a name="layers-in-windows-8-and-later"></a>Camadas no Windows 8 e posteriores

O Windows 8 introduziu novas APIs relacionadas à camada que simplificam, melhoram o desempenho e adicionam recursos a camadas.

### <a name="id2d1devicecontext-and-pushlayer"></a>ID2D1DeviceContext e PushLayer

A interface [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) é derivada da interface [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) e é a chave para exibir o conteúdo de Direct2D no Windows 8, para obter mais informações sobre essa interface, confira [dispositivos e contextos de dispositivo](devices-and-device-contexts.md). Com a interface de contexto do dispositivo, você pode ignorar a chamada do método [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) e, em seguida, passar NULL para o método [**ID2D1DeviceContext::P ushlayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer)) . O Direct2D gerencia automaticamente o recurso de camada e pode compartilhar recursos entre camadas e grafos de efeitos.

### <a name="d2d1_layer_parameters1-and-d2d1_layer_options1"></a>Camada \_ d2d1 \_ PARAMETERS1 e d2d1 \_ \_ OPTIONS1

A [**estrutura D2D1 \_ LAYER \_ PARAMETERS1**](/windows/desktop/api/d2d1_1/ns-d2d1_1-d2d1_layer_parameters1) é a mesma que [**D2D1 \_ LAYER \_ PARAMETERS**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters), exceto que o membro final da estrutura agora é uma enumeração [**D2D1 \_ LAYER \_ OPTIONS1.**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_layer_options1)

[**D2D1 \_ LAYER \_ OPTIONS1**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_layer_options1) não tem nenhuma opção ClearType e tem duas opções diferentes que você pode usar para melhorar o desempenho:

-   [**D2D1 \_ LAYER \_ OPTIONS1 \_ INITIALIZE \_ FROM \_ BACKGROUND:**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_layer_options1)o Direct2D renderiza primitivos para a camada sem desmatá-la com preto transparente. Esse não é o padrão, mas, na maioria dos casos, resulta em um melhor desempenho.

-   [**D2D1 \_ LAYER \_ OPTIONS1 \_ IGNORE \_ ALPHA**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_layer_options1): se a superfície subjacente estiver definida como [**D2D1 \_ ALPHA MODE \_ \_ IGNORE**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode), essa opção permitirá que o Direct2D evite modificar o canal alfa da camada. Não use isso em outros casos.

### <a name="blend-modes"></a>Modos do Blend

Começando no Windows 8, o contexto do dispositivo tem um modo de combinação primitivo que determina como cada primitivo é mesclado com [**a**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_primitive_blend) superfície de destino. Esse modo também se aplica a camadas quando você chama o [**método PushLayer.**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer))

Por exemplo, se você estiver usando uma camada para cortar primitivos com transparência, de conjunto de transparência, o modo [**\_ COPY BLEND \_ \_ COPY PRIMITIVO D2D1**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_primitive_blend) no contexto do dispositivo para resultados adequados. O modo de cópia faz com que o contexto linear do dispositivo interpole todos os quatro canais de cores, incluindo o canal alfa, de cada pixel com o conteúdo da superfície de destino de acordo com a máscara geométrica da camada.

### <a name="interoperation"></a>Interoperação

A partir do Windows 8, o Direct2D dá suporte à interoperação com Direct3D e GDI enquanto uma camada ou clipe é pressionado. Chame [**ID2D1GdiInteropRenderTarget::GetDC**](/windows/win32/api/d2d1/nf-d2d1-id2d1gdiinteroprendertarget-getdc) enquanto uma camada é pressionada para interoperar com gDI. Você chama [**ID2D1DeviceContext::Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) e, em seguida, renderiza para a superfície subjacente para interoperar com o Direct3D. É sua responsabilidade renderizar dentro da camada ou do clipe com Direct3D ou GDI. Se você tentar renderizar fora da camada ou cortar, os resultados serão indefinidos.

## <a name="creating-layers"></a>Criando camadas

Trabalhar com camadas requer familiaridade com os métodos [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)), [**PushLayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer))e [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) , e a estrutura [**de \_ \_ parâmetros de camada d2d1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) , que contém um conjunto de dados paramétricos que definem como a camada pode ser usada. A lista a seguir descreve os métodos e a estrutura.

-   Chame o método [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) para criar um recurso de camada.
    > [!Note]  
    > A partir do Windows 8, você pode ignorar a chamada do método [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) e, em seguida, passar NULL para o método [**PushLayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer)) na interface [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) . Isso é mais simples e permite que o Direct2D gerencie automaticamente o recurso de camada e compartilhe recursos entre camadas e grafos de efeito.

     

-   Depois que o destino de renderização começou a desenhar (depois de seu método [**BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) ter sido chamado), você pode usar o método [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) . O método **PushLayer** adiciona a camada especificada ao destino de renderização, para que o destino receba todas as operações de desenho subsequentes até que [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) seja chamado. Esse método usa um objeto [**ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) retornado chamando [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) e um *layerparameters* na estrutura de [**\_ \_ parâmetros da camada d2d1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) . A tabela a seguir descreve os campos da estrutura. 

    | Campo                 | Descrição|
    |-----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | **contentBounds**     | Os limites de conteúdo da camada. O conteúdo fora desses limites é garantido para não renderizar. O padrão desse parâmetro é [**InfiniteRect**](/windows/desktop/api/d2d1Helper/nf-d2d1helper-infiniterect). Quando o valor padrão é usado, os limites de conteúdo são efetivamente utilizados para serem os limites do destino de renderização. |
    | **geometricMask**     | Adicional A área, definida por um [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry), para o qual a camada deve ser recortada. Defina como **NULL** se a camada não deve ser recortada em uma geometria. |
    | **maskAntialiasMode** | Um valor que especifica o modo de aninhamento para a máscara geométrica especificada pelo campo **geometricMask.** |
    | **maskTransform**     | Um valor que especifica a transformação aplicada à máscara geométrica ao compor a camada. Isso é relativo à transformação do mundo.  |
    | **Opacidade**           | O valor de opacidade da camada. A opacidade de cada recurso na camada é multiplicada por esse valor ao compor para o destino.  |
    | **opacityBrush**      | (Opcional) Um pincel usado para modificar a opacidade da camada. O pincel é mapeado para a camada e o canal alfa de cada pixel de pincel mapeado é multiplicado em relação ao pixel da camada correspondente. Definido como **NULL** se a camada não deve ter uma máscara de opacidade.   |
    | **layerOptions**      | Um valor que especifica se a camada pretende renderizar texto com a antialização ClearType. Esse parâmetro assume como padrão desligado. A ative-o permite que ClearType funcione corretamente, mas resulta em uma velocidade de renderização ligeiramente mais lenta.    |

    

     

    > [!Note]  
    > Começando no Windows 8, você não pode renderizar com ClearType em uma camada, portanto, o parâmetro **layerOptions** sempre deve ser definido como [**D2D1 \_ LAYER OPTIONS \_ \_ NONE**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_layer_options)

     

    Para sua conveniência, o Direct2D fornece o [**método D2D1::LayerParameters**](/windows/desktop/api/d2d1helper/nf-d2d1helper-layerparameters) para ajudá-lo a [**criar estruturas D2D1 \_ LAYER \_ PARAMETERS.**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters)

-   Para compor o conteúdo da camada no destino de renderização, chame o [**método PopLayer.**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) Você deve chamar o **método PopLayer** antes de chamar o [**método EndDraw.**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw)

O exemplo a seguir mostra como usar [**CreateLayer,**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) [**PushLayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer))e [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer). Todos os campos na estrutura de [**\_ \_ parâmetros de camada d2d1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) são definidos como seus padrões, exceto **opacityBrush**, que é definido como um [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush).


```C++
// Create a layer.
ID2D1Layer *pLayer = NULL;
hr = pRT->CreateLayer(NULL, &pLayer);

if (SUCCEEDED(hr))
{
    pRT->SetTransform(D2D1::Matrix3x2F::Translation(300, 250));

    // Push the layer with the content bounds.
    pRT->PushLayer(
        D2D1::LayerParameters(
            D2D1::InfiniteRect(),
            NULL,
            D2D1_ANTIALIAS_MODE_PER_PRIMITIVE,
            D2D1::IdentityMatrix(),
            1.0,
            m_pRadialGradientBrush,
            D2D1_LAYER_OPTIONS_NONE),
        pLayer
        );

    pRT->DrawBitmap(m_pBambooBitmap, D2D1::RectF(0, 0, 190, 127));

    pRT->FillRectangle(
        D2D1::RectF(25.f, 25.f, 50.f, 50.f), 
        m_pSolidColorBrush
        );
    pRT->FillRectangle(
        D2D1::RectF(50.f, 50.f, 75.f, 75.f),
        m_pSolidColorBrush
        ); 
    pRT->FillRectangle(
        D2D1::RectF(75.f, 75.f, 100.f, 100.f),
        m_pSolidColorBrush
        );    
 
    pRT->PopLayer();
}
SafeRelease(&pLayer);
```



O código foi omitido neste exemplo.

Observe que quando você chama [**PushLayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer)) e [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer), certifique-se de que cada **PushLayer** tenha uma chamada **PopLayer** correspondente. Se houver mais chamadas **PopLayer** que chamadas **PushLayer** , o destino de renderização será colocado em um estado de erro. Se a [**liberação**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) for chamada antes que todas as camadas pendentes sejam retiradas, o destino de renderização será colocado em um estado de erro e retornará um erro. Para limpar o estado de erro, use [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw).

## <a name="content-bounds"></a>Limites de conteúdo

O **contentBounds** define o limite de o que deve ser desenhado para a camada. Somente as coisas dentro dos limites de conteúdo são compostas de volta ao destino de renderização.

O exemplo a seguir mostra como especificar **contentBounds** para que a imagem original seja recortada para o conteúdo associado ao canto superior esquerdo em (10, 108) e no canto inferior direito em (121, 177). A ilustração a seguir mostra a imagem original e o resultado de recortar a imagem para os limites de conteúdo.

![ilustração de limites de conteúdo em uma imagem original e a imagem recortada resultante](images/layers-contentbounds.png)


```C++
HRESULT DemoApp::RenderWithLayerWithContentBounds(ID2D1RenderTarget *pRT)
{
    
    HRESULT hr = S_OK;

    // Create a layer.
    ID2D1Layer *pLayer = NULL;
    hr = pRT->CreateLayer(NULL, &pLayer);

    if (SUCCEEDED(hr))
    {
        pRT->SetTransform(D2D1::Matrix3x2F::Translation(300, 0));

        // Push the layer with the content bounds.
        pRT->PushLayer(
            D2D1::LayerParameters(D2D1::RectF(10, 108, 121, 177)),
            pLayer
            );

        pRT->DrawBitmap(m_pWaterBitmap, D2D1::RectF(0, 0, 128, 192));
        pRT->PopLayer();
    }

    SafeRelease(&pLayer);

    return hr;
    
}
```



O código foi omitido neste exemplo.

> [!Note]
>
> A imagem recortada resultante será ainda afetada se você especificar um **geometricMask**. Consulte a seção [máscaras geométricas](#geometric-masks) para obter mais informações.

 

## <a name="geometric-masks"></a>Máscaras geométricas

Uma máscara geométrica é um clipe ou um recorte, definido por um objeto [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) , que mascara uma camada quando ela é desenhada por um destino de renderização. Você pode usar o campo **geometricMask** da estrutura [**de \_ \_ parâmetros de camada d2d1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) para mascarar os resultados em uma geometria. Por exemplo, se você quiser exibir uma imagem mascarada por uma letra de bloco "A", você pode primeiro criar uma geometria representando a letra "A" e usar essa geometria como uma máscara geométrica para uma camada. Em seguida, depois de enviar a camada por push, você pode desenhar a imagem. A recortar a camada resulta na imagem sendo recortada para a forma "A" da letra do bloco.

O exemplo a seguir mostra como criar um [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) que contém uma forma de uma mountain e, em seguida, passar a geometria do caminho para o [**PushLayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer)). Em seguida, ele desenha um bitmap e quadrados. Se houver apenas um bitmap na camada a ser renderização, use [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) com um pincel de bitmap fixado para eficiência. A ilustração a seguir mostra a saída do exemplo.

![ilustração de uma imagem de uma folha e a imagem resultante depois que uma máscara geométrica de uma mountain é aplicada](images/layers-bitmapmask.png)

O primeiro exemplo define a geometria a ser usada como uma máscara.


```C++
hr = m_pD2DFactory->CreatePathGeometry(&m_pPathGeometry);
    
if(SUCCEEDED(hr))
{
    ID2D1GeometrySink *pSink = NULL;
    // Write to the path geometry using the geometry sink.
    hr = m_pPathGeometry->Open(&pSink);

    if (SUCCEEDED(hr))
    {
        pSink->SetFillMode(D2D1_FILL_MODE_WINDING);
        pSink->BeginFigure(
            D2D1::Point2F(0, 90),
            D2D1_FIGURE_BEGIN_FILLED
            );

        D2D1_POINT_2F points[7] = {
           D2D1::Point2F(35, 30),
           D2D1::Point2F(50, 50),
           D2D1::Point2F(70, 45),
           D2D1::Point2F(105, 90),
           D2D1::Point2F(130, 90),
           D2D1::Point2F(150, 60),
           D2D1::Point2F(170, 90)
           };

        pSink->AddLines(points, 7);
        pSink->EndFigure(D2D1_FIGURE_END_CLOSED);
        hr = pSink->Close();
    }
    SafeRelease(&pSink);
       }
```



O exemplo a seguir usa a geometria como uma máscara para a camada.


```C++
HRESULT DemoApp::RenderWithLayerWithGeometricMask(ID2D1RenderTarget *pRT)
{
    
    HRESULT hr;

    // Create a layer.
    ID2D1Layer *pLayer = NULL;
    hr = pRT->CreateLayer(NULL, &pLayer);

    if (SUCCEEDED(hr))
    {
        pRT->SetTransform(D2D1::Matrix3x2F::Translation(300, 450));

        pRT->PushLayer(
            D2D1::LayerParameters(D2D1::InfiniteRect(), m_pPathGeometry),
            pLayer
            );

        pRT->DrawBitmap(m_pLeafBitmap, D2D1::RectF(0, 0, 198, 132));

        pRT->FillRectangle(
            D2D1::RectF(50.f, 50.f, 75.f, 75.f), 
            m_pSolidColorBrush
            ); 
        pRT->FillRectangle(
            D2D1::RectF(75.f, 75.f, 100.f, 100.f),
            m_pSolidColorBrush
            );        

        pRT->PopLayer();
    }

    SafeRelease(&pLayer);

    return hr;
    
}
```



O código foi omitido neste exemplo.

> [!Note]
>
> Em geral, se você especificar **um geometricMask**, poderá usar o valor padrão, [**InfiniteRect**](/windows/desktop/api/d2d1Helper/nf-d2d1helper-infiniterect), para **contentBounds.**
>
> Se **contentBounds** for NULL e **geometricMask** não for NULL, os limites de conteúdo serão efetivamente os limites da máscara geométrica depois que a transformação de máscara for aplicada.
>
> Se **contentBounds** for não NULL e **geometricMask** não for NULL, a máscara geométrica transformada será efetivamente recortada em relação aos limites de conteúdo e os limites de conteúdo serão presumidos como infinitos.

 

## <a name="opacity-masks"></a>Máscaras de opacidade

Uma máscara de opacidade é uma máscara, descrita por um pincel ou bitmap, que é aplicada a outro objeto para tornar esse objeto parcial ou completamente transparente. Ele permite que o uso do canal alfa de um pincel seja usado como uma máscara de conteúdo. Por exemplo, você pode definir um pincel de gradiente radial que varia de opaco a transparente para criar um efeito de vinheta.

O exemplo a seguir usa um [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) (*m \_ pRadialGradientBrush*) como uma máscara de opacidade. Em seguida, ele desenha um bitmap e quadrados. Se houver apenas um bitmap na camada a ser renderização, use [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) com um pincel de bitmap fixado para eficiência. A ilustração a seguir mostra a saída deste exemplo.

![ilustração de uma imagem de árvores e a imagem resultante depois que uma máscara de opacidade é aplicada](images/layers-opacitymask.png)


```C++
HRESULT DemoApp::RenderWithLayerWithOpacityMask(ID2D1RenderTarget *pRT)
{   

    HRESULT hr = S_OK;

    // Create a layer.
    ID2D1Layer *pLayer = NULL;
    hr = pRT->CreateLayer(NULL, &pLayer);

    if (SUCCEEDED(hr))
    {
        pRT->SetTransform(D2D1::Matrix3x2F::Translation(300, 250));

        // Push the layer with the content bounds.
        pRT->PushLayer(
            D2D1::LayerParameters(
                D2D1::InfiniteRect(),
                NULL,
                D2D1_ANTIALIAS_MODE_PER_PRIMITIVE,
                D2D1::IdentityMatrix(),
                1.0,
                m_pRadialGradientBrush,
                D2D1_LAYER_OPTIONS_NONE),
            pLayer
            );

        pRT->DrawBitmap(m_pBambooBitmap, D2D1::RectF(0, 0, 190, 127));

        pRT->FillRectangle(
            D2D1::RectF(25.f, 25.f, 50.f, 50.f), 
            m_pSolidColorBrush
            );
        pRT->FillRectangle(
            D2D1::RectF(50.f, 50.f, 75.f, 75.f),
            m_pSolidColorBrush
            ); 
        pRT->FillRectangle(
            D2D1::RectF(75.f, 75.f, 100.f, 100.f),
            m_pSolidColorBrush
            );    
 
        pRT->PopLayer();
    }
    SafeRelease(&pLayer);
   
    return hr;
    
}
```



O código foi omitido neste exemplo.

> [!Note]  
> Este exemplo usa uma camada para aplicar uma máscara de opacidade a um único objeto para manter o exemplo o mais simples possível. Ao aplicar uma máscara de opacidade a um único objeto, seu mais eficiente é usar os métodos [**FillOpacityMask**](id2d1rendertarget-fillopacitymask.md) ou [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) , em vez de uma camada.

 

Para obter instruções sobre como aplicar uma máscara de opacidade sem usar uma camada, consulte a [visão geral das máscaras de opacidade](opacity-masks-overview.md).

## <a name="alternatives-to-layers"></a>Alternativas para camadas

Como mencionado anteriormente, o número excessivo de camadas pode afetar negativamente o desempenho do seu aplicativo. Para melhorar o desempenho, evite usar camadas sempre que possível; em vez disso, use suas alternativas. O exemplo de código a seguir mostra como usar [**PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f_d2d1_antialias_mode)) e [**PopAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-popaxisalignedclip) para recortar uma região, como uma alternativa ao uso de uma camada com limites de conteúdo.


```C++
pRT->PushAxisAlignedClip(
    D2D1::RectF(20, 20, 100, 100),
    D2D1_ANTIALIAS_MODE_PER_PRIMITIVE
    );

pRT->FillRectangle(D2D1::RectF(0, 0, 200, 133), m_pOriginalBitmapBrush);
pRT->PopAxisAlignedClip();
```



Da mesma forma, use [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) com um pincel de bitmap clamped como uma alternativa ao uso de uma camada com uma máscara de opacidade quando houver apenas um conteúdo na camada a ser renderizado, conforme mostrado no exemplo a seguir.


```C++
        m_pRenderTarget->FillGeometry(
            m_pRectGeo, 
            m_pLinearFadeFlowersBitmapBrush, 
            m_pLinearGradientBrush
            );
```



Como alternativa ao uso de uma camada com uma máscara geométrica, considere usar uma máscara de bitmap para recortar uma região, conforme mostrado no exemplo a seguir.


```C++
// D2D1_ANTIALIAS_MODE_ALIASED must be set for FillOpacityMask
// to function properly.
m_pRenderTarget->SetAntialiasMode(D2D1_ANTIALIAS_MODE_ALIASED);

m_pRenderTarget->FillOpacityMask(
    m_pBitmapMask,
    m_pOriginalBitmapBrush,
    D2D1_OPACITY_MASK_CONTENT_GRAPHICS,
    &rcBrushRect,
    NULL
    );

m_pRenderTarget->SetAntialiasMode(D2D1_ANTIALIAS_MODE_PER_PRIMITIVE);

```



Por fim, se você quiser aplicar a opacidade a um único primitivo, deverá multiplicar a opacidade na cor do pincel e, em seguida, renderizar o primitivo. Você não precisa de uma camada ou bitmap de máscara de opacidade.


```C++
float opacity = 0.9f;

ID2D1SolidColorBrush *pBrush = NULL;
hr = pCompatibleRenderTarget->CreateSolidColorBrush(
    D2D1::ColorF(D2D1::ColorF(0.93f, 0.94f, 0.96f, 1.0f * opacity)),
    &pBrush
    );

m_pRenderTarget->FillRectangle(
    D2D1::RectF(50.0f, 50.0f, 75.0f, 75.0f), 
    pBrush
    ); 
```



## <a name="clipping-an-arbitrary-shape"></a>Recortando uma forma arbitrária

A figura aqui mostra o resultado da aplicação de um clipe a uma imagem.

![uma imagem que mostra um exemplo de uma imagem antes e depois de um clipe.](images/clip.png)

Você pode obter esse resultado usando camadas com uma máscara de geometria ou o método [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) com um pincel de opacidade.

Aqui está um exemplo que usa uma camada:


```C++
// Call PushLayer() and pass in the clipping geometry.
m_d2dContext->PushLayer(
    D2D1::LayerParameters(
        boundsRect,
        geometricMask));
```



Aqui está um exemplo que usa o método [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) :


```C++
// Create an opacity bitmap and render content.
m_d2dContext->CreateBitmap(size, nullptr, 0,
    D2D1::BitmapProperties(
        D2D1_BITMAP_OPTIONS_TARGET,
        D2D1::PixelFormat(
            DXGI_FORMAT_A8_UNORM,
            D2D1_ALPHA_MODE_PREMULTIPLIED),
        dpiX, dpiY),
    &opacityBitmap);

m_d2dContext->SetTarget(opacityBitmap.Get());
m_d2dContext->BeginDraw();
…
m_d2dContext->EndDraw();

// Create an opacity brush from the opacity bitmap.
m_d2dContext->CreateBitmapBrush(opacityBitmap.Get(),
    D2D1::BitmapBrushProperties(),
    D2D1::BrushProperties(),
    &bitmapBrush);

// Call the FillGeometry method and pass in the clip geometry and the opacity brush
m_d2dContext->FillGeometry( 
    clipGeometry.Get(),
    brush.Get(),
    opacityBrush.Get()); 
```



Neste exemplo de código, ao chamar o método PushLayer, você não passa uma camada de aplicativo criado. O Direct2D cria uma camada para você. O Direct2D é capaz de gerenciar a alocação e a destruição desse recurso sem qualquer envolvimento do aplicativo. Isso permite que o Direct2D reutilizar camadas internamente e aplicar otimizações de gerenciamento de recursos.

> [!Note]  
> Neste Windows 8 muitas otimizações foram feitas para o uso de camadas e recomendamos que você tente usar APIs de camada em vez de [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) sempre que possível.

 

### <a name="axis-aligned-clips"></a>Clipes alinhados ao eixo

Se a região a ser recortada estiver alinhada ao eixo da superfície de desenho, em vez de arbitrária. Esse caso é adequado para usar um retângulo de clipe em vez de uma camada. O ganho de desempenho é mais para geometria com alias do que geometria suavizada. Para obter mais informações sobre clipes alinhados ao eixo, consulte o [**tópico PushAxisAlignedClip.**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode))

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência do Direct2D](reference.md)
</dt> </dl>

 

 