---
title: Registro de coordenadas de textura (referência de HLSL VS)
description: Este registro de saída do sombreador de vértice contém coordenadas de textura por vértice.
ms.assetid: d42c8e4c-8227-4fe8-9432-90c592011024
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ad3937b8f0b3f7acd6313774f6de7cde133e69c5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084846"
---
# <a name="texture-coordinate-register-hlsl-vs-reference"></a><span data-ttu-id="a3b66-103">Registro de coordenadas de textura (referência de HLSL VS)</span><span class="sxs-lookup"><span data-stu-id="a3b66-103">Texture Coordinate Register (HLSL VS reference)</span></span>

<span data-ttu-id="a3b66-104">Este registro de saída do sombreador de vértice contém coordenadas de textura por vértice.</span><span class="sxs-lookup"><span data-stu-id="a3b66-104">This vertex shader output register contains per-vertex texture coordinates.</span></span>

<span data-ttu-id="a3b66-105">Um registro consiste em propriedades que determinam se o registro se comporta.</span><span class="sxs-lookup"><span data-stu-id="a3b66-105">A register consists of properties that determine how each register behaves.</span></span>



| <span data-ttu-id="a3b66-106">Propriedade</span><span class="sxs-lookup"><span data-stu-id="a3b66-106">Property</span></span>        | <span data-ttu-id="a3b66-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="a3b66-107">Description</span></span>   |
|-----------------|---------------|
| <span data-ttu-id="a3b66-108">Name</span><span class="sxs-lookup"><span data-stu-id="a3b66-108">Name</span></span>            | <span data-ttu-id="a3b66-109">oT0 - oT7</span><span class="sxs-lookup"><span data-stu-id="a3b66-109">oT0 - oT7</span></span>     |
| <span data-ttu-id="a3b66-110">Contagem</span><span class="sxs-lookup"><span data-stu-id="a3b66-110">Count</span></span>           | <span data-ttu-id="a3b66-111">Oito vetores</span><span class="sxs-lookup"><span data-stu-id="a3b66-111">Eight vectors</span></span> |
| <span data-ttu-id="a3b66-112">Permissões de e/s</span><span class="sxs-lookup"><span data-stu-id="a3b66-112">I/O permissions</span></span> | <span data-ttu-id="a3b66-113">Somente gravação</span><span class="sxs-lookup"><span data-stu-id="a3b66-113">Write-only</span></span>    |



 

<span data-ttu-id="a3b66-114">Os registros de coordenadas de textura de saída são uma matriz de registros de dados de saída.</span><span class="sxs-lookup"><span data-stu-id="a3b66-114">The output texture coordinates registers are an array of output data registers.</span></span> <span data-ttu-id="a3b66-115">Os dados de registro são iterados e usados como coordenadas de textura pelos estágios de amostragem de textura para fornecer dados ao sombreador de pixel.</span><span class="sxs-lookup"><span data-stu-id="a3b66-115">The register data is iterated and used as texture coordinates by the texture sampling stages to supply data to the pixel shader.</span></span>

<span data-ttu-id="a3b66-116">Ao gravar em um registro de coordenadas de textura, é recomendável que você passe apenas o número de valores de ponto flutuante como a dimensão do mapa de textura correspondente.</span><span class="sxs-lookup"><span data-stu-id="a3b66-116">When writing to a texture coordinate register, it is recommended that you pass only as many floating point values as the dimension of the corresponding texture map.</span></span> <span data-ttu-id="a3b66-117">Controle os valores que são passados com um modificador.</span><span class="sxs-lookup"><span data-stu-id="a3b66-117">Control the values that are passed with a modifier.</span></span> <span data-ttu-id="a3b66-118">Por exemplo, use. XY para um mapa de textura 2D.</span><span class="sxs-lookup"><span data-stu-id="a3b66-118">For example, use .xy for a 2D texture map.</span></span>

<span data-ttu-id="a3b66-119">Os sinalizadores de pipeline de vértice de função fixa, [**D3DTEXTURETRANSFORMFLAGS**](/windows/desktop/direct3d9/d3dtexturetransformflags) (D3DTTFF \_ COUNT1, D3DTTFF \_ COUNT2, D3DTTFF \_ COUNT3, D3DTTFF \_ COUNT4), devem ser definidos como zero se você estiver usando um sombreador de vértice programável.</span><span class="sxs-lookup"><span data-stu-id="a3b66-119">The fixed function vertex pipeline flags, [**D3DTEXTURETRANSFORMFLAGS**](/windows/desktop/direct3d9/d3dtexturetransformflags) (D3DTTFF\_COUNT1, D3DTTFF\_COUNT2, D3DTTFF\_COUNT3, D3DTTFF\_COUNT4), should be set to zero if you are using a programmable vertex shader.</span></span>

