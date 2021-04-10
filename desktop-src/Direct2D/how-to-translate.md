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
# <a name="how-to-translate-an-object"></a><span data-ttu-id="2cd25-103">Como converter um objeto</span><span class="sxs-lookup"><span data-stu-id="2cd25-103">How to Translate an Object</span></span>

<span data-ttu-id="2cd25-104">Converter um objeto 2D é mover o objeto ao longo do eixo x, do eixo y ou de ambos.</span><span class="sxs-lookup"><span data-stu-id="2cd25-104">To translate a 2-D object is to move the object along the x-axis, the y-axis, or both.</span></span> <span data-ttu-id="2cd25-105">Você pode chamar qualquer um dos dois métodos a seguir para criar uma transformação de tradução.</span><span class="sxs-lookup"><span data-stu-id="2cd25-105">You can call either one of the following two methods to create a translation transformation.</span></span>

-   <span data-ttu-id="2cd25-106">[**Translation (tamanho do d2d1 \_ tamanho \_ F)**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-translation(d2d1_size_f)): usa um par ordenado que define a distância a ser transvertida ao longo do eixo x e do eixo y.</span><span class="sxs-lookup"><span data-stu-id="2cd25-106">[**Translation(D2D1\_SIZE\_F size)**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-translation(d2d1_size_f)): takes an ordered pair that defines the distance to translate along the x-axis and the y-axis.</span></span>
-   <span data-ttu-id="2cd25-107">[**Translação (float x, float y)**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-translation(float_float)): usa a distância para converter ao longo do eixo x e a distância a ser transvertida ao longo do eixo y.</span><span class="sxs-lookup"><span data-stu-id="2cd25-107">[**Translation(float x, float y)**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-translation(float_float)): takes the distance to translate along the x-axis and the distance to translate along the y-axis.</span></span>

<span data-ttu-id="2cd25-108">O código a seguir cria uma matriz de transformação de tradução que move as 20 unidades quadradas para a direita ao longo do eixo x e 10 unidades para baixo ao longo do eixo y.</span><span class="sxs-lookup"><span data-stu-id="2cd25-108">The following code creates a translation transformation matrix that moves the square 20 units to the right along the x-axis and 10 units downward along the y-axis.</span></span>


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



<span data-ttu-id="2cd25-109">A ilustração a seguir mostra o efeito de aplicar a transformação translação ao quadrado, em que o quadrado original é um contorno pontilhado e o quadrado traduzido é uma estrutura de tópicos sólida.</span><span class="sxs-lookup"><span data-stu-id="2cd25-109">The following illustration shows the effect of applying the translation transformation to the square, where the original square is a dotted outline and the translated square is a solid outline.</span></span>

![ilustração de um quadrado moveu 20 unidades para a direita ao longo do eixo x e 10 unidades para baixo ao longo do eixo y](images/translation-ovw.png)

## <a name="related-topics"></a><span data-ttu-id="2cd25-111">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2cd25-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2cd25-112">Referência de Direct2D</span><span class="sxs-lookup"><span data-stu-id="2cd25-112">Direct2D Reference</span></span>](reference.md)
</dt> <dt>

[<span data-ttu-id="2cd25-113">Visão geral das transformações do Direct2D</span><span class="sxs-lookup"><span data-stu-id="2cd25-113">Direct2D Transforms Overview</span></span>](direct2d-transforms-overview.md)
</dt> </dl>

 

 