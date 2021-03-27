---
title: texkill-PS
description: Cancela a renderização do pixel atual se qualquer um dos três primeiros componentes (UVW) das coordenadas de textura for menor que zero.
ms.assetid: 7641aef8-8931-4a19-827a-75ab17e901ac
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4da9c6b59a3c16eeecb8755f2f19542df6ee8a7b
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104293551"
---
# <a name="texkill---ps"></a><span data-ttu-id="7b0de-103">texkill-PS</span><span class="sxs-lookup"><span data-stu-id="7b0de-103">texkill - ps</span></span>

<span data-ttu-id="7b0de-104">Cancela a renderização do pixel atual se qualquer um dos três primeiros componentes (UVW) das coordenadas de textura for menor que zero.</span><span class="sxs-lookup"><span data-stu-id="7b0de-104">Cancels rendering of the current pixel if any of the first three components (UVW) of the texture coordinates is less than zero.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b0de-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7b0de-105">Syntax</span></span>



| <span data-ttu-id="7b0de-106">texkill DST</span><span class="sxs-lookup"><span data-stu-id="7b0de-106">texkill dst</span></span> |
|-------------|



 

<span data-ttu-id="7b0de-107">onde</span><span class="sxs-lookup"><span data-stu-id="7b0de-107">where</span></span>

-   <span data-ttu-id="7b0de-108">o DST é um registro de destino</span><span class="sxs-lookup"><span data-stu-id="7b0de-108">dst is a destination register</span></span>

## <a name="remarks"></a><span data-ttu-id="7b0de-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="7b0de-109">Remarks</span></span>



| <span data-ttu-id="7b0de-110">Versões do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="7b0de-110">Pixel shader versions</span></span> | <span data-ttu-id="7b0de-111">1\_1</span><span class="sxs-lookup"><span data-stu-id="7b0de-111">1\_1</span></span> | <span data-ttu-id="7b0de-112">1\_2</span><span class="sxs-lookup"><span data-stu-id="7b0de-112">1\_2</span></span> | <span data-ttu-id="7b0de-113">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="7b0de-113">1\_3</span></span> | <span data-ttu-id="7b0de-114">1\_4</span><span class="sxs-lookup"><span data-stu-id="7b0de-114">1\_4</span></span> | <span data-ttu-id="7b0de-115">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="7b0de-115">2\_0</span></span> | <span data-ttu-id="7b0de-116">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="7b0de-116">2\_x</span></span> | <span data-ttu-id="7b0de-117">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="7b0de-117">2\_sw</span></span> | <span data-ttu-id="7b0de-118">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="7b0de-118">3\_0</span></span> | <span data-ttu-id="7b0de-119">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="7b0de-119">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="7b0de-120">texkill</span><span class="sxs-lookup"><span data-stu-id="7b0de-120">texkill</span></span>               | <span data-ttu-id="7b0de-121">x</span><span class="sxs-lookup"><span data-stu-id="7b0de-121">x</span></span>    | <span data-ttu-id="7b0de-122">x</span><span class="sxs-lookup"><span data-stu-id="7b0de-122">x</span></span>    | <span data-ttu-id="7b0de-123">x</span><span class="sxs-lookup"><span data-stu-id="7b0de-123">x</span></span>    | <span data-ttu-id="7b0de-124">x</span><span class="sxs-lookup"><span data-stu-id="7b0de-124">x</span></span>    | <span data-ttu-id="7b0de-125">x</span><span class="sxs-lookup"><span data-stu-id="7b0de-125">x</span></span>    | <span data-ttu-id="7b0de-126">x</span><span class="sxs-lookup"><span data-stu-id="7b0de-126">x</span></span>    | <span data-ttu-id="7b0de-127">x</span><span class="sxs-lookup"><span data-stu-id="7b0de-127">x</span></span>     | <span data-ttu-id="7b0de-128">x</span><span class="sxs-lookup"><span data-stu-id="7b0de-128">x</span></span>    | <span data-ttu-id="7b0de-129">x</span><span class="sxs-lookup"><span data-stu-id="7b0de-129">x</span></span>     |



 

<span data-ttu-id="7b0de-130">Essa instrução corresponde à função de [**clipe**](dx-graphics-hlsl-clip.md) do HLSL.</span><span class="sxs-lookup"><span data-stu-id="7b0de-130">This instruction corresponds to the HLSL's [**clip**](dx-graphics-hlsl-clip.md) function.</span></span>

