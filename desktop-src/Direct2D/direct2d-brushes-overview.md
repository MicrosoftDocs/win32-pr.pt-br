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
# <a name="brushes-overview"></a><span data-ttu-id="adb95-103">Visão geral de pincéis </span><span class="sxs-lookup"><span data-stu-id="adb95-103">Brushes overview</span></span>

<span data-ttu-id="adb95-104">Esta visão geral descreve como criar e usar objetos [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush), [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush), [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush)e [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) para pintar áreas com cores sólidas, gradientes e bitmaps.</span><span class="sxs-lookup"><span data-stu-id="adb95-104">This overview describes how to create and use [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush), [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush), [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush), and [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) objects to paint areas with solid colors, gradients, and bitmaps.</span></span> <span data-ttu-id="adb95-105">Ele contém as seguintes seções:</span><span class="sxs-lookup"><span data-stu-id="adb95-105">It contains the following sections.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="adb95-106">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="adb95-106">Prerequisites</span></span>

<span data-ttu-id="adb95-107">Esta visão geral pressupõe que você esteja familiarizado com a estrutura de um aplicativo Direct2D básico, conforme descrito em [criando um aplicativo Direct2D simples](direct2d-quickstart.md).</span><span class="sxs-lookup"><span data-stu-id="adb95-107">This overview assumes that you are familiar with the structure of a basic Direct2D application, as described in [Creating a Simple Direct2D Application](direct2d-quickstart.md).</span></span>

## <a name="brush-types"></a><span data-ttu-id="adb95-108">Tipos de pincel</span><span class="sxs-lookup"><span data-stu-id="adb95-108">Brush types</span></span>

<span data-ttu-id="adb95-109">Um pincel "pinta" uma área com sua saída.</span><span class="sxs-lookup"><span data-stu-id="adb95-109">A brush "paints" an area with its output.</span></span> <span data-ttu-id="adb95-110">Pincéis diferentes têm tipos diferentes de saída.</span><span class="sxs-lookup"><span data-stu-id="adb95-110">Different brushes have different types of output.</span></span> <span data-ttu-id="adb95-111">O Direct2D fornece quatro tipos de pincel: [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) pinta uma área com uma cor sólida, [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) com um gradiente linear, [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) com um gradiente radial e [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) com um bitmap.</span><span class="sxs-lookup"><span data-stu-id="adb95-111">Direct2D provides four brush types: [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) paints an area with a solid color, [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) with a linear gradient, [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) with a radial gradient, and [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) with a bitmap.</span></span>

> [!NOTE]  
> <span data-ttu-id="adb95-112">A partir do Windows 8, você também pode usar o [**ID2D1ImageBrush**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1imagebrush), que é semelhante a um pincel de bitmap, mas é possível usar primitivos.</span><span class="sxs-lookup"><span data-stu-id="adb95-112">Starting with Windows 8, you can also use [**ID2D1ImageBrush**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1imagebrush), which is similar to a bitmap brush, but you can use primitives, too.</span></span>

<span data-ttu-id="adb95-113">Todos os pincéis herdam de [**ID2D1Brush**](/windows/win32/api/d2d1/nn-d2d1-id2d1brush) e compartilham um conjunto de recursos comuns (Configurando e obtendo a opacidade, e transformando pincéis); Eles são criados por [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) e são recursos dependentes do dispositivo: seu aplicativo deve criar pincéis depois de inicializar o destino de renderização com o qual os pincéis serão usados e recriar os pincéis sempre que o destino de renderização precisar ser recriado.</span><span class="sxs-lookup"><span data-stu-id="adb95-113">All brushes inherit from [**ID2D1Brush**](/windows/win32/api/d2d1/nn-d2d1-id2d1brush) and share a set of common features (setting and getting opacity, and transforming brushes); they are created by [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) and are device-dependent resources: your application should create brushes after it initializes the render target with which the brushes will be used, and recreate the brushes whenever the render target needs recreated.</span></span> <span data-ttu-id="adb95-114">(Para obter mais informações sobre recursos, consulte [visão geral de recursos](resources-and-resource-domains.md).)</span><span class="sxs-lookup"><span data-stu-id="adb95-114">(For more information about resources, see [Resources Overview](resources-and-resource-domains.md).)</span></span>

<span data-ttu-id="adb95-115">A ilustração a seguir mostra exemplos de cada um dos diferentes tipos de pincel.</span><span class="sxs-lookup"><span data-stu-id="adb95-115">The following illustration shows examples of each of the different brush types.</span></span>

![Ilustração dos efeitos visuais de pincéis de cores sólidas, pincéis de gradiente linear, pincéis de gradiente radial e pincéis de bitmap](images/brushes-ovw-brushes.png)

## <a name="color-basics"></a><span data-ttu-id="adb95-117">Noções básicas sobre cores</span><span class="sxs-lookup"><span data-stu-id="adb95-117">Color basics</span></span>

<span data-ttu-id="adb95-118">Antes de pintar com um [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) ou um pincel de gradiente, você precisa escolher cores.</span><span class="sxs-lookup"><span data-stu-id="adb95-118">Before you paint with an [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) or a gradient brush, you need to choose colors.</span></span> <span data-ttu-id="adb95-119">No Direct2D, as cores são representadas pela estrutura [**\_ \_ F de cor d2d1**](d2d1-color-f.md) (que é, na verdade, apenas um novo nome para a estrutura usada pelo Direct3D, [D3DCOLORVALUE](../direct3d9/d3dcolorvalue.md)).</span><span class="sxs-lookup"><span data-stu-id="adb95-119">In Direct2D, colors are represented by the [**D2D1\_COLOR\_F**](d2d1-color-f.md) structure (which is actually just a new name for the structure that is used by Direct3D, [D3DCOLORVALUE](../direct3d9/d3dcolorvalue.md)).</span></span>

<span data-ttu-id="adb95-120">Antes do Windows 8, [**a \_ cor \_ F do d2d1**](d2d1-color-f.md) usa a codificação sRGB.</span><span class="sxs-lookup"><span data-stu-id="adb95-120">Prior to Windows 8, [**D2D1\_COLOR\_F**](d2d1-color-f.md) uses sRGB encoding.</span></span> <span data-ttu-id="adb95-121">a codificação sRGB divide as cores em quatro componentes: vermelho, verde, azul e alfa.</span><span class="sxs-lookup"><span data-stu-id="adb95-121">sRGB encoding divides colors into four components: red, green, blue, and alpha.</span></span> <span data-ttu-id="adb95-122">Cada componente é representado por um valor de ponto flutuante com um intervalo normal de 0.0 a 1.0.</span><span class="sxs-lookup"><span data-stu-id="adb95-122">Each component is represented by a floating point value with a normal range of 0.0 to 1.0.</span></span> <span data-ttu-id="adb95-123">Um valor de 0.0 indica a ausência completa da cor, enquanto um valor de 1.0 indica que a cor está totalmente presente.</span><span class="sxs-lookup"><span data-stu-id="adb95-123">A value of 0.0 indicates the complete absence of that color, while a value of 1.0 indicates that the color is fully present.</span></span> <span data-ttu-id="adb95-124">Para o componente alfa, 0.0 representa uma cor totalmente transparente e 1.0 representa uma cor totalmente opaca.</span><span class="sxs-lookup"><span data-stu-id="adb95-124">For the alpha component, 0.0 represents a fully transparent color and 1.0 represents a fully opaque color.</span></span>

