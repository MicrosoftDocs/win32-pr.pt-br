---
description: Este tópico descreve como usar diferentes tipos de pincéis em um OM XPS.
ms.assetid: 392ca1d5-283e-4eed-ae21-6477c469014d
title: Pincéis de OM XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0557757bfaf81156b2015525d35897cfb042e44b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105782969"
---
# <a name="xps-om-brushes"></a><span data-ttu-id="d1f02-103">Pincéis de OM XPS</span><span class="sxs-lookup"><span data-stu-id="d1f02-103">XPS OM Brushes</span></span>

<span data-ttu-id="d1f02-104">Este tópico descreve como usar diferentes tipos de pincéis em um OM XPS.</span><span class="sxs-lookup"><span data-stu-id="d1f02-104">This topic describes how to use different types of brushes in an XPS OM.</span></span>

<span data-ttu-id="d1f02-105">Os pincéis no OM XPS são baseados na [**interface IXpsOMBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsombrush) e incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="d1f02-105">The brushes in the XPS OM are based on the [**IXpsOMBrush Interface**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsombrush) and include the following:</span></span>

<dl> <span data-ttu-id="d1f02-106">Pincéis de bloco</span><span class="sxs-lookup"><span data-stu-id="d1f02-106">Tile Brushes</span></span>

-   [<span data-ttu-id="d1f02-107">**Interface IXpsOMTileBrush**</span><span class="sxs-lookup"><span data-stu-id="d1f02-107">**IXpsOMTileBrush Interface**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomtilebrush)
-   [<span data-ttu-id="d1f02-108">**Interface IXpsOMSolidColorBrush**</span><span class="sxs-lookup"><span data-stu-id="d1f02-108">**IXpsOMSolidColorBrush Interface**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomsolidcolorbrush)
-   [<span data-ttu-id="d1f02-109">**Interface IXpsOMVisualBrush**</span><span class="sxs-lookup"><span data-stu-id="d1f02-109">**IXpsOMVisualBrush Interface**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualbrush)
-   [<span data-ttu-id="d1f02-110">**Interface IXpsOMImageBrush**</span><span class="sxs-lookup"><span data-stu-id="d1f02-110">**IXpsOMImageBrush Interface**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomimagebrush)

  
<span data-ttu-id="d1f02-111">Pincéis de Gradiente</span><span class="sxs-lookup"><span data-stu-id="d1f02-111">Gradient Brushes</span></span>

-   [<span data-ttu-id="d1f02-112">**Interface IXpsOMGradientBrush**</span><span class="sxs-lookup"><span data-stu-id="d1f02-112">**IXpsOMGradientBrush Interface**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgradientbrush)
-   [<span data-ttu-id="d1f02-113">**Interface IXpsOMLinearGradientBrush**</span><span class="sxs-lookup"><span data-stu-id="d1f02-113">**IXpsOMLinearGradientBrush Interface**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomlineargradientbrush)
-   [<span data-ttu-id="d1f02-114">**Interface IXpsOMRadialGradientBrush**</span><span class="sxs-lookup"><span data-stu-id="d1f02-114">**IXpsOMRadialGradientBrush Interface**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomradialgradientbrush)

  
</dl>

## <a name="code-examples"></a><span data-ttu-id="d1f02-115">Exemplos de código</span><span class="sxs-lookup"><span data-stu-id="d1f02-115">Code Examples</span></span>

### <a name="create-a-solid-color-brush"></a><span data-ttu-id="d1f02-116">Criar um pincel de cor sólida</span><span class="sxs-lookup"><span data-stu-id="d1f02-116">Create a solid-color brush</span></span>

<span data-ttu-id="d1f02-117">O exemplo de código a seguir cria um pincel de cor sólida a partir de um valor de cor que é definido no código.</span><span class="sxs-lookup"><span data-stu-id="d1f02-117">The following code example creates a solid-color brush from a color value that is defined in the code.</span></span>


```C++
    HRESULT                hr = S_OK;

    XPS_COLOR              xpsColor;
    IXpsOMSolidColorBrush  *brush;

    // creates a solid red brush
    xpsColor.colorType = XPS_COLOR_TYPE_SRGB;
    xpsColor.value.sRGB.alpha = 0xFF;
    xpsColor.value.sRGB.red = 0xFF;
    xpsColor.value.sRGB.green = 0x00;
    xpsColor.value.sRGB.blue = 0x00;

    hr = xpsFactory->CreateSolidColorBrush(
       &xpsColor, 
       NULL, 
       reinterpret_cast<IXpsOMSolidColorBrush**>(&brush));
    
    // use brush

    // when finished with brush, release pointer
    brush->Release();
```



### <a name="create-a-visual-brush"></a><span data-ttu-id="d1f02-118">Criar um pincel Visual</span><span class="sxs-lookup"><span data-stu-id="d1f02-118">Create a visual brush</span></span>

<span data-ttu-id="d1f02-119">O exemplo de código a seguir cria um pincel a partir de um objeto visual.</span><span class="sxs-lookup"><span data-stu-id="d1f02-119">The following code example creates a brush from a visual object.</span></span>


```C++
    HRESULT                       hr = S_OK;
    IXpsOMVisualBrush             *brush;

    XPS_RECT viewBoxRect = {0,0,0,0};
    XPS_RECT viewPortRect = {0,0,0,0};

    // set viewBoxRect to define the portion of the visual to use
    // as the brush.
    //
    // set viewPortRect to define the location and size of the 
    // the brush in the destination 
    //
    // create the brush
    hr = xpsFactory->CreateVisualBrush (
        &viewBoxRect,
        &viewPortRect,
        reinterpret_cast<IXpsOMVisualBrush**>(&brush));

    // assign the visual object
    //   brushVisual points to a visual
    //   that is defined outside of this example

    hr = brush->SetVisualLocal (brushVisual);
    
    // use brush
    
    // when finished with brush, release pointer
    brush->Release();
    
```



