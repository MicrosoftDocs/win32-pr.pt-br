---
title: RWTexture2D
description: Um recurso de leitura/gravação. | RWTexture2D
ms.assetid: 19b383f1-c787-4c20-b77a-60ef9f212b9f
keywords:
- RWTexture2D HLSL
topic_type:
- apiref
api_name:
- RWTexture2D
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ccdeae4dd47d3ad4bf5d756c2ca362033eae6814
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104298243"
---
# <a name="rwtexture2d"></a><span data-ttu-id="07ed9-105">RWTexture2D</span><span class="sxs-lookup"><span data-stu-id="07ed9-105">RWTexture2D</span></span>

<span data-ttu-id="07ed9-106">Um recurso de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="07ed9-106">A read/write resource.</span></span>



| <span data-ttu-id="07ed9-107">Método</span><span class="sxs-lookup"><span data-stu-id="07ed9-107">Method</span></span>                                                        | <span data-ttu-id="07ed9-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="07ed9-108">Description</span></span>                   |
|---------------------------------------------------------------|-------------------------------|
| [<span data-ttu-id="07ed9-109">**GetDimensions**</span><span class="sxs-lookup"><span data-stu-id="07ed9-109">**GetDimensions**</span></span>](sm5-object-rwtexture2d-getdimensions.md) | <span data-ttu-id="07ed9-110">Obtém as dimensões do recurso.</span><span class="sxs-lookup"><span data-stu-id="07ed9-110">Gets the resource dimensions.</span></span> |
| [<span data-ttu-id="07ed9-111">**Carregamento**</span><span class="sxs-lookup"><span data-stu-id="07ed9-111">**Load**</span></span>](rwtexture2d-load.md)                              | <span data-ttu-id="07ed9-112">Lê dados de textura.</span><span class="sxs-lookup"><span data-stu-id="07ed9-112">Reads texture data.</span></span>           |
| <span data-ttu-id="07ed9-113">[**Operador\[\]**](sm5-object-rwtexture2d-operatorindex.md)</span><span class="sxs-lookup"><span data-stu-id="07ed9-113">[**Operator\[\]**](sm5-object-rwtexture2d-operatorindex.md)</span></span>  | <span data-ttu-id="07ed9-114">Obtém uma variável de recurso.</span><span class="sxs-lookup"><span data-stu-id="07ed9-114">Gets a resource variable.</span></span>     |



 

<span data-ttu-id="07ed9-115">Você pode prefixar objetos RWTexture2D com a classe de armazenamento **globallycoherent**.</span><span class="sxs-lookup"><span data-stu-id="07ed9-115">You can prefix RWTexture2D objects with the storage class **globallycoherent**.</span></span> <span data-ttu-id="07ed9-116">Essa classe de armazenamento causa barreiras de memória e sincronizações para liberar dados em toda a GPU, de modo que outros grupos possam ver gravações.</span><span class="sxs-lookup"><span data-stu-id="07ed9-116">This storage class causes memory barriers and syncs to flush data across the entire GPU such that other groups can see writes.</span></span> <span data-ttu-id="07ed9-117">Sem esse especificador, uma barreira de memória ou sincronização liberará apenas um UAV (modo de exibição de acesso não ordenado) no grupo atual.</span><span class="sxs-lookup"><span data-stu-id="07ed9-117">Without this specifier, a memory barrier or sync will flush only an unordered access view (UAV) within the current group.</span></span>

<span data-ttu-id="07ed9-118">Um objeto RWTexture2D requer um tipo de elemento em uma instrução de declaração para o objeto.</span><span class="sxs-lookup"><span data-stu-id="07ed9-118">A RWTexture2D object requires an element type in a declaration statement for the object.</span></span> <span data-ttu-id="07ed9-119">Por exemplo, a declaração a seguir não está correta:</span><span class="sxs-lookup"><span data-stu-id="07ed9-119">For example, the following declaration is not correct:</span></span>


```
// The following declaration is incorrectly coded.
RWTexture2D myTexture;
```



<span data-ttu-id="07ed9-120">A seguinte declaração está correta:</span><span class="sxs-lookup"><span data-stu-id="07ed9-120">The following declaration is correct:</span></span>


```
// The following declaration is correctly coded.
RWTexture2D<float> tex;
```



<span data-ttu-id="07ed9-121">Como um objeto RWTexture2D é um objeto de tipo UAV, suas propriedades diferem de um objeto de tipo SRV (modo de exibição de recursos do sombreador), como um objeto [Texture2D](sm5-object-texture2d.md) .</span><span class="sxs-lookup"><span data-stu-id="07ed9-121">Because a RWTexture2D object is a UAV-type object, its properties differ from a shader resource view (SRV)-type object, such as a [Texture2D](sm5-object-texture2d.md) object.</span></span> <span data-ttu-id="07ed9-122">Por exemplo, você pode ler e gravar em um objeto RWTexture2D, mas só pode ler de um objeto Texture2D.</span><span class="sxs-lookup"><span data-stu-id="07ed9-122">For example, you can read from and write to a RWTexture2D object, but you can only read from a Texture2D object.</span></span>

