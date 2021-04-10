---
title: Como converter um objeto
description: Mostra como converter um objeto.
ms.assetid: 0fc48801-de14-4398-816d-6e7ddf4ffdd7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9ab7921e6de3286f3e1b5cf7e3da8571815848d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294377"
---
# <a name="how-to-translate-an-object"></a>Como converter um objeto

Converter um objeto 2D é mover o objeto ao longo do eixo x, do eixo y ou de ambos. Você pode chamar qualquer um dos dois métodos a seguir para criar uma transformação de tradução.

-   [**Translation (tamanho do d2d1 \_ tamanho \_ F)**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-translation(d2d1_size_f)): usa um par ordenado que define a distância a ser transvertida ao longo do eixo x e do eixo y.
-   [**Translação (float x, float y)**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-translation(float_float)): usa a distância para converter ao longo do eixo x e a distância a ser transvertida ao longo do eixo y.

O código a seguir cria uma matriz de transformação de tradução que move as 20 unidades quadradas para a direita ao longo do eixo x e 10 unidades para baixo ao longo do eixo y.


```C++
    // Create a rectangle.
    D2D1_RECT_F rectangle = D2D1::Rect(126.0f, 80.5f, 186.0f, 140.5f);

    // Draw the outline of the rectangle.
    m_pRenderTarget->DrawRectangle(
        rectangle,
        m_pOriginalShapeBrush,
        1.0f,
        m_pStrokeStyleDash
        );

    // Apply the translation transform to the render target.
    m_pRenderTarget->SetTransform(D2D1::Matrix3x2F::Translation(20, 10));

    // Paint the interior of the rectangle.
    m_pRenderTarget->FillRectangle(rectangle, m_pFillBrush);

    // Draw the outline of the rectangle.
    m_pRenderTarget->DrawRectangle(rectangle, m_pTransformedShapeBrush);
```



A ilustração a seguir mostra o efeito de aplicar a transformação translação ao quadrado, em que o quadrado original é um contorno pontilhado e o quadrado traduzido é uma estrutura de tópicos sólida.

![ilustração de um quadrado moveu 20 unidades para a direita ao longo do eixo x e 10 unidades para baixo ao longo do eixo y](images/translation-ovw.png)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de Direct2D](reference.md)
</dt> <dt>

[Visão geral das transformações do Direct2D](direct2d-transforms-overview.md)
</dt> </dl>

 

 