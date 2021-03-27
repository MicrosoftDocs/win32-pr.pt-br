---
title: Tipos de escalares
description: Tipos de escalares
ms.assetid: bf24d27f-2720-4268-bc74-fc46afedb9aa
keywords:
- Tipos escalares HLSL
topic_type:
- apiref
api_name:
- Scalar Types
api_type:
- NA
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/29/2020
ms.openlocfilehash: 7198932c6edb91e6f797b232b6c980976f3696a7
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/10/2021
ms.locfileid: "103663954"
---
# <a name="scalar-types"></a><span data-ttu-id="2b4e3-104">Tipos de escalares</span><span class="sxs-lookup"><span data-stu-id="2b4e3-104">Scalar Types</span></span>


<span data-ttu-id="2b4e3-105">O HLSL dá suporte a vários tipos de dados escalares:</span><span class="sxs-lookup"><span data-stu-id="2b4e3-105">HLSL supports several scalar data types:</span></span>

-   <span data-ttu-id="2b4e3-106">**bool** -true ou false.</span><span class="sxs-lookup"><span data-stu-id="2b4e3-106">**bool** - true or false.</span></span>
-   <span data-ttu-id="2b4e3-107">inteiro com sinal **int** -32-bit.</span><span class="sxs-lookup"><span data-stu-id="2b4e3-107">**int** - 32-bit signed integer.</span></span>
-   <span data-ttu-id="2b4e3-108">**uint** -32-bit inteiro sem sinal.</span><span class="sxs-lookup"><span data-stu-id="2b4e3-108">**uint** - 32-bit unsigned integer.</span></span>
-   <span data-ttu-id="2b4e3-109">**DWORD** -32 bits inteiro sem sinal.</span><span class="sxs-lookup"><span data-stu-id="2b4e3-109">**dword** - 32-bit unsigned integer.</span></span>
-   <span data-ttu-id="2b4e3-110">valor de ponto flutuante de **metade** de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="2b4e3-110">**half** - 16-bit floating point value.</span></span> <span data-ttu-id="2b4e3-111">Esse tipo de dados é fornecido somente para compatibilidade de idioma.</span><span class="sxs-lookup"><span data-stu-id="2b4e3-111">This data type is provided only for language compatibility.</span></span> <span data-ttu-id="2b4e3-112">Os destinos do sombreador do Direct3D 10 mapeiam todos os tipos de dados em anel para tipos de dados float.</span><span class="sxs-lookup"><span data-stu-id="2b4e3-112">Direct3D 10 shader targets map all half data types to float data types.</span></span> <span data-ttu-id="2b4e3-113">Um tipo de metade de dados não pode ser usado em uma variável global uniforme (use o sinalizador/GEC se essa funcionalidade for desejada).</span><span class="sxs-lookup"><span data-stu-id="2b4e3-113">A half data type cannot be used on a uniform global variable (use the /Gec flag if this functionality is desired).</span></span>
-   <span data-ttu-id="2b4e3-114">**float** -valor de ponto flutuante de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="2b4e3-114">**float** - 32-bit floating point value.</span></span>
-   <span data-ttu-id="2b4e3-115">valor de ponto flutuante de 64 bits **duplo** .</span><span class="sxs-lookup"><span data-stu-id="2b4e3-115">**double** - 64-bit floating point value.</span></span> <span data-ttu-id="2b4e3-116">Você não pode usar valores de precisão dupla como entradas e saídas para um fluxo.</span><span class="sxs-lookup"><span data-stu-id="2b4e3-116">You cannot use double precision values as inputs and outputs for a stream.</span></span> <span data-ttu-id="2b4e3-117">Para passar valores de precisão dupla entre sombreadores, declare cada **duplo** como um par de tipos de dados **uint** .</span><span class="sxs-lookup"><span data-stu-id="2b4e3-117">To pass double precision values between shaders, declare each **double** as a pair of **uint** data types.</span></span> <span data-ttu-id="2b4e3-118">Em seguida, use a função [**asuint**](asuint.md) para empacotar cada **duplo** no par de s **uint** e a função [**AsDouble**](asdouble.md) para desempacotar o par de s **uint** no **Double**.</span><span class="sxs-lookup"><span data-stu-id="2b4e3-118">Then, use the [**asuint**](asuint.md) function to pack each **double** into the pair of **uint** s and the [**asdouble**](asdouble.md) function to unpack the pair of **uint** s back into the **double**.</span></span>

<span data-ttu-id="2b4e3-119">A partir do Windows 8 HLSL também dá suporte a tipos de dados escalares de precisão mínima.</span><span class="sxs-lookup"><span data-stu-id="2b4e3-119">Starting with Windows 8 HLSL also supports minimum precision scalar data types.</span></span> <span data-ttu-id="2b4e3-120">Os drivers gráficos podem implementar os tipos de dados escalares de precisão mínima usando qualquer precisão maior ou igual à precisão de bit especificada.</span><span class="sxs-lookup"><span data-stu-id="2b4e3-120">Graphics drivers can implement minimum precision scalar data types by using any precision greater than or equal to their specified bit precision.</span></span> <span data-ttu-id="2b4e3-121">Recomendamos não contar com o comportamento de fixação MSS ou encapsulamento que depende da precisão subjacente específica.</span><span class="sxs-lookup"><span data-stu-id="2b4e3-121">We recommend not to rely on clamping or wrapping behavior that depends on specific underlying precision.</span></span> <span data-ttu-id="2b4e3-122">Por exemplo, o driver de gráficos pode executar aritmética em um valor de **min16float** na precisão total de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="2b4e3-122">For example, the graphics driver might execute arithmetic on a **min16float** value at full 32-bit precision.</span></span>

