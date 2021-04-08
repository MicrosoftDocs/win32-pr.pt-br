---
description: Aplicativos Direct3D usam decalque para controlar quais pixels de uma determinada imagem primitiva são desenhados na superfície de destino de renderização. Os apps aplicam os decalques às imagens de objetos primitivos para permitir que polígonos coplanares sejam renderizados corretamente.
ms.assetid: 0d57983c-c8f3-4095-9495-a3ec5d280bda
title: Decaling (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5606bdbc798d8b1e834aff53b04984f659af650
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087391"
---
# <a name="decaling-direct3d-9"></a><span data-ttu-id="38c0c-104">Decaling (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="38c0c-104">Decaling (Direct3D 9)</span></span>

<span data-ttu-id="38c0c-105">Aplicativos Direct3D usam decalque para controlar quais pixels de uma determinada imagem primitiva são desenhados na superfície de destino de renderização.</span><span class="sxs-lookup"><span data-stu-id="38c0c-105">Direct3D applications use decaling to control which pixels from a particular primitive image are drawn to the rendering target surface.</span></span> <span data-ttu-id="38c0c-106">Os apps aplicam os decalques às imagens de objetos primitivos para permitir que polígonos coplanares sejam renderizados corretamente.</span><span class="sxs-lookup"><span data-stu-id="38c0c-106">Applications apply decals to the images of primitives to enable coplanar polygons to render correctly.</span></span>

<span data-ttu-id="38c0c-107">Por exemplo, ao aplicar marcas de pneus e linhas amarelas em uma estrada, as marcas devem aparecer diretamente sobre a pista.</span><span class="sxs-lookup"><span data-stu-id="38c0c-107">For instance, when applying tire marks and yellow lines to a roadway, the markings should appear directly on top of the road.</span></span> <span data-ttu-id="38c0c-108">No entanto, os valores z das marcas e da estrada são os mesmos.</span><span class="sxs-lookup"><span data-stu-id="38c0c-108">However, the z values of the markings and the road are the same.</span></span> <span data-ttu-id="38c0c-109">Portanto, o buffer de profundidade pode não produzir uma separação clara entre os dois.</span><span class="sxs-lookup"><span data-stu-id="38c0c-109">Therefore, the depth buffer might not produce a clean separation between the two.</span></span> <span data-ttu-id="38c0c-110">Alguns pixels da parte primitiva traseira podem ser renderizados na parte superior da parte primitiva frontal e vice-versa.</span><span class="sxs-lookup"><span data-stu-id="38c0c-110">Some pixels in the back primitive may be rendered on top of the front primitive and vice versa.</span></span> <span data-ttu-id="38c0c-111">A imagem resultante parece tremida de quadro a quadro.</span><span class="sxs-lookup"><span data-stu-id="38c0c-111">The resulting image appears to shimmer from frame to frame.</span></span> <span data-ttu-id="38c0c-112">Esse efeito é chamado *luta z* ou *flimmering*.</span><span class="sxs-lookup"><span data-stu-id="38c0c-112">This effect is called *z-fighting* or *flimmering*.</span></span>

<span data-ttu-id="38c0c-113">Para resolver esse problema, use um estêncil para mascarar a seção da parte traseira primitiva onde aparecerá o decalque.</span><span class="sxs-lookup"><span data-stu-id="38c0c-113">To solve this problem, use a stencil to mask the section of the back primitive where the decal will appear.</span></span> <span data-ttu-id="38c0c-114">Desligue o buffer z e renderize a imagem da parte primitiva dianteira na área sem máscara da superfície de destino de renderização.</span><span class="sxs-lookup"><span data-stu-id="38c0c-114">Turn off z-buffering and render the image of the front primitive into the masked-off area of the render-target surface.</span></span>

<span data-ttu-id="38c0c-115">Embora diversas mesclagens de textura possam ser usadas para resolver esse problema, fazer isso limitará o número de outros efeitos especiais que seu aplicativo pode produzir.</span><span class="sxs-lookup"><span data-stu-id="38c0c-115">Although multiple texture blending can be used to solve this problem, doing so limits the number of other special effects that your application can produce.</span></span> <span data-ttu-id="38c0c-116">Usar o buffer de estêncil para aplicar os decalques libera estágios de mesclagem de textura para outros efeitos.</span><span class="sxs-lookup"><span data-stu-id="38c0c-116">Using the stencil buffer to apply decals frees up texture blending stages for other effects.</span></span>

## <a name="related-topics"></a><span data-ttu-id="38c0c-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="38c0c-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="38c0c-118">Técnicas de buffer de estêncil</span><span class="sxs-lookup"><span data-stu-id="38c0c-118">Stencil Buffer Techniques</span></span>](stencil-buffer-techniques.md)
</dt> </dl>

 

 



