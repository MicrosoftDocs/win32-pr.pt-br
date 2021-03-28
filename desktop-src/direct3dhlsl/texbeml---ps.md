---
title: texbeml-PS
description: Aplicar um ambiente de relevo falso – mapear transformação com correção de luminância. Isso é feito modificando os dados de endereço de textura do registro de destino, usando o endereço muito data (du, DV), uma matriz de ambiente de choque 2D e uma luminância.
ms.assetid: 345a0b77-8d4e-4a0b-a31a-1153f8cb5961
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d97877c67970f43a995fcfbe21d9aead2d792e09
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103917629"
---
# <a name="texbeml---ps"></a><span data-ttu-id="4006d-104">texbeml-PS</span><span class="sxs-lookup"><span data-stu-id="4006d-104">texbeml - ps</span></span>

<span data-ttu-id="4006d-105">Aplicar um ambiente de relevo falso – mapear transformação com correção de luminância.</span><span class="sxs-lookup"><span data-stu-id="4006d-105">Apply a fake bump environment-map transform with luminance correction.</span></span> <span data-ttu-id="4006d-106">Isso é feito modificando os dados de endereço de textura do registro de destino, usando o endereço muito data (du, DV), uma matriz de ambiente de choque 2D e uma luminância.</span><span class="sxs-lookup"><span data-stu-id="4006d-106">This is accomplished by modifying the texture address data of the destination register, using address perturbation data (du,dv), a 2D bump environment matrix, and luminance.</span></span>

## <a name="syntax"></a><span data-ttu-id="4006d-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="4006d-107">Syntax</span></span>



| <span data-ttu-id="4006d-108">texbeml DST, src</span><span class="sxs-lookup"><span data-stu-id="4006d-108">texbeml dst, src</span></span> |
|------------------|



 

<span data-ttu-id="4006d-109">onde</span><span class="sxs-lookup"><span data-stu-id="4006d-109">where</span></span>

-   <span data-ttu-id="4006d-110">DST é o registro de destino.</span><span class="sxs-lookup"><span data-stu-id="4006d-110">dst is the destination register.</span></span>
-   <span data-ttu-id="4006d-111">src é um registro de origem.</span><span class="sxs-lookup"><span data-stu-id="4006d-111">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="4006d-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="4006d-112">Remarks</span></span>



| <span data-ttu-id="4006d-113">Versões do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="4006d-113">Pixel shader versions</span></span> | <span data-ttu-id="4006d-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="4006d-114">1\_1</span></span> | <span data-ttu-id="4006d-115">1\_2</span><span class="sxs-lookup"><span data-stu-id="4006d-115">1\_2</span></span> | <span data-ttu-id="4006d-116">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="4006d-116">1\_3</span></span> | <span data-ttu-id="4006d-117">1\_4</span><span class="sxs-lookup"><span data-stu-id="4006d-117">1\_4</span></span> | <span data-ttu-id="4006d-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="4006d-118">2\_0</span></span> | <span data-ttu-id="4006d-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="4006d-119">2\_x</span></span> | <span data-ttu-id="4006d-120">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="4006d-120">2\_sw</span></span> | <span data-ttu-id="4006d-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="4006d-121">3\_0</span></span> | <span data-ttu-id="4006d-122">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="4006d-122">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="4006d-123">texbeml</span><span class="sxs-lookup"><span data-stu-id="4006d-123">texbeml</span></span>               | <span data-ttu-id="4006d-124">x</span><span class="sxs-lookup"><span data-stu-id="4006d-124">x</span></span>    | <span data-ttu-id="4006d-125">x</span><span class="sxs-lookup"><span data-stu-id="4006d-125">x</span></span>    | <span data-ttu-id="4006d-126">x</span><span class="sxs-lookup"><span data-stu-id="4006d-126">x</span></span>    |      |      |      |       |      |       |



 

<span data-ttu-id="4006d-127">Os dados de cor vermelho e verde no registro src são interpretados como os dados de muito (du, DV).</span><span class="sxs-lookup"><span data-stu-id="4006d-127">The red and green color data in the src register is interpreted as the perturbation data (du,dv).</span></span> <span data-ttu-id="4006d-128">Os dados de cor azul no registro src são interpretados como os dados de luminância.</span><span class="sxs-lookup"><span data-stu-id="4006d-128">The blue color data in the src register is interpreted as the luminance data.</span></span>

