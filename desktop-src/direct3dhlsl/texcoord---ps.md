---
title: texcoord-PS
description: Interpreta dados de coordenadas de textura (UVW1) como dados de cor (RGBA).
ms.assetid: 0f79a62c-1142-4dcd-aa2f-a5bd1c369ffc
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9e871d1f91d89d0eb0ddadee34b5ac215916d0af
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641289"
---
# <a name="texcoord---ps"></a><span data-ttu-id="7cdfc-103">texcoord-PS</span><span class="sxs-lookup"><span data-stu-id="7cdfc-103">texcoord - ps</span></span>

<span data-ttu-id="7cdfc-104">Interpreta dados de coordenadas de textura (UVW1) como dados de cor (RGBA).</span><span class="sxs-lookup"><span data-stu-id="7cdfc-104">Interprets texture coordinate data (UVW1) as color data (RGBA).</span></span>

## <a name="syntax"></a><span data-ttu-id="7cdfc-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7cdfc-105">Syntax</span></span>



| <span data-ttu-id="7cdfc-106">texcoord DST</span><span class="sxs-lookup"><span data-stu-id="7cdfc-106">texcoord dst</span></span> |
|--------------|



 

<span data-ttu-id="7cdfc-107">onde</span><span class="sxs-lookup"><span data-stu-id="7cdfc-107">where</span></span>

-   <span data-ttu-id="7cdfc-108">DST é o registro de destino.</span><span class="sxs-lookup"><span data-stu-id="7cdfc-108">dst is the destination register.</span></span>

## <a name="remarks"></a><span data-ttu-id="7cdfc-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="7cdfc-109">Remarks</span></span>



| <span data-ttu-id="7cdfc-110">Versões do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="7cdfc-110">Pixel shader versions</span></span> | <span data-ttu-id="7cdfc-111">1\_1</span><span class="sxs-lookup"><span data-stu-id="7cdfc-111">1\_1</span></span> | <span data-ttu-id="7cdfc-112">1\_2</span><span class="sxs-lookup"><span data-stu-id="7cdfc-112">1\_2</span></span> | <span data-ttu-id="7cdfc-113">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="7cdfc-113">1\_3</span></span> | <span data-ttu-id="7cdfc-114">1\_4</span><span class="sxs-lookup"><span data-stu-id="7cdfc-114">1\_4</span></span> | <span data-ttu-id="7cdfc-115">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="7cdfc-115">2\_0</span></span> | <span data-ttu-id="7cdfc-116">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="7cdfc-116">2\_x</span></span> | <span data-ttu-id="7cdfc-117">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="7cdfc-117">2\_sw</span></span> | <span data-ttu-id="7cdfc-118">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="7cdfc-118">3\_0</span></span> | <span data-ttu-id="7cdfc-119">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="7cdfc-119">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="7cdfc-120">texcoord</span><span class="sxs-lookup"><span data-stu-id="7cdfc-120">texcoord</span></span>              | <span data-ttu-id="7cdfc-121">x</span><span class="sxs-lookup"><span data-stu-id="7cdfc-121">x</span></span>    | <span data-ttu-id="7cdfc-122">x</span><span class="sxs-lookup"><span data-stu-id="7cdfc-122">x</span></span>    | <span data-ttu-id="7cdfc-123">x</span><span class="sxs-lookup"><span data-stu-id="7cdfc-123">x</span></span>    |      |      |      |       |      |       |



 

<span data-ttu-id="7cdfc-124">Essa instrução interpreta o conjunto de coordenadas de textura (UVW1) correspondente ao número de registro de destino como dados de cor (RGBA).</span><span class="sxs-lookup"><span data-stu-id="7cdfc-124">This instruction interprets the texture coordinate set (UVW1) corresponding to the destination register number as color data (RGBA).</span></span> <span data-ttu-id="7cdfc-125">Se o conjunto de coordenadas de textura contiver menos de três componentes, os componentes ausentes serão definidos como 0.</span><span class="sxs-lookup"><span data-stu-id="7cdfc-125">If the texture coordinate set contains fewer than three components, the missing components are set to 0.</span></span> <span data-ttu-id="7cdfc-126">O quarto componente é sempre definido como 1.</span><span class="sxs-lookup"><span data-stu-id="7cdfc-126">The fourth component is always set to 1.</span></span> <span data-ttu-id="7cdfc-127">Todos os valores são clampeddos entre 0 e 1.</span><span class="sxs-lookup"><span data-stu-id="7cdfc-127">All values are clamped between 0 and 1.</span></span>

