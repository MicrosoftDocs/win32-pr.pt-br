---
title: texcrd-PS
description: Copia dados de coordenadas de textura do iterador de coordenadas de origem registrar como dados de cores no registro de destino.
ms.assetid: b3330d70-6e18-4494-a01c-51f0a282e305
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e1b7bda7ab06c4af43eaa40393d2c5d64b09d9f4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104988663"
---
# <a name="texcrd---ps"></a><span data-ttu-id="f7cd2-103">texcrd-PS</span><span class="sxs-lookup"><span data-stu-id="f7cd2-103">texcrd - ps</span></span>

<span data-ttu-id="f7cd2-104">Copia dados de coordenadas de textura do iterador de coordenadas de origem registrar como dados de cores no registro de destino.</span><span class="sxs-lookup"><span data-stu-id="f7cd2-104">Copies texture coordinate data from the source texture coordinate iterator register as color data in the destination register.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7cd2-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f7cd2-105">Syntax</span></span>



| <span data-ttu-id="f7cd2-106">texcrd DST, src</span><span class="sxs-lookup"><span data-stu-id="f7cd2-106">texcrd dst, src</span></span> |
|-----------------|



 

<span data-ttu-id="f7cd2-107">onde</span><span class="sxs-lookup"><span data-stu-id="f7cd2-107">where</span></span>

-   <span data-ttu-id="f7cd2-108">DST é o registro de destino.</span><span class="sxs-lookup"><span data-stu-id="f7cd2-108">dst is the destination register.</span></span>
-   <span data-ttu-id="f7cd2-109">src é um registro de origem.</span><span class="sxs-lookup"><span data-stu-id="f7cd2-109">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="f7cd2-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="f7cd2-110">Remarks</span></span>



| <span data-ttu-id="f7cd2-111">Versões do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="f7cd2-111">Pixel shader versions</span></span> | <span data-ttu-id="f7cd2-112">1\_1</span><span class="sxs-lookup"><span data-stu-id="f7cd2-112">1\_1</span></span> | <span data-ttu-id="f7cd2-113">1\_2</span><span class="sxs-lookup"><span data-stu-id="f7cd2-113">1\_2</span></span> | <span data-ttu-id="f7cd2-114">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="f7cd2-114">1\_3</span></span> | <span data-ttu-id="f7cd2-115">1\_4</span><span class="sxs-lookup"><span data-stu-id="f7cd2-115">1\_4</span></span> | <span data-ttu-id="f7cd2-116">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="f7cd2-116">2\_0</span></span> | <span data-ttu-id="f7cd2-117">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="f7cd2-117">2\_x</span></span> | <span data-ttu-id="f7cd2-118">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="f7cd2-118">2\_sw</span></span> | <span data-ttu-id="f7cd2-119">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="f7cd2-119">3\_0</span></span> | <span data-ttu-id="f7cd2-120">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="f7cd2-120">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="f7cd2-121">texcrd</span><span class="sxs-lookup"><span data-stu-id="f7cd2-121">texcrd</span></span>                |      |      |      | <span data-ttu-id="f7cd2-122">x</span><span class="sxs-lookup"><span data-stu-id="f7cd2-122">x</span></span>    |      |      |       |      |       |



 

<span data-ttu-id="f7cd2-123">Essa instrução interpreta os dados de coordenadas como dados de cores (RGBA).</span><span class="sxs-lookup"><span data-stu-id="f7cd2-123">This instruction interprets coordinate data as color data (RGBA).</span></span>

<span data-ttu-id="f7cd2-124">Nenhuma textura é amostrada por essa instrução.</span><span class="sxs-lookup"><span data-stu-id="f7cd2-124">No texture is sampled by this instruction.</span></span> <span data-ttu-id="f7cd2-125">Somente as coordenadas de textura definidas neste estágio de textura são relevantes.</span><span class="sxs-lookup"><span data-stu-id="f7cd2-125">Only texture coordinates set on this texture stage are relevant.</span></span>