<span data-ttu-id="4006d-129">Essa instrução transforma os componentes vermelho e verde no registro de origem usando a matriz de mapeamento de ambiente de choque 2D.</span><span class="sxs-lookup"><span data-stu-id="4006d-129">This instruction transforms the red and green components in the source register using the 2D bump environment mapping matrix.</span></span> <span data-ttu-id="4006d-130">O resultado é adicionado ao conjunto de coordenadas de textura correspondente ao número de registro de destino.</span><span class="sxs-lookup"><span data-stu-id="4006d-130">The result is added to the texture coordinate set corresponding to the destination register number.</span></span> <span data-ttu-id="4006d-131">Uma correção de luminância é aplicada usando o valor de luminância e os valores de estágio de textura de tendência.</span><span class="sxs-lookup"><span data-stu-id="4006d-131">A luminance correction is applied using the luminance value and the bias texture stage values.</span></span> <span data-ttu-id="4006d-132">O resultado é usado para exemplificar o estágio de textura atual.</span><span class="sxs-lookup"><span data-stu-id="4006d-132">The result is used to sample the current texture stage.</span></span>

<span data-ttu-id="4006d-133">Isso pode ser usado para uma variedade de técnicas com base no endereço muito, como o mapeamento de ambiente falso por pixel.</span><span class="sxs-lookup"><span data-stu-id="4006d-133">This can be used for a variety of techniques based on address perturbation such as fake per-pixel environment mapping.</span></span>

<span data-ttu-id="4006d-134">Essa operação sempre interpreta du e DV como quantidades assinadas.</span><span class="sxs-lookup"><span data-stu-id="4006d-134">This operation always interprets du and dv as signed quantities.</span></span> <span data-ttu-id="4006d-135">Para as versões 1 \_ e 1 \_ 1, o modificador de entrada de [dimensionamento assinado do registro de origem](dx9-graphics-reference-asm-ps-registers-modifiers-signed-scale.md) ( \_ BX2) não é permitido no argumento de entrada.</span><span class="sxs-lookup"><span data-stu-id="4006d-135">For versions 1\_0 and 1\_1, the [Source Register Signed Scaling](dx9-graphics-reference-asm-ps-registers-modifiers-signed-scale.md) input modifier (\_bx2) is not permitted on the input argument.</span></span>

<span data-ttu-id="4006d-136">Essa instrução produz resultados definidos quando texturas de entrada contêm dados de formato misto.</span><span class="sxs-lookup"><span data-stu-id="4006d-136">This instruction produces defined results when input textures contain mixed format data.</span></span> <span data-ttu-id="4006d-137">Para obter mais informações sobre formatos de superfície, consulte [D3DFORMAT](/windows/desktop/direct3d9/d3dformat).</span><span class="sxs-lookup"><span data-stu-id="4006d-137">For more information about surface formats, see [D3DFORMAT](/windows/desktop/direct3d9/d3dformat).</span></span>


```
// When using this instruction, texture registers must follow 
//   the following sequence:
// The texture assigned to stage tn contains the (du,dv) data
// The texture assigned to stage t(m) is sampled
tex     t(n)                    
texbeml t(m),  t(n)      where m > n
```



<span data-ttu-id="4006d-138">Este exemplo mostra os cálculos feitos dentro da instrução.</span><span class="sxs-lookup"><span data-stu-id="4006d-138">This example shows the calculations done within the instruction.</span></span>


```
// 1. New values for texture addresses (u',v') are calculated
// 2. Sample the texture using (u',v')
// 3. Luminance correction is applied
```



<span data-ttu-id="4006d-139">u ' = TextureCoordinates (estágio m)<sub>u</sub> +</span><span class="sxs-lookup"><span data-stu-id="4006d-139">u' = TextureCoordinates(stage m)<sub>u</sub> +</span></span>

<span data-ttu-id="4006d-140">D3DTSS \_ BUMPENVMAT00 (estágio m) \* t (n)<sub>R</sub> +</span><span class="sxs-lookup"><span data-stu-id="4006d-140">D3DTSS\_BUMPENVMAT00(stage m)\*t(n)<sub>R</sub> +</span></span>

<span data-ttu-id="4006d-141">D3DTSS \_ BUMPENVMAT10 (estágio m) \* t (n)<sub>G</sub></span><span class="sxs-lookup"><span data-stu-id="4006d-141">D3DTSS\_BUMPENVMAT10(stage m)\*t(n)<sub>G</sub></span></span>

<span data-ttu-id="4006d-142">v ' = TextureCoordinates (estágio m)<sub>v</sub> +</span><span class="sxs-lookup"><span data-stu-id="4006d-142">v' = TextureCoordinates(stage m)<sub>v</sub> +</span></span>