<span data-ttu-id="7cdfc-128">A vantagem do texcoord é que ele fornece uma maneira de passar dados de vértice interpolados a alta precisão diretamente no sombreador de pixel.</span><span class="sxs-lookup"><span data-stu-id="7cdfc-128">The advantage of texcoord is that it provides a way to pass vertex data interpolated at high precision directly into the pixel shader.</span></span> <span data-ttu-id="7cdfc-129">No entanto, quando os dados são gravados no registro de destino, alguma precisão será perdida, dependendo do número de bits usados pelo hardware para os registros.</span><span class="sxs-lookup"><span data-stu-id="7cdfc-129">However, when the data is written into the destination register, some precision will be lost, depending on the number of bits used by the hardware for registers.</span></span>

<span data-ttu-id="7cdfc-130">Nenhuma textura é amostrada por essa instrução.</span><span class="sxs-lookup"><span data-stu-id="7cdfc-130">No texture is sampled by this instruction.</span></span> <span data-ttu-id="7cdfc-131">Somente as coordenadas de textura definidas neste estágio de textura são relevantes.</span><span class="sxs-lookup"><span data-stu-id="7cdfc-131">Only texture coordinates set on this texture stage are relevant.</span></span>

<span data-ttu-id="7cdfc-132">Todos os dados de textura (como posição, normal e direção da fonte de luz) podem ser mapeados por um sombreador de vértice em uma coordenada de textura.</span><span class="sxs-lookup"><span data-stu-id="7cdfc-132">Any texture data (such as position, normal, and light source direction) can be mapped by a vertex shader into a texture coordinate.</span></span> <span data-ttu-id="7cdfc-133">Isso é feito associando uma textura a um registro de textura usando [**SetTexture**](/windows/desktop/direct3d9/id3dxbaseeffect--settexture) e especificando como a amostragem de textura é feita usando [**SetTextureStageState**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate).</span><span class="sxs-lookup"><span data-stu-id="7cdfc-133">This is done by associating a texture with a texture register using [**SetTexture**](/windows/desktop/direct3d9/id3dxbaseeffect--settexture) and by specifying how the texture sampling is done using [**SetTextureStageState**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate).</span></span> <span data-ttu-id="7cdfc-134">Se o pipeline de função fixa for usado, não se esqueça de fornecer o \_ sinalizador TSS TEXCOORDINDEX.</span><span class="sxs-lookup"><span data-stu-id="7cdfc-134">If the fixed function pipeline is used, be sure to supply the TSS\_TEXCOORDINDEX flag.</span></span>

<span data-ttu-id="7cdfc-135">Essa instrução é usada da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="7cdfc-135">This instruction is used as follows:</span></span>


```
texcoord tn
```



<span data-ttu-id="7cdfc-136">Um TN ( [registro de coordenadas de textura](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md) ) contém quatro valores de cor (RGBA).</span><span class="sxs-lookup"><span data-stu-id="7cdfc-136">An [Texture Coordinate Register](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md) (tn) contains four color values (RGBA).</span></span> <span data-ttu-id="7cdfc-137">Os dados também podem ser considerados como dados de vetor (xyzw).</span><span class="sxs-lookup"><span data-stu-id="7cdfc-137">The data can also be thought of as vector data (xyzw).</span></span> <span data-ttu-id="7cdfc-138">texcoord recuperará três desses valores (XYZ) do conjunto de coordenadas de textura x, e o quarto componente (w) é definido como 1.</span><span class="sxs-lookup"><span data-stu-id="7cdfc-138">texcoord will retrieve three of these values (xyz) from texture coordinate set x, and the fourth component (w) is set to 1.</span></span> <span data-ttu-id="7cdfc-139">O endereço de textura é copiado do conjunto de coordenadas de textura n.</span><span class="sxs-lookup"><span data-stu-id="7cdfc-139">The texture address is copied from the texture coordinate set n.</span></span> <span data-ttu-id="7cdfc-140">O resultado é clamped entre 0 e 1.</span><span class="sxs-lookup"><span data-stu-id="7cdfc-140">The result is clamped between 0 and 1.</span></span>