<span data-ttu-id="7b0de-131">texkill não faz amostragem de nenhuma textura.</span><span class="sxs-lookup"><span data-stu-id="7b0de-131">texkill does not sample any texture.</span></span> <span data-ttu-id="7b0de-132">Ele opera nos três primeiros componentes das coordenadas de textura dadas pelo número de registro de destino.</span><span class="sxs-lookup"><span data-stu-id="7b0de-132">It operates on the first three components of the texture coordinates given by the destination register number.</span></span> <span data-ttu-id="7b0de-133">Para o PS \_ 1 \_ 4, o texkill opera nos dados nos três primeiros componentes do registro de destino.</span><span class="sxs-lookup"><span data-stu-id="7b0de-133">For ps\_1\_4, texkill operates on the data in the first three components of the destination register.</span></span>

<span data-ttu-id="7b0de-134">Você pode usar essa instrução para implementar planos de corte arbitrários no rasterizador.</span><span class="sxs-lookup"><span data-stu-id="7b0de-134">You can use this instruction to implement arbitrary clip planes in the rasterizer.</span></span>

<span data-ttu-id="7b0de-135">Ao usar sombreadores de vértice, o aplicativo é responsável por aplicar a transformação de perspectiva.</span><span class="sxs-lookup"><span data-stu-id="7b0de-135">When using vertex shaders, the application is responsible for applying the perspective transform.</span></span> <span data-ttu-id="7b0de-136">Isso pode causar problemas para os planos de recorte arbitrários porque, se ele contiver fatores de escala anisomorphic, os planos de corte também precisam ser transformados.</span><span class="sxs-lookup"><span data-stu-id="7b0de-136">This can cause problems for the arbitrary clipping planes because if it contains anisomorphic scale factors, the clip planes need to be transformed as well.</span></span> <span data-ttu-id="7b0de-137">Portanto, é melhor fornecer uma posição de vértice não projetada para uso no Clipper arbitrário, que é o conjunto de coordenadas de textura identificado pelo operador texkill.</span><span class="sxs-lookup"><span data-stu-id="7b0de-137">Therefore, it is best to provide an unprojected vertex position to use in the arbitrary clipper, which is the texture coordinate set identified by the texkill operator.</span></span>

<span data-ttu-id="7b0de-138">Essa instrução é usada da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="7b0de-138">This instruction is used as follows:</span></span>

<dl> <span data-ttu-id="7b0de-139">texkill TN</span><span class="sxs-lookup"><span data-stu-id="7b0de-139">texkill tn</span></span>  
<span data-ttu-id="7b0de-140">O mascaramento de pixels é feito da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="7b0de-140">// The pixel masking is accomplished as follows:</span></span>  
<span data-ttu-id="7b0de-141">If (os componentes x, y, z de TextureCoordinates (estágio n)<sub>UVWQ</sub>< 0)</span><span class="sxs-lookup"><span data-stu-id="7b0de-141">if ( the x,y,z components of TextureCoordinates(stage n)<sub>UVWQ</sub>< 0 )</span></span>  
<span data-ttu-id="7b0de-142">cancelar renderização de pixel</span><span class="sxs-lookup"><span data-stu-id="7b0de-142">cancel pixel render</span></span>
</dl>

<span data-ttu-id="7b0de-143">Para o sombreador de pixel 1 \_ 1, 1 \_ 2 e 1 \_ 3, texkill opera no conjunto de coordenadas de textura fornecido pelo número de registro de destino.</span><span class="sxs-lookup"><span data-stu-id="7b0de-143">For pixel shader 1\_1, 1\_2, and 1\_3, texkill operates on the texture coordinate set given by the destination register number.</span></span> <span data-ttu-id="7b0de-144">No \_ entanto, na versão 1 4, o texkill opera nos dados contidos no TN ( [registro de coordenadas de textura](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md) ) ou no registro temporário (RN) que foi especificado como o destino.</span><span class="sxs-lookup"><span data-stu-id="7b0de-144">In version 1\_4, however, texkill operates on the data contained in the [Texture Coordinate Register](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md) (tn) or in the temporary register (rn) that has been specified as the destination.</span></span>

