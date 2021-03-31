---
title: 'Visão geral de geometrias '
description: Descreve as noções básicas de geometrias de Direct2D, objetos que você pode usar para representar, manipular e analisar formas.
ms.assetid: f5870d4b-dd30-4034-884e-1c398a6865c6
keywords:
- Visão geral de Direct2D, geometrias
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: cb97b0737bfad391fb9ba2501793a970fcbd9886
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/09/2020
ms.locfileid: "103642917"
---
# <a name="geometries-overview"></a><span data-ttu-id="076b3-104">Visão geral de geometrias </span><span class="sxs-lookup"><span data-stu-id="076b3-104">Geometries overview</span></span>

<span data-ttu-id="076b3-105">Esta visão geral descreve como criar e usar objetos [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) para definir e manipular figuras 2D.</span><span class="sxs-lookup"><span data-stu-id="076b3-105">This overview describes how to create and use [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) objects to define and manipulate 2D figures.</span></span> <span data-ttu-id="076b3-106">Ele contém as seguintes seções:</span><span class="sxs-lookup"><span data-stu-id="076b3-106">It contains the following sections.</span></span>

## <a name="what-is-a-direct2d-geometry"></a><span data-ttu-id="076b3-107">O que é uma geometria Direct2D?</span><span class="sxs-lookup"><span data-stu-id="076b3-107">What is a Direct2D geometry?</span></span>

<span data-ttu-id="076b3-108">Uma geometria Direct2D é um objeto [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) .</span><span class="sxs-lookup"><span data-stu-id="076b3-108">A Direct2D geometry is an [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) object.</span></span> <span data-ttu-id="076b3-109">Esse objeto pode ser uma geometria simples ([**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry), [**ID2D1RoundedRectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1roundedrectanglegeometry)ou [**ID2D1EllipseGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1ellipsegeometry)), uma geometria de caminho ([**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry)) ou uma geometria composta ([**ID2D1GeometryGroup**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrygroup) e [**ID2D1TransformedGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1transformedgeometry)).</span><span class="sxs-lookup"><span data-stu-id="076b3-109">This object can be a simple geometry ([**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry), [**ID2D1RoundedRectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1roundedrectanglegeometry), or [**ID2D1EllipseGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1ellipsegeometry)), a path geometry ([**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry)), or a composite geometry ([**ID2D1GeometryGroup**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrygroup) and [**ID2D1TransformedGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1transformedgeometry)).</span></span>

<span data-ttu-id="076b3-110">As geometrias de Direct2D permitem que você descreva figuras bidimensionais e ofereça muitos usos, como a definição de regiões de teste de clique, regiões de clipes e até mesmo caminhos de animação.</span><span class="sxs-lookup"><span data-stu-id="076b3-110">Direct2D geometries enable you to describe two-dimensional figures and offer many uses, such as defining hit-test regions, clip regions, and even animation paths.</span></span>

<span data-ttu-id="076b3-111">As geometrias de Direct2D são recursos imutáveis e independentes de dispositivo criados pelo [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory).</span><span class="sxs-lookup"><span data-stu-id="076b3-111">Direct2D geometries are immutable and device-independent resources created by [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory).</span></span> <span data-ttu-id="076b3-112">Em geral, você deve criar geometrias uma vez e mantê-las durante a vida útil do aplicativo ou até que elas precisem ser alteradas.</span><span class="sxs-lookup"><span data-stu-id="076b3-112">Generally, you should create geometries one time and keep them for the life of the application, or until they have to be changed.</span></span> <span data-ttu-id="076b3-113">Para obter mais informações sobre recursos independentes de dispositivo e de dispositivo, consulte a [visão geral de recursos](resources-and-resource-domains.md).</span><span class="sxs-lookup"><span data-stu-id="076b3-113">For more information about device-independent and device-dependent resources, see the [Resources Overview](resources-and-resource-domains.md).</span></span>

<span data-ttu-id="076b3-114">As seções a seguir descrevem os diferentes tipos de geometrias.</span><span class="sxs-lookup"><span data-stu-id="076b3-114">The following sections describe the different kinds of geometries.</span></span>

## <a name="simple-geometries"></a><span data-ttu-id="076b3-115">Geometrias simples</span><span class="sxs-lookup"><span data-stu-id="076b3-115">Simple geometries</span></span>

<span data-ttu-id="076b3-116">As geometrias simples incluem os objetos [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry), [**ID2D1RoundedRectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1roundedrectanglegeometry)e [**ID2D1EllipseGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1ellipsegeometry) e podem ser usadas para criar valores geométricos básicos, como retângulos, retângulos arredondados, círculos e elipses.</span><span class="sxs-lookup"><span data-stu-id="076b3-116">Simple geometries include [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry), [**ID2D1RoundedRectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1roundedrectanglegeometry), and [**ID2D1EllipseGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1ellipsegeometry) objects, and can be used to create basic geometric figures, such as rectangles, rounded rectangles, circles, and ellipses.</span></span>

<span data-ttu-id="076b3-117">Para criar uma geometria simples, use um dos métodos de [**geometria ID2D1Factory:: create<*geometrytype*>**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) .</span><span class="sxs-lookup"><span data-stu-id="076b3-117">To create a simple geometry, use one of the [**ID2D1Factory::Create<*geometryType*>Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) methods.</span></span> <span data-ttu-id="076b3-118">Esses métodos criam um objeto do tipo especificado.</span><span class="sxs-lookup"><span data-stu-id="076b3-118">These methods create an object of the specified type.</span></span> <span data-ttu-id="076b3-119">Por exemplo, para criar um retângulo, chame [**ID2D1Factory:: CreateRectangleGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createrectanglegeometry(constd2d1_rect_f_id2d1rectanglegeometry)), que retorna um objeto [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry) ; para criar um retângulo arredondado, chame [**ID2D1Factory:: CreateRoundedRectangleGeometry**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-createroundedrectanglegeometry(constd2d1_rounded_rect__id2d1roundedrectanglegeometry)), que retorna um objeto [**ID2D1RoundedRectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1roundedrectanglegeometry) e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="076b3-119">For example, to create a rectangle, call [**ID2D1Factory::CreateRectangleGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createrectanglegeometry(constd2d1_rect_f_id2d1rectanglegeometry)), which returns an [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry) object; to create a rounded rectangle, call [**ID2D1Factory::CreateRoundedRectangleGeometry**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-createroundedrectanglegeometry(constd2d1_rounded_rect__id2d1roundedrectanglegeometry)), which returns an [**ID2D1RoundedRectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1roundedrectanglegeometry) object, and so on.</span></span>

<span data-ttu-id="076b3-120">O exemplo de código a seguir chama o método [**createellipsegeometry**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-createellipsegeometry(constd2d1_ellipse__id2d1ellipsegeometry)) , passando uma estrutura Ellipse com a *central* definida como (100, 100), *x-RADIUS* para 100 e *y-RADIUS* para 50.</span><span class="sxs-lookup"><span data-stu-id="076b3-120">The following code example calls the [**CreateEllipseGeometry**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-createellipsegeometry(constd2d1_ellipse__id2d1ellipsegeometry)) method, passing in an ellipse structure with the *center* set to (100, 100), *x-radius* to 100, and *y-radius* to 50.</span></span> <span data-ttu-id="076b3-121">Em seguida, ele chama [**DrawGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry), passando a geometria da elipse retornada, um ponteiro para um [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush)preto e uma largura de traço de 5.</span><span class="sxs-lookup"><span data-stu-id="076b3-121">Then, it calls [**DrawGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry), passing in the returned ellipse geometry, a pointer to a black [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush), and a stroke width of 5.</span></span> <span data-ttu-id="076b3-122">A ilustração a seguir mostra a saída do exemplo de código.</span><span class="sxs-lookup"><span data-stu-id="076b3-122">The following illustration shows the output from the code example.</span></span>

