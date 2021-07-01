---
title: texld - ps_1_4
description: Carrega o registro de destino com dados de cor (RGBA) amostrados usando o conteúdo do registro de origem como coordenadas de textura. A textura amostrada é a textura associada ao número do registro de destino.
ms.assetid: 1970aed4-4da7-40a1-960d-fba4dfd8c433
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d956d9176a6356dc3837ee4f4d13b5bb700dda98
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118821"
---
# <a name="texld---ps_1_4"></a><span data-ttu-id="dea38-104">texld - ps \_ 1 \_ 4</span><span class="sxs-lookup"><span data-stu-id="dea38-104">texld - ps\_1\_4</span></span>

<span data-ttu-id="dea38-105">Carrega o registro de destino com dados de cor (RGBA) amostrados usando o conteúdo do registro de origem como coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="dea38-105">Loads the destination register with color data (RGBA) sampled using the contents of the source register as texture coordinates.</span></span> <span data-ttu-id="dea38-106">A textura amostrada é a textura associada ao número do registro de destino.</span><span class="sxs-lookup"><span data-stu-id="dea38-106">The sampled texture is the texture associated with the destination register number.</span></span>



| <span data-ttu-id="dea38-107">texld dst, src</span><span class="sxs-lookup"><span data-stu-id="dea38-107">texld dst, src</span></span> |
|----------------|



 

## <a name="registers"></a><span data-ttu-id="dea38-108">Registros</span><span class="sxs-lookup"><span data-stu-id="dea38-108">Registers</span></span>



| <span data-ttu-id="dea38-109">Valor</span><span class="sxs-lookup"><span data-stu-id="dea38-109">Value</span></span>         | <span data-ttu-id="dea38-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="dea38-110">Description</span></span>                     | <span data-ttu-id="dea38-111">Vn</span><span class="sxs-lookup"><span data-stu-id="dea38-111">vₙ</span></span>        | <span data-ttu-id="dea38-112">Cn</span><span class="sxs-lookup"><span data-stu-id="dea38-112">cₙ</span></span>  | <span data-ttu-id="dea38-113">Tn</span><span class="sxs-lookup"><span data-stu-id="dea38-113">tₙ</span></span>  | <span data-ttu-id="dea38-114">Rn</span><span class="sxs-lookup"><span data-stu-id="dea38-114">rₙ</span></span>  | <span data-ttu-id="dea38-115">Versão do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="dea38-115">Pixel shader version</span></span>              |
|----------|----------------------|-----------|-----|-----|-----|--------------|
| <span data-ttu-id="dea38-116">Dst</span><span class="sxs-lookup"><span data-stu-id="dea38-116">dst</span></span>      | <span data-ttu-id="dea38-117">Registro de destino</span><span class="sxs-lookup"><span data-stu-id="dea38-117">Destination register</span></span> |           |     |     | <span data-ttu-id="dea38-118">x</span><span class="sxs-lookup"><span data-stu-id="dea38-118">x</span></span>   | <span data-ttu-id="dea38-119">1\_4</span><span class="sxs-lookup"><span data-stu-id="dea38-119">1\_4</span></span>         |
| <span data-ttu-id="dea38-120">src</span><span class="sxs-lookup"><span data-stu-id="dea38-120">src</span></span>      | <span data-ttu-id="dea38-121">Registro de origem</span><span class="sxs-lookup"><span data-stu-id="dea38-121">Source register</span></span>      |           |     | <span data-ttu-id="dea38-122">x</span><span class="sxs-lookup"><span data-stu-id="dea38-122">x</span></span>   |     | <span data-ttu-id="dea38-123">1 \_ 4 fase 1</span><span class="sxs-lookup"><span data-stu-id="dea38-123">1\_4 phase 1</span></span> |
|          |                      |           |     | <span data-ttu-id="dea38-124">x</span><span class="sxs-lookup"><span data-stu-id="dea38-124">x</span></span>   | <span data-ttu-id="dea38-125">x</span><span class="sxs-lookup"><span data-stu-id="dea38-125">x</span></span>   | <span data-ttu-id="dea38-126">1 \_ 4 fase</span><span class="sxs-lookup"><span data-stu-id="dea38-126">1\_4 phase</span></span>   |



 

<span data-ttu-id="dea38-127">Ao usar r(n) como um registro de origem, os três primeiros componentes (XYZ) devem ter sido inicializados na fase anterior do sombreador.</span><span class="sxs-lookup"><span data-stu-id="dea38-127">When using r(n) as a source register, the first three components (XYZ) must have been initialized in the previous phase of the shader.</span></span>

