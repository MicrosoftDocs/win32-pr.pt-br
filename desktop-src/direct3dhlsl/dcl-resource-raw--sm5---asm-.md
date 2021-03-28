---
title: dcl_resource bruto (SM5-ASM)
description: Declare uma entrada de recurso de sombreador e atribua-a a um t \-um registro de espaço reservado para o recurso. | dcl_resource bruto (SM5-ASM)
ms.assetid: ECBA9DAB-F217-47FB-9588-F35866004E72
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8dd6ccc5990e34990772a072086d9e080cde67b4
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104172732"
---
# <a name="dcl_resource-raw-sm5---asm"></a><span data-ttu-id="544a1-104">\_recurso DCL bruto (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="544a1-104">dcl\_resource raw (sm5 - asm)</span></span>

<span data-ttu-id="544a1-105">Declare uma entrada de recurso de sombreador e atribua-a a um \# registro de espaço reservado t-a para o recurso.</span><span class="sxs-lookup"><span data-stu-id="544a1-105">Declare a shader resource input and assign it to a t\# - a placeholder register for the resource.</span></span>



| <span data-ttu-id="544a1-106">\_dstSRV de recursos \_ brutos de DCL</span><span class="sxs-lookup"><span data-stu-id="544a1-106">dcl\_resource\_raw dstSRV</span></span> |
|---------------------------|



 



| <span data-ttu-id="544a1-107">Item</span><span class="sxs-lookup"><span data-stu-id="544a1-107">Item</span></span>                                                                                           | <span data-ttu-id="544a1-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="544a1-108">Description</span></span>                                                                                       |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="544a1-109"><span id="dstSRV"></span><span id="dstsrv"></span><span id="DSTSRV"></span>*dstSRV*</span><span class="sxs-lookup"><span data-stu-id="544a1-109"><span id="dstSRV"></span><span id="dstsrv"></span><span id="DSTSRV"></span>*dstSRV*</span></span><br/> | <span data-ttu-id="544a1-110">\[em \] um \# registro t declarado como uma referência a um ShaderResourceView de um buffer bruto.</span><span class="sxs-lookup"><span data-stu-id="544a1-110">\[in\] A t\# register declared as a reference to a ShaderResourceView of a raw buffer.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="544a1-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="544a1-111">Remarks</span></span>

<span data-ttu-id="544a1-112">O conteúdo da estrutura não tem tipo; as operações executadas na memória podem interpretar implicitamente os dados como tendo um tipo.</span><span class="sxs-lookup"><span data-stu-id="544a1-112">The contents of the structure have no type; operations performed on the memory may implicitly interpret the data as having a type.</span></span>

<span data-ttu-id="544a1-113">Instruções que fazem referência a um t bruto \# usam um endereço 1D, um valor de 32 bits sem sinal especificando o deslocamento de byte para um local alinhado de 32 bits no buffer.</span><span class="sxs-lookup"><span data-stu-id="544a1-113">Instructions that reference a raw t\# take a 1D address, an unsigned 32-bit value specifying the byte offset to a 32-bit aligned location in the Buffer.</span></span> <span data-ttu-id="544a1-114">O endereço deve ser um múltiplo de 4 (bytes).</span><span class="sxs-lookup"><span data-stu-id="544a1-114">The address must be a multiple of 4 (bytes).</span></span>

<span data-ttu-id="544a1-115">Exibições associadas a t \# declaradas como RAW devem ter RAW especificado em sua criação; caso contrário, o comportamento quando acessado de um sombreador é indefinido.</span><span class="sxs-lookup"><span data-stu-id="544a1-115">Views bound to t\# declared as raw must have RAW specified on their creation; otherwise behavior when accessed from a shader is undefined.</span></span>

<span data-ttu-id="544a1-116">cs \_ 4 \_ 0 e cs \_ 4 \_ 1 dão suporte a essa instrução.</span><span class="sxs-lookup"><span data-stu-id="544a1-116">cs\_4\_0 and cs\_4\_1 support this instruction.</span></span>

<span data-ttu-id="544a1-117">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="544a1-117">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="544a1-118">Vértice</span><span class="sxs-lookup"><span data-stu-id="544a1-118">Vertex</span></span> | <span data-ttu-id="544a1-119">Envoltória</span><span class="sxs-lookup"><span data-stu-id="544a1-119">Hull</span></span> | <span data-ttu-id="544a1-120">Domínio</span><span class="sxs-lookup"><span data-stu-id="544a1-120">Domain</span></span> | <span data-ttu-id="544a1-121">Geometria</span><span class="sxs-lookup"><span data-stu-id="544a1-121">Geometry</span></span> | <span data-ttu-id="544a1-122">16x16</span><span class="sxs-lookup"><span data-stu-id="544a1-122">Pixel</span></span> | <span data-ttu-id="544a1-123">Computação</span><span class="sxs-lookup"><span data-stu-id="544a1-123">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="544a1-124">X</span><span class="sxs-lookup"><span data-stu-id="544a1-124">X</span></span>      | <span data-ttu-id="544a1-125">X</span><span class="sxs-lookup"><span data-stu-id="544a1-125">X</span></span>    | <span data-ttu-id="544a1-126">X</span><span class="sxs-lookup"><span data-stu-id="544a1-126">X</span></span>      | <span data-ttu-id="544a1-127">X</span><span class="sxs-lookup"><span data-stu-id="544a1-127">X</span></span>        | <span data-ttu-id="544a1-128">X</span><span class="sxs-lookup"><span data-stu-id="544a1-128">X</span></span>     | <span data-ttu-id="544a1-129">X</span><span class="sxs-lookup"><span data-stu-id="544a1-129">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="544a1-130">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="544a1-130">Minimum Shader Model</span></span>

<span data-ttu-id="544a1-131">Essa instrução tem suporte nos seguintes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="544a1-131">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="544a1-132">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="544a1-132">Shader Model</span></span>                                              | <span data-ttu-id="544a1-133">Com suporte</span><span class="sxs-lookup"><span data-stu-id="544a1-133">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="544a1-134">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="544a1-134">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="544a1-135">sim</span><span class="sxs-lookup"><span data-stu-id="544a1-135">yes</span></span>       |
| [<span data-ttu-id="544a1-136">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="544a1-136">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="544a1-137">não</span><span class="sxs-lookup"><span data-stu-id="544a1-137">no</span></span>        |
| [<span data-ttu-id="544a1-138">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="544a1-138">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="544a1-139">não</span><span class="sxs-lookup"><span data-stu-id="544a1-139">no</span></span>        |
| [<span data-ttu-id="544a1-140">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="544a1-140">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="544a1-141">não</span><span class="sxs-lookup"><span data-stu-id="544a1-141">no</span></span>        |
| [<span data-ttu-id="544a1-142">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="544a1-142">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="544a1-143">não</span><span class="sxs-lookup"><span data-stu-id="544a1-143">no</span></span>        |
| [<span data-ttu-id="544a1-144">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="544a1-144">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="544a1-145">não</span><span class="sxs-lookup"><span data-stu-id="544a1-145">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="544a1-146">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="544a1-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="544a1-147">Assembly do Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="544a1-147">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





