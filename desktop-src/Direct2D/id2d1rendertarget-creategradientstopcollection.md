---
title: Métodos ID2D1RenderTarget CreateGradientStopCollection (D2d1 \_ 1. h)
description: Cria um ID2D1GradientStopCollection da matriz especificada de estruturas de \_ parada de gradiente d2d1 \_ .
ms.assetid: 674ffba5-18c5-46bf-8813-d8d13e5ba903
keywords:
- Métodos CreateGradientStopCollection Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: f099c1c71015ca433299843d388085103571d31d
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549411"
---
# <a name="id2d1rendertargetcreategradientstopcollection-methods"></a>Métodos ID2D1RenderTarget:: CreateGradientStopCollection

Cria um [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) da matriz especificada de estruturas [**de \_ \_ parada de gradiente d2d1**](/windows/win32/api/d2d1/ns-d2d1-d2d1_gradient_stop) .

### <a name="overload-list"></a>Lista de sobrecargas



| Método                                                                                                                                                                                                                                                               | Descrição                                                                                                                                                                                                                           |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateGradientStopCollection ( \_ parada de gradiente d2d1 \_ \* , D2D1 \_ gama, d2d1 \_ \_ modo de extensão, ID2D1GradientStopCollection \* \* )**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) | Cria um [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) a partir das interrupções de gradiente especificadas, da interpolação de cor gama e do modo de extensão. <br/>                                                              |
| [**CreateGradientStopCollection ( \_ parada de gradiente d2d1 \_ \* , ID2D1GradientStopCollection \* \* )**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection)                                                            | Cria um [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) a partir das interrupções de gradiente especificadas que usa o gama de interpolação de cor [**d2d1 \_ gama \_ 2 \_ 2**](/windows/win32/api/d2d1/ne-d2d1-d2d1_gamma) e o modo de extensão fixe.<br/> |



## <a name="examples"></a>Exemplos

O exemplo a seguir cria uma matriz de interrupções de gradiente e as usa para criar um [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection).


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



O próximo exemplo de código usa o [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) para criar um [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush).


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



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D2d1 \_ 1. h (inclui D2d1. h)</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D2d1. lib</dt> </dl>                   |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl>                   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> <dt>

[**\_Parada de gradiente d2d1 \_**](/windows/win32/api/d2d1/ns-d2d1-d2d1_gradient_stop)
</dt> <dt>

[Como criar um pincel de gradiente linear](how-to-create-a-linear-gradient-brush.md)
</dt> <dt>

[Como criar um pincel gradiente radial](how-to-create-a-radial-gradient-brush.md)
</dt> <dt>

[Visão geral de pincéis](direct2d-brushes-overview.md)
</dt> </dl>