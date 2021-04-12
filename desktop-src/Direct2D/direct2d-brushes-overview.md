---
title: 'Visão geral de pincéis '
description: Descreve os diferentes tipos de pincéis fornecidos pelo Direct2D.
ms.assetid: 7a31d9e7-0521-40ee-b2c1-592dfaf5301e
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 7c8b4c4762a03650f150a74d3207d12767e1fb4e
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/20/2020
ms.locfileid: "104366885"
---
# <a name="brushes-overview"></a>Visão geral de pincéis 

Esta visão geral descreve como criar e usar objetos [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush), [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush), [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush)e [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) para pintar áreas com cores sólidas, gradientes e bitmaps. Ele contém as seguintes seções:

## <a name="prerequisites"></a>Pré-requisitos

Esta visão geral pressupõe que você esteja familiarizado com a estrutura de um aplicativo Direct2D básico, conforme descrito em [criando um aplicativo Direct2D simples](direct2d-quickstart.md).

## <a name="brush-types"></a>Tipos de pincel

Um pincel "pinta" uma área com sua saída. Pincéis diferentes têm tipos diferentes de saída. O Direct2D fornece quatro tipos de pincel: [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) pinta uma área com uma cor sólida, [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) com um gradiente linear, [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) com um gradiente radial e [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) com um bitmap.

> [!NOTE]  
> A partir do Windows 8, você também pode usar o [**ID2D1ImageBrush**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1imagebrush), que é semelhante a um pincel de bitmap, mas é possível usar primitivos.

Todos os pincéis herdam de [**ID2D1Brush**](/windows/win32/api/d2d1/nn-d2d1-id2d1brush) e compartilham um conjunto de recursos comuns (Configurando e obtendo a opacidade, e transformando pincéis); Eles são criados por [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) e são recursos dependentes do dispositivo: seu aplicativo deve criar pincéis depois de inicializar o destino de renderização com o qual os pincéis serão usados e recriar os pincéis sempre que o destino de renderização precisar ser recriado. (Para obter mais informações sobre recursos, consulte [visão geral de recursos](resources-and-resource-domains.md).)

A ilustração a seguir mostra exemplos de cada um dos diferentes tipos de pincel.

![Ilustração dos efeitos visuais de pincéis de cores sólidas, pincéis de gradiente linear, pincéis de gradiente radial e pincéis de bitmap](images/brushes-ovw-brushes.png)

## <a name="color-basics"></a>Noções básicas sobre cores

Antes de pintar com um [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) ou um pincel de gradiente, você precisa escolher cores. No Direct2D, as cores são representadas pela estrutura [**\_ \_ F de cor d2d1**](d2d1-color-f.md) (que é, na verdade, apenas um novo nome para a estrutura usada pelo Direct3D, [D3DCOLORVALUE](../direct3d9/d3dcolorvalue.md)).

Antes do Windows 8, [**a \_ cor \_ F do d2d1**](d2d1-color-f.md) usa a codificação sRGB. a codificação sRGB divide as cores em quatro componentes: vermelho, verde, azul e alfa. Cada componente é representado por um valor de ponto flutuante com um intervalo normal de 0.0 a 1.0. Um valor de 0.0 indica a ausência completa da cor, enquanto um valor de 1.0 indica que a cor está totalmente presente. Para o componente alfa, 0.0 representa uma cor totalmente transparente e 1.0 representa uma cor totalmente opaca.

A partir do Windows 8, o [**d2d1 \_ Color \_ F**](d2d1-color-f.md) também aceita a codificação ScRGB. scRGB é um superconjunto de que permite valores de cor acima de 1,0 e abaixo de 0,0.

Para definir uma cor, você pode usar a [**estrutura \_ \_ F de cor d2d1**](d2d1-color-f.md) e inicializar seus campos por conta própria ou pode usar a classe [**d2d1:: colorf**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf) para ajudá-lo a criar a cor. A classe **colorf** fornece vários construtores para definir cores. Se o valor alfa não for especificado nos construtores, o padrão será 1,0.