![ilustração de uma elipse](images/geometry-ovw-drawstep6.png)


```C++
ID2D1EllipseGeometry *m_pEllipseGeometry;
```




```C++
if (SUCCEEDED(hr))
{
    hr = m_pD2DFactory->CreateEllipseGeometry(
        D2D1::Ellipse(D2D1::Point2F(100.f, 60.f), 100.f, 50.f),
        &m_pEllipseGeometry
        );
}
```




```C++
m_pRenderTarget->DrawGeometry(m_pEllipseGeometry, m_pBlackBrush, 5);
```



<span data-ttu-id="076b3-124">Para desenhar o contorno de qualquer geometria, use o método [**DrawGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) .</span><span class="sxs-lookup"><span data-stu-id="076b3-124">To draw the outline of any geometry, use the [**DrawGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) method.</span></span> <span data-ttu-id="076b3-125">Para pintar seu interior, use o método [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) .</span><span class="sxs-lookup"><span data-stu-id="076b3-125">To paint its interior, use the [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) method.</span></span>

## <a name="path-geometries"></a><span data-ttu-id="076b3-126">Geometrias de caminho</span><span class="sxs-lookup"><span data-stu-id="076b3-126">Path geometries</span></span>

<span data-ttu-id="076b3-127">As geometrias de caminho são representadas pela interface [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) .</span><span class="sxs-lookup"><span data-stu-id="076b3-127">Path geometries are represented by the [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) interface.</span></span> <span data-ttu-id="076b3-128">Esses objetos podem ser usados para descrever valores geométricos complexos compostos de segmentos como arcos, curvas e linhas.</span><span class="sxs-lookup"><span data-stu-id="076b3-128">These objects can be used to describe complex geometric figures composed of segments such as arcs, curves, and lines.</span></span> <span data-ttu-id="076b3-129">A ilustração a seguir mostra um desenho criado usando a geometria de caminho.</span><span class="sxs-lookup"><span data-stu-id="076b3-129">The following illustration shows a drawing created by using path geometry.</span></span>

![ilustração de um rio, montanhas e o sol](images/path-geo-mnts.png)

<span data-ttu-id="076b3-131">Para obter mais informações e exemplos, consulte a [visão geral de geometrias de caminho](path-geometries-overview.md).</span><span class="sxs-lookup"><span data-stu-id="076b3-131">For more information and examples, see the [Path Geometries Overview](path-geometries-overview.md).</span></span>

## <a name="composite-geometries"></a><span data-ttu-id="076b3-132">Geometrias compostas</span><span class="sxs-lookup"><span data-stu-id="076b3-132">Composite geometries</span></span>

<span data-ttu-id="076b3-133">Uma geometria composta é uma geometria agrupada ou combinada com outro objeto Geometry ou com uma transformação.</span><span class="sxs-lookup"><span data-stu-id="076b3-133">A composite geometry is a geometry grouped or combined with another geometry object, or with a transform.</span></span> <span data-ttu-id="076b3-134">As geometrias compostas incluem objetos [**ID2D1TransformedGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1transformedgeometry) e [**ID2D1GeometryGroup**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrygroup) .</span><span class="sxs-lookup"><span data-stu-id="076b3-134">Composite geometries include [**ID2D1TransformedGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1transformedgeometry) and [**ID2D1GeometryGroup**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrygroup) objects.</span></span>

### <a name="geometry-groups"></a><span data-ttu-id="076b3-135">Grupos de geometria</span><span class="sxs-lookup"><span data-stu-id="076b3-135">Geometry groups</span></span>

<span data-ttu-id="076b3-136">Os grupos de geometria são uma maneira conveniente de agrupar várias geometrias ao mesmo tempo para que todas as figuras de várias geometrias distintas sejam concatenadas em uma.</span><span class="sxs-lookup"><span data-stu-id="076b3-136">Geometry groups are a convenient way to group several geometries at the same time so all figures of several distinct geometries are concatenated into one.</span></span> <span data-ttu-id="076b3-137">Para criar um [**objeto ID2D1GeometryGroup**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrygroup) , chame o método [**creategeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-creategeometrygroup) no objeto [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) , passando o *fillMode* com os valores possíveis de [**d2d1 modo de \_ preenchimento \_ \_ alternativo**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_fill_mode) (alternativo) e d2d1 do **\_ \_ modo de \_ preenchimento**, uma matriz de objetos Geometry para adicionar ao grupo Geometry e o número de elementos nessa matriz.</span><span class="sxs-lookup"><span data-stu-id="076b3-137">To create a [**ID2D1GeometryGroup**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrygroup) object, call the [**CreateGeometryGroup**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-creategeometrygroup) method on the [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) object, passing in the *fillMode* with possible values of [**D2D1\_FILL\_MODE\_ALTERNATE**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_fill_mode) (alternate) and **D2D1\_FILL\_MODE\_WINDING**, an array of geometry objects to add to the geometry group, and the number of elements in this array.</span></span>

<span data-ttu-id="076b3-138">O exemplo de código a seguir declara primeiro uma matriz de objetos Geometry.</span><span class="sxs-lookup"><span data-stu-id="076b3-138">The following code example first declares an array of geometry objects.</span></span> <span data-ttu-id="076b3-139">Esses objetos são quatro círculos concêntricos que têm o seguinte raios: 25, 50, 75 e 100.</span><span class="sxs-lookup"><span data-stu-id="076b3-139">These objects are four concentric circles that have the following radii: 25, 50, 75, and 100.</span></span> <span data-ttu-id="076b3-140">Em seguida, chame o grupo [**creategeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-creategeometrygroup) no objeto [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) , passando [**o \_ modo de preenchimento d2d1 \_ \_ alternativo**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_fill_mode), uma matriz de objetos Geometry para adicionar ao grupo Geometry e o número de elementos nessa matriz.</span><span class="sxs-lookup"><span data-stu-id="076b3-140">Then call the [**CreateGeometryGroup**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-creategeometrygroup) on the [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) object, passing in [**D2D1\_FILL\_MODE\_ALTERNATE**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_fill_mode), an array of geometry objects to add to the geometry group, and the number of elements in this array.</span></span>


```C++
ID2D1Geometry *ppGeometries[] =
{
    m_pEllipseGeometry1,
    m_pEllipseGeometry2,
    m_pEllipseGeometry3,
    m_pEllipseGeometry4
};

hr = m_pD2DFactory->CreateGeometryGroup(
    D2D1_FILL_MODE_ALTERNATE,
    ppGeometries,
    ARRAYSIZE(ppGeometries),
    &m_pGeoGroup_AlternateFill
    );

if (SUCCEEDED(hr))
{
    hr = m_pD2DFactory->CreateGeometryGroup(
        D2D1_FILL_MODE_WINDING,
        ppGeometries,
        ARRAYSIZE(ppGeometries),
        &m_pGeoGroup_WindingFill
        );
}
```

