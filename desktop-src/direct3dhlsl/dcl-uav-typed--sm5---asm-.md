---
title: dcl_uav_typed (SM5-ASM)
description: Declare um UAV (modo de exibição de acesso não ordenado) para uso por um sombreador. | dcl_uav_typed (SM5-ASM)
ms.assetid: F9F5583F-E3D0-447F-9227-BBB1B4E71934
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b789714c7ec825620b73e387fa8a4dd73e1a590d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104989252"
---
# <a name="dcl_uav_typed-sm5---asm"></a><span data-ttu-id="f52ef-104">DCL \_ UAV \_ tipado (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="f52ef-104">dcl\_uav\_typed (sm5 - asm)</span></span>

<span data-ttu-id="f52ef-105">Declare um UAV (modo de exibição de acesso não ordenado) para uso por um sombreador.</span><span class="sxs-lookup"><span data-stu-id="f52ef-105">Declare an unordered access view (UAV) for use by a shader.</span></span>



| <span data-ttu-id="f52ef-106">DCL \_ UAV \_ digitou \[ \_ GLC \] dstUAV, Dimension, Type</span><span class="sxs-lookup"><span data-stu-id="f52ef-106">dcl\_uav\_typed\[\_glc\] dstUAV, dimension, type</span></span> |
|--------------------------------------------------|



 



| <span data-ttu-id="f52ef-107">Item</span><span class="sxs-lookup"><span data-stu-id="f52ef-107">Item</span></span>                                                                                           | <span data-ttu-id="f52ef-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="f52ef-108">Description</span></span>                                                                                       |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f52ef-109"><span id="dstUAV"></span><span id="dstuav"></span><span id="DSTUAV"></span>*dstUAV*</span><span class="sxs-lookup"><span data-stu-id="f52ef-109"><span id="dstUAV"></span><span id="dstuav"></span><span id="DSTUAV"></span>*dstUAV*</span></span><br/> | <span data-ttu-id="f52ef-110">\[no \] UAV.</span><span class="sxs-lookup"><span data-stu-id="f52ef-110">\[in\] The UAV.</span></span><br/>                                                                        |
| <span data-ttu-id="f52ef-111"><span id="dimension"></span><span id="DIMENSION"></span>*dimensões*</span><span class="sxs-lookup"><span data-stu-id="f52ef-111"><span id="dimension"></span><span id="DIMENSION"></span>*dimension*</span></span><br/>                 | <span data-ttu-id="f52ef-112">\[em \] especifica quantas dimensões as instruções que acessam o UAV estão fornecendo.</span><span class="sxs-lookup"><span data-stu-id="f52ef-112">\[in\] Specifies how many dimensions the instructions accessing the UAV are providing.</span></span><br/> |
| <span data-ttu-id="f52ef-113"><span id="type"></span><span id="TYPE"></span>*Escreva*</span><span class="sxs-lookup"><span data-stu-id="f52ef-113"><span id="type"></span><span id="TYPE"></span>*type*</span></span><br/>                                | <span data-ttu-id="f52ef-114">\[no \] tipo de UAV.</span><span class="sxs-lookup"><span data-stu-id="f52ef-114">\[in\] The type of the UAV.</span></span><br/>                                                            |



 

## <a name="remarks"></a><span data-ttu-id="f52ef-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="f52ef-115">Remarks</span></span>

<span data-ttu-id="f52ef-116">*dstUAV* é um \# registro u sendo declarado como uma referência a um UnorderedAccessView que deve ser associado ao slot UAV \# na API.</span><span class="sxs-lookup"><span data-stu-id="f52ef-116">*dstUAV* is a u\# register being declared as a reference to an UnorderedAccessView that must be bound to UAV slot \# at the API.</span></span>

<span data-ttu-id="f52ef-117">A dimensão deve ser buffer, Texture1D, Texture1DArray, Texture2D, Texture2DArray ou Texture3D.</span><span class="sxs-lookup"><span data-stu-id="f52ef-117">The dimension must be buffer, Texture1D, Texture1DArray, Texture2D, Texture2DArray, or Texture3D.</span></span> <span data-ttu-id="f52ef-118">Isso indica quantas dimensões todas as instruções que acessam o UAV estão fornecendo: 1 (Texture1D, buffer), 2 (Texture1DArray, Texture2D) ou 3 (Texture2DArray, Texture3D).</span><span class="sxs-lookup"><span data-stu-id="f52ef-118">This indicates how many dimensions any instructions accessing the UAV are providing: 1 (Texture1D, Buffer), 2 (Texture1DArray, Texture2D) or 3 (Texture2DArray, Texture3D).</span></span>

<span data-ttu-id="f52ef-119">O tipo é {UNORM, SNORM, UINT, Santo, FLOAT}.</span><span class="sxs-lookup"><span data-stu-id="f52ef-119">Type is {UNORM,SNORM,UINT,SINT,FLOAT}.</span></span> <span data-ttu-id="f52ef-120">As operações feitas com o u declarado \# devem ser compatíveis com o tipo declarado aqui e o UAV associado ao slot \# também deve ter o mesmo tipo.</span><span class="sxs-lookup"><span data-stu-id="f52ef-120">Operations done with the declared u\# must be compatible with the type declared here, and the UAV bound to slot \# must also have the same type.</span></span>

<span data-ttu-id="f52ef-121">O \_ sinalizador GLC significa "globalmente coerente".</span><span class="sxs-lookup"><span data-stu-id="f52ef-121">The \_glc flag stands for "globally coherent".</span></span> <span data-ttu-id="f52ef-122">A ausência de \_ GLC significa que o UAV está sendo declarado somente como "grupo coerente" no sombreador de computação ou "coerente localmente" em uma invocação de sombreador de pixel único.</span><span class="sxs-lookup"><span data-stu-id="f52ef-122">The absence of \_glc means the UAV is being declared only as "group coherent" in the compute shader, or "locally coherent" in a single pixel shader invocation.</span></span>