-   Use o construtor [**colorf (enum, float)**](/previous-versions/windows/desktop/legacy/dd370909(v=vs.85)) para especificar uma cor predefinida e um valor de canal alfa. Um valor de canal alfa varia de 0,0 a 1,0, em que 0,0 representa uma cor totalmente transparente e 1,0 representa uma cor totalmente opaca. A ilustração a seguir mostra várias cores predefinidas e seus equivalentes hexadecimais. Para obter uma lista completa de cores predefinidas, consulte a seção de constantes de cor da classe [**colorf**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf) .

    ![ilustração de cores predefinidas](images/brushes-ovw-colors.png)

    O exemplo a seguir cria uma cor predefinida e a usa para especificar a cor de um [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush).

```C++
hr = m_pRenderTarget->CreateSolidColorBrush(
    D2D1::ColorF(D2D1::ColorF::Black, 1.0f),
    &m_pBlackBrush
    );
```

-   Use o construtor [**colorf (float, float, float, float)**](/windows/win32/api/d2d1helper/nf-d2d1helper-colorf-colorf(float_float_float_float)) para especificar uma cor na sequência de um vermelho, verde, azul e alfa, em que cada elemento tem um valor entre 0,0 e 1,0.

    O exemplo a seguir especifica os valores vermelho, verde, azul e alfa para uma cor.

```C++
    ID2D1SolidColorBrush *pGridBrush = NULL;
    hr = pCompatibleRenderTarget->CreateSolidColorBrush(
        D2D1::ColorF(D2D1::ColorF(0.93f, 0.94f, 0.96f, 1.0f)),
        &pGridBrush
        );
```

-   Use o construtor [**colorf (UINT32, float)**](/windows/win32/api/d2d1helper/nf-d2d1helper-colorf-colorf(uint32_float)) para especificar o valor hexadecimal de uma cor e um valor alfa, conforme mostrado no exemplo a seguir.
```C++
    hr = m_pRenderTarget->CreateSolidColorBrush(
        D2D1::ColorF(D2D1::ColorF(0x9ACD32, 1.0f)),  
        &m_pYellowGreenBrush
        );
```

### <a name="alpha-modes"></a>Modos alfa

Independentemente do modo alfa do destino de renderização com o qual você usa um pincel, os valores [**\_ \_ F de cor de d2d1**](d2d1-color-f.md) são sempre interpretados como um alfa reto.

## <a name="using-solid-color-brushes"></a>Usando pincéis de cores sólidas

Para criar um pincel de cor sólida, chame o método [**ID2D1RenderTarget:: CreateSolidColorBrush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsolidcolorbrush(constd2d1_color_f__id2d1solidcolorbrush)) , que retorna um HRESULT e um objeto [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) . A ilustração a seguir mostra um quadrado que é traçado com um pincel de cor preta e pintado com um pincel de cor sólida que tem o valor de cor de 0x9ACD32.

![ilustração de um quadrado pintado com um pincel de cor sólida](images/brushes-ovw-solidcolor.png)

O código a seguir mostra como criar e usar um pincel de cor preta e um pincel com um valor de cor de 0x9ACD32 para preencher e desenhar esse quadrado.


```C++
    ID2D1SolidColorBrush *m_pBlackBrush;
    ID2D1SolidColorBrush *m_pYellowGreenBrush;
```




```C++
if (SUCCEEDED(hr))
{
    hr = m_pRenderTarget->CreateSolidColorBrush(
        D2D1::ColorF(D2D1::ColorF::Black, 1.0f),
        &m_pBlackBrush
        );
}

// Create a solid color brush with its rgb value 0x9ACD32.
if (SUCCEEDED(hr))
{
    hr = m_pRenderTarget->CreateSolidColorBrush(
        D2D1::ColorF(D2D1::ColorF(0x9ACD32, 1.0f)),  
        &m_pYellowGreenBrush
        );
}
```




```C++
m_pRenderTarget->FillRectangle(&rcBrushRect, m_pYellowGreenBrush);
m_pRenderTarget->DrawRectangle(&rcBrushRect, m_pBlackBrush, 1, NULL);
```



Ao contrário de outros pincéis, a criação de um [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) é uma operação relativamente barata. Você pode criar objetos **ID2D1SolidColorBrush** cada vez que renderizar com pouco ou nenhum impacto no desempenho. Essa abordagem não é recomendada para pincéis de gradiente ou bitmap.

## <a name="using-linear-gradient-brushes"></a>Usando pincéis de gradiente linear

