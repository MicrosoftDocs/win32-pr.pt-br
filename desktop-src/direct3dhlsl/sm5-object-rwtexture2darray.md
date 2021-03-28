---
title: RWTexture2DArray
description: Um recurso de leitura/gravação. | RWTexture2DArray
ms.assetid: 6a6f3655-f1c0-4d5b-91a2-d79da65858b8
keywords:
- RWTexture2DArray HLSL
topic_type:
- apiref
api_name:
- RWTexture2DArray
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5ada0fcaba729eff37f41f1ae7666841175689ff
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104968393"
---
# <a name="rwtexture2darray"></a><span data-ttu-id="8ca1b-105">RWTexture2DArray</span><span class="sxs-lookup"><span data-stu-id="8ca1b-105">RWTexture2DArray</span></span>

<span data-ttu-id="8ca1b-106">Um recurso de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="8ca1b-106">A read/write resource.</span></span>



| <span data-ttu-id="8ca1b-107">Método</span><span class="sxs-lookup"><span data-stu-id="8ca1b-107">Method</span></span>                                                             | <span data-ttu-id="8ca1b-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="8ca1b-108">Description</span></span>                   |
|--------------------------------------------------------------------|-------------------------------|
| [<span data-ttu-id="8ca1b-109">**GetDimensions**</span><span class="sxs-lookup"><span data-stu-id="8ca1b-109">**GetDimensions**</span></span>](sm5-object-rwtexture2darray-getdimensions.md) | <span data-ttu-id="8ca1b-110">Obtém as dimensões do recurso.</span><span class="sxs-lookup"><span data-stu-id="8ca1b-110">Gets the resource dimensions.</span></span> |
| [<span data-ttu-id="8ca1b-111">**Carregamento**</span><span class="sxs-lookup"><span data-stu-id="8ca1b-111">**Load**</span></span>](rwtexture2darray-load.md)                              | <span data-ttu-id="8ca1b-112">Lê dados de textura.</span><span class="sxs-lookup"><span data-stu-id="8ca1b-112">Reads texture data.</span></span>           |
| <span data-ttu-id="8ca1b-113">[**Operador\[\]**](sm5-object-rwtexture2darray-operatorindex.md)</span><span class="sxs-lookup"><span data-stu-id="8ca1b-113">[**Operator\[\]**](sm5-object-rwtexture2darray-operatorindex.md)</span></span>  | <span data-ttu-id="8ca1b-114">Obtém uma variável de recurso.</span><span class="sxs-lookup"><span data-stu-id="8ca1b-114">Gets a resource variable.</span></span>     |



 

<span data-ttu-id="8ca1b-115">Você pode prefixar objetos **RWTexture2DArray** com a classe de armazenamento **globallycoherent**.</span><span class="sxs-lookup"><span data-stu-id="8ca1b-115">You can prefix **RWTexture2DArray** objects with the storage class **globallycoherent**.</span></span> <span data-ttu-id="8ca1b-116">Essa classe de armazenamento causa barreiras de memória e sincronizações para liberar dados em toda a GPU, de modo que outros grupos possam ver gravações.</span><span class="sxs-lookup"><span data-stu-id="8ca1b-116">This storage class causes memory barriers and syncs to flush data across the entire GPU such that other groups can see writes.</span></span> <span data-ttu-id="8ca1b-117">Sem esse especificador, uma barreira de memória ou sincronização liberará um UAV somente dentro do grupo atual.</span><span class="sxs-lookup"><span data-stu-id="8ca1b-117">Without this specifier, a memory barrier or sync will flush a UAV only within the current group.</span></span>

<span data-ttu-id="8ca1b-118">Um objeto **RWTexture2DArray** requer um tipo de elemento em uma instrução de declaração para o objeto.</span><span class="sxs-lookup"><span data-stu-id="8ca1b-118">A **RWTexture2DArray** object requires an element type in a declaration statement for the object.</span></span> <span data-ttu-id="8ca1b-119">Por exemplo, a seguinte declaração está correta:</span><span class="sxs-lookup"><span data-stu-id="8ca1b-119">For example, the following declaration is correct:</span></span>


```
RWTexture2DArray<float> tex;
```



<span data-ttu-id="8ca1b-120">Como um objeto **RWTexture2DArray** é um objeto de tipo UAV, suas propriedades diferem de um objeto de tipo SRV (modo de exibição de recursos do sombreador), como um objeto [**Texture2DArray**](sm5-object-texture2darray.md) .</span><span class="sxs-lookup"><span data-stu-id="8ca1b-120">Because a **RWTexture2DArray** object is a UAV-type object, its properties differ from a shader resource view (SRV)-type object, such as a [**Texture2DArray**](sm5-object-texture2darray.md) object.</span></span> <span data-ttu-id="8ca1b-121">Por exemplo, você pode ler e gravar em um objeto **RWTexture2DArray** , mas só pode ler de um objeto **Texture2DArray** .</span><span class="sxs-lookup"><span data-stu-id="8ca1b-121">For example, you can read from and write to a **RWTexture2DArray** object, but you can only read from a **Texture2DArray** object.</span></span>