<span data-ttu-id="adb95-125">A partir do Windows 8, o [**d2d1 \_ Color \_ F**](d2d1-color-f.md) também aceita a codificação ScRGB.</span><span class="sxs-lookup"><span data-stu-id="adb95-125">Starting in Windows 8, [**D2D1\_COLOR\_F**](d2d1-color-f.md) also accepts scRGB encoding.</span></span> <span data-ttu-id="adb95-126">scRGB é um superconjunto de que permite valores de cor acima de 1,0 e abaixo de 0,0.</span><span class="sxs-lookup"><span data-stu-id="adb95-126">scRGB is a superset of that allows color values above 1.0 and below 0.0.</span></span>

<span data-ttu-id="adb95-127">Para definir uma cor, você pode usar a [**estrutura \_ \_ F de cor d2d1**](d2d1-color-f.md) e inicializar seus campos por conta própria ou pode usar a classe [**d2d1:: colorf**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf) para ajudá-lo a criar a cor.</span><span class="sxs-lookup"><span data-stu-id="adb95-127">To define a color, you can use the [**D2D1\_COLOR\_F**](d2d1-color-f.md) structure and initialize its fields yourself, or you can use the [**D2D1::ColorF**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf) class to help you create the color.</span></span> <span data-ttu-id="adb95-128">A classe **colorf** fornece vários construtores para definir cores.</span><span class="sxs-lookup"><span data-stu-id="adb95-128">The **ColorF** class provides several constructors for defining colors.</span></span> <span data-ttu-id="adb95-129">Se o valor alfa não for especificado nos construtores, o padrão será 1,0.</span><span class="sxs-lookup"><span data-stu-id="adb95-129">If the alpha value is not specified in the constructors, it defaults to 1.0.</span></span>

-   <span data-ttu-id="adb95-130">Use o construtor [**colorf (enum, float)**](/previous-versions/windows/desktop/legacy/dd370909(v=vs.85)) para especificar uma cor predefinida e um valor de canal alfa.</span><span class="sxs-lookup"><span data-stu-id="adb95-130">Use the [**ColorF(Enum, FLOAT)**](/previous-versions/windows/desktop/legacy/dd370909(v=vs.85)) constructor to specify a predefined color and an alpha channel value.</span></span> <span data-ttu-id="adb95-131">Um valor de canal alfa varia de 0,0 a 1,0, em que 0,0 representa uma cor totalmente transparente e 1,0 representa uma cor totalmente opaca.</span><span class="sxs-lookup"><span data-stu-id="adb95-131">An alpha channel value ranges from 0.0 to 1.0, where 0.0 represents a fully transparent color and 1.0 represents a fully opaque color.</span></span> <span data-ttu-id="adb95-132">A ilustração a seguir mostra várias cores predefinidas e seus equivalentes hexadecimais.</span><span class="sxs-lookup"><span data-stu-id="adb95-132">The following illustration shows several predefined colors and their hexadecimal equivalents.</span></span> <span data-ttu-id="adb95-133">Para obter uma lista completa de cores predefinidas, consulte a seção de constantes de cor da classe [**colorf**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf) .</span><span class="sxs-lookup"><span data-stu-id="adb95-133">For a complete list of predefined colors, see the Color constants section of the [**ColorF**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf) class.</span></span>

    ![ilustração de cores predefinidas](images/brushes-ovw-colors.png)

    <span data-ttu-id="adb95-135">O exemplo a seguir cria uma cor predefinida e a usa para especificar a cor de um [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush).</span><span class="sxs-lookup"><span data-stu-id="adb95-135">The following example creates a predefined color and uses it to specify the color of an [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush).</span></span>

```C++
hr = m_pRenderTarget->CreateSolidColorBrush(
    D2D1::ColorF(D2D1::ColorF::Black, 1.0f),
    &m_pBlackBrush
    );
```

-   <span data-ttu-id="adb95-136">Use o construtor [**colorf (float, float, float, float)**](/windows/win32/api/d2d1helper/nf-d2d1helper-colorf-colorf(float_float_float_float)) para especificar uma cor na sequência de um vermelho, verde, azul e alfa, em que cada elemento tem um valor entre 0,0 e 1,0.</span><span class="sxs-lookup"><span data-stu-id="adb95-136">Use the [**ColorF(FLOAT, FLOAT, FLOAT, FLOAT)**](/windows/win32/api/d2d1helper/nf-d2d1helper-colorf-colorf(float_float_float_float)) constructor to specify a color in the sequence of a red, green, blue, and alpha, where each element has a value between 0.0 and 1.0.</span></span>

    <span data-ttu-id="adb95-137">O exemplo a seguir especifica os valores vermelho, verde, azul e alfa para uma cor.</span><span class="sxs-lookup"><span data-stu-id="adb95-137">The following example specifies the red, green, blue, and alpha values for a color.</span></span>

```C++
    ID2D1SolidColorBrush *pGridBrush = NULL;
    hr = pCompatibleRenderTarget->CreateSolidColorBrush(
        D2D1::ColorF(D2D1::ColorF(0.93f, 0.94f, 0.96f, 1.0f)),
        &pGridBrush
        );
```

-   <span data-ttu-id="adb95-138">Use o construtor [**colorf (UINT32, float)**](/windows/win32/api/d2d1helper/nf-d2d1helper-colorf-colorf(uint32_float)) para especificar o valor hexadecimal de uma cor e um valor alfa, conforme mostrado no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="adb95-138">Use the [**ColorF(UINT32, FLOAT)**](/windows/win32/api/d2d1helper/nf-d2d1helper-colorf-colorf(uint32_float)) constructor to specify the hexadecimal value of a color and an alpha value, as shown in the following example.</span></span>
```C++
    hr = m_pRenderTarget->CreateSolidColorBrush(
        D2D1::ColorF(D2D1::ColorF(0x9ACD32, 1.0f)),  
        &m_pYellowGreenBrush
        );
```

### <a name="alpha-modes"></a><span data-ttu-id="adb95-139">Modos alfa</span><span class="sxs-lookup"><span data-stu-id="adb95-139">Alpha modes</span></span>

<span data-ttu-id="adb95-140">Independentemente do modo alfa do destino de renderização com o qual você usa um pincel, os valores [**\_ \_ F de cor de d2d1**](d2d1-color-f.md) são sempre interpretados como um alfa reto.</span><span class="sxs-lookup"><span data-stu-id="adb95-140">Regardless of the alpha mode of the render target with which you use a brush, [**D2D1\_COLOR\_F**](d2d1-color-f.md) values are always interpreted as straight alpha.</span></span>

## <a name="using-solid-color-brushes"></a><span data-ttu-id="adb95-141">Usando pincéis de cores sólidas</span><span class="sxs-lookup"><span data-stu-id="adb95-141">Using solid color brushes</span></span>