Um [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) pinta uma área com um gradiente linear definido ao longo de uma linha, o eixo gradiente. Você especifica as cores do gradiente e sua localização ao longo do eixo gradiente usando objetos [**ID2D1GradientStop**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) . Você também pode modificar o eixo gradiente, que permite criar gradiente horizontal e vertical e para inverter a direção do gradiente. Para criar um pincel de gradiente linear, chame o método [**ID2D1RenderTarget:: CreateLinearGradientBrush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createlineargradientbrush(constd2d1_linear_gradient_brush_properties__constd2d1_brush_properties__id2d1gradientstopcollection_id2d1lineargradientbrush)) .

A ilustração a seguir mostra um quadrado que é pintado com um [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) que tem duas cores predefinidas, "amarelo" e "ForestGreen".

![ilustração de um quadrado pintado com um pincel de gradiente linear de amarelo e de floresta verde](images/brushes-ovw-lineargradient.png)

Para criar o gradiente mostrado na ilustração anterior, conclua estas etapas:

1.  Declare dois objetos de [**\_ \_ parada de gradiente d2d1**](/windows/win32/api/d2d1/ns-d2d1-d2d1_gradient_stop) . Cada parada de gradiente especifica uma cor e uma posição. Uma posição de 0,0 indica o início do gradiente, enquanto uma posição de 1,0 indica o fim do gradiente.

    O código a seguir cria uma matriz de dois objetos de [**\_ \_ parada de gradiente d2d1**](/windows/win32/api/d2d1/ns-d2d1-d2d1_gradient_stop) . A primeira parada especifica a cor "amarelo" em uma posição 0 e a segunda parada especifica a cor "ForestGreen" na posição 1.

```C++
    // Create an array of gradient stops to put in the gradient stop
    // collection that will be used in the gradient brush.
    ID2D1GradientStopCollection *pGradientStops = NULL;

    D2D1_GRADIENT_STOP gradientStops[2];
    gradientStops[0].color = D2D1::ColorF(D2D1::ColorF::Yellow, 1);
    gradientStops[0].position = 0.0f;
    gradientStops[1].color = D2D1::ColorF(D2D1::ColorF::ForestGreen, 1);
    gradientStops[1].position = 1.0f;
```

    

2.  Crie um [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection). O exemplo a seguir chama [**CreateGradientStopCollection**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-creategradientstopcollection(constd2d1_gradient_stop_uint32_d2d1_gamma_d2d1_extend_mode_id2d1gradientstopcollection)), passando a matriz de objetos de [**\_ \_ parada de gradiente d2d1**](/windows/win32/api/d2d1/ns-d2d1-d2d1_gradient_stop) , o número de paradas de gradiente (2), [**d2d1 \_ gama \_ 2 \_ 2**](/windows/win32/api/d2d1/ne-d2d1-d2d1_gamma) para interpolação e o [**modo de \_ extensão d2d1 \_ \_ fixe**](/windows/win32/api/d2d1/ne-d2d1-d2d1_extend_mode) para o modo de extensão.

```C++
    // Create the ID2D1GradientStopCollection from a previously
    // declared array of D2D1_GRADIENT_STOP structs.
    hr = m_pRenderTarget->CreateGradientStopCollection(
        gradientStops,
        2,
        D2D1_GAMMA_2_2,
        D2D1_EXTEND_MODE_CLAMP,
        &pGradientStops
        );
```

    

3.  Crie o [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush). O exemplo a seguir chama o método [**CreateLinearGradientBrush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createlineargradientbrush(constd2d1_linear_gradient_brush_properties__constd2d1_brush_properties__id2d1gradientstopcollection_id2d1lineargradientbrush)) e passa para ele as propriedades de pincel de gradiente linear que contêm o ponto inicial em (0, 0) e o ponto de extremidade em (150, 150) e as paradas de gradiente criadas na etapa anterior.
```C++
    // The line that determines the direction of the gradient starts at
    // the upper-left corner of the square and ends at the lower-right corner.

    if (SUCCEEDED(hr))
    {
        hr = m_pRenderTarget->CreateLinearGradientBrush(
            D2D1::LinearGradientBrushProperties(
                D2D1::Point2F(0, 0),
                D2D1::Point2F(150, 150)),
            pGradientStops,
            &m_pLinearGradientBrush
            );
    }
```

    

