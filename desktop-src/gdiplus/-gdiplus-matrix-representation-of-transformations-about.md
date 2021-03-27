---
description: Uma matriz m&\# 215; n é um conjunto de números organizados em m linhas e n colunas. A ilustração a seguir mostra diversas matrizes.
ms.assetid: 62215ae0-b095-42b2-911c-aa7607a8b61a
title: Representação matricial de transformações
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0577cae38c401e842cff2ff14179594f9118dfd2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647108"
---
# <a name="matrix-representation-of-transformations"></a><span data-ttu-id="b4bb4-104">Representação matricial de transformações</span><span class="sxs-lookup"><span data-stu-id="b4bb4-104">Matrix Representation of Transformations</span></span>

<span data-ttu-id="b4bb4-105">Uma matriz *m × n* é um conjunto de números organizados em *m* linhas e *n* colunas.</span><span class="sxs-lookup"><span data-stu-id="b4bb4-105">An *m×n* matrix is a set of numbers arranged in *m* rows and *n* columns.</span></span> <span data-ttu-id="b4bb4-106">A ilustração a seguir mostra diversas matrizes.</span><span class="sxs-lookup"><span data-stu-id="b4bb4-106">The following illustration shows several matrices.</span></span>

![ilustração mostrando seis matrizes de dimensões variadas](images/aboutgdip05-art04.png)

<span data-ttu-id="b4bb4-108">Você pode adicionar duas matrizes do mesmo tamanho ao adicionar elementos individuais.</span><span class="sxs-lookup"><span data-stu-id="b4bb4-108">You can add two matrices of the same size by adding individual elements.</span></span> <span data-ttu-id="b4bb4-109">A ilustração a seguir mostra dois exemplos de adição de matriz.</span><span class="sxs-lookup"><span data-stu-id="b4bb4-109">The following illustration shows two examples of matrix addition.</span></span>

![ilustração que mostra como executar a adição de matriz](images/aboutgdip05-art05.png)

<span data-ttu-id="b4bb4-111">Uma matriz *m × n* pode ser multiplicada por uma matriz *n × p* e o resultado é uma matriz *m × p* .</span><span class="sxs-lookup"><span data-stu-id="b4bb4-111">An *m×n* matrix can be multiplied by an *n×p* matrix, and the result is an *m×p* matrix.</span></span> <span data-ttu-id="b4bb4-112">O número de colunas da primeira matriz deve ser igual ao número de linhas da segunda.</span><span class="sxs-lookup"><span data-stu-id="b4bb4-112">The number of columns in the first matrix must be the same as the number of rows in the second matrix.</span></span> <span data-ttu-id="b4bb4-113">Por exemplo, uma matriz de 4 × 2 pode ser multiplicada por uma matriz de 2 × 3 para produzir uma matriz 4 × 3.</span><span class="sxs-lookup"><span data-stu-id="b4bb4-113">For example, a 4 ×2 matrix can be multiplied by a 2 ×3 matrix to produce a 4 ×3 matrix.</span></span>

<span data-ttu-id="b4bb4-114">Os pontos no plano e as linhas e as colunas de uma matriz podem ser pensados como vetores.</span><span class="sxs-lookup"><span data-stu-id="b4bb4-114">Points in the plane and rows and columns of a matrix can be thought of as vectors.</span></span> <span data-ttu-id="b4bb4-115">Por exemplo, (2, 5) é um vetor com dois componentes e (3, 7, 1) é um vetor com três componentes.</span><span class="sxs-lookup"><span data-stu-id="b4bb4-115">For example, (2, 5) is a vector with two components, and (3, 7, 1) is a vector with three components.</span></span> <span data-ttu-id="b4bb4-116">O produto escalar de dois vetores é definido da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="b4bb4-116">The dot product of two vectors is defined as follows:</span></span>

<span data-ttu-id="b4bb4-117">(a, b) • (c, d) = ac + bd</span><span class="sxs-lookup"><span data-stu-id="b4bb4-117">(a, b) • (c, d) = ac + bd</span></span>

<span data-ttu-id="b4bb4-118">(a, b, c) • (d, e, f) = ad + be + cf</span><span class="sxs-lookup"><span data-stu-id="b4bb4-118">(a, b, c) • (d, e, f) = ad + be + cf</span></span>

