---
title: 'Visão geral de geometrias '
description: Descreve os conceitos básicos Direct2D geometrias, objetos que você pode usar para representar, manipular e analisar formas.
ms.assetid: f5870d4b-dd30-4034-884e-1c398a6865c6
keywords:
- Direct2D,visão geral de geometrias
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: d3f8cd7420325fd876897d538ea9e01a5c0adb64b2d0c55437514773904d6013
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117825797"
---
# <a name="geometries-overview"></a>Visão geral de geometrias 

Esta visão geral descreve como criar e usar [**objetos ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) para definir e manipular figuras 2D. Ele contém as seguintes seções:

## <a name="what-is-a-direct2d-geometry"></a>O que é uma Direct2D geometria?

Uma Direct2D geometria é um [**objeto ID2D1Geometry.**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) Esse objeto pode ser uma geometria simples ([**ID2D1RectangleGeometry,**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry) [**ID2D1RoundedRectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1roundedrectanglegeometry)ou [**ID2D1EllipseGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1ellipsegeometry)), uma geometria de caminho ([**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry)) ou uma geometria composta ([**ID2D1GeometryGroup**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrygroup) e [**ID2D1TransformedGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1transformedgeometry)).

Direct2D geometrias permitem descrever figuras bidimensionais e oferecer muitos usos, como definir regiões de teste de acerto, regiões de clipe e até mesmo caminhos de animação.

Direct2D geometrias são recursos imutáveis e independentes de dispositivo criados por [**ID2D1Factory.**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) Em geral, você deve criar geometrias uma vez e mantê-las durante a vida útil do aplicativo ou até que elas tenham que ser alteradas. Para obter mais informações sobre recursos dependentes de dispositivo e independentes de dispositivo, consulte Visão [geral de recursos.](resources-and-resource-domains.md)

As seções a seguir descrevem os diferentes tipos de geometrias.

## <a name="simple-geometries"></a>Geometrias simples

Geometrias simples incluem [**objetos ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry), [**ID2D1RoundedRectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1roundedrectanglegeometry)e [**ID2D1EllipseGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1ellipsegeometry) e podem ser usadas para criar figuras geométricas básicas, como retângulos, retângulos arredondados, círculos e reellipses.

Para criar uma geometria simples, use um dos métodos [**Geometry Geometry>Type<ID2D1Factory::Create<*geometryType.***](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) Esses métodos criam um objeto do tipo especificado. Por exemplo, para criar um retângulo, chame [**ID2D1Factory::CreateRectangleGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createrectanglegeometry(constd2d1_rect_f_id2d1rectanglegeometry)), que retorna um [**objeto ID2D1RectangleGeometry;**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry) para criar um retângulo arredondado, chame [**ID2D1Factory::CreateRoundedRectangleGeometry**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-createroundedrectanglegeometry(constd2d1_rounded_rect__id2d1roundedrectanglegeometry)), que retorna um [**objeto ID2D1RoundedRectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1roundedrectanglegeometry) e assim por diante.

O exemplo de código a seguir chama o método [**CreateEllipseGeometry,**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-createellipsegeometry(constd2d1_ellipse__id2d1ellipsegeometry)) passando uma estrutura de elipse com o centro definido como (100, 100), *x-radius* como 100 e *y-radius* como 50.  Em seguida, ele chama [**DrawGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry), passando a geometria de elipse retornada, um ponteiro para um [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush)preto e uma largura de traço de 5. A ilustração a seguir mostra a saída do exemplo de código.

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



Para desenhar o contorno de qualquer geometria, use o [**método DrawGeometry.**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) Para pintar seu interior, use o [**método FillGeometry.**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry)

## <a name="path-geometries"></a>Geometrias de caminho

As geometrias de caminho são representadas pela interface [**ID2D1PathGeometry.**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) Esses objetos podem ser usados para descrever figuras geométricas complexas compostas por segmentos, como arcos, curvas e linhas. A ilustração a seguir mostra um desenho criado usando geometria de caminho.

![ilustração de um rio, rio e o sol](images/path-geo-mnts.png)

Para obter mais informações e exemplos, consulte Visão [geral de geometrias de caminho](path-geometries-overview.md).

## <a name="composite-geometries"></a>Geometrias compostas

Uma geometria composta é uma geometria agrupada ou combinada com outro objeto de geometria ou com uma transformação. As geometrias compostas [**incluem objetos ID2D1TransformedGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1transformedgeometry) [**e ID2D1GeometryGroup.**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrygroup)

### <a name="geometry-groups"></a>Grupos de geometria

