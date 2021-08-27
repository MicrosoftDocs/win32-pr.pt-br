---
title: Visão geral de máscaras da opacidade
description: 'Este tópico descreve como usar bitmaps e pincéis para definir máscaras de opacidade. Ele contém as seguintes seções:'
ms.assetid: 869821b0-6ebe-46c2-aab6-93177d8a92c5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 513365474ed6b1f6f42d34f9b876226e00ba6e85
ms.sourcegitcommit: 4e94fc75fad7b2a0f3c92a26f97e89924e59b7a9
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/24/2021
ms.locfileid: "122786372"
---
# <a name="opacity-masks-overview"></a>Visão geral de máscaras da opacidade

Este tópico descreve como usar bitmaps e pincéis para definir máscaras de opacidade. Ele contém as seguintes seções:

-   [Pré-requisitos](#prerequisites)
-   [O que é uma máscara de opacidade?](#what-is-an-opacity-mask)
-   [Usar um bitmap como uma máscara de opacidade com o método FillOpacityMask](#use-a-bitmap-as-an-opacity-mask-with-the-fillopacitymask-method)
-   [Usar um pincel como uma máscara de opacidade com o método FillGeometry](#use-a-brush-as-an-opacity-mask-with-the-fillgeometry-method)
    -   [Usar um pincel de gradiente linear como uma máscara de opacidade](#use-an-linear-gradient-brush-as-an-opacity-mask)
    -   [Usar um pincel de gradiente radial como uma máscara de opacidade](#use-a-radial-gradient-brush-as-an-opacity-mask)
-   [Aplicar uma máscara de opacidade a uma camada](#apply-an-opacity-mask-to-a-layer)
-   [Tópicos relacionados](#related-topics)

## <a name="prerequisites"></a>Pré-requisitos

Esta visão geral pressuporá que você está familiarizado com Direct2D operações básicas de desenho, conforme descrito no passo [a](direct2d-quickstart.md) passo Criando um aplicativo de Direct2D simples. Você também deve estar familiarizado com os diferentes tipos de pincéis, conforme descrito na Visão geral [de pincéis](direct2d-brushes-overview.md).

## <a name="what-is-an-opacity-mask"></a>O que é uma máscara de opacidade?

Uma máscara de opacidade é uma máscara, descrita por um pincel ou bitmap, que é aplicada a outro objeto para tornar esse objeto parcial ou completamente transparente. Uma máscara de opacidade usa informações de canal alfa para especificar como os pixels de origem do objeto são mesclados no destino final. As partes transparentes da máscara indicam as áreas em que a imagem subjacente está oculta, enquanto as partes opacas da máscara indicam onde o objeto mascarado está visível.

Há várias maneiras de aplicar uma máscara de opacidade:

-   Use o [**método ID2D1RenderTarget::FillOpacityMask.**](id2d1rendertarget-fillopacitymask.md) O **método FillOpacityMask** pinta uma região retangular de um destino de renderização e aplica uma máscara de opacidade, definida por um bitmap. Use esse método quando a máscara de opacidade for um bitmap e você quiser preencher uma região retangular.
-   Use o [**método ID2D1RenderTarget::FillGeometry.**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) O **método FillGeometry** pinta o interior da geometria com o [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush)especificado e, em seguida, aplica uma máscara de opacidade, definida por um pincel. Use esse método quando quiser aplicar uma máscara de opacidade a uma geometria ou quiser usar um pincel como uma máscara de opacidade.
-   Use um [**ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) para aplicar uma máscara de opacidade. Use essa abordagem quando quiser aplicar uma máscara de opacidade a um grupo de conteúdo de desenho, não apenas a uma única forma ou imagem. Para obter detalhes, consulte Visão [geral das camadas.](direct2d-layers-overview.md)

## <a name="use-a-bitmap-as-an-opacity-mask-with-the-fillopacitymask-method"></a>Usar um bitmap como uma máscara de opacidade com o método FillOpacityMask

O [**método FillOpacityMask**](id2d1rendertarget-fillopacitymask.md) pinta uma região retangular de um destino de renderização e aplica uma máscara de opacidade, definida por [**um ID2D1Bitmap.**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) Use esse método quando você tiver um bitmap que deseja usar como uma máscara de opacidade para uma região retangular.

O diagrama a seguir mostra um efeito da aplicação da máscara de opacidade [**(um ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) com uma imagem de uma flor) a [**uma ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) com uma imagem de uma planta de flores. A imagem resultante é um bitmap de uma planta recortada na forma de flor.

![diagrama de um bitmap de flor usado como uma máscara de opacidade em uma imagem de uma planta de flores](images/brushes-ovw-bitmapopacity.png)

Os exemplos de código a seguir mostram como isso é feito.

O primeiro exemplo carrega o bitmap a seguir, *m \_ pBitmapMask,* para uso como uma máscara de bitmap. A ilustração a seguir mostra a saída produzida. Observe que, embora a parte opaca do bitmap pareça preta, as informações de cor no bitmap não têm efeito sobre a máscara de opacidade; somente as informações de opacidade de cada pixel no bitmap são usadas. Os pixels totalmente opacos neste bitmap foram coloridos em preto apenas para fins ilustrativos.

![ilustração da máscara de bitmap de flor](images/bitmapmask.png)

Neste exemplo, o [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) é carregado por um método auxiliar, LoadResourceBitmap, definido em outro lugar no exemplo.


```C++
            if (SUCCEEDED(hr))
            {
                hr = LoadResourceBitmap(
                    m_pRenderTarget,
                    m_pWICFactory,
                    L"BitmapMask",
                    L"Image",
                    &m_pBitmapMask
                    );
            }
```



O exemplo a seguir define o *pincel, m \_ pFernBitmapBrush,* ao qual a máscara de opacidade é aplicada. Este exemplo usa [**um ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) que contém uma imagem de um cão, mas você pode usar um [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush), [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush)ou [**ID2D1RadialGradientBrush.**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) A ilustração a seguir mostra a saída produzida.

![ilustração do bitmap usado pelo pincel de bitmap](images/fern.png)


```C++
            if (SUCCEEDED(hr))
            {
                D2D1_BITMAP_BRUSH_PROPERTIES propertiesXClampYClamp = 
                    D2D1::BitmapBrushProperties(
                    D2D1_EXTEND_MODE_CLAMP,
                    D2D1_EXTEND_MODE_CLAMP,
                    D2D1_BITMAP_INTERPOLATION_MODE_NEAREST_NEIGHBOR
                    );
                hr = m_pRenderTarget->CreateBitmapBrush(
                    m_pFernBitmap,
                    propertiesXClampYClamp,
                    &m_pFernBitmapBrush
                    );


            }
```





Agora que a máscara de opacidade e o pincel estão definidos, você pode usar o [**método FillOpacityMask**](id2d1rendertarget-fillopacitymask.md) no método de renderização do aplicativo. Ao chamar o método **FillOpacityMask,** você deve especificar o tipo de máscara de opacidade que está usando: GRÁFICOS DE CONTEÚDO DE **MÁSCARA DE \_ OPACIDADE \_ \_ \_ D2D1**, **D2D1 \_ OPACITY \_ MASK CONTENT TEXT \_ \_ \_ NATURAL** e **D2D1 \_ OPACITY \_ MASK CONTENT TEXT \_ \_ \_ GDI \_ COMPATIBLE**. Para os significados desses três tipos, consulte [**D2D1 \_ OPACITY \_ MASK \_ CONTENT**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_opacity_mask_content).

> [!Note]  
> A partir Windows 8, o CONTEÚDO DE [**MÁSCARA de OPACIDADE D2D1 \_ \_ \_**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_opacity_mask_content) não é necessário. Consulte o [**método ID2D1DeviceContext::FillOpacityMask,**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-fillopacitymask(id2d1bitmap_id2d1brush_constd2d1_rect_f_constd2d1_rect_f)) que não tem nenhum parâmetro **D2D1 \_ OPACITY \_ MASK \_ CONTENT.**

 

O exemplo a seguir define o modo de suavização do destino de renderização como ALIAS DO MODO [**\_ ANTIALIAS \_ \_ D2D1**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_antialias_mode) para que a máscara de opacidade funcione corretamente. Em seguida, ele chama o método [**FillOpacityMask**](id2d1rendertarget-fillopacitymask.md) e passa a máscara de opacidade (*m \_ pBitmapMask*), o pincel ao qual a máscara de opacidade é aplicada (*m \_ pFernBitmapBrush*), o tipo de conteúdo dentro da máscara de opacidade [**(D2D1 \_ OPACITY \_ MASK CONTENT \_ \_ GRAPHICS)**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_opacity_mask_content)e a área a ser pintado. A ilustração a seguir mostra a saída produzida.

![ilustração da imagem da planta com uma máscara de opacidade aplicada](images/opacitymaskoutput.png)


```C++
        D2D1_RECT_F rcBrushRect = D2D1::RectF(5, 5, 155, 155);


        // D2D1_ANTIALIAS_MODE_ALIASED must be set for FillOpacityMask to function properly
        m_pRenderTarget->SetAntialiasMode(D2D1_ANTIALIAS_MODE_ALIASED);
        m_pRenderTarget->FillOpacityMask(
            m_pBitmapMask,
            m_pFernBitmapBrush,
            D2D1_OPACITY_MASK_CONTENT_GRAPHICS,
            &rcBrushRect
            );
        m_pRenderTarget->SetAntialiasMode(D2D1_ANTIALIAS_MODE_PER_PRIMITIVE);
```





O código foi omitido neste exemplo.

## <a name="use-a-brush-as-an-opacity-mask-with-the-fillgeometry-method"></a>Usar um pincel como uma máscara de opacidade com o método FillGeometry

A seção anterior descreveu como usar um [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) como uma máscara de opacidade. Direct2D também fornece o método [**ID2D1RenderTarget::FillGeometry,**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) que permite que você especifique opcionalmente o pincel como uma máscara de opacidade ao preencher um [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry). Isso permite que você crie máscaras de opacidade de gradientes (usando [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) ou [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush)) e bitmaps (usando **ID2D1Bitmap**).

O [**método FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) aceita três parâmetros:

-   O primeiro parâmetro, [**um ID2D1Geometry,**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry)define a forma a ser pintada.
-   O segundo parâmetro, [**um ID2D1Brush,**](/windows/win32/api/d2d1/nn-d2d1-id2d1brush)especifica o pincel usado para pintar a geometria. Esse parâmetro deve ser [**um ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) que tenha seus modos x e y-extend definidos como [**D2D1 \_ EXTEND MODE \_ \_ PIN.**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_extend_mode)
-   O terceiro parâmetro, [**um ID2D1Brush,**](/windows/win32/api/d2d1/nn-d2d1-id2d1brush)especifica um pincel a ser usado como a máscara de opacidade. Esse pincel pode ser [**um ID2D1LinearGradientBrush,**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush)ou [**um ID2D1BitmapBrush.**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) (Tecnicamente, você pode usar um [**ID2D1SolidColorBrush,**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush)mas usar um pincel de cor sólida como uma máscara de opacidade não produz resultados interessantes.)

As seções a seguir descrevem como usar [**objetos ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) e [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) como máscaras de opacidade.

### <a name="use-an-linear-gradient-brush-as-an-opacity-mask"></a>Usar um pincel de gradiente linear como uma máscara de opacidade

O diagrama a seguir mostra o efeito de aplicar um pincel de gradiente linear a um retângulo que é preenchido com um bitmap de flores.

![diagrama de um bitmap de flor com um pincel de gradiente linear aplicado](images/brushes-ovw-lineargradient-opacitymask.png)

As etapas a seguir descrevem como re-criar esse efeito.

1.  Defina o conteúdo a ser mascarado. O exemplo a seguir cria [**um ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush), *m \_ pLinearFade Operação Dep.* Os modos de extensão x- e y- para *m \_ pLinearFadeXtendersBitmap* são definidos como [**D2D1 \_ EXTEND MODE \_ \_ FIX**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_extend_mode) para que ele possa ser usado com uma máscara de opacidade pelo [**método FillGeometry.**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry)

    ```cpp
    if (SUCCEEDED(hr))
    {
        // Create the bitmap to be used by the bitmap brush.
        hr = LoadResourceBitmap(
            m_pRenderTarget,
            m_pWICFactory,
            L"LinearFadeFlowers",
            L"Image",
            &m_pLinearFadeFlowersBitmap
            );
    }
 
    if (SUCCEEDED(hr))
        {
            D2D1_BITMAP_BRUSH_PROPERTIES propertiesXClampYClamp = 
                D2D1::BitmapBrushProperties(
                D2D1_EXTEND_MODE_CLAMP,
                D2D1_EXTEND_MODE_CLAMP,
                D2D1_BITMAP_INTERPOLATION_MODE_NEAREST_NEIGHBOR
                );
    ```

    
    <table>
    <colgroup>
    <col  />
    </colgroup>
    <thead>
    <tr class="header">
    <th>C++</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><pre><code>                if (SUCCEEDED(hr))
                    {
                        hr = m_pRenderTarget->CreateBitmapBrush(
                            m_pLinearFadeFlowersBitmap,
                            propertiesXClampYClamp,
                            &m_pLinearFadeFlowersBitmapBrush
                            );
                    }</code></pre></td>
    </tr>
    </tbody>
    </table>

    
    <table>
    <colgroup>
    <col  />
    </colgroup>
    <thead>
    <tr class="header">
    <th>C++</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><pre><code>            }</code></pre></td>
    </tr>
    </tbody>
    </table>

    

2.  Defina a máscara de opacidade. O próximo exemplo de código cria um pincel de gradiente linear diagonal (*m \_ pLinearGradientBrush*) que esmaece de preto totalmente opaco na posição 0 para branco completamente transparente na posição 1.
```C++
                if (SUCCEEDED(hr))
                {
                    ID2D1GradientStopCollection *pGradientStops = NULL;

                    static const D2D1_GRADIENT_STOP gradientStops[] =
                    {
                        {   0.f,  D2D1::ColorF(D2D1::ColorF::Black, 1.0f)  },
                        {   1.f,  D2D1::ColorF(D2D1::ColorF::White, 0.0f)  },
                    };

                    hr = m_pRenderTarget->CreateGradientStopCollection(
                        gradientStops,
                        2,
                        &pGradientStops);


                    if (SUCCEEDED(hr))
                    {
                        hr = m_pRenderTarget->CreateLinearGradientBrush(
                            D2D1::LinearGradientBrushProperties(
                                D2D1::Point2F(0, 0),
                                D2D1::Point2F(150, 150)),
                            pGradientStops,
                            &m_pLinearGradientBrush);
                    }

    
                pGradientStops->Release();
                }
```



    

3.  Use o [**método FillGeometry.**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) O exemplo final usa o método **FillGeometry** para o pincel de conteúdo para preencher um [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry) (*m \_ pRectGeo*) com [**um ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) (*m \_ pLinearFadeBjsBitmap*) e aplica uma máscara de opacidade (*m \_ pLinearGradientBrush*).
```C++
            m_pRenderTarget->FillGeometry(
                m_pRectGeo, 
                m_pLinearFadeFlowersBitmapBrush, 
                m_pLinearGradientBrush
                );
```

    

O código foi omitido neste exemplo.

### <a name="use-a-radial-gradient-brush-as-an-opacity-mask"></a>Usar um pincel de gradiente radial como uma máscara de opacidade

O diagrama a seguir mostra o efeito visual da aplicação de um pincel de gradiente radial a um retângulo que é preenchido com um bitmap de bitmap.

![diagrama de um bitmap com um pincel de gradiente radial aplicado](images/brushes-ovw-radialgradient-opacitymask.png)

O primeiro exemplo cria [**um ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush), *m \_ pRadialFadeMosMostrasBitmapBrush*. Para que ele possa ser usado com uma máscara de opacidade pelo método [**FillGeometry,**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) os modos de extensão x e y para *m \_ pRadialFadeXtendersBitmapBrush* são definidos como [**D2D1 \_ EXTEND MODE \_ \_ FIX.**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_extend_mode)


```C++
            if (SUCCEEDED(hr))
            {
                // Create the bitmap to be used by the bitmap brush.
                hr = LoadResourceBitmap(
                    m_pRenderTarget,
                    m_pWICFactory,
                    L"RadialFadeFlowers",
                    L"Image",
                    &m_pRadialFadeFlowersBitmap
                    );
            }


            if (SUCCEEDED(hr))
            {
                D2D1_BITMAP_BRUSH_PROPERTIES propertiesXClampYClamp = 
                    D2D1::BitmapBrushProperties(
                    D2D1_EXTEND_MODE_CLAMP,
                    D2D1_EXTEND_MODE_CLAMP,
                    D2D1_BITMAP_INTERPOLATION_MODE_NEAREST_NEIGHBOR
                    );
```





<table>
<colgroup>
<col  />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>                if (SUCCEEDED(hr))
                {
                    hr = m_pRenderTarget->CreateBitmapBrush(
                        m_pLinearFadeFlowersBitmap,
                        propertiesXClampYClamp,
                        &m_pLinearFadeFlowersBitmapBrush
                        );
                }</code></pre></td>
</tr>
</tbody>
</table>



<table>
<colgroup>
<col  />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>            }</code></pre></td>
</tr>
</tbody>
</table>



O exemplo a seguir define o pincel de gradiente radial que será usado como a máscara de opacidade.


```C++
            if (SUCCEEDED(hr))
            {
                ID2D1GradientStopCollection *pGradientStops = NULL;

                static const D2D1_GRADIENT_STOP gradientStops[] =
                {
                    {   0.f,  D2D1::ColorF(D2D1::ColorF::Black, 1.0f)  },
                    {   1.f,  D2D1::ColorF(D2D1::ColorF::White, 0.0f)  },
                };

                hr = m_pRenderTarget->CreateGradientStopCollection(
                    gradientStops,
                    2,
                    &pGradientStops);




                if (SUCCEEDED(hr))
                {
                    hr = m_pRenderTarget->CreateRadialGradientBrush(
                        D2D1::RadialGradientBrushProperties(
                            D2D1::Point2F(75, 75),
                            D2D1::Point2F(0, 0),
                            75,
                            75),
                        pGradientStops,
                        &m_pRadialGradientBrush);
                }
                pGradientStops->Release();
            }
```





O exemplo de código final usa [**o ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) (*m \_ pRadialFadeBrushBitmapBrush*) e a máscara de opacidade (*m \_ pRadialGradientBrush*) para preencher [**um ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry) ( m *\_ pRectGeo*).


```C++
        m_pRenderTarget->FillGeometry(
            m_pRectGeo,
            m_pRadialFadeFlowersBitmapBrush, 
            m_pRadialGradientBrush
            );
```



O código foi omitido neste exemplo.

## <a name="apply-an-opacity-mask-to-a-layer"></a>Aplicar uma máscara de opacidade a uma camada

Quando você chama [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) para efetuar push de [**um ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) para um destino de renderização, você pode usar a estrutura [**D2D1 \_ LAYER \_ PARAMETERS**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) para aplicar um pincel como uma máscara de opacidade. O exemplo de código a seguir usa [**um ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) como uma máscara de opacidade.


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



Para obter mais informações sobre como usar camadas, consulte Visão [geral de camadas.](direct2d-layers-overview.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Visão geral de pincéis](direct2d-brushes-overview.md)
</dt> <dt>

[Visão geral de camadas](direct2d-layers-overview.md)
</dt> </dl>

 

 