4.  Use o [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush). O próximo exemplo de código usa o pincel para Fille um retângulo.
```C++
    m_pRenderTarget->FillRectangle(&rcBrushRect, m_pLinearGradientBrush);
```

    

## <a name="more-about-gradient-stops"></a>Mais sobre paradas de gradiente

A [**\_ \_ parada de gradiente d2d1**](/windows/win32/api/d2d1/ns-d2d1-d2d1_gradient_stop) é o bloco de construção básico de um pincel de gradiente. Uma parada de gradiente especifica a cor e a posição ao longo do eixo de gradiente. O valor da posição do gradiente varia entre 0,0 e 1,0. Quanto mais próximo for 0,0, mais próximo será a cor do início do gradiente; Quanto mais próximo for 1,0, mais próximo será a cor do final do gradiente.

A ilustração a seguir realça as interrupções de gradiente. O círculo marca a posição das interrupções de gradiente e uma linha tracejada mostra o eixo gradiente.

![ilustração de um pincel de gradiente linear com quatro paradas ao longo do eixo](images/4stoplineargradient.png)

A primeira parada de gradiente especifica a cor amarela em uma posição de 0,0. A segunda parada de gradiente especifica a cor vermelha em uma posição de 0,25. Da esquerda para a direita ao longo do eixo de gradiente, as cores entre essas duas paradas mudam gradualmente de amarelo para vermelho. A terceira parada de gradiente especifica a cor azul em uma posição de 0,75. As cores entre o segundo e o terceiro gradiente param gradualmente de vermelho para azul. A quarta parada de gradiente especifica verde-limão em uma posição de 1,0. As cores entre o terceiro e o quarto gradiente param gradualmente de azul para verde-limão.

## <a name="the-gradient-axis"></a>O eixo gradiente

Conforme mencionado anteriormente, as interrupções de gradiente de um pincel de gradiente linear são posicionadas ao longo de uma linha, o eixo gradiente. Você pode especificar a orientação e o tamanho da linha usando os campos **StartPoint** e **Endpoint** da estrutura [**de \_ \_ Propriedades do \_ pincel \_ de gradiente linear d2d1**](/windows/win32/api/d2d1/ns-d2d1-d2d1_linear_gradient_brush_properties) ao criar um pincel de gradiente linear. Depois de criar um pincel, você pode ajustar o eixo de gradiente chamando os métodos [**SetStartPoint**](/windows/win32/api/d2d1/nf-d2d1-id2d1lineargradientbrush-setstartpoint) e [**SetEndPoint**](/windows/win32/api/d2d1/nf-d2d1-id2d1lineargradientbrush-setendpoint) do pincel. Ao manipular o ponto de partida e o ponto de extremidade do pincel, você pode criar gradientes horizontais e verticais, reverter a direção do gradiente e muito mais.

Por exemplo, na ilustração a seguir, o ponto inicial é definido como (0, 0) e o ponto de extremidade para (150, 50); Isso cria um gradiente diagonal que começa no canto superior esquerdo e se estende para o canto inferior direito da área que está sendo pintada. Quando você define o ponto inicial como (0, 25) e o ponto de extremidade para (150, 25), um gradiente horizontal é criado. Da mesma forma, definir o ponto de início como (75, 0) e o ponto de extremidade para (75, 50) cria um gradiente vertical. Definir o ponto de partida para (0, 50) e o ponto de extremidade para (150, 0) cria um gradiente diagonal que começa no canto inferior esquerdo e se estende para o canto superior direito da área que está sendo pintada.

![ilustração de quatro eixos de gradiente diferentes no mesmo retângulo](images/linear-gradients.png)

## <a name="using-radial-gradient-brushes"></a>Usando pincéis de gradiente radial

Ao contrário de um [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush), que combina duas ou mais cores ao longo de um eixo de gradiente, um [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) pinta uma área com um gradiente radial que mistura duas ou mais cores em uma elipse. Enquanto um **ID2D1LinearGradientBrush** define seu eixo de gradiente com um ponto inicial e um ponto de extremidade, um **ID2D1RadialGradientBrush** define sua elipse de gradiente especificando um centro, um raios horizontais e verticais e um deslocamento de origem de gradiente.

