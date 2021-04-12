---
description: O mapeamento de relevo é uma forma especial de mapeamento de ambiente especular ou difuso que simula os reflexos de objetos mosaico sem exigir contagens de polígono extremamente altas.
ms.assetid: 3e195e4f-3fa9-43c4-b2e5-42a6b3aaccf2
title: Mapeamento de relevo (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9dba4621568f595eae965941168ad6930e183f7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089491"
---
# <a name="bump-mapping-direct3d-9"></a><span data-ttu-id="243b3-103">Mapeamento de relevo (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="243b3-103">Bump Mapping (Direct3D 9)</span></span>

<span data-ttu-id="243b3-104">O mapeamento de relevo é uma forma especial de mapeamento de ambiente especular ou difuso que simula os reflexos de objetos mosaico sem exigir contagens de polígono extremamente altas.</span><span class="sxs-lookup"><span data-stu-id="243b3-104">Bump mapping is a special form of specular or diffuse environment mapping that simulates the reflections of finely tessellated objects without requiring extremely high polygon counts.</span></span> <span data-ttu-id="243b3-105">O mapeamento de relevo implementado pelo Direct3D pode ser descrito com precisão como muito de coordenadas de textura por pixel de mapas de ambiente especular ou difuso, pois você fornece informações sobre a delimitação do mapa de relevo em termos de valores Delta, que o sistema aplica às coordenadas de textura de você e v de um mapa de ambiente no próximo estágio de textura.</span><span class="sxs-lookup"><span data-stu-id="243b3-105">Bump mapping implemented by Direct3D can be accurately described as per-pixel texture coordinate perturbation of specular or diffuse environment maps, because you provide information about the contour of the bump map in terms of delta values, which the system applies to the u and v texture coordinates of an environment map in the next texture stage.</span></span> <span data-ttu-id="243b3-106">Os valores Delta são codificados no formato de pixel da superfície do mapa de relevo (consulte [formatos de pixel do mapa de relevo](bump-map-pixel-formats.md)).</span><span class="sxs-lookup"><span data-stu-id="243b3-106">The delta values are encoded in the pixel format of the bump map surface (see [Bump Map Pixel Formats](bump-map-pixel-formats.md)).</span></span>

<span data-ttu-id="243b3-107">O mapeamento de choques depende de mesclar várias texturas.</span><span class="sxs-lookup"><span data-stu-id="243b3-107">Bump mapping relies on blending multiple textures.</span></span> <span data-ttu-id="243b3-108">Isso significa que o dispositivo deve dar suporte a pelo menos dois estágios de mesclagem; um para o mapa de relevo e outro para um mapa de ambiente.</span><span class="sxs-lookup"><span data-stu-id="243b3-108">This means the device must support at least two blending stages; one for the bump map and another for an environment map.</span></span> <span data-ttu-id="243b3-109">Um mínimo de três estágios de mesclagem de textura é necessário para aplicar um mapa de textura de base adicional, que é o caso mais comum.</span><span class="sxs-lookup"><span data-stu-id="243b3-109">A minimum of three texture blending stages are required to apply an additional base texture map, which is the most common case.</span></span> <span data-ttu-id="243b3-110">O diagrama a seguir mostra as relações entre a textura básica, o mapa de relevo e o mapa do ambiente na cascata de mesclagem de textura.</span><span class="sxs-lookup"><span data-stu-id="243b3-110">The following diagram shows the relationships between the base texture, the bump map, and the environment map in the texture blending cascade.</span></span>

![diagrama da cascata de mesclagem de textura](images/bumpmap-tcascade.png)

<span data-ttu-id="243b3-112">Você deve preparar os estágios de textura adequadamente para habilitar o mapeamento de rebatida.</span><span class="sxs-lookup"><span data-stu-id="243b3-112">You must prepare the texture stages appropriately to enable bump mapping.</span></span> <span data-ttu-id="243b3-113">Os tópicos a seguir apresentam o mapeamento de relevo e fornecem detalhes sobre como você pode usá-lo em seus aplicativos:</span><span class="sxs-lookup"><span data-stu-id="243b3-113">The following topics introduce bump mapping, and provide details about how you can use it in your applications:</span></span>

-   [<span data-ttu-id="243b3-114">Formatos de pixel do mapa de relevo</span><span class="sxs-lookup"><span data-stu-id="243b3-114">Bump Map Pixel Formats</span></span>](bump-map-pixel-formats.md)
-   [<span data-ttu-id="243b3-115">Fórmulas de mapeamento de relevo</span><span class="sxs-lookup"><span data-stu-id="243b3-115">Bump Mapping Formulas</span></span>](bump-mapping-formulas.md)
-   [<span data-ttu-id="243b3-116">Usando o mapeamento de relevo</span><span class="sxs-lookup"><span data-stu-id="243b3-116">Using Bump Mapping</span></span>](using-bump-mapping.md)

<span data-ttu-id="243b3-117">O Direct3D não dá suporte nativo a mapas de altura; Eles são meramente um formato conveniente para armazenar e Visualizar dados de delimitação.</span><span class="sxs-lookup"><span data-stu-id="243b3-117">Direct3D does not natively support height maps; they are merely a convenient format in which to store and visualize contour data.</span></span> <span data-ttu-id="243b3-118">Seu aplicativo pode armazenar informações de delimitação em qualquer formato ou até mesmo gerar um mapa de relevo de procedimento.</span><span class="sxs-lookup"><span data-stu-id="243b3-118">Your application can store contour information in any format, or even generate a procedural bump map.</span></span>

## <a name="related-topics"></a><span data-ttu-id="243b3-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="243b3-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="243b3-120">Pipeline de pixel</span><span class="sxs-lookup"><span data-stu-id="243b3-120">Pixel Pipeline</span></span>](pixel-pipeline.md)
</dt> </dl>

 

 



