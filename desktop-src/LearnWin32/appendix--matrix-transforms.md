---
title: Transformações de matriz de apêndice
description: Este tópico fornece uma visão geral matemática das transformações de matriz para gráficos 2D.
ms.assetid: 8cc01f45-dd84-4f3e-a5f2-26edc5cbdfa1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a5a9b09f75b17e4baf8afe5e7fde8643c06982f
ms.sourcegitcommit: ee06501cc29132927ade9813e0888aaa4decc487
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/28/2021
ms.locfileid: "104559295"
---
# <a name="appendix-matrix-transforms"></a><span data-ttu-id="4c38a-103">Apêndice: transformações de matriz</span><span class="sxs-lookup"><span data-stu-id="4c38a-103">Appendix: Matrix Transforms</span></span>

<span data-ttu-id="4c38a-104">Este tópico fornece uma visão geral matemática das transformações de matriz para gráficos 2D.</span><span class="sxs-lookup"><span data-stu-id="4c38a-104">This topic provides a mathematical overview of matrix transforms for 2-D graphics.</span></span> <span data-ttu-id="4c38a-105">No entanto, você não precisa conhecer matriz matemática para usar transformações no Direct2D.</span><span class="sxs-lookup"><span data-stu-id="4c38a-105">However, you don't need to know matrix math in order to use transforms in Direct2D.</span></span> <span data-ttu-id="4c38a-106">Leia este tópico se você estiver interessado na matemática; caso contrário, fique à vontade para ignorar este tópico.</span><span class="sxs-lookup"><span data-stu-id="4c38a-106">Read this topic if you are interested in the math; otherwise, feel free to skip this topic.</span></span>

