---
title: Métodos ID2D1Factory CreateTransformedGeometry (D2d1. h)
description: Transforma a geometria especificada e armazena o resultado como um objeto ID2D1TransformedGeometry.
ms.assetid: 71f26200-0f35-49d7-951d-2962768d16bc
keywords:
- Métodos CreateTransformedGeometry Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 5da3b548c3118209c915714e03fe9e4061c77e96
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757710"
---
# <a name="id2d1factorycreatetransformedgeometry-methods"></a>Métodos ID2D1Factory:: CreateTransformedGeometry

Transforma a geometria especificada e armazena o resultado como um objeto [**ID2D1TransformedGeometry**](/previous-versions/windows/desktop/legacy/dd371304(v=vs.85)) .

### <a name="overload-list"></a>Lista de sobrecargas



| Método                                                                                                                                                                                                                  | Descrição                                                                                                                                    |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateTransformedGeometry (ID2D1Geometry \* , D2D \_ Matrix \_ 3x2 \_ F \* , ID2D1TransformedGeometry \* \* )**](/previous-versions/windows/desktop/legacy/dd371304(v=vs.85)) | Transforma a geometria especificada e armazena o resultado como um objeto [**ID2D1TransformedGeometry**](/previous-versions/windows/desktop/legacy/dd371304(v=vs.85)) . <br/> |
| [**CreateTransformedGeometry (ID2D1Geometry \* , D2D \_ Matrix \_ 3x2 \_ F&, ID2D1TransformedGeometry \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createtransformedgeometry(id2d1geometry_constd2d1_matrix_3x2_f__id2d1transformedgeometry))  | Transforma a geometria especificada e armazena o resultado como um objeto [**ID2D1TransformedGeometry**](/previous-versions/windows/desktop/legacy/dd371304(v=vs.85)) . <br/> |



## <a name="remarks"></a>Comentários

Assim como outros recursos, uma geometria transformada herda o espaço de recursos e a política de Threading da fábrica que o criou. Esse objeto é imutável.

Ao traçar uma geometria transformada com o método [**DrawGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) , a largura do traço não é afetada pela transformação aplicada à geometria. A largura do traço só é afetada pela transformação do mundo.

## <a name="examples"></a>Exemplos

O exemplo a seguir cria um [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createrectanglegeometry(constd2d1_rect_f_id2d1rectanglegeometry))e, em seguida, o Desenha sem transformá-lo. Ele produz a saída mostrada na ilustração a seguir.

![ilustração de um retângulo](images/transformedgeometry2-step1.png)


```C++
hr = m_pD2DFactory->CreateRectangleGeometry(
    D2D1::RectF(150.f, 150.f, 200.f, 200.f),
    &m_pRectangleGeometry
    );
```



O exemplo a seguir usa o destino render para dimensionar a geometria por um fator de 3 e, em seguida, a desenha. A ilustração a seguir mostra o resultado do desenho do retângulo sem a transformação e com a transformação; observa que o traço é mais espesso após a transformação, embora a espessura do traço seja 1.

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



O exemplo a seguir usa o método **CreateTransformedGeometry** para dimensionar a geometria por um fator de 3 e, em seguida, a desenha. Ele produz a saída mostrada na ilustração a seguir. Observe que, embora o retângulo seja maior, seu traço ainda não aumentou.

![ilustração de um retângulo menor dentro de um retângulo maior com o mesmo traço](images/transformedgeometry2-step3.png)


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


// Replace the previous render target transform.
m_pRenderTarget->SetTransform(D2D1::Matrix3x2F::Identity());

// Draw the transformed geometry.
m_pRenderTarget->DrawGeometry(m_pTransformedGeometry, m_pBlackBrush, 1);
```





## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D2d1. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D2d1. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory)
</dt> </dl>
