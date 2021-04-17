---
title: Operadores
description: As expressões são sequências de variáveis e literais pontuados por operadores.
ms.assetid: c31aa0b8-1284-48aa-b000-d72433f0f5cc
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 69fc29f366fa781483edb5fd4653674b387fd156
ms.sourcegitcommit: 37fb32f6150b6ca1db6c52d68a553ec2c8c0879a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/22/2020
ms.locfileid: "104453871"
---
# <a name="operators"></a><span data-ttu-id="7a2f9-103">Operadores</span><span class="sxs-lookup"><span data-stu-id="7a2f9-103">Operators</span></span>

<span data-ttu-id="7a2f9-104">As expressões são sequências de [variáveis](dx-graphics-hlsl-variable-syntax.md) e literais pontuados por [operadores](dx-graphics-hlsl-statement-blocks.md).</span><span class="sxs-lookup"><span data-stu-id="7a2f9-104">Expressions are sequences of [variables](dx-graphics-hlsl-variable-syntax.md) and literals punctuated by [operators](dx-graphics-hlsl-statement-blocks.md).</span></span> <span data-ttu-id="7a2f9-105">Os operadores determinam como as variáveis e os literais são combinados, comparados, selecionados e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="7a2f9-105">Operators determine how the variables and literals are combined, compared, selected, and so on.</span></span> <span data-ttu-id="7a2f9-106">Os operadores incluem:</span><span class="sxs-lookup"><span data-stu-id="7a2f9-106">The operators include:</span></span>



|                                                                                 |                                                                    |
|---------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="7a2f9-107">Nome do operador</span><span class="sxs-lookup"><span data-stu-id="7a2f9-107">Operator Name</span></span>                                                                   | <span data-ttu-id="7a2f9-108">Operadores</span><span class="sxs-lookup"><span data-stu-id="7a2f9-108">Operators</span></span>                                                          |
| [<span data-ttu-id="7a2f9-109">Operadores aditivos e multiplicativas</span><span class="sxs-lookup"><span data-stu-id="7a2f9-109">Additive and Multiplicative Operators</span></span>](#additive-and-multiplicative-operators) | <span data-ttu-id="7a2f9-110">+, -, \*, /, %</span><span class="sxs-lookup"><span data-stu-id="7a2f9-110">+, -, \*, /, %</span></span>                                                     |
| [<span data-ttu-id="7a2f9-111">Operador de matriz</span><span class="sxs-lookup"><span data-stu-id="7a2f9-111">Array Operator</span></span>](#array-operator)                                               | <span data-ttu-id="7a2f9-112">\[i\]</span><span class="sxs-lookup"><span data-stu-id="7a2f9-112">\[i\]</span></span>                                                              |
| [<span data-ttu-id="7a2f9-113">Operadores de atribuição</span><span class="sxs-lookup"><span data-stu-id="7a2f9-113">Assignment Operators</span></span>](#assignment-operators)                                   | <span data-ttu-id="7a2f9-114">=, +=, -=, \*=, /=, %=</span><span class="sxs-lookup"><span data-stu-id="7a2f9-114">=, +=, -=, \*=, /=, %=</span></span>                                             |
| [<span data-ttu-id="7a2f9-115">Conversões binárias</span><span class="sxs-lookup"><span data-stu-id="7a2f9-115">Binary Casts</span></span>](#binary-casts)                                                   | <span data-ttu-id="7a2f9-116">Regras c para as regras float e int, C ou intrínsecos HLSL para bool</span><span class="sxs-lookup"><span data-stu-id="7a2f9-116">C rules for float and int, C rules or HLSL intrinsics for bool</span></span>     |
| [<span data-ttu-id="7a2f9-117">Operadores bit a bit</span><span class="sxs-lookup"><span data-stu-id="7a2f9-117">Bitwise Operators</span></span>](#bitwise-operators)                                         | <span data-ttu-id="7a2f9-118">~,  <<,  >>, &, \| , ^,  <<=,  >>=, &=, \| =, ^ =</span><span class="sxs-lookup"><span data-stu-id="7a2f9-118">~, <<, >>, &, \|, ^, <<=, >>=, &=, \|=, ^=</span></span> |
| [<span data-ttu-id="7a2f9-119">Operadores matemáticos boolianos</span><span class="sxs-lookup"><span data-stu-id="7a2f9-119">Boolean Math Operators</span></span>](#boolean-math-operators)                               | <span data-ttu-id="7a2f9-120">& &, \| \| ,?:</span><span class="sxs-lookup"><span data-stu-id="7a2f9-120">& &, \|\|, ?:</span></span>                                                      |
| [<span data-ttu-id="7a2f9-121">Operador cast</span><span class="sxs-lookup"><span data-stu-id="7a2f9-121">Cast Operator</span></span>](#cast-operator)                                                 | <span data-ttu-id="7a2f9-122">Escreva</span><span class="sxs-lookup"><span data-stu-id="7a2f9-122">(type)</span></span>                                                             |
| [<span data-ttu-id="7a2f9-123">Operador de vírgula</span><span class="sxs-lookup"><span data-stu-id="7a2f9-123">Comma Operator</span></span>](#comma-operator)                                               | <span data-ttu-id="7a2f9-124">,</span><span class="sxs-lookup"><span data-stu-id="7a2f9-124">,</span></span>                                                                  |
| [<span data-ttu-id="7a2f9-125">Operadores de comparação</span><span class="sxs-lookup"><span data-stu-id="7a2f9-125">Comparison Operators</span></span>](#comparison-operators)                                   | <span data-ttu-id="7a2f9-126"><, >, = =,! =, <=, >=</span><span class="sxs-lookup"><span data-stu-id="7a2f9-126"><, >, ==, !=, <=, >=</span></span>                                   |
| [<span data-ttu-id="7a2f9-127">Operadores de prefixo ou sufixo</span><span class="sxs-lookup"><span data-stu-id="7a2f9-127">Prefix or Postfix Operators</span></span>](#prefix-or-postfix-operators)                     | <span data-ttu-id="7a2f9-128">++, --</span><span class="sxs-lookup"><span data-stu-id="7a2f9-128">++, --</span></span>                                                             |
| [<span data-ttu-id="7a2f9-129">Operador de estrutura</span><span class="sxs-lookup"><span data-stu-id="7a2f9-129">Structure Operator</span></span>](#structure-operator)                                       | <span data-ttu-id="7a2f9-130">.</span><span class="sxs-lookup"><span data-stu-id="7a2f9-130">.</span></span>                                                                  |
| [<span data-ttu-id="7a2f9-131">Operadores unários</span><span class="sxs-lookup"><span data-stu-id="7a2f9-131">Unary Operators</span></span>](#unary-operators)                                             | <span data-ttu-id="7a2f9-132">!, -, +</span><span class="sxs-lookup"><span data-stu-id="7a2f9-132">!, -, +</span></span>                                                            |



 

<span data-ttu-id="7a2f9-133">Muitos dos operadores são por componente, o que significa que a operação é executada de forma independente para cada componente de cada variável.</span><span class="sxs-lookup"><span data-stu-id="7a2f9-133">Many of the operators are per-component, which means that the operation is performed independently for each component of each variable.</span></span> <span data-ttu-id="7a2f9-134">Por exemplo, uma única variável de componente tem uma operação executada.</span><span class="sxs-lookup"><span data-stu-id="7a2f9-134">For example, a single component variable has one operation performed.</span></span> <span data-ttu-id="7a2f9-135">Por outro lado, uma variável de quatro componentes tem quatro operações executadas, uma para cada componente.</span><span class="sxs-lookup"><span data-stu-id="7a2f9-135">On the other hand, a four-component variable has four operations performed, one for each component.</span></span>

<span data-ttu-id="7a2f9-136">Todos os operadores que fazem algo com o valor, como + e \* , funcionam por componente.</span><span class="sxs-lookup"><span data-stu-id="7a2f9-136">All of the operators that do something to the value, such as + and \*, work per component.</span></span>

<span data-ttu-id="7a2f9-137">Os operadores de comparação exigem que um único componente funcione, a menos que você use a função [**All**](dx-graphics-hlsl-all.md) [**ou intrínseca**](dx-graphics-hlsl-any.md) com uma variável de vários componentes.</span><span class="sxs-lookup"><span data-stu-id="7a2f9-137">The comparison operators require a single component to work unless you use the [**all**](dx-graphics-hlsl-all.md) or [**any**](dx-graphics-hlsl-any.md) intrinsic function with a multiple-component variable.</span></span> <span data-ttu-id="7a2f9-138">A operação a seguir falha porque a instrução If requer um bool único, mas recebe um bool4:</span><span class="sxs-lookup"><span data-stu-id="7a2f9-138">The following operation fails because the if statement requires a single bool but receives a bool4:</span></span>


```
if (A4 < B4)
```



<span data-ttu-id="7a2f9-139">As seguintes operações foram realizadas com sucesso:</span><span class="sxs-lookup"><span data-stu-id="7a2f9-139">The following operations succeed:</span></span>


```
if ( any(A4 < B4) )
if ( all(A4 < B4) )
```



<span data-ttu-id="7a2f9-140">Os operadores de conversão binária [**asfloat**](dx-graphics-hlsl-asfloat.md), [**asent**](dx-graphics-hlsl-asint.md)e assim por diante funcionam por componente, com exceção de [**duas vezes**](asdouble.md) cujas regras especiais são documentadas.</span><span class="sxs-lookup"><span data-stu-id="7a2f9-140">The binary cast operators [**asfloat**](dx-graphics-hlsl-asfloat.md), [**asint**](dx-graphics-hlsl-asint.md), and so on work per component except for [**asdouble**](asdouble.md) whose special rules are documented.</span></span>

<span data-ttu-id="7a2f9-141">Operadores de seleção como ponto, vírgula e colchetes de matriz não funcionam por componente.</span><span class="sxs-lookup"><span data-stu-id="7a2f9-141">Selection operators like period, comma, and array brackets do not work per component.</span></span>

<span data-ttu-id="7a2f9-142">Os operadores de conversão alteram o número de componentes.</span><span class="sxs-lookup"><span data-stu-id="7a2f9-142">Cast operators change the number of components.</span></span> <span data-ttu-id="7a2f9-143">As operações de conversão a seguir mostram sua equivalência:</span><span class="sxs-lookup"><span data-stu-id="7a2f9-143">The following cast operations show their equivalence:</span></span>


```
(float) i4 ->   float(i4.x)
(float4)i ->   float4(i, i, i, i)
```



## <a name="additive-and-multiplicative-operators"></a><span data-ttu-id="7a2f9-144">Operadores aditivos e multiplicativas</span><span class="sxs-lookup"><span data-stu-id="7a2f9-144">Additive and Multiplicative Operators</span></span>

<span data-ttu-id="7a2f9-145">Os operadores aditivo e multiplicativa são: +,-, \* ,/,%</span><span class="sxs-lookup"><span data-stu-id="7a2f9-145">The additive and multiplicative operators are: +, -, \*, /, %</span></span>


```
int i1 = 1;
int i2 = 2;
int i3 = i1 + i2;  // i3 = 3
i3 = i1 * i2;        // i3 = 1 * 2 = 2
```




```
i3 = i1/i2;       // i3 = 1/3 = 0.333. Truncated to 0 because i3 is an integer.
i3 = i2/i1;       // i3 = 2/1 = 2
```




```
float f1 = 1.0;
float f2 = 2.0f;
float f3 = f1 - f2; // f3 = 1.0 - 2.0 = -1.0
f3 = f1 * f2;         // f3 = 1.0 * 2.0 = 2.0
```




```
f3 = f1/f2;        // f3 = 1.0/2.0 = 0.5
f3 = f2/f1;        // f3 = 2.0/1.0 = 2.0
```



<span data-ttu-id="7a2f9-146">O operador de módulo retorna o restante de uma divisão.</span><span class="sxs-lookup"><span data-stu-id="7a2f9-146">The modulus operator returns the remainder of a division.</span></span> <span data-ttu-id="7a2f9-147">Isso produz resultados diferentes ao usar inteiros e números de ponto flutuante.</span><span class="sxs-lookup"><span data-stu-id="7a2f9-147">This produces different results when using integers and floating-point numbers.</span></span> <span data-ttu-id="7a2f9-148">Os pendências inteiros que são fracionários serão truncados.</span><span class="sxs-lookup"><span data-stu-id="7a2f9-148">Integer remainders that are fractional will be truncated.</span></span>


```
int i1 = 1;
int i2 = 2;
i3 = i1 % i2;      // i3 = remainder of 1/2, which is 1
i3 = i2 % i1;      // i3 = remainder of 2/1, which is 0
i3 = 5 % 2;        // i3 = remainder of 5/2, which is 1
i3 = 9 % 2;        // i3 = remainder of 9/2, which is 1
```



<span data-ttu-id="7a2f9-149">O operador de módulo Trunca um resto fracionário ao usar números inteiros.</span><span class="sxs-lookup"><span data-stu-id="7a2f9-149">The modulus operator truncates a fractional remainder when using integers.</span></span>


```
f3 = f1 % f2;      // f3 = remainder of 1.0/2.0, which is 0.5
f3 = f2 % f1;      // f3 = remainder of 2.0/1.0, which is 0.0
```



<span data-ttu-id="7a2f9-150">O operador% é definido somente em casos em que ambos os lados são positivos ou ambos os lados são negativos.</span><span class="sxs-lookup"><span data-stu-id="7a2f9-150">The % operator is defined only in cases where either both sides are positive or both sides are negative.</span></span> <span data-ttu-id="7a2f9-151">Ao contrário de C, ele também opera em tipos de dados de ponto flutuante, bem como inteiros.</span><span class="sxs-lookup"><span data-stu-id="7a2f9-151">Unlike C, it also operates on floating-point data types, as well as integers.</span></span>

## <a name="array-operator"></a><span data-ttu-id="7a2f9-152">Operador de matriz</span><span class="sxs-lookup"><span data-stu-id="7a2f9-152">Array Operator</span></span>

<span data-ttu-id="7a2f9-153">O operador de seleção de membro da matriz " \[ i \] " seleciona um ou mais componentes em uma matriz.</span><span class="sxs-lookup"><span data-stu-id="7a2f9-153">The array member selection operator "\[i\]" selects one or more components in an array.</span></span> <span data-ttu-id="7a2f9-154">É um conjunto de colchetes que contêm um índice baseado em zero.</span><span class="sxs-lookup"><span data-stu-id="7a2f9-154">It is a set of square brackets that contain a zero-based index.</span></span>


```
int arrayOfInts[4] = { 0,1,2,3 };
arrayOfInts[0] = 2;
arrayOfInts[1] = arrayOfInts[0];
```



<span data-ttu-id="7a2f9-155">O operador de matriz também pode ser usado para acessar um vetor.</span><span class="sxs-lookup"><span data-stu-id="7a2f9-155">The array operator can also be used to access a vector.</span></span>


```
float4 4D_Vector = { 0.0f, 1.0f, 2.0f, 3.0f  };         
float 1DFloat = 4D_Vector[1];          // 1.0f
```



<span data-ttu-id="7a2f9-156">Ao adicionar um índice adicional, o operador de matriz também pode acessar uma matriz.</span><span class="sxs-lookup"><span data-stu-id="7a2f9-156">By adding an additional index, the array operator can also access a matrix.</span></span>


```
float4x4 mat4x4 = {{0,0,0,0}, {1,1,1,1}, {2,2,2,2}, {3,3,3,3} };
mat4x4[0][1] = 1.1f;
float 1DFloat = mat4x4[0][1];      // 0.0f
```



<span data-ttu-id="7a2f9-157">O primeiro índice é o índice de linha com base em zero.</span><span class="sxs-lookup"><span data-stu-id="7a2f9-157">The first index is the zero-based row index.</span></span> <span data-ttu-id="7a2f9-158">O segundo índice é o índice de coluna com base em zero.</span><span class="sxs-lookup"><span data-stu-id="7a2f9-158">The second index is the zero-based column index.</span></span>

## <a name="assignment-operators"></a><span data-ttu-id="7a2f9-159">Operadores de atribuição</span><span class="sxs-lookup"><span data-stu-id="7a2f9-159">Assignment Operators</span></span>

<span data-ttu-id="7a2f9-160">Os operadores de atribuição são: =, + =,-=, \* =,/=</span><span class="sxs-lookup"><span data-stu-id="7a2f9-160">The assignment operators are: =, +=, -=, \*=, /=</span></span>

<span data-ttu-id="7a2f9-161">Variáveis podem receber valores literais:</span><span class="sxs-lookup"><span data-stu-id="7a2f9-161">Variables can be assigned literal values:</span></span>


```
int i = 1;            
float f2 = 3.1f; 
bool b = false;
string str = "string";
```



<span data-ttu-id="7a2f9-162">As variáveis também podem ser atribuídas ao resultado de uma operação matemática:</span><span class="sxs-lookup"><span data-stu-id="7a2f9-162">Variables can also be assigned the result of a mathematical operation:</span></span>


```
int i1 = 1;
i1 += 2;           // i1 = 1 + 2 = 3
```



<span data-ttu-id="7a2f9-163">Uma variável pode ser usada em qualquer um dos lados do sinal de igual:</span><span class="sxs-lookup"><span data-stu-id="7a2f9-163">A variable can be used on either side of the equals sign:</span></span>


```
float f3 = 0.5f;
f3 *= f3;          // f3 = 0.5 * 0.5 = 0.25
```



<span data-ttu-id="7a2f9-164">A divisão para variáveis de ponto flutuante é como esperado porque as pendências decimais não são um problema.</span><span class="sxs-lookup"><span data-stu-id="7a2f9-164">Division for floating-point variables is as expected because decimal remainders are not a problem.</span></span>


```
float f1 = 1.0;
f1 /= 3.0f;        // f1 = 1.0/3.0 = 0.333
```



<span data-ttu-id="7a2f9-165">Tenha cuidado se você estiver usando inteiros que podem ser divididos, especialmente quando o truncamento afetar o resultado.</span><span class="sxs-lookup"><span data-stu-id="7a2f9-165">Be careful if you are using integers that may get divided, especially when truncation affects the result.</span></span> <span data-ttu-id="7a2f9-166">Este exemplo é idêntico ao exemplo anterior, exceto para o tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="7a2f9-166">This example is identical to the previous example, except for the data type.</span></span> <span data-ttu-id="7a2f9-167">O truncamento causa um resultado muito diferente.</span><span class="sxs-lookup"><span data-stu-id="7a2f9-167">The truncation causes a very different result.</span></span>


```
int i1 = 1;
i1 /= 3;           // i1 = 1/3 = 0.333, which gets truncated to 0
```



## <a name="binary-casts"></a><span data-ttu-id="7a2f9-168">Conversões binárias</span><span class="sxs-lookup"><span data-stu-id="7a2f9-168">Binary Casts</span></span>

<span data-ttu-id="7a2f9-169">A operação de conversão entre int e float converterá o valor numérico em representações apropriadas, seguindo as regras de C para truncar um tipo int.</span><span class="sxs-lookup"><span data-stu-id="7a2f9-169">Casting operation between int and float will convert the numeric value into the appropriate representations following C rules for truncating an int type.</span></span> <span data-ttu-id="7a2f9-170">Converter um valor de um float para um int e voltar para um float resultará em uma conversão com perdas com base na precisão do destino.</span><span class="sxs-lookup"><span data-stu-id="7a2f9-170">Casting a value from a float to an int and back to a float will result in a lossy conversion based on the precision of the target.</span></span>

<span data-ttu-id="7a2f9-171">As conversões binárias também podem ser executadas usando [**funções intrínsecas (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md), que reinterpreta a representação de bits de um número no tipo de dados de destino.</span><span class="sxs-lookup"><span data-stu-id="7a2f9-171">Binary casts may also be performed using [**Intrinsic Functions (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md), which reinterpret the bit representation of a number into the target data type.</span></span>


```
asfloat() // Cast to float
asint()   // Cast to int 
asuint()  // Cast to uint
```



## <a name="bitwise-operators"></a><span data-ttu-id="7a2f9-172">Operadores bit a bit</span><span class="sxs-lookup"><span data-stu-id="7a2f9-172">Bitwise Operators</span></span>

<span data-ttu-id="7a2f9-173">O HLSL dá suporte aos operadores bit a seguir, que seguem a mesma precedência de C com relação a outros operadores.</span><span class="sxs-lookup"><span data-stu-id="7a2f9-173">HLSL supports the following bitwise operators, which follow the same precedence as C with regard to other operators.</span></span> <span data-ttu-id="7a2f9-174">A tabela a seguir descreve os operadores.</span><span class="sxs-lookup"><span data-stu-id="7a2f9-174">The following table describes the operators.</span></span>

> [!Note]  
> <span data-ttu-id="7a2f9-175">Os operadores de bit a bit exigem o [modelo de sombreador 4 \_ 0](dx-graphics-hlsl-sm4.md) com hardware Direct3D 10 e superior.</span><span class="sxs-lookup"><span data-stu-id="7a2f9-175">Bitwise operators require [Shader Model 4\_0](dx-graphics-hlsl-sm4.md) with Direct3D 10 and higher hardware.</span></span>

 



|           |                   |
|-----------|-------------------|
| <span data-ttu-id="7a2f9-176">Operador</span><span class="sxs-lookup"><span data-stu-id="7a2f9-176">Operator</span></span>  | <span data-ttu-id="7a2f9-177">Função</span><span class="sxs-lookup"><span data-stu-id="7a2f9-177">Function</span></span>          |
| ~         | <span data-ttu-id="7a2f9-178">Não lógico</span><span class="sxs-lookup"><span data-stu-id="7a2f9-178">Logical Not</span></span>       |
| <<  | <span data-ttu-id="7a2f9-179">Deslocamento à esquerda</span><span class="sxs-lookup"><span data-stu-id="7a2f9-179">Left Shift</span></span>        |
| >>  | <span data-ttu-id="7a2f9-180">Deslocamento à direita</span><span class="sxs-lookup"><span data-stu-id="7a2f9-180">Right Shift</span></span>       |
| &         | <span data-ttu-id="7a2f9-181">And lógico</span><span class="sxs-lookup"><span data-stu-id="7a2f9-181">Logical And</span></span>       |
| \|        | <span data-ttu-id="7a2f9-182">Ou lógico</span><span class="sxs-lookup"><span data-stu-id="7a2f9-182">Logical Or</span></span>        |
| ^         | <span data-ttu-id="7a2f9-183">XOR lógico</span><span class="sxs-lookup"><span data-stu-id="7a2f9-183">Logical Xor</span></span>       |
| <<= | <span data-ttu-id="7a2f9-184">Deslocamento à esquerda igual</span><span class="sxs-lookup"><span data-stu-id="7a2f9-184">Left Shift Equal</span></span>  |
| >>= | <span data-ttu-id="7a2f9-185">Deslocamento à direita igual</span><span class="sxs-lookup"><span data-stu-id="7a2f9-185">Right Shift Equal</span></span> |
| &=        | <span data-ttu-id="7a2f9-186">E igual a</span><span class="sxs-lookup"><span data-stu-id="7a2f9-186">And Equal</span></span>         |
| \|=       | <span data-ttu-id="7a2f9-187">Ou igual a</span><span class="sxs-lookup"><span data-stu-id="7a2f9-187">Or Equal</span></span>          |
| ^=        | <span data-ttu-id="7a2f9-188">XOR igual</span><span class="sxs-lookup"><span data-stu-id="7a2f9-188">Xor Equal</span></span>         |



 

<span data-ttu-id="7a2f9-189">Os operadores bit a bit são definidos para operar somente em tipos de dados int e uint.</span><span class="sxs-lookup"><span data-stu-id="7a2f9-189">Bitwise operators are defined to operate only on int and uint data types.</span></span> <span data-ttu-id="7a2f9-190">A tentativa de usar operadores bit-a-ponto nos tipos de dados float ou struct resultará em um erro.</span><span class="sxs-lookup"><span data-stu-id="7a2f9-190">Attempting to use bitwise operators on float, or struct data types will result in an error.</span></span>

## <a name="boolean-math-operators"></a><span data-ttu-id="7a2f9-191">Operadores matemáticos boolianos</span><span class="sxs-lookup"><span data-stu-id="7a2f9-191">Boolean Math Operators</span></span>

<span data-ttu-id="7a2f9-192">Os operadores matemáticos boolianos são:  &&, \| \| ,?:</span><span class="sxs-lookup"><span data-stu-id="7a2f9-192">The Boolean math operators are: &&, \|\|, ?:</span></span>


```
bool b1 = true;
bool b2 = false;
bool b3 = b1 && b2 // b3 = true AND false = false
b3 = b1 || b2                // b3 = true OR false = true
```



<span data-ttu-id="7a2f9-193">Diferentemente da avaliação de curto-circuito de &&, \| \| e?: em C, as expressões HLSL nunca fazem um circuito curto de uma avaliação porque são operações de vetor.</span><span class="sxs-lookup"><span data-stu-id="7a2f9-193">Unlike short-circuit evaluation of &&, \|\|, and ?: in C, HLSL expressions never short-circuit an evaluation because they are vector operations.</span></span> <span data-ttu-id="7a2f9-194">Todos os lados da expressão são sempre avaliados.</span><span class="sxs-lookup"><span data-stu-id="7a2f9-194">All sides of the expression are always evaluated.</span></span>

<span data-ttu-id="7a2f9-195">Operadores boolianos funcionam em uma base por componente.</span><span class="sxs-lookup"><span data-stu-id="7a2f9-195">Boolean operators function on a per-component basis.</span></span> <span data-ttu-id="7a2f9-196">Isso significa que, se você comparar dois vetores, o resultado será um vetor que contém o resultado booliano da comparação para cada componente.</span><span class="sxs-lookup"><span data-stu-id="7a2f9-196">This means that if you compare two vectors, the result is a vector containing the Boolean result of the comparison for each component.</span></span>

<span data-ttu-id="7a2f9-197">Para expressões que usam operadores boolianos, o tamanho e o tipo de componente de cada variável são promovidos para serem os mesmos antes que a operação ocorra.</span><span class="sxs-lookup"><span data-stu-id="7a2f9-197">For expressions that use Boolean operators, the size and component type of each variable are promoted to be the same before the operation occurs.</span></span> <span data-ttu-id="7a2f9-198">O tipo promovido determina a resolução na qual a operação ocorre, bem como o tipo de resultado da expressão.</span><span class="sxs-lookup"><span data-stu-id="7a2f9-198">The promoted type determines the resolution at which the operation takes place, as well as the result type of the expression.</span></span> <span data-ttu-id="7a2f9-199">Por exemplo, uma expressão Int3 + float seria promovida para float3 + float3 para avaliação, e seu resultado seria do tipo float3.</span><span class="sxs-lookup"><span data-stu-id="7a2f9-199">For example an int3 + float expression would be promoted to float3 + float3 for evaluation, and its result would be of type float3.</span></span>

## <a name="cast-operator"></a><span data-ttu-id="7a2f9-200">Operador cast</span><span class="sxs-lookup"><span data-stu-id="7a2f9-200">Cast Operator</span></span>

<span data-ttu-id="7a2f9-201">Uma expressão precedida por um nome de tipo entre parênteses é uma conversão de tipo explícita.</span><span class="sxs-lookup"><span data-stu-id="7a2f9-201">An expression preceded by a type name in parenthesis is an explicit type cast.</span></span> <span data-ttu-id="7a2f9-202">Uma conversão de tipo converte a expressão original para o tipo de dados da conversão.</span><span class="sxs-lookup"><span data-stu-id="7a2f9-202">A type cast converts the original expression to the data type of the cast.</span></span> <span data-ttu-id="7a2f9-203">Em geral, os tipos de dados simples podem ser convertidos para os tipos de dados mais complexos (com uma conversão de promoção), mas apenas alguns tipos de dados complexos podem ser convertidos em tipos de dados simples (com uma conversão de rebaixamento).</span><span class="sxs-lookup"><span data-stu-id="7a2f9-203">In general, the simple data types can be cast to the more complex data types (with a promotion cast), but only some complex data types can be cast into simple data types (with a demotion cast).</span></span>

<span data-ttu-id="7a2f9-204">Somente a conversão de tipo de lado direito é legal.</span><span class="sxs-lookup"><span data-stu-id="7a2f9-204">Only right hand side type casting is legal.</span></span> <span data-ttu-id="7a2f9-205">Por exemplo, expressões como `(int)myFloat = myInt;` são ilegais.</span><span class="sxs-lookup"><span data-stu-id="7a2f9-205">For example, expressions such as `(int)myFloat = myInt;` are illegal.</span></span> <span data-ttu-id="7a2f9-206">Use `myFloat = (float)myInt;` em vez disso.</span><span class="sxs-lookup"><span data-stu-id="7a2f9-206">Use `myFloat = (float)myInt;` instead.</span></span>

<span data-ttu-id="7a2f9-207">O compilador também executa a conversão implícita de tipo.</span><span class="sxs-lookup"><span data-stu-id="7a2f9-207">The compiler also performs implicit type cast.</span></span> <span data-ttu-id="7a2f9-208">Por exemplo, as duas expressões a seguir são equivalentes:</span><span class="sxs-lookup"><span data-stu-id="7a2f9-208">For example, the following two expressions are equivalent:</span></span>


```
int2 b = int2(1,2) + 2;
int2 b = int2(1,2) + int2(2,2);
```



## <a name="comma-operator"></a><span data-ttu-id="7a2f9-209">Operador de vírgula</span><span class="sxs-lookup"><span data-stu-id="7a2f9-209">Comma Operator</span></span>

<span data-ttu-id="7a2f9-210">O operador de vírgula (,) separa uma ou mais expressões que devem ser avaliadas na ordem.</span><span class="sxs-lookup"><span data-stu-id="7a2f9-210">The comma operator (,) separates one or more expressions that are to be evaluated in order.</span></span> <span data-ttu-id="7a2f9-211">O valor da última expressão na sequência é usado como o valor da sequência.</span><span class="sxs-lookup"><span data-stu-id="7a2f9-211">The value of the last expression in the sequence is used as the value of the sequence.</span></span>

<span data-ttu-id="7a2f9-212">Aqui está um caso vale a pena chamar atenção para.</span><span class="sxs-lookup"><span data-stu-id="7a2f9-212">Here is one case worth calling attention to.</span></span> <span data-ttu-id="7a2f9-213">Se o tipo de Construtor for acidentalmente deixado do lado direito do sinal de igual, o lado direito agora conterá quatro expressões, separadas por três vírgulas.</span><span class="sxs-lookup"><span data-stu-id="7a2f9-213">If the constructor type is accidentally left off the right side of the equals sign, the right side now contains four expressions, separated by three commas.</span></span>


```
// Instead of using a constructor
float4 x = float4(0,0,0,1); 

// The type on the right side is accidentally left off
float4 x = (0,0,0,1); 
```



<span data-ttu-id="7a2f9-214">O operador de vírgulas avalia uma expressão da esquerda para a direita.</span><span class="sxs-lookup"><span data-stu-id="7a2f9-214">The comma operator evaluates an expression from left to right.</span></span> <span data-ttu-id="7a2f9-215">Isso reduz o lado direito para:</span><span class="sxs-lookup"><span data-stu-id="7a2f9-215">This reduces the right hand side to:</span></span>


```
float4 x = 1; 
```



<span data-ttu-id="7a2f9-216">O HLSL usa a promoção escalar nesse caso, portanto, o resultado é como se isso tivesse sido escrito da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="7a2f9-216">HLSL uses scalar promotion in this case, so the result is as if this were written as follows:</span></span>


```
float4 x = float4(1,1,1,1);
```



<span data-ttu-id="7a2f9-217">Nessa instância, deixar o tipo FLOAT4 do lado direito provavelmente é um erro informando que o compilador não consegue detectar porque esta é uma instrução válida.</span><span class="sxs-lookup"><span data-stu-id="7a2f9-217">In this instance, leaving off the float4 type from the right side is probably a mistake that the compiler is unable to detect because this is a valid statement.</span></span>

## <a name="comparison-operators"></a><span data-ttu-id="7a2f9-218">Operadores de comparação</span><span class="sxs-lookup"><span data-stu-id="7a2f9-218">Comparison Operators</span></span>

<span data-ttu-id="7a2f9-219">Os operadores de comparação são: <, >, = =,! =, <=, >=.</span><span class="sxs-lookup"><span data-stu-id="7a2f9-219">The comparison operators are: <, >, ==, !=, <=, >=.</span></span>

<span data-ttu-id="7a2f9-220">Compare valores que sejam maiores que (ou menores que) qualquer valor escalar:</span><span class="sxs-lookup"><span data-stu-id="7a2f9-220">Compare values that are greater than (or less than) any scalar value:</span></span>


```
if( dot(lightDirection, normalVector) > 0 )
   // Do something; the face is lit
```




```
if( dot(lightDirection, normalVector) < 0 )
   // Do nothing; the face is backwards
```



<span data-ttu-id="7a2f9-221">Ou compare valores iguais a (ou não iguais a) qualquer valor escalar:</span><span class="sxs-lookup"><span data-stu-id="7a2f9-221">Or, compare values equal to (or not equal to) any scalar value:</span></span>


```
if(color.a == 0)
   // Skip processing because the face is invisible

if(color.a != 0)
   // Blend two colors together using the alpha value
```



<span data-ttu-id="7a2f9-222">Ou combine e compare valores que sejam maiores ou iguais a (ou menores ou iguais a) qualquer valor escalar:</span><span class="sxs-lookup"><span data-stu-id="7a2f9-222">Or combine both and compare values that are greater than or equal to (or less than or equal to) any scalar value:</span></span>


```
if( position.z >= oldPosition.z )
   // Skip the new face because it is behind the existing face
```




```
if( currentValue <= someInitialCondition )
   // Reset the current value to its initial condition
```



<span data-ttu-id="7a2f9-223">Cada uma dessas comparações pode ser feita com qualquer tipo de dados escalar.</span><span class="sxs-lookup"><span data-stu-id="7a2f9-223">Each of these comparisons can be done with any scalar data type.</span></span>

<span data-ttu-id="7a2f9-224">Para usar operadores de comparação com tipos de vetor e matriz, use a função [**All**](dx-graphics-hlsl-all.md) ou [**qualquer**](dx-graphics-hlsl-any.md) intrínseca.</span><span class="sxs-lookup"><span data-stu-id="7a2f9-224">To use comparison operators with vector and matrix types, use the [**all**](dx-graphics-hlsl-all.md) or [**any**](dx-graphics-hlsl-any.md) intrinsic function.</span></span>

<span data-ttu-id="7a2f9-225">Essa operação falha porque a instrução If requer um bool único, mas recebe um bool4:</span><span class="sxs-lookup"><span data-stu-id="7a2f9-225">This operation fails because the if statement requires a single bool but receives a bool4:</span></span>


```
if (A4 < B4)
```



<span data-ttu-id="7a2f9-226">Essas operações têm sucesso:</span><span class="sxs-lookup"><span data-stu-id="7a2f9-226">These operations succeed:</span></span>


```
if ( any(A4 < B4) )
if ( all(A4 < B4) )
```



## <a name="prefix-or-postfix-operators"></a><span data-ttu-id="7a2f9-227">Operadores de prefixo ou sufixo</span><span class="sxs-lookup"><span data-stu-id="7a2f9-227">Prefix or Postfix Operators</span></span>

<span data-ttu-id="7a2f9-228">Os operadores de prefixo e sufixo são: + +,--.</span><span class="sxs-lookup"><span data-stu-id="7a2f9-228">The prefix and postfix operators are: ++, --.</span></span> <span data-ttu-id="7a2f9-229">Os operadores de prefixo alteram o conteúdo da variável antes que a expressão seja avaliada.</span><span class="sxs-lookup"><span data-stu-id="7a2f9-229">Prefix operators change the contents of the variable before the expression is evaluated.</span></span> <span data-ttu-id="7a2f9-230">Os operadores de sufixo alteram o conteúdo da variável depois que a expressão é avaliada.</span><span class="sxs-lookup"><span data-stu-id="7a2f9-230">Postfix operators change the contents of the variable after the expression is evaluated.</span></span>

<span data-ttu-id="7a2f9-231">Nesse caso, um loop usa o conteúdo de i para controlar a contagem de loops.</span><span class="sxs-lookup"><span data-stu-id="7a2f9-231">In this case, a loop uses the contents of i to keep track of the loop count.</span></span>


```
float4 arrayOfFloats[4] = { 1.0f, 2.0f, 3.0f, 4.4f };

for (int i = 0; i<4; )
{
    arrayOfFloats[i++] *= 2; 
}
```



<span data-ttu-id="7a2f9-232">Como o operador de incremento de sufixo (+ +) é usado, arrayOfFloats \[ i \] é multiplicado por 2 antes de ser incrementado.</span><span class="sxs-lookup"><span data-stu-id="7a2f9-232">Because the postfix increment operator (++) is used, arrayOfFloats\[i\] is multiplied by 2 before i is incremented.</span></span> <span data-ttu-id="7a2f9-233">Isso pode ser ligeiramente reorganizado para usar o operador de incremento de prefixo.</span><span class="sxs-lookup"><span data-stu-id="7a2f9-233">This could be slightly rearranged to use the prefix increment operator.</span></span> <span data-ttu-id="7a2f9-234">Esse é mais difícil de ler, embora ambos os exemplos sejam equivalentes.</span><span class="sxs-lookup"><span data-stu-id="7a2f9-234">This one is harder to read, although both examples are equivalent.</span></span>


```
float4 arrayOfFloats[4] = { 1.0f, 2.0f, 3.0f, 4.4f };

for (int i = 0; i<4; )
{
    arrayOfFloats[++i - 1] *= 2; 
}
```



<span data-ttu-id="7a2f9-235">Como o operador de prefixo (+ +) é usado, arrayOfFloats \[ i + 1-1 \] é multiplicado por 2 depois de incrementado.</span><span class="sxs-lookup"><span data-stu-id="7a2f9-235">Because the prefix operator (++) is used, arrayOfFloats\[i+1 - 1\] is multiplied by 2 after i is incremented.</span></span>

<span data-ttu-id="7a2f9-236">O prefixo decremento e o operador decremento de sufixo (--) são aplicados na mesma sequência que o operador de incremento.</span><span class="sxs-lookup"><span data-stu-id="7a2f9-236">The prefix decrement and postfix decrement operator (--) are applied in the same sequence as the increment operator.</span></span> <span data-ttu-id="7a2f9-237">A diferença é que decrementa subtrai 1 em vez de adicionar 1.</span><span class="sxs-lookup"><span data-stu-id="7a2f9-237">The difference is that decrement subtracts 1 instead of adding 1.</span></span>

## <a name="structure-operator"></a><span data-ttu-id="7a2f9-238">Operador de estrutura</span><span class="sxs-lookup"><span data-stu-id="7a2f9-238">Structure Operator</span></span>

<span data-ttu-id="7a2f9-239">O operador de seleção de membro de estrutura (.) é um ponto.</span><span class="sxs-lookup"><span data-stu-id="7a2f9-239">The structure member selection operator (.) is a period.</span></span> <span data-ttu-id="7a2f9-240">Dada esta estrutura:</span><span class="sxs-lookup"><span data-stu-id="7a2f9-240">Given this structure:</span></span>


```
struct position
{
float4 x;
float4 y;
float4 z;
};
```



<span data-ttu-id="7a2f9-241">Ela pode ser lida da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="7a2f9-241">It can be read like this:</span></span>


```
struct position pos = { 1,2,3 };

float 1D_Float = pos.x
1D_Float = pos.y
```



<span data-ttu-id="7a2f9-242">Cada membro pode ser lido ou gravado com o operador de estrutura:</span><span class="sxs-lookup"><span data-stu-id="7a2f9-242">Each member can be read or written with the structure operator:</span></span>


```
struct position pos = { 1,2,3 };
pos.x = 2.0f;
pos.z = 1.0f;       // z = 1.0f
pos.z = pos.x      // z = 2.0f
```



## <a name="unary-operators"></a><span data-ttu-id="7a2f9-243">Operadores unários</span><span class="sxs-lookup"><span data-stu-id="7a2f9-243">Unary Operators</span></span>

<span data-ttu-id="7a2f9-244">Os operadores unários são:!,-, +</span><span class="sxs-lookup"><span data-stu-id="7a2f9-244">The unary operators are: !, -, +</span></span>

<span data-ttu-id="7a2f9-245">Operadores unários operam em um único operando.</span><span class="sxs-lookup"><span data-stu-id="7a2f9-245">Unary operators operate on a single operand.</span></span>


```
bool b = false;
bool b2 = !b;      // b2 = true
int i = 2;
int i2 = -i;       // i2 = -2
int j = +i2;       // j = +2
```



## <a name="operator-precedence"></a><span data-ttu-id="7a2f9-246">Precedência de operador</span><span class="sxs-lookup"><span data-stu-id="7a2f9-246">Operator Precedence</span></span>

<span data-ttu-id="7a2f9-247">Quando uma expressão contém mais de um operador, a precedência de operador determina a ordem de avaliação.</span><span class="sxs-lookup"><span data-stu-id="7a2f9-247">When an expression contains more than one operator, operator precedence determines the order of evaluation.</span></span> <span data-ttu-id="7a2f9-248">A precedência de operador para HLSL segue a mesma precedência de C.</span><span class="sxs-lookup"><span data-stu-id="7a2f9-248">Operator precedence for HLSL follows the same precedence as C.</span></span>

## <a name="remarks"></a><span data-ttu-id="7a2f9-249">Comentários</span><span class="sxs-lookup"><span data-stu-id="7a2f9-249">Remarks</span></span>

<span data-ttu-id="7a2f9-250">Chaves ( {,} ) iniciam e terminam um bloco de instruções.</span><span class="sxs-lookup"><span data-stu-id="7a2f9-250">Curly braces ({,}) start and end a statement block.</span></span> <span data-ttu-id="7a2f9-251">Quando um bloco de instrução usa uma única instrução, as chaves são opcionais.</span><span class="sxs-lookup"><span data-stu-id="7a2f9-251">When a statement block uses a single statement, the curly braces are optional.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7a2f9-252">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7a2f9-252">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7a2f9-253">Instruções (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7a2f9-253">Statements (DirectX HLSL)</span></span>](dx-graphics-hlsl-statements.md)
</dt> </dl>

 

 