-   [<span data-ttu-id="4c38a-107">Introdução às matrizes</span><span class="sxs-lookup"><span data-stu-id="4c38a-107">Introduction to Matrices</span></span>](#introduction-to-matrices)
    -   [<span data-ttu-id="4c38a-108">Operações de matriz</span><span class="sxs-lookup"><span data-stu-id="4c38a-108">Matrix Operations</span></span>](#matrix-operations)
-   [<span data-ttu-id="4c38a-109">Transformações afim</span><span class="sxs-lookup"><span data-stu-id="4c38a-109">Affine Transforms</span></span>](#affine-transforms)
    -   [<span data-ttu-id="4c38a-110">Transformação de tradução</span><span class="sxs-lookup"><span data-stu-id="4c38a-110">Translation Transform</span></span>](#translation-transform)
    -   [<span data-ttu-id="4c38a-111">Transformação de dimensionamento</span><span class="sxs-lookup"><span data-stu-id="4c38a-111">Scaling Transform</span></span>](#scaling-transform)
    -   [<span data-ttu-id="4c38a-112">Rotação em volta da origem</span><span class="sxs-lookup"><span data-stu-id="4c38a-112">Rotation Around the Origin</span></span>](#rotation-around-the-origin)
    -   [<span data-ttu-id="4c38a-113">Rotação em um ponto arbitrário</span><span class="sxs-lookup"><span data-stu-id="4c38a-113">Rotation Around an Arbitrary Point</span></span>](#rotation-around-an-arbitrary-point)
    -   [<span data-ttu-id="4c38a-114">Transformação de distorção</span><span class="sxs-lookup"><span data-stu-id="4c38a-114">Skew Transform</span></span>](#skew-transform)
-   [<span data-ttu-id="4c38a-115">Representando transformações em Direct2D</span><span class="sxs-lookup"><span data-stu-id="4c38a-115">Representing Transforms in Direct2D</span></span>](#representing-transforms-in-direct2d)
-   [<span data-ttu-id="4c38a-116">Próximo</span><span class="sxs-lookup"><span data-stu-id="4c38a-116">Next</span></span>](#next)

## <a name="introduction-to-matrices"></a><span data-ttu-id="4c38a-117">Introdução às matrizes</span><span class="sxs-lookup"><span data-stu-id="4c38a-117">Introduction to Matrices</span></span>

<span data-ttu-id="4c38a-118">Uma matriz é uma matriz retangular de números reais.</span><span class="sxs-lookup"><span data-stu-id="4c38a-118">A matrix is a rectangular array of real numbers.</span></span> <span data-ttu-id="4c38a-119">A *ordem* da matriz é o número de linhas e colunas.</span><span class="sxs-lookup"><span data-stu-id="4c38a-119">The *order* of the matrix is the number of rows and columns.</span></span> <span data-ttu-id="4c38a-120">Por exemplo, se a matriz tiver 3 linhas e 2 colunas, a ordem será 3 × 2.</span><span class="sxs-lookup"><span data-stu-id="4c38a-120">For example, if the matrix has 3 rows and 2 columns, the order is 3 × 2.</span></span> <span data-ttu-id="4c38a-121">As matrizes são geralmente mostradas com os elementos de matriz entre colchetes:</span><span class="sxs-lookup"><span data-stu-id="4c38a-121">Matrices are usually shown with the matrix elements enclosed in square brackets:</span></span>

![matriz 3 x 2.](images/matrix01.png)

<span data-ttu-id="4c38a-123">Notação: uma matriz é designada por uma letra maiúscula.</span><span class="sxs-lookup"><span data-stu-id="4c38a-123">Notation: A matrix is designated by a capital letter.</span></span> <span data-ttu-id="4c38a-124">Os elementos são designados por letras minúsculas.</span><span class="sxs-lookup"><span data-stu-id="4c38a-124">Elements are designated by lowercase letters.</span></span> <span data-ttu-id="4c38a-125">Subscritos indicam o número de linha e coluna de um elemento.</span><span class="sxs-lookup"><span data-stu-id="4c38a-125">Subscripts indicate the row and column number of an element.</span></span> <span data-ttu-id="4c38a-126">Por exemplo, um *IJ* é o elemento na linha i'th e na coluna j'th da matriz a.</span><span class="sxs-lookup"><span data-stu-id="4c38a-126">For example, a *ij* is the element at the i'th row and j'th column of the matrix A.</span></span>

<span data-ttu-id="4c38a-127">O diagrama a seguir mostra uma matriz i × j, com os elementos individuais em cada célula da matriz.</span><span class="sxs-lookup"><span data-stu-id="4c38a-127">The following diagram shows an i × j matrix, with the individual elements in each cell of the matrix.</span></span>

![uma matriz com i Rows e colunas j.](images/matrix15.png)

### <a name="matrix-operations"></a><span data-ttu-id="4c38a-129">Operações de matriz</span><span class="sxs-lookup"><span data-stu-id="4c38a-129">Matrix Operations</span></span>

<span data-ttu-id="4c38a-130">Esta seção descreve as operações básicas definidas em matrizes.</span><span class="sxs-lookup"><span data-stu-id="4c38a-130">This section describes the basic operations defined on matrices.</span></span>

<span data-ttu-id="4c38a-131">*Adição*.</span><span class="sxs-lookup"><span data-stu-id="4c38a-131">*Addition*.</span></span> <span data-ttu-id="4c38a-132">A soma a + B de duas matrizes é obtida com a adição dos elementos correspondentes de A e B:</span><span class="sxs-lookup"><span data-stu-id="4c38a-132">The sum A + B of two matrices is obtained by adding the corresponding elements of A and B:</span></span>

<dl> <span data-ttu-id="4c38a-133">A + b = \[ a *IJ* \]  +  \[ B *IJ* \]  =  \[ a *IJ* + B *IJ*\]</span><span class="sxs-lookup"><span data-stu-id="4c38a-133">A + B = \[ a *ij* \] + \[ b *ij* \] = \[ a *ij* + b *ij* \]</span></span>
</dl>

<span data-ttu-id="4c38a-134">*Multiplicação escalar*.</span><span class="sxs-lookup"><span data-stu-id="4c38a-134">*Scalar multiplication*.</span></span> <span data-ttu-id="4c38a-135">Esta operação multiplica uma matriz por um número real.</span><span class="sxs-lookup"><span data-stu-id="4c38a-135">This operation multiplies a matrix by a real number.</span></span> <span data-ttu-id="4c38a-136">Dado um número real *k*, o produto escalar ka é obtido multiplicando cada elemento de a por *k*.</span><span class="sxs-lookup"><span data-stu-id="4c38a-136">Given a real number *k*, the scalar product kA is obtained by multiplying every element of A by *k*.</span></span>

<dl> <span data-ttu-id="4c38a-137">Ka = k \[ a *IJ* \]  =  \[ k × a *IJ*\]</span><span class="sxs-lookup"><span data-stu-id="4c38a-137">kA = k\[ a *ij* \] = \[ k × a *ij* \]</span></span>
</dl>

<span data-ttu-id="4c38a-138">*Multiplicação de matriz*.</span><span class="sxs-lookup"><span data-stu-id="4c38a-138">*Matrix multiplication*.</span></span> <span data-ttu-id="4c38a-139">Dadas duas matrizes A e B com Order (m × n) e (n × p), o produto C = A × B é uma matriz com Order (m × p), definida da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="4c38a-139">Given two matrices A and B with order (m × n) and (n × p), the product C = A × B is a matrix with order (m × p), defined as follows:</span></span>

![Mostra uma fórmula para multiplicação de matriz.](images/matrix02.png)

<span data-ttu-id="4c38a-141">ou, de maneira equivalente:</span><span class="sxs-lookup"><span data-stu-id="4c38a-141">or, equivalently:</span></span>

<dl> <span data-ttu-id="4c38a-142">c *IJ* = a *i* 1 x B1 *j* + a *i* 2 x B2 *j* +... + a *em* + b *NJ*  
</span><span class="sxs-lookup"><span data-stu-id="4c38a-142">c *ij* = a *i* 1 x b1 *j* + a *i* 2 x b2 *j* + ... + a *in* + b *nj*  
</span></span></dl>

<span data-ttu-id="4c38a-143">Ou seja, para computar cada elemento c *IJ*, faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="4c38a-143">That is, to compute each element c *ij*, do the following:</span></span>

1.  <span data-ttu-id="4c38a-144">Pegue a linha i'th de a e a coluna j'th de B.</span><span class="sxs-lookup"><span data-stu-id="4c38a-144">Take the i'th row of A and the j'th column of B.</span></span>
2.  <span data-ttu-id="4c38a-145">Multiplique cada par de elementos na linha e coluna: a primeira entrada de linha pela primeira entrada de coluna, a segunda entrada de linha pela segunda entrada de coluna e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="4c38a-145">Multiply each pair of elements in the row and column: the first row entry by the first column entry, the second row entry by the second column entry, and so forth.</span></span>
3.  <span data-ttu-id="4c38a-146">Some o resultado.</span><span class="sxs-lookup"><span data-stu-id="4c38a-146">Sum the result.</span></span>

<span data-ttu-id="4c38a-147">Aqui está um exemplo de multiplicação de uma matriz (2 × 2) por uma matriz (2 × 3).</span><span class="sxs-lookup"><span data-stu-id="4c38a-147">Here is an example of multiplying a (2 × 2) matrix by a (2 × 3) matrix.</span></span>

![multiplicação de matriz.](images/matrix03.png)

<span data-ttu-id="4c38a-149">A multiplicação de matriz não é comutada.</span><span class="sxs-lookup"><span data-stu-id="4c38a-149">Matrix multiplication is not commutative.</span></span> <span data-ttu-id="4c38a-150">Ou seja, A × B ≠ B × A. Além disso, da definição, ela segue que nem todos os pares de matrizes podem ser multiplicados.</span><span class="sxs-lookup"><span data-stu-id="4c38a-150">That is, A × B ≠ B × A. Also, from the definition it follows that not every pair of matrices can be multiplied.</span></span> <span data-ttu-id="4c38a-151">O número de colunas na matriz à esquerda deve ser igual ao número de linhas na matriz à direita.</span><span class="sxs-lookup"><span data-stu-id="4c38a-151">The number of columns in the left-hand matrix must equal the number of rows in the right-hand matrix.</span></span> <span data-ttu-id="4c38a-152">Caso contrário, o operador × não será definido.</span><span class="sxs-lookup"><span data-stu-id="4c38a-152">Otherwise, the × operator is not defined.</span></span>

<span data-ttu-id="4c38a-153">*Identificar matriz*.</span><span class="sxs-lookup"><span data-stu-id="4c38a-153">*Identify matrix*.</span></span> <span data-ttu-id="4c38a-154">Uma matriz de identidade, designada, é uma matriz quadrada definida da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="4c38a-154">An identity matrix, designated I, is a square matrix defined as follows:</span></span>

<dl> <span data-ttu-id="4c38a-155">Eu me *IJ* = 1 se *eu*  =  *j* ou 0 caso contrário.</span><span class="sxs-lookup"><span data-stu-id="4c38a-155">I *ij* = 1 if *i* = *j*, or 0 otherwise.</span></span>  
</dl>

<span data-ttu-id="4c38a-156">Em outras palavras, uma matriz de identidade contém 1 para cada elemento em que o número da linha é igual ao número da coluna e zero para todos os outros elementos.</span><span class="sxs-lookup"><span data-stu-id="4c38a-156">In other words, an identity matrix contains 1 for each element where the row number equals the column number, and zero for all other elements.</span></span> <span data-ttu-id="4c38a-157">Por exemplo, aqui está a matriz de identidade 3 × 3.</span><span class="sxs-lookup"><span data-stu-id="4c38a-157">For example, here is the 3 × 3 identity matrix.</span></span>

![matriz de identidade.](images/matrix04.png)

<span data-ttu-id="4c38a-159">O equalities a seguir mantém a matriz M.</span><span class="sxs-lookup"><span data-stu-id="4c38a-159">The following equalities hold for any matrix M.</span></span>

<dl> <span data-ttu-id="4c38a-160">M x I = M</span><span class="sxs-lookup"><span data-stu-id="4c38a-160">M x I = M</span></span>  
<span data-ttu-id="4c38a-161">X M = M</span><span class="sxs-lookup"><span data-stu-id="4c38a-161">I x M = M</span></span>  
</dl>

## <a name="affine-transforms"></a><span data-ttu-id="4c38a-162">Transformações afim</span><span class="sxs-lookup"><span data-stu-id="4c38a-162">Affine Transforms</span></span>

<span data-ttu-id="4c38a-163">Uma *transformação afim* é uma operação matemática que mapeia um espaço de coordenadas para outro.</span><span class="sxs-lookup"><span data-stu-id="4c38a-163">An *affine transform* is a mathematical operation that maps one coordinate space to another.</span></span> <span data-ttu-id="4c38a-164">Em outras palavras, ele mapeia um conjunto de pontos para outro conjunto de pontos.</span><span class="sxs-lookup"><span data-stu-id="4c38a-164">In other words, it maps one set of points to another set of points.</span></span> <span data-ttu-id="4c38a-165">As transformações afim têm alguns recursos que os tornam úteis em gráficos de computador.</span><span class="sxs-lookup"><span data-stu-id="4c38a-165">Affine transforms have some features that make them useful in computer graphics.</span></span>

-   <span data-ttu-id="4c38a-166">As transformações de afinidade preservam *Collinearity*.</span><span class="sxs-lookup"><span data-stu-id="4c38a-166">Affine transforms preserve *collinearity*.</span></span> <span data-ttu-id="4c38a-167">Se três ou mais pontos ficarem em uma linha, eles ainda formam uma linha após a transformação.</span><span class="sxs-lookup"><span data-stu-id="4c38a-167">If three or more points fall on a line, they still form a line after the transformation.</span></span> <span data-ttu-id="4c38a-168">Linhas retas permanecem retas.</span><span class="sxs-lookup"><span data-stu-id="4c38a-168">Straight lines remain straight.</span></span>
-   <span data-ttu-id="4c38a-169">A composição de duas transformações afim é uma transformação afim.</span><span class="sxs-lookup"><span data-stu-id="4c38a-169">The composition of two affine transforms is an affine transform.</span></span>

<span data-ttu-id="4c38a-170">As transformações de afinidade para o espaço de 2 D têm o seguinte formato.</span><span class="sxs-lookup"><span data-stu-id="4c38a-170">Affine transforms for 2-D space have the following form.</span></span>

![Mostra uma transformação afim para o espaço de 2-D.](images/matrix05.png)

<span data-ttu-id="4c38a-172">Se você aplicar a definição de multiplicação de matriz fornecida anteriormente, poderá mostrar que o produto de duas transformações afim é outra transformação afim.</span><span class="sxs-lookup"><span data-stu-id="4c38a-172">If you apply the definition of matrix multiplication given earlier, you can show that the product of two affine transforms is another affine transform.</span></span> <span data-ttu-id="4c38a-173">Para transformar um ponto 2D usando uma transformação afim, o ponto é representado como uma matriz 1 × 3.</span><span class="sxs-lookup"><span data-stu-id="4c38a-173">To transform a 2D point using an affine transform, the point is represented as a 1 × 3 matrix.</span></span>

<dl> <span data-ttu-id="4c38a-174">P = \| x y 1 \|</span><span class="sxs-lookup"><span data-stu-id="4c38a-174">P = \| x y 1 \|</span></span>  
</dl>

<span data-ttu-id="4c38a-175">Os dois primeiros elementos contêm as coordenadas x e y do ponto.</span><span class="sxs-lookup"><span data-stu-id="4c38a-175">The first two elements contain the x and y coordinates of the point.</span></span> <span data-ttu-id="4c38a-176">O 1 é colocado no terceiro elemento para que o cálculo do seu trabalho seja feito corretamente.</span><span class="sxs-lookup"><span data-stu-id="4c38a-176">The 1 is placed in the third element to make the math work out correctly.</span></span> <span data-ttu-id="4c38a-177">Para aplicar a transformação, multiplique as duas matrizes da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="4c38a-177">To apply the transform, multiply the two matrices as follows.</span></span>

<dl> <span data-ttu-id="4c38a-178">P ' = P × M</span><span class="sxs-lookup"><span data-stu-id="4c38a-178">P' = P × M</span></span>  
</dl>

<span data-ttu-id="4c38a-179">Isso se expande para o seguinte.</span><span class="sxs-lookup"><span data-stu-id="4c38a-179">This expands to the following.</span></span>

![a transformação afim.](images/matrix06.png)

<span data-ttu-id="4c38a-181">onde</span><span class="sxs-lookup"><span data-stu-id="4c38a-181">where</span></span>

<dl> <span data-ttu-id="4c38a-182">x ' = AX + Cy + e</span><span class="sxs-lookup"><span data-stu-id="4c38a-182">x' = ax + cy + e</span></span>  
<span data-ttu-id="4c38a-183">y ' = BX + DY + f</span><span class="sxs-lookup"><span data-stu-id="4c38a-183">y' = bx + dy + f</span></span>  
</dl>

<span data-ttu-id="4c38a-184">Para obter o ponto transformado, pegue os dois primeiros elementos da matriz P '.</span><span class="sxs-lookup"><span data-stu-id="4c38a-184">To get the transformed point, take the first two elements of matrix P'.</span></span>

<dl> <span data-ttu-id="4c38a-185">p = (x ', y ') = (AX + Cy + e, BX + DY + f)</span><span class="sxs-lookup"><span data-stu-id="4c38a-185">p = (x', y') = (ax + cy + e, bx + dy + f)</span></span>  
</dl>

> [!Note]  
> <span data-ttu-id="4c38a-186">Uma matriz 1 × *n* é chamada de *vetor de linha*.</span><span class="sxs-lookup"><span data-stu-id="4c38a-186">A 1 × *n* matrix is called a *row vector*.</span></span> <span data-ttu-id="4c38a-187">Direct2D e Direct3D usam vetores de linha para representar pontos em espaço 2D ou 3D.</span><span class="sxs-lookup"><span data-stu-id="4c38a-187">Direct2D and Direct3D both use row vectors to represent points in 2D or 3D space.</span></span> <span data-ttu-id="4c38a-188">Você pode obter um resultado equivalente usando um vetor de coluna (*n* × 1) e transposando a matriz de transformação.</span><span class="sxs-lookup"><span data-stu-id="4c38a-188">You can get an equivalent result by using a column vector (*n* × 1) and transposing the transform matrix.</span></span> <span data-ttu-id="4c38a-189">A maioria dos textos de elementos gráficos usa o formulário de vetor de coluna.</span><span class="sxs-lookup"><span data-stu-id="4c38a-189">Most graphics texts use the column vector form.</span></span> <span data-ttu-id="4c38a-190">Este tópico apresenta o formulário de vetor de linha para consistência com Direct2D e Direct3D.</span><span class="sxs-lookup"><span data-stu-id="4c38a-190">This topic presents the row vector form for consistency with Direct2D and Direct3D.</span></span>

 

<span data-ttu-id="4c38a-191">As próximas várias seções derivam as transformações básicas.</span><span class="sxs-lookup"><span data-stu-id="4c38a-191">The next several sections derive the basic transforms.</span></span>

### <a name="translation-transform"></a><span data-ttu-id="4c38a-192">Transformação de tradução</span><span class="sxs-lookup"><span data-stu-id="4c38a-192">Translation Transform</span></span>

<span data-ttu-id="4c38a-193">A matriz de transformação de tradução tem o seguinte formato.</span><span class="sxs-lookup"><span data-stu-id="4c38a-193">The translation transform matrix has the following form.</span></span>

![transformação de tradução.](images/matrix07.png)

<span data-ttu-id="4c38a-195">A conexão de um ponto *P* a esta equação resulta:</span><span class="sxs-lookup"><span data-stu-id="4c38a-195">Plugging a point *P* into this equation yields:</span></span>

<dl> <span data-ttu-id="4c38a-196">P ' = (*x*  +  *DX*, *y*  +  *DY*)</span><span class="sxs-lookup"><span data-stu-id="4c38a-196">P' = (*x* + *dx*, *y* + *dy*)</span></span>
</dl>

<span data-ttu-id="4c38a-197">que corresponde ao ponto (x, y) traduzido pelo *DX* no eixo x e *DY* no eixo y.</span><span class="sxs-lookup"><span data-stu-id="4c38a-197">which corresponds to the point (x, y) translated by *dx* in the X-axis and *dy* in the Y-axis.</span></span>

![um diagrama que mostra a tradução de dois pontos.](images/graphics22.png)

### <a name="scaling-transform"></a><span data-ttu-id="4c38a-199">Transformação de dimensionamento</span><span class="sxs-lookup"><span data-stu-id="4c38a-199">Scaling Transform</span></span>

<span data-ttu-id="4c38a-200">A matriz de transformação de dimensionamento tem o seguinte formato.</span><span class="sxs-lookup"><span data-stu-id="4c38a-200">The scaling transform matrix has the following form.</span></span>

![transformação de dimensionamento.](images/matrix09.png)

<span data-ttu-id="4c38a-202">A conexão de um ponto *P* a esta equação resulta:</span><span class="sxs-lookup"><span data-stu-id="4c38a-202">Plugging a point *P* into this equation yields:</span></span>

<dl> <span data-ttu-id="4c38a-203">P ' = (*x* ∙ *DX*, *y* ∙ *DY*)</span><span class="sxs-lookup"><span data-stu-id="4c38a-203">P' = (*x* ∙ *dx*, *y* ∙ *dy*)</span></span>
</dl>

<span data-ttu-id="4c38a-204">que corresponde ao ponto (x, y) dimensionado por *DX* e *DY*.</span><span class="sxs-lookup"><span data-stu-id="4c38a-204">which corresponds to the point (x,y) scaled by *dx* and *dy*.</span></span>

![um diagrama que mostra o dimensionamento de dois pontos.](images/graphics23.png)

### <a name="rotation-around-the-origin"></a><span data-ttu-id="4c38a-206">Rotação em volta da origem</span><span class="sxs-lookup"><span data-stu-id="4c38a-206">Rotation Around the Origin</span></span>

<span data-ttu-id="4c38a-207">A matriz para girar um ponto em volta da origem tem o seguinte formato.</span><span class="sxs-lookup"><span data-stu-id="4c38a-207">The matrix to rotate a point around the origin has the following form.</span></span>

![Mostra uma fórmula para uma transformação de rotação.](images/matrix11.png)

<span data-ttu-id="4c38a-209">O ponto transformado é:</span><span class="sxs-lookup"><span data-stu-id="4c38a-209">The transformed point is:</span></span>

<dl> <span data-ttu-id="4c38a-210">P ' = (*x* CosΘ – ysinΘ, *x* sinΘ + *y* cosΘ)</span><span class="sxs-lookup"><span data-stu-id="4c38a-210">P' = (*x* cosΘ – ysinΘ, *x* sinΘ + *y* cosΘ)</span></span>
</dl>

<span data-ttu-id="4c38a-211">Gramatica.</span><span class="sxs-lookup"><span data-stu-id="4c38a-211">Proof.</span></span> <span data-ttu-id="4c38a-212">Para mostrar que P ' representa uma rotação, considere o diagrama a seguir.</span><span class="sxs-lookup"><span data-stu-id="4c38a-212">To show that P' represents a rotation, consider the following diagram.</span></span>

![um diagrama que mostra a rotação em volta da origem.](images/graphics24.png)

<span data-ttu-id="4c38a-214">Considerando:</span><span class="sxs-lookup"><span data-stu-id="4c38a-214">Given:</span></span>

<dl> <dt>

<span data-ttu-id="4c38a-215"><span id="P____x_y_"></span><span id="p____x_y_"></span><span id="P____X_Y_"></span>P = (x, y)</span><span class="sxs-lookup"><span data-stu-id="4c38a-215"><span id="P____x_y_"></span><span id="p____x_y_"></span><span id="P____X_Y_"></span>P = (x,y)</span></span>
</dt> <dd>

<span data-ttu-id="4c38a-216">O ponto original a ser transformado.</span><span class="sxs-lookup"><span data-stu-id="4c38a-216">The original point to transform.</span></span>

</dd> <dt>

<span data-ttu-id="4c38a-217">Φ</span><span class="sxs-lookup"><span data-stu-id="4c38a-217">Φ</span></span>
</dt> <dd>

<span data-ttu-id="4c38a-218">O ângulo formado pela linha (0, 0) a P.</span><span class="sxs-lookup"><span data-stu-id="4c38a-218">The angle formed by the line (0,0) to P.</span></span>

</dd> <dt>

<span data-ttu-id="4c38a-219">Θ</span><span class="sxs-lookup"><span data-stu-id="4c38a-219">Θ</span></span>
</dt> <dd>

<span data-ttu-id="4c38a-220">O ângulo pelo qual girar (x, y) sobre a origem.</span><span class="sxs-lookup"><span data-stu-id="4c38a-220">The angle by which to rotate (x,y) about the origin.</span></span>

</dd> <dt>

<span data-ttu-id="4c38a-221"><span id="P_____x__y__"></span><span id="p_____x__y__"></span><span id="P_____X__Y__"></span>P ' = (x ', y ')</span><span class="sxs-lookup"><span data-stu-id="4c38a-221"><span id="P_____x__y__"></span><span id="p_____x__y__"></span><span id="P_____X__Y__"></span>P' = (x',y')</span></span>
</dt> <dd>

<span data-ttu-id="4c38a-222">O ponto transformado.</span><span class="sxs-lookup"><span data-stu-id="4c38a-222">The transformed point.</span></span>

</dd> <dt>

<span data-ttu-id="4c38a-223"><span id="R"></span><span id="r"></span>D</span><span class="sxs-lookup"><span data-stu-id="4c38a-223"><span id="R"></span><span id="r"></span>R</span></span>
</dt> <dd>

<span data-ttu-id="4c38a-224">O comprimento da linha (0, 0) a P. Também o raio do círculo de rotação.</span><span class="sxs-lookup"><span data-stu-id="4c38a-224">The length of the line (0,0) to P. Also the radius of the circle of rotation.</span></span>

</dd> </dl>

> [!Note]  
> <span data-ttu-id="4c38a-225">Esse diagrama usa o sistema de coordenadas padrão usado em Geometry, onde o eixo y positivo aponta para cima.</span><span class="sxs-lookup"><span data-stu-id="4c38a-225">This diagram uses the standard coordinate system used in geometry, where the positive y-axis points up.</span></span> <span data-ttu-id="4c38a-226">Direct2D usa o sistema de coordenadas do Windows, onde o eixo y positivo aponta para baixo.</span><span class="sxs-lookup"><span data-stu-id="4c38a-226">Direct2D uses the Windows coordinate system, where the positive y-axis points down.</span></span>

 

<span data-ttu-id="4c38a-227">O ângulo entre o eixo x e a linha (0, 0) para P ' é Φ + Θ.</span><span class="sxs-lookup"><span data-stu-id="4c38a-227">The angle between the x-axis and the line (0,0) to P' is Φ + Θ.</span></span> <span data-ttu-id="4c38a-228">As identidades a seguir contêm:</span><span class="sxs-lookup"><span data-stu-id="4c38a-228">The following identities hold:</span></span>

<dl> <span data-ttu-id="4c38a-229">x = R cosΦ</span><span class="sxs-lookup"><span data-stu-id="4c38a-229">x = R cosΦ</span></span>  
<span data-ttu-id="4c38a-230">y = R sinΦ</span><span class="sxs-lookup"><span data-stu-id="4c38a-230">y = R sinΦ</span></span>  
<span data-ttu-id="4c38a-231">x ' = R cos (Φ + Θ)</span><span class="sxs-lookup"><span data-stu-id="4c38a-231">x' = R cos(Φ + Θ)</span></span>  
<span data-ttu-id="4c38a-232">y ' = R sin (Φ + Θ)</span><span class="sxs-lookup"><span data-stu-id="4c38a-232">y' = R sin(Φ+ Θ)</span></span>  
</dl>

<span data-ttu-id="4c38a-233">Agora, resolva para x ' e y ' em termos de Θ.</span><span class="sxs-lookup"><span data-stu-id="4c38a-233">Now solve for x' and y' in terms of Θ.</span></span> <span data-ttu-id="4c38a-234">Pelas fórmulas de adição trigonométrica:</span><span class="sxs-lookup"><span data-stu-id="4c38a-234">By the trigonometric addition formulas:</span></span>

<dl> <span data-ttu-id="4c38a-235">x ' = R (cosΦcosΘ – sinΦsinΘ) = RcosΦcosΘ – RsinΦsinΘ</span><span class="sxs-lookup"><span data-stu-id="4c38a-235">x' = R(cosΦcosΘ – sinΦsinΘ) = RcosΦcosΘ – RsinΦsinΘ</span></span>  
<span data-ttu-id="4c38a-236">y ' = R (sinΦcosΘ + cosΦsinΘ) = RsinΦcosΘ + RcosΦsinΘ</span><span class="sxs-lookup"><span data-stu-id="4c38a-236">y' = R(sinΦcosΘ + cosΦsinΘ) = RsinΦcosΘ + RcosΦsinΘ</span></span>  
</dl>

<span data-ttu-id="4c38a-237">Substituindo, obtemos:</span><span class="sxs-lookup"><span data-stu-id="4c38a-237">Substituting, we get:</span></span>

<dl> <span data-ttu-id="4c38a-238">x ' = xcosΘ – ysinΘ</span><span class="sxs-lookup"><span data-stu-id="4c38a-238">x' = xcosΘ – ysinΘ</span></span>  
<span data-ttu-id="4c38a-239">y ' = xsinΘ + ycosΘ</span><span class="sxs-lookup"><span data-stu-id="4c38a-239">y' = xsinΘ + ycosΘ</span></span>  
</dl>

<span data-ttu-id="4c38a-240">que corresponde ao ponto transformado P ' mostrado anteriormente.</span><span class="sxs-lookup"><span data-stu-id="4c38a-240">which corresponds to the transformed point P' shown earlier.</span></span>

### <a name="rotation-around-an-arbitrary-point"></a><span data-ttu-id="4c38a-241">Rotação em um ponto arbitrário</span><span class="sxs-lookup"><span data-stu-id="4c38a-241">Rotation Around an Arbitrary Point</span></span>

<span data-ttu-id="4c38a-242">Para girar em um ponto (x, y) diferente da origem, a matriz a seguir é usada.</span><span class="sxs-lookup"><span data-stu-id="4c38a-242">To rotate around a point (x,y) other than the origin, the following matrix is used.</span></span>

![transformação de rotação.](images/matrix13.png)

<span data-ttu-id="4c38a-244">Você pode derivar essa matriz levando o ponto (x, y) para a origem.</span><span class="sxs-lookup"><span data-stu-id="4c38a-244">You can derive this matrix by taking the point (x,y) to be the origin.</span></span>

![um diagrama que mostra a rotação em um ponto.](images/graphics25.png)

<span data-ttu-id="4c38a-246">Let (x1, y1) é o ponto que resulta da rotação do ponto (x0, y0) ao contrário do ponto (x, y).</span><span class="sxs-lookup"><span data-stu-id="4c38a-246">Let (x1, y1) be the point that results from rotating the point (x0, y0) around the point (x,y).</span></span> <span data-ttu-id="4c38a-247">Podemos derivar X1 da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="4c38a-247">We can derive x1 as follows.</span></span>

<dl> <span data-ttu-id="4c38a-248">X1 = (x0 – x) cosΘ – (y0 – y) sinΘ + x</span><span class="sxs-lookup"><span data-stu-id="4c38a-248">x1 = (x0 – x)cosΘ– (y0 – y)sinΘ + x</span></span>  
<span data-ttu-id="4c38a-249">X1 = x0cosΘ – y0sinΘ + \[ (1 – cosΘ) + ysinΘ \]</span><span class="sxs-lookup"><span data-stu-id="4c38a-249">x1 = x0cosΘ – y0sinΘ + \[ (1 – cosΘ) + ysinΘ \]</span></span>  
</dl>

<span data-ttu-id="4c38a-250">Agora, conecte esta equação novamente à matriz de transformação, usando a fórmula X1 = aX0 + cy0 + e anterior.</span><span class="sxs-lookup"><span data-stu-id="4c38a-250">Now plug this equation back into the transform matrix, using the formula x1 = ax0 + cy0 + e from earlier.</span></span> <span data-ttu-id="4c38a-251">Use o mesmo procedimento para derivar Y1.</span><span class="sxs-lookup"><span data-stu-id="4c38a-251">Use the same procedure to derive y1.</span></span>

### <a name="skew-transform"></a><span data-ttu-id="4c38a-252">Transformação de distorção</span><span class="sxs-lookup"><span data-stu-id="4c38a-252">Skew Transform</span></span>

<span data-ttu-id="4c38a-253">A transformação de distorção é definida por quatro parâmetros:</span><span class="sxs-lookup"><span data-stu-id="4c38a-253">The skew transform is defined by four parameters:</span></span>

-   <span data-ttu-id="4c38a-254">Θ: o valor a ser distorcido ao longo do eixo x, medido como um ângulo do eixo y.</span><span class="sxs-lookup"><span data-stu-id="4c38a-254">Θ: The amount to skew along the x-axis, measured as an angle from the y-axis.</span></span>
-   <span data-ttu-id="4c38a-255">Φ: o valor a ser distorcido ao longo do eixo y, medido como um ângulo do eixo x.</span><span class="sxs-lookup"><span data-stu-id="4c38a-255">Φ: The amount to skew along the y-axis, measured as an angle from the x-axis.</span></span>
-   <span data-ttu-id="4c38a-256">(*PX*, *py*): as coordenadas x e y do ponto sobre o qual a distorção é executada.</span><span class="sxs-lookup"><span data-stu-id="4c38a-256">(*px*, *py*): The x- and y-coordinates of the point about which the skew is performed.</span></span>

<span data-ttu-id="4c38a-257">A transformação de distorção usa a matriz a seguir.</span><span class="sxs-lookup"><span data-stu-id="4c38a-257">The skew transform uses the following matrix.</span></span>

![transformação de distorção.](images/matrix14.png)

<span data-ttu-id="4c38a-259">O ponto transformado é:</span><span class="sxs-lookup"><span data-stu-id="4c38a-259">The transformed point is:</span></span>

<dl> <span data-ttu-id="4c38a-260">P ' = (*x*  +  *y* tanΘ – *py* tanΘ, *y*  +  *x* tanΦ) – *py* tanΦ</span><span class="sxs-lookup"><span data-stu-id="4c38a-260">P' = (*x* + *y* tanΘ – *py* tanΘ, *y* + *x* tanΦ) – *py* tanΦ</span></span>
</dl>

<span data-ttu-id="4c38a-261">ou de maneira equivalente:</span><span class="sxs-lookup"><span data-stu-id="4c38a-261">or equivalently:</span></span>

<dl> <span data-ttu-id="4c38a-262">P ' = (*x* + (*y* – *py*) tanΘ, *y* + (*x* – *PX*) tanΦ)</span><span class="sxs-lookup"><span data-stu-id="4c38a-262">P' = (*x* + (*y* – *py*)tanΘ, *y* + (*x* – *px*)tanΦ)</span></span>
</dl>

<span data-ttu-id="4c38a-263">Para ver como essa transformação funciona, considere cada componente individualmente.</span><span class="sxs-lookup"><span data-stu-id="4c38a-263">To see how this transform works, consider each component individually.</span></span> <span data-ttu-id="4c38a-264">O parâmetro Θ move todos os pontos na direção x por um valor igual a tanΘ.</span><span class="sxs-lookup"><span data-stu-id="4c38a-264">The Θ parameter moves every point in the x direction by an amount equal to tanΘ.</span></span> <span data-ttu-id="4c38a-265">O diagrama a seguir mostra a relação entre Θ e a distorção do eixo x.</span><span class="sxs-lookup"><span data-stu-id="4c38a-265">The following diagram shows the relation between Θ and the x-axis skew.</span></span>

![Diagrama que mostra a inclinação ao longo do eixo x.](images/graphics26.png)

<span data-ttu-id="4c38a-267">Aqui está a mesma distorção aplicada a um retângulo:</span><span class="sxs-lookup"><span data-stu-id="4c38a-267">Here is the same skew applied to a rectangle:</span></span>

![Diagrama que mostra a inclinação ao longo do eixo x quando aplicado a um retângulo.](images/graphics27.png)

<span data-ttu-id="4c38a-269">O parâmetro Φ tem o mesmo efeito, mas ao longo do eixo y:</span><span class="sxs-lookup"><span data-stu-id="4c38a-269">The Φ parameter has the same effect, but along the y-axis:</span></span>

![Diagrama que mostra a inclinação ao longo do eixo y.](images/graphics28.png)

<span data-ttu-id="4c38a-271">O próximo diagrama mostra a inclinação do eixo y aplicada a um retângulo.</span><span class="sxs-lookup"><span data-stu-id="4c38a-271">The next diagram shows y-axis skew applied to a rectangle.</span></span>

![Diagrama que mostra a inclinação ao longo do eixo y quando aplicado a um retângulo.](images/graphics29.png)

<span data-ttu-id="4c38a-273">Por fim, os parâmetros *PX* e *py* alternam o ponto central para a distorção ao longo dos eixos x e y.</span><span class="sxs-lookup"><span data-stu-id="4c38a-273">Finally, the parameters *px* and *py* shift the center point for the skew along the x- and y-axes.</span></span>

## <a name="representing-transforms-in-direct2d"></a><span data-ttu-id="4c38a-274">Representando transformações em Direct2D</span><span class="sxs-lookup"><span data-stu-id="4c38a-274">Representing Transforms in Direct2D</span></span>

<span data-ttu-id="4c38a-275">Todas as transformações de Direct2D são transformações afim.</span><span class="sxs-lookup"><span data-stu-id="4c38a-275">All Direct2D transforms are affine transforms.</span></span> <span data-ttu-id="4c38a-276">Direct2D não oferece suporte a transformações não afim.</span><span class="sxs-lookup"><span data-stu-id="4c38a-276">Direct2D does not support non-affine transforms.</span></span> <span data-ttu-id="4c38a-277">As transformações são representadas pela estrutura [**d2d1 \_ matriz \_ 3x2 \_ F**](/windows/desktop/Direct2D/d2d1-matrix-3x2-f) .</span><span class="sxs-lookup"><span data-stu-id="4c38a-277">Transforms are represented by the [**D2D1\_MATRIX\_3X2\_F**](/windows/desktop/Direct2D/d2d1-matrix-3x2-f) structure.</span></span> <span data-ttu-id="4c38a-278">Essa estrutura define uma matriz de 3 × 2.</span><span class="sxs-lookup"><span data-stu-id="4c38a-278">This structure defines a 3 × 2 matrix.</span></span> <span data-ttu-id="4c38a-279">Como a terceira coluna de uma transformação afim é sempre a mesma ( \[ 0, 0, 1 \] ) e como Direct2D não oferece suporte a transformações não afim, não é necessário especificar a matriz 3 × 3 inteira.</span><span class="sxs-lookup"><span data-stu-id="4c38a-279">Because the third column of an affine transform is always the same (\[0, 0, 1\]), and because Direct2D does not support non-affine transforms, there is no need to specify the entire 3 × 3 matrix.</span></span> <span data-ttu-id="4c38a-280">Internamente, o Direct2D usa matrizes de 3 × 3 para computar as transformações.</span><span class="sxs-lookup"><span data-stu-id="4c38a-280">Internally, Direct2D uses 3 × 3 matrices to compute the transforms.</span></span>

<span data-ttu-id="4c38a-281">Os membros da [**matriz d2d1 \_ \_ 3x2 \_ F**](/windows/desktop/Direct2D/d2d1-matrix-3x2-f) são nomeados de acordo com sua posição de índice: o membro **\_ 11** é o elemento (1, 1), o membro **\_ 12** é o elemento (1, 2) e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="4c38a-281">The members of the [**D2D1\_MATRIX\_3X2\_F**](/windows/desktop/Direct2D/d2d1-matrix-3x2-f) are named according to their index position: the **\_11** member is element (1,1), the **\_12** member is element (1,2), and so forth.</span></span> <span data-ttu-id="4c38a-282">Embora você possa inicializar os membros da estrutura diretamente, é recomendável usar a classe [**d2d1:: Matrix3x2F**](/windows/desktop/api/d2d1helper/nl-d2d1helper-matrix3x2f) .</span><span class="sxs-lookup"><span data-stu-id="4c38a-282">Although you can initialize the structure members directly, it is recommended to use the [**D2D1::Matrix3x2F**](/windows/desktop/api/d2d1helper/nl-d2d1helper-matrix3x2f) class.</span></span> <span data-ttu-id="4c38a-283">Essa classe herda o **d2d1 \_ Matrix \_ 3x2 \_ F** e fornece métodos auxiliares para a criação de qualquer uma das transformações de afinidade básicas.</span><span class="sxs-lookup"><span data-stu-id="4c38a-283">This class inherits **D2D1\_MATRIX\_3X2\_F** and provides helper methods for creating any of the basic affine transforms.</span></span> <span data-ttu-id="4c38a-284">A classe também define o [**operador \* ()**](/windows/desktop/api/d2d1helper/nf-d2d1helper-matrix3x2f-operator-mult) para compor duas ou mais transformações, conforme descrito em [aplicando transformações em Direct2D](applying-transforms-in-direct2d.md).</span><span class="sxs-lookup"><span data-stu-id="4c38a-284">The class also defines [**operator\*()**](/windows/desktop/api/d2d1helper/nf-d2d1helper-matrix3x2f-operator-mult) for composing two or more transforms, as described in [Applying Transforms in Direct2D](applying-transforms-in-direct2d.md).</span></span>

## <a name="next"></a><span data-ttu-id="4c38a-285">Avançar</span><span class="sxs-lookup"><span data-stu-id="4c38a-285">Next</span></span>

[<span data-ttu-id="4c38a-286">Módulo 4. Entrada do usuário</span><span class="sxs-lookup"><span data-stu-id="4c38a-286">Module 4. User Input</span></span>](module-4--user-input.md)

 

 