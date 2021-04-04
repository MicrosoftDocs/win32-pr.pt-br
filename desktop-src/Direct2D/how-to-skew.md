---
title: Como distorcer um objeto
description: Mostra como distorcer um objeto.
ms.assetid: bdc12ca3-eb0d-49ab-8ef7-f42f24fef7ff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 691062e64d4255b1e2f7711b5ff700d72fd90063
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103823920"
---
# <a name="how-to-skew-an-object"></a>Como distorcer um objeto

Para distorcer (ou distorcer) um objeto significa distorcer um objeto por um ângulo especificado do eixo x, do eixo y ou de ambos. Por exemplo, quando você distorce um quadrado, ele se transforma em um paralelogramo.

O método [**Matrix3x2F:: skew**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-skew) usa 3 parâmetros:

-   *angleX*: o ângulo de inclinação do eixo x, que é medido em graus no sentido anti-horário do eixo y.
-   *incline*: o ângulo de inclinação do eixo y, que é medido em graus no sentido horário a partir do eixo x.
-   *centerPoint*: o ponto sobre o qual a distorção é executada.

Para prever o efeito de uma transformação de distorção, considere que *angleX* é o ângulo de distorção medido em graus no sentido anti-horário do eixo y. Por exemplo, se *angleX* for definido como 30, o objeto distorcerá 30 graus no sentido anti-horário ao longo do eixo y sobre o *centerPoint*. A ilustração a seguir mostra um quadrado inclinado horizontalmente em 30 graus sobre o canto superior esquerdo do quadrado.

![ilustração de um quadrado inclinado em 30 graus no sentido anti-horário do eixo y](images/skewx.png)

Da mesma *forma, a* inclinação é um ângulo de distorção medido em graus no sentido horário a partir do eixo x. Por exemplo, se *incline* for definido como 30, o objeto distorcerá 30 graus no sentido horário ao longo do eixo x sobre o *centerPoint*. A ilustração a seguir mostra um quadrado inclinado verticalmente em 30 graus sobre o canto superior esquerdo do quadrado.

![ilustração de um quadrado distorcido 30 graus no sentido horário a partir do eixo x](images/skewy.png)

Se você definir *angleX* e *angulares* como 30 graus e o *centerPoint* para o canto superior esquerdo do quadrado, você verá o seguinte quadrado inclinado (sólido contorno). Observe que o quadrado inclinado é distorcido em 30 graus no sentido anti-horário do eixo y e 30 graus no sentido horário do eixo x.

![ilustração de um quadrado inclinado em 30 graus no sentido anti-horário do eixo y e 30 graus no sentido horário do eixo x](images/skewxy.png)

O exemplo de código a seguir inclina o quadrado de 45 graus horizontalmente sobre o canto superior esquerdo do quadrado.


```C++
    // Create a rectangle.
    D2D1_RECT_F rectangle = D2D1::Rect(126.0f, 301.5f, 186.0f, 361.5f);

    // Draw the outline of the rectangle.
    m_pRenderTarget->DrawRectangle(
        rectangle,
        m_pOriginalShapeBrush,
        1.0f,
        m_pStrokeStyleDash
        );

    // Apply the skew transform to the render target.
    m_pRenderTarget->SetTransform(
        D2D1::Matrix3x2F::Skew(
            45.0f,
            0.0f,
            D2D1::Point2F(126.0f, 301.5f))
        );

    // Paint the interior of the rectangle.
    m_pRenderTarget->FillRectangle(rectangle, m_pFillBrush);

    // Draw the outline of the rectangle.
    m_pRenderTarget->DrawRectangle(rectangle, m_pTransformedShapeBrush);
```



A ilustração a seguir mostra o efeito de aplicar a transformação de distorção ao quadrado, em que o quadrado original é um contorno pontilhado e o paralelogramo (objeto inclinado) é uma estrutura de tópicos sólida. Observe que o ângulo de inclinação é 45 graus no sentido anti-horário do eixo y.

![ilustração de um quadrado distorcido 45 graus no sentido anti-horário do eixo y](images/skew-ovw.png)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Visão geral das transformações do Direct2D](direct2d-transforms-overview.md)
</dt> <dt>

[Referência de Direct2D](reference.md)
</dt> </dl>

 

 