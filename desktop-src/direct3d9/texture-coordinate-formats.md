---
description: As coordenadas de textura no Direct3D podem incluir um, dois, três ou quatro elementos de ponto flutuante para endereçar texturas com níveis variados de dimensão.
ms.assetid: d841af62-41b0-4b80-960b-4630b9a7210c
title: Formatos de coordenadas de textura (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c95eada1cf21f0a4db38589794b08b88023e72d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103646178"
---
# <a name="texture-coordinate-formats-direct3d-9"></a><span data-ttu-id="dc28f-103">Formatos de coordenadas de textura (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="dc28f-103">Texture Coordinate Formats (Direct3D 9)</span></span>

<span data-ttu-id="dc28f-104">As coordenadas de textura no Direct3D podem incluir um, dois, três ou quatro elementos de ponto flutuante para endereçar texturas com níveis variados de dimensão.</span><span class="sxs-lookup"><span data-stu-id="dc28f-104">Texture coordinates in Direct3D can include one, two, three, or four floating point elements to address textures with varying levels of dimension.</span></span> <span data-ttu-id="dc28f-105">Uma textura 1D – uma superfície de textura com dimensões de texels 1 por n – é endereçada por uma coordenada de textura.</span><span class="sxs-lookup"><span data-stu-id="dc28f-105">A 1D texture - a texture surface with dimensions of 1-by-n texels - is addressed by one texture coordinate.</span></span> <span data-ttu-id="dc28f-106">O caso mais comum, texturas 2D, são abordados com duas coordenadas de textura normalmente chamadas de você e de v.</span><span class="sxs-lookup"><span data-stu-id="dc28f-106">The most common case, 2D textures, are addressed with two texture coordinates commonly called u and v.</span></span> <span data-ttu-id="dc28f-107">O Direct3D dá suporte a dois tipos de texturas 3D, mapas de ambiente cúbico e texturas de volume.</span><span class="sxs-lookup"><span data-stu-id="dc28f-107">Direct3D supports two types of 3D textures, cubic-environment maps and volume textures.</span></span> <span data-ttu-id="dc28f-108">Os mapas de ambiente cúbico não são verdadeiramente 3D, mas são tratados com um vetor de 3 elementos.</span><span class="sxs-lookup"><span data-stu-id="dc28f-108">Cubic environment maps aren't truly 3D, but they are addressed with a 3-element vector.</span></span> <span data-ttu-id="dc28f-109">Para obter detalhes, consulte [mapeamento de ambiente cúbico (Direct3D 9)](cubic-environment-mapping.md).</span><span class="sxs-lookup"><span data-stu-id="dc28f-109">For details, see [Cubic Environment Mapping (Direct3D 9)](cubic-environment-mapping.md).</span></span>

<span data-ttu-id="dc28f-110">Conforme descrito em [códigos de FVF de função fixas (Direct3D 9)](fixed-function-fvf-codes.md), os aplicativos codificam coordenadas de textura no formato de vértice.</span><span class="sxs-lookup"><span data-stu-id="dc28f-110">As described in [Fixed Function FVF Codes (Direct3D 9)](fixed-function-fvf-codes.md), applications encode texture coordinates in the vertex format.</span></span> <span data-ttu-id="dc28f-111">O formato de vértice pode incluir vários conjuntos de coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="dc28f-111">The vertex format can include multiple sets of texture coordinates.</span></span> <span data-ttu-id="dc28f-112">Use o D3DFVF \_ TEX0 até D3DFVF \_ TEX8 [D3DFVF](d3dfvf.md) para descrever um formato de vértice que não inclui nenhuma coordenada de textura ou até oito conjuntos.</span><span class="sxs-lookup"><span data-stu-id="dc28f-112">Use the D3DFVF\_TEX0 through D3DFVF\_TEX8 [D3DFVF](d3dfvf.md) to describe a vertex format that includes no texture coordinates, or as many as eight sets.</span></span>

<span data-ttu-id="dc28f-113">Cada conjunto de coordenadas de textura pode ter entre um e quatro elementos.</span><span class="sxs-lookup"><span data-stu-id="dc28f-113">Each texture coordinate set can have between one and four elements.</span></span> <span data-ttu-id="dc28f-114">Os \_ sinalizadores D3DFVF TEXTUREFORMAT1 a D3DFVF \_ TEXTUREFORMAT4 descrevem o número de elementos em uma coordenada de textura em um conjunto, mas esses sinalizadores não são usados por si mesmos.</span><span class="sxs-lookup"><span data-stu-id="dc28f-114">The D3DFVF\_TEXTUREFORMAT1 through D3DFVF\_TEXTUREFORMAT4 flags describe the number of elements in a texture coordinate in a set, but these flags aren't used by themselves.</span></span> <span data-ttu-id="dc28f-115">Em vez disso, o conjunto de macros [**D3DFVF \_ TEXCOORDSIZEN**](d3dfvf-texcoordsizen.md) usa esses sinalizadores para criar padrões de bits que descrevem o número de elementos usados por um determinado conjunto de coordenadas de textura no formato de vértice.</span><span class="sxs-lookup"><span data-stu-id="dc28f-115">Rather, the [**D3DFVF\_TEXCOORDSIZEN**](d3dfvf-texcoordsizen.md) set of macros use these flags to create bit patterns that describe the number of elements used by a particular set of texture coordinates in the vertex format.</span></span> <span data-ttu-id="dc28f-116">Essas macros aceitam um único parâmetro que identifica o índice do conjunto de coordenadas cujo número de elementos está sendo definido.</span><span class="sxs-lookup"><span data-stu-id="dc28f-116">These macros accept a single parameter that identifies the index of the coordinate set whose number of elements is being defined.</span></span> <span data-ttu-id="dc28f-117">O exemplo a seguir ilustra como essas macros são usadas.</span><span class="sxs-lookup"><span data-stu-id="dc28f-117">The following example illustrates how these macros are used.</span></span>


```
// This vertex format contains two sets of texture coordinates.
// The first set (index 0) has 2 elements, and the second set 
// has 1 element. The description for this vertex format would be: 
//     dwFVF = D3DFVF_XYZ  | D3DFVF_NORMAL | D3DFVF_DIFFUSE | D3DFVF_TEX2 |
//             D3DFVF_TEXCOORDSIZE2(0) | D3DFVF_TEXCOORDSIZE1(1); 
//
typedef struct CVF
{
    D3DVECTOR position;
    D3DVECTOR normal;
    D3DCOLOR  diffuse;
    float     u, v;   // 1st set, 2D
    float     t;      // 2nd set, 1D
} CustomVertexFormat;
```



> [!Note]  
> <span data-ttu-id="dc28f-118">Com exceção de mapas de ambiente cúbico e texturas de volume, os rasterizadores não podem resolver texturas usando mais de dois elementos.</span><span class="sxs-lookup"><span data-stu-id="dc28f-118">With the exception of cubic-environment maps and volume textures, rasterizers cannot address textures by using any more than two elements.</span></span> <span data-ttu-id="dc28f-119">Os aplicativos podem fornecer até três elementos para uma coordenada de textura, mas somente se a textura for um mapa de cubo, uma textura de volume ou o \_ sinalizador de transformação de textura projetado D3DTTFF for usado.</span><span class="sxs-lookup"><span data-stu-id="dc28f-119">Applications can supply up to three elements for a texture coordinate, but only if the texture is a cube map, a volume texture, or the D3DTTFF\_PROJECTED texture transform flag is used.</span></span> <span data-ttu-id="dc28f-120">O \_ sinalizador projetado D3DTTFF faz com que o rasterizador divida os dois primeiros elementos pelo terceiro (ou n) elemento.</span><span class="sxs-lookup"><span data-stu-id="dc28f-120">The D3DTTFF\_PROJECTED flag causes the rasterizer to divide the first two elements by the third (or n) element.</span></span> <span data-ttu-id="dc28f-121">Para obter mais informações, consulte [transformações de coordenadas de textura (Direct3D 9)](texture-coordinate-transformations.md).</span><span class="sxs-lookup"><span data-stu-id="dc28f-121">For more information, see [Texture Coordinate Transformations (Direct3D 9)](texture-coordinate-transformations.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="dc28f-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="dc28f-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dc28f-123">Coordenadas de textura</span><span class="sxs-lookup"><span data-stu-id="dc28f-123">Texture Coordinates</span></span>](texture-coordinates.md)
</dt> </dl>

 

 



