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
# <a name="applying-transforms-in-direct2d"></a><span data-ttu-id="e7217-103">Aplicar transformações em Direct2D</span><span class="sxs-lookup"><span data-stu-id="e7217-103">Applying Transforms in Direct2D</span></span>

<span data-ttu-id="e7217-104">No [desenho com Direct2D](drawing-with-direct2d.md), vimos que o método [**ID2D1RenderTarget:: FillEllipse**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse__id2d1brush)) desenha uma elipse que está alinhada aos eixos x e y.</span><span class="sxs-lookup"><span data-stu-id="e7217-104">In [Drawing with Direct2D](drawing-with-direct2d.md), we saw that the [**ID2D1RenderTarget::FillEllipse**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse__id2d1brush)) method draws an ellipse that is aligned to the x- and y-axes.</span></span> <span data-ttu-id="e7217-105">Mas suponha que você queira desenhar uma elipse inclinada em um ângulo?</span><span class="sxs-lookup"><span data-stu-id="e7217-105">But suppose that you want to draw an ellipse tilted at an angle?</span></span>

![uma imagem que mostra uma elipse inclinada.](images/graphics16.png)

<span data-ttu-id="e7217-107">Usando transformações, você pode alterar uma forma das seguintes maneiras.</span><span class="sxs-lookup"><span data-stu-id="e7217-107">By using transforms, you can alter a shape in the following ways.</span></span>

-   <span data-ttu-id="e7217-108">Rotação em um ponto.</span><span class="sxs-lookup"><span data-stu-id="e7217-108">Rotation around a point.</span></span>
-   <span data-ttu-id="e7217-109">Dimensionamento.</span><span class="sxs-lookup"><span data-stu-id="e7217-109">Scaling.</span></span>
-   <span data-ttu-id="e7217-110">Translação (deslocamento na direção X ou Y).</span><span class="sxs-lookup"><span data-stu-id="e7217-110">Translation (displacement in the X or Y direction).</span></span>
-   <span data-ttu-id="e7217-111">Distorção (também conhecida como *distorção*).</span><span class="sxs-lookup"><span data-stu-id="e7217-111">Skew (also known as *shear*).</span></span>

<span data-ttu-id="e7217-112">Uma transformação é uma operação matemática que mapeia um conjunto de pontos para um novo conjunto de pontos.</span><span class="sxs-lookup"><span data-stu-id="e7217-112">A transform is a mathematical operation that maps a set of points to a new set of points.</span></span> <span data-ttu-id="e7217-113">Por exemplo, o diagrama a seguir mostra um triângulo girado em volta do ponto P3.</span><span class="sxs-lookup"><span data-stu-id="e7217-113">For example, the following diagram shows a triangle rotated around the point P3.</span></span> <span data-ttu-id="e7217-114">Depois que a rotação for aplicada, o ponto P1 será mapeado para P1 ', o ponto P2 será mapeado para P2 ' e o ponto P3 se mapeará para si mesmo.</span><span class="sxs-lookup"><span data-stu-id="e7217-114">After the rotation is applied, the point P1 is mapped to P1', the point P2 is mapped to P2', and the point P3 maps to itself.</span></span>

![um diagrama que mostra a rotação em um ponto.](images/graphics17.png)

<span data-ttu-id="e7217-116">As transformações são implementadas usando matrizes.</span><span class="sxs-lookup"><span data-stu-id="e7217-116">Transforms are implemented by using matrices.</span></span> <span data-ttu-id="e7217-117">No entanto, você não precisa entender a matemática de matrizes para usá-las.</span><span class="sxs-lookup"><span data-stu-id="e7217-117">However, you do not have to understand the mathematics of matrices in order to use them.</span></span> <span data-ttu-id="e7217-118">Se você quiser saber mais sobre a matemática, consulte [Apêndice: transformações de matriz](appendix--matrix-transforms.md).</span><span class="sxs-lookup"><span data-stu-id="e7217-118">If you want to learn more about the math, see [Appendix: Matrix Transforms](appendix--matrix-transforms.md).</span></span>

