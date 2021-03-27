---
description: Um único objeto matriz pode armazenar uma única transformação ou uma sequência de transformações.
ms.assetid: 1dc68ff8-6b17-4934-82da-ab2fc612aafa
title: Por que a ordem das transformações é importante
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a7350d63456902ff47183faa08170b3b2fef481
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967394"
---
# <a name="why-transformation-order-is-significant"></a><span data-ttu-id="03db5-103">Por que a ordem das transformações é importante</span><span class="sxs-lookup"><span data-stu-id="03db5-103">Why Transformation Order Is Significant</span></span>

<span data-ttu-id="03db5-104">Um único objeto [**matriz**](/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) pode armazenar uma única transformação ou uma sequência de transformações.</span><span class="sxs-lookup"><span data-stu-id="03db5-104">A single [**Matrix**](/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) object can store a single transformation or a sequence of transformations.</span></span> <span data-ttu-id="03db5-105">O último é chamado de *transformação* composta.  </span><span class="sxs-lookup"><span data-stu-id="03db5-105">The latter is called a *composite*  *transformation*.</span></span> <span data-ttu-id="03db5-106">A matriz de uma transformação composta é obtida multiplicando-se as matrizes das transformações individuais.</span><span class="sxs-lookup"><span data-stu-id="03db5-106">The matrix of a composite transformation is obtained by multiplying the matrices of the individual transformations.</span></span>

<span data-ttu-id="03db5-107">Em uma transformação composta, a ordem das transformações individuais é importante.</span><span class="sxs-lookup"><span data-stu-id="03db5-107">In a composite transformation, the order of the individual transformations is important.</span></span> <span data-ttu-id="03db5-108">Por exemplo, girar, ajustar a escala e mover terá um resultado diferente de mover, girar e ajustar a escala.</span><span class="sxs-lookup"><span data-stu-id="03db5-108">For example, if you first rotate, then scale, then translate, you get a different result than if you first translate, then rotate, then scale.</span></span> <span data-ttu-id="03db5-109">No Windows GDI+, as transformações de composição são criadas da esquerda para a direita.</span><span class="sxs-lookup"><span data-stu-id="03db5-109">In Windows GDI+, composite transformations are built from left to right.</span></span> <span data-ttu-id="03db5-110">Se S, R e T forem matrizes de escala, rotação e translação, respectivamente, o produto SRT (nesta ordem) será a matriz da transformação composta que primeiro ajusta a escala, em seguida girará e finalmente fará a translação.</span><span class="sxs-lookup"><span data-stu-id="03db5-110">If S, R, and T are scale, rotation, and translation matrices respectively, then the product SRT (in that order) is the matrix of the composite transformation that first scales, then rotates, then translates.</span></span> <span data-ttu-id="03db5-111">A matriz produzida pelo produto SRT será diferente da matriz produzida pelo produto TRS.</span><span class="sxs-lookup"><span data-stu-id="03db5-111">The matrix produced by the product SRT is different from the matrix produced by the product TRS.</span></span>

<span data-ttu-id="03db5-112">Um motivo de a ordem ser importante é que transformações, como rotação e colocação em escala, são feitas em relação a origem do sistema de coordenadas.</span><span class="sxs-lookup"><span data-stu-id="03db5-112">One reason order is significant is that transformations like rotation and scaling are done with respect to the origin of the coordinate system.</span></span> <span data-ttu-id="03db5-113">O dimensionamento de um objeto que é centralizado na origem produz um resultado diferente do dimensionamento de um objeto que foi movido para fora da origem.</span><span class="sxs-lookup"><span data-stu-id="03db5-113">Scaling an object that is centered at the origin produces a different result than scaling an object that has been moved away from the origin.</span></span> <span data-ttu-id="03db5-114">Da mesma forma, girar um objeto centralizado na origem produz um resultado diferente de girar um objeto movido para fora da origem.</span><span class="sxs-lookup"><span data-stu-id="03db5-114">Similarly, rotating an object that is centered at the origin produces a different result than rotating an object that has been moved away from the origin.</span></span>

<span data-ttu-id="03db5-115">O exemplo a seguir combina colocação em escala, rotação e translação (nessa ordem) para formar uma transformação composta.</span><span class="sxs-lookup"><span data-stu-id="03db5-115">The following example combines scaling, rotation and translation (in that order) to form a composite transformation.</span></span> <span data-ttu-id="03db5-116">O argumento [\* \* \* \* MatrixOrderAppend \* \*](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-matrixorder) \* \* passado para o método [**Graphics:: RotateTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-rotatetransform) especifica que a rotação seguirá o dimensionamento.</span><span class="sxs-lookup"><span data-stu-id="03db5-116">The argument [\*\*\*\*MatrixOrderAppend\*\*\*\*](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-matrixorder) passed to the [**Graphics::RotateTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-rotatetransform) method specifies that the rotation will follow the scaling.</span></span> <span data-ttu-id="03db5-117">Da mesma forma, o argumento [\* \* \* \* MatrixOrderAppend \* \* \* \*](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-matrixorder) passado para o método [**Graphics:: TranslateTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-translatetransform) especifica que a conversão irá seguir a rotação.</span><span class="sxs-lookup"><span data-stu-id="03db5-117">Likewise, the argument [\*\*\*\*MatrixOrderAppend\*\*\*\*](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-matrixorder) passed to the [**Graphics::TranslateTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-translatetransform) method specifies that the translation will follow the rotation.</span></span>