<span data-ttu-id="076b3-141">A ilustração a seguir mostra os resultados da renderização das duas geometrias de grupo do exemplo.</span><span class="sxs-lookup"><span data-stu-id="076b3-141">The following illustration shows the results of rendering the two group geometries from the example.</span></span>

![ilustração de dois conjuntos de quatro círculos concêntricos, um com anéis alternados preenchidos e outro com todos os anéis preenchidos](images/create-geometry-group.png)

### <a name="transformed-geometries"></a><span data-ttu-id="076b3-143">Geometrias transformadas</span><span class="sxs-lookup"><span data-stu-id="076b3-143">Transformed geometries</span></span>

<span data-ttu-id="076b3-144">Há várias maneiras de transformar uma geometria.</span><span class="sxs-lookup"><span data-stu-id="076b3-144">There are multiple ways to transform a geometry.</span></span> <span data-ttu-id="076b3-145">Você pode usar o método [**SetTransform**](/windows/win32/api/d2d1/nf-d2d1-id2d1brush-settransform(constd2d1_matrix_3x2_f_)) de um destino de renderização para transformar tudo o que o destino de renderização desenha, ou você pode associar uma transformação diretamente a uma geometria usando o método [**CreateTransformedGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createtransformedgeometry(id2d1geometry_constd2d1_matrix_3x2_f_id2d1transformedgeometry)) para criar um [**ID2D1TransformedGeometry**](/previous-versions/windows/desktop/legacy/dd371304(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="076b3-145">You can use the [**SetTransform**](/windows/win32/api/d2d1/nf-d2d1-id2d1brush-settransform(constd2d1_matrix_3x2_f_)) method of a render target to transform everything that the render target draws, or you can associate a transform directly with a geometry by using the [**CreateTransformedGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createtransformedgeometry(id2d1geometry_constd2d1_matrix_3x2_f_id2d1transformedgeometry)) method to create an [**ID2D1TransformedGeometry**](/previous-versions/windows/desktop/legacy/dd371304(v=vs.85)).</span></span>

<span data-ttu-id="076b3-146">O método que você deve usar depende do efeito desejado.</span><span class="sxs-lookup"><span data-stu-id="076b3-146">The method that you should use depends on the effect that you want.</span></span> <span data-ttu-id="076b3-147">Quando você usa o destino render para transformar e renderizar uma geometria, a transformação afeta tudo sobre a geometria, incluindo a largura de qualquer traço que você aplicou.</span><span class="sxs-lookup"><span data-stu-id="076b3-147">When you use the render target to transform and then render a geometry, the transform affects everything about the geometry, including the width of any stroke that you have applied.</span></span> <span data-ttu-id="076b3-148">Por outro lado, quando você usa um [**ID2D1TransformedGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1transformedgeometry), a transformação afeta apenas as coordenadas que descrevem a forma.</span><span class="sxs-lookup"><span data-stu-id="076b3-148">On the other hand, when you use an [**ID2D1TransformedGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1transformedgeometry), the transform affects only the coordinates that describe the shape.</span></span> <span data-ttu-id="076b3-149">A transformação não afetará a espessura do traço quando a geometria for desenhada.</span><span class="sxs-lookup"><span data-stu-id="076b3-149">The transformation will not affect the stroke thickness when the geometry is drawn.</span></span>

> [!Note]  
> <span data-ttu-id="076b3-150">A partir do Windows 8, a transformação do mundo não afetará a espessura do traço de traços com o [**\_ tipo de transformação Stroke d2d1 \_ \_ \_ fixo**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_stroke_transform_type)ou [**d2d1 \_ \_ tipo de transformação \_ \_ traço**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_stroke_transform_type).</span><span class="sxs-lookup"><span data-stu-id="076b3-150">Starting with Windows 8 the world transform will not affect the stroke thickness of strokes with [**D2D1\_STROKE\_TRANSFORM\_TYPE\_FIXED**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_stroke_transform_type)or [**D2D1\_STROKE\_TRANSFORM\_TYPE\_HAIRLINE**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_stroke_transform_type).</span></span> <span data-ttu-id="076b3-151">Você deve usar esses tipos de transformação para obter traços independentes de transformação</span><span class="sxs-lookup"><span data-stu-id="076b3-151">You should use these transform types to achieve transform independent strokes</span></span>

 

<span data-ttu-id="076b3-152">O exemplo a seguir cria um [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry)e, em seguida, o Desenha sem transformá-lo.</span><span class="sxs-lookup"><span data-stu-id="076b3-152">The following example creates an [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry), then draws it without transforming it.</span></span> <span data-ttu-id="076b3-153">Ele produz a saída mostrada na ilustração a seguir.</span><span class="sxs-lookup"><span data-stu-id="076b3-153">It produces the output shown in the following illustration.</span></span>

![ilustração de um retângulo](images/transformedgeometry2-step1.png)


```C++
hr = m_pD2DFactory->CreateRectangleGeometry(
    D2D1::RectF(150.f, 150.f, 200.f, 200.f),
    &m_pRectangleGeometry
    );
```




```C++
// Draw the untransformed rectangle geometry.
m_pRenderTarget->DrawGeometry(m_pRectangleGeometry, m_pBlackBrush, 1);
```



<span data-ttu-id="076b3-155">O exemplo a seguir usa o destino render para dimensionar a geometria por um fator de 3 e, em seguida, a desenha.</span><span class="sxs-lookup"><span data-stu-id="076b3-155">The next example uses the render target to scale the geometry by a factor of 3, then draws it.</span></span> <span data-ttu-id="076b3-156">A ilustração a seguir mostra o resultado do desenho do retângulo sem a transformação e com a transformação.</span><span class="sxs-lookup"><span data-stu-id="076b3-156">The following illustration shows the result of drawing the rectangle without the transform and with the transform.</span></span> <span data-ttu-id="076b3-157">Observe que o traço é mais espesso após a transformação, embora a espessura do traço seja 1.</span><span class="sxs-lookup"><span data-stu-id="076b3-157">Notice that the stroke is thicker after the transform, even though the stroke thickness is 1.</span></span>

![ilustração de um retângulo menor dentro de um retângulo maior com um traço mais espesso](images/transformedgeometry2-step2.png)


```C++
// Transform the render target, then draw the rectangle geometry again.
m_pRenderTarget->SetTransform(
    D2D1::Matrix3x2F::Scale(
        D2D1::SizeF(3.f, 3.f),
        D2D1::Point2F(175.f, 175.f))
    );

m_pRenderTarget->DrawGeometry(m_pRectangleGeometry, m_pBlackBrush, 1);
```



<span data-ttu-id="076b3-159">O exemplo a seguir usa o método [**CreateTransformedGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createtransformedgeometry(id2d1geometry_constd2d1_matrix_3x2_f__id2d1transformedgeometry)) para dimensionar a geometria por um fator de 3 e, em seguida, a desenha.</span><span class="sxs-lookup"><span data-stu-id="076b3-159">The next example uses the [**CreateTransformedGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createtransformedgeometry(id2d1geometry_constd2d1_matrix_3x2_f__id2d1transformedgeometry)) method to scale the geometry by a factor of 3, then draws it.</span></span> <span data-ttu-id="076b3-160">Ele produz a saída mostrada na ilustração a seguir.</span><span class="sxs-lookup"><span data-stu-id="076b3-160">It produces the output shown in the following illustration.</span></span> <span data-ttu-id="076b3-161">Observe que, embora o retângulo seja maior, seu traço ainda não aumentou.</span><span class="sxs-lookup"><span data-stu-id="076b3-161">Notice that, although the rectangle is larger, its stroke hasn't increased.</span></span>

![ilustração de um retângulo menor dentro de um retângulo maior com a mesma espessura do traço](images/transformedgeometry2-step3.png)


```C++
 // Create a geometry that is a scaled version
 // of m_pRectangleGeometry.
 // The new geometry is scaled by a factory of 3
 // from the center of the geometry, (35, 35).

 hr = m_pD2DFactory->CreateTransformedGeometry(
     m_pRectangleGeometry,
     D2D1::Matrix3x2F::Scale(
         D2D1::SizeF(3.f, 3.f),
         D2D1::Point2F(175.f, 175.f)),
     &m_pTransformedGeometry
     );
```




```C++
// Replace the previous render target transform.
m_pRenderTarget->SetTransform(D2D1::Matrix3x2F::Identity());

// Draw the transformed geometry.
m_pRenderTarget->DrawGeometry(m_pTransformedGeometry, m_pBlackBrush, 1);
```



## <a name="geometries-as-masks"></a><span data-ttu-id="076b3-163">Geometrias como máscaras</span><span class="sxs-lookup"><span data-stu-id="076b3-163">Geometries as masks</span></span>

<span data-ttu-id="076b3-164">Você pode usar um objeto [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) como uma máscara geométrica ao chamar o método [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) .</span><span class="sxs-lookup"><span data-stu-id="076b3-164">You can use an [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) object as a geometric mask when you call the [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) method.</span></span> <span data-ttu-id="076b3-165">A máscara geométrica especifica a área da camada que é composta no destino de renderização.</span><span class="sxs-lookup"><span data-stu-id="076b3-165">The geometric mask specifies the area of the layer that is composited into the render target.</span></span> <span data-ttu-id="076b3-166">Para obter mais informações, consulte a seção máscaras geométricas da [visão geral sobre camadas](direct2d-layers-overview.md).</span><span class="sxs-lookup"><span data-stu-id="076b3-166">For more information, see the Geometric Masks section of the [Layers Overview](direct2d-layers-overview.md).</span></span>

## <a name="geometric-operations"></a><span data-ttu-id="076b3-167">Operações geométricas</span><span class="sxs-lookup"><span data-stu-id="076b3-167">Geometric operations</span></span>

<span data-ttu-id="076b3-168">A interface [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) fornece várias operações geométricas que você pode usar para manipular e medir valores geométricos.</span><span class="sxs-lookup"><span data-stu-id="076b3-168">The [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) interface provides several geometric operations that you can use to manipulate and measure geometric figures.</span></span> <span data-ttu-id="076b3-169">Por exemplo, você pode usá-los para calcular e retornar seus limites, comparar para ver como uma geometria está espacialmente relacionada a outra (útil para teste de clique), calcular as áreas e comprimentos e muito mais.</span><span class="sxs-lookup"><span data-stu-id="076b3-169">For example, you can use them to calculate and return their bounds, compare to see how one geometry is spatially related to another (useful for hit testing), calculate the areas and lengths, and more.</span></span> <span data-ttu-id="076b3-170">A tabela a seguir descreve as operações geométricas comuns.</span><span class="sxs-lookup"><span data-stu-id="076b3-170">The following table describes the common geometric operations.</span></span>



| <span data-ttu-id="076b3-171">Operação</span><span class="sxs-lookup"><span data-stu-id="076b3-171">Operation</span></span>                                                   | <span data-ttu-id="076b3-172">Método</span><span class="sxs-lookup"><span data-stu-id="076b3-172">Method</span></span>                                                                                                                                                                     |
|-------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="076b3-173">Combinar</span><span class="sxs-lookup"><span data-stu-id="076b3-173">Combine</span></span>                                                     | [<span data-ttu-id="076b3-174">**CombineWithGeometry**</span><span class="sxs-lookup"><span data-stu-id="076b3-174">**CombineWithGeometry**</span></span>](id2d1geometry-combinewithgeometry.md)                                                                                                           |
| <span data-ttu-id="076b3-175">Limites/limites ampliados/recuperados, atualização de região suja</span><span class="sxs-lookup"><span data-stu-id="076b3-175">Bounds/ Widened Bounds/Retrieve Bounds, Dirty Region update</span></span> | <span data-ttu-id="076b3-176">[**Ampliação**](id2d1geometry-widen.md), [**GetBounds**](/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1gdimetafile-getbounds), [**GetWidenedBounds**](id2d1geometry-getwidenedbounds.md)</span><span class="sxs-lookup"><span data-stu-id="076b3-176">[**Widen**](id2d1geometry-widen.md), [**GetBounds**](/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1gdimetafile-getbounds), [**GetWidenedBounds**](id2d1geometry-getwidenedbounds.md)</span></span>                             |
| <span data-ttu-id="076b3-177">Testes de clique</span><span class="sxs-lookup"><span data-stu-id="076b3-177">Hit Testing</span></span>                                                 | <span data-ttu-id="076b3-178">[**FillContainsPoint**](id2d1geometry-fillcontainspoint.md), [ **StrokeContainsPoint**](id2d1geometry-strokecontainspoint.md)</span><span class="sxs-lookup"><span data-stu-id="076b3-178">[**FillContainsPoint**](id2d1geometry-fillcontainspoint.md), [**StrokeContainsPoint**](id2d1geometry-strokecontainspoint.md)</span></span>                                             |
| <span data-ttu-id="076b3-179">Traço</span><span class="sxs-lookup"><span data-stu-id="076b3-179">Stroke</span></span>                                                      | [<span data-ttu-id="076b3-180">**StrokeContainsPoint**</span><span class="sxs-lookup"><span data-stu-id="076b3-180">**StrokeContainsPoint**</span></span>](id2d1geometry-strokecontainspoint.md)                                                                                                           |
| <span data-ttu-id="076b3-181">Comparação</span><span class="sxs-lookup"><span data-stu-id="076b3-181">Comparison</span></span>                                                  | [<span data-ttu-id="076b3-182">**CompareWithGeometry**</span><span class="sxs-lookup"><span data-stu-id="076b3-182">**CompareWithGeometry**</span></span>](id2d1geometry-comparewithgeometry.md)                                                                                                           |
| <span data-ttu-id="076b3-183">Simplificação (remove arcos e curvas quadráticas de Bézier)</span><span class="sxs-lookup"><span data-stu-id="076b3-183">Simplification (removes arcs and quadratic Bezier curves)</span></span>   | [<span data-ttu-id="076b3-184">**Simplifique**</span><span class="sxs-lookup"><span data-stu-id="076b3-184">**Simplify**</span></span>](id2d1geometry-simplify.md)                                                                                                                                 |
| <span data-ttu-id="076b3-185">Mosaico</span><span class="sxs-lookup"><span data-stu-id="076b3-185">Tessellation</span></span>                                                | [<span data-ttu-id="076b3-186">**Incluí**</span><span class="sxs-lookup"><span data-stu-id="076b3-186">**Tessellate**</span></span>](id2d1geometry-tessellate.md)                                                                                                                             |
| <span data-ttu-id="076b3-187">Estrutura de tópicos (remover interseção)</span><span class="sxs-lookup"><span data-stu-id="076b3-187">Outline (remove intersection)</span></span>                               | [<span data-ttu-id="076b3-188">**Contorno**</span><span class="sxs-lookup"><span data-stu-id="076b3-188">**Outline**</span></span>](id2d1geometry-outline.md)                                                                                                                                   |
| <span data-ttu-id="076b3-189">Calcular a área ou o comprimento de uma geometria</span><span class="sxs-lookup"><span data-stu-id="076b3-189">Calculate the area or length of a geometry</span></span>                  | <span data-ttu-id="076b3-190">[**ComputeArea**](id2d1geometry-computearea.md), [**ComputeLength**](id2d1geometry-computelength.md), [**ComputePointAtLength**](id2d1geometry-computepointatlength.md)</span><span class="sxs-lookup"><span data-stu-id="076b3-190">[**ComputeArea**](id2d1geometry-computearea.md), [**ComputeLength**](id2d1geometry-computelength.md), [**ComputePointAtLength**](id2d1geometry-computepointatlength.md)</span></span> |



 

> [!Note]  
> <span data-ttu-id="076b3-191">A partir do Windows 8, você pode usar o método [**ComputePointAndSegmentAtLength**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1pathgeometry1-computepointandsegmentatlength(float_uint32_constd2d1_matrix_3x2_f_float_d2d1_point_description)) no [**ID2D1PathGeometry1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1pathgeometry1) para calcular a área ou o comprimento de uma geometria.</span><span class="sxs-lookup"><span data-stu-id="076b3-191">Starting in Windows 8, you can use the [**ComputePointAndSegmentAtLength**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1pathgeometry1-computepointandsegmentatlength(float_uint32_constd2d1_matrix_3x2_f_float_d2d1_point_description)) method on the [**ID2D1PathGeometry1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1pathgeometry1) to calculate the area or length of a geometry.</span></span>

 

### <a name="combining-geometries"></a><span data-ttu-id="076b3-192">Combinando geometrias</span><span class="sxs-lookup"><span data-stu-id="076b3-192">Combining geometries</span></span>

<span data-ttu-id="076b3-193">Para combinar uma geometria com outra, chame o método [**ID2D1Geometry:: CombineWithGeometry**](id2d1geometry-combinewithgeometry.md) .</span><span class="sxs-lookup"><span data-stu-id="076b3-193">To combine one geometry with another, call the [**ID2D1Geometry::CombineWithGeometry**](id2d1geometry-combinewithgeometry.md) method.</span></span> <span data-ttu-id="076b3-194">Ao combinar as geometrias, você especifica uma das quatro maneiras de executar a operação combinar: [**d2d1 \_ combinar \_ modo \_ Union**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_combine_mode) (Union), [**d2d1 \_ combinar modo de \_ \_ combinação**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_combine_mode) (Intersect), [**d2d1 \_ Combine \_ mode \_ XOR**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_combine_mode) (XOR) e [**d2d1 \_ Combine \_ mode \_ Exclude**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_combine_mode) (excluir).</span><span class="sxs-lookup"><span data-stu-id="076b3-194">When you combine the geometries, you specify one of the four ways to perform the combine operation: [**D2D1\_COMBINE\_MODE\_UNION**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_combine_mode) (union), [**D2D1\_COMBINE\_MODE\_INTERSECT**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_combine_mode) (intersect), [**D2D1\_COMBINE\_MODE\_XOR**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_combine_mode) (xor), and [**D2D1\_COMBINE\_MODE\_EXCLUDE**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_combine_mode) (exclude).</span></span> <span data-ttu-id="076b3-195">O exemplo de código a seguir mostra dois círculos que são combinados usando o modo de combinação Union, em que o primeiro círculo tem o ponto central de (75, 75) e o raio de 50, e o segundo círculo tem o ponto central de (125, 75) e o raio de 50.</span><span class="sxs-lookup"><span data-stu-id="076b3-195">The following code example shows two circles that are combined by using the union combine mode, where the first circle has the center point of (75, 75) and the radius of 50, and the second circle has the center point of (125, 75) and the radius of 50.</span></span>


```C++
HRESULT hr = S_OK;
ID2D1GeometrySink *pGeometrySink = NULL;

// Create the first ellipse geometry to merge.
const D2D1_ELLIPSE circle1 = D2D1::Ellipse(
    D2D1::Point2F(75.0f, 75.0f),
    50.0f,
    50.0f
    );

hr = m_pD2DFactory->CreateEllipseGeometry(
    circle1,
    &m_pCircleGeometry1
    );

if (SUCCEEDED(hr))
{
    // Create the second ellipse geometry to merge.
    const D2D1_ELLIPSE circle2 = D2D1::Ellipse(
        D2D1::Point2F(125.0f, 75.0f),
        50.0f,
        50.0f
        );

    hr = m_pD2DFactory->CreateEllipseGeometry(circle2, &m_pCircleGeometry2);
}


if (SUCCEEDED(hr))
{
    //
    // Use D2D1_COMBINE_MODE_UNION to combine the geometries.
    //
    hr = m_pD2DFactory->CreatePathGeometry(&m_pPathGeometryUnion);

    if (SUCCEEDED(hr))
    {
        hr = m_pPathGeometryUnion->Open(&pGeometrySink);

        if (SUCCEEDED(hr))
        {
            hr = m_pCircleGeometry1->CombineWithGeometry(
                m_pCircleGeometry2,
                D2D1_COMBINE_MODE_UNION,
                NULL,
                NULL,
                pGeometrySink
                );
        }

        if (SUCCEEDED(hr))
        {
            hr = pGeometrySink->Close();
        }

        SafeRelease(&pGeometrySink);
    }
}
```



<span data-ttu-id="076b3-196">A ilustração a seguir mostra dois círculos combinados com um modo de combinação de Union.</span><span class="sxs-lookup"><span data-stu-id="076b3-196">The following illustration shows two circles combined with a combine mode of union.</span></span>

![ilustração de dois círculos sobrepostos combinados em uma União](images/combine-mode-union.png)

<span data-ttu-id="076b3-198">Para obter ilustrações de todos os modos de combinação, consulte a [**\_ \_ Enumeração modo de combinação d2d1**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_combine_mode).</span><span class="sxs-lookup"><span data-stu-id="076b3-198">For illustrations of all the combine modes, see the [**D2D1\_COMBINE\_MODE enumeration**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_combine_mode).</span></span>

### <a name="widen"></a><span data-ttu-id="076b3-199">Expansão</span><span class="sxs-lookup"><span data-stu-id="076b3-199">Widen</span></span>

<span data-ttu-id="076b3-200">O método de [**ampliação**](id2d1geometry-widen.md) gera uma nova geometria cujo preenchimento é equivalente ao traçado da geometria existente e, em seguida, grava o resultado no objeto [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink) especificado.</span><span class="sxs-lookup"><span data-stu-id="076b3-200">The [**Widen**](id2d1geometry-widen.md) method generates a new geometry whose fill is equivalent to stroking the existing geometry, and then writes the result to the specified [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink) object.</span></span> <span data-ttu-id="076b3-201">O exemplo de código a seguir chama [**Open**](/windows/win32/api/d2d1/nf-d2d1-id2d1pathgeometry-open) no objeto [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) .</span><span class="sxs-lookup"><span data-stu-id="076b3-201">The following code example calls [**Open**](/windows/win32/api/d2d1/nf-d2d1-id2d1pathgeometry-open) on the [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) object.</span></span> <span data-ttu-id="076b3-202">Se **abrir** for executado com sucesso, ele chamará **ampliação** no objeto Geometry.</span><span class="sxs-lookup"><span data-stu-id="076b3-202">If **Open** succeeds, it calls **Widen** on the geometry object.</span></span>


```C++
ID2D1GeometrySink *pGeometrySink = NULL;
hr = pPathGeometry->Open(&pGeometrySink);
if (SUCCEEDED(hr))
{
    hr = pGeometry->Widen(
            strokeWidth,
            pIStrokeStyle,
            pWorldTransform,
            pGeometrySink
            );
```



### <a name="tessellate"></a><span data-ttu-id="076b3-203">Incluí</span><span class="sxs-lookup"><span data-stu-id="076b3-203">Tessellate</span></span>

<span data-ttu-id="076b3-204">O método [**incluí**](id2d1geometry-tessellate.md) cria um conjunto de triângulos de rotação horária que cobrem a geometria depois que ela é transformada usando a matriz especificada e achatada usando a tolerância especificada.</span><span class="sxs-lookup"><span data-stu-id="076b3-204">The [**Tessellate**](id2d1geometry-tessellate.md) method creates a set of clockwise-wound triangles that cover the geometry after it is transformed by using the specified matrix and flattened by using the specified tolerance.</span></span> <span data-ttu-id="076b3-205">O exemplo de código a seguir usa **incluí** para criar uma lista de triângulos que representam *pPathGeometry*.</span><span class="sxs-lookup"><span data-stu-id="076b3-205">The following code example uses **Tessellate** to create a list of triangles that represent *pPathGeometry*.</span></span> <span data-ttu-id="076b3-206">Os triângulos são armazenados em um [**ID2D1Mesh**](/windows/win32/api/d2d1/nn-d2d1-id2d1mesh), *pMesh*, então transferidos para um membro de classe, *m \_ pStrokeMesh*, para uso posterior durante a renderização.</span><span class="sxs-lookup"><span data-stu-id="076b3-206">The triangles are stored in an [**ID2D1Mesh**](/windows/win32/api/d2d1/nn-d2d1-id2d1mesh), *pMesh*, then transferred to a class member, *m\_pStrokeMesh*, for later use when rendering.</span></span>


```C++
ID2D1Mesh *pMesh = NULL;
hr = m_pRT->CreateMesh(&pMesh);
if (SUCCEEDED(hr))
{
    ID2D1TessellationSink *pSink = NULL;
    hr = pMesh->Open(&pSink);
    if (SUCCEEDED(hr))
    {
        hr = pPathGeometry->Tessellate(
                NULL, // world transform (already handled in Widen)
                pSink
                );
        if (SUCCEEDED(hr))
        {
            hr = pSink->Close();
            if (SUCCEEDED(hr))
            {
                SafeReplace(&m_pStrokeMesh, pMesh);
            }
        }
        pSink->Release();
    }
    pMesh->Release();
}
```



### <a name="fillcontainspoint-and-strokecontainspoint"></a><span data-ttu-id="076b3-207">FillContainsPoint e StrokeContainsPoint</span><span class="sxs-lookup"><span data-stu-id="076b3-207">FillContainsPoint and StrokeContainsPoint</span></span>

<span data-ttu-id="076b3-208">O método [**FillContainsPoint**](id2d1geometry-fillcontainspoint.md) indica se a área preenchida pela geometria contém o ponto especificado.</span><span class="sxs-lookup"><span data-stu-id="076b3-208">The [**FillContainsPoint**](id2d1geometry-fillcontainspoint.md) method indicates whether the area filled by the geometry contains the specified point.</span></span> <span data-ttu-id="076b3-209">Você pode usar esse método para fazer testes de clique.</span><span class="sxs-lookup"><span data-stu-id="076b3-209">You can use this method to do hit testing.</span></span> <span data-ttu-id="076b3-210">O exemplo de código a seguir chama **FillContainsPoint** em um objeto [**ID2D1EllipseGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1ellipsegeometry) , passando um ponto em (0, 0) e uma matriz de [**identidade**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-isidentity) .</span><span class="sxs-lookup"><span data-stu-id="076b3-210">The following code example calls **FillContainsPoint** on an [**ID2D1EllipseGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1ellipsegeometry) object, passing in a point at (0,0) and an [**Identity**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-isidentity) matrix.</span></span>


```C++
BOOL containsPoint1;
hr = m_pCircleGeometry1->FillContainsPoint(
    D2D1::Point2F(0,0),
    D2D1::Matrix3x2F::Identity(),
    &containsPoint1
    );

if (SUCCEEDED(hr))
{
    // Process containsPoint.
}
```



<span data-ttu-id="076b3-211">O método [**StrokeContainsPoint**](id2d1geometry-strokecontainspoint.md) determina se o traço da geometria contém o ponto especificado.</span><span class="sxs-lookup"><span data-stu-id="076b3-211">The [**StrokeContainsPoint**](id2d1geometry-strokecontainspoint.md) method determines whether the geometry's stroke contains the specified point.</span></span> <span data-ttu-id="076b3-212">Você pode usar esse método para fazer testes de clique.</span><span class="sxs-lookup"><span data-stu-id="076b3-212">You can use this method to do hit testing.</span></span> <span data-ttu-id="076b3-213">O exemplo de código a seguir usa **StrokeContainsPoint**.</span><span class="sxs-lookup"><span data-stu-id="076b3-213">The following code example uses **StrokeContainsPoint**.</span></span>


```C++
BOOL containsPoint;

hr = m_pCircleGeometry1->StrokeContainsPoint(
    D2D1::Point2F(0,0),
    10,     // stroke width
    NULL,   // stroke style
    NULL,   // world transform
    &containsPoint
    );

if (SUCCEEDED(hr))
{
    // Process containsPoint.
}
```



### <a name="simplify"></a><span data-ttu-id="076b3-214">Simplificar o </span><span class="sxs-lookup"><span data-stu-id="076b3-214">Simplify</span></span>

<span data-ttu-id="076b3-215">O método [**simplificar**](id2d1geometry-simplify.md) remove arcos e curvas de Bezier quadrática de uma geometria especificada.</span><span class="sxs-lookup"><span data-stu-id="076b3-215">The [**Simplify**](id2d1geometry-simplify.md) method removes arcs and quadratic Bezier curves from a specified geometry.</span></span> <span data-ttu-id="076b3-216">Portanto, a geometria resultante contém apenas linhas e, opcionalmente, curvas Bézier cúbicas.</span><span class="sxs-lookup"><span data-stu-id="076b3-216">So, the resulting geometry contains only lines and, optionally, cubic Bezier curves.</span></span> <span data-ttu-id="076b3-217">O exemplo de código a seguir usa **simplificação** para transformar uma geometria com curvas de Bézier em uma geometria que contém apenas segmentos de linha.</span><span class="sxs-lookup"><span data-stu-id="076b3-217">The following code example uses **Simplify** to transform a geometry with Bezier curves into a geometry that contains only line segments.</span></span>


```C++
HRESULT D2DFlatten(
    ID2D1Geometry *pGeometry,
    float flatteningTolerance,
    ID2D1Geometry **ppGeometry
    )
{
    HRESULT hr;
    ID2D1Factory *pFactory = NULL;
    pGeometry->GetFactory(&pFactory);

    ID2D1PathGeometry *pPathGeometry = NULL;
    hr = pFactory->CreatePathGeometry(&pPathGeometry);

    if (SUCCEEDED(hr))
    {
        ID2D1GeometrySink *pSink = NULL;
        hr = pPathGeometry->Open(&pSink);

        if (SUCCEEDED(hr))
        {
            hr = pGeometry->Simplify(
                    D2D1_GEOMETRY_SIMPLIFICATION_OPTION_LINES,
                    NULL, // world transform
                    flatteningTolerance,
                    pSink
                    );

            if (SUCCEEDED(hr))
            {
                hr = pSink->Close();

                if (SUCCEEDED(hr))
                {
                    *ppGeometry = pPathGeometry;
                    (*ppGeometry)->AddRef();
                }
            }
            pSink->Release();
        }
        pPathGeometry->Release();
    }

    pFactory->Release();

    return hr;
}
```



### <a name="computelength-and-computearea"></a><span data-ttu-id="076b3-218">ComputeLength e ComputeArea</span><span class="sxs-lookup"><span data-stu-id="076b3-218">ComputeLength and ComputeArea</span></span>

<span data-ttu-id="076b3-219">O método [**ComputeLength**](id2d1geometry-computelength.md) calcula o comprimento da geometria especificada se cada segmento não tiver sido revertido em uma linha.</span><span class="sxs-lookup"><span data-stu-id="076b3-219">The [**ComputeLength**](id2d1geometry-computelength.md) method calculates the length of the specified geometry if each segment were unrolled into a line.</span></span> <span data-ttu-id="076b3-220">Isso incluirá o segmento de fechamento implícito se a geometria for fechada.</span><span class="sxs-lookup"><span data-stu-id="076b3-220">This includes the implicit closing segment if the geometry is closed.</span></span> <span data-ttu-id="076b3-221">O exemplo de código a seguir usa **ComputeLength** para calcular o comprimento de um círculo especificado (**m \_ pCircleGeometry1**).</span><span class="sxs-lookup"><span data-stu-id="076b3-221">The following code example uses **ComputeLength** to compute the length of a specified circle (**m\_pCircleGeometry1**).</span></span>


```C++
float length;

// Compute the area of circle1
hr = m_pCircleGeometry1->ComputeLength(
    D2D1::IdentityMatrix(),
    &length
    );

if (SUCCEEDED(hr))
{
    // Process the length of the geometry.
}
```



<span data-ttu-id="076b3-222">O método [**ComputeArea**](id2d1geometry-computearea.md) calcula a área da geometria especificada.</span><span class="sxs-lookup"><span data-stu-id="076b3-222">The [**ComputeArea**](id2d1geometry-computearea.md) method calculates the area of the specified geometry.</span></span> <span data-ttu-id="076b3-223">O exemplo de código a seguir usa **ComputeArea** para calcular a área de um círculo especificado (**m \_ pCircleGeometry1**).</span><span class="sxs-lookup"><span data-stu-id="076b3-223">The following code example uses **ComputeArea** to compute the area of a specified circle (**m\_pCircleGeometry1**).</span></span>


```C++
float area;

// Compute the area of circle1
hr = m_pCircleGeometry1->ComputeArea(
    D2D1::IdentityMatrix(),
    &area
    );
```



### <a name="comparewithgeometry"></a><span data-ttu-id="076b3-224">CompareWithGeometry</span><span class="sxs-lookup"><span data-stu-id="076b3-224">CompareWithGeometry</span></span>

<span data-ttu-id="076b3-225">O método [**CompareWithGeometry**](id2d1geometry-comparewithgeometry.md) descreve a interseção entre a geometria que chama esse método e a geometria especificada.</span><span class="sxs-lookup"><span data-stu-id="076b3-225">The [**CompareWithGeometry**](id2d1geometry-comparewithgeometry.md) method describes the intersection between the geometry that calls this method and the specified geometry.</span></span> <span data-ttu-id="076b3-226">Os valores possíveis para interseção incluem [**a \_ relação de geometria \_ \_ de d2d1**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_geometry_relation) (não junção), a **relação de geometria de d2d1 \_ \_ \_ está \_ contida** (está contida), **d2d1 a relação de \_ geometria \_ \_ contém** (contém) e **\_ \_ \_ sobreposição de relação de geometria de d2d1** (sobreposição).</span><span class="sxs-lookup"><span data-stu-id="076b3-226">The possible values for intersection include [**D2D1\_GEOMETRY\_RELATION\_DISJOINT**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_geometry_relation) (disjoint), **D2D1\_GEOMETRY\_RELATION\_IS\_CONTAINED** (is contained), **D2D1\_GEOMETRY\_RELATION\_CONTAINS** (contains), and **D2D1\_GEOMETRY\_RELATION\_OVERLAP** (overlap).</span></span> <span data-ttu-id="076b3-227">"não contíguo" significa que dois preenchimentos de geometria não fazem interseção.</span><span class="sxs-lookup"><span data-stu-id="076b3-227">"disjoint" means that two geometry fills do not intersect at all.</span></span> <span data-ttu-id="076b3-228">"is contained" significa que a geometria está completamente contida na geometria especificada.</span><span class="sxs-lookup"><span data-stu-id="076b3-228">"is contained" means that the geometry is completely contained by the specified geometry.</span></span> <span data-ttu-id="076b3-229">"Contains" significa que a geometria contém completamente a geometria especificada e "sobreposição" significa que as duas geometrias se sobrepõem, mas nenhuma delas contém completamente a outra.</span><span class="sxs-lookup"><span data-stu-id="076b3-229">"contains" means that the geometry completely contains the specified geometry, and "overlap" means the two geometries overlap but neither completely contains the other.</span></span>

<span data-ttu-id="076b3-230">O exemplo de código a seguir mostra como comparar dois círculos que têm o mesmo raio de 50, mas que são compensados por 50.</span><span class="sxs-lookup"><span data-stu-id="076b3-230">The following code example shows how to compare two circles that have the same radius of 50 but are offset by 50.</span></span>


```C++
HRESULT hr = S_OK;
ID2D1GeometrySink *pGeometrySink = NULL;

// Create the first ellipse geometry to merge.
const D2D1_ELLIPSE circle1 = D2D1::Ellipse(
    D2D1::Point2F(75.0f, 75.0f),
    50.0f,
    50.0f
    );

hr = m_pD2DFactory->CreateEllipseGeometry(
    circle1,
    &m_pCircleGeometry1
    );

if (SUCCEEDED(hr))
{
    // Create the second ellipse geometry to merge.
    const D2D1_ELLIPSE circle2 = D2D1::Ellipse(
        D2D1::Point2F(125.0f, 75.0f),
        50.0f,
        50.0f
        );

    hr = m_pD2DFactory->CreateEllipseGeometry(circle2, &m_pCircleGeometry2);
}

```




```C++
D2D1_GEOMETRY_RELATION result = D2D1_GEOMETRY_RELATION_UNKNOWN;

// Compare circle1 with circle2
hr = m_pCircleGeometry1->CompareWithGeometry(
    m_pCircleGeometry2,
    D2D1::IdentityMatrix(),
    0.1f,
    &result
    );

if (SUCCEEDED(hr))
{
    static const WCHAR szGeometryRelation[] = L"Two circles overlap.";
    m_pRenderTarget->SetTransform(D2D1::IdentityMatrix());
    if (result == D2D1_GEOMETRY_RELATION_OVERLAP)
    {
        m_pRenderTarget->DrawText(
            szGeometryRelation,
            ARRAYSIZE(szGeometryRelation) - 1,
            m_pTextFormat,
            D2D1::RectF(25.0f, 160.0f, 200.0f, 300.0f),
            m_pTextBrush
            );
    }
}
```



### <a name="outline"></a><span data-ttu-id="076b3-231">Contorno</span><span class="sxs-lookup"><span data-stu-id="076b3-231">Outline</span></span>

<span data-ttu-id="076b3-232">O método de [**estrutura de tópicos**](id2d1geometry-outline.md) computa o contorno da geometria (uma versão da geometria na qual nenhuma figura cruza a si mesma ou qualquer outra figura) e grava o resultado em um [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink).</span><span class="sxs-lookup"><span data-stu-id="076b3-232">The [**Outline**](id2d1geometry-outline.md) method computes the outline of the geometry (a version of the geometry in which no figure crosses itself or any other figure) and writes the result to an [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink).</span></span> <span data-ttu-id="076b3-233">O exemplo de código a seguir usa a **estrutura de tópicos** para construir uma geometria equivalente sem nenhuma interseção.</span><span class="sxs-lookup"><span data-stu-id="076b3-233">The following code example uses **Outline** to construct an equivalent geometry without any self-intersections.</span></span> <span data-ttu-id="076b3-234">Ele usa a tolerância de nivelamento padrão.</span><span class="sxs-lookup"><span data-stu-id="076b3-234">It uses the default flattening tolerance.</span></span>


```C++
HRESULT D2DOutline(
    ID2D1Geometry *pGeometry,
    ID2D1Geometry **ppGeometry
    )
{
    HRESULT hr;
    ID2D1Factory *pFactory = NULL;
    pGeometry->GetFactory(&pFactory);

    ID2D1PathGeometry *pPathGeometry = NULL;
    hr = pFactory->CreatePathGeometry(&pPathGeometry);

    if (SUCCEEDED(hr))
    {
        ID2D1GeometrySink *pSink = NULL;
        hr = pPathGeometry->Open(&pSink);

        if (SUCCEEDED(hr))
        {
            hr = pGeometry->Outline(NULL, pSink);

            if (SUCCEEDED(hr))
            {
                hr = pSink->Close();

                if (SUCCEEDED(hr))
                {
                    *ppGeometry = pPathGeometry;
                    (*ppGeometry)->AddRef();
                }
            }
            pSink->Release();
        }
        pPathGeometry->Release();
    }

    pFactory->Release();

    return hr;
}
```



### <a name="getbounds-and-getwidenedbounds"></a><span data-ttu-id="076b3-235">GetBounds e GetWidenedBounds</span><span class="sxs-lookup"><span data-stu-id="076b3-235">GetBounds and GetWidenedBounds</span></span>

<span data-ttu-id="076b3-236">O método [**GetBounds**](/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1gdimetafile-getbounds) recupera os limites da geometria.</span><span class="sxs-lookup"><span data-stu-id="076b3-236">The [**GetBounds**](/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1gdimetafile-getbounds) method retrieves the bounds of the geometry.</span></span> <span data-ttu-id="076b3-237">O exemplo de código a seguir usa **GetBounds** para recuperar os limites de um círculo especificado **( \_ m pCircleGeometry1**).</span><span class="sxs-lookup"><span data-stu-id="076b3-237">The following code example uses **GetBounds** to retrieve the bounds of a specified circle (**m\_pCircleGeometry1**).</span></span>


```C++
D2D1_RECT_F bounds;

hr = m_pCircleGeometry1->GetBounds(
      D2D1::IdentityMatrix(),
      &bounds
     );

if (SUCCEEDED(hr))
{
    // Retrieve the bounds.
}
```



<span data-ttu-id="076b3-238">O método [**GetWidenedBounds**](id2d1geometry-getwidenedbounds.md) recupera os limites da geometria depois que ela é ampliada pela largura e pelo estilo do traço especificado e transformada pela matriz especificada.</span><span class="sxs-lookup"><span data-stu-id="076b3-238">The [**GetWidenedBounds**](id2d1geometry-getwidenedbounds.md) method retrieves the bounds of the geometry after it is widened by the specified stroke width and style and transformed by the specified matrix.</span></span> <span data-ttu-id="076b3-239">O exemplo de código a seguir usa **GetWidenedBounds** para recuperar os limites de um círculo especificado (**m \_ pCircleGeometry1**) depois que ele é ampliado pela largura de traço especificada.</span><span class="sxs-lookup"><span data-stu-id="076b3-239">The following code example uses **GetWidenedBounds** to retrieve the bounds of a specified circle (**m\_pCircleGeometry1**) after it is widened by the specified stroke width.</span></span>


```C++
float dashes[] = {1.f, 1.f, 2.f, 3.f, 5.f};

m_pD2DFactory->CreateStrokeStyle(
    D2D1::StrokeStyleProperties(
        D2D1_CAP_STYLE_FLAT,
        D2D1_CAP_STYLE_FLAT,
        D2D1_CAP_STYLE_ROUND,
        D2D1_LINE_JOIN_ROUND,   // lineJoin
        10.f,   //miterLimit
        D2D1_DASH_STYLE_CUSTOM,
        0.f     //dashOffset
        ),
     dashes,
     ARRAYSIZE(dashes)-1,
     &m_pStrokeStyle
     );
```




```C++
D2D1_RECT_F bounds1;
hr = m_pCircleGeometry1->GetWidenedBounds(
      5.0,
      m_pStrokeStyle,
      D2D1::IdentityMatrix(),
      &bounds1
     );
if (SUCCEEDED(hr))
{
    // Retrieve the widened bounds.
}
```



### <a name="computepointatlength"></a><span data-ttu-id="076b3-240">ComputePointAtLength</span><span class="sxs-lookup"><span data-stu-id="076b3-240">ComputePointAtLength</span></span>

<span data-ttu-id="076b3-241">O método [**ComputePointAtLength**](id2d1geometry-computepointatlength.md) calcula o ponto e o vetor tangente na distância especificada ao longo da geometria.</span><span class="sxs-lookup"><span data-stu-id="076b3-241">The [**ComputePointAtLength**](id2d1geometry-computepointatlength.md) method calculates the point and tangent vector at the specified distance along the geometry.</span></span> <span data-ttu-id="076b3-242">O exemplo de código a seguir usa **ComputePointAtLength**.</span><span class="sxs-lookup"><span data-stu-id="076b3-242">The following code example uses **ComputePointAtLength**.</span></span>


```C++
D2D1_POINT_2F point;
D2D1_POINT_2F tangent;

hr = m_pCircleGeometry1->ComputePointAtLength(
    10, 
    NULL, 
    &point, 
    &tangent); 
```



## <a name="related-topics"></a><span data-ttu-id="076b3-243">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="076b3-243">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="076b3-244">Visão geral de geometrias de caminho</span><span class="sxs-lookup"><span data-stu-id="076b3-244">Path Geometries Overview</span></span>](path-geometries-overview.md)
</dt> <dt>

[<span data-ttu-id="076b3-245">Referência de Direct2D</span><span class="sxs-lookup"><span data-stu-id="076b3-245">Direct2D Reference</span></span>](reference.md)
</dt> </dl>

 

 