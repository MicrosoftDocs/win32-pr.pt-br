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
# <a name="how-to-scale-an-object"></a><span data-ttu-id="050a3-103">Como dimensionar um objeto</span><span class="sxs-lookup"><span data-stu-id="050a3-103">How to Scale an Object</span></span>

<span data-ttu-id="050a3-104">Este tópico descreve como dimensionar um objeto usando a classe [**Matrix3x2F**](/windows/win32/api/d2d1helper/nl-d2d1helper-matrix3x2f) .</span><span class="sxs-lookup"><span data-stu-id="050a3-104">This topic describes how to scale an object by using the [**Matrix3x2F**](/windows/win32/api/d2d1helper/nl-d2d1helper-matrix3x2f) class.</span></span> <span data-ttu-id="050a3-105">Dimensionar um objeto significa aumentar ou diminuir o objeto.</span><span class="sxs-lookup"><span data-stu-id="050a3-105">To scale an object means to make the object larger or smaller.</span></span> <span data-ttu-id="050a3-106">Você pode chamar um dos dois métodos a seguir para dimensionar um objeto.</span><span class="sxs-lookup"><span data-stu-id="050a3-106">You can call one of the following two methods to scale an object.</span></span>

-   <span data-ttu-id="050a3-107">**Matrix3x2F:: Scale (tamanho de D2D1 \_ \_ F SCALEFACTOR, d2d1 \_ Point \_ 2F CenterPoint)**</span><span class="sxs-lookup"><span data-stu-id="050a3-107">**Matrix3x2F::Scale(D2D1\_SIZE\_F scalefactor, D2D1\_POINT\_2F centerpoint)**</span></span>
-   <span data-ttu-id="050a3-108">**Matrix3x2F:: Scale (float ScaleX, float ScaleY, D2D1 \_ Point \_ 2F CenterPoint)**</span><span class="sxs-lookup"><span data-stu-id="050a3-108">**Matrix3x2F::Scale(float scalex, float scaley, D2D1\_POINT\_2F centerpoint)**</span></span>

<span data-ttu-id="050a3-109">O primeiro método armazena *ScaleX* e *ScaleY* como um par ordenado de valores de ponto flutuante na estrutura [**\_ \_ F de tamanho de d2d1**](/windows/desktop/Direct2D/d2d1-size-f) .</span><span class="sxs-lookup"><span data-stu-id="050a3-109">The first method stores *scalex* and *scaley* as an ordered pair of floating-point values in the [**D2D1\_SIZE\_F**](/windows/desktop/Direct2D/d2d1-size-f) structure.</span></span> <span data-ttu-id="050a3-110">O segundo método define *ScaleX* e *ScaleY* como parâmetros individuais.</span><span class="sxs-lookup"><span data-stu-id="050a3-110">The second method defines *scalex* and *scaley* as individual parameters.</span></span>

<span data-ttu-id="050a3-111">Independentemente do método usado, você deve especificar os fatores *ScaleX* e *ScaleY* .</span><span class="sxs-lookup"><span data-stu-id="050a3-111">Regardless of which method that you use, you must specify both *scalex* and *scaley* factors.</span></span> <span data-ttu-id="050a3-112">O valor de *ScaleX* é o fator de escala na direção x.</span><span class="sxs-lookup"><span data-stu-id="050a3-112">The *scalex* value is the scale factor in the x direction.</span></span> <span data-ttu-id="050a3-113">Por exemplo, um valor de *ScaleX* de 1,5 amplia o objeto para 150% ao longo do eixo x.</span><span class="sxs-lookup"><span data-stu-id="050a3-113">For example, a *scalex* value of 1.5 stretches the object to 150 percent along the x-axis.</span></span> <span data-ttu-id="050a3-114">Da mesma forma, o valor de *ScaleY* é o fator de escala na direção y.</span><span class="sxs-lookup"><span data-stu-id="050a3-114">Similarly, the *scaley* value is the scale factor in the y direction.</span></span> <span data-ttu-id="050a3-115">Por exemplo, um valor de *ScaleY* de 0,5 reduz a altura do objeto em 50% ao longo do eixo y.</span><span class="sxs-lookup"><span data-stu-id="050a3-115">For example, a *scaley* value of 0.5 shrinks the height of the object by 50 percent along the y-axis.</span></span>

<span data-ttu-id="050a3-116">Para especificar um ponto como o centro da operação de dimensionamento, use o parâmetro *CenterPoint* .</span><span class="sxs-lookup"><span data-stu-id="050a3-116">To specify a point as the center of the scaling operation, use the *centerpoint* parameter.</span></span> <span data-ttu-id="050a3-117">Por padrão, um objeto é centralizado sobre sua origem (0, 0).</span><span class="sxs-lookup"><span data-stu-id="050a3-117">By default, an object is centered about its origin (0,0).</span></span>

<span data-ttu-id="050a3-118">O código de exemplo a seguir cria uma transformação escala para aumentar o tamanho de um quadrado para 130% de seu tamanho original.</span><span class="sxs-lookup"><span data-stu-id="050a3-118">The following example code creates a scale transformation to increase the size of a square to 130% of its original size.</span></span> <span data-ttu-id="050a3-119">O *CenterPoint* é definido para ser o canto superior esquerdo do quadrado original.</span><span class="sxs-lookup"><span data-stu-id="050a3-119">The *centerpoint* is set to be the upper-left corner of the original square.</span></span>


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



<span data-ttu-id="050a3-120">A ilustração a seguir mostra o efeito de aplicar a transformação escala ao quadrado.</span><span class="sxs-lookup"><span data-stu-id="050a3-120">The following illustration shows the effect of applying the scale transformation to the square.</span></span> <span data-ttu-id="050a3-121">O quadrado original é um contorno pontilhado e o quadrado dimensionado é uma estrutura de tópicos sólida.</span><span class="sxs-lookup"><span data-stu-id="050a3-121">The original square is a dotted outline and the scaled square is a solid outline.</span></span>

![ilustração do quadrado redimensionado para 130% de seu tamanho original](images/scale-ovw.png)

## <a name="related-topics"></a><span data-ttu-id="050a3-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="050a3-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="050a3-124">Visão geral das transformações do Direct2D</span><span class="sxs-lookup"><span data-stu-id="050a3-124">Direct2D Transforms Overview</span></span>](direct2d-transforms-overview.md)
</dt> <dt>

[<span data-ttu-id="050a3-125">Referência de Direct2D</span><span class="sxs-lookup"><span data-stu-id="050a3-125">Direct2D Reference</span></span>](reference.md)
</dt> </dl>

 

 