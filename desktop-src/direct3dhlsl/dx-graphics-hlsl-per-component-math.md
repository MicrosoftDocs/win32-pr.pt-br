---
title: Per-Component operações matemáticas
description: Com o HLSL, você pode programar sombreadores em um nível de algoritmo.
ms.assetid: a919df50-2d13-489d-9011-1137c997e121
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 5ff30cd19b7821c9a059251e105f6acfa9cf961e
ms.sourcegitcommit: fa5c081bf792b119a7bb92182cde1f85ca75967b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/17/2021
ms.locfileid: "104968758"
---
# <a name="per-component-math-operations"></a><span data-ttu-id="b5f5a-103">Per-Component operações matemáticas</span><span class="sxs-lookup"><span data-stu-id="b5f5a-103">Per-Component Math Operations</span></span>

<span data-ttu-id="b5f5a-104">Com o HLSL, você pode programar sombreadores em um nível de algoritmo.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-104">With HLSL, you can program shaders at an algorithm level.</span></span> <span data-ttu-id="b5f5a-105">Para entender a linguagem, você precisará saber como declarar variáveis e funções, usar funções intrínsecas, definir tipos de dados personalizados e usar a semântica para conectar argumentos de sombreador a outros sombreadores e ao pipeline.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-105">To understand the language, you will need to know how to declare variables and functions, use intrinsic functions, define custom data types and use semantics to connect shader arguments to other shaders and to the pipeline.</span></span>

<span data-ttu-id="b5f5a-106">Depois de aprender a criar sombreadores no HLSL, você precisará aprender sobre chamadas de API para poder: compilar um sombreador para determinado hardware, inicializar constantes de sombreador e inicializar outro Estado de pipeline, se necessário.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-106">Once you learn how to author shaders in HLSL, you will need to learn about API calls so that you can: compile a shader for particular hardware, initialize shader constants, and initialize other pipeline state if necessary.</span></span>

