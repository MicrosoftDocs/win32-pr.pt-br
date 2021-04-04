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
# <a name="how-to-skew-an-object"></a><span data-ttu-id="29776-103">Como distorcer um objeto</span><span class="sxs-lookup"><span data-stu-id="29776-103">How to Skew an Object</span></span>

<span data-ttu-id="29776-104">Para distorcer (ou distorcer) um objeto significa distorcer um objeto por um ângulo especificado do eixo x, do eixo y ou de ambos.</span><span class="sxs-lookup"><span data-stu-id="29776-104">To skew (or shear) an object means to distort an object by a specified angle from the x-axis, the y-axis, or both.</span></span> <span data-ttu-id="29776-105">Por exemplo, quando você distorce um quadrado, ele se transforma em um paralelogramo.</span><span class="sxs-lookup"><span data-stu-id="29776-105">For example, when you skew a square, it becomes a parallelogram.</span></span>

<span data-ttu-id="29776-106">O método [**Matrix3x2F:: skew**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-skew) usa 3 parâmetros:</span><span class="sxs-lookup"><span data-stu-id="29776-106">The [**Matrix3x2F::Skew**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-skew) method takes 3 parameters:</span></span>

-   <span data-ttu-id="29776-107">*angleX*: o ângulo de inclinação do eixo x, que é medido em graus no sentido anti-horário do eixo y.</span><span class="sxs-lookup"><span data-stu-id="29776-107">*angleX*: The x-axis skew angle, which is measured in degrees counterclockwise from the y-axis.</span></span>
-   <span data-ttu-id="29776-108">*incline*: o ângulo de inclinação do eixo y, que é medido em graus no sentido horário a partir do eixo x.</span><span class="sxs-lookup"><span data-stu-id="29776-108">*angleY*: The y-axis skew angle, which is measured in degrees clockwise from the x-axis.</span></span>
-   <span data-ttu-id="29776-109">*centerPoint*: o ponto sobre o qual a distorção é executada.</span><span class="sxs-lookup"><span data-stu-id="29776-109">*centerPoint*: The point about which the skew is performed.</span></span>

<span data-ttu-id="29776-110">Para prever o efeito de uma transformação de distorção, considere que *angleX* é o ângulo de distorção medido em graus no sentido anti-horário do eixo y.</span><span class="sxs-lookup"><span data-stu-id="29776-110">To predict the effect of a skew transformation, consider that *angleX* is the skew angle measured in degrees counterclockwise from the y-axis.</span></span> <span data-ttu-id="29776-111">Por exemplo, se *angleX* for definido como 30, o objeto distorcerá 30 graus no sentido anti-horário ao longo do eixo y sobre o *centerPoint*.</span><span class="sxs-lookup"><span data-stu-id="29776-111">For example, if *angleX* is set to 30, the object skews 30 degrees counterclockwise along the y-axis about the *centerPoint*.</span></span> <span data-ttu-id="29776-112">A ilustração a seguir mostra um quadrado inclinado horizontalmente em 30 graus sobre o canto superior esquerdo do quadrado.</span><span class="sxs-lookup"><span data-stu-id="29776-112">The following illustration shows a square skewed horizontally 30 degrees about the upper-left corner of the square.</span></span>

![ilustração de um quadrado inclinado em 30 graus no sentido anti-horário do eixo y](images/skewx.png)

<span data-ttu-id="29776-114">Da mesma *forma, a* inclinação é um ângulo de distorção medido em graus no sentido horário a partir do eixo x.</span><span class="sxs-lookup"><span data-stu-id="29776-114">Similarly, *angleY* is a skew angle measured in degrees clockwise from the x-axis.</span></span> <span data-ttu-id="29776-115">Por exemplo, se *incline* for definido como 30, o objeto distorcerá 30 graus no sentido horário ao longo do eixo x sobre o *centerPoint*.</span><span class="sxs-lookup"><span data-stu-id="29776-115">For example, if *angleY* is set to 30, the object skews 30 degrees clockwise along the x-axis about the *centerPoint*.</span></span> <span data-ttu-id="29776-116">A ilustração a seguir mostra um quadrado inclinado verticalmente em 30 graus sobre o canto superior esquerdo do quadrado.</span><span class="sxs-lookup"><span data-stu-id="29776-116">The following illustration shows a square skewed vertically 30 degrees about the upper-left corner of the square.</span></span>

![ilustração de um quadrado distorcido 30 graus no sentido horário a partir do eixo x](images/skewy.png)

<span data-ttu-id="29776-118">Se você definir *angleX* e *angulares* como 30 graus e o *centerPoint* para o canto superior esquerdo do quadrado, você verá o seguinte quadrado inclinado (sólido contorno).</span><span class="sxs-lookup"><span data-stu-id="29776-118">If you set both *angleX* and *angleY* to 30 degrees, and the *centerPoint* to the upper-left corner of the square, you will see the following skewed square (solid outlined).</span></span> <span data-ttu-id="29776-119">Observe que o quadrado inclinado é distorcido em 30 graus no sentido anti-horário do eixo y e 30 graus no sentido horário do eixo x.</span><span class="sxs-lookup"><span data-stu-id="29776-119">Notice that the skewed square is skewed 30 degrees counterclockwise from the y-axis and 30 degrees clockwise from the x-axis.</span></span>

![ilustração de um quadrado inclinado em 30 graus no sentido anti-horário do eixo y e 30 graus no sentido horário do eixo x](images/skewxy.png)

<span data-ttu-id="29776-121">O exemplo de código a seguir inclina o quadrado de 45 graus horizontalmente sobre o canto superior esquerdo do quadrado.</span><span class="sxs-lookup"><span data-stu-id="29776-121">The following code example skews the square 45 degrees horizontally about the upper-left corner of the square.</span></span>


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



<span data-ttu-id="29776-122">A ilustração a seguir mostra o efeito de aplicar a transformação de distorção ao quadrado, em que o quadrado original é um contorno pontilhado e o paralelogramo (objeto inclinado) é uma estrutura de tópicos sólida.</span><span class="sxs-lookup"><span data-stu-id="29776-122">The following illustration shows the effect of applying the skew transformation to the square, where the original square is a dotted outline and the skewed object (parallelogram) is a solid outline.</span></span> <span data-ttu-id="29776-123">Observe que o ângulo de inclinação é 45 graus no sentido anti-horário do eixo y.</span><span class="sxs-lookup"><span data-stu-id="29776-123">Notice that the skew angle is 45 degrees counterclockwise from the y-axis.</span></span>

![ilustração de um quadrado distorcido 45 graus no sentido anti-horário do eixo y](images/skew-ovw.png)

## <a name="related-topics"></a><span data-ttu-id="29776-125">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="29776-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="29776-126">Visão geral das transformações do Direct2D</span><span class="sxs-lookup"><span data-stu-id="29776-126">Direct2D Transforms Overview</span></span>](direct2d-transforms-overview.md)
</dt> <dt>

[<span data-ttu-id="29776-127">Referência de Direct2D</span><span class="sxs-lookup"><span data-stu-id="29776-127">Direct2D Reference</span></span>](reference.md)
</dt> </dl>

 

 