<span data-ttu-id="7cdfc-141">Este exemplo é apenas uma ilustração.</span><span class="sxs-lookup"><span data-stu-id="7cdfc-141">This example is for illustration only.</span></span> <span data-ttu-id="7cdfc-142">O código C que acompanha o sombreador não foi otimizado para desempenho.</span><span class="sxs-lookup"><span data-stu-id="7cdfc-142">The C code accompanying the shader has not been optimized for performance.</span></span>

<span data-ttu-id="7cdfc-143">Aqui está um sombreador de exemplo usando texcoord.</span><span class="sxs-lookup"><span data-stu-id="7cdfc-143">Here is an example shader using texcoord.</span></span>


```
ps_1_1        ; version instruction
texcoord t0   ; declare t0 hold texture coordinates, 
              ; which represent rgba values in this example
mov r0, t0    ; move the color in t0 to output register r0
```



<span data-ttu-id="7cdfc-144">A saída renderizada do sombreador de pixel é mostrada na ilustração a seguir.</span><span class="sxs-lookup"><span data-stu-id="7cdfc-144">The rendered output from the pixel shader is shown in the following illustration.</span></span> <span data-ttu-id="7cdfc-145">Os valores de coordenadas (u, v, w, 1) são mapeados para os canais (RGB).</span><span class="sxs-lookup"><span data-stu-id="7cdfc-145">The (u,v,w,1) coordinate values map to the (rgb) channels.</span></span> <span data-ttu-id="7cdfc-146">O canal alfa é definido como 1.</span><span class="sxs-lookup"><span data-stu-id="7cdfc-146">The alpha channel is set to 1.</span></span> <span data-ttu-id="7cdfc-147">Nos cantos da ilustração, a coordenada (0, 0, 0, 1) é interpretada como preta; (1, 0, 0, 1) é vermelho; (0, 1, 0, 1) é verde; e (1, 1, 0, 1) contém verde e vermelho, produzindo amarelo.</span><span class="sxs-lookup"><span data-stu-id="7cdfc-147">At the corners of the illustration, coordinate (0,0,0,1) is interpreted as black; (1,0,0,1) is red; (0,1,0,1) is green; and (1,1,0,1) contains green and red, producing yellow.</span></span>

![ilustração da saída renderizada do sombreador de pixel de exemplo](images/pstexcoord.jpg)

<span data-ttu-id="7cdfc-149">O código adicional é necessário para usar este sombreador e um cenário de exemplo é mostrado abaixo.</span><span class="sxs-lookup"><span data-stu-id="7cdfc-149">Additional code is required to use this shader and an example scenario is shown below.</span></span>


```
// This code creates the shader from a file. The contents of  
// the shader file can also be supplied as a text string.
LPD3DXBUFFER        pCode;

// Assemble the vertex shader from the file
D3DXAssembleShaderFromFile(strPShaderPath, 0, NULL, &pCode, NULL);
m_pd3dDevice->CreatePixelShader((DWORD*)pCode->GetBufferPointer(),
                   &m_hPixelShader);
pCode->Release();

// This code defines the object vertex data
struct CUSTOMVERTEX
{
    FLOAT x, y, z;
    FLOAT tu1, tv1;
};

#define D3DFVF_CUSTOMVERTEX (D3DFVF_XYZ|D3DFVF_TEX1|TEXCOORD2(0))

static CUSTOMVERTEX g_Vertices[]=
{
    //  x      y     z     u1    v1   
    { -1.0f, -1.0f, 0.0f, 0.0f, 0.0f, },
    { +1.0f, -1.0f, 0.0f, 1.0f, 0.0f, },
    { +1.0f, +1.0f, 0.0f, 1.0f, 1.0f, },
    { -1.0f, +1.0f, 0.0f, 0.0f, 1.0f, },
};
```



## <a name="related-topics"></a><span data-ttu-id="7cdfc-150">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7cdfc-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7cdfc-151">Instruções do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="7cdfc-151">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 