Como um [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush), um [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) usa um [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) para especificar as cores e as posições no gradiente.

A ilustração a seguir mostra um círculo pintado com um [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush). O círculo tem duas interrupções de gradiente: a primeira especifica uma cor predefinida "amarelo" em uma posição de 0,0 e a segunda especifica uma cor predefinida "ForestGreen" em uma posição de 1,0. O gradiente tem um centro de (75, 75), um deslocamento de origem de gradiente de (0, 0) e um raio x e y de 75.

![ilustração de um círculo pintado com um pincel de gradiente radial](images/brushes-ovw-radials.png)

Os exemplos de código a seguir mostram como pintar este círculo com um [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) que tem duas paradas de cor: "amarelo" em uma posição de 0,0 e "ForestGreen" em uma posição de 1,0. Semelhante à criação de um [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush), o exemplo chama [**CreateGradientStopCollection**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-creategradientstopcollection(constd2d1_gradient_stop_uint32_d2d1_gamma_d2d1_extend_mode_id2d1gradientstopcollection)) para criar um [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) de uma matriz de interrupções de gradiente.


```C++
// Create an array of gradient stops to put in the gradient stop
// collection that will be used in the gradient brush.
ID2D1GradientStopCollection *pGradientStops = NULL;

D2D1_GRADIENT_STOP gradientStops[2];
gradientStops[0].color = D2D1::ColorF(D2D1::ColorF::Yellow, 1);
gradientStops[0].position = 0.0f;
gradientStops[1].color = D2D1::ColorF(D2D1::ColorF::ForestGreen, 1);
gradientStops[1].position = 1.0f;
// Create the ID2D1GradientStopCollection from a previously
// declared array of D2D1_GRADIENT_STOP structs.
hr = m_pRenderTarget->CreateGradientStopCollection(
    gradientStops,
    2,
    D2D1_GAMMA_2_2,
    D2D1_EXTEND_MODE_CLAMP,
    &pGradientStops
    );
```



Para criar um [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush), use o método [**ID2D1RenderTarget:: CreateRadialGradientBrush**](/windows/win32/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createradialgradientbrush) . O **CreateRadialGradientBrush** usa três parâmetros. O primeiro parâmetro, uma [**\_ propriedade de \_ \_ pincel de \_ gradiente radial d2d1**](/windows/win32/api/d2d1/ns-d2d1-d2d1_radial_gradient_brush_properties) especifica o centro, o deslocamento da origem do gradiente e o raios horizontal e vertical do gradiente. O segundo parâmetro é um [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) que descreve as cores e suas posições no gradiente, e o terceiro parâmetro é o endereço do ponteiro que recebe a nova referência **ID2D1RadialGradientBrush** . Algumas sobrecargas usam um parâmetro adicional, uma estrutura de [**\_ \_ Propriedades de pincel d2d1**](/windows/win32/api/d2d1/ns-d2d1-d2d1_brush_properties) que especifica um valor de opacidade e uma transformação a ser aplicada ao novo pincel.

O exemplo a seguir chama [**CreateRadialGradientBrush**](/windows/win32/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createradialgradientbrush), passando a matriz de interrupções de gradiente e as propriedades de pincel de gradiente radial que têm o valor *Center* definido como (75, 75), *gradientOriginOffset* definido como (0, 0) e *RadiusX* e *RADIUS* definidos como 75.


```C++
// The center of the gradient is in the center of the box.
// The gradient origin offset was set to zero(0, 0) or center in this case.
if (SUCCEEDED(hr))
{
    hr = m_pRenderTarget->CreateRadialGradientBrush(
        D2D1::RadialGradientBrushProperties(
            D2D1::Point2F(75, 75),
            D2D1::Point2F(0, 0),
            75,
            75),
        pGradientStops,
        &m_pRadialGradientBrush
        );
}
```



O exemplo final usa o pincel para preencher uma elipse.


```C++
m_pRenderTarget->FillEllipse(ellipse, m_pRadialGradientBrush);
m_pRenderTarget->DrawEllipse(ellipse, m_pBlackBrush, 1, NULL);
```



### <a name="configuring-a-radial-gradient"></a>Configurando um gradiente radial

