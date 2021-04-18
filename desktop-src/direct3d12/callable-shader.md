---
description: Um sombreador que é invocado de outro sombreador com o intrínseco CallShader.
ms.assetid: ''
title: Sombreador resgatável
ms.date: 05/31/2018
ms.localizationpriority: low
ms.topic: reference
topic_type:
- APIRef
- kbSyntax
api_name:
- Callable Shader
api_type:
- NA
ms.openlocfilehash: 65df547c5e40a46cc4c35361b88ceb797c2e8852
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105795447"
---
# <a name="callable-shader"></a><span data-ttu-id="1834a-103">Sombreador resgatável</span><span class="sxs-lookup"><span data-stu-id="1834a-103">Callable Shader</span></span>

<span data-ttu-id="1834a-104">Um sombreador que é invocado de outro sombreador com o intrínseco [**CallShader**](callshader-function.md) .</span><span class="sxs-lookup"><span data-stu-id="1834a-104">A shader that is invoked from another shader with the [**CallShader**](callshader-function.md) intrinsic.</span></span>

<span data-ttu-id="1834a-105">Há uma estrutura de parâmetro fornecida no site de chamada **CallShader** que deve corresponder à estrutura de parâmetro usada no sombreador callable apontado pelo índice solicitado para a tabela de sombreador callable fornecida por meio do método [**DispatchRays**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-dispatchrays) .</span><span class="sxs-lookup"><span data-stu-id="1834a-105">There is a parameter structure supplied at the **CallShader** call site that must match the parameter structure used in the callable shader pointed to by the requested index into the callable shader table supplied through the [**DispatchRays**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-dispatchrays) method.</span></span>  <span data-ttu-id="1834a-106">O sombreador callable deve declarar esse parâmetro como *Inout*.</span><span class="sxs-lookup"><span data-stu-id="1834a-106">The callable shader must declare this parameter as *inout*.</span></span>  <span data-ttu-id="1834a-107">Além disso, o sombreador callable pode ler as entradas de índice e de dimensão de inicialização.</span><span class="sxs-lookup"><span data-stu-id="1834a-107">Additionally, the callable shader may read launch index and dimension inputs.</span></span> <span data-ttu-id="1834a-108">Para obter mais informações, consulte [**intrínsecos de valor do sistema**](direct3d-12-raytracing-hlsl-system-value-intrinsics.md).</span><span class="sxs-lookup"><span data-stu-id="1834a-108">For more information, see [**System Value Intrinsics**](direct3d-12-raytracing-hlsl-system-value-intrinsics.md).</span></span> 


## <a name="shader-type-attribute"></a><span data-ttu-id="1834a-109">Atributo de tipo de sombreador</span><span class="sxs-lookup"><span data-stu-id="1834a-109">Shader Type attribute</span></span>


```
[shader("callable")]
```



## <a name="example"></a><span data-ttu-id="1834a-110">Exemplo</span><span class="sxs-lookup"><span data-stu-id="1834a-110">Example</span></span>

```
[shader("callable")]
void callable_main(inout MyParams params)
{
    // Perform some common operations and update params
    CallShader( ... );  // maybe
}

```

 

 