<span data-ttu-id="4006d-143">D3DTSS \_ BUMPENVMAT01 (estágio m) \* t (n)<sub>R</sub> +</span><span class="sxs-lookup"><span data-stu-id="4006d-143">D3DTSS\_BUMPENVMAT01(stage m)\*t(n)<sub>R</sub> +</span></span>

<span data-ttu-id="4006d-144">D3DTSS \_ BUMPENVMAT11 (estágio m) \* t (n)<sub>G</sub></span><span class="sxs-lookup"><span data-stu-id="4006d-144">D3DTSS\_BUMPENVMAT11(stage m)\*t(n)<sub>G</sub></span></span>

<span data-ttu-id="4006d-145">t (m)<sub>RGBA</sub> = TextureSample (estágio m) usando (u ', v ') como coordenadas</span><span class="sxs-lookup"><span data-stu-id="4006d-145">t(m)<sub>RGBA</sub> = TextureSample(stage m) using (u',v') as coordinates</span></span>

<span data-ttu-id="4006d-146">t (m)<sub>RGBA</sub> = t (m)<sub>RGBA</sub>\*</span><span class="sxs-lookup"><span data-stu-id="4006d-146">t(m)<sub>RGBA</sub> = t(m)<sub>RGBA</sub> \*</span></span>

<span data-ttu-id="4006d-147">\[(t (n)<sub>B</sub> \* D3DTSS \_ BUMPENVLSCALE (estágio m)) +</span><span class="sxs-lookup"><span data-stu-id="4006d-147">\[(t(n)<sub>B</sub> \* D3DTSS\_BUMPENVLSCALE(stage m)) +</span></span>

<span data-ttu-id="4006d-148">D3DTSS \_ BUMPENVLOFFSET (estágio m)\]</span><span class="sxs-lookup"><span data-stu-id="4006d-148">D3DTSS\_BUMPENVLOFFSET(stage m)\]</span></span>

<span data-ttu-id="4006d-149">Os dados de registro que foram lidos por uma instrução [texbem](texbem---ps.md) ou texbeml não podem ser lidos mais tarde, exceto por outro texbem ou texbeml.</span><span class="sxs-lookup"><span data-stu-id="4006d-149">Register data that has been read by a [texbem](texbem---ps.md) or texbeml instruction cannot be read later, except by another texbem or texbeml.</span></span>


```
// This example demonstrates the validation error caused by 
//   t0 being reread
ps_1_1
tex t0
texbem t1, t0
add r0, t1, t0

(Instruction Error) (Statement 4) Register data that has been read by 
texbem or texbeml instruction cannot be read by other instructions
```



## <a name="examples"></a><span data-ttu-id="4006d-150">Exemplos</span><span class="sxs-lookup"><span data-stu-id="4006d-150">Examples</span></span>

<span data-ttu-id="4006d-151">Aqui está um sombreador de exemplo com os mapas de textura identificados e os estágios de textura identificados.</span><span class="sxs-lookup"><span data-stu-id="4006d-151">Here is an example shader with the texture maps identified and the texture stages identified.</span></span>


```
ps_1_1
tex t0              ; Define t0 to get a 2-tuple DuDv
texbeml t1, t0      ; Compute (u',v')
                    ; Apply luminance correction                    
                    ; Sample t1 using (u',v')
mov r0, t1          ; Output result
```



<span data-ttu-id="4006d-152">Este exemplo requer as seguintes texturas nos seguintes estágios de textura.</span><span class="sxs-lookup"><span data-stu-id="4006d-152">This example requires the following textures in the following texture stages.</span></span>

-   <span data-ttu-id="4006d-153">O estágio 0 recebe um mapa de relevo com os dados (du, DV) muito.</span><span class="sxs-lookup"><span data-stu-id="4006d-153">Stage 0 is assigned a bump map with (du, dv) perturbation data.</span></span>
-   <span data-ttu-id="4006d-154">O estágio 1 recebe um mapa de textura com dados de cores.</span><span class="sxs-lookup"><span data-stu-id="4006d-154">Stage 1 is assigned a texture map with color data.</span></span>
-   <span data-ttu-id="4006d-155">texbeml define os dados de matriz no estágio de textura que é amostrado.</span><span class="sxs-lookup"><span data-stu-id="4006d-155">texbeml sets the matrix data on the texture stage that is sampled.</span></span> <span data-ttu-id="4006d-156">Isso é diferente da funcionalidade do pipeline de função fixa em que os dados muito e as matrizes ocupam o mesmo estágio de textura.</span><span class="sxs-lookup"><span data-stu-id="4006d-156">This is different from the functionality of the fixed function pipeline where the perturbation data and the matrices occupy the same texture stage.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4006d-157">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4006d-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4006d-158">Instruções do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="4006d-158">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 