<span data-ttu-id="adb95-142">Para criar um pincel de cor sólida, chame o método [**ID2D1RenderTarget:: CreateSolidColorBrush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsolidcolorbrush(constd2d1_color_f__id2d1solidcolorbrush)) , que retorna um HRESULT e um objeto [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) .</span><span class="sxs-lookup"><span data-stu-id="adb95-142">To create a solid color brush, call the [**ID2D1RenderTarget::CreateSolidColorBrush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsolidcolorbrush(constd2d1_color_f__id2d1solidcolorbrush)) method, which returns an HRESULT and an [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) object.</span></span> <span data-ttu-id="adb95-143">A ilustração a seguir mostra um quadrado que é traçado com um pincel de cor preta e pintado com um pincel de cor sólida que tem o valor de cor de 0x9ACD32.</span><span class="sxs-lookup"><span data-stu-id="adb95-143">The following illustration shows a square that is stroked with a black color brush and painted with a solid color brush that has the color value of 0x9ACD32.</span></span>

![ilustração de um quadrado pintado com um pincel de cor sólida](images/brushes-ovw-solidcolor.png)

<span data-ttu-id="adb95-145">O código a seguir mostra como criar e usar um pincel de cor preta e um pincel com um valor de cor de 0x9ACD32 para preencher e desenhar esse quadrado.</span><span class="sxs-lookup"><span data-stu-id="adb95-145">The following code shows how to create and use a black color brush and a brush with a color value of 0x9ACD32 to fill and draw this square.</span></span>


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



<span data-ttu-id="adb95-146">Ao contrário de outros pincéis, a criação de um [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) é uma operação relativamente barata.</span><span class="sxs-lookup"><span data-stu-id="adb95-146">Unlike other brushes, creating an [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) is a relatively inexpensive operation.</span></span> <span data-ttu-id="adb95-147">Você pode criar objetos **ID2D1SolidColorBrush** cada vez que renderizar com pouco ou nenhum impacto no desempenho.</span><span class="sxs-lookup"><span data-stu-id="adb95-147">You may create **ID2D1SolidColorBrush** objects each time you render with little to no performance impact.</span></span> <span data-ttu-id="adb95-148">Essa abordagem não é recomendada para pincéis de gradiente ou bitmap.</span><span class="sxs-lookup"><span data-stu-id="adb95-148">This approach is not recommended for gradient or bitmap brushes.</span></span>

## <a name="using-linear-gradient-brushes"></a><span data-ttu-id="adb95-149">Usando pincéis de gradiente linear</span><span class="sxs-lookup"><span data-stu-id="adb95-149">Using linear gradient brushes</span></span>

<span data-ttu-id="adb95-150">Um [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) pinta uma área com um gradiente linear definido ao longo de uma linha, o eixo gradiente.</span><span class="sxs-lookup"><span data-stu-id="adb95-150">An [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) paints an area with a linear gradient defined along a line, the gradient axis.</span></span> <span data-ttu-id="adb95-151">Você especifica as cores do gradiente e sua localização ao longo do eixo gradiente usando objetos [**ID2D1GradientStop**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) .</span><span class="sxs-lookup"><span data-stu-id="adb95-151">You specify the gradient's colors and their location along the gradient axis using [**ID2D1GradientStop**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) objects.</span></span> <span data-ttu-id="adb95-152">Você também pode modificar o eixo gradiente, que permite criar gradiente horizontal e vertical e para inverter a direção do gradiente.</span><span class="sxs-lookup"><span data-stu-id="adb95-152">You may also modify the gradient axis, which enables you to create horizontal and vertical gradient and to reverse the gradient direction.</span></span> <span data-ttu-id="adb95-153">Para criar um pincel de gradiente linear, chame o método [**ID2D1RenderTarget:: CreateLinearGradientBrush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createlineargradientbrush(constd2d1_linear_gradient_brush_properties__constd2d1_brush_properties__id2d1gradientstopcollection_id2d1lineargradientbrush)) .</span><span class="sxs-lookup"><span data-stu-id="adb95-153">To create a linear gradient brush, call the [**ID2D1RenderTarget::CreateLinearGradientBrush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createlineargradientbrush(constd2d1_linear_gradient_brush_properties__constd2d1_brush_properties__id2d1gradientstopcollection_id2d1lineargradientbrush)) method.</span></span>

<span data-ttu-id="adb95-154">A ilustração a seguir mostra um quadrado que é pintado com um [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) que tem duas cores predefinidas, "amarelo" e "ForestGreen".</span><span class="sxs-lookup"><span data-stu-id="adb95-154">The following illustration shows a square that is painted with an [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) that has two predefined colors, "Yellow" and "ForestGreen".</span></span>

![ilustração de um quadrado pintado com um pincel de gradiente linear de amarelo e de floresta verde](images/brushes-ovw-lineargradient.png)

<span data-ttu-id="adb95-156">Para criar o gradiente mostrado na ilustração anterior, conclua estas etapas:</span><span class="sxs-lookup"><span data-stu-id="adb95-156">To create the gradient shown in the preceding illustration, complete these steps:</span></span>

1.  <span data-ttu-id="adb95-157">Declare dois objetos de [**\_ \_ parada de gradiente d2d1**](/windows/win32/api/d2d1/ns-d2d1-d2d1_gradient_stop) .</span><span class="sxs-lookup"><span data-stu-id="adb95-157">Declare two [**D2D1\_GRADIENT\_STOP**](/windows/win32/api/d2d1/ns-d2d1-d2d1_gradient_stop) objects.</span></span> <span data-ttu-id="adb95-158">Cada parada de gradiente especifica uma cor e uma posição.</span><span class="sxs-lookup"><span data-stu-id="adb95-158">Each gradient stop specifies a color and a position.</span></span> <span data-ttu-id="adb95-159">Uma posição de 0,0 indica o início do gradiente, enquanto uma posição de 1,0 indica o fim do gradiente.</span><span class="sxs-lookup"><span data-stu-id="adb95-159">A position of 0.0 indicates the beginning of the gradient, while a position of 1.0 indicates the end of the gradient.</span></span>

    <span data-ttu-id="adb95-160">O código a seguir cria uma matriz de dois objetos de [**\_ \_ parada de gradiente d2d1**](/windows/win32/api/d2d1/ns-d2d1-d2d1_gradient_stop) .</span><span class="sxs-lookup"><span data-stu-id="adb95-160">The following code creates an array of two [**D2D1\_GRADIENT\_STOP**](/windows/win32/api/d2d1/ns-d2d1-d2d1_gradient_stop) objects.</span></span> <span data-ttu-id="adb95-161">A primeira parada especifica a cor "amarelo" em uma posição 0 e a segunda parada especifica a cor "ForestGreen" na posição 1.</span><span class="sxs-lookup"><span data-stu-id="adb95-161">The first stop specifies the color "Yellow" at a position 0, and the second stop specifies the color "ForestGreen" at position 1.</span></span>

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

    

