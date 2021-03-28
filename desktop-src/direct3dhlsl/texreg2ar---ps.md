---
title: texreg2ar-PS
description: Interpreta os componentes de cor alfa e vermelha do registro de origem como dados de endereço de textura (u, v) para amostrar a textura no estágio correspondente ao número de registro de destino. O resultado é armazenado no registro de destino.
ms.assetid: b31a2ee4-f9b9-4aee-b3be-7ccc5b8c6f3e
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 93418e7e9e87178cd64c2d7238b5227de0990378
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104454149"
---
# <a name="texreg2ar---ps"></a><span data-ttu-id="ca670-104">texreg2ar-PS</span><span class="sxs-lookup"><span data-stu-id="ca670-104">texreg2ar - ps</span></span>

<span data-ttu-id="ca670-105">Interpreta os componentes de cor alfa e vermelha do registro de origem como dados de endereço de textura (u, v) para amostrar a textura no estágio correspondente ao número de registro de destino.</span><span class="sxs-lookup"><span data-stu-id="ca670-105">Interprets the alpha and red color components of the source register as texture address data (u,v) to sample the texture at the stage corresponding to the destination register number.</span></span> <span data-ttu-id="ca670-106">O resultado é armazenado no registro de destino.</span><span class="sxs-lookup"><span data-stu-id="ca670-106">The result is stored in the destination register.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca670-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="ca670-107">Syntax</span></span>



| <span data-ttu-id="ca670-108">texreg2ar DST, src</span><span class="sxs-lookup"><span data-stu-id="ca670-108">texreg2ar dst, src</span></span> |
|--------------------|



 

<span data-ttu-id="ca670-109">onde</span><span class="sxs-lookup"><span data-stu-id="ca670-109">where</span></span>

-   <span data-ttu-id="ca670-110">DST é o registro de destino.</span><span class="sxs-lookup"><span data-stu-id="ca670-110">dst is the destination register.</span></span>
-   <span data-ttu-id="ca670-111">src é um registro de origem.</span><span class="sxs-lookup"><span data-stu-id="ca670-111">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="ca670-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="ca670-112">Remarks</span></span>



| <span data-ttu-id="ca670-113">Versões do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="ca670-113">Pixel shader versions</span></span> | <span data-ttu-id="ca670-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="ca670-114">1\_1</span></span> | <span data-ttu-id="ca670-115">1\_2</span><span class="sxs-lookup"><span data-stu-id="ca670-115">1\_2</span></span> | <span data-ttu-id="ca670-116">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="ca670-116">1\_3</span></span> | <span data-ttu-id="ca670-117">1\_4</span><span class="sxs-lookup"><span data-stu-id="ca670-117">1\_4</span></span> | <span data-ttu-id="ca670-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="ca670-118">2\_0</span></span> | <span data-ttu-id="ca670-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="ca670-119">2\_x</span></span> | <span data-ttu-id="ca670-120">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="ca670-120">2\_sw</span></span> | <span data-ttu-id="ca670-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="ca670-121">3\_0</span></span> | <span data-ttu-id="ca670-122">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="ca670-122">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="ca670-123">texreg2ar</span><span class="sxs-lookup"><span data-stu-id="ca670-123">texreg2ar</span></span>             | <span data-ttu-id="ca670-124">x</span><span class="sxs-lookup"><span data-stu-id="ca670-124">x</span></span>    | <span data-ttu-id="ca670-125">x</span><span class="sxs-lookup"><span data-stu-id="ca670-125">x</span></span>    | <span data-ttu-id="ca670-126">x</span><span class="sxs-lookup"><span data-stu-id="ca670-126">x</span></span>    |      |      |      |       |      |       |



 

<span data-ttu-id="ca670-127">Essa instrução é útil para operações de remapeamento de espaço de cor.</span><span class="sxs-lookup"><span data-stu-id="ca670-127">This instruction is useful for color-space remapping operations.</span></span>

<span data-ttu-id="ca670-128">Aqui está um exemplo da seqüência da instrução a seguir:</span><span class="sxs-lookup"><span data-stu-id="ca670-128">Here is an example of the sequence the instruction follows:</span></span>

<dl> <span data-ttu-id="ca670-129">Tex t (n)</span><span class="sxs-lookup"><span data-stu-id="ca670-129">tex t(n)</span></span>  
<span data-ttu-id="ca670-130">texreg2ar t (m), t (n) onde m > n</span><span class="sxs-lookup"><span data-stu-id="ca670-130">texreg2ar t(m), t(n) where m > n</span></span>  
<span data-ttu-id="ca670-131">A primeira instrução carrega a cor de textura (RGBA)</span><span class="sxs-lookup"><span data-stu-id="ca670-131">// The first instruction loads the texture color (RGBA)</span></span>  
<span data-ttu-id="ca670-132">em registrar TN</span><span class="sxs-lookup"><span data-stu-id="ca670-132">// into register tn</span></span>  
<span data-ttu-id="ca670-133">Tex TN</span><span class="sxs-lookup"><span data-stu-id="ca670-133">tex tn</span></span>  
<span data-ttu-id="ca670-134">A segunda instrução remapeia a cor</span><span class="sxs-lookup"><span data-stu-id="ca670-134">// The second instruction remaps the color</span></span>  
<span data-ttu-id="ca670-135">t (m)<sub>RGBA</sub> = TextureSample (estágio m)<sub>RGBA</sub> usando t (n)<sub>ar</sub> como coordenadas</span><span class="sxs-lookup"><span data-stu-id="ca670-135">t(m)<sub>RGBA</sub> = TextureSample(stage m)<sub>RGBA</sub> using t(n)<sub>AR</sub> as coordinates</span></span>
</dl>

<span data-ttu-id="ca670-136">\_BX2 não pode ser usado no registro src para obter instruções texreg2ar ou [texreg2gb-PS](texreg2gb---ps.md) .</span><span class="sxs-lookup"><span data-stu-id="ca670-136">\_bx2 cannot be used on the src register for texreg2ar or [texreg2gb - ps](texreg2gb---ps.md) instructions.</span></span>

<span data-ttu-id="ca670-137">Para essa instrução, o registro de origem deve usar dados não assinados.</span><span class="sxs-lookup"><span data-stu-id="ca670-137">For this instruction, the source register must use unsigned data.</span></span> <span data-ttu-id="ca670-138">O uso de dados assinados ou mistos no registro de origem produzirá resultados indefinidos.</span><span class="sxs-lookup"><span data-stu-id="ca670-138">Use of signed or mixed data in the source register will produce undefined results.</span></span> <span data-ttu-id="ca670-139">Para obter mais informações, consulte [D3DFORMAT](/windows/desktop/direct3d9/d3dformat).</span><span class="sxs-lookup"><span data-stu-id="ca670-139">For more information, see [D3DFORMAT](/windows/desktop/direct3d9/d3dformat).</span></span>

## <a name="related-topics"></a><span data-ttu-id="ca670-140">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ca670-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ca670-141">Instruções do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="ca670-141">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 