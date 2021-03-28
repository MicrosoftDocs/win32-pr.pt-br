---
title: texldd-PS
description: Amostra uma textura com entradas de gradiente adicionais.
ms.assetid: 6d6b3180-d82e-4be4-929b-e5a6431bec38
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 72f3c4aaf9ac7e6beaad1343c024aa28bd2a85ab
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366040"
---
# <a name="texldd---ps"></a><span data-ttu-id="8b9b6-103">texldd-PS</span><span class="sxs-lookup"><span data-stu-id="8b9b6-103">texldd - ps</span></span>

<span data-ttu-id="8b9b6-104">Amostra uma textura com entradas de gradiente adicionais.</span><span class="sxs-lookup"><span data-stu-id="8b9b6-104">Samples a texture with additional gradient inputs.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b9b6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8b9b6-105">Syntax</span></span>



| <span data-ttu-id="8b9b6-106">texldd, DST, src0, src1, src2, src3</span><span class="sxs-lookup"><span data-stu-id="8b9b6-106">texldd, dst, src0, src1, src2, src3</span></span> |
|-------------------------------------|



 

<span data-ttu-id="8b9b6-107">Em que:</span><span class="sxs-lookup"><span data-stu-id="8b9b6-107">Where:</span></span>

-   <span data-ttu-id="8b9b6-108">o DST é um registro de destino.</span><span class="sxs-lookup"><span data-stu-id="8b9b6-108">dst is a destination register.</span></span>
-   <span data-ttu-id="8b9b6-109">src0 é um registro de origem que fornece as coordenadas de textura para o exemplo de textura.</span><span class="sxs-lookup"><span data-stu-id="8b9b6-109">src0 is a source register that provides the texture coordinates for the texture sample.</span></span> <span data-ttu-id="8b9b6-110">Consulte [registro de coordenadas de textura](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md).</span><span class="sxs-lookup"><span data-stu-id="8b9b6-110">See [Texture Coordinate Register](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md).</span></span>
-   <span data-ttu-id="8b9b6-111">src1 identifica os registros de amostra de origem \# , em que \# especifica qual número de amostra de textura deve ser amostrado.</span><span class="sxs-lookup"><span data-stu-id="8b9b6-111">src1 identifies the source sampler register (s\#), where \# specifies which texture sampler number to sample.</span></span> <span data-ttu-id="8b9b6-112">O classificador foi associado a ele uma textura e um estado de controle definido pela enumeração [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype) (por exemplo,</span><span class="sxs-lookup"><span data-stu-id="8b9b6-112">The sampler has associated with it a texture and a control state defined by the [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype) enumeration (ex.</span></span> <span data-ttu-id="8b9b6-113">D3DSAMP \_ MINFILTER).</span><span class="sxs-lookup"><span data-stu-id="8b9b6-113">D3DSAMP\_MINFILTER).</span></span>
-   <span data-ttu-id="8b9b6-114">src2 é um registro de fonte de entrada que especifica o gradiente x.</span><span class="sxs-lookup"><span data-stu-id="8b9b6-114">src2 is an input source register that specifies the x gradient.</span></span>
-   <span data-ttu-id="8b9b6-115">src3 é um registro de fonte de entrada que especifica o gradiente y.</span><span class="sxs-lookup"><span data-stu-id="8b9b6-115">src3 is an input source register that specifies the y gradient.</span></span>

## <a name="remarks"></a><span data-ttu-id="8b9b6-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="8b9b6-116">Remarks</span></span>



| <span data-ttu-id="8b9b6-117">Versões do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="8b9b6-117">Pixel shader versions</span></span> | <span data-ttu-id="8b9b6-118">1\_1</span><span class="sxs-lookup"><span data-stu-id="8b9b6-118">1\_1</span></span> | <span data-ttu-id="8b9b6-119">1\_2</span><span class="sxs-lookup"><span data-stu-id="8b9b6-119">1\_2</span></span> | <span data-ttu-id="8b9b6-120">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="8b9b6-120">1\_3</span></span> | <span data-ttu-id="8b9b6-121">1\_4</span><span class="sxs-lookup"><span data-stu-id="8b9b6-121">1\_4</span></span> | <span data-ttu-id="8b9b6-122">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="8b9b6-122">2\_0</span></span> | <span data-ttu-id="8b9b6-123">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="8b9b6-123">2\_x</span></span> | <span data-ttu-id="8b9b6-124">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="8b9b6-124">2\_sw</span></span> | <span data-ttu-id="8b9b6-125">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="8b9b6-125">3\_0</span></span> | <span data-ttu-id="8b9b6-126">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="8b9b6-126">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="8b9b6-127">texldd</span><span class="sxs-lookup"><span data-stu-id="8b9b6-127">texldd</span></span>                |      |      |      |      |      | <span data-ttu-id="8b9b6-128">w.x.y. \*</span><span class="sxs-lookup"><span data-stu-id="8b9b6-128">x \*</span></span> | <span data-ttu-id="8b9b6-129">x</span><span class="sxs-lookup"><span data-stu-id="8b9b6-129">x</span></span>     | <span data-ttu-id="8b9b6-130">x</span><span class="sxs-lookup"><span data-stu-id="8b9b6-130">x</span></span>    | <span data-ttu-id="8b9b6-131">x</span><span class="sxs-lookup"><span data-stu-id="8b9b6-131">x</span></span>     |



 

<span data-ttu-id="8b9b6-132">\* Essa instrução só tem suporte no PS \_ 2 \_ a.</span><span class="sxs-lookup"><span data-stu-id="8b9b6-132">\* This instruction is only supported by ps\_2\_a.</span></span> <span data-ttu-id="8b9b6-133">Não há suporte para ele no PS \_ 2 \_ b.</span><span class="sxs-lookup"><span data-stu-id="8b9b6-133">It is not supported by ps\_2\_b.</span></span> <span data-ttu-id="8b9b6-134">Para obter mais informações sobre perfis, consulte [**D3DXGetPixelShaderProfile**](/windows/desktop/direct3d9/d3dxgetpixelshaderprofile).</span><span class="sxs-lookup"><span data-stu-id="8b9b6-134">For more information about profiles, see [**D3DXGetPixelShaderProfile**](/windows/desktop/direct3d9/d3dxgetpixelshaderprofile).</span></span>

<span data-ttu-id="8b9b6-135">Esta instrução amostra uma textura usando as coordenadas de textura em src0, a amostra especificada por src1 e os gradientes DSX e DSY provenientes de src2 e src3.</span><span class="sxs-lookup"><span data-stu-id="8b9b6-135">This instruction samples a texture using the texture coordinates at src0, the sampler specified by src1, and the gradients DSX and DSY coming from src2 and src3.</span></span> <span data-ttu-id="8b9b6-136">Os valores de gradiente x e y são usados para selecionar o nível de mipmap apropriado da textura para amostragem.</span><span class="sxs-lookup"><span data-stu-id="8b9b6-136">The x and y gradient values are used to select the appropriate mipmap level of the texture for sampling.</span></span>

<span data-ttu-id="8b9b6-137">Todas as fontes dão suporte a swizzles arbitrários.</span><span class="sxs-lookup"><span data-stu-id="8b9b6-137">All sources support arbitrary swizzles.</span></span>

<span data-ttu-id="8b9b6-138">Todas as máscaras de gravação são válidas no destino.</span><span class="sxs-lookup"><span data-stu-id="8b9b6-138">All write masks are valid on the destination.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8b9b6-139">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8b9b6-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8b9b6-140">Instruções do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="8b9b6-140">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 