Grupos de geometria são uma maneira conveniente de agrupar várias geometrias ao mesmo tempo para que todas as figuras de várias geometrias distintas sejam concatenadas em uma. Para criar um objeto [**ID2D1GeometryGroup,**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrygroup) chame o método [**CreateGeometryGroup**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-creategeometrygroup) no objeto [**ID2D1Factory,**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) passando o *fillMode* com possíveis valores de [**D2D1 \_ FILL MODE \_ \_ ALTERNATE**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_fill_mode) (alternativo) e **D2D1 \_ FILL MODE \_ \_ WINDING**, uma matriz de objetos geometry a adicionar ao grupo geometry e o número de elementos nessa matriz.

O exemplo de código a seguir primeiro declara uma matriz de objetos geometry. Esses objetos são quatro círculos concêntricos que têm os seguintes raios: 25, 50, 75 e 100. Em seguida, chame [**CreateGeometryGroup**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-creategeometrygroup) no objeto [**ID2D1Factory,**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) passando [**D2D1 \_ FILL MODE \_ \_ ALTERNATE**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_fill_mode), uma matriz de objetos geometry para adicionar ao grupo de geometria e o número de elementos nessa matriz.


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

A ilustração a seguir mostra os resultados da renderização das duas geometrias de grupo do exemplo.

![ilustração de dois conjuntos de quatro círculos concêntricos, um com anéis alternados preenchidos e outro com todos os anéis preenchidos](images/create-geometry-group.png)

### <a name="transformed-geometries"></a>Geometrias transformadas

Há várias maneiras de transformar uma geometria. Você pode usar o método [**SetTransform**](/windows/win32/api/d2d1/nf-d2d1-id2d1brush-settransform(constd2d1_matrix_3x2_f_)) de um destino de renderização para transformar tudo o que o destino de renderização desenha ou pode associar uma transformação diretamente a uma geometria usando o [**método CreateTransformedGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createtransformedgeometry(id2d1geometry_constd2d1_matrix_3x2_f_id2d1transformedgeometry)) para criar um [**ID2D1TransformedGeometry**](/previous-versions/windows/desktop/legacy/dd371304(v=vs.85)).

O método que você deve usar depende do efeito desejado. Quando você usa o destino de renderização para transformar e renderizar uma geometria, a transformação afeta tudo sobre a geometria, incluindo a largura de qualquer traço que você aplicou. Por outro lado, quando você usa um [**ID2D1TransformedGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1transformedgeometry), a transformação afeta apenas as coordenadas que descrevem a forma. A transformação não afetará a espessura do traço quando a geometria for desenhada.

> [!Note]  
> A partir Windows 8 transformação do mundo não afetará a espessura do traço de traços com [**D2D1 \_ STROKE TRANSFORM TYPE \_ \_ \_ FIXED**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_stroke_transform_type)ou [**D2D1 \_ STROKE TRANSFORM TYPE \_ \_ \_ HAIRLINE**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_stroke_transform_type). Você deve usar esses tipos de transformação para obter traços independentes de transformação

 

O exemplo a seguir cria [**um ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry)e, em seguida, o desenha sem transformá-lo. Ele produz a saída mostrada na ilustração a seguir.

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



O exemplo a seguir usa o destino de renderização para dimensionar a geometria em um fator de 3 e, em seguida, desenha-a. A ilustração a seguir mostra o resultado do desenho do retângulo sem a transformação e com a transformação. Observe que o traço é mais espesso após a transformação, mesmo que a espessura do traço seja 1.

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



O exemplo a seguir usa [**o método CreateTransformedGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createtransformedgeometry(id2d1geometry_constd2d1_matrix_3x2_f__id2d1transformedgeometry)) para dimensionar a geometria em um fator de 3 e, em seguida, desenha-a. Ele produz a saída mostrada na ilustração a seguir. Observe que, embora o retângulo seja maior, seu traço não aumentou.

![ilustração de um retângulo menor dentro de um retângulo maior com a mesma espessura de traço](images/transformedgeometry2-step3.png)


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



## <a name="geometries-as-masks"></a>Geometrias como máscaras

Você pode usar um [**objeto ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) como uma máscara geométrica ao chamar o [**método PushLayer.**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) A máscara geométrica especifica a área da camada composta no destino de renderização. Para obter mais informações, consulte a seção Máscaras Geométricas da Visão [geral de camadas](direct2d-layers-overview.md).

## <a name="geometric-operations"></a>Operações geométricas

A interface [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) fornece várias operações geométricas que você pode usar para manipular e medir figuras geométricas. Por exemplo, você pode usá-los para calcular e retornar seus limites, comparar para ver como uma geometria está espacialmente relacionada a outra (útil para testes de acerto), calcular as áreas e comprimentos e muito mais. A tabela a seguir descreve as operações geométricas comuns.



