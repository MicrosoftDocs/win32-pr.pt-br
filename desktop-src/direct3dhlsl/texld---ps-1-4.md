---
title: texld-ps_1_4
description: Carrega o registro de destino com dados de cores (RGBA) amostrados usando o conteúdo do registro de origem como coordenadas de textura. A textura amostrada é a textura associada ao número de registro de destino.
ms.assetid: 1970aed4-4da7-40a1-960d-fba4dfd8c433
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ca305b16db0f390354962a3e959f08b6e956f2ef
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996863"
---
# <a name="texld---ps_1_4"></a><span data-ttu-id="76a13-104">texld-PS \_ 1 \_ 4</span><span class="sxs-lookup"><span data-stu-id="76a13-104">texld - ps\_1\_4</span></span>

<span data-ttu-id="76a13-105">Carrega o registro de destino com dados de cores (RGBA) amostrados usando o conteúdo do registro de origem como coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="76a13-105">Loads the destination register with color data (RGBA) sampled using the contents of the source register as texture coordinates.</span></span> <span data-ttu-id="76a13-106">A textura amostrada é a textura associada ao número de registro de destino.</span><span class="sxs-lookup"><span data-stu-id="76a13-106">The sampled texture is the texture associated with the destination register number.</span></span>



| <span data-ttu-id="76a13-107">texld DST, src</span><span class="sxs-lookup"><span data-stu-id="76a13-107">texld dst, src</span></span> |
|----------------|



 

## <a name="registers"></a><span data-ttu-id="76a13-108">Registros</span><span class="sxs-lookup"><span data-stu-id="76a13-108">Registers</span></span>



|          |                      | <span data-ttu-id="76a13-109">vn</span><span class="sxs-lookup"><span data-stu-id="76a13-109">vₙ</span></span>        | <span data-ttu-id="76a13-110">Hong</span><span class="sxs-lookup"><span data-stu-id="76a13-110">cₙ</span></span>  | <span data-ttu-id="76a13-111">TN</span><span class="sxs-lookup"><span data-stu-id="76a13-111">tₙ</span></span>  | <span data-ttu-id="76a13-112">RN</span><span class="sxs-lookup"><span data-stu-id="76a13-112">rₙ</span></span>  |              |
|----------|----------------------|-----------|-----|-----|-----|--------------|
| <span data-ttu-id="76a13-113">DST</span><span class="sxs-lookup"><span data-stu-id="76a13-113">dst</span></span>      | <span data-ttu-id="76a13-114">Registro de destino</span><span class="sxs-lookup"><span data-stu-id="76a13-114">Destination register</span></span> |           |     |     | <span data-ttu-id="76a13-115">x</span><span class="sxs-lookup"><span data-stu-id="76a13-115">x</span></span>   | <span data-ttu-id="76a13-116">1\_4</span><span class="sxs-lookup"><span data-stu-id="76a13-116">1\_4</span></span>         |
| <span data-ttu-id="76a13-117">src</span><span class="sxs-lookup"><span data-stu-id="76a13-117">src</span></span>      | <span data-ttu-id="76a13-118">Registro de origem</span><span class="sxs-lookup"><span data-stu-id="76a13-118">Source register</span></span>      |           |     | <span data-ttu-id="76a13-119">x</span><span class="sxs-lookup"><span data-stu-id="76a13-119">x</span></span>   |     | <span data-ttu-id="76a13-120">1 \_ 4 fase 1</span><span class="sxs-lookup"><span data-stu-id="76a13-120">1\_4 phase 1</span></span> |
|          |                      |           |     | <span data-ttu-id="76a13-121">x</span><span class="sxs-lookup"><span data-stu-id="76a13-121">x</span></span>   | <span data-ttu-id="76a13-122">x</span><span class="sxs-lookup"><span data-stu-id="76a13-122">x</span></span>   | <span data-ttu-id="76a13-123">\_fase 1 4</span><span class="sxs-lookup"><span data-stu-id="76a13-123">1\_4 phase</span></span>   |



 

<span data-ttu-id="76a13-124">Ao usar r (n) como um registro de origem, os três primeiros componentes (XYZ) devem ter sido inicializados na fase anterior do sombreador.</span><span class="sxs-lookup"><span data-stu-id="76a13-124">When using r(n) as a source register, the first three components (XYZ) must have been initialized in the previous phase of the shader.</span></span>