2.  <span data-ttu-id="adb95-162">Crie um [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection).</span><span class="sxs-lookup"><span data-stu-id="adb95-162">Create an [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection).</span></span> <span data-ttu-id="adb95-163">O exemplo a seguir chama [**CreateGradientStopCollection**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-creategradientstopcollection(constd2d1_gradient_stop_uint32_d2d1_gamma_d2d1_extend_mode_id2d1gradientstopcollection)), passando a matriz de objetos de [**\_ \_ parada de gradiente d2d1**](/windows/win32/api/d2d1/ns-d2d1-d2d1_gradient_stop) , o número de paradas de gradiente (2), [**d2d1 \_ gama \_ 2 \_ 2**](/windows/win32/api/d2d1/ne-d2d1-d2d1_gamma) para interpolação e o [**modo de \_ extensão d2d1 \_ \_ fixe**](/windows/win32/api/d2d1/ne-d2d1-d2d1_extend_mode) para o modo de extensão.</span><span class="sxs-lookup"><span data-stu-id="adb95-163">The following example calls [**CreateGradientStopCollection**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-creategradientstopcollection(constd2d1_gradient_stop_uint32_d2d1_gamma_d2d1_extend_mode_id2d1gradientstopcollection)), passing in the array of [**D2D1\_GRADIENT\_STOP**](/windows/win32/api/d2d1/ns-d2d1-d2d1_gradient_stop) objects, the number of gradient stops (2), [**D2D1\_GAMMA\_2\_2**](/windows/win32/api/d2d1/ne-d2d1-d2d1_gamma) for interpolation, and [**D2D1\_EXTEND\_MODE\_CLAMP**](/windows/win32/api/d2d1/ne-d2d1-d2d1_extend_mode) for the extend mode.</span></span>

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

    

3.  <span data-ttu-id="adb95-164">Crie o [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush).</span><span class="sxs-lookup"><span data-stu-id="adb95-164">Create the [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush).</span></span> <span data-ttu-id="adb95-165">O exemplo a seguir chama o método [**CreateLinearGradientBrush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createlineargradientbrush(constd2d1_linear_gradient_brush_properties__constd2d1_brush_properties__id2d1gradientstopcollection_id2d1lineargradientbrush)) e passa para ele as propriedades de pincel de gradiente linear que contêm o ponto inicial em (0, 0) e o ponto de extremidade em (150, 150) e as paradas de gradiente criadas na etapa anterior.</span><span class="sxs-lookup"><span data-stu-id="adb95-165">The next example calls the [**CreateLinearGradientBrush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createlineargradientbrush(constd2d1_linear_gradient_brush_properties__constd2d1_brush_properties__id2d1gradientstopcollection_id2d1lineargradientbrush)) method and passes it the linear gradient brush properties that contain the start point at (0, 0) and the end point at (150, 150), and the gradient stops created in the previous step.</span></span>
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

    

4.  <span data-ttu-id="adb95-166">Use o [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush).</span><span class="sxs-lookup"><span data-stu-id="adb95-166">Use the [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush).</span></span> <span data-ttu-id="adb95-167">O próximo exemplo de código usa o pincel para Fille um retângulo.</span><span class="sxs-lookup"><span data-stu-id="adb95-167">The next code example uses the brush to fille a rectangle.</span></span>
```C++
    m_pRenderTarget->FillRectangle(&rcBrushRect, m_pLinearGradientBrush);
```

    

## <a name="more-about-gradient-stops"></a><span data-ttu-id="adb95-168">Mais sobre paradas de gradiente</span><span class="sxs-lookup"><span data-stu-id="adb95-168">More about gradient stops</span></span>

<span data-ttu-id="adb95-169">A [**\_ \_ parada de gradiente d2d1**](/windows/win32/api/d2d1/ns-d2d1-d2d1_gradient_stop) é o bloco de construção básico de um pincel de gradiente.</span><span class="sxs-lookup"><span data-stu-id="adb95-169">The [**D2D1\_GRADIENT\_STOP**](/windows/win32/api/d2d1/ns-d2d1-d2d1_gradient_stop) is the basic building block of a gradient brush.</span></span> <span data-ttu-id="adb95-170">Uma parada de gradiente especifica a cor e a posição ao longo do eixo de gradiente.</span><span class="sxs-lookup"><span data-stu-id="adb95-170">A gradient stop specifies the color and the position along the gradient axis.</span></span> <span data-ttu-id="adb95-171">O valor da posição do gradiente varia entre 0,0 e 1,0.</span><span class="sxs-lookup"><span data-stu-id="adb95-171">The value of the gradient position ranges between 0.0 and 1.0.</span></span> <span data-ttu-id="adb95-172">Quanto mais próximo for 0,0, mais próximo será a cor do início do gradiente; Quanto mais próximo for 1,0, mais próximo será a cor do final do gradiente.</span><span class="sxs-lookup"><span data-stu-id="adb95-172">The closer it is to 0.0, the closer the color is to the start of the gradient; the closer it is to 1.0, the closer the color is to the end of the gradient.</span></span>

<span data-ttu-id="adb95-173">A ilustração a seguir realça as interrupções de gradiente.</span><span class="sxs-lookup"><span data-stu-id="adb95-173">The following illustration highlights the gradient stops.</span></span> <span data-ttu-id="adb95-174">O círculo marca a posição das interrupções de gradiente e uma linha tracejada mostra o eixo gradiente.</span><span class="sxs-lookup"><span data-stu-id="adb95-174">The circle marks the position of gradient stops and a dashed line shows the gradient axis.</span></span>

![ilustração de um pincel de gradiente linear com quatro paradas ao longo do eixo](images/4stoplineargradient.png)

<span data-ttu-id="adb95-176">A primeira parada de gradiente especifica a cor amarela em uma posição de 0,0.</span><span class="sxs-lookup"><span data-stu-id="adb95-176">The first gradient stop specifies the color yellow at a position of 0.0.</span></span> <span data-ttu-id="adb95-177">A segunda parada de gradiente especifica a cor vermelha em uma posição de 0,25.</span><span class="sxs-lookup"><span data-stu-id="adb95-177">The second gradient stop specifies red color at a position of 0.25.</span></span> <span data-ttu-id="adb95-178">Da esquerda para a direita ao longo do eixo de gradiente, as cores entre essas duas paradas mudam gradualmente de amarelo para vermelho.</span><span class="sxs-lookup"><span data-stu-id="adb95-178">From left to right along the gradient axis, the colors between these two stops gradually change from yellow to red.</span></span> <span data-ttu-id="adb95-179">A terceira parada de gradiente especifica a cor azul em uma posição de 0,75.</span><span class="sxs-lookup"><span data-stu-id="adb95-179">The third gradient stop specifies blue color at a position of 0.75.</span></span> <span data-ttu-id="adb95-180">As cores entre o segundo e o terceiro gradiente param gradualmente de vermelho para azul.</span><span class="sxs-lookup"><span data-stu-id="adb95-180">The colors between the second and third gradient stops gradually change from red to blue.</span></span> <span data-ttu-id="adb95-181">A quarta parada de gradiente especifica verde-limão em uma posição de 1,0.</span><span class="sxs-lookup"><span data-stu-id="adb95-181">The fourth gradient stop specifies lime green at a position of 1.0.</span></span> <span data-ttu-id="adb95-182">As cores entre o terceiro e o quarto gradiente param gradualmente de azul para verde-limão.</span><span class="sxs-lookup"><span data-stu-id="adb95-182">The colors between the third and fourth gradient stops gradually change from blue to lime green.</span></span>