| Operação                                                   | Método                                                                                                                                                                     |
|-------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Combinar                                                     | [**CombineWithGeometry**](id2d1geometry-combinewithgeometry.md)                                                                                                           |
| Limites/limites ampliados/recuperar limites, atualização de região suja | [**Widen,**](id2d1geometry-widen.md) [**GetBounds,**](/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1gdimetafile-getbounds) [**GetWidenedBounds**](id2d1geometry-getwidenedbounds.md)                             |
| Testes de clique                                                 | [**FillContainsPoint,**](id2d1geometry-fillcontainspoint.md) [ **StrokeContainsPoint**](id2d1geometry-strokecontainspoint.md)                                             |
| Traço                                                      | [**StrokeContainsPoint**](id2d1geometry-strokecontainspoint.md)                                                                                                           |
| Comparação                                                  | [**CompareWithGeometry**](id2d1geometry-comparewithgeometry.md)                                                                                                           |
| Simplificação (remove arcos e curvas quadráticas de Bézier)   | [**Simplificar**](id2d1geometry-simplify.md)                                                                                                                                 |
| Mosaico                                                | [**Tessellate**](id2d1geometry-tessellate.md)                                                                                                                             |
| Contorno (remover interseção)                               | [**Contorno**](id2d1geometry-outline.md)                                                                                                                                   |
| Calcular a área ou o comprimento de uma geometria                  | [**ComputeArea**](id2d1geometry-computearea.md), [**ComputeLength,**](id2d1geometry-computelength.md) [**ComputePointAtLength**](id2d1geometry-computepointatlength.md) |



 

> [!Note]  
> Começando no Windows 8, você pode usar o método [**ComputePointAndSegmentAtLength**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1pathgeometry1-computepointandsegmentatlength(float_uint32_constd2d1_matrix_3x2_f_float_d2d1_point_description)) no [**ID2D1PathGeometry1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1pathgeometry1) para calcular a área ou o comprimento de uma geometria.

 

### <a name="combining-geometries"></a>Combinando geometrias

Para combinar uma geometria com outra, chame o [**método ID2D1Geometry::CombineWithGeometry.**](id2d1geometry-combinewithgeometry.md) Ao combinar as geometrias, você especifica uma das quatro maneiras de executar a operação de combinação: [**D2D1 \_ COMBINE \_ MODE \_ UNION**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_combine_mode) (união), [**D2D1 \_ COMBINE MODE \_ \_ INTERSECT**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_combine_mode) (intersect), [**D2D1 \_ COMBINE MODE \_ \_ XOR**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_combine_mode) (xor) e [**D2D1 \_ COMBINE MODE EXCLUDE \_ \_ (excluir).**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_combine_mode) O exemplo de código a seguir mostra dois círculos combinados usando o modo de combinação de união, em que o primeiro círculo tem o ponto central de (75, 75) e o raio de 50 e o segundo círculo tem o ponto central de (125, 75) e o raio de 50.


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



A ilustração a seguir mostra dois círculos combinados com um modo de combinação de união.

![ilustração de dois círculos sobrepostos combinados em uma união](images/combine-mode-union.png)

Para ilustrações de todos os modos de combinação, consulte a [**\_ \_ enumeração D2D1 COMBINE MODE**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_combine_mode).

### <a name="widen"></a>Ampliar

O [**método Widen**](id2d1geometry-widen.md) gera uma nova geometria cujo preenchimento é equivalente à geometria existente e, em seguida, grava o resultado no objeto [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink) especificado. O exemplo de código a seguir chama [**Open**](/windows/win32/api/d2d1/nf-d2d1-id2d1pathgeometry-open) no objeto [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) . Se **abrir** for executado com sucesso, ele chamará **ampliação** no objeto Geometry.


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



### <a name="tessellate"></a>Incluí

O método [**incluí**](id2d1geometry-tessellate.md) cria um conjunto de triângulos de rotação horária que cobrem a geometria depois que ela é transformada usando a matriz especificada e achatada usando a tolerância especificada. O exemplo de código a seguir usa **incluí** para criar uma lista de triângulos que representam *pPathGeometry*. Os triângulos são armazenados em um [**ID2D1Mesh**](/windows/win32/api/d2d1/nn-d2d1-id2d1mesh), *pMesh*, então transferidos para um membro de classe, *m \_ pStrokeMesh*, para uso posterior durante a renderização.


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



### <a name="fillcontainspoint-and-strokecontainspoint"></a>FillContainsPoint e StrokeContainsPoint

