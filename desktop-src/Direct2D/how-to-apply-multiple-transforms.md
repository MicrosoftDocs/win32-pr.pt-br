---
title: Como aplicar várias transformações a um objeto
description: Mostra como aplicar várias transformações a um objeto.
ms.assetid: a3875072-bb73-4698-944e-102ab5539d80
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d63db7899b79dd07a6a4a14a4efbbfaeefc5723ad09c71a3462ba5d2fd0c042
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119259677"
---
# <a name="how-to-apply-multiple-transforms-to-an-object"></a>Como aplicar várias transformações a um objeto

Executar várias transformações em um objeto significa combinar várias transformações em uma. Ou seja, pegar a saída de cada matriz de transformação e usá-la como entrada para a próxima, obtendo, assim, os efeitos cumulativos de todas as transformações de matriz.

Suponha que duas matrizes de transformação, rotação e translação sejam multiplicadas juntas. O resultado é uma nova matriz que executa as funções de rotação e translação. Como a multiplicação de matriz não é comutada, uma transformação de rotação multiplicada por uma transformação de tradução é diferente da transformação de tradução multiplicada pela transformação de rotação.

Os exemplos de código a seguir mostram como aplicar a rotação seguida pela tradução e, em seguida, a tradução seguida por rotação. Observe que os resultados da renderização são diferentes.


```C++
D2D1_RECT_F rectangle = D2D1::RectF(300.0f, 40.0f, 360.0f, 100.0f);

// Draw the rectangle before transforming the render target.

m_pRenderTarget->DrawRectangle(
    rectangle,
    m_pOriginalShapeBrush,
    1.0f,
    m_pStrokeStyleDash
    );

D2D1_MATRIX_3X2_F rotation = D2D1::Matrix3x2F::Rotation(
    45.0f,
    D2D1::Point2F(330.0f, 70.0f)
    );


D2D1_MATRIX_3X2_F translation = D2D1::Matrix3x2F::Translation(20.0f, 10.0f);

// First rotate about the center of the square and then move
// 20 pixels to the right along the x-axis
// and 10 pixels downward along the y-axis.
m_pRenderTarget->SetTransform(rotation* translation);

// Draw the rectangle in the transformed space.
m_pRenderTarget->FillRectangle(rectangle, m_pFillBrush);
m_pRenderTarget->DrawRectangle(rectangle, m_pTransformedShapeBrush, 1.0f);
```




```C++
D2D1_RECT_F rectangle = D2D1::Rect(40.0f, 40.0f, 100.0f, 100.0f);

// Draw a rectangle without transforming it.
m_pRenderTarget->DrawRectangle(
    rectangle,
    m_pOriginalShapeBrush,
    1.0f,
    m_pStrokeStyleDash
    );

D2D1_MATRIX_3X2_F translation = D2D1::Matrix3x2F::Translation(20.0f, 10.0f);

m_pRenderTarget->SetTransform(translation);

D2D1_MATRIX_3X2_F rotation = D2D1::Matrix3x2F::Rotation(
    45.0f,
    D2D1::Point2F(70.0f, 70.0f)
    );

// First move 20 pixels to the right along the x-axis and
// 10 pixels downward along the y-axis,
// and then rotate about the center of the original square.
m_pRenderTarget->SetTransform(translation * rotation);

// Draw the rectangle in the transformed space.
m_pRenderTarget->FillRectangle(rectangle, m_pFillBrush);
m_pRenderTarget->DrawRectangle(rectangle, m_pTransformedShapeBrush);
```



O código produz a saída mostrada na ilustração a seguir.

![ilustração de um retângulo que foi traduzido e girado e um retângulo que foi girado e, em seguida, traduzido](images/multipletransforms.png)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Direct2D Referência](reference.md)
</dt> <dt>

[Direct2D Visão geral das transformações](direct2d-transforms-overview.md)
</dt> </dl>

 

 




