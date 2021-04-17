---
description: As imagens 3D geradas por computador antigamente, embora geralmente avançadas para o tempo, tendiam a ter uma aparência de plástico brilhante.
ms.assetid: 548ae140-c746-4fab-8000-421289d4f0a2
title: Conceitos básicos de texturing (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba8c4971f70cbe5b7b371f71191de6edb4c2be46
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105761208"
---
# <a name="basic-texturing-concepts-direct3d-9"></a><span data-ttu-id="8c066-103">Conceitos básicos de texturing (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="8c066-103">Basic Texturing Concepts (Direct3D 9)</span></span>

<span data-ttu-id="8c066-104">As imagens 3D geradas por computador antigamente, embora geralmente avançadas para o tempo, tendiam a ter uma aparência de plástico brilhante.</span><span class="sxs-lookup"><span data-stu-id="8c066-104">Early computer-generated 3D images, although generally advanced for their time, tended to have a shiny plastic look.</span></span> <span data-ttu-id="8c066-105">Eles não tinham os tipos de marcações como arranhões, rachaduras, impressões digitais e manchas da tela que dão aos objetos 3D uma complexidade visual realística.</span><span class="sxs-lookup"><span data-stu-id="8c066-105">They lacked the types of markings-such as scuffs, cracks, fingerprints, and smudges-that give 3D objects realistic visual complexity.</span></span> <span data-ttu-id="8c066-106">Nos últimos anos, as texturas ganharam popularidade entre os desenvolvedores como uma ferramenta para aprimorar o realm de imagens 3D geradas por computador.</span><span class="sxs-lookup"><span data-stu-id="8c066-106">In recent years, textures have gained popularity among developers as a tool for enhancing the realism of computer-generated 3D images.</span></span>

<span data-ttu-id="8c066-107">No seu uso diário, a textura word se refere à suavidade ou aspereza de um objeto.</span><span class="sxs-lookup"><span data-stu-id="8c066-107">In its everyday use, the word texture refers to an object's smoothness or roughness.</span></span> <span data-ttu-id="8c066-108">Em gráficos de computador, no entanto, uma textura será um bitmap de cores de pixels que dá a aparência de textura de um objeto.</span><span class="sxs-lookup"><span data-stu-id="8c066-108">In computer graphics, however, a texture is a bitmap of pixel colors that give an object the appearance of texture.</span></span>

<span data-ttu-id="8c066-109">Como as texturas do Direct3D são bitmaps, qualquer bitmap pode ser aplicado a uma primitiva do Direct3D.</span><span class="sxs-lookup"><span data-stu-id="8c066-109">Because Direct3D textures are bitmaps, any bitmap can be applied to a Direct3D primitive.</span></span> <span data-ttu-id="8c066-110">Por exemplo, os apps podem criar e tratar os objetos que aparecem com um padrão de madeira neles.</span><span class="sxs-lookup"><span data-stu-id="8c066-110">For instance, applications can create and manipulate objects that appear to have a wood grain pattern in them.</span></span> <span data-ttu-id="8c066-111">Grama, sujeira e rochas podem ser aplicadas a um conjunto de primitivas 3D que formam uma colina.</span><span class="sxs-lookup"><span data-stu-id="8c066-111">Grass, dirt, and rocks can be applied to a set of 3D primitives that form a hill.</span></span> <span data-ttu-id="8c066-112">O resultado é uma colina realista.</span><span class="sxs-lookup"><span data-stu-id="8c066-112">The result is a realistic-looking hillside.</span></span> <span data-ttu-id="8c066-113">Você também pode usar a textura para criar efeitos como sinais ao longo de um acostamento, estratos de rocha em um penhasco, ou a aparência de mármore no chão.</span><span class="sxs-lookup"><span data-stu-id="8c066-113">You can also use texturing to create effects such as signs along a roadside, rock strata in a cliff, or the appearance of marble on a floor.</span></span>

<span data-ttu-id="8c066-114">Além disso, o Direct3D dá suporte a técnicas mais avançadas de texturização como a mesclagem de textura com ou sem transparência e o mapeamento de luz.</span><span class="sxs-lookup"><span data-stu-id="8c066-114">In addition, Direct3D supports more advanced texturing techniques such as texture blending-with or without transparency-and light mapping.</span></span> <span data-ttu-id="8c066-115">Para obter mais informações, consulte [mesclagem de textura (Direct3D 9)](texture-blending.md) e o [mapeamento claro com texturas (Direct3D 9)](light-mapping-with-textures.md).</span><span class="sxs-lookup"><span data-stu-id="8c066-115">For more information, see [Texture Blending (Direct3D 9)](texture-blending.md) and [Light Mapping with Textures (Direct3D 9)](light-mapping-with-textures.md).</span></span>

<span data-ttu-id="8c066-116">Se seu app criar um dispositivo de camada de abstração de hardware (HAL) ou um dispositivo de software, ele pode usar texturas de 8, 16, 24, 32, 64 ou 128 bits.</span><span class="sxs-lookup"><span data-stu-id="8c066-116">If your application creates a hardware abstraction layer (HAL) device or a software device, it can use 8, 16, 24, 32, 64, or 128-bit textures.</span></span>

<span data-ttu-id="8c066-117">Informações adicionais estão contidas nos tópicos a seguir.</span><span class="sxs-lookup"><span data-stu-id="8c066-117">Additional information is contained in the following topics.</span></span>

-   [<span data-ttu-id="8c066-118">Modos de endereçamento de textura (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="8c066-118">Texture Addressing Modes (Direct3D 9)</span></span>](texture-addressing-modes.md)
-   [<span data-ttu-id="8c066-119">Regiões com problemas de textura (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="8c066-119">Texture Dirty Regions (Direct3D 9)</span></span>](texture-dirty-regions.md)
-   [<span data-ttu-id="8c066-120">Paletas de textura (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="8c066-120">Texture Palettes (Direct3D 9)</span></span>](texture-palettes.md)

## <a name="related-topics"></a><span data-ttu-id="8c066-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8c066-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8c066-122">Texturas do Direct3D</span><span class="sxs-lookup"><span data-stu-id="8c066-122">Direct3D Textures</span></span>](direct3d-textures.md)
</dt> </dl>

 

 