<span data-ttu-id="b4bb4-119">Por exemplo, o produto escalar (2, 3) e (5, 4) é (2)(5) + (3)(4) = 22.</span><span class="sxs-lookup"><span data-stu-id="b4bb4-119">For example, the dot product of (2, 3) and (5, 4) is (2)(5) + (3)(4) = 22.</span></span> <span data-ttu-id="b4bb4-120">O produto escalar (2, 5, 1) e (4, 3, 1) é (2)(4) + (5)(3) + (1)(1) = 24.</span><span class="sxs-lookup"><span data-stu-id="b4bb4-120">The dot product of (2, 5, 1) and (4, 3, 1) is (2)(4) + (5)(3) + (1)(1) = 24.</span></span> <span data-ttu-id="b4bb4-121">Observe que o produto escalar de dois vetores é um número e não outro vetor.</span><span class="sxs-lookup"><span data-stu-id="b4bb4-121">Note that the dot product of two vectors is a number, not another vector.</span></span> <span data-ttu-id="b4bb4-122">Observe também que você pode calcular o produto escalar somente se os dois vetores tiverem o mesmo número de componentes.</span><span class="sxs-lookup"><span data-stu-id="b4bb4-122">Also note that you can calculate the dot product only if the two vectors have the same number of components.</span></span>

<span data-ttu-id="b4bb4-123">Permita que uma (i, j) seja a entrada na matriz A **na linha i** e a **coluna j.**</span><span class="sxs-lookup"><span data-stu-id="b4bb4-123">Let A(i, j) be the entry in matrix A in the i **th** row and the j **th** column.</span></span> <span data-ttu-id="b4bb4-124">Por exemplo, A (3, 2) é a entrada na matriz A na linha 3 **RD** e na coluna 2 **ND** .</span><span class="sxs-lookup"><span data-stu-id="b4bb4-124">For example A(3, 2) is the entry in matrix A in the 3 **rd** row and the 2 **nd** column.</span></span> <span data-ttu-id="b4bb4-125">Suponha que A, B e C são matrizes e AB = C. As entradas de C são calculadas da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="b4bb4-125">Suppose A, B, and C are matrices, and AB = C. The entries of C are calculated as follows:</span></span>

<span data-ttu-id="b4bb4-126">C(i, j) = (linha i de A) • (coluna j de B)</span><span class="sxs-lookup"><span data-stu-id="b4bb4-126">C(i, j) = (row i of A) • (column j of B)</span></span>

<span data-ttu-id="b4bb4-127">A ilustração a seguir mostra dois exemplos de multiplicação de matriz.</span><span class="sxs-lookup"><span data-stu-id="b4bb4-127">The following illustration shows several examples of matrix multiplication.</span></span>

![ilustração que mostra como executar a multiplicação de matriz](images/aboutgdip05-art06.png)

<span data-ttu-id="b4bb4-129">Se você considerar um ponto no plano como uma matriz 1 × 2, poderá transformar esse ponto multiplicando-o por uma matriz 2 × 2.</span><span class="sxs-lookup"><span data-stu-id="b4bb4-129">If you think of a point in the plane as a 1 × 2 matrix, you can transform that point by multiplying it by a 2 × 2 matrix.</span></span> <span data-ttu-id="b4bb4-130">A ilustração a seguir mostra várias transformações aplicadas ao ponto (2, 1).</span><span class="sxs-lookup"><span data-stu-id="b4bb4-130">The following illustration shows several transformations applied to the point (2, 1).</span></span>

![ilustração que mostra como usar a multiplicação de matriz para dimensionar, girar ou refletir um ponto em um plano](images/aboutgdip05-art07.png)

<span data-ttu-id="b4bb4-132">Todas as transformações mostradas na figura anterior são transformações lineares.</span><span class="sxs-lookup"><span data-stu-id="b4bb4-132">All the transformations shown in the previous figure are linear transformations.</span></span> <span data-ttu-id="b4bb4-133">Algumas outras transformações, como translação, não são lineares, e não podem ser expressas como multiplicação por uma matriz 2 × 2.</span><span class="sxs-lookup"><span data-stu-id="b4bb4-133">Certain other transformations, such as translation, are not linear, and cannot be expressed as multiplication by a 2 × 2 matrix.</span></span> <span data-ttu-id="b4bb4-134">Suponha que você deseja começar com o ponto (2, 1), girá-lo 90 graus, movê-lo em 3 unidades na direção x e 4 unidades na direção y.</span><span class="sxs-lookup"><span data-stu-id="b4bb4-134">Suppose you want to start with the point (2, 1), rotate it 90 degrees, translate it 3 units in the x direction, and translate it 4 units in the y direction.</span></span> <span data-ttu-id="b4bb4-135">Você pode fazer isso executando uma multiplicação de matriz seguida por uma adição de matriz.</span><span class="sxs-lookup"><span data-stu-id="b4bb4-135">You can accomplish this by performing a matrix multiplication followed by a matrix addition.</span></span>