<span data-ttu-id="a3b66-120">Dados de vértice de objeto fornecem coordenadas de textura de entrada.</span><span class="sxs-lookup"><span data-stu-id="a3b66-120">Object vertex data supplies input texture coordinates.</span></span> <span data-ttu-id="a3b66-121">Os objetos que não usam texturas com ladrilhos normalmente têm coordenadas de textura no intervalo de \[ 0, 1 \] .</span><span class="sxs-lookup"><span data-stu-id="a3b66-121">Objects that do not use tiled textures commonly have texture coordinates in the range \[0,1\].</span></span> <span data-ttu-id="a3b66-122">Os objetos que usam texturas de lado, como o terreno, normalmente têm coordenadas de textura que variam de \[ -n, + n, \] em que n pode ser qualquer número de ponto flutuante.</span><span class="sxs-lookup"><span data-stu-id="a3b66-122">Objects that use tiled textures, such as terrain, typically have texture coordinates that range from \[-n,+n\] where n can be any floating point number.</span></span>

<span data-ttu-id="a3b66-123">A interpolação de coordenadas de textura é executada em dados de vértice para rasterização.</span><span class="sxs-lookup"><span data-stu-id="a3b66-123">Texture coordinate interpolation is performed on vertex data for rasterization.</span></span> <span data-ttu-id="a3b66-124">Durante a rasterização, as coordenadas de textura são interpoladas entre os vértices do objeto, modificadas pelo encapsulamento de textura e dimensionadas pelo tamanho da textura (também levando em conta os modos de endereçamento de textura) para produzir um índice de número inteiro.</span><span class="sxs-lookup"><span data-stu-id="a3b66-124">During rasterization, texture coordinates are interpolated between object vertices, modified by texture wrapping, and scaled by the texture size (also taking into account texture addressing modes) to produce an integer index.</span></span> <span data-ttu-id="a3b66-125">Em seguida, o índice é usado para executar uma pesquisa de textura.</span><span class="sxs-lookup"><span data-stu-id="a3b66-125">The index is then used to perform a texture lookup.</span></span> <span data-ttu-id="a3b66-126">Use o valor MaxTextureRepeat em [**D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9) para determinar o número de vezes que uma textura pode ser colocada ao lado.</span><span class="sxs-lookup"><span data-stu-id="a3b66-126">Use the MaxTextureRepeat value in [**D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9) to determine how many times a texture can be tiled.</span></span>

## <a name="example"></a><span data-ttu-id="a3b66-127">Exemplo</span><span class="sxs-lookup"><span data-stu-id="a3b66-127">Example</span></span>

<span data-ttu-id="a3b66-128">Declare o registro de coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="a3b66-128">Declare the texture coordinate register.</span></span>


```
dcl_texcoord v7
```



<span data-ttu-id="a3b66-129">Copie as coordenadas de textura por vértice para o registro de saída.</span><span class="sxs-lookup"><span data-stu-id="a3b66-129">Copy the per-vertex texture coordinates to the output register.</span></span>


```
mov oT0, v7
```





| <span data-ttu-id="a3b66-130">Versões do sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="a3b66-130">Vertex shader versions</span></span>      | <span data-ttu-id="a3b66-131">1\_1</span><span class="sxs-lookup"><span data-stu-id="a3b66-131">1\_1</span></span> | <span data-ttu-id="a3b66-132">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="a3b66-132">2\_0</span></span> | <span data-ttu-id="a3b66-133">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="a3b66-133">2\_sw</span></span> | <span data-ttu-id="a3b66-134">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="a3b66-134">2\_x</span></span> | <span data-ttu-id="a3b66-135">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="a3b66-135">3\_0</span></span> | <span data-ttu-id="a3b66-136">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="a3b66-136">3\_sw</span></span> |
|-----------------------------|------|------|-------|------|------|-------|
| <span data-ttu-id="a3b66-137">Registro de coordenadas de textura</span><span class="sxs-lookup"><span data-stu-id="a3b66-137">Texture Coordinate Register</span></span> | <span data-ttu-id="a3b66-138">x</span><span class="sxs-lookup"><span data-stu-id="a3b66-138">x</span></span>    | <span data-ttu-id="a3b66-139">x</span><span class="sxs-lookup"><span data-stu-id="a3b66-139">x</span></span>    | <span data-ttu-id="a3b66-140">x</span><span class="sxs-lookup"><span data-stu-id="a3b66-140">x</span></span>     | <span data-ttu-id="a3b66-141">x</span><span class="sxs-lookup"><span data-stu-id="a3b66-141">x</span></span>    | <span data-ttu-id="a3b66-142">x</span><span class="sxs-lookup"><span data-stu-id="a3b66-142">x</span></span>    | <span data-ttu-id="a3b66-143">x</span><span class="sxs-lookup"><span data-stu-id="a3b66-143">x</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="a3b66-144">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a3b66-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a3b66-145">Registros de sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="a3b66-145">Vertex Shader Registers</span></span>](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 