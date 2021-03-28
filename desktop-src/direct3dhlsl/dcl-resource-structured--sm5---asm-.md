---
title: dcl_resource estruturado (SM5-ASM)
description: Declare uma entrada de recurso de sombreador e atribua-a a um t \-um registro de espaço reservado para o recurso. | dcl_resource estruturado (SM5-ASM)
ms.assetid: 87FC8A56-9DB2-424B-889C-2AB59885DA13
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ab993e0cb260529c3419210c33f5d735a625bce
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104172669"
---
# <a name="dcl_resource-structured-sm5---asm"></a><span data-ttu-id="4e956-104">\_recurso DCL estruturado (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="4e956-104">dcl\_resource structured (sm5 - asm)</span></span>

<span data-ttu-id="4e956-105">Declare uma entrada de recurso de sombreador e atribua-a a um \# registro de espaço reservado t-a para o recurso.</span><span class="sxs-lookup"><span data-stu-id="4e956-105">Declare a shader resource input and assign it to a t\# - a placeholder register for the resource.</span></span>



| <span data-ttu-id="4e956-106">\_recurso DCL \_ estruturado DstSRV, structByteStride</span><span class="sxs-lookup"><span data-stu-id="4e956-106">dcl\_resource\_structured dstSRV, structByteStride</span></span> |
|----------------------------------------------------|



 



| <span data-ttu-id="4e956-107">Item</span><span class="sxs-lookup"><span data-stu-id="4e956-107">Item</span></span>                                                                                                                                   | <span data-ttu-id="4e956-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="4e956-108">Description</span></span>                                                                                                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4e956-109"><span id="dstSRV"></span><span id="dstsrv"></span><span id="DSTSRV"></span>*dstSRV*</span><span class="sxs-lookup"><span data-stu-id="4e956-109"><span id="dstSRV"></span><span id="dstsrv"></span><span id="DSTSRV"></span>*dstSRV*</span></span><br/>                                         | <span data-ttu-id="4e956-110">\[em \] um \# registro t declarado como uma referência a um ShaderResourceView de um buffer estruturado com o stride especificado que deve ser associado ao slot SRV \# na API.</span><span class="sxs-lookup"><span data-stu-id="4e956-110">\[in\] A t\# register declared as a reference to a ShaderResourceView of a structured buffer with the specified stride that must be bound to SRV slot \# at the API.</span></span> <br/> |
| <span data-ttu-id="4e956-111"><span id="structByteStride"></span><span id="structbytestride"></span><span id="STRUCTBYTESTRIDE"></span>*structByteStride*</span><span class="sxs-lookup"><span data-stu-id="4e956-111"><span id="structByteStride"></span><span id="structbytestride"></span><span id="STRUCTBYTESTRIDE"></span>*structByteStride*</span></span><br/> | <span data-ttu-id="4e956-112">\[em \] um UINT que especifica o tamanho da estrutura em bytes no buffer que está sendo declarado.</span><span class="sxs-lookup"><span data-stu-id="4e956-112">\[in\] A uint that specifies the size of the structure in bytes in the buffer being declared.</span></span> <span data-ttu-id="4e956-113">Esse valor deve ser maior que zero.</span><span class="sxs-lookup"><span data-stu-id="4e956-113">This value must be greater than zero.</span></span><br/>                                   |



 

## <a name="remarks"></a><span data-ttu-id="4e956-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="4e956-114">Remarks</span></span>

<span data-ttu-id="4e956-115">O conteúdo da estrutura não tem tipo; as operações executadas na memória podem interpretar implicitamente os dados como tendo um tipo.</span><span class="sxs-lookup"><span data-stu-id="4e956-115">The contents of the structure have no type; operations performed on the memory may implicitly interpret the data as having a type.</span></span>