-   <span data-ttu-id="2b4e3-123">**min16float** -valor de ponto flutuante de 16 bits mínimo.</span><span class="sxs-lookup"><span data-stu-id="2b4e3-123">**min16float** - minimum 16-bit floating point value.</span></span>
-   <span data-ttu-id="2b4e3-124">**min10float** -valor de ponto flutuante de 10 bits mínimo.</span><span class="sxs-lookup"><span data-stu-id="2b4e3-124">**min10float** - minimum 10-bit floating point value.</span></span>
-   <span data-ttu-id="2b4e3-125">**min16int** -inteiro com sinal de 16 bits mínimo.</span><span class="sxs-lookup"><span data-stu-id="2b4e3-125">**min16int** - minimum 16-bit signed integer.</span></span>
-   <span data-ttu-id="2b4e3-126">**min12int** -inteiro com sinal de 12 bits mínimo.</span><span class="sxs-lookup"><span data-stu-id="2b4e3-126">**min12int** - minimum 12-bit signed integer.</span></span>
-   <span data-ttu-id="2b4e3-127">**min16uint** -inteiro sem sinal de 16 bits mínimo.</span><span class="sxs-lookup"><span data-stu-id="2b4e3-127">**min16uint** - minimum 16-bit unsigned integer.</span></span>

<span data-ttu-id="2b4e3-128">Para obter mais informações sobre literais escalares, consulte [gramática](dx-graphics-hlsl-appendix-grammar.md).</span><span class="sxs-lookup"><span data-stu-id="2b4e3-128">For more information about scalar literals, see [Grammar](dx-graphics-hlsl-appendix-grammar.md).</span></span>



<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2b4e3-129">Diferenças entre o Direct3D 9 e o Direct3D 10:</span><span class="sxs-lookup"><span data-stu-id="2b4e3-129">Differences between Direct3D 9 and Direct3D 10:</span></span><br/> <span data-ttu-id="2b4e3-130">No Direct3D 10, os tipos a seguir são modificadores para o tipo float.</span><span class="sxs-lookup"><span data-stu-id="2b4e3-130">In Direct3D 10, the following types are modifiers to the float type.</span></span><br/>
<ul>
<li><span data-ttu-id="2b4e3-131"><strong>snorm float</strong> - IEEE 32-bit assinado – float normalizado no intervalo de 1 a 1, inclusive.</span><span class="sxs-lookup"><span data-stu-id="2b4e3-131"><strong>snorm float</strong> - IEEE 32-bit signed-normalized float in range -1 to 1 inclusive.</span></span></li>
<li><span data-ttu-id="2b4e3-132"><strong>unorm float</strong> - IEEE 32-bit não assinado – float normalizado no intervalo de 0 a 1, inclusive.</span><span class="sxs-lookup"><span data-stu-id="2b4e3-132"><strong>unorm float</strong> - IEEE 32-bit unsigned-normalized float in range 0 to 1 inclusive.</span></span></li>
</ul>
<span data-ttu-id="2b4e3-133">Por exemplo, aqui está uma declaração float-Variable assinada com 4 componentes.</span><span class="sxs-lookup"><span data-stu-id="2b4e3-133">For example, here is a 4-component signed-normalized float-variable declaration.</span></span><br/> <span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>snorm float4 fourComponentIEEEFloat;</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>



 

## <a name="string-type"></a><span data-ttu-id="2b4e3-134">Tipo de cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="2b4e3-134">String Type</span></span>

<span data-ttu-id="2b4e3-135">O HLSL também dá suporte a um tipo de **cadeia de caracteres** , que é uma cadeia de caracteres ASCII.</span><span class="sxs-lookup"><span data-stu-id="2b4e3-135">HLSL also supports a **string** type, which is an ASCII string.</span></span> <span data-ttu-id="2b4e3-136">Não há operações ou Estados que aceitem cadeias de caracteres, mas os efeitos podem consultar os parâmetros e as anotações da cadeia.</span><span class="sxs-lookup"><span data-stu-id="2b4e3-136">There are no operations or states that accept strings, but effects can query string parameters and annotations.</span></span>

## <a name="example"></a><span data-ttu-id="2b4e3-137">Exemplo</span><span class="sxs-lookup"><span data-stu-id="2b4e3-137">Example</span></span>

```c
// top-level variable
float globalShaderVariable; 

// top-level function
void function(
in float4 position: POSITION0 // top-level argument
              )
{
  float localShaderVariable; // local variable
  function2(...)
}

void function2()
{
  ...
}
```

## <a name="see-also"></a><span data-ttu-id="2b4e3-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="2b4e3-138">See also</span></span>



* [<span data-ttu-id="2b4e3-139">Declarando tipos escalares</span><span class="sxs-lookup"><span data-stu-id="2b4e3-139">Declaring Scalar Types</span></span>](./dx-graphics-hlsl-writing-shaders-9.md#declaring-shader-variables)
* [<span data-ttu-id="2b4e3-140">Tipos de dados (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2b4e3-140">Data Types (DirectX HLSL)</span></span>](dx-graphics-hlsl-data-types.md)