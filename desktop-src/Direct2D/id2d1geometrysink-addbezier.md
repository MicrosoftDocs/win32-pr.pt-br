---
title: Métodos AddBezier ID2D1GeometrySink (D2d1.h)
description: Cria uma curva de Bezier cúbica entre o ponto atual e o ponto de extremidade especificado e a adiciona ao sink de geometria.
ms.assetid: d1e228eb-dac6-485d-b3c9-69b2bd45e531
keywords:
- Métodos AddBezier Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 5dff3f4a59b592b4820bf6e91f9415da98a0960cf333afc48115f894111d423b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119917816"
---
# <a name="id2d1geometrysinkaddbezier-methods"></a>Métodos ID2D1GeometrySink::AddBezier

Cria uma curva de Bezier cúbica entre o ponto atual e o ponto de extremidade especificado e a adiciona ao sink de geometria.

### <a name="overload-list"></a>Lista de sobrecargas



| Método                                                                                            | Descrição                                                                                    |
|:--------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------|
| [**AddBezier(D2D1 \_ BEZIER \_ SEGMENT&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometrysink-addbezier(constd2d1_bezier_segment_))  | Cria uma curva de Bézier cúbica entre o ponto atual e o ponto final especificado.<br/> |
| [**AddBezier(D2D1 \_ BEZIER \_ SEGMENT \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometrysink-addbezier(constd2d1_bezier_segment)) | Cria uma curva de Bezier cúbica entre o ponto atual e o ponto de extremidade especificado.<br/>  |



## <a name="examples"></a>Exemplos

O exemplo a seguir cria [**um ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry), recupera um sink e o usa para definir uma forma de ampulheta. Para ver o exemplo completo, [consulte Como desenhar e preencher uma forma complexa.](how-to-draw-and-fill-a-complex-shape.md)


```C++
ID2D1GeometrySink *pSink = NULL;



// Create a path geometry.
if (SUCCEEDED(hr))
{
    hr = m_pD2DFactory->CreatePathGeometry(&m_pPathGeometry);

    if (SUCCEEDED(hr))
    {
        // Write to the path geometry using the geometry sink.
        hr = m_pPathGeometry->Open(&pSink);

        if (SUCCEEDED(hr))
        {
            pSink->BeginFigure(
                D2D1::Point2F(0, 0),
                D2D1_FIGURE_BEGIN_FILLED
                );

            pSink->AddLine(D2D1::Point2F(200, 0));

            pSink->AddBezier(
                D2D1::BezierSegment(
                    D2D1::Point2F(150, 50),
                    D2D1::Point2F(150, 150),
                    D2D1::Point2F(200, 200))
                );

            pSink->AddLine(D2D1::Point2F(0, 200));

            pSink->AddBezier(
                D2D1::BezierSegment(
                    D2D1::Point2F(50, 150),
                    D2D1::Point2F(50, 50),
                    D2D1::Point2F(0, 0))
                );

            pSink->EndFigure(D2D1_FIGURE_END_CLOSED);

            hr = pSink->Close();
        }
        SafeRelease(&pSink);
    }
}
```





## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D2d1.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D2d1.lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ID2D1GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink)
</dt> </dl>

�

�
