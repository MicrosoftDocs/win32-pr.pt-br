---
title: texreg2rgb-PS
description: Interpreta os componentes de cor vermelho, verde e azul (RGB) do registro de origem como dados de endereço de textura para obter amostras da textura no estágio correspondente ao número de registro de destino. O resultado é armazenado no registro de destino.
ms.assetid: 8ec44014-d796-407c-8fe0-036decaf2a3d
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f8bcd2bbd7e57ba9dc692f34404a5610cdc517f3
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104498946"
---
# <a name="texreg2rgb---ps"></a><span data-ttu-id="4b4a9-104">texreg2rgb-PS</span><span class="sxs-lookup"><span data-stu-id="4b4a9-104">texreg2rgb - ps</span></span>

<span data-ttu-id="4b4a9-105">Interpreta os componentes de cor vermelho, verde e azul (RGB) do registro de origem como dados de endereço de textura para obter amostras da textura no estágio correspondente ao número de registro de destino.</span><span class="sxs-lookup"><span data-stu-id="4b4a9-105">Interprets the red, green, and blue (RGB) color components of the source register as texture address data in order to sample the texture at the stage corresponding to the destination register number.</span></span> <span data-ttu-id="4b4a9-106">O resultado é armazenado no registro de destino.</span><span class="sxs-lookup"><span data-stu-id="4b4a9-106">The result is stored in the destination register.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b4a9-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="4b4a9-107">Syntax</span></span>



| <span data-ttu-id="4b4a9-108">texreg2rgb DST, src</span><span class="sxs-lookup"><span data-stu-id="4b4a9-108">texreg2rgb dst, src</span></span> |
|---------------------|



 

<span data-ttu-id="4b4a9-109">onde</span><span class="sxs-lookup"><span data-stu-id="4b4a9-109">where</span></span>

-   <span data-ttu-id="4b4a9-110">DST é o registro de destino.</span><span class="sxs-lookup"><span data-stu-id="4b4a9-110">dst is the destination register.</span></span>
-   <span data-ttu-id="4b4a9-111">src é um registro de origem.</span><span class="sxs-lookup"><span data-stu-id="4b4a9-111">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="4b4a9-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="4b4a9-112">Remarks</span></span>



| <span data-ttu-id="4b4a9-113">Versões do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="4b4a9-113">Pixel shader versions</span></span> | <span data-ttu-id="4b4a9-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="4b4a9-114">1\_1</span></span> | <span data-ttu-id="4b4a9-115">1\_2</span><span class="sxs-lookup"><span data-stu-id="4b4a9-115">1\_2</span></span> | <span data-ttu-id="4b4a9-116">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="4b4a9-116">1\_3</span></span> | <span data-ttu-id="4b4a9-117">1\_4</span><span class="sxs-lookup"><span data-stu-id="4b4a9-117">1\_4</span></span> | <span data-ttu-id="4b4a9-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="4b4a9-118">2\_0</span></span> | <span data-ttu-id="4b4a9-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="4b4a9-119">2\_x</span></span> | <span data-ttu-id="4b4a9-120">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="4b4a9-120">2\_sw</span></span> | <span data-ttu-id="4b4a9-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="4b4a9-121">3\_0</span></span> | <span data-ttu-id="4b4a9-122">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="4b4a9-122">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="4b4a9-123">texreg2rgb</span><span class="sxs-lookup"><span data-stu-id="4b4a9-123">texreg2rgb</span></span>            |      | <span data-ttu-id="4b4a9-124">x</span><span class="sxs-lookup"><span data-stu-id="4b4a9-124">x</span></span>    | <span data-ttu-id="4b4a9-125">x</span><span class="sxs-lookup"><span data-stu-id="4b4a9-125">x</span></span>    |      |      |      |       |      |       |



 

<span data-ttu-id="4b4a9-126">Essa instrução é útil para operações de remapeamento de espaço de cor.</span><span class="sxs-lookup"><span data-stu-id="4b4a9-126">This instruction is useful for color-space remapping operations.</span></span> <span data-ttu-id="4b4a9-127">Ele dá suporte a coordenadas bidimensionais (2D) e tridimensionais (3D).</span><span class="sxs-lookup"><span data-stu-id="4b4a9-127">It supports two-dimensional (2D) and three-dimensional (3D) coordinates.</span></span> <span data-ttu-id="4b4a9-128">Ele pode ser usado exatamente como [texreg2ar-PS](texreg2ar---ps.md) ou [texreg2gb-PS](texreg2gb---ps.md) para remapear dados 2D.</span><span class="sxs-lookup"><span data-stu-id="4b4a9-128">It can be used just like the [texreg2ar - ps](texreg2ar---ps.md) or [texreg2gb - ps](texreg2gb---ps.md) to remap 2D data.</span></span> <span data-ttu-id="4b4a9-129">No entanto, essa instrução também dá suporte a dados 3D para que ele possa ser usado com mapas de cubo e texturas de volume 3D.</span><span class="sxs-lookup"><span data-stu-id="4b4a9-129">However, this instruction also supports 3D data so it can be used with cube maps and 3D volume textures.</span></span>

<span data-ttu-id="4b4a9-130">Veja a seguir um exemplo da seqüência da instrução.</span><span class="sxs-lookup"><span data-stu-id="4b4a9-130">Here is an example of the sequence the instruction follows.</span></span>


```
 
tex t(n)
texreg2rgb t(m), t(n)     where m > n
```



<span data-ttu-id="4b4a9-131">Veja mais detalhes sobre como o remapeamento é realizado.</span><span class="sxs-lookup"><span data-stu-id="4b4a9-131">Here is more detail about how the remapping is accomplished.</span></span>

<dl> <span data-ttu-id="4b4a9-132">A primeira instrução carrega a cor de textura (RGBA) em registrar TN</span><span class="sxs-lookup"><span data-stu-id="4b4a9-132">// The first instruction loads the texture color (RGBA) into register tn</span></span>  
<span data-ttu-id="4b4a9-133">Tex TN</span><span class="sxs-lookup"><span data-stu-id="4b4a9-133">tex tn</span></span>  
<span data-ttu-id="4b4a9-134">A segunda instrução remapeia a cor</span><span class="sxs-lookup"><span data-stu-id="4b4a9-134">// The second instruction remaps the color</span></span>  
<span data-ttu-id="4b4a9-135">t (m)<sub>RGBA</sub> = TextureSample (estágio m)<sub>RGBA</sub> usando t (n)<sub>RGB</sub> como coordenadas</span><span class="sxs-lookup"><span data-stu-id="4b4a9-135">t(m)<sub>RGBA</sub> = TextureSample(stage m)<sub>RGBA</sub> using t(n)<sub>RGB</sub> as coordinates</span></span>
</dl>

## <a name="related-topics"></a><span data-ttu-id="4b4a9-136">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4b4a9-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4b4a9-137">Instruções do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="4b4a9-137">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




