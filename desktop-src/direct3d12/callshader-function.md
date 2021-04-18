---
description: Invoca outro sombreador de dentro de um sombreador.
ms.assetid: ''
title: Função CallShader
ms.date: 05/31/2018
ms.localizationpriority: low
ms.topic: reference
topic_type:
- APIRef
- kbSyntax
api_name:
- CallShader
api_type:
- NA
ms.openlocfilehash: 8c5cdf4e0a71430d6375fd75ca553f92ca9539b9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105812091"
---
# <a name="callshader-function"></a><span data-ttu-id="6391a-103">Função CallShader</span><span class="sxs-lookup"><span data-stu-id="6391a-103">CallShader function</span></span>

<span data-ttu-id="6391a-104">Invoca outro sombreador de dentro de um sombreador.</span><span class="sxs-lookup"><span data-stu-id="6391a-104">Invokes another shader from within a shader.</span></span>

## <a name="syntax"></a><span data-ttu-id="6391a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6391a-105">Syntax</span></span>
<span data-ttu-id="6391a-106">Essa definição de função intrínseca é equivalente ao seguinte modelo de função:</span><span class="sxs-lookup"><span data-stu-id="6391a-106">This intrinsic function definition is equivalent to the following function template:</span></span>

```
template<param_t>
void CallShader(uint ShaderIndex, inout param_t Parameter);
```



## <a name="parameters"></a><span data-ttu-id="6391a-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6391a-107">Parameters</span></span>

`ShaderIndex`

<span data-ttu-id="6391a-108">Um inteiro sem sinal representando o índice na tabela de [sombreador callable](callable-shader.md) especificada na chamada para [**DispatchRays**] (/Windows/Desktop/API/d3d12/NF-d3d12-id3d12graphicscommandlist4-dispatchrays.</span><span class="sxs-lookup"><span data-stu-id="6391a-108">An unsigned integer representing the index into the [callable shader](callable-shader.md) table specified in the call to [**DispatchRays**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-dispatchrays.</span></span>

`Parameter`

<span data-ttu-id="6391a-109">Os parâmetros definidos pelo usuário a serem passados para o sombreador que possa ser chamado.</span><span class="sxs-lookup"><span data-stu-id="6391a-109">The user-defined parameters to pass to the callable shader.</span></span>  <span data-ttu-id="6391a-110">Essa estrutura de parâmetro deve corresponder à estrutura de parâmetro usada no sombreador callable apontado na tabela de sombreador.</span><span class="sxs-lookup"><span data-stu-id="6391a-110">This parameter structure must match the parameter structure used in the callable shader pointed to in the shader table.</span></span>


## <a name="return-value"></a><span data-ttu-id="6391a-111">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="6391a-111">Return Value</span></span>

<span data-ttu-id="6391a-112">**void**</span><span class="sxs-lookup"><span data-stu-id="6391a-112">**void**</span></span>

## <a name="remarks"></a><span data-ttu-id="6391a-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="6391a-113">Remarks</span></span>

<span data-ttu-id="6391a-114">Essa função pode ser chamada nos seguintes tipos de sombreador raytracing:</span><span class="sxs-lookup"><span data-stu-id="6391a-114">This function can be called from the following raytracing shader types:</span></span>

* [<span data-ttu-id="6391a-115">**Sombreador resgatável**</span><span class="sxs-lookup"><span data-stu-id="6391a-115">**Callable Shader**</span></span>](callable-shader.md)
* [<span data-ttu-id="6391a-116">**Sombreador do clique mais próximo**</span><span class="sxs-lookup"><span data-stu-id="6391a-116">**Closest Hit Shader**</span></span>](closest-hit-shader.md)
* [<span data-ttu-id="6391a-117">**Sombreador de resolução**</span><span class="sxs-lookup"><span data-stu-id="6391a-117">**Miss Shader**</span></span>](miss-shader.md)
* [<span data-ttu-id="6391a-118">**Sombreador da geração de raio**</span><span class="sxs-lookup"><span data-stu-id="6391a-118">**Ray Generation Shader**</span></span>](ray-generation-shader.md)



## <a name="see-also"></a><span data-ttu-id="6391a-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="6391a-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6391a-120">Referência HLSL de raytracing do Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="6391a-120">Direct3D 12 Raytracing HLSL Reference</span></span>](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




