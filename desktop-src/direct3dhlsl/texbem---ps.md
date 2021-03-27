---
title: texbem-PS
description: Aplicar um ambiente de relevo falso – transformação de mapa. Isso é feito modificando os dados de endereço de textura do registro de destino, usando o endereço muito data (du, DV) e uma matriz de ambiente de relevo 2D.
ms.assetid: 8e773f4a-c7a2-4caf-973f-8f50dccc9c04
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f026819b268836fd7d4c1d550033ceefdf0bbbf9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104967186"
---
# <a name="texbem---ps"></a><span data-ttu-id="123e4-104">texbem-PS</span><span class="sxs-lookup"><span data-stu-id="123e4-104">texbem - ps</span></span>

<span data-ttu-id="123e4-105">Aplicar um ambiente de relevo falso – transformação de mapa.</span><span class="sxs-lookup"><span data-stu-id="123e4-105">Apply a fake bump environment-map transform.</span></span> <span data-ttu-id="123e4-106">Isso é feito modificando os dados de endereço de textura do registro de destino, usando o endereço muito data (du, DV) e uma matriz de ambiente de relevo 2D.</span><span class="sxs-lookup"><span data-stu-id="123e4-106">This is accomplished by modifying the texture address data of the destination register, using address perturbation data (du,dv), and a 2D bump environment matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="123e4-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="123e4-107">Syntax</span></span>



| <span data-ttu-id="123e4-108">texbem DST, src</span><span class="sxs-lookup"><span data-stu-id="123e4-108">texbem dst, src</span></span> |
|-----------------|



 

<span data-ttu-id="123e4-109">onde</span><span class="sxs-lookup"><span data-stu-id="123e4-109">where</span></span>

-   <span data-ttu-id="123e4-110">DST é o registro de destino.</span><span class="sxs-lookup"><span data-stu-id="123e4-110">dst is the destination register.</span></span>
-   <span data-ttu-id="123e4-111">src é um registro de origem.</span><span class="sxs-lookup"><span data-stu-id="123e4-111">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="123e4-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="123e4-112">Remarks</span></span>



| <span data-ttu-id="123e4-113">Versões do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="123e4-113">Pixel shader versions</span></span> | <span data-ttu-id="123e4-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="123e4-114">1\_1</span></span> | <span data-ttu-id="123e4-115">1\_2</span><span class="sxs-lookup"><span data-stu-id="123e4-115">1\_2</span></span> | <span data-ttu-id="123e4-116">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="123e4-116">1\_3</span></span> | <span data-ttu-id="123e4-117">1\_4</span><span class="sxs-lookup"><span data-stu-id="123e4-117">1\_4</span></span> | <span data-ttu-id="123e4-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="123e4-118">2\_0</span></span> | <span data-ttu-id="123e4-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="123e4-119">2\_x</span></span> | <span data-ttu-id="123e4-120">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="123e4-120">2\_sw</span></span> | <span data-ttu-id="123e4-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="123e4-121">3\_0</span></span> | <span data-ttu-id="123e4-122">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="123e4-122">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="123e4-123">texbem</span><span class="sxs-lookup"><span data-stu-id="123e4-123">texbem</span></span>                | <span data-ttu-id="123e4-124">x</span><span class="sxs-lookup"><span data-stu-id="123e4-124">x</span></span>    | <span data-ttu-id="123e4-125">x</span><span class="sxs-lookup"><span data-stu-id="123e4-125">x</span></span>    | <span data-ttu-id="123e4-126">x</span><span class="sxs-lookup"><span data-stu-id="123e4-126">x</span></span>    |      |      |      |       |      |       |



 

<span data-ttu-id="123e4-127">Os dados de cor vermelho e verde no registro src são interpretados como os dados de muito (du, DV).</span><span class="sxs-lookup"><span data-stu-id="123e4-127">The red and green color data in the src register is interpreted as the perturbation data (du,dv).</span></span>