## <a name="the-gradient-axis"></a><span data-ttu-id="adb95-183">O eixo gradiente</span><span class="sxs-lookup"><span data-stu-id="adb95-183">The gradient axis</span></span>

<span data-ttu-id="adb95-184">Conforme mencionado anteriormente, as interrupções de gradiente de um pincel de gradiente linear são posicionadas ao longo de uma linha, o eixo gradiente.</span><span class="sxs-lookup"><span data-stu-id="adb95-184">As mentioned previously, gradient stops of a linear gradient brush are positioned along a line, the gradient axis.</span></span> <span data-ttu-id="adb95-185">Você pode especificar a orientação e o tamanho da linha usando os campos **StartPoint** e **Endpoint** da estrutura [**de \_ \_ Propriedades do \_ pincel \_ de gradiente linear d2d1**](/windows/win32/api/d2d1/ns-d2d1-d2d1_linear_gradient_brush_properties) ao criar um pincel de gradiente linear.</span><span class="sxs-lookup"><span data-stu-id="adb95-185">You can specify the orientation and size of the line using the **startPoint** and **endPoint** fields of the [**D2D1\_LINEAR\_GRADIENT\_BRUSH\_PROPERTIES**](/windows/win32/api/d2d1/ns-d2d1-d2d1_linear_gradient_brush_properties) structure when you create a linear gradient brush.</span></span> <span data-ttu-id="adb95-186">Depois de criar um pincel, você pode ajustar o eixo de gradiente chamando os métodos [**SetStartPoint**](/windows/win32/api/d2d1/nf-d2d1-id2d1lineargradientbrush-setstartpoint) e [**SetEndPoint**](/windows/win32/api/d2d1/nf-d2d1-id2d1lineargradientbrush-setendpoint) do pincel.</span><span class="sxs-lookup"><span data-stu-id="adb95-186">After you've created a brush, you can adjust the gradient axis by calling the brush's [**SetStartPoint**](/windows/win32/api/d2d1/nf-d2d1-id2d1lineargradientbrush-setstartpoint) and [**SetEndPoint**](/windows/win32/api/d2d1/nf-d2d1-id2d1lineargradientbrush-setendpoint) methods.</span></span> <span data-ttu-id="adb95-187">Ao manipular o ponto de partida e o ponto de extremidade do pincel, você pode criar gradientes horizontais e verticais, reverter a direção do gradiente e muito mais.</span><span class="sxs-lookup"><span data-stu-id="adb95-187">By manipulating the brush's start point and end point, you can create horizontal and vertical gradients, reverse the gradient direction, and more.</span></span>

<span data-ttu-id="adb95-188">Por exemplo, na ilustração a seguir, o ponto inicial é definido como (0, 0) e o ponto de extremidade para (150, 50); Isso cria um gradiente diagonal que começa no canto superior esquerdo e se estende para o canto inferior direito da área que está sendo pintada.</span><span class="sxs-lookup"><span data-stu-id="adb95-188">For example, in the following illustration, the start point is set to (0,0) and the end point to (150, 50); this creates a diagonal gradient that starts at the upper-left corner and extends to the lower-right corner of the area being painted.</span></span> <span data-ttu-id="adb95-189">Quando você define o ponto inicial como (0, 25) e o ponto de extremidade para (150, 25), um gradiente horizontal é criado.</span><span class="sxs-lookup"><span data-stu-id="adb95-189">When you set the start point to (0, 25) and the end point to (150, 25), a horizontal gradient is created.</span></span> <span data-ttu-id="adb95-190">Da mesma forma, definir o ponto de início como (75, 0) e o ponto de extremidade para (75, 50) cria um gradiente vertical.</span><span class="sxs-lookup"><span data-stu-id="adb95-190">Similarly, setting the start point to (75, 0) and the end point to (75, 50) creates a vertical gradient.</span></span> <span data-ttu-id="adb95-191">Definir o ponto de partida para (0, 50) e o ponto de extremidade para (150, 0) cria um gradiente diagonal que começa no canto inferior esquerdo e se estende para o canto superior direito da área que está sendo pintada.</span><span class="sxs-lookup"><span data-stu-id="adb95-191">Setting the start point to (0, 50) and the end point to (150, 0) creates a diagonal gradient that starts at the lower-left corner and extends to the upper-right corner of the area being painted.</span></span>

![ilustração de quatro eixos de gradiente diferentes no mesmo retângulo](images/linear-gradients.png)

## <a name="using-radial-gradient-brushes"></a><span data-ttu-id="adb95-193">Usando pincéis de gradiente radial</span><span class="sxs-lookup"><span data-stu-id="adb95-193">Using radial gradient brushes</span></span>

<span data-ttu-id="adb95-194">Ao contrário de um [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush), que combina duas ou mais cores ao longo de um eixo de gradiente, um [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) pinta uma área com um gradiente radial que mistura duas ou mais cores em uma elipse.</span><span class="sxs-lookup"><span data-stu-id="adb95-194">Unlike an [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush), which blends two or more colors along a gradient axis, an [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) paints an area with a radial gradient that blends two or more colors across an ellipse.</span></span> <span data-ttu-id="adb95-195">Enquanto um **ID2D1LinearGradientBrush** define seu eixo de gradiente com um ponto inicial e um ponto de extremidade, um **ID2D1RadialGradientBrush** define sua elipse de gradiente especificando um centro, um raios horizontais e verticais e um deslocamento de origem de gradiente.</span><span class="sxs-lookup"><span data-stu-id="adb95-195">While a **ID2D1LinearGradientBrush** defines its gradient axis with a start point and an end point, a **ID2D1RadialGradientBrush** defines its gradient ellipse by specifying a center, horizontal and vertical radii, and a gradient origin offset.</span></span>

<span data-ttu-id="adb95-196">Como um [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush), um [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) usa um [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) para especificar as cores e as posições no gradiente.</span><span class="sxs-lookup"><span data-stu-id="adb95-196">Like an [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush), an [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) uses an [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) to specify the colors and positions in the gradient.</span></span>

<span data-ttu-id="adb95-197">A ilustração a seguir mostra um círculo pintado com um [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush).</span><span class="sxs-lookup"><span data-stu-id="adb95-197">The following illustration shows a circle painted with an [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush).</span></span> <span data-ttu-id="adb95-198">O círculo tem duas interrupções de gradiente: a primeira especifica uma cor predefinida "amarelo" em uma posição de 0,0 e a segunda especifica uma cor predefinida "ForestGreen" em uma posição de 1,0.</span><span class="sxs-lookup"><span data-stu-id="adb95-198">The circle has two gradient stops: the first specifies a predefined color "Yellow" at a position of 0.0, and the second specifies a predefined color "ForestGreen" at a position of 1.0.</span></span> <span data-ttu-id="adb95-199">O gradiente tem um centro de (75, 75), um deslocamento de origem de gradiente de (0, 0) e um raio x e y de 75.</span><span class="sxs-lookup"><span data-stu-id="adb95-199">The gradient has a center of (75, 75), a gradient origin offset of (0, 0), and an x- and y-radius of 75.</span></span>

![ilustração de um círculo pintado com um pincel de gradiente radial](images/brushes-ovw-radials.png)

