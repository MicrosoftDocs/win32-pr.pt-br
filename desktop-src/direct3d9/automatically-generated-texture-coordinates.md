---
title: Coordenadas de textura geradas automaticamente (Direct3D 9)
description: O sistema pode usar a posição de espaço da câmera transformada ou o normal de um vértice como coordenadas de textura ou pode calcular os três vetores de elemento usados para abordar um mapa de ambiente cúbica.
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b01addbe354fb910ef68e1fc693e7dfffb1ceacf
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109843287"
---
# <a name="auto-generated-texture-coordinates-direct3d-9"></a><span data-ttu-id="82773-103">Coordenadas de textura geradas automaticamente (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="82773-103">Auto-generated texture coordinates (Direct3D 9)</span></span>

<span data-ttu-id="82773-104">O sistema pode usar a posição de espaço da câmera transformada ou o normal de um vértice como coordenadas de textura ou pode calcular os três vetores de elemento usados para abordar um mapa de ambiente cúbica.</span><span class="sxs-lookup"><span data-stu-id="82773-104">The system can use the transformed camera-space position or the normal from a vertex as texture coordinates, or it can compute the three element vectors used to address a cubic environment map.</span></span> <span data-ttu-id="82773-105">Assim como as coordenadas de textura especificadas explicitamente em um vértice, você pode usar coordenadas de textura geradas automaticamente como entrada para transformações de coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="82773-105">Like texture coordinates that you explicitly specify in a vertex, you can use automatically generated texture coordinates as input for texture coordinate transformations.</span></span>

<span data-ttu-id="82773-106">As coordenadas de textura geradas automaticamente podem reduzir significativamente a largura de banda necessária para dados de geometria eliminando a necessidade de coordenadas de textura explícitas no formato de vértice.</span><span class="sxs-lookup"><span data-stu-id="82773-106">Automatically generated texture coordinates can significantly reduce the bandwidth required for geometry data by eliminating the need for explicit texture coordinates in the vertex format.</span></span> <span data-ttu-id="82773-107">Em muitos casos, as coordenadas de textura que o sistema gera podem ser usadas com transformações para produzir efeitos especiais.</span><span class="sxs-lookup"><span data-stu-id="82773-107">In many cases, the texture coordinates that the system generates can be used with transformations to produce special effects.</span></span> <span data-ttu-id="82773-108">É claro que esse é um recurso de finalidade especial e você usará coordenadas de textura explícitas para muitas ocasiões.</span><span class="sxs-lookup"><span data-stu-id="82773-108">Of course, this is a special-purpose feature, and you will use explicit texture coordinates for many occasions.</span></span>

## <a name="configuring-automatically-generated-texture-coordinates"></a><span data-ttu-id="82773-109">Configurando coordenadas de textura geradas automaticamente</span><span class="sxs-lookup"><span data-stu-id="82773-109">Configuring Automatically Generated Texture Coordinates</span></span>

<span data-ttu-id="82773-110">No C++, o estado de estágio de textura DE TEXCOORDINDEX D3DTSS (do tipo \_ enumerado [**D3DTEXTURESTAGESTATETYPE)**](./d3dtexturestagestatetype.md) controla como o sistema gera coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="82773-110">In C++, the D3DTSS\_TEXCOORDINDEX texture-stage state (from the [**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md) enumerated type) controls how the system generates texture coordinates.</span></span>

<span data-ttu-id="82773-111">Normalmente, esse estado instrui o sistema a usar um conjunto específico de coordenadas de textura codificadas no formato de vértice.</span><span class="sxs-lookup"><span data-stu-id="82773-111">Normally, this state instructs the system to use a particular set of texture coordinates encoded in the vertex format.</span></span> <span data-ttu-id="82773-112">Quando você inclui os sinalizadores \_ \_ CAMERASPACENORMAL, D3DTSS \_ TCI \_ CAMERASPACEPOSITION ou D3DTSS \_ \_ TCI CAMERASPACEREFLECTIONVECTOR no valor que você atribui a esse estado, o comportamento do sistema é bastante diferente.</span><span class="sxs-lookup"><span data-stu-id="82773-112">When you include the D3DTSS\_TCI\_CAMERASPACENORMAL, D3DTSS\_TCI\_CAMERASPACEPOSITION, or D3DTSS\_TCI\_CAMERASPACEREFLECTIONVECTOR flags in the value that you assign to this state, the system behavior is quite different.</span></span> <span data-ttu-id="82773-113">Se qualquer um desses sinalizadores estiver presente, o estágio de textura ignorará as coordenadas de textura dentro do formato de vértice em favor das coordenadas que o sistema gera.</span><span class="sxs-lookup"><span data-stu-id="82773-113">If any of these flags are present, the texture stage ignores the texture coordinates within the vertex format in favor of coordinates that the system generates.</span></span> <span data-ttu-id="82773-114">Os significados de cada sinalizador são mostrados na lista a seguir.</span><span class="sxs-lookup"><span data-stu-id="82773-114">The meanings for each flag are shown in the following list.</span></span>