O método [**FillContainsPoint**](id2d1geometry-fillcontainspoint.md) indica se a área preenchida pela geometria contém o ponto especificado. Você pode usar esse método para fazer testes de clique. O exemplo de código a seguir chama **FillContainsPoint** em um objeto [**ID2D1EllipseGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1ellipsegeometry) , passando um ponto em (0, 0) e uma matriz de [**identidade**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-isidentity) .


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



O método [**StrokeContainsPoint**](id2d1geometry-strokecontainspoint.md) determina se o traço da geometria contém o ponto especificado. Você pode usar esse método para fazer testes de clique. O exemplo de código a seguir usa **StrokeContainsPoint**.


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



### <a name="simplify"></a>Simplificar o 

O método [**simplificar**](id2d1geometry-simplify.md) remove arcos e curvas de Bezier quadrática de uma geometria especificada. Portanto, a geometria resultante contém apenas linhas e, opcionalmente, curvas Bézier cúbicas. O exemplo de código a seguir usa **simplificação** para transformar uma geometria com curvas de Bézier em uma geometria que contém apenas segmentos de linha.


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



### <a name="computelength-and-computearea"></a>ComputeLength e ComputeArea

O método [**ComputeLength**](id2d1geometry-computelength.md) calcula o comprimento da geometria especificada se cada segmento não tiver sido revertido em uma linha. Isso incluirá o segmento de fechamento implícito se a geometria for fechada. O exemplo de código a seguir usa **ComputeLength** para calcular o comprimento de um círculo especificado (**m \_ pCircleGeometry1**).


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



O método [**ComputeArea**](id2d1geometry-computearea.md) calcula a área da geometria especificada. O exemplo de código a seguir usa **ComputeArea** para calcular a área de um círculo especificado (**m \_ pCircleGeometry1**).


```C++
float area;

// Compute the area of circle1
hr = m_pCircleGeometry1->ComputeArea(
    D2D1::IdentityMatrix(),
    &area
    );
```



### <a name="comparewithgeometry"></a>CompareWithGeometry

O método [**CompareWithGeometry**](id2d1geometry-comparewithgeometry.md) descreve a interseção entre a geometria que chama esse método e a geometria especificada. Os valores possíveis para interseção incluem [**a \_ relação de geometria \_ \_ de d2d1**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_geometry_relation) (não junção), a **relação de geometria de d2d1 \_ \_ \_ está \_ contida** (está contida), **d2d1 a relação de \_ geometria \_ \_ contém** (contém) e **\_ \_ \_ sobreposição de relação de geometria de d2d1** (sobreposição). "não contíguo" significa que dois preenchimentos de geometria não fazem interseção. "is contained" significa que a geometria está completamente contida na geometria especificada. "Contains" significa que a geometria contém completamente a geometria especificada e "sobreposição" significa que as duas geometrias se sobrepõem, mas nenhuma delas contém completamente a outra.

O exemplo de código a seguir mostra como comparar dois círculos que têm o mesmo raio de 50, mas que são compensados por 50.


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



### <a name="outline"></a>Contorno

O método de [**estrutura de tópicos**](id2d1geometry-outline.md) computa o contorno da geometria (uma versão da geometria na qual nenhuma figura cruza a si mesma ou qualquer outra figura) e grava o resultado em um [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink). O exemplo de código a seguir usa a **estrutura de tópicos** para construir uma geometria equivalente sem nenhuma interseção. Ele usa a tolerância de nivelamento padrão.


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



### <a name="getbounds-and-getwidenedbounds"></a>GetBounds e GetWidenedBounds

O método [**GetBounds**](/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1gdimetafile-getbounds) recupera os limites da geometria. O exemplo de código a seguir usa **GetBounds** para recuperar os limites de um círculo especificado **( \_ m pCircleGeometry1**).


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



O método [**GetWidenedBounds**](id2d1geometry-getwidenedbounds.md) recupera os limites da geometria depois que ela é ampliada pela largura e pelo estilo do traço especificado e transformada pela matriz especificada. O exemplo de código a seguir usa **GetWidenedBounds** para recuperar os limites de um círculo especificado (**m \_ pCircleGeometry1**) depois que ele é ampliado pela largura de traço especificada.


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



### <a name="computepointatlength"></a>ComputePointAtLength

O método [**ComputePointAtLength**](id2d1geometry-computepointatlength.md) calcula o ponto e o vetor tangente na distância especificada ao longo da geometria. O exemplo de código a seguir usa **ComputePointAtLength**.


```C++
D2D1_POINT_2F point;
D2D1_POINT_2F tangent;

hr = m_pCircleGeometry1->ComputePointAtLength(
    10, 
    NULL, 
    &point, 
    &tangent); 
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Visão geral de geometrias de caminho](path-geometries-overview.md)
</dt> <dt>

[Direct2D Referência](reference.md)
</dt> </dl>

 

 