<span data-ttu-id="76a13-125">Para saber mais sobre os registros, consulte [PS \_ 1 1 PS 1 2 PS 1 3 PS 1 \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ 4 Registers](dx9-graphics-reference-asm-ps-registers-ps-1-x.md).</span><span class="sxs-lookup"><span data-stu-id="76a13-125">To learn more about registers, see [ps\_1\_1\_\_ps\_1\_2\_\_ps\_1\_3\_\_ps\_1\_4 Registers](dx9-graphics-reference-asm-ps-registers-ps-1-x.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="76a13-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="76a13-126">Remarks</span></span>

<span data-ttu-id="76a13-127">Esta instrução amostra a textura no estágio de textura associado ao número de registro de destino.</span><span class="sxs-lookup"><span data-stu-id="76a13-127">This instruction samples the texture in the texture stage associated with the destination register number.</span></span> <span data-ttu-id="76a13-128">A textura é amostrada usando dados de coordenadas de textura do registro de origem.</span><span class="sxs-lookup"><span data-stu-id="76a13-128">The texture is sampled using texture coordinate data from the source register.</span></span>

<span data-ttu-id="76a13-129">A sintaxe das instruções texld e texcrd expõe o suporte para uma divisão projetada com um modificador de registro de textura.</span><span class="sxs-lookup"><span data-stu-id="76a13-129">The syntax for the texld and texcrd instructions expose support for a projective divide with a Texture Register Modifier.</span></span> <span data-ttu-id="76a13-130">Para o sombreador de pixel versão 1,4, o \_ sinalizador de transformação de textura projetada D3DTTFF é sempre ignorado.</span><span class="sxs-lookup"><span data-stu-id="76a13-130">For pixel shader version 1.4, the D3DTTFF\_PROJECTED texture transform flag is always ignored.</span></span>

<span data-ttu-id="76a13-131">Regras para usar texld:</span><span class="sxs-lookup"><span data-stu-id="76a13-131">Rules for using texld:</span></span>

1.  <span data-ttu-id="76a13-132">O mesmo modificador. xyz ou. xyw deve ser aplicado a cada leitura de um t (n) registro individual em ambas as instruções texcrd ou texld.</span><span class="sxs-lookup"><span data-stu-id="76a13-132">The same .xyz or .xyw modifier must be applied to every read of an individual t(n) register within both texcrd or texld instructions.</span></span> <span data-ttu-id="76a13-133">Se. xyw estiver sendo usado nas leituras de registro t (n), isso poderá ser misturado com outras leituras do mesmo registro t (n) usando. xyw \_ DW.</span><span class="sxs-lookup"><span data-stu-id="76a13-133">If .xyw is being used on t(n) register reads, this can be mixed with other reads of the same t(n) register using .xyw\_dw.</span></span>
2.  <span data-ttu-id="76a13-134">O \_ modificador de origem DZ só é válido em texld com o registro de origem r (n) (portanto, fase 2 somente).</span><span class="sxs-lookup"><span data-stu-id="76a13-134">The \_dz source modifier is only valid on texld with r(n) source register (thus phase 2 only).</span></span>
3.  <span data-ttu-id="76a13-135">O \_ modificador de origem DZ pode ser usado não mais do que duas vezes por sombreador.</span><span class="sxs-lookup"><span data-stu-id="76a13-135">The \_dz source modifier may be used no more than two times per shader.</span></span>



| <span data-ttu-id="76a13-136">Versões do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="76a13-136">Pixel shader versions</span></span> | <span data-ttu-id="76a13-137">1\_1</span><span class="sxs-lookup"><span data-stu-id="76a13-137">1\_1</span></span> | <span data-ttu-id="76a13-138">1\_2</span><span class="sxs-lookup"><span data-stu-id="76a13-138">1\_2</span></span> | <span data-ttu-id="76a13-139">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="76a13-139">1\_3</span></span> | <span data-ttu-id="76a13-140">1\_4</span><span class="sxs-lookup"><span data-stu-id="76a13-140">1\_4</span></span> | <span data-ttu-id="76a13-141">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="76a13-141">2\_0</span></span> | <span data-ttu-id="76a13-142">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="76a13-142">2\_x</span></span> | <span data-ttu-id="76a13-143">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="76a13-143">2\_sw</span></span> | <span data-ttu-id="76a13-144">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="76a13-144">3\_0</span></span> | <span data-ttu-id="76a13-145">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="76a13-145">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="76a13-146">texld</span><span class="sxs-lookup"><span data-stu-id="76a13-146">texld</span></span>                 |      |      |      | <span data-ttu-id="76a13-147">x</span><span class="sxs-lookup"><span data-stu-id="76a13-147">x</span></span>    |      |      |       |      |       |



 

## <a name="examples"></a><span data-ttu-id="76a13-148">Exemplos</span><span class="sxs-lookup"><span data-stu-id="76a13-148">Examples</span></span>

<span data-ttu-id="76a13-149">A instrução texld oferece algum controle sobre quais componentes dos dados de coordenadas de textura de origem são usados.</span><span class="sxs-lookup"><span data-stu-id="76a13-149">The texld instruction offers some control over which components of the source texture coordinate data are used.</span></span> <span data-ttu-id="76a13-150">O conjunto completo de sintaxe permitida para texld segue e inclui todos os modificadores de registro de origem válidos, seletores e combinações de máscara de gravação.</span><span class="sxs-lookup"><span data-stu-id="76a13-150">The complete set of allowed syntax for texld follows, and includes all valid source register modifiers, selectors, and write mask combinations.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="76a13-151">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="76a13-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="76a13-152">Instruções do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="76a13-152">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