<span data-ttu-id="4e956-116">Instruções que fazem referência a um t estruturado \# usam um endereço 2D, em que o primeiro componente escolhe \[ struct \] e o segundo componente escolhe o \[ deslocamento dentro de struct, vários de 32 bits \] .</span><span class="sxs-lookup"><span data-stu-id="4e956-116">Instructions that reference a structured t\# take a 2D address, where the first component picks \[struct\], and the second component picks \[offset within struct, multiple of 32-bits\].</span></span>

<span data-ttu-id="4e956-117">cs \_ 4 \_ 0 e cs \_ 4 \_ 1 dão suporte a essa instrução.</span><span class="sxs-lookup"><span data-stu-id="4e956-117">cs\_4\_0 and cs\_4\_1 support this instruction.</span></span>

<span data-ttu-id="4e956-118">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="4e956-118">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="4e956-119">Vértice</span><span class="sxs-lookup"><span data-stu-id="4e956-119">Vertex</span></span> | <span data-ttu-id="4e956-120">Envoltória</span><span class="sxs-lookup"><span data-stu-id="4e956-120">Hull</span></span> | <span data-ttu-id="4e956-121">Domínio</span><span class="sxs-lookup"><span data-stu-id="4e956-121">Domain</span></span> | <span data-ttu-id="4e956-122">Geometria</span><span class="sxs-lookup"><span data-stu-id="4e956-122">Geometry</span></span> | <span data-ttu-id="4e956-123">16x16</span><span class="sxs-lookup"><span data-stu-id="4e956-123">Pixel</span></span> | <span data-ttu-id="4e956-124">Computação</span><span class="sxs-lookup"><span data-stu-id="4e956-124">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="4e956-125">X</span><span class="sxs-lookup"><span data-stu-id="4e956-125">X</span></span>      | <span data-ttu-id="4e956-126">X</span><span class="sxs-lookup"><span data-stu-id="4e956-126">X</span></span>    | <span data-ttu-id="4e956-127">X</span><span class="sxs-lookup"><span data-stu-id="4e956-127">X</span></span>      | <span data-ttu-id="4e956-128">X</span><span class="sxs-lookup"><span data-stu-id="4e956-128">X</span></span>        | <span data-ttu-id="4e956-129">X</span><span class="sxs-lookup"><span data-stu-id="4e956-129">X</span></span>     | <span data-ttu-id="4e956-130">X</span><span class="sxs-lookup"><span data-stu-id="4e956-130">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="4e956-131">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="4e956-131">Minimum Shader Model</span></span>

<span data-ttu-id="4e956-132">Essa instrução tem suporte nos seguintes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="4e956-132">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="4e956-133">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="4e956-133">Shader Model</span></span>                                              | <span data-ttu-id="4e956-134">Com suporte</span><span class="sxs-lookup"><span data-stu-id="4e956-134">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="4e956-135">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="4e956-135">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="4e956-136">sim</span><span class="sxs-lookup"><span data-stu-id="4e956-136">yes</span></span>       |
| [<span data-ttu-id="4e956-137">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="4e956-137">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="4e956-138">não</span><span class="sxs-lookup"><span data-stu-id="4e956-138">no</span></span>        |
| [<span data-ttu-id="4e956-139">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="4e956-139">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="4e956-140">não</span><span class="sxs-lookup"><span data-stu-id="4e956-140">no</span></span>        |
| [<span data-ttu-id="4e956-141">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4e956-141">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="4e956-142">não</span><span class="sxs-lookup"><span data-stu-id="4e956-142">no</span></span>        |
| [<span data-ttu-id="4e956-143">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4e956-143">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="4e956-144">não</span><span class="sxs-lookup"><span data-stu-id="4e956-144">no</span></span>        |
| [<span data-ttu-id="4e956-145">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4e956-145">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="4e956-146">não</span><span class="sxs-lookup"><span data-stu-id="4e956-146">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="4e956-147">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4e956-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4e956-148">Assembly do Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4e956-148">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





