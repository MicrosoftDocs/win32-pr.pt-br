---
description: Define operações de mesclagem de textura por estágio.
ms.assetid: 7bfdcb15-c3c3-4e7e-b924-6ecfa350e2f3
title: Enumeração D3DTEXTUREOP (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DTEXTUREOP
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: d35e2d4b65cd41a49d8ed8edb3252295ca3baef3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298552"
---
# <a name="d3dtextureop-enumeration"></a><span data-ttu-id="d1797-103">Enumeração D3DTEXTUREOP</span><span class="sxs-lookup"><span data-stu-id="d1797-103">D3DTEXTUREOP enumeration</span></span>

<span data-ttu-id="d1797-104">Define operações de mesclagem de textura por estágio.</span><span class="sxs-lookup"><span data-stu-id="d1797-104">Defines per-stage texture-blending operations.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1797-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d1797-105">Syntax</span></span>


```C++
typedef enum D3DTEXTUREOP { 
  D3DTOP_DISABLE                    = 1,
  D3DTOP_SELECTARG1                 = 2,
  D3DTOP_SELECTARG2                 = 3,
  D3DTOP_MODULATE                   = 4,
  D3DTOP_MODULATE2X                 = 5,
  D3DTOP_MODULATE4X                 = 6,
  D3DTOP_ADD                        = 7,
  D3DTOP_ADDSIGNED                  = 8,
  D3DTOP_ADDSIGNED2X                = 9,
  D3DTOP_SUBTRACT                   = 10,
  D3DTOP_ADDSMOOTH                  = 11,
  D3DTOP_BLENDDIFFUSEALPHA          = 12,
  D3DTOP_BLENDTEXTUREALPHA          = 13,
  D3DTOP_BLENDFACTORALPHA           = 14,
  D3DTOP_BLENDTEXTUREALPHAPM        = 15,
  D3DTOP_BLENDCURRENTALPHA          = 16,
  D3DTOP_PREMODULATE                = 17,
  D3DTOP_MODULATEALPHA_ADDCOLOR     = 18,
  D3DTOP_MODULATECOLOR_ADDALPHA     = 19,
  D3DTOP_MODULATEINVALPHA_ADDCOLOR  = 20,
  D3DTOP_MODULATEINVCOLOR_ADDALPHA  = 21,
  D3DTOP_BUMPENVMAP                 = 22,
  D3DTOP_BUMPENVMAPLUMINANCE        = 23,
  D3DTOP_DOTPRODUCT3                = 24,
  D3DTOP_MULTIPLYADD                = 25,
  D3DTOP_LERP                       = 26,
  D3DTOP_FORCE_DWORD                = 0x7fffffff
} D3DTEXTUREOP, *LPD3DTEXTUREOP;
```



## <a name="constants"></a><span data-ttu-id="d1797-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="d1797-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="d1797-107"><span id="D3DTOP_DISABLE"></span><span id="d3dtop_disable"></span>**D3DTOP \_ desabilitar**</span><span class="sxs-lookup"><span data-stu-id="d1797-107"><span id="D3DTOP_DISABLE"></span><span id="d3dtop_disable"></span>**D3DTOP\_DISABLE**</span></span>
</dt> <dd>

<span data-ttu-id="d1797-108">Desabilita a saída deste estágio de textura e todos os estágios com um índice mais alto.</span><span class="sxs-lookup"><span data-stu-id="d1797-108">Disables output from this texture stage and all stages with a higher index.</span></span> <span data-ttu-id="d1797-109">Para desabilitar o mapeamento de textura, defina como a operação de cor para o primeiro estágio de textura (estágio 0).</span><span class="sxs-lookup"><span data-stu-id="d1797-109">To disable texture mapping, set this as the color operation for the first texture stage (stage 0).</span></span> <span data-ttu-id="d1797-110">As operações alfa não podem ser desabilitadas quando as operações de cores estão habilitadas.</span><span class="sxs-lookup"><span data-stu-id="d1797-110">Alpha operations cannot be disabled when color operations are enabled.</span></span> <span data-ttu-id="d1797-111">Definir a operação Alpha como D3DTOP \_ Disable quando a mesclagem de cores está habilitada causa um comportamento indefinido.</span><span class="sxs-lookup"><span data-stu-id="d1797-111">Setting the alpha operation to D3DTOP\_DISABLE when color blending is enabled causes undefined behavior.</span></span>

</dd> <dt>

<span data-ttu-id="d1797-112"><span id="D3DTOP_SELECTARG1"></span><span id="d3dtop_selectarg1"></span>**D3DTOP \_ SELECTARG1**</span><span class="sxs-lookup"><span data-stu-id="d1797-112"><span id="D3DTOP_SELECTARG1"></span><span id="d3dtop_selectarg1"></span>**D3DTOP\_SELECTARG1**</span></span>
</dt> <dd>

<span data-ttu-id="d1797-113">Use a primeira cor ou argumento alfa do estágio de textura, sem modificações, como a saída.</span><span class="sxs-lookup"><span data-stu-id="d1797-113">Use this texture stage's first color or alpha argument, unmodified, as the output.</span></span> <span data-ttu-id="d1797-114">Essa operação afeta o argumento de cor quando usado com o \_ estado de D3DTSS COLOROP de textura e o argumento alfa quando usado com D3DTSS \_ ALPHAOP.</span><span class="sxs-lookup"><span data-stu-id="d1797-114">This operation affects the color argument when used with the D3DTSS\_COLOROP texture-stage state, and the alpha argument when used with D3DTSS\_ALPHAOP.</span></span>

![equação deste argumento (s (RGBA) = arg1)](images/topfrm1.png)

</dd> <dt>

<span data-ttu-id="d1797-116"><span id="D3DTOP_SELECTARG2"></span><span id="d3dtop_selectarg2"></span>**D3DTOP \_ SELECTARG2**</span><span class="sxs-lookup"><span data-stu-id="d1797-116"><span id="D3DTOP_SELECTARG2"></span><span id="d3dtop_selectarg2"></span>**D3DTOP\_SELECTARG2**</span></span>
</dt> <dd>

<span data-ttu-id="d1797-117">Use a segunda cor ou o argumento alfa do estágio de textura, sem modificações, como a saída.</span><span class="sxs-lookup"><span data-stu-id="d1797-117">Use this texture stage's second color or alpha argument, unmodified, as the output.</span></span> <span data-ttu-id="d1797-118">Essa operação afeta o argumento de cor quando usado com o \_ estado de estágio de textura D3DTSS COLOROP e o argumento alfa quando usado com D3DTSS \_ ALPHAOP.</span><span class="sxs-lookup"><span data-stu-id="d1797-118">This operation affects the color argument when used with the D3DTSS\_COLOROP texture stage state, and the alpha argument when used with D3DTSS\_ALPHAOP.</span></span>

![equação deste argumento (s (RGBA) = arg2)](images/topfrm2.png)

</dd> <dt>

<span data-ttu-id="d1797-120"><span id="D3DTOP_MODULATE"></span><span id="d3dtop_modulate"></span>**\_Modular D3DTOP**</span><span class="sxs-lookup"><span data-stu-id="d1797-120"><span id="D3DTOP_MODULATE"></span><span id="d3dtop_modulate"></span>**D3DTOP\_MODULATE**</span></span>
</dt> <dd>

<span data-ttu-id="d1797-121">Multiplique os componentes dos argumentos.</span><span class="sxs-lookup"><span data-stu-id="d1797-121">Multiply the components of the arguments.</span></span>

![equação da operação modular (s (RGBA) = arg1 x ARG 2)](images/topfrm3.png)

</dd> <dt>

<span data-ttu-id="d1797-123"><span id="D3DTOP_MODULATE2X"></span><span id="d3dtop_modulate2x"></span>**D3DTOP \_ MODULATE2X**</span><span class="sxs-lookup"><span data-stu-id="d1797-123"><span id="D3DTOP_MODULATE2X"></span><span id="d3dtop_modulate2x"></span>**D3DTOP\_MODULATE2X**</span></span>
</dt> <dd>

<span data-ttu-id="d1797-124">Multiplique os componentes dos argumentos e SHIFTe os produtos para a esquerda 1 bit (efetivamente multiplicando-os por 2) para clareamento.</span><span class="sxs-lookup"><span data-stu-id="d1797-124">Multiply the components of the arguments, and shift the products to the left 1 bit (effectively multiplying them by 2) for brightening.</span></span>

![equação da operação Modulate2X (s (RGBA) = (arg1 x ARG 2) e, em seguida, SHIFT esquerda 1)](images/topfrm4.png)

</dd> <dt>

<span data-ttu-id="d1797-126"><span id="D3DTOP_MODULATE4X"></span><span id="d3dtop_modulate4x"></span>**D3DTOP \_ MODULATE4X**</span><span class="sxs-lookup"><span data-stu-id="d1797-126"><span id="D3DTOP_MODULATE4X"></span><span id="d3dtop_modulate4x"></span>**D3DTOP\_MODULATE4X**</span></span>
</dt> <dd>

<span data-ttu-id="d1797-127">Multiplique os componentes dos argumentos e mude os produtos para os 2 bits à esquerda (com eficiência, multiplique-os por 4) para clarear.</span><span class="sxs-lookup"><span data-stu-id="d1797-127">Multiply the components of the arguments, and shift the products to the left 2 bits (effectively multiplying them by 4) for brightening.</span></span>

![equação da operação Modulate4X (s (RGBA) = (arg1 x ARG 2) e, em seguida, SHIFT esquerda 2)](images/topfrm5.png)

</dd> <dt>

<span data-ttu-id="d1797-129"><span id="D3DTOP_ADD"></span><span id="d3dtop_add"></span>**D3DTOP \_ Adicionar**</span><span class="sxs-lookup"><span data-stu-id="d1797-129"><span id="D3DTOP_ADD"></span><span id="d3dtop_add"></span>**D3DTOP\_ADD**</span></span>
</dt> <dd>

<span data-ttu-id="d1797-130">Adicione os componentes dos argumentos.</span><span class="sxs-lookup"><span data-stu-id="d1797-130">Add the components of the arguments.</span></span>

![equação da operação de adição (s (RGBA) = arg1 + ARG 2)](images/topfrm6.png)

</dd> <dt>

<span data-ttu-id="d1797-132"><span id="D3DTOP_ADDSIGNED"></span><span id="d3dtop_addsigned"></span>**D3DTOP \_ ADDsigned**</span><span class="sxs-lookup"><span data-stu-id="d1797-132"><span id="D3DTOP_ADDSIGNED"></span><span id="d3dtop_addsigned"></span>**D3DTOP\_ADDSIGNED**</span></span>
</dt> <dd>

<span data-ttu-id="d1797-133">Adicione os componentes dos argumentos com uma diferença de a-0,5, tornando o intervalo de valores efetivo de-0,5 até 0,5.</span><span class="sxs-lookup"><span data-stu-id="d1797-133">Add the components of the arguments with a - 0.5 bias, making the effective range of values from - 0.5 through 0.5.</span></span>

![equação da operação Adicionar assinada (s (RGBA) = arg1 + ARG 2 – 0,5)](images/topfrm7.png)

</dd> <dt>

<span data-ttu-id="d1797-135"><span id="D3DTOP_ADDSIGNED2X"></span><span id="d3dtop_addsigned2x"></span>**D3DTOP \_ ADDSIGNED2X**</span><span class="sxs-lookup"><span data-stu-id="d1797-135"><span id="D3DTOP_ADDSIGNED2X"></span><span id="d3dtop_addsigned2x"></span>**D3DTOP\_ADDSIGNED2X**</span></span>
</dt> <dd>

<span data-ttu-id="d1797-136">Adicione os componentes dos argumentos com uma tendência de a-0,5 e SHIFTe os produtos para a esquerda 1 bit.</span><span class="sxs-lookup"><span data-stu-id="d1797-136">Add the components of the arguments with a - 0.5 bias, and shift the products to the left 1 bit.</span></span>

![equação do Adicionar operação 2x assinada ((s (RGBA) = arg1 + ARG 2-0,5) e, em seguida, SHIFT esquerda 1)](images/topfrm8.png)

</dd> <dt>

<span data-ttu-id="d1797-138"><span id="D3DTOP_SUBTRACT"></span><span id="d3dtop_subtract"></span>**\_Subtrair D3DTOP**</span><span class="sxs-lookup"><span data-stu-id="d1797-138"><span id="D3DTOP_SUBTRACT"></span><span id="d3dtop_subtract"></span>**D3DTOP\_SUBTRACT**</span></span>
</dt> <dd>

<span data-ttu-id="d1797-139">Subtraia os componentes do segundo argumento daqueles do primeiro argumento.</span><span class="sxs-lookup"><span data-stu-id="d1797-139">Subtract the components of the second argument from those of the first argument.</span></span>

![equação da operação de subtração (s (RGBA) = arg1-ARG 2)](images/topfrm9.png)

</dd> <dt>

<span data-ttu-id="d1797-141"><span id="D3DTOP_ADDSMOOTH"></span><span id="d3dtop_addsmooth"></span>**D3DTOP \_ ADDsmooth**</span><span class="sxs-lookup"><span data-stu-id="d1797-141"><span id="D3DTOP_ADDSMOOTH"></span><span id="d3dtop_addsmooth"></span>**D3DTOP\_ADDSMOOTH**</span></span>
</dt> <dd>

<span data-ttu-id="d1797-142">Adicionar o primeiro e o segundo argumentos; em seguida, subtraia seu produto da soma.</span><span class="sxs-lookup"><span data-stu-id="d1797-142">Add the first and second arguments; then subtract their product from the sum.</span></span>

![equação da operação Adicionar suave (s (RGBA) = arg1 + ARG 2 x (1-arg1))](images/topfrm10.png)

</dd> <dt>

<span data-ttu-id="d1797-144"><span id="D3DTOP_BLENDDIFFUSEALPHA"></span><span id="d3dtop_blenddiffusealpha"></span>**D3DTOP \_ BLENDDIFFUSEALPHA**</span><span class="sxs-lookup"><span data-stu-id="d1797-144"><span id="D3DTOP_BLENDDIFFUSEALPHA"></span><span id="d3dtop_blenddiffusealpha"></span>**D3DTOP\_BLENDDIFFUSEALPHA**</span></span>
</dt> <dd>

<span data-ttu-id="d1797-145">Mescle linearmente esse estágio de textura, usando o alfa interpolado de cada vértice.</span><span class="sxs-lookup"><span data-stu-id="d1797-145">Linearly blend this texture stage, using the interpolated alpha from each vertex.</span></span>

![equação da operação alfa difusa do Blend (s (RGBA) = arg1 x Alpha + ARG 2 x (1-Alpha))](images/topfrm11.png)

</dd> <dt>

<span data-ttu-id="d1797-147"><span id="D3DTOP_BLENDTEXTUREALPHA"></span><span id="d3dtop_blendtexturealpha"></span>**D3DTOP \_ BLENDTEXTUREALPHA**</span><span class="sxs-lookup"><span data-stu-id="d1797-147"><span id="D3DTOP_BLENDTEXTUREALPHA"></span><span id="d3dtop_blendtexturealpha"></span>**D3DTOP\_BLENDTEXTUREALPHA**</span></span>
</dt> <dd>

<span data-ttu-id="d1797-148">Mescle linearmente este estágio de textura, usando o alfa da textura deste estágio.</span><span class="sxs-lookup"><span data-stu-id="d1797-148">Linearly blend this texture stage, using the alpha from this stage's texture.</span></span>

![equação da operação alfa de textura de mesclagem (s (RGBA) = arg1 x alfa + ARG 2 x (1-Alpha))](images/topfrm11.png)

</dd> <dt>

<span data-ttu-id="d1797-150"><span id="D3DTOP_BLENDFACTORALPHA"></span><span id="d3dtop_blendfactoralpha"></span>**D3DTOP \_ BLENDFACTORALPHA**</span><span class="sxs-lookup"><span data-stu-id="d1797-150"><span id="D3DTOP_BLENDFACTORALPHA"></span><span id="d3dtop_blendfactoralpha"></span>**D3DTOP\_BLENDFACTORALPHA**</span></span>
</dt> <dd>

<span data-ttu-id="d1797-151">Mescle linearmente esse estágio de textura, usando um conjunto de Alpha escalar com o \_ estado de RENDERIZAÇÃO D3DRS TEXTUREFACTOR.</span><span class="sxs-lookup"><span data-stu-id="d1797-151">Linearly blend this texture stage, using a scalar alpha set with the D3DRS\_TEXTUREFACTOR render state.</span></span>

![equação da operação alfa do fator de mistura (s (RGBA) = arg1 x alfa + ARG 2 x (1-Alpha))](images/topfrm11.png)

</dd> <dt>

<span data-ttu-id="d1797-153"><span id="D3DTOP_BLENDTEXTUREALPHAPM"></span><span id="d3dtop_blendtexturealphapm"></span>**D3DTOP \_ BLENDTEXTUREALPHAPM**</span><span class="sxs-lookup"><span data-stu-id="d1797-153"><span id="D3DTOP_BLENDTEXTUREALPHAPM"></span><span id="d3dtop_blendtexturealphapm"></span>**D3DTOP\_BLENDTEXTUREALPHAPM**</span></span>
</dt> <dd>

<span data-ttu-id="d1797-154">Misturar linearmente um estágio de textura que usa um alfa previamente multiplicado.</span><span class="sxs-lookup"><span data-stu-id="d1797-154">Linearly blend a texture stage that uses a premultiplied alpha.</span></span>

![equação da operação do Blend Texture Alpha PM (s (RGBA) = arg1 + ARG 2 x (1-Alpha))](images/topfrm12.png)

</dd> <dt>

<span data-ttu-id="d1797-156"><span id="D3DTOP_BLENDCURRENTALPHA"></span><span id="d3dtop_blendcurrentalpha"></span>**D3DTOP \_ BLENDCURRENTALPHA**</span><span class="sxs-lookup"><span data-stu-id="d1797-156"><span id="D3DTOP_BLENDCURRENTALPHA"></span><span id="d3dtop_blendcurrentalpha"></span>**D3DTOP\_BLENDCURRENTALPHA**</span></span>
</dt> <dd>

<span data-ttu-id="d1797-157">Mescle linearmente este estágio de textura, usando alfa tirado do estágio de textura anterior.</span><span class="sxs-lookup"><span data-stu-id="d1797-157">Linearly blend this texture stage, using the alpha taken from the previous texture stage.</span></span>

![equação da operação alfa (s (RGBA) atual de Blend = arg1 x Alpha + arg2 x (1-Alpha))](images/topfrm11.png)

</dd> <dt>

<span data-ttu-id="d1797-159"><span id="D3DTOP_PREMODULATE"></span><span id="d3dtop_premodulate"></span>**D3DTOP \_ PREmodular**</span><span class="sxs-lookup"><span data-stu-id="d1797-159"><span id="D3DTOP_PREMODULATE"></span><span id="d3dtop_premodulate"></span>**D3DTOP\_PREMODULATE**</span></span>
</dt> <dd>

<span data-ttu-id="d1797-160">D3DTOP \_ PREmodular está definido no estágio n.</span><span class="sxs-lookup"><span data-stu-id="d1797-160">D3DTOP\_PREMODULATE is set in stage n.</span></span> <span data-ttu-id="d1797-161">A saída do estágio n é arg1.</span><span class="sxs-lookup"><span data-stu-id="d1797-161">The output of stage n is arg1.</span></span> <span data-ttu-id="d1797-162">Além disso, se houver uma textura no estágio n + 1, qualquer D3DTA \_ atual no estágio n + 1 será contramultiplicado por textura no estágio n + 1.</span><span class="sxs-lookup"><span data-stu-id="d1797-162">Additionally, if there is a texture in stage n + 1, any D3DTA\_CURRENT in stage n + 1 is premultiplied by texture in stage n + 1.</span></span>

</dd> <dt>

<span data-ttu-id="d1797-163"><span id="D3DTOP_MODULATEALPHA_ADDCOLOR"></span><span id="d3dtop_modulatealpha_addcolor"></span>**Addcolor D3DTOP \_ MODULATEALPHA \_**</span><span class="sxs-lookup"><span data-stu-id="d1797-163"><span id="D3DTOP_MODULATEALPHA_ADDCOLOR"></span><span id="d3dtop_modulatealpha_addcolor"></span>**D3DTOP\_MODULATEALPHA\_ADDCOLOR**</span></span>
</dt> <dd>

<span data-ttu-id="d1797-164">Modular a cor do segundo argumento, usando o alfa do primeiro argumento; em seguida, adicione o resultado ao argumento um.</span><span class="sxs-lookup"><span data-stu-id="d1797-164">Modulate the color of the second argument, using the alpha of the first argument; then add the result to argument one.</span></span> <span data-ttu-id="d1797-165">Esta operação só tem suporte para operações de cor (D3DTSS \_ COLOROP).</span><span class="sxs-lookup"><span data-stu-id="d1797-165">This operation is supported only for color operations (D3DTSS\_COLOROP).</span></span>

![equação da operação Adicionar alfa modular de cor (s (RGBA) = arg1 (RGB) + arg1 (a) x arg2 (RGB))](images/topfrm13.png)

</dd> <dt>

<span data-ttu-id="d1797-167"><span id="D3DTOP_MODULATECOLOR_ADDALPHA"></span><span id="d3dtop_modulatecolor_addalpha"></span>**D3DTOP \_ MODULATECOLOR \_ addalpha**</span><span class="sxs-lookup"><span data-stu-id="d1797-167"><span id="D3DTOP_MODULATECOLOR_ADDALPHA"></span><span id="d3dtop_modulatecolor_addalpha"></span>**D3DTOP\_MODULATECOLOR\_ADDALPHA**</span></span>
</dt> <dd>

<span data-ttu-id="d1797-168">Modular os argumentos; em seguida, adicione o alfa do primeiro argumento.</span><span class="sxs-lookup"><span data-stu-id="d1797-168">Modulate the arguments; then add the alpha of the first argument.</span></span> <span data-ttu-id="d1797-169">Esta operação só tem suporte para operações de cor (D3DTSS \_ COLOROP).</span><span class="sxs-lookup"><span data-stu-id="d1797-169">This operation is supported only for color operations (D3DTSS\_COLOROP).</span></span>

![equação da operação de adição de cor de alfa modular (s (RGBA) = arg1 (RGB) x arg2 (RGB) + arg1 (a))](images/topfrm14.png)

</dd> <dt>

<span data-ttu-id="d1797-171"><span id="D3DTOP_MODULATEINVALPHA_ADDCOLOR"></span><span id="d3dtop_modulateinvalpha_addcolor"></span>**Addcolor D3DTOP \_ MODULATEINVALPHA \_**</span><span class="sxs-lookup"><span data-stu-id="d1797-171"><span id="D3DTOP_MODULATEINVALPHA_ADDCOLOR"></span><span id="d3dtop_modulateinvalpha_addcolor"></span>**D3DTOP\_MODULATEINVALPHA\_ADDCOLOR**</span></span>
</dt> <dd>

<span data-ttu-id="d1797-172">Semelhante a D3DTOP \_ MODULATEALPHA \_ addcolor, mas use o inverso do alfa do primeiro argumento.</span><span class="sxs-lookup"><span data-stu-id="d1797-172">Similar to D3DTOP\_MODULATEALPHA\_ADDCOLOR, but use the inverse of the alpha of the first argument.</span></span> <span data-ttu-id="d1797-173">Esta operação só tem suporte para operações de cor (D3DTSS \_ COLOROP).</span><span class="sxs-lookup"><span data-stu-id="d1797-173">This operation is supported only for color operations (D3DTSS\_COLOROP).</span></span>

![equação da operação de adição de alfa inversa (s (RGBA) de modulação de cor = (1-arg1 (a)) x arg2 (RGB) + arg1 (RGB))](images/topfrm15.png)

</dd> <dt>

<span data-ttu-id="d1797-175"><span id="D3DTOP_MODULATEINVCOLOR_ADDALPHA"></span><span id="d3dtop_modulateinvcolor_addalpha"></span>**D3DTOP \_ MODULATEINVCOLOR \_ addalpha**</span><span class="sxs-lookup"><span data-stu-id="d1797-175"><span id="D3DTOP_MODULATEINVCOLOR_ADDALPHA"></span><span id="d3dtop_modulateinvcolor_addalpha"></span>**D3DTOP\_MODULATEINVCOLOR\_ADDALPHA**</span></span>
</dt> <dd>

<span data-ttu-id="d1797-176">Semelhante a D3DTOP \_ MODULATECOLOR \_ addalpha, mas use o inverso da cor do primeiro argumento.</span><span class="sxs-lookup"><span data-stu-id="d1797-176">Similar to D3DTOP\_MODULATECOLOR\_ADDALPHA, but use the inverse of the color of the first argument.</span></span> <span data-ttu-id="d1797-177">Esta operação só tem suporte para operações de cor (D3DTSS \_ COLOROP).</span><span class="sxs-lookup"><span data-stu-id="d1797-177">This operation is supported only for color operations (D3DTSS\_COLOROP).</span></span>

![equação da operação de adição de cor inversa alfa modular (s (RGBA) = (1-arg1 (RGB)) x arg2 (RGB) + arg1 (a))](images/topfrm16.png)

</dd> <dt>

<span data-ttu-id="d1797-179"><span id="D3DTOP_BUMPENVMAP"></span><span id="d3dtop_bumpenvmap"></span>**D3DTOP \_ BUMPENVMAP**</span><span class="sxs-lookup"><span data-stu-id="d1797-179"><span id="D3DTOP_BUMPENVMAP"></span><span id="d3dtop_bumpenvmap"></span>**D3DTOP\_BUMPENVMAP**</span></span>
</dt> <dd>

<span data-ttu-id="d1797-180">Execute o mapeamento de relevo por pixel, usando o mapa de ambiente no próximo estágio de textura, sem luminância.</span><span class="sxs-lookup"><span data-stu-id="d1797-180">Perform per-pixel bump mapping, using the environment map in the next texture stage, without luminance.</span></span> <span data-ttu-id="d1797-181">Esta operação só tem suporte para operações de cor (D3DTSS \_ COLOROP).</span><span class="sxs-lookup"><span data-stu-id="d1797-181">This operation is supported only for color operations (D3DTSS\_COLOROP).</span></span>

</dd> <dt>

<span data-ttu-id="d1797-182"><span id="D3DTOP_BUMPENVMAPLUMINANCE"></span><span id="d3dtop_bumpenvmapluminance"></span>**D3DTOP \_ BUMPENVMAPLUMINANCE**</span><span class="sxs-lookup"><span data-stu-id="d1797-182"><span id="D3DTOP_BUMPENVMAPLUMINANCE"></span><span id="d3dtop_bumpenvmapluminance"></span>**D3DTOP\_BUMPENVMAPLUMINANCE**</span></span>
</dt> <dd>

<span data-ttu-id="d1797-183">Execute o mapeamento de relevo por pixel, usando o mapa de ambiente no próximo estágio de textura, com luminância.</span><span class="sxs-lookup"><span data-stu-id="d1797-183">Perform per-pixel bump mapping, using the environment map in the next texture stage, with luminance.</span></span> <span data-ttu-id="d1797-184">Esta operação só tem suporte para operações de cor (D3DTSS \_ COLOROP).</span><span class="sxs-lookup"><span data-stu-id="d1797-184">This operation is supported only for color operations (D3DTSS\_COLOROP).</span></span>

</dd> <dt>

<span data-ttu-id="d1797-185"><span id="D3DTOP_DOTPRODUCT3"></span><span id="d3dtop_dotproduct3"></span>**D3DTOP \_ DOTPRODUCT3**</span><span class="sxs-lookup"><span data-stu-id="d1797-185"><span id="D3DTOP_DOTPRODUCT3"></span><span id="d3dtop_dotproduct3"></span>**D3DTOP\_DOTPRODUCT3**</span></span>
</dt> <dd>

<span data-ttu-id="d1797-186">Modular os componentes de cada argumento como componentes assinados, adicionar seus produtos; em seguida, replique a soma para todos os canais de cores, incluindo alfa.</span><span class="sxs-lookup"><span data-stu-id="d1797-186">Modulate the components of each argument as signed components, add their products; then replicate the sum to all color channels, including alpha.</span></span> <span data-ttu-id="d1797-187">Esta operação tem suporte para operações de cor e alfa.</span><span class="sxs-lookup"><span data-stu-id="d1797-187">This operation is supported for color and alpha operations.</span></span>

![equação da operação do ponto 3 do produto (s (RGBA) = arg1 (r) x arg2 (r) + arg1 (g) x arg2 (g) + arg1 (b) x arg2 (b))](images/topfrm17.png)

<span data-ttu-id="d1797-189">No DirectX 6 e DirectX 7, as operações de multitexturas as entradas acima são todas deslocadas pela metade (y = x-0,5) antes de usar para simular dados assinados, e o resultado escalar é automaticamente clamped para valores positivos e replicados para todos os três canais de saída.</span><span class="sxs-lookup"><span data-stu-id="d1797-189">In DirectX 6 and DirectX 7, multitexture operations the above inputs are all shifted down by half (y = x - 0.5) before use to simulate signed data, and the scalar result is automatically clamped to positive values and replicated to all three output channels.</span></span> <span data-ttu-id="d1797-190">Além disso, observe que, como uma operação de cor, isso não atualizou o alfa que apenas atualiza os componentes RGB.</span><span class="sxs-lookup"><span data-stu-id="d1797-190">Also, note that as a color operation this does not updated the alpha it just updates the RGB components.</span></span>

<span data-ttu-id="d1797-191">No entanto, em sombreadores do DirectX 8,1, você pode especificar que a saída seja roteada para os componentes. RGB ou. a ou ambos (o padrão).</span><span class="sxs-lookup"><span data-stu-id="d1797-191">However, in DirectX 8.1 shaders you can specify that the output be routed to the .rgb or the .a components or both (the default).</span></span> <span data-ttu-id="d1797-192">Você também pode especificar uma operação escalar separada no canal alfa.</span><span class="sxs-lookup"><span data-stu-id="d1797-192">You can also specify a separate scalar operation on the alpha channel.</span></span>

</dd> <dt>

<span data-ttu-id="d1797-193"><span id="D3DTOP_MULTIPLYADD"></span><span id="d3dtop_multiplyadd"></span>**D3DTOP \_ MULTIPLYADD**</span><span class="sxs-lookup"><span data-stu-id="d1797-193"><span id="D3DTOP_MULTIPLYADD"></span><span id="d3dtop_multiplyadd"></span>**D3DTOP\_MULTIPLYADD**</span></span>
</dt> <dd>

<span data-ttu-id="d1797-194">Executa uma operação de acumulação de multiplicação.</span><span class="sxs-lookup"><span data-stu-id="d1797-194">Performs a multiply-accumulate operation.</span></span> <span data-ttu-id="d1797-195">Ele usa os dois últimos argumentos, multiplica-os juntos e os adiciona ao argumento restante de entrada/origem e coloca isso no resultado.</span><span class="sxs-lookup"><span data-stu-id="d1797-195">It takes the last two arguments, multiplies them together, and adds them to the remaining input/source argument, and places that into the result.</span></span>

<span data-ttu-id="d1797-196">S<sub>RGBA</sub> = Arg1 + Arg2 \* Arg3</span><span class="sxs-lookup"><span data-stu-id="d1797-196">S<sub>RGBA</sub> = Arg1 + Arg2 \* Arg3</span></span>

</dd> <dt>

<span data-ttu-id="d1797-197"><span id="D3DTOP_LERP"></span><span id="d3dtop_lerp"></span>**D3DTOP \_ LERP**</span><span class="sxs-lookup"><span data-stu-id="d1797-197"><span id="D3DTOP_LERP"></span><span id="d3dtop_lerp"></span>**D3DTOP\_LERP**</span></span>
</dt> <dd>

<span data-ttu-id="d1797-198">Interpola linearmente entre o segundo e o terceiro argumentos de origem por uma proporção especificada no primeiro argumento de origem.</span><span class="sxs-lookup"><span data-stu-id="d1797-198">Linearly interpolates between the second and third source arguments by a proportion specified in the first source argument.</span></span>

<span data-ttu-id="d1797-199">S<sub>RGBA</sub> = (arg1) \* arg2 + (1-arg1) \* Arg3.</span><span class="sxs-lookup"><span data-stu-id="d1797-199">S<sub>RGBA</sub> = (Arg1) \* Arg2 + (1- Arg1) \* Arg3.</span></span>

</dd> <dt>

<span data-ttu-id="d1797-200"><span id="D3DTOP_FORCE_DWORD"></span><span id="d3dtop_force_dword"></span>**D3DTOP \_ forçar \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="d1797-200"><span id="D3DTOP_FORCE_DWORD"></span><span id="d3dtop_force_dword"></span>**D3DTOP\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="d1797-201">Força essa enumeração a compilar a 32 bits de tamanho.</span><span class="sxs-lookup"><span data-stu-id="d1797-201">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="d1797-202">Sem esse valor, alguns compiladores permitiriam que essa enumeração fosse compilada em um tamanho diferente de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="d1797-202">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="d1797-203">Este valor não é usado.</span><span class="sxs-lookup"><span data-stu-id="d1797-203">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d1797-204">Comentários</span><span class="sxs-lookup"><span data-stu-id="d1797-204">Remarks</span></span>

<span data-ttu-id="d1797-205">Os membros desse tipo são usados ao definir operações de cor ou alfa usando os valores de D3DTSS \_ COLOROP ou D3DTSS \_ ALPHAOP com o método [**IDirect3DDevice9:: SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate) .</span><span class="sxs-lookup"><span data-stu-id="d1797-205">The members of this type are used when setting color or alpha operations by using the D3DTSS\_COLOROP or D3DTSS\_ALPHAOP values with the [**IDirect3DDevice9::SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate) method.</span></span>

<span data-ttu-id="d1797-206">Nas fórmulas acima, S<sub>RGBA</sub> é a cor RGBA produzida por uma operação de textura e arg1, arg2 e Arg3 representam a cor de RGBA completa dos argumentos de textura.</span><span class="sxs-lookup"><span data-stu-id="d1797-206">In the above formulas, S<sub>RGBA</sub> is the RGBA color produced by a texture operation, and Arg1, Arg2, and Arg3 represent the complete RGBA color of the texture arguments.</span></span> <span data-ttu-id="d1797-207">Componentes individuais de um argumento são mostrados com subscritos.</span><span class="sxs-lookup"><span data-stu-id="d1797-207">Individual components of an argument are shown with subscripts.</span></span> <span data-ttu-id="d1797-208">Por exemplo, o componente alfa para o argumento 1 seria mostrado como arg1<sub>A</sub>.</span><span class="sxs-lookup"><span data-stu-id="d1797-208">For example, the alpha component for argument 1 would be shown as Arg1<sub>A</sub>.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1797-209">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d1797-209">Requirements</span></span>



| <span data-ttu-id="d1797-210">Requisito</span><span class="sxs-lookup"><span data-stu-id="d1797-210">Requirement</span></span> | <span data-ttu-id="d1797-211">Valor</span><span class="sxs-lookup"><span data-stu-id="d1797-211">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d1797-212">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d1797-212">Header</span></span><br/> | <dl> <span data-ttu-id="d1797-213"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="d1797-213"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d1797-214">Confira também</span><span class="sxs-lookup"><span data-stu-id="d1797-214">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1797-215">Enumerações do Direct3D</span><span class="sxs-lookup"><span data-stu-id="d1797-215">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="d1797-216">**D3DTEXTURESTAGESTATETYPE**</span><span class="sxs-lookup"><span data-stu-id="d1797-216">**D3DTEXTURESTAGESTATETYPE**</span></span>](./d3dtexturestagestatetype.md)
</dt> </dl>

 

 
