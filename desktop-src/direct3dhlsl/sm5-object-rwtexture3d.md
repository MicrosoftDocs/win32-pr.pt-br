---
title: RWTexture3D
description: Um recurso de leitura/gravação. | RWTexture3D
ms.assetid: 4d02810e-4f3c-4b20-b057-0ff27d6732b5
keywords:
- RWTexture3D HLSL
topic_type:
- apiref
api_name:
- RWTexture3D
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9b89ed7ff724eabef9fc2b2757c6ac0e5272c69e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104298183"
---
# <a name="rwtexture3d"></a><span data-ttu-id="a0c6a-105">RWTexture3D</span><span class="sxs-lookup"><span data-stu-id="a0c6a-105">RWTexture3D</span></span>

<span data-ttu-id="a0c6a-106">Um recurso de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="a0c6a-106">A read/write resource.</span></span>



| <span data-ttu-id="a0c6a-107">Método</span><span class="sxs-lookup"><span data-stu-id="a0c6a-107">Method</span></span>                                                        | <span data-ttu-id="a0c6a-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="a0c6a-108">Description</span></span>                   |
|---------------------------------------------------------------|-------------------------------|
| [<span data-ttu-id="a0c6a-109">**GetDimensions**</span><span class="sxs-lookup"><span data-stu-id="a0c6a-109">**GetDimensions**</span></span>](sm5-object-rwtexture3d-getdimensions.md) | <span data-ttu-id="a0c6a-110">Obtém as dimensões do recurso.</span><span class="sxs-lookup"><span data-stu-id="a0c6a-110">Gets the resource dimensions.</span></span> |
| [<span data-ttu-id="a0c6a-111">**Carregamento**</span><span class="sxs-lookup"><span data-stu-id="a0c6a-111">**Load**</span></span>](rwtexture3d-load.md)                              | <span data-ttu-id="a0c6a-112">Lê dados de textura.</span><span class="sxs-lookup"><span data-stu-id="a0c6a-112">Reads texture data.</span></span>           |
| <span data-ttu-id="a0c6a-113">[**Operador\[\]**](sm5-object-rwtexture3d-operatorindex.md)</span><span class="sxs-lookup"><span data-stu-id="a0c6a-113">[**Operator\[\]**](sm5-object-rwtexture3d-operatorindex.md)</span></span>  | <span data-ttu-id="a0c6a-114">Obtém uma variável de recurso.</span><span class="sxs-lookup"><span data-stu-id="a0c6a-114">Gets a resource variable.</span></span>     |



 

<span data-ttu-id="a0c6a-115">Você pode prefixar objetos **RWTexture3D** com a classe de armazenamento **globallycoherent**.</span><span class="sxs-lookup"><span data-stu-id="a0c6a-115">You can prefix **RWTexture3D** objects with the storage class **globallycoherent**.</span></span> <span data-ttu-id="a0c6a-116">Essa classe de armazenamento causa barreiras de memória e sincronizações para liberar dados em toda a GPU, de modo que outros grupos possam ver gravações.</span><span class="sxs-lookup"><span data-stu-id="a0c6a-116">This storage class causes memory barriers and syncs to flush data across the entire GPU such that other groups can see writes.</span></span> <span data-ttu-id="a0c6a-117">Sem esse especificador, uma barreira de memória ou sincronização liberará um UAV somente dentro do grupo atual.</span><span class="sxs-lookup"><span data-stu-id="a0c6a-117">Without this specifier, a memory barrier or sync will flush a UAV only within the current group.</span></span>

<span data-ttu-id="a0c6a-118">Um objeto **RWTexture3D** requer um tipo de elemento em uma instrução de declaração para o objeto.</span><span class="sxs-lookup"><span data-stu-id="a0c6a-118">A **RWTexture3D** object requires an element type in a declaration statement for the object.</span></span> <span data-ttu-id="a0c6a-119">Por exemplo, a seguinte declaração está correta:</span><span class="sxs-lookup"><span data-stu-id="a0c6a-119">For example, the following declaration is correct:</span></span>


```
RWTexture3D<float> tex;
```



<span data-ttu-id="a0c6a-120">Como um objeto **RWTexture3D** é um objeto de tipo UAV, suas propriedades diferem de um objeto de tipo SRV (modo de exibição de recursos do sombreador), como um objeto [**Texture3D**](sm5-object-texture3d.md) .</span><span class="sxs-lookup"><span data-stu-id="a0c6a-120">Because a **RWTexture3D** object is a UAV-type object, its properties differ from a shader resource view (SRV)-type object, such as a [**Texture3D**](sm5-object-texture3d.md) object.</span></span> <span data-ttu-id="a0c6a-121">Por exemplo, você pode ler e gravar em um objeto **RWTexture3D** , mas só pode ler de um objeto **Texture3D** .</span><span class="sxs-lookup"><span data-stu-id="a0c6a-121">For example, you can read from and write to a **RWTexture3D** object, but you can only read from a **Texture3D** object.</span></span>