<span data-ttu-id="e7217-119">Para aplicar uma transformação em Direct2D, chame o método [**ID2D1RenderTarget:: SetTransform**](/windows/desktop/Direct2D/id2d1rendertarget-settransform) .</span><span class="sxs-lookup"><span data-stu-id="e7217-119">To apply a transform in Direct2D, call the [**ID2D1RenderTarget::SetTransform**](/windows/desktop/Direct2D/id2d1rendertarget-settransform) method.</span></span> <span data-ttu-id="e7217-120">Esse método usa uma estrutura [**d2d1 \_ matriz \_ 3x2 \_ F**](/windows/desktop/Direct2D/d2d1-matrix-3x2-f) que define a transformação.</span><span class="sxs-lookup"><span data-stu-id="e7217-120">This method takes a [**D2D1\_MATRIX\_3X2\_F**](/windows/desktop/Direct2D/d2d1-matrix-3x2-f) structure that defines the transformation.</span></span> <span data-ttu-id="e7217-121">Você pode inicializar essa estrutura chamando métodos na classe [**d2d1:: Matrix3x2F**](/windows/desktop/api/d2d1helper/nl-d2d1helper-matrix3x2f) .</span><span class="sxs-lookup"><span data-stu-id="e7217-121">You can initialize this structure by calling methods on the [**D2D1::Matrix3x2F**](/windows/desktop/api/d2d1helper/nl-d2d1helper-matrix3x2f) class.</span></span> <span data-ttu-id="e7217-122">Essa classe contém métodos estáticos que retornam uma matriz para cada tipo de transformação:</span><span class="sxs-lookup"><span data-stu-id="e7217-122">This class contains static methods that return a matrix for each kind of transform:</span></span>

-   [<span data-ttu-id="e7217-123">**Matrix3x2F:: Rotation**</span><span class="sxs-lookup"><span data-stu-id="e7217-123">**Matrix3x2F::Rotation**</span></span>](/windows/desktop/api/d2d1helper/nf-d2d1helper-matrix3x2f-rotation)
-   <span data-ttu-id="e7217-124">[**Matrix3x2F:: Scale**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-scale(d2d1_size_f_d2d1_point_2f))</span><span class="sxs-lookup"><span data-stu-id="e7217-124">[**Matrix3x2F::Scale**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-scale(d2d1_size_f_d2d1_point_2f))</span></span>
-   <span data-ttu-id="e7217-125">[**Matrix3x2F:: translation**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-translation(d2d1_size_f))</span><span class="sxs-lookup"><span data-stu-id="e7217-125">[**Matrix3x2F::Translation**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-translation(d2d1_size_f))</span></span>
-   [<span data-ttu-id="e7217-126">**Matrix3x2F:: skew**</span><span class="sxs-lookup"><span data-stu-id="e7217-126">**Matrix3x2F::Skew**</span></span>](/windows/desktop/api/d2d1helper/nf-d2d1helper-matrix3x2f-skew)

<span data-ttu-id="e7217-127">Por exemplo, o código a seguir aplica uma rotação de 20 graus ao seu ponto (100, 100).</span><span class="sxs-lookup"><span data-stu-id="e7217-127">For example, the following code applies a 20-degree rotation around the point (100, 100).</span></span>


```C++
pRenderTarget->SetTransform(
    D2D1::Matrix3x2F::Rotation(20, D2D1::Point2F(100,100)));
```

<span data-ttu-id="e7217-128">A transformação será aplicada a todas as operações de desenho posteriores até que você chame [**SetTransform**](/windows/desktop/Direct2D/id2d1rendertarget-settransform) novamente.</span><span class="sxs-lookup"><span data-stu-id="e7217-128">The transform is applied to all later drawing operations until you call [**SetTransform**](/windows/desktop/Direct2D/id2d1rendertarget-settransform) again.</span></span> <span data-ttu-id="e7217-129">Para remover a transformação atual, chame **SetTransform** com a matriz de identidade.</span><span class="sxs-lookup"><span data-stu-id="e7217-129">To remove the current transform, call **SetTransform** with the identity matrix.</span></span> <span data-ttu-id="e7217-130">Para criar a matriz de identidade, chame a função [**Matrix3x2F:: Identity**](/windows/desktop/api/d2d1helper/nf-d2d1helper-identitymatrix) .</span><span class="sxs-lookup"><span data-stu-id="e7217-130">To create the identity matrix, call the [**Matrix3x2F::Identity**](/windows/desktop/api/d2d1helper/nf-d2d1helper-identitymatrix) function.</span></span>