![ilustração que mostra como a multiplicação de matriz e a adição podem girar um ponto e convertê-lo duas vezes](images/aboutgdip05-art08.png)

<span data-ttu-id="b4bb4-137">Uma transformação linear (multiplicação por uma matriz 2 × 2) seguida por uma tradução (adição de uma matriz de 1 × 2) é chamada de transformação afim.</span><span class="sxs-lookup"><span data-stu-id="b4bb4-137">A linear transformation (multiplication by a 2 × 2 matrix) followed by a translation (addition of a 1 × 2 matrix) is called an affine transformation.</span></span> <span data-ttu-id="b4bb4-138">Uma alternativa ao armazenamento de uma transformação afim em um par de matrizes (uma para a parte linear e outra para a tradução) é armazenar toda a transformação em uma matriz 3 × 3.</span><span class="sxs-lookup"><span data-stu-id="b4bb4-138">An alternative to storing an affine transformation in a pair of matrices (one for the linear part and one for the translation) is to store the entire transformation in a 3 × 3 matrix.</span></span> <span data-ttu-id="b4bb4-139">Para fazer isso funcionar, um ponto no plano deve ser armazenado em uma matriz 1 × 3 com uma terceira coordenada fictícia.</span><span class="sxs-lookup"><span data-stu-id="b4bb4-139">To make this work, a point in the plane must be stored in a 1 × 3 matrix with a dummy 3rd coordinate.</span></span> <span data-ttu-id="b4bb4-140">A técnica comum é fazer todas as terceiras coordenadas iguais a 1.</span><span class="sxs-lookup"><span data-stu-id="b4bb4-140">The usual technique is to make all 3rd coordinates equal to 1.</span></span> <span data-ttu-id="b4bb4-141">Por exemplo, o ponto (2, 1) é representado pela matriz \[ 2 1 1 \] .</span><span class="sxs-lookup"><span data-stu-id="b4bb4-141">For example, the point (2, 1) is represented by the matrix \[2 1 1\].</span></span> <span data-ttu-id="b4bb4-142">A ilustração a seguir mostra uma transformação afim (girar 90 graus; traduzir 3 unidades na direção x, 4 unidades na direção y) expressas como multiplicação por uma única matriz 3 × 3.</span><span class="sxs-lookup"><span data-stu-id="b4bb4-142">The following illustration shows an affine transformation (rotate 90 degrees; translate 3 units in the x direction, 4 units in the y direction) expressed as multiplication by a single 3 × 3 matrix.</span></span>

![ilustração que mostra como a multiplicação de matriz pode executar uma transformação afim](images/aboutgdip05-art09.png)

<span data-ttu-id="b4bb4-144">No exemplo anterior, o ponto (2, 1) é mapeado para o ponto (2, 6).</span><span class="sxs-lookup"><span data-stu-id="b4bb4-144">In the previous example, the point (2, 1) is mapped to the point (2, 6).</span></span> <span data-ttu-id="b4bb4-145">Observe que a terceira coluna da matriz 3 × 3 contém os números 0, 0, 1.</span><span class="sxs-lookup"><span data-stu-id="b4bb4-145">Note that the third column of the 3 × 3 matrix contains the numbers 0, 0, 1.</span></span> <span data-ttu-id="b4bb4-146">Esse será sempre o caso da matriz 3 × 3 de uma transformação afim.</span><span class="sxs-lookup"><span data-stu-id="b4bb4-146">This will always be the case for the 3 × 3 matrix of an affine transformation.</span></span> <span data-ttu-id="b4bb4-147">Os números importantes são os seis números nas colunas 1 e 2.</span><span class="sxs-lookup"><span data-stu-id="b4bb4-147">The important numbers are the six numbers in columns 1 and 2.</span></span> <span data-ttu-id="b4bb4-148">A parte superior esquerda 2 × 2 da matriz representa a parte linear da transformação e as duas primeiras entradas na terceira linha representam a tradução.</span><span class="sxs-lookup"><span data-stu-id="b4bb4-148">The upper-left 2 × 2 portion of the matrix represents the linear part of the transformation, and the first two entries in the 3rd row represent the translation.</span></span>

