---
title: Aplicar transformações em Direct2D
description: Aplicar transformações em Direct2D
ms.assetid: 4b54dcfc-f915-4e4a-aa88-ee23c341c2a4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8edddbb3150f16428c56bd4c6da828c9b2ce594e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103641109"
---
# <a name="applying-transforms-in-direct2d"></a>Aplicar transformações em Direct2D

No [desenho com Direct2D](drawing-with-direct2d.md), vimos que o método [**ID2D1RenderTarget:: FillEllipse**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse__id2d1brush)) desenha uma elipse que está alinhada aos eixos x e y. Mas suponha que você queira desenhar uma elipse inclinada em um ângulo?

![uma imagem que mostra uma elipse inclinada.](images/graphics16.png)

Usando transformações, você pode alterar uma forma das seguintes maneiras.

-   Rotação em um ponto.
-   Dimensionamento.
-   Translação (deslocamento na direção X ou Y).
-   Distorção (também conhecida como *distorção*).

Uma transformação é uma operação matemática que mapeia um conjunto de pontos para um novo conjunto de pontos. Por exemplo, o diagrama a seguir mostra um triângulo girado em volta do ponto P3. Depois que a rotação for aplicada, o ponto P1 será mapeado para P1 ', o ponto P2 será mapeado para P2 ' e o ponto P3 se mapeará para si mesmo.

![um diagrama que mostra a rotação em um ponto.](images/graphics17.png)

As transformações são implementadas usando matrizes. No entanto, você não precisa entender a matemática de matrizes para usá-las. Se você quiser saber mais sobre a matemática, consulte [Apêndice: transformações de matriz](appendix--matrix-transforms.md).

Para aplicar uma transformação em Direct2D, chame o método [**ID2D1RenderTarget:: SetTransform**](/windows/desktop/Direct2D/id2d1rendertarget-settransform) . Esse método usa uma estrutura [**d2d1 \_ matriz \_ 3x2 \_ F**](/windows/desktop/Direct2D/d2d1-matrix-3x2-f) que define a transformação. Você pode inicializar essa estrutura chamando métodos na classe [**d2d1:: Matrix3x2F**](/windows/desktop/api/d2d1helper/nl-d2d1helper-matrix3x2f) . Essa classe contém métodos estáticos que retornam uma matriz para cada tipo de transformação:

-   [**Matrix3x2F:: Rotation**](/windows/desktop/api/d2d1helper/nf-d2d1helper-matrix3x2f-rotation)
-   [**Matrix3x2F:: Scale**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-scale(d2d1_size_f_d2d1_point_2f))
-   [**Matrix3x2F:: translation**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-translation(d2d1_size_f))
-   [**Matrix3x2F:: skew**](/windows/desktop/api/d2d1helper/nf-d2d1helper-matrix3x2f-skew)

Por exemplo, o código a seguir aplica uma rotação de 20 graus ao seu ponto (100, 100).


```C++
pRenderTarget->SetTransform(
    D2D1::Matrix3x2F::Rotation(20, D2D1::Point2F(100,100)));
```

A transformação será aplicada a todas as operações de desenho posteriores até que você chame [**SetTransform**](/windows/desktop/Direct2D/id2d1rendertarget-settransform) novamente. Para remover a transformação atual, chame **SetTransform** com a matriz de identidade. Para criar a matriz de identidade, chame a função [**Matrix3x2F:: Identity**](/windows/desktop/api/d2d1helper/nf-d2d1helper-identitymatrix) .


```C++
pRenderTarget->SetTransform(D2D1::Matrix3x2F::Identity());
```

## <a name="drawing-clock-hands"></a>Mãos do relógio de desenho

Vamos colocar transformações para usar convertendo nosso programa em círculo em um relógio analógico. Podemos fazer isso adicionando linhas para as mãos.

![uma captura de tela do programa de relógio analógico.](images/graphics18.png)

Em vez de calcular as coordenadas das linhas, podemos calcular o ângulo e, em seguida, aplicar uma transformação de rotação. O código a seguir mostra uma função que desenha uma mão do relógio. O parâmetro *fAngle* fornece o ângulo da mão, em graus.