<span data-ttu-id="adb95-201">Os exemplos de código a seguir mostram como pintar este círculo com um [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) que tem duas paradas de cor: "amarelo" em uma posição de 0,0 e "ForestGreen" em uma posição de 1,0.</span><span class="sxs-lookup"><span data-stu-id="adb95-201">The following code examples shows how to paint this circle with an [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) that has two color stops: "Yellow" at a position of 0.0, and "ForestGreen" at a position of 1.0.</span></span> <span data-ttu-id="adb95-202">Semelhante à criação de um [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush), o exemplo chama [**CreateGradientStopCollection**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-creategradientstopcollection(constd2d1_gradient_stop_uint32_d2d1_gamma_d2d1_extend_mode_id2d1gradientstopcollection)) para criar um [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) de uma matriz de interrupções de gradiente.</span><span class="sxs-lookup"><span data-stu-id="adb95-202">Similar to creating an [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush), the example calls [**CreateGradientStopCollection**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-creategradientstopcollection(constd2d1_gradient_stop_uint32_d2d1_gamma_d2d1_extend_mode_id2d1gradientstopcollection)) to create an [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) from an array of gradient stops.</span></span>


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



<span data-ttu-id="adb95-203">Para criar um [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush), use o método [**ID2D1RenderTarget:: CreateRadialGradientBrush**](/windows/win32/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createradialgradientbrush) .</span><span class="sxs-lookup"><span data-stu-id="adb95-203">To create an [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush), use the [**ID2D1RenderTarget::CreateRadialGradientBrush**](/windows/win32/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createradialgradientbrush) method.</span></span> <span data-ttu-id="adb95-204">O **CreateRadialGradientBrush** usa três parâmetros.</span><span class="sxs-lookup"><span data-stu-id="adb95-204">The **CreateRadialGradientBrush** takes three parameters.</span></span> <span data-ttu-id="adb95-205">O primeiro parâmetro, uma [**\_ propriedade de \_ \_ pincel de \_ gradiente radial d2d1**](/windows/win32/api/d2d1/ns-d2d1-d2d1_radial_gradient_brush_properties) especifica o centro, o deslocamento da origem do gradiente e o raios horizontal e vertical do gradiente.</span><span class="sxs-lookup"><span data-stu-id="adb95-205">The first parameter, a [**D2D1\_RADIAL\_GRADIENT\_BRUSH\_PROPERTIES**](/windows/win32/api/d2d1/ns-d2d1-d2d1_radial_gradient_brush_properties) specifies the center, gradient origin offset, and the horizontal and vertical radii of the gradient.</span></span> <span data-ttu-id="adb95-206">O segundo parâmetro é um [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) que descreve as cores e suas posições no gradiente, e o terceiro parâmetro é o endereço do ponteiro que recebe a nova referência **ID2D1RadialGradientBrush** .</span><span class="sxs-lookup"><span data-stu-id="adb95-206">The second parameter is an [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) that describes the colors and their positions in the gradient, and the third parameter is the address of the pointer that receive the new **ID2D1RadialGradientBrush** reference.</span></span> <span data-ttu-id="adb95-207">Algumas sobrecargas usam um parâmetro adicional, uma estrutura de [**\_ \_ Propriedades de pincel d2d1**](/windows/win32/api/d2d1/ns-d2d1-d2d1_brush_properties) que especifica um valor de opacidade e uma transformação a ser aplicada ao novo pincel.</span><span class="sxs-lookup"><span data-stu-id="adb95-207">Some overloads take an additional parameter, a [**D2D1\_BRUSH\_PROPERTIES**](/windows/win32/api/d2d1/ns-d2d1-d2d1_brush_properties) structure that specifies an opacity value and a transform to apply to the new brush.</span></span>

<span data-ttu-id="adb95-208">O exemplo a seguir chama [**CreateRadialGradientBrush**](/windows/win32/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createradialgradientbrush), passando a matriz de interrupções de gradiente e as propriedades de pincel de gradiente radial que têm o valor *Center* definido como (75, 75), *gradientOriginOffset* definido como (0, 0) e *RadiusX* e *RADIUS* definidos como 75.</span><span class="sxs-lookup"><span data-stu-id="adb95-208">The next example calls [**CreateRadialGradientBrush**](/windows/win32/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createradialgradientbrush), passing in the array of gradient stops, and the radial gradient brush properties that have the *center* value set to (75, 75), the *gradientOriginOffset* set to (0, 0), and *radiusX* and *radiusY* both set to 75.</span></span>


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



<span data-ttu-id="adb95-209">O exemplo final usa o pincel para preencher uma elipse.</span><span class="sxs-lookup"><span data-stu-id="adb95-209">The final example uses the brush to fill an ellipse.</span></span>


```C++
m_pRenderTarget->FillEllipse(ellipse, m_pRadialGradientBrush);
m_pRenderTarget->DrawEllipse(ellipse, m_pBlackBrush, 1, NULL);
```



### <a name="configuring-a-radial-gradient"></a><span data-ttu-id="adb95-210">Configurando um gradiente radial</span><span class="sxs-lookup"><span data-stu-id="adb95-210">Configuring a radial gradient</span></span>

<span data-ttu-id="adb95-211">Valores diferentes para *Center*, *gradientOriginOffset*, *RadiusX* e/ou *RADIUS* produzem gradientes diferentes.</span><span class="sxs-lookup"><span data-stu-id="adb95-211">Different values for *center*, *gradientOriginOffset*, *radiusX* and/or *radiusY* produce different gradients.</span></span> <span data-ttu-id="adb95-212">A ilustração a seguir mostra vários gradientes radiais que têm deslocamentos de origem de gradiente diferentes, criando a aparência da luz iluminando os círculos de diferentes ângulos.</span><span class="sxs-lookup"><span data-stu-id="adb95-212">The following illustration shows several radial gradients that have different gradient origin offsets, creating the appearance of the light illuminating the circles from different angles.</span></span>

![ilustração do mesmo círculo pintado com pincéis de gradiente radial com deslocamentos de origem diferentes](images/radialgradient.png)

## <a name="using-bitmap-brushes"></a><span data-ttu-id="adb95-214">Usando pincéis de bitmap</span><span class="sxs-lookup"><span data-stu-id="adb95-214">Using bitmap brushes</span></span>

<span data-ttu-id="adb95-215">Um [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) pinta uma área com um bitmap (representado por um objeto [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) ).</span><span class="sxs-lookup"><span data-stu-id="adb95-215">An [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) paints an area with a bitmap (represented by an [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) object).</span></span>

<span data-ttu-id="adb95-216">A ilustração a seguir mostra um quadrado pintado com um bitmap de uma planta.</span><span class="sxs-lookup"><span data-stu-id="adb95-216">The following illustration shows a square painted with a bitmap of a plant.</span></span>

![ilustração de um bitmap quadrado pintado com a planta](images/brushes-ovw-bitmap.png)

<span data-ttu-id="adb95-218">Os exemplos a seguir mostram como pintar esse quadrado com um [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush).</span><span class="sxs-lookup"><span data-stu-id="adb95-218">The examples that follow shows how to paint this square with an [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush).</span></span>