### <a name="create-an-image-brush"></a><span data-ttu-id="d1f02-120">Criar um pincel de imagem</span><span class="sxs-lookup"><span data-stu-id="d1f02-120">Create an image brush</span></span>

<span data-ttu-id="d1f02-121">Consulte o exemplo de código no [local imagens em um om XPS](place-images-in-an-xps-om.md).</span><span class="sxs-lookup"><span data-stu-id="d1f02-121">Refer to the code example in [Place Images in an XPS OM](place-images-in-an-xps-om.md).</span></span>

### <a name="create-a-linear-gradient-brush"></a><span data-ttu-id="d1f02-122">Criar um pincel de gradiente linear</span><span class="sxs-lookup"><span data-stu-id="d1f02-122">Create a linear-gradient brush</span></span>

<span data-ttu-id="d1f02-123">O exemplo de código a seguir cria um pincel de gradiente linear.</span><span class="sxs-lookup"><span data-stu-id="d1f02-123">The following code example creates a linear-gradient brush.</span></span> <span data-ttu-id="d1f02-124">O gradiente tem duas paradas de gradiente.</span><span class="sxs-lookup"><span data-stu-id="d1f02-124">The gradient has two gradient stops.</span></span>


```C++
    HRESULT                       hr = S_OK;
    XPS_COLOR                     xpsColorStop;
    IXpsOMGradientStop            *xpsGradientStop1, *xpsGradientStop2;
    IXpsOMLinearGradientBrush     *brush;
    XPS_POINT                     startPoint, endPoint;

    // define the start color
    xpsColorStop.colorType        = XPS_COLOR_TYPE_SRGB;
    xpsColorStop.value.sRGB.alpha = 0xFF;
    xpsColorStop.value.sRGB.red   = 0xE4;
    xpsColorStop.value.sRGB.green = 0x3B;
    xpsColorStop.value.sRGB.blue  = 0x2F;
    
    // create a gradient stop by setting the color and location 
    // for the beginning of the gradient
    hr = xpsFactory->CreateGradientStop(
        &xpsColorStop, 
        NULL, 
        0.0f,
        &xpsGradientStop1);
    startPoint.x = 375.75f;
    startPoint.y = 18.0f;

    // define the end color
    xpsColorStop.colorType        = XPS_COLOR_TYPE_SRGB;
    xpsColorStop.value.sRGB.alpha = 0xFF;
    xpsColorStop.value.sRGB.red   = 0xEF;
    xpsColorStop.value.sRGB.green = 0x79;
    xpsColorStop.value.sRGB.blue  = 0x2F;

    // create a gradient stop by setting the color and  location
    //  for the end of the gradient
    hr = xpsFactory->CreateGradientStop(
        &xpsColorStop,
        NULL, 
        1.0f, 
        &xpsGradientStop2);
    endPoint.x   = 375.75f;
    endPoint.y   = 134.6f;

    // create the brush
    hr = xpsFactory->CreateLinearGradientBrush(
        xpsGradientStop1, 
        xpsGradientStop2, 
        &startPoint, 
        &endPoint, 
        &brush);
    // release gradient stops after creating brush
    xpsGradientStop1->Release();
    xpsGradientStop2->Release();

    // when finished with brush, release pointer to brush
    brush->Release();
```



## <a name="related-topics"></a><span data-ttu-id="d1f02-125">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d1f02-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d1f02-126">**Interface IXpsOMGradientBrush**</span><span class="sxs-lookup"><span data-stu-id="d1f02-126">**IXpsOMGradientBrush Interface**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgradientbrush)
</dt> <dt>

[<span data-ttu-id="d1f02-127">**Interface IXpsOMImageBrush**</span><span class="sxs-lookup"><span data-stu-id="d1f02-127">**IXpsOMImageBrush Interface**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomimagebrush)
</dt> <dt>

[<span data-ttu-id="d1f02-128">**Interface IXpsOMLinearGradientBrush**</span><span class="sxs-lookup"><span data-stu-id="d1f02-128">**IXpsOMLinearGradientBrush Interface**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomlineargradientbrush)
</dt> <dt>

[<span data-ttu-id="d1f02-129">**Interface IXpsOMRadialGradientBrush**</span><span class="sxs-lookup"><span data-stu-id="d1f02-129">**IXpsOMRadialGradientBrush Interface**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomradialgradientbrush)
</dt> <dt>

[<span data-ttu-id="d1f02-130">**Interface IXpsOMSolidColorBrush**</span><span class="sxs-lookup"><span data-stu-id="d1f02-130">**IXpsOMSolidColorBrush Interface**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomsolidcolorbrush)
</dt> <dt>

[<span data-ttu-id="d1f02-131">**Interface IXpsOMTileBrush**</span><span class="sxs-lookup"><span data-stu-id="d1f02-131">**IXpsOMTileBrush Interface**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomtilebrush)
</dt> <dt>

[<span data-ttu-id="d1f02-132">**Interface IXpsOMVisualBrush**</span><span class="sxs-lookup"><span data-stu-id="d1f02-132">**IXpsOMVisualBrush Interface**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualbrush)
</dt> <dt>

[<span data-ttu-id="d1f02-133">**cor do XPS \_**</span><span class="sxs-lookup"><span data-stu-id="d1f02-133">**XPS\_COLOR**</span></span>](xps-color.md)
</dt> <dt>

[<span data-ttu-id="d1f02-134">Especificação de Papel XML</span><span class="sxs-lookup"><span data-stu-id="d1f02-134">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 



