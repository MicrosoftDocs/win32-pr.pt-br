---
title: Como desenhar e preencher uma forma básica
description: Este tópico descreve como desenhar uma forma básica.
ms.assetid: 8a68fc3f-118c-447b-856c-05417ae4ef29
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 93d8f3a3ddeb06c9168971789dff3ac8c9222d22
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/09/2021
ms.locfileid: "111826995"
---
# <a name="how-to-draw-and-fill-a-basic-shape"></a><span data-ttu-id="b5523-103">Como desenhar e preencher uma forma básica</span><span class="sxs-lookup"><span data-stu-id="b5523-103">How to Draw and Fill a Basic Shape</span></span>

<span data-ttu-id="b5523-104">Este tópico descreve como desenhar uma forma básica.</span><span class="sxs-lookup"><span data-stu-id="b5523-104">This topic describes how to draw a basic shape.</span></span> <span data-ttu-id="b5523-105">A interface [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) fornece métodos para delinear e preencher re elipses, retângulos e linhas.</span><span class="sxs-lookup"><span data-stu-id="b5523-105">The [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) interface provides methods for outlining and filling ellipses, rectangles, and lines.</span></span> <span data-ttu-id="b5523-106">Os exemplos a seguir mostram como criar e desenhar uma elipse.</span><span class="sxs-lookup"><span data-stu-id="b5523-106">The following examples show how to create and draw an ellipse.</span></span>

