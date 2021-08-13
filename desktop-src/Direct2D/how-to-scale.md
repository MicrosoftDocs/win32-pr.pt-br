---
title: Como dimensionar um objeto
description: Mostra como dimensionar um objeto .
ms.assetid: 3da749e2-50d5-4f4e-9ccd-8c230efe3436
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d833ea44e4a38672729dd7647063e8ed9f8de3574d820a3db40d5a848064ef15
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119259137"
---
# <a name="how-to-scale-an-object"></a>Como dimensionar um objeto

Este tópico descreve como dimensionar um objeto usando a [**classe Matrix3x2F.**](/windows/win32/api/d2d1helper/nl-d2d1helper-matrix3x2f) Dimensionar um objeto significa tornar o objeto maior ou menor. Você pode chamar um dos dois métodos a seguir para dimensionar um objeto .

-   **Matrix3x2F::Scale(D2D1 \_ SIZE \_ F scalefactor, D2D1 \_ POINT \_ 2F centerpoint)**
-   **Matrix3x2F::Scale(float scalex, float scaley, D2D1 \_ POINT \_ 2F centerpoint)**

O primeiro método armazena *scalex* e *scaley* como um par ordenado de valores de ponto flutuante na estrutura [**D2D1 \_ SIZE \_ F.**](/windows/desktop/Direct2D/d2d1-size-f) O segundo método define *scalex* e *scaley* como parâmetros individuais.

Independentemente do método usado, você deve especificar *fatores escalares* e *escalares.* O *valor scalex* é o fator de escala na direção x. Por exemplo, um *valor scalex* de 1,5 alonga o objeto para 150% ao longo do eixo x. Da mesma forma, o *valor dimensionado* é o fator de escala na direção y. Por exemplo, um *valor dimensionado* de 0,5 reduz a altura do objeto em 50% ao longo do eixo y.

Para especificar um ponto como o centro da operação de dimensionamento, use o parâmetro *centerpoint.* Por padrão, um objeto é centralizado sobre sua origem (0,0).

O código de exemplo a seguir cria uma transformação de escala para aumentar o tamanho de um quadrado para 130% de seu tamanho original. O *ponto central* está definido como o canto superior esquerdo do quadrado original.


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



A ilustração a seguir mostra o efeito da aplicação da transformação de escala ao quadrado. O quadrado original é um contorno pontilhado e o quadrado dimensionado é um contorno sólido.

![ilustração do quadrado resized para 130% de seu tamanho original](images/scale-ovw.png)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Direct2D Visão geral de transformaçãos](direct2d-transforms-overview.md)
</dt> <dt>

[Direct2D Referência](reference.md)
</dt> </dl>

 

 