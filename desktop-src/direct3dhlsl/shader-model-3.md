---
title: Modelo de sombreador 3 (referência HLSL)
description: Sombreadores de vértice e sombreadores de pixel são simplificados consideravelmente de versões anteriores do sombreador.
ms.assetid: 01ac85cb-b309-4169-acc2-320a929b65cb
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2d87c791694e91de135052b4172e3bd5f55577d7
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/09/2021
ms.locfileid: "111827095"
---
# <a name="shader-model-3-hlsl-reference"></a><span data-ttu-id="7a2da-103">Modelo de sombreador 3 (referência HLSL)</span><span class="sxs-lookup"><span data-stu-id="7a2da-103">Shader model 3 (HLSL reference)</span></span>

<span data-ttu-id="7a2da-104">Sombreadores de vértice e sombreadores de pixel são simplificados consideravelmente de versões anteriores do sombreador.</span><span class="sxs-lookup"><span data-stu-id="7a2da-104">Vertex shaders and pixel shaders are simplified considerably from earlier shader versions.</span></span> <span data-ttu-id="7a2da-105">Se você estiver implementando sombreadores em hardware, talvez não use vs \_ 3 0 ou ps 3 0 com outras versões de sombreador e não poderá usar nenhum tipo de sombreador com o pipeline de funções \_ \_ \_ fixas.</span><span class="sxs-lookup"><span data-stu-id="7a2da-105">If you are implementing shaders in hardware, you may not use vs\_3\_0 or ps\_3\_0 with any other shader versions, and you may not use either shader type with the fixed function pipeline.</span></span> <span data-ttu-id="7a2da-106">Essas alterações possibilitam simplificar os drivers e o runtime.</span><span class="sxs-lookup"><span data-stu-id="7a2da-106">These changes make it possible to simplify drivers and the runtime.</span></span> <span data-ttu-id="7a2da-107">A única exceção é que os sombreadores somente de software \_ \_ versus 3 0 podem ser usados com qualquer versão do sombreador de pixel.</span><span class="sxs-lookup"><span data-stu-id="7a2da-107">The only exception is that software-only vs\_3\_0 shaders may be used with any pixel shader version.</span></span> <span data-ttu-id="7a2da-108">Além disso, se você estiver usando um sombreador somente de software versus 3 0 com uma versão anterior do sombreador de pixel, o sombreador de vértice só poderá usar a semântica de saída compatível com códigos FVF (formato de vértice \_ \_ flexível).</span><span class="sxs-lookup"><span data-stu-id="7a2da-108">In addition, if you are using a software-only vs\_3\_0 shader with a previous pixel shader version, the vertex shader can only use output semantics that are compatible with flexible vertex format (FVF) codes.</span></span>

<span data-ttu-id="7a2da-109">A semântica usada nas saídas do sombreador de vértice deve ser usada em entradas de sombreador de pixel.</span><span class="sxs-lookup"><span data-stu-id="7a2da-109">The semantics used on vertex shader outputs must be used on pixel shader inputs.</span></span> <span data-ttu-id="7a2da-110">A semântica é usada para mapear as saídas do sombreador de vértice para as entradas do sombreador de pixel, semelhante à maneira como a declaração de vértice é mapeada para os registros de entrada do sombreador de vértice e modelos de sombreador anteriores.</span><span class="sxs-lookup"><span data-stu-id="7a2da-110">The semantics are used to map the vertex shader outputs to the pixel shader inputs, similar to the way the vertex declaration is mapped to the vertex shader input registers and previous shader models.</span></span> <span data-ttu-id="7a2da-111">Consulte Semântica de corresponder em sombreadores vs 3.0 e ps 3.0.</span><span class="sxs-lookup"><span data-stu-id="7a2da-111">See Match Semantics on vs 3.0 and ps 3.0 Shaders.</span></span>

<span data-ttu-id="7a2da-112">Outros estados de renderização do modo de wrap foram adicionados para cobrir a possibilidade de coordenadas de textura adicionais nesse novo esquema.</span><span class="sxs-lookup"><span data-stu-id="7a2da-112">Additional wrap mode render states have been added to cover the possibility of additional texture coordinates in this new scheme.</span></span> <span data-ttu-id="7a2da-113">Atributos com D3DDECLUSAGE TEXCOORD e índice de uso de 0 a 15 são interpolados no modo de wrap quando o \_ [**\_ WRAP \* D3DRS**](/windows/desktop/direct3d9/d3drenderstatetype) correspondente é definido.</span><span class="sxs-lookup"><span data-stu-id="7a2da-113">Attributes with D3DDECLUSAGE\_TEXCOORD and usage index from 0 to 15 are interpolated in wrap mode when the corresponding [**D3DRS\_WRAP\***](/windows/desktop/direct3d9/d3drenderstatetype) is set.</span></span>