<span data-ttu-id="123e4-128">Essa instrução transforma os componentes vermelho e verde no registro de origem usando a matriz de mapeamento do ambiente de choque 2D.</span><span class="sxs-lookup"><span data-stu-id="123e4-128">This instruction transforms red and green components in the source register using the 2D bump environment-mapping matrix.</span></span> <span data-ttu-id="123e4-129">O resultado é adicionado ao conjunto de coordenadas de textura correspondente ao número de registro de destino e é usado para exemplificar o estágio de textura atual.</span><span class="sxs-lookup"><span data-stu-id="123e4-129">The result is added to the texture coordinate set corresponding to the destination register number, and is used to sample the current texture stage.</span></span>

<span data-ttu-id="123e4-130">Essa operação sempre interpreta du e DV como quantidades assinadas.</span><span class="sxs-lookup"><span data-stu-id="123e4-130">This operation always interprets du and dv as signed quantities.</span></span> <span data-ttu-id="123e4-131">Para as versões 1 \_ e 1 \_ 1, o modificador de entrada de [dimensionamento assinado do registro de origem](dx9-graphics-reference-asm-ps-registers-modifiers-signed-scale.md) ( \_ BX2) não é permitido no argumento de entrada.</span><span class="sxs-lookup"><span data-stu-id="123e4-131">For versions 1\_0 and 1\_1, the [Source Register Signed Scaling](dx9-graphics-reference-asm-ps-registers-modifiers-signed-scale.md) input modifier (\_bx2) is not permitted on the input argument.</span></span>

<span data-ttu-id="123e4-132">Essa instrução produz resultados definidos quando as texturas de entrada contêm dados de formato assinado.</span><span class="sxs-lookup"><span data-stu-id="123e4-132">This instruction produces defined results when input textures contain signed format data.</span></span> <span data-ttu-id="123e4-133">Os dados de formato misto só funcionarão se os dois primeiros canais contiverem dados assinados.</span><span class="sxs-lookup"><span data-stu-id="123e4-133">Mixed format data works only if the first two channels contain signed data.</span></span> <span data-ttu-id="123e4-134">Para obter mais informações sobre formatos de superfície, consulte [D3DFORMAT](/windows/desktop/direct3d9/d3dformat).</span><span class="sxs-lookup"><span data-stu-id="123e4-134">For more information about surface formats, see [D3DFORMAT](/windows/desktop/direct3d9/d3dformat).</span></span>

<span data-ttu-id="123e4-135">Isso pode ser usado para uma variedade de técnicas com base no endereço muito, incluindo mapeamento de ambiente falso por pixel e iluminação difusa (mapeamento de choque).</span><span class="sxs-lookup"><span data-stu-id="123e4-135">This can be used for a variety of techniques based on address perturbation, including fake per-pixel environment mapping and diffuse lighting (bump mapping).</span></span>

<span data-ttu-id="123e4-136">Ao usar essa instrução, os registros de textura devem seguir a sequência a seguir.</span><span class="sxs-lookup"><span data-stu-id="123e4-136">When using this instruction, texture registers must follow the following sequence.</span></span>


```
// The texture assigned to stage t(n) contains the (du,dv) data
// The texture assigned to stage t(m) is sampled
tex     t(n)                    
texbem  t(m),  t(n)      where m > n
```



<span data-ttu-id="123e4-137">Os cálculos feitos dentro da instrução são mostrados abaixo.</span><span class="sxs-lookup"><span data-stu-id="123e4-137">The calculations done within the instruction are shown below.</span></span>


```
// 1. New values for texture addresses (u',v') are calculated
// 2. Sample the texture using (u',v')
```



