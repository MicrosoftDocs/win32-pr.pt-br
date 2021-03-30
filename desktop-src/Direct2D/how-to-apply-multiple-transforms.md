---
title: Como aplicar várias transformações a um objeto
description: Mostra como aplicar várias transformações a um objeto.
ms.assetid: a3875072-bb73-4698-944e-102ab5539d80
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e031a46545c59513767ed4d260be9dc677b3fb77
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635189"
---
# <a name="how-to-apply-multiple-transforms-to-an-object"></a><span data-ttu-id="1bf42-103">Como aplicar várias transformações a um objeto</span><span class="sxs-lookup"><span data-stu-id="1bf42-103">How to Apply Multiple Transforms to an Object</span></span>

<span data-ttu-id="1bf42-104">Executar várias transformações em um objeto significa combinar várias transformações em uma.</span><span class="sxs-lookup"><span data-stu-id="1bf42-104">To perform multiple transforms on an object means to combine several transforms into one.</span></span> <span data-ttu-id="1bf42-105">Ou seja, pegar a saída de cada matriz de transformação e usá-la como entrada para a próxima, obtendo, assim, os efeitos cumulativos de todas as transformações de matriz.</span><span class="sxs-lookup"><span data-stu-id="1bf42-105">That is, taking the output from each transformation matrix and using it as the input for the next, thereby getting the cumulative effects of all the matrix transformations.</span></span>

<span data-ttu-id="1bf42-106">Suponha que duas matrizes de transformação, rotação e translação sejam multiplicadas juntas.</span><span class="sxs-lookup"><span data-stu-id="1bf42-106">Suppose two transformation matrices, rotation and translation, are multiplied together.</span></span> <span data-ttu-id="1bf42-107">O resultado é uma nova matriz que executa as funções de rotação e translação.</span><span class="sxs-lookup"><span data-stu-id="1bf42-107">The result is a new matrix that performs the functions of both rotation and translation.</span></span> <span data-ttu-id="1bf42-108">Como a multiplicação de matriz não é comutada, uma transformação de rotação multiplicada por uma transformação de tradução é diferente da transformação de tradução multiplicada pela transformação de rotação.</span><span class="sxs-lookup"><span data-stu-id="1bf42-108">Because matrix multiplication is not commutative, a rotation transformation multiplied by a translation transformation is different from the translation transformation multiplied by the rotation transformation.</span></span>

<span data-ttu-id="1bf42-109">Os exemplos de código a seguir mostram como aplicar a rotação seguida pela tradução e, em seguida, a tradução seguida por rotação.</span><span class="sxs-lookup"><span data-stu-id="1bf42-109">The following code examples show how to apply rotation followed by translation, and then translation followed by rotation.</span></span> <span data-ttu-id="1bf42-110">Observe que os resultados da renderização são diferentes.</span><span class="sxs-lookup"><span data-stu-id="1bf42-110">Notice that the rendering results are different.</span></span>


```C++
D2D1_RECT_F rectangle = D2D1::RectF(300.0f, 40.0f, 360.0f, 100.0f);

// Draw the rectangle before transforming the render target.

m_pRenderTarget->DrawRectangle(
    rectangle,
    m_pOriginalShapeBrush,
    1.0f,
    m_pStrokeStyleDash
    );

D2D1_MATRIX_3X2_F rotation = D2D1::Matrix3x2F::Rotation(
    45.0f,
    D2D1::Point2F(330.0f, 70.0f)
    );


D2D1_MATRIX_3X2_F translation = D2D1::Matrix3x2F::Translation(20.0f, 10.0f);

// First rotate about the center of the square and then move
// 20 pixels to the right along the x-axis
// and 10 pixels downward along the y-axis.
m_pRenderTarget->SetTransform(rotation* translation);

// Draw the rectangle in the transformed space.
m_pRenderTarget->FillRectangle(rectangle, m_pFillBrush);
m_pRenderTarget->DrawRectangle(rectangle, m_pTransformedShapeBrush, 1.0f);
```




```C++
D2D1_RECT_F rectangle = D2D1::Rect(40.0f, 40.0f, 100.0f, 100.0f);

// Draw a rectangle without transforming it.
m_pRenderTarget->DrawRectangle(
    rectangle,
    m_pOriginalShapeBrush,
    1.0f,
    m_pStrokeStyleDash
    );

D2D1_MATRIX_3X2_F translation = D2D1::Matrix3x2F::Translation(20.0f, 10.0f);

m_pRenderTarget->SetTransform(translation);

D2D1_MATRIX_3X2_F rotation = D2D1::Matrix3x2F::Rotation(
    45.0f,
    D2D1::Point2F(70.0f, 70.0f)
    );

// First move 20 pixels to the right along the x-axis and
// 10 pixels downward along the y-axis,
// and then rotate about the center of the original square.
m_pRenderTarget->SetTransform(translation * rotation);

// Draw the rectangle in the transformed space.
m_pRenderTarget->FillRectangle(rectangle, m_pFillBrush);
m_pRenderTarget->DrawRectangle(rectangle, m_pTransformedShapeBrush);
```



<span data-ttu-id="1bf42-111">O código produz a saída mostrada na ilustração a seguir.</span><span class="sxs-lookup"><span data-stu-id="1bf42-111">The code produces the output shown in the following illustration.</span></span>

![ilustração de um retângulo que foi traduzido e girado e um retângulo que foi girado e, em seguida, traduzido](images/multipletransforms.png)

## <a name="related-topics"></a><span data-ttu-id="1bf42-113">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1bf42-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1bf42-114">Referência de Direct2D</span><span class="sxs-lookup"><span data-stu-id="1bf42-114">Direct2D Reference</span></span>](reference.md)
</dt> <dt>

[<span data-ttu-id="1bf42-115">Visão geral das transformações do Direct2D</span><span class="sxs-lookup"><span data-stu-id="1bf42-115">Direct2D Transforms Overview</span></span>](direct2d-transforms-overview.md)
</dt> </dl>

 

 