<span data-ttu-id="b5523-107">Este tópico contém as seguintes seções:</span><span class="sxs-lookup"><span data-stu-id="b5523-107">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="b5523-108">Desenhar o contorno de uma elipse com um traço sólido</span><span class="sxs-lookup"><span data-stu-id="b5523-108">Draw the Outline of an Ellipse with a Solid Stroke</span></span>](#draw-the-outline-of-an-ellipse-with-a-solid-stroke)
-   [<span data-ttu-id="b5523-109">Desenhar uma elipse com um traço tracejado</span><span class="sxs-lookup"><span data-stu-id="b5523-109">Draw an Ellipse with a Dashed Stroke</span></span>](#draw-an-ellipse-with-a-dashed-stroke)
-   [<span data-ttu-id="b5523-110">Desenhar e preencher uma elipse</span><span class="sxs-lookup"><span data-stu-id="b5523-110">Draw and Fill an Ellipse</span></span>](#draw-and-fill-an-ellipse)
-   [<span data-ttu-id="b5523-111">Desenhando formas mais complexas</span><span class="sxs-lookup"><span data-stu-id="b5523-111">Drawing More Complex Shapes</span></span>](#drawing-more-complex-shapes)
-   [<span data-ttu-id="b5523-112">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b5523-112">Related topics</span></span>](#related-topics)

## <a name="draw-the-outline-of-an-ellipse-with-a-solid-stroke"></a><span data-ttu-id="b5523-113">Desenhar o contorno de uma elipse com um traço sólido</span><span class="sxs-lookup"><span data-stu-id="b5523-113">Draw the Outline of an Ellipse with a Solid Stroke</span></span>

<span data-ttu-id="b5523-114">Para desenhar o contorno de uma elipse, defina um pincel (como [**uma ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) ou [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush)) para pintar o contorno e uma [**\_ ELLIPSE D2D1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_ellipse) para descrever a posição e as dimensões da elipse e, em seguida, passar esses objetos para o método [**ID2D1RenderTarget::D rawEllipse.**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-drawellipse(constd2d1_ellipse__id2d1brush_float_id2d1strokestyle))</span><span class="sxs-lookup"><span data-stu-id="b5523-114">To draw the outline of an ellipse, you define a brush (such as a [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) or [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush)) for painting the outline and a [**D2D1\_ELLIPSE**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_ellipse) for describing the ellipse's position and dimensions, then pass these objects to the [**ID2D1RenderTarget::DrawEllipse**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-drawellipse(constd2d1_ellipse__id2d1brush_float_id2d1strokestyle)) method.</span></span> <span data-ttu-id="b5523-115">O exemplo a seguir cria um pincel de cor sólida preta e o armazena no membro da classe m \_ spBlackBrush.</span><span class="sxs-lookup"><span data-stu-id="b5523-115">The following example creates a black solid color brush and stores it in the m\_spBlackBrush class member.</span></span>


```C++
hr = m_pRenderTarget->CreateSolidColorBrush(
    D2D1::ColorF(D2D1::ColorF::Black),
    &m_pBlackBrush
    );
```



<span data-ttu-id="b5523-116">O exemplo a seguir define uma [**\_ ELLIPSE D2D1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_ellipse) e a usa com o pincel definido no exemplo anterior para desenhar o contorno de uma elipse.</span><span class="sxs-lookup"><span data-stu-id="b5523-116">The next example defines an [**D2D1\_ELLIPSE**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_ellipse) and uses it with the brush defined in the previous example to draw the outline of an ellipse.</span></span> <span data-ttu-id="b5523-117">Este exemplo produz a saída mostrada na ilustração a seguir.</span><span class="sxs-lookup"><span data-stu-id="b5523-117">This example produces the output shown in the following illustration.</span></span>

![ilustração de uma elipse com um traço sólido](images/drawandfillellipseexample-1.png)


```C++
D2D1_ELLIPSE ellipse = D2D1::Ellipse(
    D2D1::Point2F(100.f, 100.f),
    75.f,
    50.f
    );

m_pRenderTarget->DrawEllipse(ellipse, m_pBlackBrush, 10.f);
```



## <a name="draw-an-ellipse-with-a-dashed-stroke"></a><span data-ttu-id="b5523-119">Desenhar uma elipse com um traço tracejado</span><span class="sxs-lookup"><span data-stu-id="b5523-119">Draw an Ellipse with a Dashed Stroke</span></span>

<span data-ttu-id="b5523-120">O exemplo anterior usou um traço simples.</span><span class="sxs-lookup"><span data-stu-id="b5523-120">The preceding example used a plain stroke.</span></span> <span data-ttu-id="b5523-121">Você pode modificar a aparência de um traço de várias maneiras criando [**um ID2D1StroseStyle.**](/windows/win32/api/d2d1/nn-d2d1-id2d1strokestyle)</span><span class="sxs-lookup"><span data-stu-id="b5523-121">You can modify the look of a stroke in several ways by creating an [**ID2D1StrokeStyle**](/windows/win32/api/d2d1/nn-d2d1-id2d1strokestyle).</span></span> <span data-ttu-id="b5523-122">O **ID2D1StrkeStyle** permite especificar a forma no início e no final de um traço, se ele tem um padrão de traço e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="b5523-122">The **ID2D1StrokeStyle** lets you specify the shape at the beginning and end of a stroke, whether it has a dash pattern, and so on.</span></span> <span data-ttu-id="b5523-123">O exemplo a seguir cria **um ID2D1 CadakeStyle** que descreve um traço tracejado.</span><span class="sxs-lookup"><span data-stu-id="b5523-123">The following example creates an **ID2D1StrokeStyle** that describes a dashed stroke.</span></span> <span data-ttu-id="b5523-124">Este exemplo usa um padrão de traço predefinido, [**D2D1 \_ DASH STYLE DASH DOT \_ \_ \_ \_ DOT**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_dash_style), mas você também pode especificar seu próprio.</span><span class="sxs-lookup"><span data-stu-id="b5523-124">This example uses a predefined dash pattern, [**D2D1\_DASH\_STYLE\_DASH\_DOT\_DOT**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_dash_style), but you can also specify your own.</span></span>


```C++
D2D1_STROKE_STYLE_PROPERTIES strokeStyleProperties = D2D1::StrokeStyleProperties(
    D2D1_CAP_STYLE_FLAT,  // The start cap.
    D2D1_CAP_STYLE_FLAT,  // The end cap.
    D2D1_CAP_STYLE_TRIANGLE, // The dash cap.
    D2D1_LINE_JOIN_MITER, // The line join.
    10.0f, // The miter limit.
    D2D1_DASH_STYLE_DASH_DOT_DOT, // The dash style.
    0.0f // The dash offset.
    );

hr = m_pDirect2dFactory->CreateStrokeStyle(strokeStyleProperties, NULL, 0, &m_pStrokeStyle);

```



<span data-ttu-id="b5523-125">O exemplo a seguir usa o estilo de traço com o [**método DrawEllipse.**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-drawellipse(constd2d1_ellipse__id2d1brush_float_id2d1strokestyle))</span><span class="sxs-lookup"><span data-stu-id="b5523-125">The next example uses the stroke style with the [**DrawEllipse**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-drawellipse(constd2d1_ellipse__id2d1brush_float_id2d1strokestyle)) method.</span></span> <span data-ttu-id="b5523-126">Este exemplo produz a saída mostrada na ilustração a seguir.</span><span class="sxs-lookup"><span data-stu-id="b5523-126">This example produces the output shown in the following illustration.</span></span>

![ilustração de uma elipse com um traço tracejado](images/drawandfillellipseexample-2.png)


```C++
m_pRenderTarget->DrawEllipse(ellipse, m_pBlackBrush, 10.f, m_pStrokeStyle);
```



## <a name="draw-and-fill-an-ellipse"></a><span data-ttu-id="b5523-128">Desenhar e preencher uma elipse</span><span class="sxs-lookup"><span data-stu-id="b5523-128">Draw and Fill an Ellipse</span></span>

<span data-ttu-id="b5523-129">Para pintar o interior de uma elipse, use o [**método FillEllipse.**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse__id2d1brush))</span><span class="sxs-lookup"><span data-stu-id="b5523-129">To paint the interior of an ellipse, you use the [**FillEllipse**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse__id2d1brush)) method.</span></span> <span data-ttu-id="b5523-130">O exemplo a seguir usa o [**método DrawEllipse**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-drawellipse(constd2d1_ellipse__id2d1brush_float_id2d1strokestyle)) para delinear a elipse e, em seguida, usa o **método FillEllipse** para pintar seu interior.</span><span class="sxs-lookup"><span data-stu-id="b5523-130">The following example uses the [**DrawEllipse**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-drawellipse(constd2d1_ellipse__id2d1brush_float_id2d1strokestyle)) method to outline the ellipse, then uses the **FillEllipse** method to paint its interior.</span></span> <span data-ttu-id="b5523-131">Este exemplo produz a saída mostrada na ilustração a seguir.</span><span class="sxs-lookup"><span data-stu-id="b5523-131">This example produces the output shown in the following illustration.</span></span>

![ilustração de uma elipse com um traço tracejado e, em seguida, preenchida com uma cor cinza sólida](images/drawandfillellipseexample-3.png)


```C++
m_pRenderTarget->DrawEllipse(ellipse, m_pBlackBrush, 10.f, m_pStrokeStyle);
m_pRenderTarget->FillEllipse(ellipse, m_pSilverBrush);
```



<span data-ttu-id="b5523-133">O exemplo a seguir preenche a elipse primeiro e, em seguida, desenha seu contorno.</span><span class="sxs-lookup"><span data-stu-id="b5523-133">The next example fills the ellipse first, then draws its outline.</span></span> <span data-ttu-id="b5523-134">Este exemplo produz a saída mostrada na ilustração a seguir.</span><span class="sxs-lookup"><span data-stu-id="b5523-134">This example produces the output shown in the following illustration.</span></span>

![ilustração de uma elipse preenchida com uma cor cinza sólida e, em seguida, descrita com um traço tracejado](images/drawandfillellipseexample-4.png)


```C++
m_pRenderTarget->FillEllipse(ellipse, m_pSilverBrush);
m_pRenderTarget->DrawEllipse(ellipse, m_pBlackBrush, 10.f, m_pStrokeStyle);
```



<span data-ttu-id="b5523-136">O código foi omitido desses exemplos.</span><span class="sxs-lookup"><span data-stu-id="b5523-136">Code has been omitted from these examples.</span></span>

## <a name="drawing-more-complex-shapes"></a><span data-ttu-id="b5523-137">Desenhando formas mais complexas</span><span class="sxs-lookup"><span data-stu-id="b5523-137">Drawing More Complex Shapes</span></span>

<span data-ttu-id="b5523-138">Para desenhar formas mais complexas, defina objetos ID2D1Geometry e use-os com os métodos [**DrawGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) e [**FillGeometry.**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry)</span><span class="sxs-lookup"><span data-stu-id="b5523-138">To draw more complex shapes, you define ID2D1Geometry objects and use them with the [**DrawGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) and [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) methods.</span></span> <span data-ttu-id="b5523-139">Para obter mais informações, consulte a [Visão geral de geometrias.](direct2d-geometries-overview.md)</span><span class="sxs-lookup"><span data-stu-id="b5523-139">For more information, see the [Geometries Overview](direct2d-geometries-overview.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b5523-140">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b5523-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b5523-141">Visão geral de geometrias</span><span class="sxs-lookup"><span data-stu-id="b5523-141">Geometries Overview</span></span>](direct2d-geometries-overview.md)
</dt> <dt>

[<span data-ttu-id="b5523-142">Visão geral de pincéis</span><span class="sxs-lookup"><span data-stu-id="b5523-142">Brushes Overview</span></span>](direct2d-brushes-overview.md)
</dt> </dl>

 

 