<span data-ttu-id="f52ef-123">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="f52ef-123">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="f52ef-124">Vértice</span><span class="sxs-lookup"><span data-stu-id="f52ef-124">Vertex</span></span> | <span data-ttu-id="f52ef-125">Envoltória</span><span class="sxs-lookup"><span data-stu-id="f52ef-125">Hull</span></span> | <span data-ttu-id="f52ef-126">Domínio</span><span class="sxs-lookup"><span data-stu-id="f52ef-126">Domain</span></span> | <span data-ttu-id="f52ef-127">Geometria</span><span class="sxs-lookup"><span data-stu-id="f52ef-127">Geometry</span></span> | <span data-ttu-id="f52ef-128">16x16</span><span class="sxs-lookup"><span data-stu-id="f52ef-128">Pixel</span></span> | <span data-ttu-id="f52ef-129">Computação</span><span class="sxs-lookup"><span data-stu-id="f52ef-129">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="f52ef-130">X</span><span class="sxs-lookup"><span data-stu-id="f52ef-130">X</span></span>     | <span data-ttu-id="f52ef-131">X</span><span class="sxs-lookup"><span data-stu-id="f52ef-131">X</span></span>       |



 

<span data-ttu-id="f52ef-132">Como UAVs estão disponíveis em todos os estágios do sombreador para o Direct3D 11,1, essa instrução se aplica a todos os estágios do sombreador para o tempo de execução do Direct3D 11,1, que está disponível a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="f52ef-132">Because UAVs are available at all shader stages for Direct3D 11.1, this instruction applies to all shader stages for the Direct3D 11.1 runtime, which is available starting with Windows 8.</span></span>



| <span data-ttu-id="f52ef-133">Vértice</span><span class="sxs-lookup"><span data-stu-id="f52ef-133">Vertex</span></span> | <span data-ttu-id="f52ef-134">Envoltória</span><span class="sxs-lookup"><span data-stu-id="f52ef-134">Hull</span></span> | <span data-ttu-id="f52ef-135">Domínio</span><span class="sxs-lookup"><span data-stu-id="f52ef-135">Domain</span></span> | <span data-ttu-id="f52ef-136">Geometria</span><span class="sxs-lookup"><span data-stu-id="f52ef-136">Geometry</span></span> | <span data-ttu-id="f52ef-137">16x16</span><span class="sxs-lookup"><span data-stu-id="f52ef-137">Pixel</span></span> | <span data-ttu-id="f52ef-138">Computação</span><span class="sxs-lookup"><span data-stu-id="f52ef-138">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="f52ef-139">X</span><span class="sxs-lookup"><span data-stu-id="f52ef-139">X</span></span>      | <span data-ttu-id="f52ef-140">X</span><span class="sxs-lookup"><span data-stu-id="f52ef-140">X</span></span>    | <span data-ttu-id="f52ef-141">X</span><span class="sxs-lookup"><span data-stu-id="f52ef-141">X</span></span>      | <span data-ttu-id="f52ef-142">X</span><span class="sxs-lookup"><span data-stu-id="f52ef-142">X</span></span>        | <span data-ttu-id="f52ef-143">X</span><span class="sxs-lookup"><span data-stu-id="f52ef-143">X</span></span>     | <span data-ttu-id="f52ef-144">X</span><span class="sxs-lookup"><span data-stu-id="f52ef-144">X</span></span>       |



 

> [!Note]  
> <span data-ttu-id="f52ef-145">Não há suporte para essa instrução no sombreador de computação 4. x.</span><span class="sxs-lookup"><span data-stu-id="f52ef-145">This instruction is not supported in compute shader 4.x.</span></span>

 

## <a name="minimum-shader-model"></a><span data-ttu-id="f52ef-146">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="f52ef-146">Minimum Shader Model</span></span>

<span data-ttu-id="f52ef-147">Essa instrução tem suporte nos seguintes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="f52ef-147">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="f52ef-148">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="f52ef-148">Shader Model</span></span>                                              | <span data-ttu-id="f52ef-149">Com suporte</span><span class="sxs-lookup"><span data-stu-id="f52ef-149">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="f52ef-150">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="f52ef-150">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="f52ef-151">sim</span><span class="sxs-lookup"><span data-stu-id="f52ef-151">yes</span></span>       |
| [<span data-ttu-id="f52ef-152">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="f52ef-152">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="f52ef-153">não</span><span class="sxs-lookup"><span data-stu-id="f52ef-153">no</span></span>        |
| [<span data-ttu-id="f52ef-154">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="f52ef-154">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="f52ef-155">não</span><span class="sxs-lookup"><span data-stu-id="f52ef-155">no</span></span>        |
| [<span data-ttu-id="f52ef-156">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f52ef-156">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="f52ef-157">não</span><span class="sxs-lookup"><span data-stu-id="f52ef-157">no</span></span>        |
| [<span data-ttu-id="f52ef-158">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f52ef-158">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="f52ef-159">não</span><span class="sxs-lookup"><span data-stu-id="f52ef-159">no</span></span>        |
| [<span data-ttu-id="f52ef-160">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f52ef-160">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="f52ef-161">não</span><span class="sxs-lookup"><span data-stu-id="f52ef-161">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="f52ef-162">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f52ef-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f52ef-163">Assembly do Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f52ef-163">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





