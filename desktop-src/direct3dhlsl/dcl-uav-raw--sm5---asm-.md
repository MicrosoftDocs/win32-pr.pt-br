---
title: dcl_uav_raw (SM5-ASM)
description: Declare um UAV (modo de exibição de acesso não ordenado) para uso por um sombreador. | dcl_uav_raw (SM5-ASM)
ms.assetid: D0F43FF8-FF1C-4E42-AF42-F528C98FD680
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f47614d5a9327f2d686a36db6bfe4afeb653788
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104989176"
---
# <a name="dcl_uav_raw-sm5---asm"></a><span data-ttu-id="a2480-104">DCL \_ UAV \_ bruto (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="a2480-104">dcl\_uav\_raw (sm5 - asm)</span></span>

<span data-ttu-id="a2480-105">Declare um UAV (modo de exibição de acesso não ordenado) para uso por um sombreador.</span><span class="sxs-lookup"><span data-stu-id="a2480-105">Declare an unordered access view (UAV) for use by a shader.</span></span>



| <span data-ttu-id="a2480-106">DCL \_ UAV \_ RAW \[ \_ GLC \] dstUAV</span><span class="sxs-lookup"><span data-stu-id="a2480-106">dcl\_uav\_raw\[\_glc\] dstUAV</span></span> |
|-------------------------------|



 



| <span data-ttu-id="a2480-107">Item</span><span class="sxs-lookup"><span data-stu-id="a2480-107">Item</span></span>                                                                                           | <span data-ttu-id="a2480-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="a2480-108">Description</span></span>                |
|------------------------------------------------------------------------------------------------|----------------------------|
| <span data-ttu-id="a2480-109"><span id="dstUAV"></span><span id="dstuav"></span><span id="DSTUAV"></span>*dstUAV*</span><span class="sxs-lookup"><span data-stu-id="a2480-109"><span id="dstUAV"></span><span id="dstuav"></span><span id="DSTUAV"></span>*dstUAV*</span></span><br/> | <span data-ttu-id="a2480-110">\[no \] UAV.</span><span class="sxs-lookup"><span data-stu-id="a2480-110">\[in\] The UAV.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="a2480-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="a2480-111">Remarks</span></span>

<span data-ttu-id="a2480-112">*dstUAV* é um \# registro u declarado como uma referência a um UnorderedAccessView de um buffer, em que o buffer aparece como uma matriz 1D simples de entradas não tipadas de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="a2480-112">*dstUAV* is a u\# register declared as a reference to an UnorderedAccessView of a Buffer, where the buffer appears as a simple 1D array of 32-bit untyped entries.</span></span>

<span data-ttu-id="a2480-113">As operações executadas na memória podem interpretar implicitamente os dados como tendo um tipo.</span><span class="sxs-lookup"><span data-stu-id="a2480-113">Operations performed on the memory may implicitly interpret the data as having a type.</span></span>

<span data-ttu-id="a2480-114">O \_ sinalizador GLC significa "globalmente coerente".</span><span class="sxs-lookup"><span data-stu-id="a2480-114">The \_glc flag means "globally coherent".</span></span> <span data-ttu-id="a2480-115">A ausência de \_ GLC significa que o UAV está sendo declarado somente como "grupo coerente" no sombreador de computação ou "coerente localmente" em uma invocação de sombreador de pixel único.</span><span class="sxs-lookup"><span data-stu-id="a2480-115">The absence of \_glc means the UAV is being declared only as "group coherent" in the compute shader, or "locally coherent" in a single pixel shader invocation.</span></span>

<span data-ttu-id="a2480-116">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="a2480-116">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="a2480-117">Vértice</span><span class="sxs-lookup"><span data-stu-id="a2480-117">Vertex</span></span> | <span data-ttu-id="a2480-118">Envoltória</span><span class="sxs-lookup"><span data-stu-id="a2480-118">Hull</span></span> | <span data-ttu-id="a2480-119">Domínio</span><span class="sxs-lookup"><span data-stu-id="a2480-119">Domain</span></span> | <span data-ttu-id="a2480-120">Geometria</span><span class="sxs-lookup"><span data-stu-id="a2480-120">Geometry</span></span> | <span data-ttu-id="a2480-121">16x16</span><span class="sxs-lookup"><span data-stu-id="a2480-121">Pixel</span></span> | <span data-ttu-id="a2480-122">Computação</span><span class="sxs-lookup"><span data-stu-id="a2480-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="a2480-123">X</span><span class="sxs-lookup"><span data-stu-id="a2480-123">X</span></span>     | <span data-ttu-id="a2480-124">X</span><span class="sxs-lookup"><span data-stu-id="a2480-124">X</span></span>       |



 

