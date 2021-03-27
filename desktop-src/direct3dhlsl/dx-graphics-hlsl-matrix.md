---
title: Tipo de matriz
description: Uma matriz é um tipo de dados especial que contém entre um e dezesseis componentes. Cada componente de uma matriz deve ser do mesmo tipo.
ms.assetid: 728eb472-103d-4c7f-b6f6-e515fc024801
keywords:
- Tipo de matriz HLSL
topic_type:
- apiref
api_name:
- Matrix Type
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c580706a2ddae3e4a94c138a1ca0f6932457732a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104006328"
---
# <a name="matrix-type"></a><span data-ttu-id="46e1a-105">Tipo de matriz</span><span class="sxs-lookup"><span data-stu-id="46e1a-105">Matrix Type</span></span>

<span data-ttu-id="46e1a-106">Uma matriz é um tipo de dados especial que contém entre um e dezesseis componentes.</span><span class="sxs-lookup"><span data-stu-id="46e1a-106">A matrix is a special data type that contains between one and sixteen components.</span></span> <span data-ttu-id="46e1a-107">Cada componente de uma matriz deve ser do mesmo tipo.</span><span class="sxs-lookup"><span data-stu-id="46e1a-107">Every component of a matrix must be of the same type.</span></span>



|                         |
|-------------------------|
| <span data-ttu-id="46e1a-108">**Nome do TypeComponents**</span><span class="sxs-lookup"><span data-stu-id="46e1a-108">**TypeComponents Name**</span></span> |



 

## <a name="components"></a><span data-ttu-id="46e1a-109">Componentes</span><span class="sxs-lookup"><span data-stu-id="46e1a-109">Components</span></span>



| <span data-ttu-id="46e1a-110">Item</span><span class="sxs-lookup"><span data-stu-id="46e1a-110">Item</span></span>                                                                                                                             | <span data-ttu-id="46e1a-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="46e1a-111">Description</span></span>                                                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="46e1a-112"><span id="TypeComponents"></span><span id="typecomponents"></span><span id="TYPECOMPONENTS"></span>**TypeComponents**</span><span class="sxs-lookup"><span data-stu-id="46e1a-112"><span id="TypeComponents"></span><span id="typecomponents"></span><span id="TYPECOMPONENTS"></span>**TypeComponents**</span></span><br/> | <span data-ttu-id="46e1a-113">Um único nome que contém três partes.</span><span class="sxs-lookup"><span data-stu-id="46e1a-113">A single name that contains three parts.</span></span> <span data-ttu-id="46e1a-114">A primeira parte é um dos tipos [escalares](dx-graphics-hlsl-data-types.md) .</span><span class="sxs-lookup"><span data-stu-id="46e1a-114">The first part is one of the [scalar](dx-graphics-hlsl-data-types.md) types.</span></span> <span data-ttu-id="46e1a-115">A segunda parte é o número de linhas.</span><span class="sxs-lookup"><span data-stu-id="46e1a-115">The second part is the number of rows.</span></span> <span data-ttu-id="46e1a-116">A terceira parte é o número de colunas.</span><span class="sxs-lookup"><span data-stu-id="46e1a-116">The third part is the number of columns.</span></span> <span data-ttu-id="46e1a-117">O número de linhas e colunas é um inteiro positivo entre 1 e 4, inclusive.</span><span class="sxs-lookup"><span data-stu-id="46e1a-117">The number of rows and columns is a positive integer between 1 and 4 inclusive.</span></span><br/> |
| <span data-ttu-id="46e1a-118"><span id="Name"></span><span id="name"></span><span id="NAME"></span>**Nomes**</span><span class="sxs-lookup"><span data-stu-id="46e1a-118"><span id="Name"></span><span id="name"></span><span id="NAME"></span>**Name**</span></span><br/>                                         | <span data-ttu-id="46e1a-119">Uma cadeia de caracteres ASCII que identifica exclusivamente o nome da variável.</span><span class="sxs-lookup"><span data-stu-id="46e1a-119">An ASCII string that uniquely identifies the variable name.</span></span><br/>                                                                                                                                                                                                                            |



 

## <a name="examples"></a><span data-ttu-id="46e1a-120">Exemplos</span><span class="sxs-lookup"><span data-stu-id="46e1a-120">Examples</span></span>

<span data-ttu-id="46e1a-121">Estes são alguns exemplos:</span><span class="sxs-lookup"><span data-stu-id="46e1a-121">Here are some examples:</span></span>


```
int1x1    iMatrix;   // integer matrix with 1 row,  1 column
int4x1    iMatrix;   // integer matrix with 4 rows, 1 column
int1x4    iMatrix;   // integer matrix with 1 row, 4 columns
double3x3 dMatrix;   // double matrix with 3 rows, 3 columns

float2x2 fMatrix = { 0.0f, 0.1, // row 1
                     2.1f, 2.2f // row 2
                   };   
```



<span data-ttu-id="46e1a-122">Uma matriz pode ser declarada usando essa sintaxe também:</span><span class="sxs-lookup"><span data-stu-id="46e1a-122">A matrix can be declared using this syntax also:</span></span>


```
matrix <Type, Number> VariableName
```



<span data-ttu-id="46e1a-123">O tipo de matriz usa os colchetes angulares para especificar o tipo, o número de linhas e o número de colunas.</span><span class="sxs-lookup"><span data-stu-id="46e1a-123">The matrix type uses the angle brackets to specify the type, the number of rows, and the number of columns.</span></span> <span data-ttu-id="46e1a-124">Este exemplo cria uma matriz de ponto flutuante, com duas linhas e duas colunas.</span><span class="sxs-lookup"><span data-stu-id="46e1a-124">This example creates a floating-point matrix, with two rows and two columns.</span></span> <span data-ttu-id="46e1a-125">Qualquer um dos tipos de dados escalares pode ser usado.</span><span class="sxs-lookup"><span data-stu-id="46e1a-125">Any of the scalar data types can be used.</span></span>

<span data-ttu-id="46e1a-126">Veja um exemplo:</span><span class="sxs-lookup"><span data-stu-id="46e1a-126">Here is an example:</span></span>


```
matrix <float, 2, 2> fMatrix = { 0.0f, 0.1, // row 1
                                 2.1f, 2.2f // row 2
                               };
```



## <a name="see-also"></a><span data-ttu-id="46e1a-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="46e1a-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46e1a-128">Tipos de dados (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="46e1a-128">Data Types (DirectX HLSL)</span></span>](dx-graphics-hlsl-data-types.md)
</dt> </dl>

 

 