Valores diferentes para *Center*, *gradientOriginOffset*, *RadiusX* e/ou *RADIUS* produzem gradientes diferentes. A ilustração a seguir mostra vários gradientes radiais que têm deslocamentos de origem de gradiente diferentes, criando a aparência da luz iluminando os círculos de diferentes ângulos.

![ilustração do mesmo círculo pintado com pincéis de gradiente radial com deslocamentos de origem diferentes](images/radialgradient.png)

## <a name="using-bitmap-brushes"></a>Usando pincéis de bitmap

Um [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) pinta uma área com um bitmap (representado por um objeto [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) ).

A ilustração a seguir mostra um quadrado pintado com um bitmap de uma planta.

![ilustração de um bitmap quadrado pintado com a planta](images/brushes-ovw-bitmap.png)

Os exemplos a seguir mostram como pintar esse quadrado com um [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush).

O primeiro exemplo inicializa um [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) para uso com o pincel. O **ID2D1Bitmap** é fornecido por um método auxiliar, LoadResourceBitmap, definido em outro lugar no exemplo.


```C++
// Create the bitmap to be used by the bitmap brush.
if (SUCCEEDED(hr))
{
    hr = LoadResourceBitmap(
        m_pRenderTarget,
        m_pWICFactory,
        L"FERN",
        L"Image",
        &m_pBitmap
        );
}
```



Para criar o pincel de bitmap, chame o método [**ID2D1RenderTarget:: CreateBitmapBrush**](id2d1rendertarget-createbitmapbrush.md) e especifique o [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) com o qual pintar. O método retorna um **HRESULT** e um objeto [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) . Algumas sobrecargas **CreateBitmapBrush** permitem que você especifique opções adicionais aceitando [**\_ \_ as propriedades de um pincel d2d1**](/windows/win32/api/d2d1/ns-d2d1-d2d1_brush_properties) e uma estrutura de [**\_ \_ \_ Propriedades de pincel de bitmap d2d1**](/windows/win32/api/d2d1/ns-d2d1-d2d1_bitmap_brush_properties) .


```C++
if (SUCCEEDED(hr))
{
    hr = m_pRenderTarget->CreateBitmapBrush(
        m_pBitmap,
        &m_pBitmapBrush
        );
}
```



O exemplo a seguir usa o pincel para preencher um retângulo.


```C++
m_pRenderTarget->FillRectangle(&rcBrushRect, m_pBitmapBrush);
```



## <a name="configuring-extend-modes"></a>Configurando modos de extensão

Às vezes, o gradiente de um pincel de gradiente ou o bitmap para um pincel de bitmap não preenche completamente a área que está sendo pintada.

-   Quando isso acontece para um [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush), o Direct2D usa as configurações do modo de extensão horizontal ([**SetExtendModeX**](/windows/win32/api/d2d1/nf-d2d1-id2d1bitmapbrush-setextendmodex)) e vertical ([**SetExtendModeY**](/windows/win32/api/d2d1/nf-d2d1-id2d1bitmapbrush-setextendmodey)) do pincel para determinar como preencher a área restante.

-   Quando isso acontece com um pincel de gradiente, Direct2D determina como preencher a área restante usando o valor do parâmetro [**de \_ \_ modo estendido d2d1**](/windows/win32/api/d2d1/ne-d2d1-d2d1_extend_mode) que você especificou quando chamou o [**CreateGradientStopCollection**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-creategradientstopcollection(constd2d1_gradient_stop_uint32_d2d1_gamma_d2d1_extend_mode_id2d1gradientstopcollection)) para criar a [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection)do pincel de gradiente.

A ilustração a seguir mostra os resultados de cada combinação possível dos modos de extensão para um [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush): [**d2d1 \_ Extend \_ mode \_ fixe**](/windows/win32/api/d2d1/ne-d2d1-d2d1_extend_mode) (fixe), **d2d1 \_ estender \_ modo \_ encapsulamento** (Wrap) e **d2d1 \_ estender \_ espelho** (espelho).

![ilustração de uma imagem original e as imagens resultantes de vários modos de extensão](images/bitmapwrap-clamp-mirror.png)

O exemplo a seguir mostra como definir os modos x-e y de extensão do pincel de bitmap para [**d2d1 \_ estender \_ espelho**](/windows/win32/api/d2d1/ne-d2d1-d2d1_extend_mode). Em seguida, ele pinta o retângulo com o [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush).