![ilustração mostrando que as duas primeiras colunas são mais significativas para uma matriz 3x3 de uma transformação afim](images/aboutgdip05-art10.png)

<span data-ttu-id="b4bb4-150">No Windows GDI+, você pode armazenar uma transformação afim em um objeto de [**matriz**](/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) .</span><span class="sxs-lookup"><span data-stu-id="b4bb4-150">In Windows GDI+ you can store an affine transformation in a [**Matrix**](/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) object.</span></span> <span data-ttu-id="b4bb4-151">Como a terceira coluna de uma matriz que representa uma transformação afim é sempre (0, 0, 1), você especifica apenas seis números nas duas primeiras colunas ao construir um objeto de **matriz** .</span><span class="sxs-lookup"><span data-stu-id="b4bb4-151">Because the third column of a matrix that represents an affine transformation is always (0, 0, 1), you specify only the six numbers in the first two columns when you construct a **Matrix** object.</span></span> <span data-ttu-id="b4bb4-152">A instrução `Matrix myMatrix(0.0f, 1.0f, -1.0f, 0.0f, 3.0f, 4.0f);` constrói a matriz mostrada na figura anterior.</span><span class="sxs-lookup"><span data-stu-id="b4bb4-152">The statement `Matrix myMatrix(0.0f, 1.0f, -1.0f, 0.0f, 3.0f, 4.0f);` constructs the matrix shown in the previous figure.</span></span>

## <a name="composite-transformations"></a><span data-ttu-id="b4bb4-153">Transformações de composição</span><span class="sxs-lookup"><span data-stu-id="b4bb4-153">Composite Transformations</span></span>

<span data-ttu-id="b4bb4-154">Uma transformação de composição é uma sequência de transformações, uma seguida da outra.</span><span class="sxs-lookup"><span data-stu-id="b4bb4-154">A composite transformation is a sequence of transformations, one followed by the other.</span></span> <span data-ttu-id="b4bb4-155">Considere as matrizes e transformações na lista a seguir:</span><span class="sxs-lookup"><span data-stu-id="b4bb4-155">Consider the matrices and transformations in the following list:</span></span>

-   <span data-ttu-id="b4bb4-156">Matriz A gira 90 graus</span><span class="sxs-lookup"><span data-stu-id="b4bb4-156">Matrix A    Rotate 90 degrees</span></span>
-   <span data-ttu-id="b4bb4-157">Escala da matriz B por um fator de 2 na direção x</span><span class="sxs-lookup"><span data-stu-id="b4bb4-157">Matrix B    Scale by a factor of 2 in the x direction</span></span>
-   <span data-ttu-id="b4bb4-158">Matriz C converte 3 unidades na direção y</span><span class="sxs-lookup"><span data-stu-id="b4bb4-158">Matrix C    Translate 3 units in the y direction</span></span>

<span data-ttu-id="b4bb4-159">Se você começar com o ponto (2, 1) — representado pela matriz \[ 2 1 1 \] — e multiplicado por a, B, então C, o ponto (2, 1) passará as três transformações na ordem listada.</span><span class="sxs-lookup"><span data-stu-id="b4bb4-159">If you start with the point (2, 1) — represented by the matrix \[2 1 1\] — and multiply by A, then B, then C, the point (2,1) will undergo the three transformations in the order listed.</span></span>

<span data-ttu-id="b4bb4-160">\[2 1 1 \] ABC = \[ – 2 5 1\]</span><span class="sxs-lookup"><span data-stu-id="b4bb4-160">\[2 1 1\]ABC = \[ –2 5 1\]</span></span>

<span data-ttu-id="b4bb4-161">Em vez de armazenar as três partes da transformação composta em três matrizes separadas, você pode multiplicar a, B e C em conjunto para obter uma única matriz 3 × 3 que armazena toda a transformação composta.</span><span class="sxs-lookup"><span data-stu-id="b4bb4-161">Rather than store the three parts of the composite transformation in three separate matrices, you can multiply A, B, and C together to get a single 3 × 3 matrix that stores the entire composite transformation.</span></span> <span data-ttu-id="b4bb4-162">Suponha que a ABC = D. Em seguida, um ponto multiplicado por D fornece o mesmo resultado que um ponto multiplicado por A, B e, em seguida, C.</span><span class="sxs-lookup"><span data-stu-id="b4bb4-162">Suppose ABC = D. Then a point multiplied by D gives the same result as a point multiplied by A, then B, then C.</span></span>

