---
title: Registro de cor de saída
description: Os registros de saída de cor do sombreador de pixel (oC \) são registros somente gravação que geram resultados de saída para vários destinos de renderização.
ms.assetid: 88e69189-3956-47de-a336-921f1e62c025
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 316160e39ce172d56e4ecac17dfbd1d53077005b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366509"
---
# <a name="output-color-register"></a><span data-ttu-id="c2e05-103">Registro de cor de saída</span><span class="sxs-lookup"><span data-stu-id="c2e05-103">Output Color Register</span></span>

<span data-ttu-id="c2e05-104">Os registros de saída de cor do sombreador de pixel (oC #) são registros somente gravação que geram resultados de saída para vários destinos de renderização.</span><span class="sxs-lookup"><span data-stu-id="c2e05-104">The pixel shader color output registers (oC#) are write-only registers that output results to multiple render targets.</span></span>

<span data-ttu-id="c2e05-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c2e05-105">Syntax</span></span>



| <span data-ttu-id="c2e05-106">oC #</span><span class="sxs-lookup"><span data-stu-id="c2e05-106">oC#</span></span> |
|------|



 

<span data-ttu-id="c2e05-107">Em que:</span><span class="sxs-lookup"><span data-stu-id="c2e05-107">Where:</span></span>



| <span data-ttu-id="c2e05-108">Name</span><span class="sxs-lookup"><span data-stu-id="c2e05-108">Name</span></span> | <span data-ttu-id="c2e05-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="c2e05-109">Description</span></span>       |
|------|-------------------|
| <span data-ttu-id="c2e05-110">oC0</span><span class="sxs-lookup"><span data-stu-id="c2e05-110">oC0</span></span>  | <span data-ttu-id="c2e05-111">renderizar destino \# 0</span><span class="sxs-lookup"><span data-stu-id="c2e05-111">render target \#0</span></span> |
| <span data-ttu-id="c2e05-112">oC1</span><span class="sxs-lookup"><span data-stu-id="c2e05-112">oC1</span></span>  | <span data-ttu-id="c2e05-113">destino de renderização \# 1</span><span class="sxs-lookup"><span data-stu-id="c2e05-113">render target \#1</span></span> |
| <span data-ttu-id="c2e05-114">oC2</span><span class="sxs-lookup"><span data-stu-id="c2e05-114">oC2</span></span>  | <span data-ttu-id="c2e05-115">destino de renderização \# 2</span><span class="sxs-lookup"><span data-stu-id="c2e05-115">render target \#2</span></span> |
| <span data-ttu-id="c2e05-116">oC3</span><span class="sxs-lookup"><span data-stu-id="c2e05-116">oC3</span></span>  | <span data-ttu-id="c2e05-117">destino de renderização \# 3</span><span class="sxs-lookup"><span data-stu-id="c2e05-117">render target \#3</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="c2e05-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="c2e05-118">Remarks</span></span>

-   <span data-ttu-id="c2e05-119">Se oCn for gravado, mas não houver nenhum destino de renderização correspondente, essa gravação em oCn será ignorada.</span><span class="sxs-lookup"><span data-stu-id="c2e05-119">If oCn is written but there is no corresponding render target, then this write to oCn is ignored.</span></span>
-   <span data-ttu-id="c2e05-120">Os Estados de renderização D3DRS \_ COLORWRITEENABLE, D3DRS \_ COLORWRITEENABLE1, D3DRS \_ COLORWRITEENABLE2 e D3DRS COLORWRITEENABLE3 \_ determinam quais componentes de oCn, por fim, são gravados no destino de renderização (após Blend, se aplicável).</span><span class="sxs-lookup"><span data-stu-id="c2e05-120">The render states D3DRS\_COLORWRITEENABLE, D3DRS\_COLORWRITEENABLE1, D3DRS\_COLORWRITEENABLE2 and D3DRS\_COLORWRITEENABLE3 determine which components of oCn ultimately get written to the render target (after blend, if applicable).</span></span> <span data-ttu-id="c2e05-121">Se o sombreador gravar alguns, mas não todos os componentes definidos pelos \_ Estados de RENDERIZAÇÃO D3DRS COLORWRITEENABLE \* para um determinado registro oCn, os canais não gravados produzirão valores indefinidos no destino de renderização correspondente.</span><span class="sxs-lookup"><span data-stu-id="c2e05-121">If the shader writes some but not all of the components defined by the D3DRS\_COLORWRITEENABLE\* render states for a given oCn register, then the unwritten channels produce undefined values in the corresponding render target.</span></span> <span data-ttu-id="c2e05-122">Se nenhum dos componentes de um oCn for gravado, o destino de renderização correspondente não deverá ser atualizado (como mencionado acima), de modo que os \_ Estados de RENDERIZAÇÃO D3DRS COLORWRITEENABLE \* não se aplicarão.</span><span class="sxs-lookup"><span data-stu-id="c2e05-122">If none of the components of an oCn are written, the corresponding render target must not be updated at all (as stated above), so the D3DRS\_COLORWRITEENABLE\* render states do not apply.</span></span>

### <a name="shader-model-2-restrictions"></a><span data-ttu-id="c2e05-123">Restrições do modelo de sombreador 2</span><span class="sxs-lookup"><span data-stu-id="c2e05-123">Shader Model 2 Restrictions</span></span>

-   <span data-ttu-id="c2e05-124">oCn só pode ser escrito com a instrução [Mov-PS](mov---ps.md) .</span><span class="sxs-lookup"><span data-stu-id="c2e05-124">oCn can only be written with the [mov - ps](mov---ps.md) instruction.</span></span>
-   <span data-ttu-id="c2e05-125">oC0 deve ser sempre escrito no sombreador.</span><span class="sxs-lookup"><span data-stu-id="c2e05-125">oC0 must be always written in the shader.</span></span>
-   <span data-ttu-id="c2e05-126">Nenhum swizzle de origem (exceto. xyzw = default swizzle) ou modificador de origem é permitido ao gravar em qualquer oCn.</span><span class="sxs-lookup"><span data-stu-id="c2e05-126">No source swizzle (except .xyzw = default swizzle) or source modifier is allowed when writing to any oCn.</span></span>
-   <span data-ttu-id="c2e05-127">Nenhuma máscara de gravação de destino (exceto. xyzw = máscara padrão) ou modificador de instrução é permitido ao gravar em qualquer oCn.</span><span class="sxs-lookup"><span data-stu-id="c2e05-127">No destination write mask (except .xyzw = default mask) or instruction modifier is allowed when writing to any oCn.</span></span>
-   <span data-ttu-id="c2e05-128">Se oCn for gravado, oC0-oCn-1 também deverá ser gravado.</span><span class="sxs-lookup"><span data-stu-id="c2e05-128">If oCn is written, then oC0 - oCn-1 must also be written.</span></span> <span data-ttu-id="c2e05-129">Por exemplo, para gravar em oC2, você também deve gravar em oC0 e oC1.</span><span class="sxs-lookup"><span data-stu-id="c2e05-129">For example, to write to oC2, you must also write to oC0 and oC1.</span></span>
-   <span data-ttu-id="c2e05-130">É permitido no máximo uma gravação para qualquer oC # por sombreador.</span><span class="sxs-lookup"><span data-stu-id="c2e05-130">At most one write to any oC# per shader is allowed.</span></span>
-   <span data-ttu-id="c2e05-131">Para o PS \_ 2 \_ x e o PS \_ 3 \_ 0, não é possível gravar nos registros OC # e OD \# no controle de fluxo dinâmico ou predicação (as gravações para o OC # dentro do controle de fluxo estático estão corretas).</span><span class="sxs-lookup"><span data-stu-id="c2e05-131">For ps\_2\_x and ps\_3\_0, you cannot write to oC# and oD\# registers within dynamic flow control or predication (writes to oC# inside static flow control is fine).</span></span>

### <a name="shader-model-3-restrictions"></a><span data-ttu-id="c2e05-132">Restrições do modelo do sombreador 3</span><span class="sxs-lookup"><span data-stu-id="c2e05-132">Shader Model 3 Restrictions</span></span>

-   <span data-ttu-id="c2e05-133">Para o PS \_ 3 \_ 0, os registros de saída OC # e OD \# podem ser gravados várias vezes.</span><span class="sxs-lookup"><span data-stu-id="c2e05-133">For ps\_3\_0, output registers oC# and oD\# can be written any number of times.</span></span> <span data-ttu-id="c2e05-134">A saída do sombreador de pixel é proveniente do conteúdo dos registros de saída no final da execução do sombreador.</span><span class="sxs-lookup"><span data-stu-id="c2e05-134">The output of the pixel shader comes from the contents of the output registers at the end of shader execution.</span></span> <span data-ttu-id="c2e05-135">Se uma gravação em um registro de saída não ocorrer, talvez devido ao controle de fluxo ou se o sombreador simplesmente não o escreveu, o renderTarget correspondente também não será atualizado.</span><span class="sxs-lookup"><span data-stu-id="c2e05-135">If a write to an output register does not happen, perhaps due to flow control or if the shader just did not write it, the corresponding rendertarget is also not updated.</span></span> <span data-ttu-id="c2e05-136">Se um subconjunto dos canais em um registro de saída for gravado, os valores indefinidos serão gravados nos canais restantes.</span><span class="sxs-lookup"><span data-stu-id="c2e05-136">If a subset of the channels in an output register are written, then undefined values will be written to the remaining channels.</span></span>
-   <span data-ttu-id="c2e05-137">Para \_ o PS 3 \_ 0, os registros de OC # podem ser gravados com qualquer writemasks.</span><span class="sxs-lookup"><span data-stu-id="c2e05-137">For ps\_3\_0, the oC# registers can be written with any writemasks.</span></span>
-   <span data-ttu-id="c2e05-138">Para o PS \_ 2 \_ x e o PS \_ 3 \_ 0, não é possível gravar nos registros OC # e OD \# no controle de fluxo dinâmico ou predicação (as gravações para o OC # dentro do controle de fluxo estático estão corretas).</span><span class="sxs-lookup"><span data-stu-id="c2e05-138">For ps\_2\_x and ps\_3\_0, you cannot write to oC# and oD\# registers within dynamic flow control or predication (writes to oC# inside static flow control is fine).</span></span>
-   <span data-ttu-id="c2e05-139">Você não pode executar cálculos de gradiente (ou operações que invocam implicitamente cálculos de gradiente, como [texld-PS \_ 2 \_ 0 e up](texld---ps-2-0.md), [texldb-PS](texldb---ps.md), [texldp-PS](texldp---ps.md)) dentro de instruções de controle de fluxo cujas condições de ramificação variam em uma base por primitiva (isto é: instruções de controle de fluxo dinâmico).</span><span class="sxs-lookup"><span data-stu-id="c2e05-139">You may not perform any gradient calculations (or operations that implicitly invoke gradient calculations such as [texld - ps\_2\_0 and up](texld---ps-2-0.md), [texldb - ps](texldb---ps.md), [texldp - ps](texldp---ps.md)) inside of flow control statements whose branching conditions vary on a per-primitive basis (ie: dynamic flow control instructions).</span></span> <span data-ttu-id="c2e05-140">Instrução predicação não é considerada controle de fluxo dinâmico.</span><span class="sxs-lookup"><span data-stu-id="c2e05-140">Instruction predication is not considered dynamic flow control.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c2e05-141">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c2e05-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c2e05-142">Register</span><span class="sxs-lookup"><span data-stu-id="c2e05-142">Registers</span></span>](dx9-graphics-reference-asm-ps-registers.md)
</dt> <dt>

[<span data-ttu-id="c2e05-143">Vários destinos de renderização (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="c2e05-143">Multiple Render Targets (Direct3D 9)</span></span>](/windows/desktop/direct3d9/multiple-render-targets)
</dt> </dl>

 

 