<span data-ttu-id="f7cd2-126">Ao usar o texcrd, tenha em mente os detalhes a seguir sobre como os dados são copiados do registro de origem para o registro de destino.</span><span class="sxs-lookup"><span data-stu-id="f7cd2-126">When using texcrd, keep in mind the following detail about how data is copied from the source register to the destination register.</span></span> <span data-ttu-id="f7cd2-127">O registro de coordenadas de textura de origem (t \# ) contém dados no intervalo \[ -D3DCAPS9. MaxTextureRepeat, D3DCAPS9. MaxTextureRepeat \] , enquanto o registro de destino (r \# ) pode armazenar dados somente no intervalo (provavelmente menor) \[ -D3DCAPS9. PixelShader1xMaxValue, D3DCAPS9. PixelShader1xMaxValue \] .</span><span class="sxs-lookup"><span data-stu-id="f7cd2-127">The source texture coordinate register (t\#) holds data in the range \[-D3DCAPS9.MaxTextureRepeat, D3DCAPS9.MaxTextureRepeat\], while the destination register (r\#) can hold data only in the (likely smaller) range \[-D3DCAPS9.PixelShader1xMaxValue, D3DCAPS9.PixelShader1xMaxValue\].</span></span> <span data-ttu-id="f7cd2-128">Observe que para o sombreador de pixel versão 1 \_ 4, D3DCAPS9. PixelShader1xMaxValue deve ser um mínimo de oito.</span><span class="sxs-lookup"><span data-stu-id="f7cd2-128">Note that for pixel shader version 1\_4, D3DCAPS9.PixelShader1xMaxValue must be a minimum of eight.</span></span> <span data-ttu-id="f7cd2-129">A instrução texcrd, no processo de dados de origem fixação MSS que está fora do alcance do registro de destino, provavelmente se comportará de forma diferente em um hardware diferente.</span><span class="sxs-lookup"><span data-stu-id="f7cd2-129">The texcrd instruction, in the process of clamping source data that is out of range of the destination register, is likely to behave differently on different hardware.</span></span> <span data-ttu-id="f7cd2-130">O primeiro pixel shader versão 1 \_ 4 hardware no mercado executará um fixe especial para valores fora do intervalo.</span><span class="sxs-lookup"><span data-stu-id="f7cd2-130">The first pixel shader version 1\_4 hardware on the market will perform a special clamp for values outside of range.</span></span> <span data-ttu-id="f7cd2-131">Esse fixe foi projetado para produzir um número que possa se ajustar ao registro de destino, mas também para preservar o comportamento de endereçamento de textura para dados fora do intervalo (consulte [**D3DTEXTUREADDRESS**](/windows/desktop/direct3d9/d3dtextureaddress)) se os dados forem usados posteriormente para amostragem de textura.</span><span class="sxs-lookup"><span data-stu-id="f7cd2-131">This clamp is designed to produce a number that can fit into the destination register, but also to preserve texture addressing behavior for out-of-range data (see [**D3DTEXTUREADDRESS**](/windows/desktop/direct3d9/d3dtextureaddress)) if the data were to be subsequently used for texture sampling.</span></span> <span data-ttu-id="f7cd2-132">No entanto, um novo hardware de fabricantes diferentes pode não apresentar esse comportamento e pode apenas Chop dados para se ajustarem ao intervalo de registro de destino.</span><span class="sxs-lookup"><span data-stu-id="f7cd2-132">However, new hardware from different manufacturers might not exhibit this behavior and might just chop data to fit the destination register range.</span></span> <span data-ttu-id="f7cd2-133">Portanto, o curso de ação mais seguro ao usar o sombreador de pixel versão 1 \_ 4 texcrd é fornecer dados de coordenadas de textura apenas para o sombreador de pixel que já está dentro do intervalo \[ de 8, oito \] para que você não confie na maneira como o hardware coloca.</span><span class="sxs-lookup"><span data-stu-id="f7cd2-133">Therefore, the safest course of action when using pixel shader version 1\_4 texcrd is to supply texture coordinate data only into the pixel shader that is already within the range \[-8,8\] so that you do not rely on the way hardware clamps.</span></span>

<span data-ttu-id="f7cd2-134">Ao contrário \_ de texcoord, texcrd não fixe valores entre 0 e 1.</span><span class="sxs-lookup"><span data-stu-id="f7cd2-134">Unlike texcoord\_, texcrd does not clamp values between 0 and 1.</span></span>

<span data-ttu-id="f7cd2-135">Regras para usar texcrd:</span><span class="sxs-lookup"><span data-stu-id="f7cd2-135">Rules for using texcrd :</span></span>

1.  <span data-ttu-id="f7cd2-136">O mesmo modificador. xyz ou. xyw deve ser aplicado a todas as leituras de um registro t (n) individual em uma instrução texcrd ou texld.</span><span class="sxs-lookup"><span data-stu-id="f7cd2-136">The same .xyz or .xyw modifier must be applied to every read of an individual t(n) register within a texcrd or texld instruction.</span></span>
2.  <span data-ttu-id="f7cd2-137">O quarto resultado de canal de texcrd é undefined/indefinido em todos os casos.</span><span class="sxs-lookup"><span data-stu-id="f7cd2-137">The fourth channel result of texcrd is unset/undefined in all cases.</span></span>
3.  <span data-ttu-id="f7cd2-138">O terceiro canal é desdefinido/indefinida para o \_ caso xyw DW.</span><span class="sxs-lookup"><span data-stu-id="f7cd2-138">The third channel is unset/undefined for the xyw\_dw case.</span></span>

## <a name="examples"></a><span data-ttu-id="f7cd2-139">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f7cd2-139">Examples</span></span>

<span data-ttu-id="f7cd2-140">O conjunto completo de sintaxe permitida para texcrd, levando em conta todas as combinações válidas de modificador de origem/seletor e máscara de gravação de destino, é mostrada abaixo.</span><span class="sxs-lookup"><span data-stu-id="f7cd2-140">The complete set of allowed syntax for texcrd, taking into account all valid source modifier/selector and destination write mask combinations, is shown below.</span></span> <span data-ttu-id="f7cd2-141">Observe que a notação. RGBA e. xyzw pode ser usada de forma intercambiável.</span><span class="sxs-lookup"><span data-stu-id="f7cd2-141">Note that the .rgba and .xyzw notation can be used interchangeably.</span></span>

<span data-ttu-id="f7cd2-142">Copia os três primeiros canais do registro do iterador de coordenadas de textura, t (n), em r (m).</span><span class="sxs-lookup"><span data-stu-id="f7cd2-142">Copies first three channels of texture coordinate iterator register, t(n), into r(m).</span></span> <span data-ttu-id="f7cd2-143">O quarto canal de r (m) não foi inicializado.</span><span class="sxs-lookup"><span data-stu-id="f7cd2-143">The fourth channel of r(m) is uninitialized.</span></span>


```
texcrd  r(m).rgb, t(n).xyz  

// Produces the same result as the previous instruction
texcrd  r(m).rgb, t(n)
```



<span data-ttu-id="f7cd2-144">Coloca o primeiro, o segundo e o quarto componente de t (n) nos três primeiros canais de r (m).</span><span class="sxs-lookup"><span data-stu-id="f7cd2-144">Puts first, second, and fourth components of t(n) into first three channels of r(m).</span></span> <span data-ttu-id="f7cd2-145">O quarto canal de r (m) não foi inicializado.</span><span class="sxs-lookup"><span data-stu-id="f7cd2-145">The fourth channel of r(m) is uninitialized.</span></span>


```
texcrd  r(m).rgb, t(n).xyw
```



<span data-ttu-id="f7cd2-146">Aqui está um exemplo de divisão projetada usando o \_ modificador de DW.</span><span class="sxs-lookup"><span data-stu-id="f7cd2-146">Here is a projective divide example using the \_dw modifier.</span></span>

<span data-ttu-id="f7cd2-147">Este exemplo copia x/w e y/w de t (n) para os dois primeiros canais de r (m).</span><span class="sxs-lookup"><span data-stu-id="f7cd2-147">This example copies x/w and y/w from t(n) into the first two channels of r(m).</span></span> <span data-ttu-id="f7cd2-148">O terceiro e o quarto canais de r (m) não são inicializados.</span><span class="sxs-lookup"><span data-stu-id="f7cd2-148">The third and fourth channels of r(m) are uninitialized.</span></span> <span data-ttu-id="f7cd2-149">Todos os dados gravados anteriormente no terceiro canal de r (m) serão perdidos.</span><span class="sxs-lookup"><span data-stu-id="f7cd2-149">Any data previously written to the third channel of r(m) will be lost.</span></span> <span data-ttu-id="f7cd2-150">Os dados no quarto canal de r (m) são perdidos devido ao marcador de fase.</span><span class="sxs-lookup"><span data-stu-id="f7cd2-150">Data in the fourth channel of r(m) is lost due to the phase marker.</span></span> <span data-ttu-id="f7cd2-151">Para a versão 1 \_ 4, o \_ sinalizador projetado D3DTTFF é ignorado.</span><span class="sxs-lookup"><span data-stu-id="f7cd2-151">For version 1\_4, the D3DTTFF\_PROJECTED flag is ignored.</span></span>


```
texcrd  r(m).rg,  t(n)_dw.xyw
```



## <a name="related-topics"></a><span data-ttu-id="f7cd2-152">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f7cd2-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f7cd2-153">Instruções do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="f7cd2-153">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 