```
Rect rect(0, 0, 50, 50);
Pen pen(Color(255, 255, 0, 0), 0);
graphics.ScaleTransform(1.75f, 0.5f);
graphics.RotateTransform(28.0f, MatrixOrderAppend);
graphics.TranslateTransform(150.0f, 150.0f, MatrixOrderAppend);
graphics.DrawRectangle(&pen, rect);
```



<span data-ttu-id="03db5-118">O exemplo a seguir faz as mesmas chamadas de método que o exemplo anterior, mas a ordem das chamadas é revertida.</span><span class="sxs-lookup"><span data-stu-id="03db5-118">The following example makes the same method calls as the previous example, but the order of the calls is reversed.</span></span> <span data-ttu-id="03db5-119">A ordem resultante das operações é primeiro traduzir, depois girar e dimensionar, o que produz um resultado muito diferente do que a primeira escala, em seguida, girar e depois converter:</span><span class="sxs-lookup"><span data-stu-id="03db5-119">The resulting order of operations is first translate, then rotate, then scale, which produces a very different result than first scale, then rotate, then translate:</span></span>


```
Rect rect(0, 0, 50, 50);
Pen pen(Color(255, 255, 0, 0), 0);
graphics.TranslateTransform(150.0f, 150.0f);
graphics.RotateTransform(28.0f, MatrixOrderAppend);
graphics.ScaleTransform(1.75f, 0.5f, MatrixOrderAppend);
graphics.DrawRectangle(&pen, rect);
```



<span data-ttu-id="03db5-120">Uma maneira de inverter a ordem das transformações individuais em uma transformação composta é inverter a ordem de uma sequência de chamadas de método.</span><span class="sxs-lookup"><span data-stu-id="03db5-120">One way to reverse the order of the individual transformations in a composite transformation is to reverse the order of a sequence of method calls.</span></span> <span data-ttu-id="03db5-121">Outra maneira de controlar a ordem das operações é alterar o argumento de ordem de matriz.</span><span class="sxs-lookup"><span data-stu-id="03db5-121">A second way to control the order of operations is to change the matrix order argument.</span></span> <span data-ttu-id="03db5-122">O exemplo a seguir é o mesmo que o exemplo anterior, exceto que [\* \* \* \* MatrixOrderAppend \* \*](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-matrixorder) \* \* foi alterado para [\* \* \* \* MatrixOrderPrepend \* \*](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-matrixorder)\* \*.</span><span class="sxs-lookup"><span data-stu-id="03db5-122">The following example is the same as the previous example, except that [\*\*\*\*MatrixOrderAppend\*\*\*\*](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-matrixorder) has been changed to [\*\*\*\*MatrixOrderPrepend\*\*\*\*](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-matrixorder).</span></span> <span data-ttu-id="03db5-123">A multiplicação de matriz é feita na ordem SRT, em que S, R e T são matrizes para ajustar escala, girar e mover, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="03db5-123">The matrix multiplication is done in the order SRT, where S, R, and T are the matrices for scale, rotate, and translate, respectively.</span></span> <span data-ttu-id="03db5-124">A ordem da transformação composta é ajustar escala, girar e mover.</span><span class="sxs-lookup"><span data-stu-id="03db5-124">The order of the composite transformation is first scale, then rotate, then translate.</span></span>


```
Rect rect(0, 0, 50, 50);
Pen pen(Color(255, 255, 0, 0), 0);
graphics.TranslateTransform(150.0f, 150.0f,MatrixOrderPrepend);
graphics.RotateTransform(28.0f, MatrixOrderPrepend);
graphics.ScaleTransform(1.75f, 0.5f, MatrixOrderPrepend);
graphics.DrawRectangle(&pen, rect);
```



<span data-ttu-id="03db5-125">O resultado do exemplo anterior é o mesmo resultado que obtivemos no primeiro exemplo desta seção.</span><span class="sxs-lookup"><span data-stu-id="03db5-125">The result of the preceding example is the same result that we achieved in the first example of this section.</span></span> <span data-ttu-id="03db5-126">Isso ocorre porque invertemos a ordem das chamadas de método e a ordem de multiplicação da matriz.</span><span class="sxs-lookup"><span data-stu-id="03db5-126">This is because we reversed both the order of the method calls and the order of the matrix multiplication.</span></span>

 

 



