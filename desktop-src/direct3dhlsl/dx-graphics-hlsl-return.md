---
title: Instrução Return
description: Uma instrução de retorno sinaliza o fim de uma função.
ms.assetid: e6c097af-ba0b-4abc-8099-69882ced1e18
keywords:
- return Statement HLSL
topic_type:
- apiref
api_name:
- return Statement
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 876c69f3ecfcf1ee1c8391ccc503b2316056b37a
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119581"
---
# <a name="return-statement"></a><span data-ttu-id="8c697-104">Instrução Return</span><span class="sxs-lookup"><span data-stu-id="8c697-104">return Statement</span></span>

<span data-ttu-id="8c697-105">Uma instrução de retorno sinaliza o fim de uma função.</span><span class="sxs-lookup"><span data-stu-id="8c697-105">A return statement signals the end of a function.</span></span>

<span data-ttu-id="8c697-106">valor \[ de retorno \] ;</span><span class="sxs-lookup"><span data-stu-id="8c697-106">return \[value\];</span></span>



 

<span data-ttu-id="8c697-107">A instrução return mais simples retorna o controle da função para o programa de chamada; ele não retorna nenhum valor.</span><span class="sxs-lookup"><span data-stu-id="8c697-107">The simplest return statement returns control from the function to the calling program; it returns no value.</span></span>


```
void main()
{
    return ;
}
```



<span data-ttu-id="8c697-108">No entanto, uma instrução de retorno pode retornar um ou mais valores.</span><span class="sxs-lookup"><span data-stu-id="8c697-108">However, a return statement can return one or more values.</span></span> <span data-ttu-id="8c697-109">Este exemplo retorna um valor literal:</span><span class="sxs-lookup"><span data-stu-id="8c697-109">This example returns a literal value:</span></span>


```
float main( float input : COLOR0) : COLOR0
{
    return 0;
}
```



<span data-ttu-id="8c697-110">Este exemplo retorna o resultado escalar de uma expressão.</span><span class="sxs-lookup"><span data-stu-id="8c697-110">This example returns the scalar result of an expression.</span></span>


```
return  light.enabled = true ;
```



<span data-ttu-id="8c697-111">Este exemplo retorna um vetor de quatro componentes que é construído de uma variável local e um literal.</span><span class="sxs-lookup"><span data-stu-id="8c697-111">This example returns a four-component vector that is constructed from a local variable and a literal.</span></span>


```
return  float4(color.rgb, 1) ;
```



<span data-ttu-id="8c697-112">Este exemplo retorna um vetor de quatro componentes que é construído a partir do resultado retornado de uma função intrínseca, junto com valores literais.</span><span class="sxs-lookup"><span data-stu-id="8c697-112">This example returns a four-component vector that is constructed from the result that is returned from an intrinsic function, together with literal values.</span></span>


```
float4 func(float2 a: POSITION): COLOR
{
    return float4(sin(length(a) * 100.0) * 0.5 + 0.5, sin(a.y * 50.0), 0, 1);
}
```



<span data-ttu-id="8c697-113">Este exemplo retorna uma estrutura que contém um ou mais membros.</span><span class="sxs-lookup"><span data-stu-id="8c697-113">This example returns a structure that contains one or more members.</span></span>


```
float4x4 WorldViewProj;

struct VS_OUTPUT
{
    float4 Pos  : POSITION;
};

VS_OUTPUT VertexShader_Tutorial_1(float4 inPos : POSITION )
{
    VS_OUTPUT out;
    out.Pos = mul(inPos, WorldViewProj );
    return out;
};
```



## <a name="see-also"></a><span data-ttu-id="8c697-114">Confira também</span><span class="sxs-lookup"><span data-stu-id="8c697-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c697-115">Funções (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8c697-115">Functions (DirectX HLSL)</span></span>](dx-graphics-hlsl-functions.md)
</dt> </dl>

 

 