-   <span data-ttu-id="82773-115">D3DTSS \_ TCI \_ CAMERASPACENORMAL</span><span class="sxs-lookup"><span data-stu-id="82773-115">D3DTSS\_TCI\_CAMERASPACENORMAL</span></span>

    <span data-ttu-id="82773-116">Use o vértice normal, transformado para o espaço da câmera, como coordenadas de textura de entrada.</span><span class="sxs-lookup"><span data-stu-id="82773-116">Use the vertex normal, transformed to camera space, as input texture coordinates.</span></span>

-   <span data-ttu-id="82773-117">D3DTSS \_ TCI \_ CAMERASPACEPOSITION</span><span class="sxs-lookup"><span data-stu-id="82773-117">D3DTSS\_TCI\_CAMERASPACEPOSITION</span></span>

    <span data-ttu-id="82773-118">Use a posição do vértice, transformada no espaço da câmera, como coordenadas de textura de entrada.</span><span class="sxs-lookup"><span data-stu-id="82773-118">Use the vertex position, transformed to camera space, as input texture coordinates.</span></span>

-   <span data-ttu-id="82773-119">D3DTSS \_ TCI \_ CAMERASPACEREFLECTIONVECTOR</span><span class="sxs-lookup"><span data-stu-id="82773-119">D3DTSS\_TCI\_CAMERASPACEREFLECTIONVECTOR</span></span>

    <span data-ttu-id="82773-120">Use o vetor de reflexo, transformado no espaço da câmera, como coordenadas de textura de entrada.</span><span class="sxs-lookup"><span data-stu-id="82773-120">Use the reflection vector, transformed to camera space, as input texture coordinates.</span></span> <span data-ttu-id="82773-121">O vetor de reflexão é calculado a partir da posição do vértice de entrada e do vetor normal.</span><span class="sxs-lookup"><span data-stu-id="82773-121">The reflection vector is computed from the input vertex position and normal vector.</span></span>

<span data-ttu-id="82773-122">Os sinalizadores de índice de coordenadas de textura são mutuamente exclusivos.</span><span class="sxs-lookup"><span data-stu-id="82773-122">The texture coordinate index flags are mutually exclusive.</span></span> <span data-ttu-id="82773-123">Este exemplo usa:</span><span class="sxs-lookup"><span data-stu-id="82773-123">This example uses:</span></span>

-   <span data-ttu-id="82773-124">A posição do vértice (em câmera-espaço) como as coordenadas de textura de entrada para este estágio de textura</span><span class="sxs-lookup"><span data-stu-id="82773-124">The vertex position (in camera-space) as the input texture coordinates for this texture stage</span></span>
-   <span data-ttu-id="82773-125">O modo Wrap definido no estado de \_ RENDERIZAÇÃO D3DRENDERSTATE WRAP1</span><span class="sxs-lookup"><span data-stu-id="82773-125">The wrap mode set in the D3DRENDERSTATE\_WRAP1 render state</span></span>


```
// Assume d3dDevice is a valid pointer to an IDirect3DDevice9 interface
d3dDevice->SetTextureStageState(0, D3DTSS_TEXCOORDINDEX, 
                                   D3DTSS_TCI_CAMERASPACEPOSITION | 1);
```



<span data-ttu-id="82773-126">Coordenadas de textura geradas automaticamente são mais úteis como valores de entrada para uma transformação de coordenadas de textura ou para eliminar a necessidade de seu aplicativo de computar vetores de três elementos para mapas de ambiente cúbico.</span><span class="sxs-lookup"><span data-stu-id="82773-126">Automatically generated texture coordinates are most useful as input values for a texture coordinate transformation, or to eliminate the need for your application to compute three-element vectors for cubic-environment maps.</span></span>

<span data-ttu-id="82773-127">O mapeamento de esfera usa um mapa de textura de computação (no momento do modelo) que contém todo o ambiente, conforme refletido por uma esfera do Chrome.</span><span class="sxs-lookup"><span data-stu-id="82773-127">Sphere-mapping uses a precomputed (at model time) texture map that contains the entire environment as reflected by a chrome sphere.</span></span> <span data-ttu-id="82773-128">O Direct3D tem um recurso de geração de coordenadas de textura usando o estado de renderização D3DTSS \_ TCI \_ CAMERASPACENORMAL, que assume o normal do vértice no espaço da câmera e o coloca por meio de uma transformação de textura para gerar coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="82773-128">Direct3D has a texture-coordinate generation feature using render state D3DTSS\_TCI\_CAMERASPACENORMAL, which takes the normal of the vertex in camera space and puts it through a texture transform to generate texture coordinates.</span></span>

## <a name="related-topics"></a><span data-ttu-id="82773-129">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="82773-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="82773-130">Processamento de coordenadas de textura</span><span class="sxs-lookup"><span data-stu-id="82773-130">Texture Coordinate Processing</span></span>](texture-coordinate-processing.md)
</dt> <dt>

[<span data-ttu-id="82773-131">Transformações de coordenadas de textura (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="82773-131">Texture Coordinate Transformations (Direct3D 9)</span></span>](texture-coordinate-transformations.md)
</dt> <dt>

[<span data-ttu-id="82773-132">Mapeamento de ambiente cúbico (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="82773-132">Cubic Environment Mapping (Direct3D 9)</span></span>](cubic-environment-mapping.md)
</dt> </dl>

 

 