<span data-ttu-id="123e4-138">u ' = TextureCoordinates (estágio m)<sub>u</sub> + D3DTSS \_ BUMPENVMAT00 (estágio m) \* t (n)<sub>R</sub> + D3DTSS \_ BUMPENVMAT10 (estágio m) \* t (n)<sub>G</sub> v ' = TextureCoordinates (estágio m)<sub>v</sub> + D3DTSS \_ BUMPENVMAT01 (estágio m) \* t (n)<sub>R</sub> + D3DTSS \_ BUMPENVMAT11 (estágio m) \* t (n)<sub>G</sub> t (m)<sub>RGBA</sub> = TextureSample (etapa m)</span><span class="sxs-lookup"><span data-stu-id="123e4-138">u' = TextureCoordinates(stage m)<sub>u</sub> + D3DTSS\_BUMPENVMAT00(stage m)\*t(n)<sub>R</sub> + D3DTSS\_BUMPENVMAT10(stage m)\*t(n)<sub>G</sub> v' = TextureCoordinates(stage m)<sub>v</sub> + D3DTSS\_BUMPENVMAT01(stage m)\*t(n)<sub>R</sub> + D3DTSS\_BUMPENVMAT11(stage m)\*t(n)<sub>G</sub> t(m)<sub>RGBA</sub> = TextureSample(stage m)</span></span>

<span data-ttu-id="123e4-139">usando (u ', v ') como coordenadas</span><span class="sxs-lookup"><span data-stu-id="123e4-139">// using (u',v') as coordinates</span></span>

<span data-ttu-id="123e4-140">Os dados de registro que foram lidos por uma instrução texbem-PS ou [texbeml-PS](texbeml---ps.md) não podem ser lidos mais tarde, exceto por outro texbem-PS ou texbeml-PS.</span><span class="sxs-lookup"><span data-stu-id="123e4-140">Register data that has been read by a texbem - ps or [texbeml - ps](texbeml---ps.md) instruction cannot be read later, except by another texbem - ps or texbeml - ps.</span></span>


```
// This example demonstrates the validation error caused by t0 being reread:
ps_1_1
tex t0
texbem t1, t0
add r0, t1, t0

(Instruction Error) (Statement 4) Register data that has been read by 
texbem or texbeml instruction cannot be read by other instructions
```



## <a name="examples"></a><span data-ttu-id="123e4-141">Exemplos</span><span class="sxs-lookup"><span data-stu-id="123e4-141">Examples</span></span>

<span data-ttu-id="123e4-142">Aqui está um sombreador de exemplo com os mapas de textura identificados e os estágios de textura identificados.</span><span class="sxs-lookup"><span data-stu-id="123e4-142">Here is an example shader with the texture maps identified and the texture stages identified.</span></span>


```
ps_1_1
tex t0              ; Define t0 to get a 2-tuple DuDv
texbem t1, t0       ; Compute (u',v')
                    ; Sample t1 using (u',v')
mov r0, t1          ; Output result
```



<span data-ttu-id="123e4-143">texbem requer as seguintes texturas nos seguintes estágios de textura.</span><span class="sxs-lookup"><span data-stu-id="123e4-143">texbem requires the following textures in the following texture stages.</span></span>

-   <span data-ttu-id="123e4-144">O estágio 0 recebe um mapa de relevo com os dados (du, DV) muito.</span><span class="sxs-lookup"><span data-stu-id="123e4-144">Stage 0 is assigned a bump map with (du, dv) perturbation data.</span></span>
-   <span data-ttu-id="123e4-145">O estágio 1 usa um mapa de textura com dados de cores.</span><span class="sxs-lookup"><span data-stu-id="123e4-145">Stage 1 uses a texture map with color data.</span></span>
-   <span data-ttu-id="123e4-146">Essa instrução define os dados de matriz no estágio de textura que é amostrado.</span><span class="sxs-lookup"><span data-stu-id="123e4-146">This instruction sets the matrix data on the texture stage that is sampled.</span></span>
-   <span data-ttu-id="123e4-147">Isso é diferente da funcionalidade do pipeline de função fixa em que os dados muito e as matrizes ocupam o mesmo estágio de textura.</span><span class="sxs-lookup"><span data-stu-id="123e4-147">This is different from the functionality of the fixed function pipeline where the perturbation data and the matrices occupy the same texture stage.</span></span>

## <a name="related-topics"></a><span data-ttu-id="123e4-148">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="123e4-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="123e4-149">Instruções do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="123e4-149">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 