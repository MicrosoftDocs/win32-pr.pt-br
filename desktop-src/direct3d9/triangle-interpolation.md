---
description: Durante a renderização, o pipeline interpola os dados de vértice em cada triângulo.
ms.assetid: 6fa05e56-c4cd-4623-abe9-2b1c8bbc644b
title: Interpolação de triângulo (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 405cbecd6123145d412a3e7f58f727bdf5b5a3e8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105791464"
---
# <a name="triangle-interpolation-direct3d-9"></a><span data-ttu-id="a1c00-103">Interpolação de triângulo (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="a1c00-103">Triangle Interpolation (Direct3D 9)</span></span>

<span data-ttu-id="a1c00-104">Durante a renderização, o pipeline interpola os dados de vértice em cada triângulo.</span><span class="sxs-lookup"><span data-stu-id="a1c00-104">During rendering, the pipeline interpolates vertex data across each triangle.</span></span> <span data-ttu-id="a1c00-105">Os dados de vértice podem ser uma grande variedade de dados e podem incluir (mas não se limitam a): cor difusa, cor especular, alfa difusa (opacidade de triângulo), alfanuméricos de especulação e um fator de neblina (tirado da especulação alfa para pipeline de vértice de função fixa e do registro de neblina para pipeline de vértice programável).</span><span class="sxs-lookup"><span data-stu-id="a1c00-105">Vertex data can be a broad variety of data and can include (but is not limited to): diffuse color, specular color, diffuse alpha (triangle opacity), specular alpha, and a fog factor (taken from specular alpha for fixed function vertex pipeline and from fog register for programmable vertex pipeline).</span></span> <span data-ttu-id="a1c00-106">Os dados de vértice são definidos pela [declaração de vértice (Direct3D 9)](vertex-declaration.md).</span><span class="sxs-lookup"><span data-stu-id="a1c00-106">The vertex data is defined by the [Vertex Declaration (Direct3D 9)](vertex-declaration.md).</span></span>

<span data-ttu-id="a1c00-107">Para alguns dados de vértice, a interpolação depende do modo de sombreamento atual, conforme mostrado na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="a1c00-107">For some vertex data, the interpolation is dependent on the current shading mode, as shown in the following table.</span></span>



| <span data-ttu-id="a1c00-108">Modo de sombreamento</span><span class="sxs-lookup"><span data-stu-id="a1c00-108">Shading mode</span></span> | <span data-ttu-id="a1c00-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="a1c00-109">Description</span></span>                                                                                                                                                                 |
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a1c00-110">Plano</span><span class="sxs-lookup"><span data-stu-id="a1c00-110">Flat</span></span>         | <span data-ttu-id="a1c00-111">Somente o fator de nevoeiro é interpolado no modo de sombreamento simples.</span><span class="sxs-lookup"><span data-stu-id="a1c00-111">Only the fog factor is interpolated in flat shade mode.</span></span> <span data-ttu-id="a1c00-112">Para todos os outros valores interpolados, a cor do primeiro vértice no triângulo é aplicada em toda a face.</span><span class="sxs-lookup"><span data-stu-id="a1c00-112">For all other interpolated values, the color of the first vertex in the triangle is applied across the entire face.</span></span> |
| <span data-ttu-id="a1c00-113">Gouraud</span><span class="sxs-lookup"><span data-stu-id="a1c00-113">Gouraud</span></span>      | <span data-ttu-id="a1c00-114">A interpolação linear é executada entre todos os três vértices.</span><span class="sxs-lookup"><span data-stu-id="a1c00-114">Linear interpolation is performed between all three vertices.</span></span>                                                                                                               |



 

<span data-ttu-id="a1c00-115">As cores difusas e realces especulares são tratados de forma diferente, dependendo do modelo de cor.</span><span class="sxs-lookup"><span data-stu-id="a1c00-115">The diffuse color and specular color are treated differently, depending on the color model.</span></span> <span data-ttu-id="a1c00-116">No modelo de cor RGB, o sistema usa os componentes de cor vermelha, verde e azul na interpolação.</span><span class="sxs-lookup"><span data-stu-id="a1c00-116">In the RGB color model, the system uses the red, green, and blue color components in the interpolation.</span></span>

<span data-ttu-id="a1c00-117">O componente alfa de uma cor é tratado como um valor interpolado separado porque drivers de dispositivo podem implementar transparência de duas maneiras diferentes: utilizando uma mesclagem de textura ou usando textura pontilhada.</span><span class="sxs-lookup"><span data-stu-id="a1c00-117">The alpha component of a color is treated as a separate interpolated value because device drivers can implement transparency in two different ways: by using texture blending or by using stippling.</span></span>

<span data-ttu-id="a1c00-118">Use o membro ShadeCaps da estrutura [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) para determinar a quais formas de interpolação o driver de dispositivo atual oferece suporte.</span><span class="sxs-lookup"><span data-stu-id="a1c00-118">Use the ShadeCaps member of the [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) structure to determine what forms of interpolation the current device driver supports.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a1c00-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a1c00-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a1c00-120">Coordenar sistemas e geometria</span><span class="sxs-lookup"><span data-stu-id="a1c00-120">Coordinate Systems and Geometry</span></span>](coordinate-systems-and-geometry.md)
</dt> </dl>

 

 