<span data-ttu-id="adb95-219">O primeiro exemplo inicializa um [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) para uso com o pincel.</span><span class="sxs-lookup"><span data-stu-id="adb95-219">The first example initializes an [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) for use with the brush.</span></span> <span data-ttu-id="adb95-220">O **ID2D1Bitmap** é fornecido por um método auxiliar, LoadResourceBitmap, definido em outro lugar no exemplo.</span><span class="sxs-lookup"><span data-stu-id="adb95-220">The **ID2D1Bitmap** is provided by a helper method, LoadResourceBitmap, defined elsewhere in the sample.</span></span>


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



<span data-ttu-id="adb95-221">Para criar o pincel de bitmap, chame o método [**ID2D1RenderTarget:: CreateBitmapBrush**](id2d1rendertarget-createbitmapbrush.md) e especifique o [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) com o qual pintar.</span><span class="sxs-lookup"><span data-stu-id="adb95-221">To create the bitmap brush, call the [**ID2D1RenderTarget::CreateBitmapBrush**](id2d1rendertarget-createbitmapbrush.md) method and specify the [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) with which to paint.</span></span> <span data-ttu-id="adb95-222">O método retorna um **HRESULT** e um objeto [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) .</span><span class="sxs-lookup"><span data-stu-id="adb95-222">The method returns an **HRESULT** and an [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) object.</span></span> <span data-ttu-id="adb95-223">Algumas sobrecargas **CreateBitmapBrush** permitem que você especifique opções adicionais aceitando [**\_ \_ as propriedades de um pincel d2d1**](/windows/win32/api/d2d1/ns-d2d1-d2d1_brush_properties) e uma estrutura de [**\_ \_ \_ Propriedades de pincel de bitmap d2d1**](/windows/win32/api/d2d1/ns-d2d1-d2d1_bitmap_brush_properties) .</span><span class="sxs-lookup"><span data-stu-id="adb95-223">Some **CreateBitmapBrush** overloads enable you to specify additional options by accepting a [**D2D1\_BRUSH\_PROPERTIES**](/windows/win32/api/d2d1/ns-d2d1-d2d1_brush_properties) and a [**D2D1\_BITMAP\_BRUSH\_PROPERTIES**](/windows/win32/api/d2d1/ns-d2d1-d2d1_bitmap_brush_properties) structure.</span></span>


```C++
if (SUCCEEDED(hr))
{
    hr = m_pRenderTarget->CreateBitmapBrush(
        m_pBitmap,
        &m_pBitmapBrush
        );
}
```



<span data-ttu-id="adb95-224">O exemplo a seguir usa o pincel para preencher um retângulo.</span><span class="sxs-lookup"><span data-stu-id="adb95-224">The next example uses the brush to fill a rectangle.</span></span>


```C++
m_pRenderTarget->FillRectangle(&rcBrushRect, m_pBitmapBrush);
```



## <a name="configuring-extend-modes"></a><span data-ttu-id="adb95-225">Configurando modos de extensão</span><span class="sxs-lookup"><span data-stu-id="adb95-225">Configuring extend modes</span></span>

<span data-ttu-id="adb95-226">Às vezes, o gradiente de um pincel de gradiente ou o bitmap para um pincel de bitmap não preenche completamente a área que está sendo pintada.</span><span class="sxs-lookup"><span data-stu-id="adb95-226">Sometimes, the gradient of a gradient brush or the bitmap for a bitmap brush doesn't completely fill the area being painted.</span></span>

-   <span data-ttu-id="adb95-227">Quando isso acontece para um [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush), o Direct2D usa as configurações do modo de extensão horizontal ([**SetExtendModeX**](/windows/win32/api/d2d1/nf-d2d1-id2d1bitmapbrush-setextendmodex)) e vertical ([**SetExtendModeY**](/windows/win32/api/d2d1/nf-d2d1-id2d1bitmapbrush-setextendmodey)) do pincel para determinar como preencher a área restante.</span><span class="sxs-lookup"><span data-stu-id="adb95-227">When this happens for an [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush), Direct2D uses the brush's horizontal ([**SetExtendModeX**](/windows/win32/api/d2d1/nf-d2d1-id2d1bitmapbrush-setextendmodex)) and vertical ([**SetExtendModeY**](/windows/win32/api/d2d1/nf-d2d1-id2d1bitmapbrush-setextendmodey)) extend mode settings to determine how to fill the remaining area.</span></span>

-   <span data-ttu-id="adb95-228">Quando isso acontece com um pincel de gradiente, Direct2D determina como preencher a área restante usando o valor do parâmetro [**de \_ \_ modo estendido d2d1**](/windows/win32/api/d2d1/ne-d2d1-d2d1_extend_mode) que você especificou quando chamou o [**CreateGradientStopCollection**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-creategradientstopcollection(constd2d1_gradient_stop_uint32_d2d1_gamma_d2d1_extend_mode_id2d1gradientstopcollection)) para criar a [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection)do pincel de gradiente.</span><span class="sxs-lookup"><span data-stu-id="adb95-228">When this happens for a gradient brush, Direct2D determines how to fill the remaining area by using the value of the [**D2D1\_EXTEND\_MODE**](/windows/win32/api/d2d1/ne-d2d1-d2d1_extend_mode) parameter that you specified when you called the [**CreateGradientStopCollection**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-creategradientstopcollection(constd2d1_gradient_stop_uint32_d2d1_gamma_d2d1_extend_mode_id2d1gradientstopcollection)) to create the gradient brush's [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection).</span></span>

<span data-ttu-id="adb95-229">A ilustração a seguir mostra os resultados de cada combinação possível dos modos de extensão para um [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush): [**d2d1 \_ Extend \_ mode \_ fixe**](/windows/win32/api/d2d1/ne-d2d1-d2d1_extend_mode) (fixe), **d2d1 \_ estender \_ modo \_ encapsulamento** (Wrap) e **d2d1 \_ estender \_ espelho** (espelho).</span><span class="sxs-lookup"><span data-stu-id="adb95-229">The following illustration shows the results from every possible combination of the extend modes for an [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush): [**D2D1\_EXTEND\_MODE\_CLAMP**](/windows/win32/api/d2d1/ne-d2d1-d2d1_extend_mode) (CLAMP), **D2D1\_EXTEND\_MODE\_WRAP** (WRAP), and **D2D1\_EXTEND\_MIRROR** (MIRROR).</span></span>

![ilustração de uma imagem original e as imagens resultantes de vários modos de extensão](images/bitmapwrap-clamp-mirror.png)

<span data-ttu-id="adb95-231">O exemplo a seguir mostra como definir os modos x-e y de extensão do pincel de bitmap para [**d2d1 \_ estender \_ espelho**](/windows/win32/api/d2d1/ne-d2d1-d2d1_extend_mode).</span><span class="sxs-lookup"><span data-stu-id="adb95-231">The following example shows how to set the bitmap brush's x- and y-extend modes to [**D2D1\_EXTEND\_MIRROR**](/windows/win32/api/d2d1/ne-d2d1-d2d1_extend_mode).</span></span> <span data-ttu-id="adb95-232">Em seguida, ele pinta o retângulo com o [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush).</span><span class="sxs-lookup"><span data-stu-id="adb95-232">It then paints the rectangle with the [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush).</span></span>