```C++
pRenderTarget->SetTransform(D2D1::Matrix3x2F::Identity());
```

## <a name="drawing-clock-hands"></a><span data-ttu-id="e7217-131">Mãos do relógio de desenho</span><span class="sxs-lookup"><span data-stu-id="e7217-131">Drawing Clock Hands</span></span>

<span data-ttu-id="e7217-132">Vamos colocar transformações para usar convertendo nosso programa em círculo em um relógio analógico.</span><span class="sxs-lookup"><span data-stu-id="e7217-132">Let's put transforms to use by converting our Circle program into an analog clock.</span></span> <span data-ttu-id="e7217-133">Podemos fazer isso adicionando linhas para as mãos.</span><span class="sxs-lookup"><span data-stu-id="e7217-133">We can do this by adding lines for the hands.</span></span>

![uma captura de tela do programa de relógio analógico.](images/graphics18.png)

<span data-ttu-id="e7217-135">Em vez de calcular as coordenadas das linhas, podemos calcular o ângulo e, em seguida, aplicar uma transformação de rotação.</span><span class="sxs-lookup"><span data-stu-id="e7217-135">Instead of calculating the coordinates for the lines, we can calculate the angle and then apply a rotation transform.</span></span> <span data-ttu-id="e7217-136">O código a seguir mostra uma função que desenha uma mão do relógio.</span><span class="sxs-lookup"><span data-stu-id="e7217-136">The following code shows a function that draws one clock hand.</span></span> <span data-ttu-id="e7217-137">O parâmetro *fAngle* fornece o ângulo da mão, em graus.</span><span class="sxs-lookup"><span data-stu-id="e7217-137">The *fAngle* parameter gives the angle of the hand, in degrees.</span></span>

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

<span data-ttu-id="e7217-138">Esse código desenha uma linha vertical, começando do centro da face do relógio e terminando no ponto de *extremidade*.</span><span class="sxs-lookup"><span data-stu-id="e7217-138">This code draws a vertical line, starting from the center of the clock face and ending at the point *endPoint*.</span></span> <span data-ttu-id="e7217-139">A linha é girada ao lado do centro da elipse aplicando uma transformação de rotação.</span><span class="sxs-lookup"><span data-stu-id="e7217-139">The line is rotated around the center of the ellipse by applying a rotation transform.</span></span> <span data-ttu-id="e7217-140">O ponto central da rotação é o centro da elipse que forma o relógio.</span><span class="sxs-lookup"><span data-stu-id="e7217-140">The center point for the rotation is the center of ellipse that forms the clock face.</span></span>

![um diagrama que mostra a rotação da mão do relógio.](images/graphics19.png)

<span data-ttu-id="e7217-142">O código a seguir mostra como toda a face do relógio é desenhada.</span><span class="sxs-lookup"><span data-stu-id="e7217-142">The following code shows how the whole clock face is drawn.</span></span>

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

<span data-ttu-id="e7217-143">Você pode baixar o projeto completo do Visual Studio do [exemplo de relógio Direct2D](direct2d-clock-sample.md).</span><span class="sxs-lookup"><span data-stu-id="e7217-143">You can download the complete Visual Studio project from [Direct2D Clock Sample](direct2d-clock-sample.md).</span></span> <span data-ttu-id="e7217-144">(Apenas para diversão, a versão de download adiciona um gradiant radial à face do relógio.)</span><span class="sxs-lookup"><span data-stu-id="e7217-144">(Just for fun, the download version adds a radial gradiant to the clock face.)</span></span>

## <a name="combining-transforms"></a><span data-ttu-id="e7217-145">Combinando transformações</span><span class="sxs-lookup"><span data-stu-id="e7217-145">Combining Transforms</span></span>

<span data-ttu-id="e7217-146">As quatro transformações básicas podem ser combinadas multiplicando duas ou mais matrizes.</span><span class="sxs-lookup"><span data-stu-id="e7217-146">The four basic transforms can be combined by multiplying two or more matrices.</span></span> <span data-ttu-id="e7217-147">Por exemplo, o código a seguir combina uma rotação com uma tradução.</span><span class="sxs-lookup"><span data-stu-id="e7217-147">For example, the following code combines a rotation with a translation.</span></span>

