---
title: Como girar um objeto
description: Mostra como girar um objeto.
ms.assetid: 468e29b6-941b-4cf8-8649-9e513326ccb2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b69cd900a78ba4d81919df91b85fd97723172eba
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103917501"
---
# <a name="how-to-rotate-an-object"></a><span data-ttu-id="052c4-103">Como girar um objeto</span><span class="sxs-lookup"><span data-stu-id="052c4-103">How to Rotate an Object</span></span>

<span data-ttu-id="052c4-104">Este tópico descreve como girar um objeto sobre um ponto especificado.</span><span class="sxs-lookup"><span data-stu-id="052c4-104">This topic describes how to rotate an object about a specified point.</span></span> <span data-ttu-id="052c4-105">Para girar um objeto, chame o método [**Matrix3x2F:: Rotation**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-rotation) .</span><span class="sxs-lookup"><span data-stu-id="052c4-105">To rotate an object, call [**Matrix3x2F::Rotation**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-rotation) method.</span></span> <span data-ttu-id="052c4-106">Esse método usa dois parâmetros, o ângulo especificado e o ponto central.</span><span class="sxs-lookup"><span data-stu-id="052c4-106">This method takes two parameters, the specified angle and the center point.</span></span> <span data-ttu-id="052c4-107">O ângulo é um ângulo de rotação no sentido horário em graus, e o ponto central é o ponto sobre o qual o objeto gira.</span><span class="sxs-lookup"><span data-stu-id="052c4-107">The angle is a clockwise rotation angle in degrees, and the center point is the point about which the object rotates.</span></span> <span data-ttu-id="052c4-108">O ponto central é expresso no sistema de coordenadas do objeto que é transformado.</span><span class="sxs-lookup"><span data-stu-id="052c4-108">The center point is expressed in the coordinate system of the object that is transformed.</span></span>

<span data-ttu-id="052c4-109">Por exemplo, o código a seguir gira um quadrado no sentido horário 45 graus sobre o centro do quadrado.</span><span class="sxs-lookup"><span data-stu-id="052c4-109">For example, the following code rotates a square clockwise 45 degrees about the center of the square.</span></span>


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



<span data-ttu-id="052c4-110">A ilustração a seguir mostra o efeito de aplicar a transformação de rotação anterior ao quadrado.</span><span class="sxs-lookup"><span data-stu-id="052c4-110">The following illustration shows the effect of applying the preceding rotation transformation to the square.</span></span> <span data-ttu-id="052c4-111">O quadrado original é um contorno pontilhado e o quadrado girado é uma estrutura de tópicos sólida.</span><span class="sxs-lookup"><span data-stu-id="052c4-111">The original square is a dotted outline, and the rotated square is a solid outline.</span></span>

![ilustração de um quadrado girado no sentido horário 45 graus sobre o centro do quadrado original](images/rotate-ovw.png)

<span data-ttu-id="052c4-113">A ilustração a seguir mostra o efeito de girar pelo mesmo ângulo sobre um ponto central diferente.</span><span class="sxs-lookup"><span data-stu-id="052c4-113">The following illustration shows the effect of rotating by the same angle about a different center point.</span></span> <span data-ttu-id="052c4-114">Observe que os objetos girados estão em posições diferentes em relação ao original.</span><span class="sxs-lookup"><span data-stu-id="052c4-114">Notice that the rotated objects are in different positions relative to the original.</span></span> <span data-ttu-id="052c4-115">O quadrado com contorno à esquerda é o resultado da rotação sobre o centro do quadrado original, e o quadrado descrito à direita é o resultado da rotação sobre o canto superior esquerdo do quadrado original.</span><span class="sxs-lookup"><span data-stu-id="052c4-115">The left outlined square is the result of rotating about the center of the original square, and the right outlined square is the result of rotating about the upper-left corner of the original square.</span></span>

![ilustração de um quadrado girado no sentido horário 45 graus sobre um ponto central diferente](images/translate-rotationcompare.png)

## <a name="related-topics"></a><span data-ttu-id="052c4-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="052c4-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="052c4-118">Referência de Direct2D</span><span class="sxs-lookup"><span data-stu-id="052c4-118">Direct2D Reference</span></span>](reference.md)
</dt> <dt>

[<span data-ttu-id="052c4-119">Visão geral das transformações do Direct2D</span><span class="sxs-lookup"><span data-stu-id="052c4-119">Direct2D Transforms Overview</span></span>](direct2d-transforms-overview.md)
</dt> </dl>

 

 