```C++
m_pBitmapBrush->SetExtendModeX(D2D1_EXTEND_MODE_MIRROR);
m_pBitmapBrush->SetExtendModeY(D2D1_EXTEND_MODE_MIRROR);

m_pRenderTarget->FillRectangle(exampleRectangle, m_pBitmapBrush);
```



<span data-ttu-id="adb95-233">Ele produz a saída conforme mostrado na ilustração a seguir.</span><span class="sxs-lookup"><span data-stu-id="adb95-233">It produces output as shown in the following illustration.</span></span>

![ilustração de uma imagem original e a imagem resultante após o espelhamento da direção x e da direção y](images/brushes-ovw-bitmapmirrormirror.png)

## <a name="transforming-brushes"></a><span data-ttu-id="adb95-235">Transformando pincéis</span><span class="sxs-lookup"><span data-stu-id="adb95-235">Transforming brushes</span></span>

<span data-ttu-id="adb95-236">Quando você pinta com um pincel, ele pinta no espaço de coordenadas do destino de renderização.</span><span class="sxs-lookup"><span data-stu-id="adb95-236">When you paint with a brush, it paints in the coordinate space of the render target.</span></span> <span data-ttu-id="adb95-237">Os pincéis não se posicionam automaticamente para se alinharem com o objeto que está sendo pintado; Por padrão, eles começam a pintar na origem (0, 0) do destino de renderização.</span><span class="sxs-lookup"><span data-stu-id="adb95-237">Brushes do not automatically position themselves to align with the object being painted; by default, they begin painting at the origin (0, 0) of the render target.</span></span>

<span data-ttu-id="adb95-238">Você pode "mover" o gradiente definido por um [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) para uma área de destino definindo seu ponto de partida e ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="adb95-238">You can "move" the gradient defined by an [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) to a target area by setting its start point and end point.</span></span> <span data-ttu-id="adb95-239">Da mesma forma, você pode mover o gradiente definido por um [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) alterando seu centro e raios.</span><span class="sxs-lookup"><span data-stu-id="adb95-239">Likewise, you can move the gradient defined by an [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) by changing its center and radii.</span></span>

<span data-ttu-id="adb95-240">Para alinhar o conteúdo de um [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) à área que está sendo pintada, você pode usar o método [**SetTransform**](/windows/win32/api/d2d1/nf-d2d1-id2d1brush-settransform(constd2d1_matrix_3x2_f)) para converter o bitmap no local desejado.</span><span class="sxs-lookup"><span data-stu-id="adb95-240">To align the content of an [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) to the area being painted, you can use the [**SetTransform**](/windows/win32/api/d2d1/nf-d2d1-id2d1brush-settransform(constd2d1_matrix_3x2_f)) method to translate the bitmap to the desired location.</span></span> <span data-ttu-id="adb95-241">Essa transformação afeta apenas o pincel; Ele não afeta nenhum outro conteúdo desenhado pelo destino de renderização.</span><span class="sxs-lookup"><span data-stu-id="adb95-241">This transform only affects the brush; it does not affect any other content drawn by the render target.</span></span>

<span data-ttu-id="adb95-242">A ilustração a seguir mostra o efeito de usar um [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) para preencher um retângulo localizado em (100, 100).</span><span class="sxs-lookup"><span data-stu-id="adb95-242">The following illustrations shows the effect of using an [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) to fill a rectangle located at (100, 100).</span></span> <span data-ttu-id="adb95-243">A ilustração na ilustração à esquerda mostra o resultado do preenchimento do retângulo sem transformar o pincel: o bitmap é desenhado na origem do destino do processamento.</span><span class="sxs-lookup"><span data-stu-id="adb95-243">The illustration on the left illustration shows the result of filling the rectangle without transforming the brush: the bitmap is drawn at the render target's origin.</span></span> <span data-ttu-id="adb95-244">Como resultado, apenas uma parte do bitmap é exibida no retângulo.</span><span class="sxs-lookup"><span data-stu-id="adb95-244">As a result, only a portion of the bitmap appears in the rectangle.</span></span> <span data-ttu-id="adb95-245">A ilustração à direita mostra o resultado da transformação do **ID2D1BitmapBrush** para que seu conteúdo seja deslocado 50 pixels para a direita e 50 pixels para baixo.</span><span class="sxs-lookup"><span data-stu-id="adb95-245">The illustration on the right shows the result of transforming the **ID2D1BitmapBrush** so that its content is shifted 50 pixels to the right and 50 pixels down.</span></span> <span data-ttu-id="adb95-246">O bitmap agora preenche o retângulo.</span><span class="sxs-lookup"><span data-stu-id="adb95-246">The bitmap now fills the rectangle.</span></span>

![ilustração de um quadrado pintado com um pincel de bitmap sem transformar o pincel e transformando o pincel](images/brushes-ovw-transform.png)

<span data-ttu-id="adb95-248">O código a seguir mostra como fazer isso.</span><span class="sxs-lookup"><span data-stu-id="adb95-248">The following code shows how to accomplish this.</span></span> <span data-ttu-id="adb95-249">Primeiro, aplique uma tradução ao [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush), movendo o pincel 50 pixels para o eixo x e 50 pixels para baixo ao longo do eixo y.</span><span class="sxs-lookup"><span data-stu-id="adb95-249">First apply a translation to the [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush), moving the brush 50 pixels right along the x-axis and 50 pixels down along the y-axis.</span></span> <span data-ttu-id="adb95-250">Em seguida, use o **ID2D1BitmapBrush** para preencher o retângulo que tem o canto superior esquerdo em (100, 100) e no canto inferior direito em (200, 200).</span><span class="sxs-lookup"><span data-stu-id="adb95-250">Then use the **ID2D1BitmapBrush** to fill the rectangle that has the upper-left corner at (100, 100) and the lower-right corner at (200, 200).</span></span>


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

## <a name="related-topics"></a><span data-ttu-id="adb95-251">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="adb95-251">Related topics</span></span>

* [<span data-ttu-id="adb95-252">Referência de Direct2D</span><span class="sxs-lookup"><span data-stu-id="adb95-252">Direct2D reference</span></span>](reference.md)
* [<span data-ttu-id="adb95-253">Como criar um pincel de cor sólida</span><span class="sxs-lookup"><span data-stu-id="adb95-253">How to create a solid color brush</span></span>](how-to-create-a-solid-color-brush.md)
* [<span data-ttu-id="adb95-254">Como criar um pincel de gradiente linear</span><span class="sxs-lookup"><span data-stu-id="adb95-254">How to create a linear gradient brush</span></span>](how-to-create-a-linear-gradient-brush.md)
* [<span data-ttu-id="adb95-255">Como criar um pincel gradiente radial</span><span class="sxs-lookup"><span data-stu-id="adb95-255">How to create a radial gradient brush</span></span>](how-to-create-a-radial-gradient-brush.md)
* [<span data-ttu-id="adb95-256">Como criar um pincel de bitmap</span><span class="sxs-lookup"><span data-stu-id="adb95-256">How to create a bitmap brush</span></span>](how-to-create-a-bitmap-brush.md)