```C++
const D2D1::Matrix3x2F rot = D2D1::Matrix3x2F::Rotation(20);
const D2D1::Matrix3x2F trans = D2D1::Matrix3x2F::Translation(40, 10);

pRenderTarget->SetTransform(rot * trans);
```

<span data-ttu-id="e7217-148">A classe [**Matrix3x2F**](/windows/desktop/api/d2d1helper/nl-d2d1helper-matrix3x2f) fornece o [**operador \* ()**](/windows/desktop/api/d2d1helper/nf-d2d1helper-matrix3x2f-operator-mult) para multiplicação de matriz.</span><span class="sxs-lookup"><span data-stu-id="e7217-148">The [**Matrix3x2F**](/windows/desktop/api/d2d1helper/nl-d2d1helper-matrix3x2f) class provides [**operator\*()**](/windows/desktop/api/d2d1helper/nf-d2d1helper-matrix3x2f-operator-mult) for matrix multiplication.</span></span> <span data-ttu-id="e7217-149">A ordem na qual você multiplica as matrizes é importante.</span><span class="sxs-lookup"><span data-stu-id="e7217-149">The order in which you multiply the matrices is important.</span></span> <span data-ttu-id="e7217-150">Definir uma transformação (M × N) significa "aplicar M primeiro, seguido por N".</span><span class="sxs-lookup"><span data-stu-id="e7217-150">Setting a transform (M × N) means "Apply M first, followed by N."</span></span> <span data-ttu-id="e7217-151">Por exemplo, aqui está a rotação seguida da Tradução:</span><span class="sxs-lookup"><span data-stu-id="e7217-151">For example, here is rotation followed by translation:</span></span>

![um diagrama que mostra a rotação seguida pela tradução.](images/graphics20.png)

<span data-ttu-id="e7217-153">Este é o código para esta transformação:</span><span class="sxs-lookup"><span data-stu-id="e7217-153">Here is the code for this transform:</span></span>

```C++
const D2D1::Matrix3x2F rot = D2D1::Matrix3x2F::Rotation(45, center);
const D2D1::Matrix3x2F trans = D2D1::Matrix3x2F::Translation(x, 0);
pRenderTarget->SetTransform(rot * trans);
```

<span data-ttu-id="e7217-154">Agora, compare essa transformação com uma transformação na ordem inversa, a tradução seguida por rotação.</span><span class="sxs-lookup"><span data-stu-id="e7217-154">Now compare that transform with a transform in the reverse order, translation followed by rotation.</span></span>

![um diagrama que mostra a tradução seguida por rotação.](images/graphics21.png)

<span data-ttu-id="e7217-156">A rotação é realizada em todo o centro do retângulo original.</span><span class="sxs-lookup"><span data-stu-id="e7217-156">The rotation is performed around the center of the original rectangle.</span></span> <span data-ttu-id="e7217-157">Este é o código para essa transformação.</span><span class="sxs-lookup"><span data-stu-id="e7217-157">Here is the code for this transform.</span></span>

```C++
D2D1::Matrix3x2F rot = D2D1::Matrix3x2F::Rotation(45, center);
D2D1::Matrix3x2F trans = D2D1::Matrix3x2F::Translation(x, 0);
pRenderTarget->SetTransform(trans * rot);
```

<span data-ttu-id="e7217-158">Como você pode ver, as matrizes são as mesmas, mas a ordem das operações foi alterada.</span><span class="sxs-lookup"><span data-stu-id="e7217-158">As you can see, the matrices are the same, but the order of operations has changed.</span></span> <span data-ttu-id="e7217-159">Isso acontece porque a multiplicação de matriz não é comutada: M × N ≠ N × M.</span><span class="sxs-lookup"><span data-stu-id="e7217-159">This happens because matrix multiplication is not commutative: M × N ≠ N × M.</span></span>

## <a name="next"></a><span data-ttu-id="e7217-160">Avançar</span><span class="sxs-lookup"><span data-stu-id="e7217-160">Next</span></span>

[<span data-ttu-id="e7217-161">Apêndice: transformações de matriz</span><span class="sxs-lookup"><span data-stu-id="e7217-161">Appendix: Matrix Transforms</span></span>](appendix--matrix-transforms.md)