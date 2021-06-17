---
description: Saiba mais sobre a mistura alfa. A mesclagem alfa é usada para exibir uma imagem que tem pixels transparentes ou semi-transparente.
ms.assetid: 553b0bc8-1bd8-4282-9260-cdc5f2b8788d
title: Mistura alfa (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd79c622778e17c5acb9b17d52b6d5db278b1508
ms.sourcegitcommit: d0eb44d0a95f5e5efbfec3d3e9c143f5cba25bc3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/17/2021
ms.locfileid: "112261998"
---
# <a name="alpha-blending-direct3d-9"></a><span data-ttu-id="63dc2-104">Mistura alfa (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="63dc2-104">Alpha Blending (Direct3D 9)</span></span>

<span data-ttu-id="63dc2-105">A mesclagem alfa é usada para exibir uma imagem que tem pixels transparentes ou semi-transparente.</span><span class="sxs-lookup"><span data-stu-id="63dc2-105">Alpha blending is used to display an image that has transparent or semi-transparent pixels.</span></span> <span data-ttu-id="63dc2-106">Além de um canal de cores vermelho, verde e azul, cada pixel em um bitmap alfa tem um componente de transparência conhecido como seu canal alfa.</span><span class="sxs-lookup"><span data-stu-id="63dc2-106">In addition to a red, green, and blue color channel, each pixel in an alpha bitmap has a transparency component known as its alpha channel.</span></span> <span data-ttu-id="63dc2-107">Normalmente, o canal alfa contém tantos bits quanto um canal de cores.</span><span class="sxs-lookup"><span data-stu-id="63dc2-107">The alpha channel typically contains as many bits as a color channel.</span></span> <span data-ttu-id="63dc2-108">Por exemplo, um canal alfa de 8 bits pode representar 256 níveis de transparência, de 0 (o pixel inteiro é transparente) a 255 (o pixel inteiro é opaco).</span><span class="sxs-lookup"><span data-stu-id="63dc2-108">For example, an 8-bit alpha channel can represent 256 levels of transparency, from 0 (the entire pixel is transparent) to 255 (the entire pixel is opaque).</span></span> <span data-ttu-id="63dc2-109">A lista a seguir mostra alguns efeitos especiais que você pode criar usando a mistura alfa.</span><span class="sxs-lookup"><span data-stu-id="63dc2-109">The list below shows some special effects you can create using alpha blending.</span></span>

<span data-ttu-id="63dc2-110">A cor pode ser definida com ou sem valores Alfa.</span><span class="sxs-lookup"><span data-stu-id="63dc2-110">Color can be defined with or without alpha values.</span></span> <span data-ttu-id="63dc2-111">Color sem alfa é a cor RGB com alfa é armazenada como ARGB.</span><span class="sxs-lookup"><span data-stu-id="63dc2-111">Color without alpha is RGB color with alpha is stored as ARGB.</span></span> <span data-ttu-id="63dc2-112">Dados de vértice, dados de material e dados de textura podem ser usados para fornecer transparência do objeto.</span><span class="sxs-lookup"><span data-stu-id="63dc2-112">Vertex data, material data and texture data can be used to give object's transparency.</span></span> <span data-ttu-id="63dc2-113">O buffer de quadros também pode ser usado para gerar efeitos de transparência.</span><span class="sxs-lookup"><span data-stu-id="63dc2-113">The frame buffer can also be used to generate transparency effects.</span></span>

-   [<span data-ttu-id="63dc2-114">Vértice alfa (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="63dc2-114">Vertex Alpha (Direct3D 9)</span></span>](vertex-alpha.md)
-   [<span data-ttu-id="63dc2-115">Material alfa (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="63dc2-115">Material Alpha (Direct3D 9)</span></span>](material-alpha.md)
-   [<span data-ttu-id="63dc2-116">Textura alfa (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="63dc2-116">Texture Alpha (Direct3D 9)</span></span>](texture-alpha.md)
-   [<span data-ttu-id="63dc2-117">Buffer de quadro alfa (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="63dc2-117">Frame Buffer Alpha (Direct3D 9)</span></span>](frame-buffer-alpha.md)
-   [<span data-ttu-id="63dc2-118">Processamento alfa de destino (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="63dc2-118">Render Target Alpha (Direct3D 9)</span></span>](render-target-alpha.md)

<span data-ttu-id="63dc2-119">Exemplos que demonstram alfa incluem:</span><span class="sxs-lookup"><span data-stu-id="63dc2-119">Samples that demonstrate alpha include:</span></span>

-   [<span data-ttu-id="63dc2-120">Mural (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="63dc2-120">Billboarding (Direct3D 9)</span></span>](billboarding.md)
-   [<span data-ttu-id="63dc2-121">Nuvens, fumaça e trilhas Vapors (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="63dc2-121">Clouds, Smoke, and Vapor Trails (Direct3D 9)</span></span>](clouds--smoke--and-vapor-trails.md)
-   [<span data-ttu-id="63dc2-122">Fogo, flares e explosões (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="63dc2-122">Fire, Flares, and Explosions (Direct3D 9)</span></span>](fire--flares--and-explosions.md)

## <a name="related-topics"></a><span data-ttu-id="63dc2-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="63dc2-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="63dc2-124">Renderização de Direct3D</span><span class="sxs-lookup"><span data-stu-id="63dc2-124">Direct3D Rendering</span></span>](direct3d-rendering.md)
</dt> </dl>

 

 