-   [<span data-ttu-id="b5f5a-107">O tipo de vetor</span><span class="sxs-lookup"><span data-stu-id="b5f5a-107">The Vector Type</span></span>](#the-vector-type)
-   [<span data-ttu-id="b5f5a-108">O tipo de matriz</span><span class="sxs-lookup"><span data-stu-id="b5f5a-108">The Matrix Type</span></span>](#the-matrix-type)
    -   [<span data-ttu-id="b5f5a-109">Ordenação de matriz</span><span class="sxs-lookup"><span data-stu-id="b5f5a-109">Matrix Ordering</span></span>](#matrix-ordering)
-   [<span data-ttu-id="b5f5a-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b5f5a-110">Examples</span></span>](#examples)
-   [<span data-ttu-id="b5f5a-111">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b5f5a-111">Related topics</span></span>](#related-topics)

## <a name="the-vector-type"></a><span data-ttu-id="b5f5a-112">O tipo de vetor</span><span class="sxs-lookup"><span data-stu-id="b5f5a-112">The Vector Type</span></span>

<span data-ttu-id="b5f5a-113">Um vetor é uma estrutura de dados que contém entre um e quatro componentes.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-113">A vector is a data structure that contains between one and four components.</span></span>


```
bool    bVector;   // scalar containing 1 Boolean
bool1   bVector;   // vector containing 1 Boolean
int1    iVector;   // vector containing 1 int
float3  fVector;   // vector containing 3 floats
double4 dVector;   // vector containing 4 doubles
```



<span data-ttu-id="b5f5a-114">O inteiro imediatamente após o tipo de dados é o número de componentes no vetor.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-114">The integer immediately following the data type is the number of components on the vector.</span></span>

<span data-ttu-id="b5f5a-115">Inicializadores também podem ser incluídos nas declarações.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-115">Initializers can also be included in the declarations.</span></span>


```
bool    bVector = false;
int1    iVector = 1;
float3  fVector = { 0.2f, 0.3f, 0.4f };
double4 dVector = { 0.2, 0.3, 0.4, 0.5 };
```



<span data-ttu-id="b5f5a-116">Como alternativa, o tipo de vetor pode ser usado para fazer as mesmas declarações:</span><span class="sxs-lookup"><span data-stu-id="b5f5a-116">Alternatively, the vector type can be used to make the same declarations:</span></span>


```
vector <bool,   1> bVector = false;
vector <int,    1> iVector = 1;
vector <float,  3> fVector = { 0.2f, 0.3f, 0.4f };
vector <double, 4> dVector = { 0.2, 0.3, 0.4, 0.5 };
```



<span data-ttu-id="b5f5a-117">O tipo de vetor usa colchetes angulares para especificar o tipo e o número de componentes.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-117">The vector type uses angle brackets to specify the type and number of components.</span></span>

<span data-ttu-id="b5f5a-118">Os vetores contêm até quatro componentes, cada um deles pode ser acessado usando um dos dois conjuntos de nomes:</span><span class="sxs-lookup"><span data-stu-id="b5f5a-118">Vectors contain up to four components, each of which can be accessed using one of two naming sets:</span></span>

-   <span data-ttu-id="b5f5a-119">O conjunto de posições: x, y, z, w</span><span class="sxs-lookup"><span data-stu-id="b5f5a-119">The position set: x,y,z,w</span></span>
-   <span data-ttu-id="b5f5a-120">O conjunto de cores: r, g, b, a</span><span class="sxs-lookup"><span data-stu-id="b5f5a-120">The color set: r,g,b,a</span></span>

<span data-ttu-id="b5f5a-121">Essas instruções retornam o valor no terceiro componente.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-121">These statements both return the value in the third component.</span></span>


```
// Given
float4 pos = float4(0,0,2,1);

pos.z    // value is 2
pos.b    // value is 2
```



<span data-ttu-id="b5f5a-122">Os conjuntos de nomenclatura podem usar um ou mais componentes, mas não podem ser misturados.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-122">Naming sets can use one or more components, but they cannot be mixed.</span></span>


```
// Given
float4 pos = float4(0,0,2,1);
float2 temp;

temp = pos.xy  // valid
temp = pos.rg  // valid

temp = pos.xg  // NOT VALID because the position and color sets were used.
```



<span data-ttu-id="b5f5a-123">A especificação de um ou mais componentes de vetor ao ler os componentes é chamada de swizzling.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-123">Specifying one or more vector components when reading components is called swizzling.</span></span> <span data-ttu-id="b5f5a-124">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="b5f5a-124">For example:</span></span>


```
float4 pos = float4(0,0,2,1);
float2 f_2D;
f_2D = pos.xy;   // read two components 
f_2D = pos.xz;   // read components in any order       
f_2D = pos.zx;

f_2D = pos.xx;   // components can be read more than once
f_2D = pos.yy;
```



<span data-ttu-id="b5f5a-125">O mascaramento controla quantos componentes são gravados.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-125">Masking controls how many components are written.</span></span>


```
float4 pos = float4(0,0,2,1);
float4 f_4D;
f_4D    = pos;     // write four components          

f_4D.xz = pos.xz;  // write two components        
f_4D.zx = pos.xz;  // change the write order

f_4D.xzyw = pos.w; // write one component to more than one component
f_4D.wzyx = pos;
```



<span data-ttu-id="b5f5a-126">As atribuições não podem ser gravadas no mesmo componente mais de uma vez.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-126">Assignments cannot be written to the same component more than once.</span></span> <span data-ttu-id="b5f5a-127">Portanto, o lado esquerdo desta instrução é inválido:</span><span class="sxs-lookup"><span data-stu-id="b5f5a-127">So the left side of this statement is invalid:</span></span>


```
f_4D.xx = pos.xy;   // cannot write to the same destination components 
```



<span data-ttu-id="b5f5a-128">Além disso, os espaços de nome de componente não podem ser misturados.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-128">Also, the component name spaces cannot be mixed.</span></span> <span data-ttu-id="b5f5a-129">Esta é uma gravação de componente inválida:</span><span class="sxs-lookup"><span data-stu-id="b5f5a-129">This is an invalid component write:</span></span>


```
f_4D.xg = pos.rgrg;    // invalid write: cannot mix component name spaces 
```



<span data-ttu-id="b5f5a-130">Acessar um vetor como um escalar acessará o primeiro componente do vetor.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-130">Accessing a vector as a scalar will access the first component of the vector.</span></span> <span data-ttu-id="b5f5a-131">As duas instruções a seguir são equivalentes.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-131">The following two statements are equivalent.</span></span>


```
f_4D.a = pos * 5.0f;
f_4D.a = pos.r * 5.0f;
```



## <a name="the-matrix-type"></a><span data-ttu-id="b5f5a-132">O tipo de matriz</span><span class="sxs-lookup"><span data-stu-id="b5f5a-132">The Matrix Type</span></span>

<span data-ttu-id="b5f5a-133">Uma matriz é uma estrutura de dados que contém linhas e colunas de dados.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-133">A matrix is a data structure that contains rows and columns of data.</span></span> <span data-ttu-id="b5f5a-134">Os dados podem ser qualquer um dos tipos de dados escalares, no entanto, cada elemento de uma matriz é do mesmo tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-134">The data can be any of the scalar data types, however, every element of a matrix is the same data type.</span></span> <span data-ttu-id="b5f5a-135">O número de linhas e colunas é especificado com a cadeia de caracteres de linha por coluna que é anexada ao tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-135">The number of rows and columns is specified with the row-by-column string that is appended to the data type.</span></span>


```
int1x1    iMatrix;   // integer matrix with 1 row,  1 column
int2x1    iMatrix;   // integer matrix with 2 rows, 1 column
...
int4x1    iMatrix;   // integer matrix with 4 rows, 1 column
...
int1x4    iMatrix;   // integer matrix with 1 row, 4 columns
double1x1 dMatrix;   // double matrix with 1 row,  1 column
double2x2 dMatrix;   // double matrix with 2 rows, 2 columns
double3x3 dMatrix;   // double matrix with 3 rows, 3 columns
double4x4 dMatrix;   // double matrix with 4 rows, 4 columns
```



<span data-ttu-id="b5f5a-136">O número máximo de linhas ou colunas é 4; o número mínimo é 1.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-136">The maximum number of rows or columns is 4; the minimum number is 1.</span></span>

<span data-ttu-id="b5f5a-137">Uma matriz pode ser inicializada quando ela é declarada:</span><span class="sxs-lookup"><span data-stu-id="b5f5a-137">A matrix can be initialized when it is declared:</span></span>


```
float2x2 fMatrix = { 0.0f, 0.1, // row 1
                     2.1f, 2.2f // row 2
                   };   
```



<span data-ttu-id="b5f5a-138">Ou, o tipo de matriz pode ser usado para fazer as mesmas declarações:</span><span class="sxs-lookup"><span data-stu-id="b5f5a-138">Or, the matrix type can be used to make the same declarations:</span></span>


```
matrix <float, 2, 2> fMatrix = { 0.0f, 0.1, // row 1
                                 2.1f, 2.2f // row 2
                               };
```



<span data-ttu-id="b5f5a-139">O tipo de matriz usa os colchetes angulares para especificar o tipo, o número de linhas e o número de colunas.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-139">The matrix type uses the angle brackets to specify the type, the number of rows, and the number of columns.</span></span> <span data-ttu-id="b5f5a-140">Este exemplo cria uma matriz de ponto flutuante, com duas linhas e duas colunas.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-140">This example creates a floating-point matrix, with two rows and two columns.</span></span> <span data-ttu-id="b5f5a-141">Qualquer um dos tipos de dados escalares pode ser usado.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-141">Any of the scalar data types can be used.</span></span>

<span data-ttu-id="b5f5a-142">Essa declaração define uma matriz de valores float (números de ponto flutuante de 32 bits) com duas linhas e três colunas:</span><span class="sxs-lookup"><span data-stu-id="b5f5a-142">This declaration defines a matrix of float values (32-bit floating-point numbers) with two rows and three columns:</span></span>


```
matrix <float, 2, 3> fFloatMatrix;
```



<span data-ttu-id="b5f5a-143">Uma matriz contém valores organizados em linhas e colunas, que podem ser acessadas usando o operador de estrutura "." seguido por um dos dois conjuntos de nomes:</span><span class="sxs-lookup"><span data-stu-id="b5f5a-143">A matrix contains values organized in rows and columns, which can be accessed using the structure operator "." followed by one of two naming sets:</span></span>

-   <span data-ttu-id="b5f5a-144">A posição da coluna de linha com base em zero:</span><span class="sxs-lookup"><span data-stu-id="b5f5a-144">The zero-based row-column position:</span></span>
    -   <span data-ttu-id="b5f5a-145">\_M00, \_ M01, \_ M02, \_ M03</span><span class="sxs-lookup"><span data-stu-id="b5f5a-145">\_m00, \_m01, \_m02, \_m03</span></span>
    -   <span data-ttu-id="b5f5a-146">\_M10, \_ M11, \_ M12, \_ M13</span><span class="sxs-lookup"><span data-stu-id="b5f5a-146">\_m10, \_m11, \_m12, \_m13</span></span>
    -   <span data-ttu-id="b5f5a-147">\_M20, \_ M21, \_ M22, \_ M23</span><span class="sxs-lookup"><span data-stu-id="b5f5a-147">\_m20, \_m21, \_m22, \_m23</span></span>
    -   <span data-ttu-id="b5f5a-148">\_M30, \_ M31, \_ M32, \_ M33</span><span class="sxs-lookup"><span data-stu-id="b5f5a-148">\_m30, \_m31, \_m32, \_m33</span></span>
-   <span data-ttu-id="b5f5a-149">A posição da coluna de linha baseada em um:</span><span class="sxs-lookup"><span data-stu-id="b5f5a-149">The one-based row-column position:</span></span>
    -   <span data-ttu-id="b5f5a-150">\_11, \_ 12, \_ 13, \_ 14</span><span class="sxs-lookup"><span data-stu-id="b5f5a-150">\_11, \_12, \_13, \_14</span></span>
    -   <span data-ttu-id="b5f5a-151">\_21, \_ 22, \_ 23, \_ 24</span><span class="sxs-lookup"><span data-stu-id="b5f5a-151">\_21, \_22, \_23, \_24</span></span>
    -   <span data-ttu-id="b5f5a-152">\_31, \_ 32, \_ 33, \_ 34</span><span class="sxs-lookup"><span data-stu-id="b5f5a-152">\_31, \_32, \_33, \_34</span></span>
    -   <span data-ttu-id="b5f5a-153">\_41, \_ 42, \_ 43, \_ 44</span><span class="sxs-lookup"><span data-stu-id="b5f5a-153">\_41, \_42, \_43, \_44</span></span>

<span data-ttu-id="b5f5a-154">Cada conjunto de nomenclatura começa com um sublinhado seguido pelo número da linha e o número da coluna.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-154">Each naming set starts with an underscore followed by the row number and the column number.</span></span> <span data-ttu-id="b5f5a-155">A convenção baseada em zero também inclui a letra "m" antes do número da linha e da coluna.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-155">The zero-based convention also includes the letter "m" before the row and column number.</span></span> <span data-ttu-id="b5f5a-156">Aqui está um exemplo que usa os dois conjuntos de nomes para acessar uma matriz:</span><span class="sxs-lookup"><span data-stu-id="b5f5a-156">Here's an example that uses the two naming sets to access a matrix:</span></span>


```
// given
float2x2 fMatrix = { 1.0f, 1.1f, // row 1
                     2.0f, 2.1f  // row 2
                   }; 

float f_1D;
f_1D = matrix._m00; // read the value in row 1, column 1: 1.0
f_1D = matrix._m11; // read the value in row 2, column 2: 2.1

f_1D = matrix._11;  // read the value in row 1, column 1: 1.0
f_1D = matrix._22;  // read the value in row 2, column 2: 2.1
```



<span data-ttu-id="b5f5a-157">Assim como os vetores, os conjuntos de nomes podem usar um ou mais componentes de um conjunto de nomes.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-157">Just like vectors, naming sets can use one or more components from either naming set.</span></span>


```
// Given
float2x2 fMatrix = { 1.0f, 1.1f, // row 1
                     2.0f, 2.1f  // row 2
                   };
float2 temp;

temp = fMatrix._m00_m11 // valid
temp = fMatrix._m11_m00 // valid
temp = fMatrix._11_22   // valid
temp = fMatrix._22_11   // valid
```



<span data-ttu-id="b5f5a-158">Uma matriz também pode ser acessada usando a notação de acesso de matriz, que é um conjunto de índices baseado em zero.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-158">A matrix can also be accessed using array access notation, which is a zero-based set of indices.</span></span> <span data-ttu-id="b5f5a-159">Cada índice está dentro de colchetes.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-159">Each index is inside of square brackets.</span></span> <span data-ttu-id="b5f5a-160">Uma matriz 4x4 é acessada com os seguintes índices:</span><span class="sxs-lookup"><span data-stu-id="b5f5a-160">A 4x4 matrix is accessed with the following indices:</span></span>

-   <span data-ttu-id="b5f5a-161">\[0 \] \[ 0 \] , \[ 0 \] \[ 1 \] , \[ 0 \] \[ 2 \] , \[ 0 \] \[ 3\]</span><span class="sxs-lookup"><span data-stu-id="b5f5a-161">\[0\]\[0\], \[0\]\[1\], \[0\]\[2\], \[0\]\[3\]</span></span>
-   <span data-ttu-id="b5f5a-162">\[1 \] \[ 0 \] , \[ 1 \] \[ 1 \] , \[ 1 \] \[ 2 \] , \[ 1 \] \[ 3\]</span><span class="sxs-lookup"><span data-stu-id="b5f5a-162">\[1\]\[0\], \[1\]\[1\], \[1\]\[2\], \[1\]\[3\]</span></span>
-   <span data-ttu-id="b5f5a-163">\[2 \] \[ 0 \] , \[ 2 \] \[ 1 \] , \[ 2 \] \[ 2 \] , \[ 2 \] \[ 3\]</span><span class="sxs-lookup"><span data-stu-id="b5f5a-163">\[2\]\[0\], \[2\]\[1\], \[2\]\[2\], \[2\]\[3\]</span></span>
-   <span data-ttu-id="b5f5a-164">\[3 \] \[ 0 \] , \[ 3 \] \[ 1 \] , \[ 3 \] \[ 2 \] , \[ 3 \] \[ 3\]</span><span class="sxs-lookup"><span data-stu-id="b5f5a-164">\[3\]\[0\], \[3\]\[1\], \[3\]\[2\], \[3\]\[3\]</span></span>

<span data-ttu-id="b5f5a-165">Aqui está um exemplo de acesso a uma matriz:</span><span class="sxs-lookup"><span data-stu-id="b5f5a-165">Here is an example of accessing a matrix:</span></span>


```
float2x2 fMatrix = { 1.0f, 1.1f, // row 1
                     2.0f, 2.1f  // row 2
                   };
float temp;

temp = fMatrix[0][0] // single component read
temp = fMatrix[0][1] // single component read
```



<span data-ttu-id="b5f5a-166">Observe que o operador de estrutura "." não é usado para acessar uma matriz.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-166">Notice that the structure operator "." is not used to access an array.</span></span> <span data-ttu-id="b5f5a-167">A notação de acesso à matriz não pode usar swizzling para ler mais de um componente.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-167">Array access notation cannot use swizzling to read more than one component.</span></span>


```
float2 temp;
temp = fMatrix[0][0]_[0][1] // invalid, cannot read two components
```



<span data-ttu-id="b5f5a-168">No entanto, o acesso à matriz pode ler um vetor de vários componentes.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-168">However, array accessing can read a multi-component vector.</span></span>


```
float2 temp;
float2x2 fMatrix;
temp = fMatrix[0] // read the first row
```



<span data-ttu-id="b5f5a-169">Assim como acontece com os vetores, a leitura de mais de um componente de matriz é chamada de swizzling.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-169">As with vectors, reading more than one matrix component is called swizzling.</span></span> <span data-ttu-id="b5f5a-170">Mais de um componente pode ser atribuído, pressupondo que apenas um espaço de nome seja usado.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-170">More than one component can be assigned, assuming only one name space is used.</span></span> <span data-ttu-id="b5f5a-171">Estas são todas as atribuições válidas:</span><span class="sxs-lookup"><span data-stu-id="b5f5a-171">These are all valid assignments:</span></span>


```
// Given these variables
float4x4 worldMatrix = float4( {0,0,0,0}, {1,1,1,1}, {2,2,2,2}, {3,3,3,3} );
float4x4 tempMatrix;

tempMatrix._m00_m11 = worldMatrix._m00_m11; // multiple components
tempMatrix._m00_m11 = worldMatrix.m13_m23;

tempMatrix._11_22_33 = worldMatrix._11_22_33; // any order on swizzles
tempMatrix._11_22_33 = worldMatrix._24_23_22;
```



<span data-ttu-id="b5f5a-172">O mascaramento controla quantos componentes são gravados.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-172">Masking controls how many components are written.</span></span>


```
// Given
float4x4 worldMatrix = float4( {0,0,0,0}, {1,1,1,1}, {2,2,2,2}, {3,3,3,3} );
float4x4 tempMatrix;

tempMatrix._m00_m11 = worldMatrix._m00_m11; // write two components
tempMatrix._m23_m00 = worldMatrix._m00_m11;
```



<span data-ttu-id="b5f5a-173">As atribuições não podem ser gravadas no mesmo componente mais de uma vez.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-173">Assignments cannot be written to the same component more than once.</span></span> <span data-ttu-id="b5f5a-174">Portanto, o lado esquerdo desta instrução é inválido:</span><span class="sxs-lookup"><span data-stu-id="b5f5a-174">So the left side of this statement is invalid:</span></span>


```
// cannot write to the same component more than once
tempMatrix._m00_m00 = worldMatrix._m00_m11;
```



<span data-ttu-id="b5f5a-175">Além disso, os espaços de nome de componente não podem ser misturados.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-175">Also, the component name spaces cannot be mixed.</span></span> <span data-ttu-id="b5f5a-176">Esta é uma gravação de componente inválida:</span><span class="sxs-lookup"><span data-stu-id="b5f5a-176">This is an invalid component write:</span></span>


```
// Invalid use of same component on left side
tempMatrix._11_m23 = worldMatrix._11_22; 
```



### <a name="matrix-ordering"></a><span data-ttu-id="b5f5a-177">Ordenação de matriz</span><span class="sxs-lookup"><span data-stu-id="b5f5a-177">Matrix Ordering</span></span>

<span data-ttu-id="b5f5a-178">Ordem de embalagem de matriz para parâmetros uniformes é definido como coluna-principal por padrão.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-178">Matrix packing order for uniform parameters is set to column-major by default.</span></span> <span data-ttu-id="b5f5a-179">Isso significa que cada coluna da matriz é armazenada em um único registro constante.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-179">This means each column of the matrix is stored in a single constant register.</span></span> <span data-ttu-id="b5f5a-180">Por outro lado, uma matriz de linha principal empacota cada linha da matriz em um único registro constante.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-180">On the other hand, a row-major matrix packs each row of the matrix in a single constant register.</span></span> <span data-ttu-id="b5f5a-181">A embalagem de matriz pode ser alterada com a diretiva de **\# \_ matriz pragmapack** ou com a **linha \_ principal** ou a palavra-chave **\_ Major da coluna** .</span><span class="sxs-lookup"><span data-stu-id="b5f5a-181">Matrix packing can be changed with the **\#pragmapack\_matrix** directive, or with the **row\_major** or the **column\_major** keyword.</span></span>

<span data-ttu-id="b5f5a-182">Os dados em uma matriz são carregados em registros de constante de sombreador antes de um sombreador ser executado.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-182">The data in a matrix is loaded into shader constant registers before a shader runs.</span></span> <span data-ttu-id="b5f5a-183">Há duas opções de como os dados da matriz são lidos: na ordem principal da linha ou na ordem principal da coluna.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-183">There are two choices for how the matrix data is read: in row-major order or in column-major order.</span></span> <span data-ttu-id="b5f5a-184">Coluna-a ordem principal significa que cada coluna de matriz será armazenada em um único registro de constante e a ordem de principal de linha significa que cada linha da matriz será armazenada em um único registro constante.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-184">Column-major order means that each matrix column will be stored in a single constant register, and row-major order means that each row of the matrix will be stored in a single constant register.</span></span> <span data-ttu-id="b5f5a-185">Essa é uma consideração importante para quantos registros constantes são usados para uma matriz.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-185">This is an important consideration for how many constant registers are used for a matrix.</span></span>

<span data-ttu-id="b5f5a-186">Uma matriz de linha principal é disposta da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="b5f5a-186">A row-major matrix is laid out like the following:</span></span>



|     |     |     |     |
|-----|-----|-----|-----|
| <span data-ttu-id="b5f5a-187">11</span><span class="sxs-lookup"><span data-stu-id="b5f5a-187">11</span></span>  | <span data-ttu-id="b5f5a-188">12</span><span class="sxs-lookup"><span data-stu-id="b5f5a-188">12</span></span>  | <span data-ttu-id="b5f5a-189">13</span><span class="sxs-lookup"><span data-stu-id="b5f5a-189">13</span></span>  | <span data-ttu-id="b5f5a-190">14</span><span class="sxs-lookup"><span data-stu-id="b5f5a-190">14</span></span>  |
| <span data-ttu-id="b5f5a-191">21</span><span class="sxs-lookup"><span data-stu-id="b5f5a-191">21</span></span>  | <span data-ttu-id="b5f5a-192">22</span><span class="sxs-lookup"><span data-stu-id="b5f5a-192">22</span></span>  | <span data-ttu-id="b5f5a-193">23</span><span class="sxs-lookup"><span data-stu-id="b5f5a-193">23</span></span>  | <span data-ttu-id="b5f5a-194">24</span><span class="sxs-lookup"><span data-stu-id="b5f5a-194">24</span></span>  |
| <span data-ttu-id="b5f5a-195">31</span><span class="sxs-lookup"><span data-stu-id="b5f5a-195">31</span></span>  | <span data-ttu-id="b5f5a-196">32</span><span class="sxs-lookup"><span data-stu-id="b5f5a-196">32</span></span>  | <span data-ttu-id="b5f5a-197">33</span><span class="sxs-lookup"><span data-stu-id="b5f5a-197">33</span></span>  | <span data-ttu-id="b5f5a-198">34</span><span class="sxs-lookup"><span data-stu-id="b5f5a-198">34</span></span>  |
| <span data-ttu-id="b5f5a-199">41</span><span class="sxs-lookup"><span data-stu-id="b5f5a-199">41</span></span>  | <span data-ttu-id="b5f5a-200">42</span><span class="sxs-lookup"><span data-stu-id="b5f5a-200">42</span></span>  | <span data-ttu-id="b5f5a-201">43</span><span class="sxs-lookup"><span data-stu-id="b5f5a-201">43</span></span>  | <span data-ttu-id="b5f5a-202">44</span><span class="sxs-lookup"><span data-stu-id="b5f5a-202">44</span></span>  |



 

<span data-ttu-id="b5f5a-203">Uma matriz de coluna principal é disposta da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="b5f5a-203">A column-major matrix is laid out like the following:</span></span>



|     |     |     |     |
|-----|-----|-----|-----|
| <span data-ttu-id="b5f5a-204">11</span><span class="sxs-lookup"><span data-stu-id="b5f5a-204">11</span></span>  | <span data-ttu-id="b5f5a-205">21</span><span class="sxs-lookup"><span data-stu-id="b5f5a-205">21</span></span>  | <span data-ttu-id="b5f5a-206">31</span><span class="sxs-lookup"><span data-stu-id="b5f5a-206">31</span></span>  | <span data-ttu-id="b5f5a-207">41</span><span class="sxs-lookup"><span data-stu-id="b5f5a-207">41</span></span>  |
| <span data-ttu-id="b5f5a-208">12</span><span class="sxs-lookup"><span data-stu-id="b5f5a-208">12</span></span>  | <span data-ttu-id="b5f5a-209">22</span><span class="sxs-lookup"><span data-stu-id="b5f5a-209">22</span></span>  | <span data-ttu-id="b5f5a-210">32</span><span class="sxs-lookup"><span data-stu-id="b5f5a-210">32</span></span>  | <span data-ttu-id="b5f5a-211">42</span><span class="sxs-lookup"><span data-stu-id="b5f5a-211">42</span></span>  |
| <span data-ttu-id="b5f5a-212">13</span><span class="sxs-lookup"><span data-stu-id="b5f5a-212">13</span></span>  | <span data-ttu-id="b5f5a-213">23</span><span class="sxs-lookup"><span data-stu-id="b5f5a-213">23</span></span>  | <span data-ttu-id="b5f5a-214">33</span><span class="sxs-lookup"><span data-stu-id="b5f5a-214">33</span></span>  | <span data-ttu-id="b5f5a-215">43</span><span class="sxs-lookup"><span data-stu-id="b5f5a-215">43</span></span>  |
| <span data-ttu-id="b5f5a-216">14</span><span class="sxs-lookup"><span data-stu-id="b5f5a-216">14</span></span>  | <span data-ttu-id="b5f5a-217">24</span><span class="sxs-lookup"><span data-stu-id="b5f5a-217">24</span></span>  | <span data-ttu-id="b5f5a-218">34</span><span class="sxs-lookup"><span data-stu-id="b5f5a-218">34</span></span>  | <span data-ttu-id="b5f5a-219">44</span><span class="sxs-lookup"><span data-stu-id="b5f5a-219">44</span></span>  |



 

<span data-ttu-id="b5f5a-220">Classificação de matriz de linha principal e coluna-principal determine a ordem em que os componentes de matriz são lidos de entradas de sombreador.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-220">Row-major and column-major matrix ordering determine the order the matrix components are read from shader inputs.</span></span> <span data-ttu-id="b5f5a-221">Depois que os dados são gravados em registros constantes, a ordem de matriz não tem nenhum efeito sobre como os dados são usados ou acessados no código do sombreador.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-221">Once the data is written into constant registers, matrix order has no effect on how the data is used or accessed from within shader code.</span></span> <span data-ttu-id="b5f5a-222">Além disso, as matrizes declaradas em um corpo de sombreador não são incluídas em registros constantes.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-222">Also, matrices declared in a shader body do not get packed into constant registers.</span></span> <span data-ttu-id="b5f5a-223">A ordem de embalagem de linha principal e coluna-principal não tem influência sobre a ordem de embalagem dos construtores (que sempre segue a ordenação da linha principal).</span><span class="sxs-lookup"><span data-stu-id="b5f5a-223">Row-major and column-major packing order has no influence on the packing order of constructors (which always follows row-major ordering).</span></span>

<span data-ttu-id="b5f5a-224">A ordem dos dados em uma matriz pode ser declarada no momento da compilação ou o compilador solicitará os dados em tempo de execução para o uso mais eficiente.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-224">The order of the data in a matrix can be declared at compile time or the compiler will order the data at runtime for the most efficient use.</span></span>

## <a name="examples"></a><span data-ttu-id="b5f5a-225">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b5f5a-225">Examples</span></span>

<span data-ttu-id="b5f5a-226">O HLSL usa dois tipos especiais, um tipo de vetor e um tipo de matriz para facilitar a programação de gráficos 2D e 3D.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-226">HLSL uses two special types, a vector type and a matrix type to make programming 2D and 3D graphics easier.</span></span> <span data-ttu-id="b5f5a-227">Cada um desses tipos contém mais de um componente; um vetor contém até quatro componentes, e uma matriz contém até 16 componentes.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-227">Each of these types contain more than one component; a vector contains up to four components, and a matrix contains up to 16 components.</span></span> <span data-ttu-id="b5f5a-228">Quando vetores e matrizes são usados em equações HLSLs padrão, a matemática realizada é projetada para funcionar por componente.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-228">When vectors and matrices are used in standard HLSL equations, the math performed is designed to work per-component.</span></span> <span data-ttu-id="b5f5a-229">Por exemplo, HLSL implementa essa multiplicação:</span><span class="sxs-lookup"><span data-stu-id="b5f5a-229">For instance, HLSL implements this multiply:</span></span>


```
float4 v = a*b;
```



<span data-ttu-id="b5f5a-230">como uma multiplicação de quatro componentes.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-230">as a four-component multiply.</span></span> <span data-ttu-id="b5f5a-231">O resultado é quatro escalares:</span><span class="sxs-lookup"><span data-stu-id="b5f5a-231">The result is four scalars:</span></span>


```
float4 v = a*b;

v.x = a.x*b.x;
v.y = a.y*b.y;
v.z = a.z*b.z;
v.w = a.w*b.w;
```



<span data-ttu-id="b5f5a-232">São quatro multiplicações em que cada resultado é armazenado em um componente separado do v.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-232">This is four multiplications where each result is stored in a separate component of v.</span></span> <span data-ttu-id="b5f5a-233">Isso é chamado de multiplicação de quatro componentes.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-233">This is called a four-component multiply.</span></span> <span data-ttu-id="b5f5a-234">O HLSL usa a matemática do componente, o que torna os sombreadores de escrita muito eficientes.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-234">HLSL uses component math which makes writing shaders very efficient.</span></span>

<span data-ttu-id="b5f5a-235">Isso é muito diferente de uma multiplicação, que normalmente é implementada como um produto de ponto que gera um único escalar:</span><span class="sxs-lookup"><span data-stu-id="b5f5a-235">This is very different from a multiply which is typically implemented as a dot product which generates a single scalar:</span></span>


```
v = a.x*b.x + a.y*b.y + a.z*b.z + a.w*b.w;
```



<span data-ttu-id="b5f5a-236">Uma matriz também usa operações por componente em HLSL:</span><span class="sxs-lookup"><span data-stu-id="b5f5a-236">A matrix also uses per-component operations in HLSL:</span></span>


```
float3x3 mat1,mat2;
...
float3x3 mat3 = mat1*mat2;
```



<span data-ttu-id="b5f5a-237">O resultado é uma multiplicação por componente das duas matrizes (em oposição a uma multiplicação padrão de matriz 3x3).</span><span class="sxs-lookup"><span data-stu-id="b5f5a-237">The result is a per-component multiply of the two matrices (as opposed to a standard 3x3 matrix multiply).</span></span> <span data-ttu-id="b5f5a-238">Uma multiplicação por matriz de componente produz esse primeiro termo:</span><span class="sxs-lookup"><span data-stu-id="b5f5a-238">A per component matrix multiply yields this first term:</span></span>


```
mat3.m00 = mat1.m00 * mat2._m00;
```



<span data-ttu-id="b5f5a-239">Isso é diferente de uma multiplicação de matriz 3x3 que produziria esse primeiro termo:</span><span class="sxs-lookup"><span data-stu-id="b5f5a-239">This is different from a 3x3 matrix multiply which would yield this first term:</span></span>


```
// First component of a four-component matrix multiply
mat.m00 = mat1._m00 * mat2._m00 + 
          mat1._m01 * mat2._m10 + 
          mat1._m02 * mat2._m20 + 
          mat1._m03 * mat2._m30;
```



<span data-ttu-id="b5f5a-240">Versões sobrecarregadas da função intrínseca de multiplicação tratam casos em que um operando é um vetor e o outro operando é uma matriz.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-240">Overloaded versions of the multiply intrinsic function handle cases where one operand is a vector and the other operand is a matrix.</span></span> <span data-ttu-id="b5f5a-241">Como: \* vetor de vetor, \* matriz de vetor, \* vetor de matriz e \* matriz de matriz.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-241">Such as: vector \* vector, vector \* matrix, matrix \* vector, and matrix \* matrix.</span></span> <span data-ttu-id="b5f5a-242">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="b5f5a-242">For instance:</span></span>


```
float4x3 World;

float4 main(float4 pos : SV_POSITION) : SV_POSITION
{
    float4 val;
    val.xyz = mul(pos,World);
    val.w = 0;

    return val;
}   
```



<span data-ttu-id="b5f5a-243">produz o mesmo resultado que:</span><span class="sxs-lookup"><span data-stu-id="b5f5a-243">produces the same result as:</span></span>


```
float4x3 World;

float4 main(float4 pos : SV_POSITION) : SV_POSITION
{
    float4 val;
    val.xyz = (float3) mul((float1x4)pos,World);
    val.w = 0;

    return val;
}   
```



<span data-ttu-id="b5f5a-244">Este exemplo converte o vetor de pos em um vetor de coluna usando a conversão (float1x4).</span><span class="sxs-lookup"><span data-stu-id="b5f5a-244">This example casts the pos vector to a column vector using the (float1x4) cast.</span></span> <span data-ttu-id="b5f5a-245">A alteração de um vetor por meio da conversão ou troca da ordem dos argumentos fornecidos para multiplicar é equivalente a transposição da matriz.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-245">Changing a vector by casting, or swapping the order of the arguments supplied to multiply is equivalent to transposing the matrix.</span></span>

<span data-ttu-id="b5f5a-246">Conversão de conversão automática faz com que as funções de multiplicação e de ponto intrínsecos retornem os mesmos resultados usados aqui:</span><span class="sxs-lookup"><span data-stu-id="b5f5a-246">Automatic cast conversion causes the multiply and dot intrinsic functions to return the same results as used here:</span></span>


```
{
  float4 val;
  return mul(val,val);
}
```



<span data-ttu-id="b5f5a-247">Esse resultado da multiplicação é um \* 4x = 1x1 vector.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-247">This result of the multiply is a 1x4 \* 4x1 = 1x1 vector.</span></span> <span data-ttu-id="b5f5a-248">Isso é equivalente a um produto de ponto:</span><span class="sxs-lookup"><span data-stu-id="b5f5a-248">This is equivalent to a dot product:</span></span>


```
{
  float4 val;
  return dot(val,val);
}
```



<span data-ttu-id="b5f5a-249">que retorna um único valor escalar.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-249">which returns a single scalar value.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b5f5a-250">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b5f5a-250">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b5f5a-251">Tipos de dados (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b5f5a-251">Data Types (DirectX HLSL)</span></span>](dx-graphics-hlsl-data-types.md)
</dt> </dl>

 

 




