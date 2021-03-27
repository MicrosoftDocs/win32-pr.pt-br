---
title: StructuredBuffer
description: Um buffer somente leitura, que pode usar um tipo T que é uma estrutura.
ms.assetid: fe2ec0b8-0e19-42b6-9dad-c992ecdeb19e
keywords:
- StructuredBuffer HLSL
topic_type:
- apiref
api_name:
- StructuredBuffer
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 524078780ac28d691c4999491bed146a04d34439
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104988665"
---
# <a name="structuredbuffer"></a><span data-ttu-id="9ef86-104">StructuredBuffer</span><span class="sxs-lookup"><span data-stu-id="9ef86-104">StructuredBuffer</span></span>

<span data-ttu-id="9ef86-105">Um buffer somente leitura, que pode usar um tipo T que é uma estrutura.</span><span class="sxs-lookup"><span data-stu-id="9ef86-105">A read-only buffer, which can take a T type that is a structure.</span></span>



| <span data-ttu-id="9ef86-106">Método</span><span class="sxs-lookup"><span data-stu-id="9ef86-106">Method</span></span>                                                             | <span data-ttu-id="9ef86-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="9ef86-107">Description</span></span>                            |
|--------------------------------------------------------------------|----------------------------------------|
| [<span data-ttu-id="9ef86-108">**GetDimensions**</span><span class="sxs-lookup"><span data-stu-id="9ef86-108">**GetDimensions**</span></span>](sm5-object-structuredbuffer-getdimensions.md) | <span data-ttu-id="9ef86-109">Obtém as dimensões do recurso.</span><span class="sxs-lookup"><span data-stu-id="9ef86-109">Gets the resource dimensions.</span></span>          |
| [<span data-ttu-id="9ef86-110">**Carregamento**</span><span class="sxs-lookup"><span data-stu-id="9ef86-110">**Load**</span></span>](structuredbuffer-load.md)                              | <span data-ttu-id="9ef86-111">Lê dados de buffer.</span><span class="sxs-lookup"><span data-stu-id="9ef86-111">Reads buffer data.</span></span>                     |
| <span data-ttu-id="9ef86-112">[**Operador\[\]**](sm5-object-structuredbuffer-operatorindex.md)</span><span class="sxs-lookup"><span data-stu-id="9ef86-112">[**Operator\[\]**](sm5-object-structuredbuffer-operatorindex.md)</span></span>  | <span data-ttu-id="9ef86-113">Retorna uma variável de recurso somente leitura.</span><span class="sxs-lookup"><span data-stu-id="9ef86-113">Returns a read-only resource variable.</span></span> |



 

<span data-ttu-id="9ef86-114">O formato UAV associado a esse recurso precisa ser criado com o formato \_ desconhecido de formato dxgi \_ .</span><span class="sxs-lookup"><span data-stu-id="9ef86-114">The UAV format bound to this resource needs to be created with the DXGI\_FORMAT\_UNKNOWN format.</span></span>

<span data-ttu-id="9ef86-115">Para saber mais sobre [buffers estruturados](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources), consulte o material de visão geral.</span><span class="sxs-lookup"><span data-stu-id="9ef86-115">To find out more about [structured buffers](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources), see the overview material.</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="9ef86-116">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="9ef86-116">Minimum Shader Model</span></span>

<span data-ttu-id="9ef86-117">Esse objeto tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="9ef86-117">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="9ef86-118">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="9ef86-118">Shader Model</span></span>                                                                                                                                                                                                            | <span data-ttu-id="9ef86-119">Com suporte</span><span class="sxs-lookup"><span data-stu-id="9ef86-119">Supported</span></span> |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="9ef86-120">O [Shader Model 5](d3d11-graphics-reference-sm5.md) e os modelos de sombreador superior modelo de sombreador [4](dx-graphics-hlsl-sm4.md) (disponível para sombreadores de computação e pixel no Direct3D 11 em alguns dispositivos Direct3D 10).</span><span class="sxs-lookup"><span data-stu-id="9ef86-120">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models [Shader Model 4](dx-graphics-hlsl-sm4.md) (Available for compute and pixel shaders in Direct3D 11 on some Direct3D 10 devices.)</span></span><br/> | <span data-ttu-id="9ef86-121">sim</span><span class="sxs-lookup"><span data-stu-id="9ef86-121">yes</span></span>       |



 

<span data-ttu-id="9ef86-122">Esse objeto tem suporte para os seguintes tipos de sombreadores.</span><span class="sxs-lookup"><span data-stu-id="9ef86-122">This object is supported for the following types of shaders.</span></span>



| <span data-ttu-id="9ef86-123">Vértice</span><span class="sxs-lookup"><span data-stu-id="9ef86-123">Vertex</span></span> | <span data-ttu-id="9ef86-124">Envoltória</span><span class="sxs-lookup"><span data-stu-id="9ef86-124">Hull</span></span> | <span data-ttu-id="9ef86-125">Domínio</span><span class="sxs-lookup"><span data-stu-id="9ef86-125">Domain</span></span> | <span data-ttu-id="9ef86-126">Geometria</span><span class="sxs-lookup"><span data-stu-id="9ef86-126">Geometry</span></span> | <span data-ttu-id="9ef86-127">16x16</span><span class="sxs-lookup"><span data-stu-id="9ef86-127">Pixel</span></span> | <span data-ttu-id="9ef86-128">Computação</span><span class="sxs-lookup"><span data-stu-id="9ef86-128">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="9ef86-129">x</span><span class="sxs-lookup"><span data-stu-id="9ef86-129">x</span></span>      | <span data-ttu-id="9ef86-130">x</span><span class="sxs-lookup"><span data-stu-id="9ef86-130">x</span></span>    | <span data-ttu-id="9ef86-131">x</span><span class="sxs-lookup"><span data-stu-id="9ef86-131">x</span></span>      | <span data-ttu-id="9ef86-132">x</span><span class="sxs-lookup"><span data-stu-id="9ef86-132">x</span></span>        | <span data-ttu-id="9ef86-133">x</span><span class="sxs-lookup"><span data-stu-id="9ef86-133">x</span></span>     | <span data-ttu-id="9ef86-134">x</span><span class="sxs-lookup"><span data-stu-id="9ef86-134">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="9ef86-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="9ef86-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ef86-136">Objetos do Shader Model 5</span><span class="sxs-lookup"><span data-stu-id="9ef86-136">Shader Model 5 Objects</span></span>](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

