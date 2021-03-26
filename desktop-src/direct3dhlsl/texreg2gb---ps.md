---
title: texreg2gb-PS
description: Interpreta os componentes de cor verde e azul do registro de origem como dados de endereço de textura para amostrar a textura no estágio correspondente ao número de registro de destino.
ms.assetid: 81d3fb3e-ef53-4d25-b65d-c4c9fea0c74c
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8d6c428ee5a532919916f0a714db7f81a1c75c12
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104967185"
---
# <a name="texreg2gb---ps"></a><span data-ttu-id="2d8f8-103">texreg2gb-PS</span><span class="sxs-lookup"><span data-stu-id="2d8f8-103">texreg2gb - ps</span></span>

<span data-ttu-id="2d8f8-104">Interpreta os componentes de cor verde e azul do registro de origem como dados de endereço de textura para amostrar a textura no estágio correspondente ao número de registro de destino.</span><span class="sxs-lookup"><span data-stu-id="2d8f8-104">Interprets the green and blue color components of the source register as texture address data to sample the texture at the stage corresponding to the destination register number.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d8f8-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2d8f8-105">Syntax</span></span>



| <span data-ttu-id="2d8f8-106">texreg2gb DST, src</span><span class="sxs-lookup"><span data-stu-id="2d8f8-106">texreg2gb dst, src</span></span> |
|--------------------|



 

<span data-ttu-id="2d8f8-107">onde</span><span class="sxs-lookup"><span data-stu-id="2d8f8-107">where</span></span>

-   <span data-ttu-id="2d8f8-108">DST é o registro de destino.</span><span class="sxs-lookup"><span data-stu-id="2d8f8-108">dst is the destination register.</span></span>
-   <span data-ttu-id="2d8f8-109">src é um registro de origem.</span><span class="sxs-lookup"><span data-stu-id="2d8f8-109">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="2d8f8-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="2d8f8-110">Remarks</span></span>



| <span data-ttu-id="2d8f8-111">Versões do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="2d8f8-111">Pixel shader versions</span></span> | <span data-ttu-id="2d8f8-112">1\_1</span><span class="sxs-lookup"><span data-stu-id="2d8f8-112">1\_1</span></span> | <span data-ttu-id="2d8f8-113">1\_2</span><span class="sxs-lookup"><span data-stu-id="2d8f8-113">1\_2</span></span> | <span data-ttu-id="2d8f8-114">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="2d8f8-114">1\_3</span></span> | <span data-ttu-id="2d8f8-115">1\_4</span><span class="sxs-lookup"><span data-stu-id="2d8f8-115">1\_4</span></span> | <span data-ttu-id="2d8f8-116">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="2d8f8-116">2\_0</span></span> | <span data-ttu-id="2d8f8-117">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="2d8f8-117">2\_x</span></span> | <span data-ttu-id="2d8f8-118">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="2d8f8-118">2\_sw</span></span> | <span data-ttu-id="2d8f8-119">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="2d8f8-119">3\_0</span></span> | <span data-ttu-id="2d8f8-120">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="2d8f8-120">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="2d8f8-121">texreg2gb</span><span class="sxs-lookup"><span data-stu-id="2d8f8-121">texreg2gb</span></span>             |      | <span data-ttu-id="2d8f8-122">x</span><span class="sxs-lookup"><span data-stu-id="2d8f8-122">x</span></span>    | <span data-ttu-id="2d8f8-123">x</span><span class="sxs-lookup"><span data-stu-id="2d8f8-123">x</span></span>    |      |      |      |       |      |       |



 

<span data-ttu-id="2d8f8-124">Essa instrução é útil para operações de remapeamento de espaço de cor.</span><span class="sxs-lookup"><span data-stu-id="2d8f8-124">This instruction is useful for color-space remapping operations.</span></span>

<span data-ttu-id="2d8f8-125">Veja a seguir um exemplo da seqüência da instrução.</span><span class="sxs-lookup"><span data-stu-id="2d8f8-125">Here is an example of the sequence the instruction follows.</span></span>

<dl> <span data-ttu-id="2d8f8-126">Tex t (n)</span><span class="sxs-lookup"><span data-stu-id="2d8f8-126">tex t(n)</span></span>  
<span data-ttu-id="2d8f8-127">texreg2gb t (m), t (n) onde m > n</span><span class="sxs-lookup"><span data-stu-id="2d8f8-127">texreg2gb t(m), t(n) where m > n</span></span>  
<span data-ttu-id="2d8f8-128">A primeira instrução carrega a cor de textura (RGBA)</span><span class="sxs-lookup"><span data-stu-id="2d8f8-128">// The first instruction loads the texture color (RGBA)</span></span>  
<span data-ttu-id="2d8f8-129">em registrar TN</span><span class="sxs-lookup"><span data-stu-id="2d8f8-129">// into register tn</span></span>  
<span data-ttu-id="2d8f8-130">Tex TN</span><span class="sxs-lookup"><span data-stu-id="2d8f8-130">tex tn</span></span>  
<span data-ttu-id="2d8f8-131">A segunda instrução remapeia a cor</span><span class="sxs-lookup"><span data-stu-id="2d8f8-131">// The second instruction remaps the color</span></span>  
<span data-ttu-id="2d8f8-132">t (m)<sub>RGBA</sub> = TextureSample (estágio m)<sub>RGBA</sub> usando t (n)<sub>GB</sub> como coordenadas</span><span class="sxs-lookup"><span data-stu-id="2d8f8-132">t(m)<sub>RGBA</sub> = TextureSample(stage m)<sub>RGBA</sub> using t(n)<sub>GB</sub> as coordinates</span></span>
</dl>

<span data-ttu-id="2d8f8-133">\_BX2 não pode ser usado no registro src para instruções [texreg2ar-PS](texreg2ar---ps.md) ou texreg2gb.</span><span class="sxs-lookup"><span data-stu-id="2d8f8-133">\_bx2 cannot be used on the src register for [texreg2ar - ps](texreg2ar---ps.md) or texreg2gb instructions.</span></span>

<span data-ttu-id="2d8f8-134">Para essa instrução, o registro de origem deve usar dados não assinados.</span><span class="sxs-lookup"><span data-stu-id="2d8f8-134">For this instruction, the source register must use unsigned data.</span></span> <span data-ttu-id="2d8f8-135">O uso de dados assinados ou mistos no registro de origem produzirá resultados indefinidos.</span><span class="sxs-lookup"><span data-stu-id="2d8f8-135">Use of signed or mixed data in the source register will produce undefined results.</span></span> <span data-ttu-id="2d8f8-136">Para obter mais informações, consulte [D3DFORMAT](/windows/desktop/direct3d9/d3dformat).</span><span class="sxs-lookup"><span data-stu-id="2d8f8-136">For more information, see [D3DFORMAT](/windows/desktop/direct3d9/d3dformat).</span></span>

## <a name="related-topics"></a><span data-ttu-id="2d8f8-137">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2d8f8-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2d8f8-138">Instruções do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="2d8f8-138">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 