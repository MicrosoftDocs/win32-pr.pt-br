---
title: Como girar um objeto
description: Mostra como girar um objeto .
ms.assetid: 468e29b6-941b-4cf8-8649-9e513326ccb2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: babc84c08af759d8484c8ba85db40780f68570d93a0a8b9442e93b960ecac39c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118003518"
---
# <a name="how-to-rotate-an-object"></a>Como girar um objeto

Este tópico descreve como girar um objeto sobre um ponto especificado. Para girar um objeto, chame [**o método Matrix3x2F::Rotation.**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-rotation) Esse método aceita dois parâmetros, o ângulo especificado e o ponto central. O ângulo é um ângulo de rotação no sentido horário em graus e o ponto central é o ponto sobre o qual o objeto gira. O ponto central é expresso no sistema de coordenadas do objeto que é transformado.

Por exemplo, o código a seguir gira um quadrado de 45 graus no sentido horário sobre o centro do quadrado.


```C++
    // Create a rectangle.
    D2D1_RECT_F rectangle = D2D1::Rect(438.0f, 301.5f, 498.0f, 361.5f);

    // Draw the rectangle.
    m_pRenderTarget->DrawRectangle(
        rectangle,
        m_pOriginalShapeBrush,
        1.0f,
        m_pStrokeStyleDash
        );

    // Apply the rotation transform to the render target.
    m_pRenderTarget->SetTransform(
        D2D1::Matrix3x2F::Rotation(
            45.0f,
            D2D1::Point2F(468.0f, 331.5f))
        );

    // Fill the rectangle.
    m_pRenderTarget->FillRectangle(rectangle, m_pFillBrush);

    // Draw the transformed rectangle.
    m_pRenderTarget->DrawRectangle(rectangle, m_pTransformedShapeBrush);

```



A ilustração a seguir mostra o efeito da aplicação da transformação de rotação anterior ao quadrado. O quadrado original é um contorno pontilhado e o quadrado girado é um contorno sólido.

![ilustração de um quadrado girado no sentido horário 45 graus sobre o centro do quadrado original](images/rotate-ovw.png)

A ilustração a seguir mostra o efeito de girar pelo mesmo ângulo sobre um ponto central diferente. Observe que os objetos girados estão em posições diferentes em relação ao original. O quadrado contornado à esquerda é o resultado da rotação sobre o centro do quadrado original, e o quadrado contornado à direita é o resultado da rotação sobre o canto superior esquerdo do quadrado original.

![ilustração de um quadrado girado no sentido horário 45 graus sobre um ponto central diferente](images/translate-rotationcompare.png)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Direct2D Referência](reference.md)
</dt> <dt>

[Direct2D Visão geral de transformaçãos](direct2d-transforms-overview.md)
</dt> </dl>

 

 