<span data-ttu-id="dea38-128">Para saber mais sobre registros, consulte [ps \_ \_ 1 1 \_ \_ ps \_ 1 \_ 2 \_ \_ ps \_ 1 \_ 3 \_ \_ ps \_ 1 \_ 4 Registers](dx9-graphics-reference-asm-ps-registers-ps-1-x.md).</span><span class="sxs-lookup"><span data-stu-id="dea38-128">To learn more about registers, see [ps\_1\_1\_\_ps\_1\_2\_\_ps\_1\_3\_\_ps\_1\_4 Registers](dx9-graphics-reference-asm-ps-registers-ps-1-x.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="dea38-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="dea38-129">Remarks</span></span>

<span data-ttu-id="dea38-130">Esta instrução amostra a textura no estágio de textura associado ao número do registro de destino.</span><span class="sxs-lookup"><span data-stu-id="dea38-130">This instruction samples the texture in the texture stage associated with the destination register number.</span></span> <span data-ttu-id="dea38-131">A textura é amostrada usando dados de coordenadas de textura do registro de origem.</span><span class="sxs-lookup"><span data-stu-id="dea38-131">The texture is sampled using texture coordinate data from the source register.</span></span>

<span data-ttu-id="dea38-132">A sintaxe das instruções texld e texcrd expõe o suporte para uma divisão projetiva com um modificador de registro de textura.</span><span class="sxs-lookup"><span data-stu-id="dea38-132">The syntax for the texld and texcrd instructions expose support for a projective divide with a Texture Register Modifier.</span></span> <span data-ttu-id="dea38-133">Para o sombreador de pixel versão 1.4, o sinalizador de transformação de textura PROJECTED D3DTTFF \_ é sempre ignorado.</span><span class="sxs-lookup"><span data-stu-id="dea38-133">For pixel shader version 1.4, the D3DTTFF\_PROJECTED texture transform flag is always ignored.</span></span>

<span data-ttu-id="dea38-134">Regras para usar o texld:</span><span class="sxs-lookup"><span data-stu-id="dea38-134">Rules for using texld:</span></span>

1.  <span data-ttu-id="dea38-135">O mesmo modificador .xyz ou .xyw deve ser aplicado a cada leitura de um registro t(n) individual dentro de instruções de texcrd ou texld.</span><span class="sxs-lookup"><span data-stu-id="dea38-135">The same .xyz or .xyw modifier must be applied to every read of an individual t(n) register within both texcrd or texld instructions.</span></span> <span data-ttu-id="dea38-136">Se .xyw estiver sendo usado em leituras de registro t(n), isso poderá ser misto com outras leituras do mesmo registro t(n) usando .xyw \_ dw.</span><span class="sxs-lookup"><span data-stu-id="dea38-136">If .xyw is being used on t(n) register reads, this can be mixed with other reads of the same t(n) register using .xyw\_dw.</span></span>
2.  <span data-ttu-id="dea38-137">O \_ modificador de origem dz só é válido em texld com o registro de origem r(n) (portanto, somente a fase 2).</span><span class="sxs-lookup"><span data-stu-id="dea38-137">The \_dz source modifier is only valid on texld with r(n) source register (thus phase 2 only).</span></span>
3.  <span data-ttu-id="dea38-138">O \_ modificador de origem dz pode ser usado não mais de duas vezes por sombreador.</span><span class="sxs-lookup"><span data-stu-id="dea38-138">The \_dz source modifier may be used no more than two times per shader.</span></span>



| <span data-ttu-id="dea38-139">Versões do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="dea38-139">Pixel shader versions</span></span> | <span data-ttu-id="dea38-140">1\_1</span><span class="sxs-lookup"><span data-stu-id="dea38-140">1\_1</span></span> | <span data-ttu-id="dea38-141">1\_2</span><span class="sxs-lookup"><span data-stu-id="dea38-141">1\_2</span></span> | <span data-ttu-id="dea38-142">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="dea38-142">1\_3</span></span> | <span data-ttu-id="dea38-143">1\_4</span><span class="sxs-lookup"><span data-stu-id="dea38-143">1\_4</span></span> | <span data-ttu-id="dea38-144">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="dea38-144">2\_0</span></span> | <span data-ttu-id="dea38-145">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="dea38-145">2\_x</span></span> | <span data-ttu-id="dea38-146">2 \_ sw</span><span class="sxs-lookup"><span data-stu-id="dea38-146">2\_sw</span></span> | <span data-ttu-id="dea38-147">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="dea38-147">3\_0</span></span> | <span data-ttu-id="dea38-148">3 \_ sw</span><span class="sxs-lookup"><span data-stu-id="dea38-148">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="dea38-149">texld</span><span class="sxs-lookup"><span data-stu-id="dea38-149">texld</span></span>                 |      |      |      | <span data-ttu-id="dea38-150">x</span><span class="sxs-lookup"><span data-stu-id="dea38-150">x</span></span>    |      |      |       |      |       |



 

## <a name="examples"></a><span data-ttu-id="dea38-151">Exemplos</span><span class="sxs-lookup"><span data-stu-id="dea38-151">Examples</span></span>

<span data-ttu-id="dea38-152">A instrução texld oferece algum controle sobre quais componentes dos dados de coordenada de textura de origem são usados.</span><span class="sxs-lookup"><span data-stu-id="dea38-152">The texld instruction offers some control over which components of the source texture coordinate data are used.</span></span> <span data-ttu-id="dea38-153">O conjunto completo de sintaxe permitida para o texld segue e inclui todos os modificadores de registro de origem válidos, seletores e combinações de máscara de gravação.</span><span class="sxs-lookup"><span data-stu-id="dea38-153">The complete set of allowed syntax for texld follows, and includes all valid source register modifiers, selectors, and write mask combinations.</span></span>


```
texld  r(m), t(n).xyz
// Uses xyz from t(n) to sample 1D, 2D, or 3D texture
```




```
texld  r(m), t(n)
// Same as previous
```




```
texld  r(m), t(n).xyw
// Uses xyw (skipping z) from t(n) to sample 1D, 2D or 3D texture
```




```
texld  r(m), t(n)_dw.xyw  
// Samples 1D or 2D texture at x/w, y/w from t(n). The result
// is undefined for a cube-map lookup.
```




```
texld  r(m), r(n).xyz
// Samples 1D, 2D, or 3D texture at xyz from r(m) 
// This is possible in the second phase of the shader
```




```
texld  r(m), r(n)
// Same as previous
```




```
texld  r(m), r(n)_dz.xyz
// Samples 1D or 2D texture at x/z, y/z from r(m)
// Possible only in second phase
// The result is undefined for a cube-map lookup
```




```
texld  r(n), r(n)_dz
// Same as previous
```



## <a name="related-topics"></a><span data-ttu-id="dea38-154">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="dea38-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dea38-155">Instruções do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="dea38-155">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