<span data-ttu-id="8ca1b-122">Um objeto **RWTexture2DArray** não pode usar métodos de um objeto [**Texture2DArray**](sm5-object-texture2darray.md) , como [Sample](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="8ca1b-122">A **RWTexture2DArray** object cannot use methods from a [**Texture2DArray**](sm5-object-texture2darray.md) object, such as [Sample](dx-graphics-hlsl-to-sample.md).</span></span> <span data-ttu-id="8ca1b-123">No entanto, como você pode criar vários tipos de exibição para o mesmo recurso, você pode declarar vários tipos de textura como uma única textura em vários sombreadores.</span><span class="sxs-lookup"><span data-stu-id="8ca1b-123">However, because you can create multiple view types to the same resource, you can declare multiple texture types as a single texture in multiple shaders.</span></span> <span data-ttu-id="8ca1b-124">Por exemplo, você pode declarar e usar um objeto **RWTexture2DArray** como *Tex* em um sombreador de computação e, em seguida, declarar e usar um objeto **Texture2DArray** como *Tex* em um sombreador de pixel.</span><span class="sxs-lookup"><span data-stu-id="8ca1b-124">For example, you can declare and use a **RWTexture2DArray** object as *tex* in a compute shader and then declare and use a **Texture2DArray** object as *tex* in a pixel shader.</span></span>

> [!Note]  
> <span data-ttu-id="8ca1b-125">O tempo de execução impõe determinados padrões de uso quando você cria vários tipos de exibição para o mesmo recurso.</span><span class="sxs-lookup"><span data-stu-id="8ca1b-125">The runtime enforces certain usage patterns when you create multiple view types to the same resource.</span></span> <span data-ttu-id="8ca1b-126">Por exemplo, o tempo de execução não permite que você tenha um mapeamento UAV para um recurso e mapeamento SRV para o mesmo recurso ativo ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="8ca1b-126">For example, the runtime does not allow you to have both a UAV mapping for a resource and SRV mapping for the same resource active at the same time.</span></span>

 

## <a name="minimum-shader-model"></a><span data-ttu-id="8ca1b-127">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="8ca1b-127">Minimum Shader Model</span></span>

<span data-ttu-id="8ca1b-128">Esse objeto tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="8ca1b-128">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="8ca1b-129">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="8ca1b-129">Shader Model</span></span>                                                                | <span data-ttu-id="8ca1b-130">Com suporte</span><span class="sxs-lookup"><span data-stu-id="8ca1b-130">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="8ca1b-131">[Modelo](d3d11-graphics-reference-sm5.md) de sombreador 5 e modelos de sombreador mais altos</span><span class="sxs-lookup"><span data-stu-id="8ca1b-131">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="8ca1b-132">sim</span><span class="sxs-lookup"><span data-stu-id="8ca1b-132">yes</span></span>       |



 

<span data-ttu-id="8ca1b-133">Este objeto tem suporte para os seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="8ca1b-133">This object is supported for the following types of shaders:</span></span>



| <span data-ttu-id="8ca1b-134">Vértice</span><span class="sxs-lookup"><span data-stu-id="8ca1b-134">Vertex</span></span> | <span data-ttu-id="8ca1b-135">Envoltória</span><span class="sxs-lookup"><span data-stu-id="8ca1b-135">Hull</span></span> | <span data-ttu-id="8ca1b-136">Domínio</span><span class="sxs-lookup"><span data-stu-id="8ca1b-136">Domain</span></span> | <span data-ttu-id="8ca1b-137">Geometria</span><span class="sxs-lookup"><span data-stu-id="8ca1b-137">Geometry</span></span> | <span data-ttu-id="8ca1b-138">16x16</span><span class="sxs-lookup"><span data-stu-id="8ca1b-138">Pixel</span></span> | <span data-ttu-id="8ca1b-139">Computação</span><span class="sxs-lookup"><span data-stu-id="8ca1b-139">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="8ca1b-140">x</span><span class="sxs-lookup"><span data-stu-id="8ca1b-140">x</span></span>     | <span data-ttu-id="8ca1b-141">x</span><span class="sxs-lookup"><span data-stu-id="8ca1b-141">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="8ca1b-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="8ca1b-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ca1b-143">Objetos do Shader Model 5</span><span class="sxs-lookup"><span data-stu-id="8ca1b-143">Shader Model 5 Objects</span></span>](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 