<span data-ttu-id="a0c6a-122">Um objeto **RWTexture3D** não pode usar métodos de um objeto [**Texture3D**](sm5-object-texture3d.md) , como [Sample](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="a0c6a-122">A **RWTexture3D** object cannot use methods from a [**Texture3D**](sm5-object-texture3d.md) object, such as [Sample](dx-graphics-hlsl-to-sample.md).</span></span> <span data-ttu-id="a0c6a-123">No entanto, como você pode criar vários tipos de exibição para o mesmo recurso, você pode declarar vários tipos de textura como uma única textura em vários sombreadores.</span><span class="sxs-lookup"><span data-stu-id="a0c6a-123">However, because you can create multiple view types to the same resource, you can declare multiple texture types as a single texture in multiple shaders.</span></span> <span data-ttu-id="a0c6a-124">Por exemplo, você pode declarar e usar um objeto **RWTexture3D** como *Tex* em um sombreador de computação e, em seguida, declarar e usar um objeto **Texture3D** como *Tex* em um sombreador de pixel.</span><span class="sxs-lookup"><span data-stu-id="a0c6a-124">For example, you can declare and use a **RWTexture3D** object as *tex* in a compute shader and then declare and use a **Texture3D** object as *tex* in a pixel shader.</span></span>

> [!Note]  
> <span data-ttu-id="a0c6a-125">O tempo de execução impõe determinados padrões de uso quando você cria vários tipos de exibição para o mesmo recurso.</span><span class="sxs-lookup"><span data-stu-id="a0c6a-125">The runtime enforces certain usage patterns when you create multiple view types to the same resource.</span></span> <span data-ttu-id="a0c6a-126">Por exemplo, o tempo de execução não permite que você tenha um mapeamento UAV para um recurso e mapeamento SRV para o mesmo recurso ativo ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="a0c6a-126">For example, the runtime does not allow you to have both a UAV mapping for a resource and SRV mapping for the same resource active at the same time.</span></span>

 

## <a name="minimum-shader-model"></a><span data-ttu-id="a0c6a-127">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="a0c6a-127">Minimum Shader Model</span></span>

<span data-ttu-id="a0c6a-128">Esse objeto tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="a0c6a-128">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="a0c6a-129">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="a0c6a-129">Shader Model</span></span>                                                                | <span data-ttu-id="a0c6a-130">Com suporte</span><span class="sxs-lookup"><span data-stu-id="a0c6a-130">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="a0c6a-131">[Modelo](d3d11-graphics-reference-sm5.md) de sombreador 5 e modelos de sombreador mais altos</span><span class="sxs-lookup"><span data-stu-id="a0c6a-131">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="a0c6a-132">sim</span><span class="sxs-lookup"><span data-stu-id="a0c6a-132">yes</span></span>       |



 

<span data-ttu-id="a0c6a-133">Este objeto tem suporte para os seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="a0c6a-133">This object is supported for the following types of shaders:</span></span>



| <span data-ttu-id="a0c6a-134">Vértice</span><span class="sxs-lookup"><span data-stu-id="a0c6a-134">Vertex</span></span> | <span data-ttu-id="a0c6a-135">Envoltória</span><span class="sxs-lookup"><span data-stu-id="a0c6a-135">Hull</span></span> | <span data-ttu-id="a0c6a-136">Domínio</span><span class="sxs-lookup"><span data-stu-id="a0c6a-136">Domain</span></span> | <span data-ttu-id="a0c6a-137">Geometria</span><span class="sxs-lookup"><span data-stu-id="a0c6a-137">Geometry</span></span> | <span data-ttu-id="a0c6a-138">16x16</span><span class="sxs-lookup"><span data-stu-id="a0c6a-138">Pixel</span></span> | <span data-ttu-id="a0c6a-139">Computação</span><span class="sxs-lookup"><span data-stu-id="a0c6a-139">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="a0c6a-140">x</span><span class="sxs-lookup"><span data-stu-id="a0c6a-140">x</span></span>     | <span data-ttu-id="a0c6a-141">x</span><span class="sxs-lookup"><span data-stu-id="a0c6a-141">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="a0c6a-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="a0c6a-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0c6a-143">Objetos do Shader Model 5</span><span class="sxs-lookup"><span data-stu-id="a0c6a-143">Shader Model 5 Objects</span></span>](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 