-   [<span data-ttu-id="7a2da-114">Recursos do Modelo 3 do Sombreador de Vértice</span><span class="sxs-lookup"><span data-stu-id="7a2da-114">Vertex Shader Model 3 Features</span></span>](#vertex-shader-model-3-features)
-   [<span data-ttu-id="7a2da-115">Recursos do Modelo 3 do Sombreador de Pixel</span><span class="sxs-lookup"><span data-stu-id="7a2da-115">Pixel Shader Model 3 Features</span></span>](#pixel-shader-model-3-features)
-   [<span data-ttu-id="7a2da-116">Corresponder semântica em \_ \_ versus 3 0 e ps \_ 3 \_ 0 Sombreadores</span><span class="sxs-lookup"><span data-stu-id="7a2da-116">Match Semantics on vs\_3\_0 and ps\_3\_0 Shaders</span></span>](/windows)
-   [<span data-ttu-id="7a2da-117">Alterações no modo de sombra, profundidade e sombreamento</span><span class="sxs-lookup"><span data-stu-id="7a2da-117">Fog, Depth, and Shading Mode Changes</span></span>](#fog-depth-and-shading-mode-changes)
-   [<span data-ttu-id="7a2da-118">Conversões de ponto flutuante e inteiro</span><span class="sxs-lookup"><span data-stu-id="7a2da-118">Floating Point and Integer Conversions</span></span>](#floating-point-and-integer-conversions)
-   [<span data-ttu-id="7a2da-119">Especificando precisão total ou parcial</span><span class="sxs-lookup"><span data-stu-id="7a2da-119">Specifying Full or Partial Precision</span></span>](#specifying-full-or-partial-precision)
-   [<span data-ttu-id="7a2da-120">Sombreadores de vértice e pixel de software</span><span class="sxs-lookup"><span data-stu-id="7a2da-120">Software Vertex and Pixel Shaders</span></span>](#software-vertex-and-pixel-shaders)

## <a name="vertex-shader-model-3-features"></a><span data-ttu-id="7a2da-121">Recursos do Modelo 3 do Sombreador de Vértice</span><span class="sxs-lookup"><span data-stu-id="7a2da-121">Vertex Shader Model 3 Features</span></span>

<span data-ttu-id="7a2da-122">Os tipos de registro de saída do sombreador de vértice foram recolhidos em doze registros (consulte [Registros de Saída](dx9-graphics-reference-asm-vs-registers-output.md)).</span><span class="sxs-lookup"><span data-stu-id="7a2da-122">The vertex shader output register types have been collapsed into twelve registers (see [Output Registers](dx9-graphics-reference-asm-vs-registers-output.md)).</span></span> <span data-ttu-id="7a2da-123">Cada registro usado precisa ser declarado usando a instrução [dcl](dcl-usage---ps.md) e uma semântica (por exemplo, dcl \_ color0 o0.xyzw).</span><span class="sxs-lookup"><span data-stu-id="7a2da-123">Each register that is used needs to be declared using the [dcl](dcl-usage---ps.md) instruction and a semantic (for example, dcl\_color0 o0.xyzw).</span></span>

<span data-ttu-id="7a2da-124">O modelo de sombreador de vértice 3 \_ 0 (versus 3 0) expande os recursos do vs 2 0 com indexação de registro mais eficiente, um conjunto de registros de saída simplificados, a capacidade de amostra de uma textura em um sombreador de vértice e a capacidade de controlar a taxa na qual as entradas do sombreador são \_ \_ \_ \_ inicializadas.</span><span class="sxs-lookup"><span data-stu-id="7a2da-124">The 3\_0 vertex shader model (vs\_3\_0) expands on the features of vs\_2\_0 with more powerful register indexing, a set of simplified output registers, the ability to sample a texture in a vertex shader, and the ability to control the rate at which shader inputs are initialized.</span></span>

### <a name="index-any-register"></a><span data-ttu-id="7a2da-125">Indexar qualquer registro</span><span class="sxs-lookup"><span data-stu-id="7a2da-125">Index Any Register</span></span>

<span data-ttu-id="7a2da-126">Todos os registros( [Registro de](dx9-graphics-reference-asm-vs-registers-input.md) Entrada e Registros de Saída [)](dx9-graphics-reference-asm-vs-registers-output.md)podem ser indexados usando o Registro de Contador de [Loop](dx9-graphics-reference-asm-vs-registers-loop-counter.md) (somente registros constantes podem ser indexados em versões anteriores.)</span><span class="sxs-lookup"><span data-stu-id="7a2da-126">All registers( [Input Register](dx9-graphics-reference-asm-vs-registers-input.md) and [Output Registers](dx9-graphics-reference-asm-vs-registers-output.md)) can be indexed using [Loop Counter Register](dx9-graphics-reference-asm-vs-registers-loop-counter.md) (only constant registers could be indexed in earlier versions.)</span></span>

<span data-ttu-id="7a2da-127">Você deve declarar registros de entrada e saída antes de indexá-los.</span><span class="sxs-lookup"><span data-stu-id="7a2da-127">You must declare input and output registers before indexing them.</span></span> <span data-ttu-id="7a2da-128">No entanto, você não pode indexar nenhum registro de saída que tenha sido declarado com uma semântica de tamanho de posição ou ponto.</span><span class="sxs-lookup"><span data-stu-id="7a2da-128">However, you may not index any output register that has been declared with a position or point size semantic.</span></span> <span data-ttu-id="7a2da-129">Na verdade, se a indexação for usada, a posição e a semântica de psize deverão ser declaradas nos registros o0 e o1, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="7a2da-129">In fact, if indexing is used the position and psize semantics have to be declared in the o0 and o1 registers respectively.</span></span>

<span data-ttu-id="7a2da-130">Você só tem permissão para indexar um intervalo contínuo de registros; ou seja, você não pode indexar entre registros que não foram declarados.</span><span class="sxs-lookup"><span data-stu-id="7a2da-130">You are only allowed to index a continuous range of registers; that is, you cannot index across registers that have not been declared.</span></span> <span data-ttu-id="7a2da-131">Embora essa restrição possa ser inconveniente, ela permite que a otimização de hardware seja realizada.</span><span class="sxs-lookup"><span data-stu-id="7a2da-131">While this restriction may be inconvenient, it permits hardware optimization to take place.</span></span> <span data-ttu-id="7a2da-132">A tentativa de indexar entre registros não contíguos produzirá resultados indefinido.</span><span class="sxs-lookup"><span data-stu-id="7a2da-132">Attempting to index across non-contiguous registers will produce undefined results.</span></span> <span data-ttu-id="7a2da-133">A validação do sombreador não impõe essa restrição.</span><span class="sxs-lookup"><span data-stu-id="7a2da-133">Shader validation does not enforce this restriction.</span></span>

### <a name="simplify-output-registers"></a><span data-ttu-id="7a2da-134">Simplificar registros de saída</span><span class="sxs-lookup"><span data-stu-id="7a2da-134">Simplify Output Registers</span></span>

<span data-ttu-id="7a2da-135">Todos os vários tipos de registros de saída foram recolhidos em doze registros de saída: 1 para posição, 2 para cor, 8 para textura e 1 para tamanho do ponto ou da bola.</span><span class="sxs-lookup"><span data-stu-id="7a2da-135">All the various types of output registers have been collapsed into twelve output registers: 1 for position, 2 for color, 8 for texture, and 1 for fog or point size.</span></span> <span data-ttu-id="7a2da-136">Esses registros interpolarão todos os dados que eles contêm para o sombreador de pixel.</span><span class="sxs-lookup"><span data-stu-id="7a2da-136">These registers will interpolate any data they contain for the pixel shader.</span></span> <span data-ttu-id="7a2da-137">As declarações de registro de saída são necessárias e a semântica é atribuída a cada registro.</span><span class="sxs-lookup"><span data-stu-id="7a2da-137">Output register declarations are required and semantics are assigned to each register.</span></span>

<span data-ttu-id="7a2da-138">Os registros podem ser divididos da seguinte forma:</span><span class="sxs-lookup"><span data-stu-id="7a2da-138">The registers can be broken down as follows:</span></span>

-   <span data-ttu-id="7a2da-139">Pelo menos um registro deve ser declarado como um registro de posição de quatro componentes.</span><span class="sxs-lookup"><span data-stu-id="7a2da-139">At least one register must be declared as a four-component position register.</span></span> <span data-ttu-id="7a2da-140">Esse é o único registro de sombreador de vértice necessário.</span><span class="sxs-lookup"><span data-stu-id="7a2da-140">This is the only vertex shader register that is required.</span></span>
-   <span data-ttu-id="7a2da-141">Os dez primeiros registros consumidos por um sombreador podem usar até quatro componentes (xyzw) máximo.</span><span class="sxs-lookup"><span data-stu-id="7a2da-141">The first ten registers consumed by a shader may use up to four components (xyzw) maximum.</span></span>
-   <span data-ttu-id="7a2da-142">O último (ou décimo segundo) registro pode conter apenas um escalar (como tamanho de ponto).</span><span class="sxs-lookup"><span data-stu-id="7a2da-142">The last (or twelfth) register may only contain a scalar (such as point size).</span></span>

<span data-ttu-id="7a2da-143">Para ver uma listagem dos registros, consulte [Registros – \_ versus 3 \_ 0](dx9-graphics-reference-asm-vs-registers-vs-3-0.md).</span><span class="sxs-lookup"><span data-stu-id="7a2da-143">For a listing of the registers, see [Registers - vs\_3\_0](dx9-graphics-reference-asm-vs-registers-vs-3-0.md).</span></span>

### <a name="texture-sample-in-a-vertex-shader"></a><span data-ttu-id="7a2da-144">Amostra de textura em um sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="7a2da-144">Texture Sample in a Vertex Shader</span></span>

<span data-ttu-id="7a2da-145">O sombreador de vértice 3 0 dá suporte à lookup de textura no sombreador de \_ vértice usando [o texldl – vs](texldl---vs.md).</span><span class="sxs-lookup"><span data-stu-id="7a2da-145">Vertex shader 3\_0 supports texture lookup in the vertex shader using [texldl - vs](texldl---vs.md).</span></span>

## <a name="pixel-shader-model-3-features"></a><span data-ttu-id="7a2da-146">Recursos do Modelo 3 do Sombreador de Pixel</span><span class="sxs-lookup"><span data-stu-id="7a2da-146">Pixel Shader Model 3 Features</span></span>

<span data-ttu-id="7a2da-147">Os registros de cor e textura do sombreador de pixel foram recolhidos em dez registros de entrada (consulte [Tipos de registro de entrada](dx9-graphics-reference-asm-ps-registers-ps-3-0.md)).</span><span class="sxs-lookup"><span data-stu-id="7a2da-147">The pixel shader color and texture registers have been collapsed into ten input registers (see [Input Register Types](dx9-graphics-reference-asm-ps-registers-ps-3-0.md)).</span></span> <span data-ttu-id="7a2da-148">O Registro Facial é um registro escalar de ponto flutuante.</span><span class="sxs-lookup"><span data-stu-id="7a2da-148">The Face Register is a floating point scalar register.</span></span> <span data-ttu-id="7a2da-149">Somente o sinal desse registro é válido.</span><span class="sxs-lookup"><span data-stu-id="7a2da-149">Only the sign of this register is valid.</span></span> <span data-ttu-id="7a2da-150">Se o sinal for negativo, o primitivo será uma face traseira.</span><span class="sxs-lookup"><span data-stu-id="7a2da-150">If the sign is negative the primitive is a back face.</span></span> <span data-ttu-id="7a2da-151">Isso pode ser usado dentro de um sombreador de pixel para obter iluminação de dois lados, por exemplo.</span><span class="sxs-lookup"><span data-stu-id="7a2da-151">This can be used inside a pixel shader to achieve two-sided lighting, for instance.</span></span> <span data-ttu-id="7a2da-152">O Registro de Posição faz referência aos pixels atuais (x,y).</span><span class="sxs-lookup"><span data-stu-id="7a2da-152">The Position Register references the current (x,y) pixels.</span></span>

<span data-ttu-id="7a2da-153">Os registros constantes do sombreador podem ser definidos usando:</span><span class="sxs-lookup"><span data-stu-id="7a2da-153">The shader constant registers can be set using:</span></span>

-   [<span data-ttu-id="7a2da-154">**SetPixelShaderConstantB**</span><span class="sxs-lookup"><span data-stu-id="7a2da-154">**SetPixelShaderConstantB**</span></span>](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantb)
-   [<span data-ttu-id="7a2da-155">**SetPixelShaderConstantI**</span><span class="sxs-lookup"><span data-stu-id="7a2da-155">**SetPixelShaderConstantI**</span></span>](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstanti)
-   [<span data-ttu-id="7a2da-156">**SetPixelShaderConstantF**</span><span class="sxs-lookup"><span data-stu-id="7a2da-156">**SetPixelShaderConstantF**</span></span>](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantf)

## <a name="match-semantics-on-vs_3_0-and-ps_3_0-shaders"></a><span data-ttu-id="7a2da-157">Corresponder semântica em \_ \_ versus 3 0 e ps \_ 3 \_ 0 Sombreadores</span><span class="sxs-lookup"><span data-stu-id="7a2da-157">Match Semantics on vs\_3\_0 and ps\_3\_0 Shaders</span></span>

<span data-ttu-id="7a2da-158">Há algumas restrições de uso semântico com vs \_ 3 \_ 0 e ps \_ 3 \_ 0.</span><span class="sxs-lookup"><span data-stu-id="7a2da-158">There are some restrictions on semantic usage with vs\_3\_0 and ps\_3\_0.</span></span> <span data-ttu-id="7a2da-159">Em geral, você precisa ter cuidado ao usar uma semântica para uma entrada de sombreador que corresponde a uma semântica usada em uma saída do sombreador.</span><span class="sxs-lookup"><span data-stu-id="7a2da-159">In general, you need to be careful when using a semantic for a shader input that matches a semantic used on a shader output.</span></span>

<span data-ttu-id="7a2da-160">Por exemplo, esse sombreador de pixel empacota vários nomes em um registro:</span><span class="sxs-lookup"><span data-stu-id="7a2da-160">For instance, this pixel shader packs multiple names into one register:</span></span>


```
ps_3_0 
dcl_texcoord0 v0.x 
dcl_texcoord1 v0.yz // Valid to pack multiple names into one register 
dcl_texcoord2_centroid v1.w
...
```



<span data-ttu-id="7a2da-161">Cada registro tem uma semântica diferente.</span><span class="sxs-lookup"><span data-stu-id="7a2da-161">Each register has a different semantic.</span></span> <span data-ttu-id="7a2da-162">Observe que você também pode nomear v0.x e v0.yz com semântica diferente (várias) devido ao uso da máscara de gravação.</span><span class="sxs-lookup"><span data-stu-id="7a2da-162">Notice that you can also name v0.x and v0.yz with different (multiple) semantics because of the use of the write mask.</span></span>

<span data-ttu-id="7a2da-163">Considerando o sombreador de pixel, o seguinte sombreador \_ \_ versus 3 0 não pode ser emparelhado com ele:</span><span class="sxs-lookup"><span data-stu-id="7a2da-163">Given the pixel shader, the following vs\_3\_0 shader cannot be paired with it:</span></span>


```
vs_3_0 
... 
dcl_texcoord0 o5.x 
dcl_texcoord1 o6.yzw 
...
```



<span data-ttu-id="7a2da-164">Esses dois sombreadores estão em conflito com o uso da semântica [**D3DDECLUSAGE \_ TEXCOORD0**](/windows/desktop/direct3d9/d3ddeclusage) e **D3DDECLUSAGE \_ TEXCOORD1.**</span><span class="sxs-lookup"><span data-stu-id="7a2da-164">These two shaders conflict with their use of the [**D3DDECLUSAGE\_TEXCOORD0**](/windows/desktop/direct3d9/d3ddeclusage) And **D3DDECLUSAGE\_TEXCOORD1** semantics.</span></span>

<span data-ttu-id="7a2da-165">Reescreva o sombreador de vértice como este para evitar a colisão semântica:</span><span class="sxs-lookup"><span data-stu-id="7a2da-165">Rewrite the vertex shader like this to avoid the semantic collision:</span></span>


```
vs_3_0 
... 
dcl_texcoord2 o3 
dcl_texcoord3 o9 
...
```



<span data-ttu-id="7a2da-166">Da mesma forma, um nome semântico declarado em diferentes registros de entrada no sombreador de pixel (v0 e v1 no sombreador de pixel) não pode ser usado em um único registro de saída nesse sombreador de vértice.</span><span class="sxs-lookup"><span data-stu-id="7a2da-166">Similarly, a semantic name declared on different input registers in the pixel shader (v0 and v1 in the pixel shader) cannot be used in a single output register in this vertex shader.</span></span> <span data-ttu-id="7a2da-167">Por exemplo, esse sombreador de vértice não pode ser emparelhado com o sombreador de pixel porque D3DDECLUSAGE TEXCOORD1 é usado para registros de entrada do sombreador de pixel (v0, v1) e o registro de saída do sombreador de \_ vértice o3.</span><span class="sxs-lookup"><span data-stu-id="7a2da-167">For instance, this vertex shader cannot be paired with the pixel shader because D3DDECLUSAGE\_TEXCOORD1 is used for both pixel shader input registers (v0, v1) and the vertex shader output register o3.</span></span>


```
vs_3_0 
... 
dcl_texcoord0 o3.x 
dcl_texcoord1 o3.yz 

dcl_texcoord2 o3.w // BAD! Would be valid if this were not o3 
dcl_texcoord3 o9 ... 
```



<span data-ttu-id="7a2da-168">Por outro lado, esse sombreador de vértice não pode ser emparelhado com o sombreador de pixel porque a máscara de saída para um parâmetro com uma determinada semântica não fornece os dados solicitados pelo sombreador de pixel:</span><span class="sxs-lookup"><span data-stu-id="7a2da-168">On the other hand, this vertex shader cannot be paired with the pixel shader because the output mask for a parameter with a given semantic does not provide the data that is requested by the pixel shader:</span></span>


```
vs_3_0 
... 
dcl_texcoord0 o5.x 
dcl_texcoord1 o5.yzw 
dcl_texcoord2 o7.yz // BAD! Would be valid if w were included 
dcl_texcoord3 o9 
... 
```



<span data-ttu-id="7a2da-169">Esse sombreador de vértice não fornece uma saída com um dos nomes semânticos solicitados pelo sombreador de pixel, portanto, o emparelhamento do sombreador é inválido:</span><span class="sxs-lookup"><span data-stu-id="7a2da-169">This vertex shader does not provide an output with one of the semantic names requested by the pixel shader, so the shader pairing is invalid:</span></span>


```
vs_3_0 
... 
dcl_texcoord0 o5.x 
dcl_texcoord1 o5.yzw 
dcl_texcoord3 o9 
// The pixel shader wants texcoord2, with a w component, 
// but it isn't output by this vertex shader at all! 
... 
```



## <a name="fog-depth-and-shading-mode-changes"></a><span data-ttu-id="7a2da-170">Alterações no modo de sombra, profundidade e sombreamento</span><span class="sxs-lookup"><span data-stu-id="7a2da-170">Fog, Depth, and Shading Mode Changes</span></span>

<span data-ttu-id="7a2da-171">Quando D3DRS SHADEMODE é definido para sombreamento simples durante a rasterização de recorte e triângulo, os atributos com \_ D3DDECLUSAGE COLOR são interpolados como \_ sombreados simples.</span><span class="sxs-lookup"><span data-stu-id="7a2da-171">When D3DRS\_SHADEMODE is set for flat shading during clipping and triangle rasterization, attributes with D3DDECLUSAGE\_COLOR are interpolated as flat shaded.</span></span> <span data-ttu-id="7a2da-172">Se qualquer componente de um registro for declarado com uma semântica de cor, mas outros componentes do mesmo registro receberem semântica diferente, a interpolação de sombreamento simples (linear versus simples) será indefinida nos componentes que se registram sem uma semântica de cores.</span><span class="sxs-lookup"><span data-stu-id="7a2da-172">If any components of a register are declared with a color semantic but other components of the same register are given different semantics, flat shading interpolation (linear vs. flat) will be undefined on the components in that register without a color semantic.</span></span>

<span data-ttu-id="7a2da-173">Se a renderização de replicação for desejada, os sombreadores vs \_ 3 0 e \_ ps \_ 3 \_ 0 deverão implementar o torção.</span><span class="sxs-lookup"><span data-stu-id="7a2da-173">If fog rendering is desired, vs\_3\_0 and ps\_3\_0 shaders must implement fog.</span></span> <span data-ttu-id="7a2da-174">Nenhum cálculo de lodo é feito fora dos sombreadores.</span><span class="sxs-lookup"><span data-stu-id="7a2da-174">No fog calculations are done outside of the shaders.</span></span> <span data-ttu-id="7a2da-175">Não há nenhum registro de cinza em versus 3 0, e a semântica adicional D3DDECLUSAGE CHAP (para fator de combinação de blend computada por \_ \_ \_ vértice) e D3DDECLUSAGE DEPTH (para passar um valor de profundidade para o sombreador de pixel para calcular o fator de mesclagem de \_ mesclagem) foram adicionadas.</span><span class="sxs-lookup"><span data-stu-id="7a2da-175">There is no fog register in vs\_3\_0, and additional semantics D3DDECLUSAGE\_FOG (for fog blend factor computed per vertex) and D3DDECLUSAGE\_DEPTH (for passing in a depth value to the pixel shader to compute the fog blend factor) have been added.</span></span>

<span data-ttu-id="7a2da-176">O estado do estágio de textura D3DTSS \_ TEXCOORDINDEX é ignorado ao usar o sombreador de pixel 3.0.</span><span class="sxs-lookup"><span data-stu-id="7a2da-176">Texture stage state D3DTSS\_TEXCOORDINDEX is ignored when using pixel shader 3.0.</span></span>

<span data-ttu-id="7a2da-177">Os seguintes valores foram adicionados para acomodar essas alterações:</span><span class="sxs-lookup"><span data-stu-id="7a2da-177">The following values have been added to accommodate these changes:</span></span>


```
// Fog and Depth usages
D3DDECLUSAGE_FOG 
D3DDECLUSAGE_DEPTH 

// Additional wrap states for vs_3_0 attributes with D3DDECLUSAGE_TEXCOORD 
D3DRS_WRAP8 
D3DRS_WRAP9 
D3DRS_WRAP10 
D3DRS_WRAP11 
D3DRS_WRAP12 
D3DRS_WRAP13 
D3DRS_WRAP14 
D3DRS_WRAP15
```



## <a name="floating-point-and-integer-conversions"></a><span data-ttu-id="7a2da-178">Conversões de ponto flutuante e inteiro</span><span class="sxs-lookup"><span data-stu-id="7a2da-178">Floating Point and Integer Conversions</span></span>

<span data-ttu-id="7a2da-179">A matemática de ponto flutuante ocorre em diferentes precisões e intervalos (16 bits, 24 bits e 32 bits) em diferentes partes do pipeline.</span><span class="sxs-lookup"><span data-stu-id="7a2da-179">Floating point math happens at different precision and ranges (16-bit, 24-bit, and 32-bit) in different parts of the pipeline.</span></span> <span data-ttu-id="7a2da-180">Um valor maior que o intervalo dinâmico do pipeline que entra nesse pipeline (por exemplo, um mapa de textura float de 32 bits é amostrado em um pipeline float de 24 bits em ps 2 0) cria um resultado \_ \_ indefinido.</span><span class="sxs-lookup"><span data-stu-id="7a2da-180">A value greater than the dynamic range of the pipeline that enters that pipeline (for example, a 32-bit float texture map is sampled into a 24-bit float pipeline in ps\_2\_0) creates an undefined result.</span></span> <span data-ttu-id="7a2da-181">Para um comportamento previsível, você deve fixar esse valor no intervalo dinâmico máximo.</span><span class="sxs-lookup"><span data-stu-id="7a2da-181">For predictable behavior, you should clamp such a value to the dynamic range maximum.</span></span>

<span data-ttu-id="7a2da-182">A conversão de um valor de ponto flutuante em um inteiro ocorre em vários locais, como:</span><span class="sxs-lookup"><span data-stu-id="7a2da-182">Conversion from a floating point value to an integer happens in several places such as:</span></span>

-   <span data-ttu-id="7a2da-183">Ao encontrar um [mova - vs instrução.](mova---vs.md)</span><span class="sxs-lookup"><span data-stu-id="7a2da-183">When encountering a [mova - vs](mova---vs.md) instruction.</span></span>
-   <span data-ttu-id="7a2da-184">Durante o endereçamento de textura.</span><span class="sxs-lookup"><span data-stu-id="7a2da-184">During texture addressing.</span></span>
-   <span data-ttu-id="7a2da-185">Ao escrever em um destino de renderização de ponto não flutuante.</span><span class="sxs-lookup"><span data-stu-id="7a2da-185">When writing out to a non-floating point render target.</span></span>

## <a name="specifying-full-or-partial-precision"></a><span data-ttu-id="7a2da-186">Especificando precisão total ou parcial</span><span class="sxs-lookup"><span data-stu-id="7a2da-186">Specifying Full or Partial Precision</span></span>

<span data-ttu-id="7a2da-187">Ps \_ 3 \_ 0 e ps 2 x dão \_ suporte a dois níveis de \_ precisão:</span><span class="sxs-lookup"><span data-stu-id="7a2da-187">Both ps\_3\_0 and ps\_2\_x provide support for two levels of precision:</span></span>



| <span data-ttu-id="7a2da-188">ps \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="7a2da-188">ps\_3\_0</span></span> | <span data-ttu-id="7a2da-189">ps \_ 2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="7a2da-189">ps\_2\_0</span></span> | <span data-ttu-id="7a2da-190">Precisão</span><span class="sxs-lookup"><span data-stu-id="7a2da-190">Precision</span></span>         | <span data-ttu-id="7a2da-191">Valor</span><span class="sxs-lookup"><span data-stu-id="7a2da-191">Value</span></span>                |
|----------|----------|-------------------|----------------------|
| <span data-ttu-id="7a2da-192">x</span><span class="sxs-lookup"><span data-stu-id="7a2da-192">x</span></span>        |          | <span data-ttu-id="7a2da-193">Completo</span><span class="sxs-lookup"><span data-stu-id="7a2da-193">Full</span></span>              | <span data-ttu-id="7a2da-194">fp32 ou superior</span><span class="sxs-lookup"><span data-stu-id="7a2da-194">fp32 or higher</span></span>       |
| <span data-ttu-id="7a2da-195">x</span><span class="sxs-lookup"><span data-stu-id="7a2da-195">x</span></span>        |          | <span data-ttu-id="7a2da-196">Precisão parcial</span><span class="sxs-lookup"><span data-stu-id="7a2da-196">Partial precision</span></span> | <span data-ttu-id="7a2da-197">fp16=s10e5</span><span class="sxs-lookup"><span data-stu-id="7a2da-197">fp16=s10e5</span></span>           |
| <span data-ttu-id="7a2da-198">x</span><span class="sxs-lookup"><span data-stu-id="7a2da-198">x</span></span>        | <span data-ttu-id="7a2da-199">x</span><span class="sxs-lookup"><span data-stu-id="7a2da-199">x</span></span>        | <span data-ttu-id="7a2da-200">Completo</span><span class="sxs-lookup"><span data-stu-id="7a2da-200">Full</span></span>              | <span data-ttu-id="7a2da-201">fp24 = s16e7 ou superior</span><span class="sxs-lookup"><span data-stu-id="7a2da-201">fp24=s16e7 or higher</span></span> |
| <span data-ttu-id="7a2da-202">x</span><span class="sxs-lookup"><span data-stu-id="7a2da-202">x</span></span>        | <span data-ttu-id="7a2da-203">x</span><span class="sxs-lookup"><span data-stu-id="7a2da-203">x</span></span>        | <span data-ttu-id="7a2da-204">Precisão parcial</span><span class="sxs-lookup"><span data-stu-id="7a2da-204">Partial precision</span></span> | <span data-ttu-id="7a2da-205">FP16 = s10e5</span><span class="sxs-lookup"><span data-stu-id="7a2da-205">fp16=s10e5</span></span>           |



 

<span data-ttu-id="7a2da-206">\_o PS 3 \_ 0 dá suporte a mais precisão do que \_ o PS 2 \_ 0.</span><span class="sxs-lookup"><span data-stu-id="7a2da-206">ps\_3\_0 supports more precision than ps\_2\_0 does.</span></span> <span data-ttu-id="7a2da-207">Por padrão, todas as operações ocorrem no nível de precisão total.</span><span class="sxs-lookup"><span data-stu-id="7a2da-207">By default, all operations occur at the full precision level.</span></span>

<span data-ttu-id="7a2da-208">A precisão parcial (consulte [modificadores de registro de sombreador de pixel](dx9-graphics-reference-asm-ps-registers-modifiers.md)) é solicitada adicionando o \_ modificador PP ao código do sombreador (desde que a implementação subjacente ofereça suporte a ela).</span><span class="sxs-lookup"><span data-stu-id="7a2da-208">Partial precision (see [Pixel Shader Register Modifiers](dx9-graphics-reference-asm-ps-registers-modifiers.md)) is requested by adding the \_pp modifier to shader code (provided that the underlying implementation supports it).</span></span> <span data-ttu-id="7a2da-209">As implementações sempre são gratuitas para ignorar o modificador e executar as operações afetadas com precisão total.</span><span class="sxs-lookup"><span data-stu-id="7a2da-209">Implementations are always free to ignore the modifier and perform the affected operations in full precision.</span></span>

<span data-ttu-id="7a2da-210">O \_ modificador PP pode ocorrer em dois contextos:</span><span class="sxs-lookup"><span data-stu-id="7a2da-210">The \_pp modifier can occur in two contexts:</span></span>

-   <span data-ttu-id="7a2da-211">Em uma declaração de coordenada de textura para passar coordenadas de textura de precisão parcial para o sombreador de pixel.</span><span class="sxs-lookup"><span data-stu-id="7a2da-211">On a texture coordinate declaration to pass partial-precision texture coordinates to the pixel shader.</span></span> <span data-ttu-id="7a2da-212">Isso pode ser usado quando a textura coordena dados de cores de retransmissão para o sombreador de pixel, que pode ser mais rápido com precisão parcial do que com precisão total em algumas implementações.</span><span class="sxs-lookup"><span data-stu-id="7a2da-212">This could be used when texture coordinates relay color data to the pixel shader, which may be faster with partial precision than with full precision in some implementations.</span></span>
-   <span data-ttu-id="7a2da-213">Em qualquer instrução para solicitar o uso de precisão parcial, incluindo instruções de carga de textura.</span><span class="sxs-lookup"><span data-stu-id="7a2da-213">On any instruction to request the use of partial precision, including texture load instructions.</span></span> <span data-ttu-id="7a2da-214">Isso indica que a implementação tem permissão para executar a instrução com precisão parcial e armazenar um resultado de precisão parcial.</span><span class="sxs-lookup"><span data-stu-id="7a2da-214">This indicates that the implementation is allowed to execute the instruction with partial precision and store a partial-precision result.</span></span> <span data-ttu-id="7a2da-215">Na ausência de um modificador explícito, a instrução deve ser executada com precisão total (independentemente da precisão dos operandos de entrada).</span><span class="sxs-lookup"><span data-stu-id="7a2da-215">In the absence of an explicit modifier, the instruction must be performed at full precision (regardless of the precision of the input operands).</span></span>

<span data-ttu-id="7a2da-216">Um aplicativo pode deliberadamente optar por compensar a precisão do desempenho.</span><span class="sxs-lookup"><span data-stu-id="7a2da-216">An application might deliberately choose to trade off precision for performance.</span></span> <span data-ttu-id="7a2da-217">Há vários tipos de dados de entrada de sombreador que são candidatos naturais para processamento de precisão parcial:</span><span class="sxs-lookup"><span data-stu-id="7a2da-217">There are several kinds of shader input data which are natural candidates for partial precision processing:</span></span>

-   <span data-ttu-id="7a2da-218">Os iteradores de cor são bem representados por valores de precisão parcial.</span><span class="sxs-lookup"><span data-stu-id="7a2da-218">Color iterators are well represented by partial-precision values.</span></span>
-   <span data-ttu-id="7a2da-219">Os valores de textura da maioria dos formatos podem ser representados com precisão pelos valores de precisão parcial (os valores amostrados de 32 bits, texturas de formato de ponto flutuante são uma exceção óbvia).</span><span class="sxs-lookup"><span data-stu-id="7a2da-219">Texture values from most formats can be accurately represented by partial-precision values (values sampled from 32-bit, floating-point format textures are an obvious exception).</span></span>
-   <span data-ttu-id="7a2da-220">As constantes podem ser representadas pela representação de precisão parcial, conforme apropriado para o sombreador.</span><span class="sxs-lookup"><span data-stu-id="7a2da-220">Constants may be represented by partial-precision representation as appropriate to the shader.</span></span>

<span data-ttu-id="7a2da-221">Em todos esses casos, o desenvolvedor pode optar por especificar a precisão parcial para processar os dados, sabendo que nenhuma precisão de dados de entrada é perdida.</span><span class="sxs-lookup"><span data-stu-id="7a2da-221">In all these cases the developer may choose to specify partial precision to process the data, knowing that no input data precision is lost.</span></span> <span data-ttu-id="7a2da-222">Em alguns casos, um sombreador pode exigir que as etapas internas de um cálculo sejam executadas com precisão total mesmo quando os valores de entrada e saída final não tiverem mais do que a precisão parcial.</span><span class="sxs-lookup"><span data-stu-id="7a2da-222">In some cases, a shader may require that the internal steps of a calculation be performed at full precision even when input and final output values do not have more than partial precision.</span></span>

## <a name="software-vertex-and-pixel-shaders"></a><span data-ttu-id="7a2da-223">Vértice de software e sombreadores de pixel</span><span class="sxs-lookup"><span data-stu-id="7a2da-223">Software Vertex and Pixel Shaders</span></span>

<span data-ttu-id="7a2da-224">Implementações de software (tempo de execução e referência para sombreadores de vértice e referência para sombreadores de pixel) dos sombreadores da versão 2 \_ 0 e acima têm alguma validação relaxada.</span><span class="sxs-lookup"><span data-stu-id="7a2da-224">Software implementations (run-time and reference for vertex shaders and reference for pixel shaders) of version 2\_0 shaders and above have some validation relaxed.</span></span> <span data-ttu-id="7a2da-225">Isso é útil para fins de depuração e protótipos.</span><span class="sxs-lookup"><span data-stu-id="7a2da-225">This is useful for debugging and prototyping purposes.</span></span> <span data-ttu-id="7a2da-226">O aplicativo indica ao tempo de execução/Assembler que ele precisa de uma validação relaxada usando o \_ sinalizador SW no assembler (por exemplo, vs \_ 2 \_ SW).</span><span class="sxs-lookup"><span data-stu-id="7a2da-226">The application indicates to the runtime/assembler that it needs some of the validation relaxed using the \_sw flag in the assembler (for example, vs\_2\_sw).</span></span> <span data-ttu-id="7a2da-227">Um sombreador de software não funcionará com hardware.</span><span class="sxs-lookup"><span data-stu-id="7a2da-227">A software shader will not work with hardware.</span></span>

<span data-ttu-id="7a2da-228">\_o vs 2 \_ SW é um relaxamento até o máximo de Caps de vs \_ 2 \_ x; da mesma forma, \_ o SW de PS 2 \_ é um relaxamento para o máximo de Caps de PS \_ 2 \_ x.</span><span class="sxs-lookup"><span data-stu-id="7a2da-228">vs\_2\_sw is a relaxation to the maximum caps of vs\_2\_x; similarly, ps\_2\_sw is a relaxation to the maximum caps of ps\_2\_x.</span></span> <span data-ttu-id="7a2da-229">Especificamente, as seguintes validações são relaxadas:</span><span class="sxs-lookup"><span data-stu-id="7a2da-229">Specifically, the following validations are relaxed:</span></span>



| <span data-ttu-id="7a2da-230">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="7a2da-230">Shader model</span></span>                                           |  <span data-ttu-id="7a2da-231">Recurso</span><span class="sxs-lookup"><span data-stu-id="7a2da-231">Resource</span></span>                                    |  <span data-ttu-id="7a2da-232">Limite</span><span class="sxs-lookup"><span data-stu-id="7a2da-232">Limit</span></span>                                                                                                                                  |
|--------------------------------------------|--------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a2da-233">vs \_ 2 \_ SW, vs \_ 3 \_ SW, PS \_ 2 \_ SW, PS \_ 3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="7a2da-233">vs\_2\_sw, vs\_3\_sw, ps\_2\_sw, ps\_3\_sw</span></span> | <span data-ttu-id="7a2da-234">Contagens de instruções</span><span class="sxs-lookup"><span data-stu-id="7a2da-234">Instruction Counts</span></span>                   | <span data-ttu-id="7a2da-235">Ilimitado</span><span class="sxs-lookup"><span data-stu-id="7a2da-235">Unlimited</span></span>                                                                                                                         |
| <span data-ttu-id="7a2da-236">vs \_ 2 \_ SW, vs \_ 3 \_ SW, PS \_ 2 \_ SW, PS \_ 3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="7a2da-236">vs\_2\_sw, vs\_3\_sw, ps\_2\_sw, ps\_3\_sw</span></span> | <span data-ttu-id="7a2da-237">Registros de constante float</span><span class="sxs-lookup"><span data-stu-id="7a2da-237">Float Constant Registers</span></span>             | <span data-ttu-id="7a2da-238">8192</span><span class="sxs-lookup"><span data-stu-id="7a2da-238">8192</span></span>                                                                                                                              |
| <span data-ttu-id="7a2da-239">vs \_ 2 \_ SW, vs \_ 3 \_ SW, PS \_ 2 \_ SW, PS \_ 3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="7a2da-239">vs\_2\_sw, vs\_3\_sw, ps\_2\_sw, ps\_3\_sw</span></span> | <span data-ttu-id="7a2da-240">Registros de constante de inteiro</span><span class="sxs-lookup"><span data-stu-id="7a2da-240">Integer Constant Registers</span></span>           | <span data-ttu-id="7a2da-241">2.048</span><span class="sxs-lookup"><span data-stu-id="7a2da-241">2048</span></span>                                                                                                                              |
| <span data-ttu-id="7a2da-242">vs \_ 2 \_ SW, vs \_ 3 \_ SW, PS \_ 2 \_ SW, PS \_ 3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="7a2da-242">vs\_2\_sw, vs\_3\_sw, ps\_2\_sw, ps\_3\_sw</span></span> | <span data-ttu-id="7a2da-243">Registros constantes boolianos</span><span class="sxs-lookup"><span data-stu-id="7a2da-243">Boolean Constant Registers</span></span>           | <span data-ttu-id="7a2da-244">2.048</span><span class="sxs-lookup"><span data-stu-id="7a2da-244">2048</span></span>                                                                                                                              |
| <span data-ttu-id="7a2da-245">PS \_ 2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="7a2da-245">ps\_2\_sw</span></span>                                  | <span data-ttu-id="7a2da-246">Dependente-ler profundidade</span><span class="sxs-lookup"><span data-stu-id="7a2da-246">Dependent-read depth</span></span>                 | <span data-ttu-id="7a2da-247">Ilimitado</span><span class="sxs-lookup"><span data-stu-id="7a2da-247">Unlimited</span></span>                                                                                                                         |
| <span data-ttu-id="7a2da-248">vs \_ 2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="7a2da-248">vs\_2\_sw</span></span>                                  | <span data-ttu-id="7a2da-249">instruções e rótulos de controle de fluxo</span><span class="sxs-lookup"><span data-stu-id="7a2da-249">flow control instructions and labels</span></span> | <span data-ttu-id="7a2da-250">Ilimitado</span><span class="sxs-lookup"><span data-stu-id="7a2da-250">Unlimited</span></span>                                                                                                                         |
| <span data-ttu-id="7a2da-251">vs \_ 2 \_ SW, vs \_ 3 \_ SW, PS \_ 2 \_ SW, PS \_ 3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="7a2da-251">vs\_2\_sw, vs\_3\_sw, ps\_2\_sw, ps\_3\_sw</span></span> | <span data-ttu-id="7a2da-252">Início/etapa/contagens de loop</span><span class="sxs-lookup"><span data-stu-id="7a2da-252">Loop start/step/counts</span></span>               | <span data-ttu-id="7a2da-253">O tamanho da etapa de início e iteração da iteração para instruções de rep e loop são inteiros com sinal de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="7a2da-253">Iteration start and iteration step size for rep and loop instructions are 32-bit signed integers.</span></span> <span data-ttu-id="7a2da-254">A contagem pode ser até o máximo \_ int/64.</span><span class="sxs-lookup"><span data-stu-id="7a2da-254">Count can be up to MAX\_INT/64.</span></span> |
| <span data-ttu-id="7a2da-255">vs \_ 2 \_ SW, vs \_ 3 \_ SW, PS \_ 2 \_ SW, PS \_ 3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="7a2da-255">vs\_2\_sw, vs\_3\_sw, ps\_2\_sw, ps\_3\_sw</span></span> | <span data-ttu-id="7a2da-256">Limites de porta</span><span class="sxs-lookup"><span data-stu-id="7a2da-256">Port limits</span></span>                          | <span data-ttu-id="7a2da-257">Os limites de porta para todos os arquivos de registro são relaxados.</span><span class="sxs-lookup"><span data-stu-id="7a2da-257">Port limits for all register files are relaxed.</span></span>                                                                                   |
| <span data-ttu-id="7a2da-258">vs \_ 3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="7a2da-258">vs\_3\_sw</span></span>                                  | <span data-ttu-id="7a2da-259">Número de interpoladores</span><span class="sxs-lookup"><span data-stu-id="7a2da-259">Number of interpolators</span></span>              | <span data-ttu-id="7a2da-260">16 registros de saída no vs \_ 3 \_ SW.</span><span class="sxs-lookup"><span data-stu-id="7a2da-260">16 output registers in vs\_3\_sw.</span></span>                                                                                                 |
| <span data-ttu-id="7a2da-261">PS \_ 3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="7a2da-261">ps\_3\_sw</span></span>                                  | <span data-ttu-id="7a2da-262">Número de interpoladores</span><span class="sxs-lookup"><span data-stu-id="7a2da-262">Number of interpolators</span></span>              | <span data-ttu-id="7a2da-263">14 (16-2) registros de entrada para \_ o \_ software PS 3 SW.</span><span class="sxs-lookup"><span data-stu-id="7a2da-263">14(16-2) input registers for ps\_3\_sw.</span></span>                                                                                           |



 

## <a name="related-topics"></a><span data-ttu-id="7a2da-264">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7a2da-264">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7a2da-265">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7a2da-265">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md)
</dt> </dl>

 

 