<span data-ttu-id="07ed9-123">Um objeto RWTexture2D não pode usar métodos de um objeto [Texture2D](sm5-object-texture2d.md) , como [Sample](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="07ed9-123">A RWTexture2D object cannot use methods from a [Texture2D](sm5-object-texture2d.md) object, such as [Sample](dx-graphics-hlsl-to-sample.md).</span></span> <span data-ttu-id="07ed9-124">No entanto, como você pode criar vários tipos de exibição para o mesmo recurso, você pode declarar vários tipos de textura como uma única textura em vários sombreadores.</span><span class="sxs-lookup"><span data-stu-id="07ed9-124">However, because you can create multiple view types to the same resource, you can declare multiple texture types as a single texture in multiple shaders.</span></span> <span data-ttu-id="07ed9-125">Por exemplo, os trechos de código a seguir mostram como você pode declarar e usar um objeto RWTexture2D como *Tex* em um sombreador de computação e, em seguida, declarar e usar um objeto Texture2D como *Tex* em um sombreador de pixel.</span><span class="sxs-lookup"><span data-stu-id="07ed9-125">For example, the following code snippets show how you can declare and use a RWTexture2D object as *tex* in a compute shader and then declare and use a Texture2D object as *tex* in a pixel shader.</span></span>

> [!Note]  
> <span data-ttu-id="07ed9-126">O tempo de execução impõe determinados padrões de uso quando você cria vários tipos de exibição para o mesmo recurso.</span><span class="sxs-lookup"><span data-stu-id="07ed9-126">The runtime enforces certain usage patterns when you create multiple view types to the same resource.</span></span> <span data-ttu-id="07ed9-127">Por exemplo, o tempo de execução não permite que você tenha um mapeamento UAV para um recurso e mapeamento SRV para o mesmo recurso ativo ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="07ed9-127">For example, the runtime does not allow you to have both a UAV mapping for a resource and SRV mapping for the same resource active at the same time.</span></span>

 

<span data-ttu-id="07ed9-128">O código a seguir é para o sombreador de computação:</span><span class="sxs-lookup"><span data-stu-id="07ed9-128">The following code is for the compute shader:</span></span>


```
RWTexture2D<float> tex;
[numthreads(groupDim_x, groupDim_y, 1)]
void main(
    uint3 groupId : SV_GroupID,
    uint3 groupThreadId : SV_GroupThreadID,
    uint3 dispatchThreadId : SV_DispatchThreadID,
    uint groupIndex : SV_GroupIndex)
{
    tex [dispatchThreadId.xy] = <something>;
}
```



<span data-ttu-id="07ed9-129">O código a seguir é para o sombreador de pixel:</span><span class="sxs-lookup"><span data-stu-id="07ed9-129">The following code is for the pixel shader:</span></span>


```
struct PixelShaderInput
{
    float4 pos : SV_POSITION;
    float2 tex : TEXTURE;
};

Texture2D<float> tex;
float4 main(PixelShaderInput input) : SV_TARGET
{
    return tex.Sample(TextureSampler, input.tex);
}
```



## <a name="minimum-shader-model"></a><span data-ttu-id="07ed9-130">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="07ed9-130">Minimum Shader Model</span></span>

<span data-ttu-id="07ed9-131">Esse objeto tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="07ed9-131">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="07ed9-132">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="07ed9-132">Shader Model</span></span>                                                                | <span data-ttu-id="07ed9-133">Com suporte</span><span class="sxs-lookup"><span data-stu-id="07ed9-133">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="07ed9-134">[Modelo](d3d11-graphics-reference-sm5.md) de sombreador 5 e modelos de sombreador mais altos</span><span class="sxs-lookup"><span data-stu-id="07ed9-134">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="07ed9-135">sim</span><span class="sxs-lookup"><span data-stu-id="07ed9-135">yes</span></span>       |



 

<span data-ttu-id="07ed9-136">Este objeto tem suporte para os seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="07ed9-136">This object is supported for the following types of shaders:</span></span>



| <span data-ttu-id="07ed9-137">Vértice</span><span class="sxs-lookup"><span data-stu-id="07ed9-137">Vertex</span></span> | <span data-ttu-id="07ed9-138">Envoltória</span><span class="sxs-lookup"><span data-stu-id="07ed9-138">Hull</span></span> | <span data-ttu-id="07ed9-139">Domínio</span><span class="sxs-lookup"><span data-stu-id="07ed9-139">Domain</span></span> | <span data-ttu-id="07ed9-140">Geometria</span><span class="sxs-lookup"><span data-stu-id="07ed9-140">Geometry</span></span> | <span data-ttu-id="07ed9-141">16x16</span><span class="sxs-lookup"><span data-stu-id="07ed9-141">Pixel</span></span> | <span data-ttu-id="07ed9-142">Computação</span><span class="sxs-lookup"><span data-stu-id="07ed9-142">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="07ed9-143">x</span><span class="sxs-lookup"><span data-stu-id="07ed9-143">x</span></span>     | <span data-ttu-id="07ed9-144">x</span><span class="sxs-lookup"><span data-stu-id="07ed9-144">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="07ed9-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="07ed9-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07ed9-146">Objetos do Shader Model 5</span><span class="sxs-lookup"><span data-stu-id="07ed9-146">Shader Model 5 Objects</span></span>](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 