```C++
m_pBitmapBrush->SetExtendModeX(D2D1_EXTEND_MODE_MIRROR);
m_pBitmapBrush->SetExtendModeY(D2D1_EXTEND_MODE_MIRROR);

m_pRenderTarget->FillRectangle(exampleRectangle, m_pBitmapBrush);
```



Ele produz a saída conforme mostrado na ilustração a seguir.

![ilustração de uma imagem original e a imagem resultante após o espelhamento da direção x e da direção y](images/brushes-ovw-bitmapmirrormirror.png)

## <a name="transforming-brushes"></a>Transformando pincéis

Quando você pinta com um pincel, ele pinta no espaço de coordenadas do destino de renderização. Os pincéis não se posicionam automaticamente para se alinharem com o objeto que está sendo pintado; Por padrão, eles começam a pintar na origem (0, 0) do destino de renderização.

Você pode "mover" o gradiente definido por um [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) para uma área de destino definindo seu ponto de partida e ponto de extremidade. Da mesma forma, você pode mover o gradiente definido por um [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) alterando seu centro e raios.

Para alinhar o conteúdo de um [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) à área que está sendo pintada, você pode usar o método [**SetTransform**](/windows/win32/api/d2d1/nf-d2d1-id2d1brush-settransform(constd2d1_matrix_3x2_f)) para converter o bitmap no local desejado. Essa transformação afeta apenas o pincel; Ele não afeta nenhum outro conteúdo desenhado pelo destino de renderização.

A ilustração a seguir mostra o efeito de usar um [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) para preencher um retângulo localizado em (100, 100). A ilustração na ilustração à esquerda mostra o resultado do preenchimento do retângulo sem transformar o pincel: o bitmap é desenhado na origem do destino do processamento. Como resultado, apenas uma parte do bitmap é exibida no retângulo. A ilustração à direita mostra o resultado da transformação do **ID2D1BitmapBrush** para que seu conteúdo seja deslocado 50 pixels para a direita e 50 pixels para baixo. O bitmap agora preenche o retângulo.

![ilustração de um quadrado pintado com um pincel de bitmap sem transformar o pincel e transformando o pincel](images/brushes-ovw-transform.png)

O código a seguir mostra como fazer isso. Primeiro, aplique uma tradução ao [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush), movendo o pincel 50 pixels para o eixo x e 50 pixels para baixo ao longo do eixo y. Em seguida, use o **ID2D1BitmapBrush** para preencher o retângulo que tem o canto superior esquerdo em (100, 100) e no canto inferior direito em (200, 200).


```cpp
// Create the bitmap to be used by the bitmap brush.
if (SUCCEEDED(hr))
{
    hr = LoadResourceBitmap(
        m_pRenderTarget,
        m_pWICFactory,
        L"FERN",
        L"Image",
        &m_pBitmap
        );
   
}

if (SUCCEEDED(hr))
{
    hr = m_pRenderTarget->CreateBitmapBrush(
        m_pBitmap,
        &m_pBitmapBrush
        );
}

D2D1_RECT_F rcTransformedBrushRect = D2D1::RectF(100, 100, 200, 200);

// Demonstrate the effect of transforming a bitmap brush.
m_pBitmapBrush->SetTransform(
     D2D1::Matrix3x2F::Translation(D2D1::SizeF(50,50))
     );

// To see the content of the rcTransformedBrushRect, comment
// out this statement.
m_pRenderTarget->FillRectangle(
     &rcTransformedBrushRect, 
     m_pBitmapBrush
     );

m_pRenderTarget->DrawRectangle(rcTransformedBrushRect, m_pBlackBrush, 1, NULL);
```

## <a name="related-topics"></a>Tópicos relacionados

* [Referência de Direct2D](reference.md)
* [Como criar um pincel de cor sólida](how-to-create-a-solid-color-brush.md)
* [Como criar um pincel de gradiente linear](how-to-create-a-linear-gradient-brush.md)
* [Como criar um pincel gradiente radial](how-to-create-a-radial-gradient-brush.md)
* [Como criar um pincel de bitmap](how-to-create-a-bitmap-brush.md)
