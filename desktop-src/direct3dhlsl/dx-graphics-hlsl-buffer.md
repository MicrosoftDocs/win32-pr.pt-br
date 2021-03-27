---
title: Tipo de buffer
description: Use a sintaxe a seguir para declarar uma variável de buffer.
ms.assetid: f21f0de5-58e3-466b-97bb-e4e7efa9cc1c
keywords:
- Tipo de buffer HLSL
topic_type:
- apiref
api_name:
- Buffer Type
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e36030f3dd31f1bdada238e89c1048e4971cd45c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007748"
---
# <a name="buffer-type"></a><span data-ttu-id="d8658-104">Tipo de buffer</span><span class="sxs-lookup"><span data-stu-id="d8658-104">Buffer Type</span></span>

<span data-ttu-id="d8658-105">Use a sintaxe a seguir para declarar uma variável de buffer.</span><span class="sxs-lookup"><span data-stu-id="d8658-105">Use the following syntax to declare a buffer variable.</span></span>



| <span data-ttu-id="d8658-106">Nome do *tipo* de<de buffer >  ;</span><span class="sxs-lookup"><span data-stu-id="d8658-106">Buffer<*Type*> *Name*;</span></span> |
|------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="d8658-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d8658-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d8658-108"><span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>**Completo**</span><span class="sxs-lookup"><span data-stu-id="d8658-108"><span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>**Buffer**</span></span>
</dt> <dd>

<span data-ttu-id="d8658-109">Palavra-chave required.</span><span class="sxs-lookup"><span data-stu-id="d8658-109">Required keyword.</span></span>

</dd> <dt>

<span data-ttu-id="d8658-110"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>*Escreva*</span><span class="sxs-lookup"><span data-stu-id="d8658-110"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>*Type*</span></span>
</dt> <dd>

<span data-ttu-id="d8658-111">Um dos tipos de HLSL [escalar](dx-graphics-hlsl-scalar.md), de [vetor](dx-graphics-hlsl-vector.md)e de [matriz](dx-graphics-hlsl-matrix.md) .</span><span class="sxs-lookup"><span data-stu-id="d8658-111">One of the [scalar](dx-graphics-hlsl-scalar.md), [vector](dx-graphics-hlsl-vector.md), and some [matrix](dx-graphics-hlsl-matrix.md) HLSL types.</span></span> <span data-ttu-id="d8658-112">Você pode declarar uma variável de buffer com uma matriz, desde que ela caiba em quantidades de 4 32 bits.</span><span class="sxs-lookup"><span data-stu-id="d8658-112">You can declare a buffer variable with a matrix as long as it fits in 4 32-bit quantities.</span></span> <span data-ttu-id="d8658-113">Portanto, você pode escrever `Buffer<float2x2>` .</span><span class="sxs-lookup"><span data-stu-id="d8658-113">So, you can write `Buffer<float2x2>`.</span></span> <span data-ttu-id="d8658-114">Mas `Buffer<float4x4>` é muito grande, e o compilador irá gerar um erro.</span><span class="sxs-lookup"><span data-stu-id="d8658-114">But `Buffer<float4x4>` is too large, and the compiler will generate an error.</span></span>

</dd> <dt>

<span data-ttu-id="d8658-115"><span id="Name"></span><span id="name"></span><span id="NAME"></span>*Nomes*</span><span class="sxs-lookup"><span data-stu-id="d8658-115"><span id="Name"></span><span id="name"></span><span id="NAME"></span>*Name*</span></span>
</dt> <dd>

<span data-ttu-id="d8658-116">Uma cadeia de caracteres ASCII que identifica exclusivamente o nome da variável.</span><span class="sxs-lookup"><span data-stu-id="d8658-116">An ASCII string that uniquely identifies the variable name.</span></span>

</dd> </dl>

## <a name="example"></a><span data-ttu-id="d8658-117">Exemplo</span><span class="sxs-lookup"><span data-stu-id="d8658-117">Example</span></span>

<span data-ttu-id="d8658-118">Aqui está um exemplo de uma declaração de buffer do arquivo PipesGS. FX no [exemplo PipesGS](https://msdn.microsoft.com/library/Ee416423(v=VS.85).aspx).</span><span class="sxs-lookup"><span data-stu-id="d8658-118">Here is an example of a buffer declaration from the PipesGS.fx file in [PipesGS Sample](https://msdn.microsoft.com/library/Ee416423(v=VS.85).aspx).</span></span>


```
Buffer<float4> g_Buffer;
```



<span data-ttu-id="d8658-119">Os dados são lidos de um buffer usando uma versão sobrecarregada da função intrínseca [**Load**](dx-graphics-hlsl-to-load.md) HLSL que usa um parâmetro de entrada (um índice de número inteiro).</span><span class="sxs-lookup"><span data-stu-id="d8658-119">Data is read from a buffer using an overloaded version of the [**Load**](dx-graphics-hlsl-to-load.md) HLSL intrinsic function that takes one input parameter (an integer index).</span></span> <span data-ttu-id="d8658-120">Um buffer é acessado como uma matriz de elementos; Portanto, este exemplo lê o segundo elemento.</span><span class="sxs-lookup"><span data-stu-id="d8658-120">A buffer is accessed like an array of elements; therefore, this example reads the second element.</span></span>


```
float4 bufferData = g_Buffer.Load( 1 );
```



<span data-ttu-id="d8658-121">Use o [estágio Stream-output](/windows/desktop/direct3d11/d3d10-graphics-programming-guide-output-stream-stage) para gerar dados de saída para um buffer.</span><span class="sxs-lookup"><span data-stu-id="d8658-121">Use the [stream-output stage](/windows/desktop/direct3d11/d3d10-graphics-programming-guide-output-stream-stage) to output data to a buffer.</span></span>

## <a name="see-also"></a><span data-ttu-id="d8658-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="d8658-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8658-123">Tipos de dados (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d8658-123">Data Types (DirectX HLSL)</span></span>](dx-graphics-hlsl-data-types.md)
</dt> </dl>

 

 