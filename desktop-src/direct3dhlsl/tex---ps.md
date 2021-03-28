---
title: Tex-PS
description: Carrega o registro de destino com dados de cor (RGBA) amostrados de uma textura. A textura deve estar associada a um estágio de textura específico (n) usando SetTexture. A amostragem de textura é controlada por setsamplestate.
ms.assetid: vs|directx_sdk|~\tex___ps.htm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a3070883b167d26cf31f7d7f388f6bd3736a4bde
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103917459"
---
# <a name="tex---ps"></a><span data-ttu-id="9b16e-105">Tex-PS</span><span class="sxs-lookup"><span data-stu-id="9b16e-105">tex - ps</span></span>

<span data-ttu-id="9b16e-106">Carrega o registro de destino com dados de cor (RGBA) amostrados de uma textura.</span><span class="sxs-lookup"><span data-stu-id="9b16e-106">Loads the destination register with color data (RGBA) sampled from a texture.</span></span> <span data-ttu-id="9b16e-107">A textura deve estar associada a um estágio de textura específico (n) usando [**SetTexture**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture).</span><span class="sxs-lookup"><span data-stu-id="9b16e-107">The texture must be bound to a particular texture stage (n) using [**SetTexture**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture).</span></span> <span data-ttu-id="9b16e-108">A amostragem de textura é controlada por [**Setsamplestate**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-setsamplerstate).</span><span class="sxs-lookup"><span data-stu-id="9b16e-108">Texture sampling is controlled by [**SetSamplerState**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-setsamplerstate).</span></span>

## <a name="syntax"></a><span data-ttu-id="9b16e-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="9b16e-109">Syntax</span></span>



| <span data-ttu-id="9b16e-110">Tex DST</span><span class="sxs-lookup"><span data-stu-id="9b16e-110">tex dst</span></span> |
|---------|



 

<span data-ttu-id="9b16e-111">onde</span><span class="sxs-lookup"><span data-stu-id="9b16e-111">where</span></span>

-   <span data-ttu-id="9b16e-112">DST é o registro de destino.</span><span class="sxs-lookup"><span data-stu-id="9b16e-112">dst is the destination register.</span></span>

## <a name="remarks"></a><span data-ttu-id="9b16e-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="9b16e-113">Remarks</span></span>



| <span data-ttu-id="9b16e-114">Versões do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="9b16e-114">Pixel shader versions</span></span> | <span data-ttu-id="9b16e-115">1\_1</span><span class="sxs-lookup"><span data-stu-id="9b16e-115">1\_1</span></span> | <span data-ttu-id="9b16e-116">1\_2</span><span class="sxs-lookup"><span data-stu-id="9b16e-116">1\_2</span></span> | <span data-ttu-id="9b16e-117">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="9b16e-117">1\_3</span></span> | <span data-ttu-id="9b16e-118">1\_4</span><span class="sxs-lookup"><span data-stu-id="9b16e-118">1\_4</span></span> | <span data-ttu-id="9b16e-119">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="9b16e-119">2\_0</span></span> | <span data-ttu-id="9b16e-120">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="9b16e-120">2\_x</span></span> | <span data-ttu-id="9b16e-121">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="9b16e-121">2\_sw</span></span> | <span data-ttu-id="9b16e-122">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="9b16e-122">3\_0</span></span> | <span data-ttu-id="9b16e-123">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="9b16e-123">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="9b16e-124">tex</span><span class="sxs-lookup"><span data-stu-id="9b16e-124">tex</span></span>                   | <span data-ttu-id="9b16e-125">x</span><span class="sxs-lookup"><span data-stu-id="9b16e-125">x</span></span>    | <span data-ttu-id="9b16e-126">x</span><span class="sxs-lookup"><span data-stu-id="9b16e-126">x</span></span>    | <span data-ttu-id="9b16e-127">x</span><span class="sxs-lookup"><span data-stu-id="9b16e-127">x</span></span>    |      |      |      |       |      |       |



 

<span data-ttu-id="9b16e-128">O número de registro de destino especifica o número de estágio de textura.</span><span class="sxs-lookup"><span data-stu-id="9b16e-128">The destination register number specifies the texture stage number.</span></span>

<span data-ttu-id="9b16e-129">A amostragem de textura usa coordenadas de textura para pesquisar ou obter um valor de cor nas coordenadas especificadas (u, v, w, q) ao levar em conta os atributos de estado do estágio de textura.</span><span class="sxs-lookup"><span data-stu-id="9b16e-129">Texture sampling uses texture coordinates to look up, or sample, a color value at the specified (u,v,w,q) coordinates while taking into account the texture stage state attributes.</span></span>

<span data-ttu-id="9b16e-130">Os dados de coordenadas de textura são interpolados dos dados de coordenadas de textura de vértice e associados a um estágio de textura específico.</span><span class="sxs-lookup"><span data-stu-id="9b16e-130">The texture coordinate data is interpolated from the vertex texture coordinate data and is associated with a specific texture stage.</span></span> <span data-ttu-id="9b16e-131">A associação padrão é um mapeamento de um para um entre o número de estágio de textura e a ordem de declaração de coordenada de textura.</span><span class="sxs-lookup"><span data-stu-id="9b16e-131">The default association is a one-to-one mapping between texture stage number and texture coordinate declaration order.</span></span> <span data-ttu-id="9b16e-132">Isso significa que o primeiro conjunto de coordenadas de textura definido no formato de vértice é, por padrão, associado ao estágio 0 da textura.</span><span class="sxs-lookup"><span data-stu-id="9b16e-132">This means that the first set of texture coordinates defined in the vertex format are by default associated with texture stage 0.</span></span>

<span data-ttu-id="9b16e-133">As coordenadas de textura podem ser associadas a qualquer estágio usando duas técnicas.</span><span class="sxs-lookup"><span data-stu-id="9b16e-133">Texture coordinates may be associated with any stage using two techniques.</span></span> <span data-ttu-id="9b16e-134">Ao usar um sombreador de vértice de função fixa ou o pipeline de função fixa, o sinalizador de estado de estágio de textura TSS \_ TEXCOORDINDEX pode ser usado no [**SetTextureStageState**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate) para associar coordenadas a um estágio.</span><span class="sxs-lookup"><span data-stu-id="9b16e-134">When using a fixed function vertex shader or the fixed function pipeline, the texture stage state flag TSS\_TEXCOORDINDEX can be used in [**SetTextureStageState**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate) to associate coordinates to a stage.</span></span> <span data-ttu-id="9b16e-135">Caso contrário, as coordenadas de textura são geradas pelo oTn do sombreador de vértice que registra ao usar um sombreador de vértice programável.</span><span class="sxs-lookup"><span data-stu-id="9b16e-135">Otherwise, the texture coordinates are output by the vertex shader oTₙ registers when using a programmable vertex shader.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9b16e-136">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9b16e-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9b16e-137">Instruções do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="9b16e-137">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 