<span data-ttu-id="7b0de-145">Quando a multiamostragem está habilitada, qualquer efeito de suavização obtido nas bordas do polígono devido a uma multiamostração não será Obtido em qualquer borda que tenha sido gerada pelo texkill.</span><span class="sxs-lookup"><span data-stu-id="7b0de-145">When multisampling is enabled, any antialiasing effect achieved on polygon edges due to multisampling will not be achieved along any edge that has been generated by texkill.</span></span> <span data-ttu-id="7b0de-146">O sombreador de pixel é executado uma vez por pixel.</span><span class="sxs-lookup"><span data-stu-id="7b0de-146">The pixel shader runs once per pixel.</span></span>

<span data-ttu-id="7b0de-147">Este exemplo é apenas uma ilustração.</span><span class="sxs-lookup"><span data-stu-id="7b0de-147">This example is for illustration only.</span></span>

<span data-ttu-id="7b0de-148">Este exemplo mascara os pixels que têm coordenadas de textura negativas.</span><span class="sxs-lookup"><span data-stu-id="7b0de-148">This example masks out pixels that have negative texture coordinates.</span></span> <span data-ttu-id="7b0de-149">As cores de pixel são interpoladas das cores de vértice fornecidas nos dados do vértice.</span><span class="sxs-lookup"><span data-stu-id="7b0de-149">The pixel colors are interpolated from vertex colors provided in the vertex data.</span></span>


```
ps_1_1       // Version instruction
texkill t0   // Mask out pixel using texture coordinates from stage 0
mov r0, v0   // Move the diffuse color in v0 to r0

// The rendered output from the pixel shader is shown below
```



<span data-ttu-id="7b0de-150">As coordenadas de textura variam de-0,5 a 0,5 em u e 0,0 a 1,0 em v.</span><span class="sxs-lookup"><span data-stu-id="7b0de-150">The texture coordinates range from -0.5 to 0.5 in u, and 0.0 to 1.0 in v.</span></span> <span data-ttu-id="7b0de-151">Essa instrução faz com que os valores de u negativos sejam mascarados. A primeira ilustração abaixo mostra a cor do vértice aplicada ao Quad sem a instrução texkill aplicada.</span><span class="sxs-lookup"><span data-stu-id="7b0de-151">This instruction causes the negative u values to get masked out. The first illustration below shows the vertex color applied to the quad without the texkill instruction applied.</span></span> <span data-ttu-id="7b0de-152">A segunda ilustração abaixo mostra o resultado da instrução texkill.</span><span class="sxs-lookup"><span data-stu-id="7b0de-152">The second illustration below shows the result of the texkill instruction.</span></span> <span data-ttu-id="7b0de-153">As cores de pixel das coordenadas de textura abaixo de 0 (em que x vai de-0,5 a 0,0) são mascaradas. A cor do plano de fundo (branco) é usada onde a cor do pixel é mascarada.</span><span class="sxs-lookup"><span data-stu-id="7b0de-153">The pixel colors from the texture coordinates below 0 (where x goes from -0.5 to 0.0) are masked out. The background color (white) is used where the pixel color is masked.</span></span>

![ilustração da saída com a cor do vértice aplicada ao Quad sem a instrução texkill](images/pstexkill-in.jpg)![ilustração da saída com a instrução texkill aplicada](images/pstexkill-out.jpg)

<span data-ttu-id="7b0de-156">Os dados de coordenadas de textura são declarados na declaração de dados de vértice neste exemplo.</span><span class="sxs-lookup"><span data-stu-id="7b0de-156">The texture coordinate data is declared in the vertex data declaration in this example.</span></span>


```
   
struct CUSTOMVERTEX
{
    FLOAT x, y, z;
    DWORD color;
    FLOAT tu1, tv1;
};

#define D3DFVF_CUSTOMVERTEX (D3DFVF_XYZ|D3DFVF_DIFFUSE|D3DFVF_TEX1|D3DTEXCOORD2(0))

static CUSTOMVERTEX g_Vertices[]=
{
    //  x      y     z    color         u1,    v1  
    { -1.0f, -1.0f, 0.0f, 0xffff0000, -0.5f,  1.0f, },
    {  1.0f, -1.0f, 0.0f, 0xff00ff00,  0.5f,  1.0f, },
    {  1.0f,  1.0f, 0.0f, 0xff0000ff,  0.5f,  0.0f, },
    { -1.0f,  1.0f, 0.0f, 0xffffffff, -0.5f,  0.0f, },

};
```



## <a name="related-topics"></a><span data-ttu-id="7b0de-157">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7b0de-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7b0de-158">Instruções do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="7b0de-158">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