```C++
void Scene::DrawClockHand(float fHandLength, float fAngle, float fStrokeWidth)
{
    m_pRenderTarget->SetTransform(
        D2D1::Matrix3x2F::Rotation(fAngle, m_ellipse.point)
            );

    // endPoint defines one end of the hand.
    D2D_POINT_2F endPoint = D2D1::Point2F(
        m_ellipse.point.x,
        m_ellipse.point.y - (m_ellipse.radiusY * fHandLength)
        );

    // Draw a line from the center of the ellipse to endPoint.
    m_pRenderTarget->DrawLine(
        m_ellipse.point, endPoint, m_pStroke, fStrokeWidth);
}
```

Esse código desenha uma linha vertical, começando do centro da face do relógio e terminando no ponto de *extremidade*. A linha é girada ao lado do centro da elipse aplicando uma transformação de rotação. O ponto central da rotação é o centro da elipse que forma o relógio.

![um diagrama que mostra a rotação da mão do relógio.](images/graphics19.png)

O código a seguir mostra como toda a face do relógio é desenhada.

```C++
void Scene::RenderScene()
{
    m_pRenderTarget->Clear(D2D1::ColorF(D2D1::ColorF::SkyBlue));

    m_pRenderTarget->FillEllipse(m_ellipse, m_pFill);
    m_pRenderTarget->DrawEllipse(m_ellipse, m_pStroke);

    // Draw hands
    SYSTEMTIME time;
    GetLocalTime(&time);

    // 60 minutes = 30 degrees, 1 minute = 0.5 degree
    const float fHourAngle = (360.0f / 12) * (time.wHour) + (time.wMinute * 0.5f);
    const float fMinuteAngle =(360.0f / 60) * (time.wMinute);

    DrawClockHand(0.6f,  fHourAngle,   6);
    DrawClockHand(0.85f, fMinuteAngle, 4);

    // Restore the identity transformation.
    m_pRenderTarget->SetTransform( D2D1::Matrix3x2F::Identity() );
}
```

Você pode baixar o projeto completo do Visual Studio do [exemplo de relógio Direct2D](direct2d-clock-sample.md). (Apenas para diversão, a versão de download adiciona um gradiant radial à face do relógio.)

## <a name="combining-transforms"></a>Combinando transformações

As quatro transformações básicas podem ser combinadas multiplicando duas ou mais matrizes. Por exemplo, o código a seguir combina uma rotação com uma tradução.

```C++
const D2D1::Matrix3x2F rot = D2D1::Matrix3x2F::Rotation(20);
const D2D1::Matrix3x2F trans = D2D1::Matrix3x2F::Translation(40, 10);

pRenderTarget->SetTransform(rot * trans);
```

A classe [**Matrix3x2F**](/windows/desktop/api/d2d1helper/nl-d2d1helper-matrix3x2f) fornece o [**operador \* ()**](/windows/desktop/api/d2d1helper/nf-d2d1helper-matrix3x2f-operator-mult) para multiplicação de matriz. A ordem na qual você multiplica as matrizes é importante. Definir uma transformação (M × N) significa "aplicar M primeiro, seguido por N". Por exemplo, aqui está a rotação seguida da Tradução:

![um diagrama que mostra a rotação seguida pela tradução.](images/graphics20.png)

Este é o código para esta transformação:

```C++
const D2D1::Matrix3x2F rot = D2D1::Matrix3x2F::Rotation(45, center);
const D2D1::Matrix3x2F trans = D2D1::Matrix3x2F::Translation(x, 0);
pRenderTarget->SetTransform(rot * trans);
```

Agora, compare essa transformação com uma transformação na ordem inversa, a tradução seguida por rotação.

![um diagrama que mostra a tradução seguida por rotação.](images/graphics21.png)

A rotação é realizada em todo o centro do retângulo original. Este é o código para essa transformação.

```C++
D2D1::Matrix3x2F rot = D2D1::Matrix3x2F::Rotation(45, center);
D2D1::Matrix3x2F trans = D2D1::Matrix3x2F::Translation(x, 0);
pRenderTarget->SetTransform(trans * rot);
```

Como você pode ver, as matrizes são as mesmas, mas a ordem das operações foi alterada. Isso acontece porque a multiplicação de matriz não é comutada: M × N ≠ N × M.

## <a name="next"></a>Avançar

[Apêndice: transformações de matriz](appendix--matrix-transforms.md)