<span data-ttu-id="b4bb4-163">\[2 1 1 \] D = \[ – 2 5 1\]</span><span class="sxs-lookup"><span data-stu-id="b4bb4-163">\[2 1 1\]D = \[ –2 5 1\]</span></span>

<span data-ttu-id="b4bb4-164">A ilustração a seguir mostra as matrizes A, B, C e D.</span><span class="sxs-lookup"><span data-stu-id="b4bb4-164">The following illustration shows the matrices A, B, C, and D.</span></span>

![ilustração mostrando como executar várias transformações multiplicando as matrizes constituintes](images/aboutgdip05-art12.png)

<span data-ttu-id="b4bb4-166">O fato de que a matriz de uma transformação composta pode ser formada multiplicando as matrizes de transformação individuais significa que qualquer sequência de transformações afim pode ser armazenada em um único objeto [**matriz**](/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) .</span><span class="sxs-lookup"><span data-stu-id="b4bb4-166">The fact that the matrix of a composite transformation can be formed by multiplying the individual transformation matrices means that any sequence of affine transformations can be stored in a single [**Matrix**](/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) object.</span></span>

> [!Note]  
> <span data-ttu-id="b4bb4-167">A ordem de uma transformação de composição é importante.</span><span class="sxs-lookup"><span data-stu-id="b4bb4-167">The order of a composite transformation is important.</span></span> <span data-ttu-id="b4bb4-168">Em geral, girar, dimensionar e converter não é o mesmo que dimensionar, girar e converter.</span><span class="sxs-lookup"><span data-stu-id="b4bb4-168">In general, rotate, then scale, then translate is not the same as scale, then rotate, then translate.</span></span> <span data-ttu-id="b4bb4-169">Da mesma forma, a ordem de multiplicação de matriz é importante.</span><span class="sxs-lookup"><span data-stu-id="b4bb4-169">Similarly, the order of matrix multiplication is important.</span></span> <span data-ttu-id="b4bb4-170">Em geral, ABC não é o mesmo que BAC.</span><span class="sxs-lookup"><span data-stu-id="b4bb4-170">In general, ABC is not the same as BAC.</span></span>

 

<span data-ttu-id="b4bb4-171">A classe [**Matrix**](/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) fornece vários métodos para criar uma transformação composta: [**Matrix:: multiplicar**](/windows/desktop/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-multiply), [**matriz:: Rotate**](/windows/desktop/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-rotate), [**Matrix:: RotateAt**](/windows/desktop/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-rotateat), [**matriz:: Scale**](/windows/desktop/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-scale), [**Matrix:: distorcer**](/windows/desktop/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-shear)e [**Matrix:: translate**](/windows/desktop/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-translate).</span><span class="sxs-lookup"><span data-stu-id="b4bb4-171">The [**Matrix**](/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) class provides several methods for building a composite transformation: [**Matrix::Multiply**](/windows/desktop/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-multiply), [**Matrix::Rotate**](/windows/desktop/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-rotate), [**Matrix::RotateAt**](/windows/desktop/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-rotateat), [**Matrix::Scale**](/windows/desktop/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-scale), [**Matrix::Shear**](/windows/desktop/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-shear), and [**Matrix::Translate**](/windows/desktop/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-translate).</span></span> <span data-ttu-id="b4bb4-172">O exemplo a seguir cria a matriz de uma transformação composta que gira em primeiro lugar 30 graus e, em seguida, é dimensionada por um fator de 2 na direção y e, em seguida, converte 5 unidades na direção x.</span><span class="sxs-lookup"><span data-stu-id="b4bb4-172">The following example creates the matrix of a composite transformation that first rotates 30 degrees, then scales by a factor of 2 in the y direction, and then translates 5 units in the x direction.</span></span>


```
Matrix myMatrix;
myMatrix.Rotate(30.0f);
myMatrix.Scale(1.0f, 2.0f, MatrixOrderAppend);
myMatrix.Translate(5.0f, 0.0f, MatrixOrderAppend);
```



<span data-ttu-id="b4bb4-173">A ilustração a seguir mostra a matriz.</span><span class="sxs-lookup"><span data-stu-id="b4bb4-173">The following illustration shows the matrix.</span></span>

![ilustração que mostra uma matriz com valores expressos como funções trigonométricas e uma matriz com valores aproximados dessas funções](images/aboutgdip05-art13.png)

 

 