<span data-ttu-id="a2480-125">Como UAVs estão disponíveis em todos os estágios do sombreador para o Direct3D 11,1, essa instrução se aplica a todos os estágios do sombreador para o tempo de execução do Direct3D 11,1, que está disponível a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="a2480-125">Because UAVs are available at all shader stages for Direct3D 11.1, this instruction applies to all shader stages for the Direct3D 11.1 runtime, which is available starting with Windows 8.</span></span>



| <span data-ttu-id="a2480-126">Vértice</span><span class="sxs-lookup"><span data-stu-id="a2480-126">Vertex</span></span> | <span data-ttu-id="a2480-127">Envoltória</span><span class="sxs-lookup"><span data-stu-id="a2480-127">Hull</span></span> | <span data-ttu-id="a2480-128">Domínio</span><span class="sxs-lookup"><span data-stu-id="a2480-128">Domain</span></span> | <span data-ttu-id="a2480-129">Geometria</span><span class="sxs-lookup"><span data-stu-id="a2480-129">Geometry</span></span> | <span data-ttu-id="a2480-130">16x16</span><span class="sxs-lookup"><span data-stu-id="a2480-130">Pixel</span></span> | <span data-ttu-id="a2480-131">Computação</span><span class="sxs-lookup"><span data-stu-id="a2480-131">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="a2480-132">X</span><span class="sxs-lookup"><span data-stu-id="a2480-132">X</span></span>      | <span data-ttu-id="a2480-133">X</span><span class="sxs-lookup"><span data-stu-id="a2480-133">X</span></span>    | <span data-ttu-id="a2480-134">X</span><span class="sxs-lookup"><span data-stu-id="a2480-134">X</span></span>      | <span data-ttu-id="a2480-135">X</span><span class="sxs-lookup"><span data-stu-id="a2480-135">X</span></span>        | <span data-ttu-id="a2480-136">X</span><span class="sxs-lookup"><span data-stu-id="a2480-136">X</span></span>     | <span data-ttu-id="a2480-137">X</span><span class="sxs-lookup"><span data-stu-id="a2480-137">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="a2480-138">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="a2480-138">Minimum Shader Model</span></span>

<span data-ttu-id="a2480-139">Essa instrução tem suporte nos seguintes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="a2480-139">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="a2480-140">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="a2480-140">Shader Model</span></span>                                              | <span data-ttu-id="a2480-141">Com suporte</span><span class="sxs-lookup"><span data-stu-id="a2480-141">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="a2480-142">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="a2480-142">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="a2480-143">sim</span><span class="sxs-lookup"><span data-stu-id="a2480-143">yes</span></span>       |
| [<span data-ttu-id="a2480-144">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="a2480-144">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="a2480-145">não</span><span class="sxs-lookup"><span data-stu-id="a2480-145">no</span></span>        |
| [<span data-ttu-id="a2480-146">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="a2480-146">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="a2480-147">não</span><span class="sxs-lookup"><span data-stu-id="a2480-147">no</span></span>        |
| [<span data-ttu-id="a2480-148">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a2480-148">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="a2480-149">não</span><span class="sxs-lookup"><span data-stu-id="a2480-149">no</span></span>        |
| [<span data-ttu-id="a2480-150">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a2480-150">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="a2480-151">não</span><span class="sxs-lookup"><span data-stu-id="a2480-151">no</span></span>        |
| [<span data-ttu-id="a2480-152">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a2480-152">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="a2480-153">não</span><span class="sxs-lookup"><span data-stu-id="a2480-153">no</span></span>        |



 

> [!Note]  
> <span data-ttu-id="a2480-154">Essa instrução tem suporte em cs \_ 4 \_ 0 e cs \_ 4 \_ 1.</span><span class="sxs-lookup"><span data-stu-id="a2480-154">This instruction is supported in cs\_4\_0 and cs\_4\_1.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="a2480-155">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a2480-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a2480-156">Assembly do Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a2480-156">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





