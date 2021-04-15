---
title: Como dimensionar um objeto
description: Mostra como dimensionar um objeto.
ms.assetid: 3da749e2-50d5-4f4e-9ccd-8c230efe3436
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9f46ae37197cb7cbfeb3f86588e1b5298cfc467
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104454243"
---
# <a name="how-to-scale-an-object"></a>Como dimensionar um objeto

Este tópico descreve como dimensionar um objeto usando a classe [**Matrix3x2F**](/windows/win32/api/d2d1helper/nl-d2d1helper-matrix3x2f) . Dimensionar um objeto significa aumentar ou diminuir o objeto. Você pode chamar um dos dois métodos a seguir para dimensionar um objeto.

-   **Matrix3x2F:: Scale (tamanho de D2D1 \_ \_ F SCALEFACTOR, d2d1 \_ Point \_ 2F CenterPoint)**
-   **Matrix3x2F:: Scale (float ScaleX, float ScaleY, D2D1 \_ Point \_ 2F CenterPoint)**

O primeiro método armazena *ScaleX* e *ScaleY* como um par ordenado de valores de ponto flutuante na estrutura [**\_ \_ F de tamanho de d2d1**](/windows/desktop/Direct2D/d2d1-size-f) . O segundo método define *ScaleX* e *ScaleY* como parâmetros individuais.

Independentemente do método usado, você deve especificar os fatores *ScaleX* e *ScaleY* . O valor de *ScaleX* é o fator de escala na direção x. Por exemplo, um valor de *ScaleX* de 1,5 amplia o objeto para 150% ao longo do eixo x. Da mesma forma, o valor de *ScaleY* é o fator de escala na direção y. Por exemplo, um valor de *ScaleY* de 0,5 reduz a altura do objeto em 50% ao longo do eixo y.

Para especificar um ponto como o centro da operação de dimensionamento, use o parâmetro *CenterPoint* . Por padrão, um objeto é centralizado sobre sua origem (0, 0).

O código de exemplo a seguir cria uma transformação escala para aumentar o tamanho de um quadrado para 130% de seu tamanho original. O *CenterPoint* é definido para ser o canto superior esquerdo do quadrado original.


```C++
    // Create a rectangle.
    D2D1_RECT_F rectangle = D2D1::Rect(438.0f, 80.5f, 498.0f, 140.5f);

    // Draw the outline of the rectangle.
    m_pRenderTarget->DrawRectangle(
        rectangle,
        m_pOriginalShapeBrush,
        1.0f,
        m_pStrokeStyleDash
        );

    // Apply the scale transform to the render target.
    m_pRenderTarget->SetTransform(
        D2D1::Matrix3x2F::Scale(
            D2D1::Size(1.3f, 1.3f),
            D2D1::Point2F(438.0f, 80.5f))
        );

    // Paint the rectangle's interior.
    m_pRenderTarget->FillRectangle(rectangle, m_pFillBrush);

    // Draw the outline of the rectangle.
    m_pRenderTarget->DrawRectangle(rectangle, m_pTransformedShapeBrush);

```



A ilustração a seguir mostra o efeito de aplicar a transformação escala ao quadrado. O quadrado original é um contorno pontilhado e o quadrado dimensionado é uma estrutura de tópicos sólida.

![ilustração do quadrado redimensionado para 130% de seu tamanho original](images/scale-ovw.png)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Visão geral das transformações do Direct2D](direct2d-transforms-overview.md)
</dt> <dt>

[Referência de Direct2D](reference.md)
</dt> </dl>

 

 