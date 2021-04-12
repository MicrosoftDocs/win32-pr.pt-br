---
description: A mesclagem alfa é usada para exibir uma imagem que tem pixels transparentes ou semi-transparente.
ms.assetid: 553b0bc8-1bd8-4282-9260-cdc5f2b8788d
title: Mistura alfa (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f4ae2883c7a9a92ba1b62306dc26bf09d0d9947
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089416"
---
# <a name="alpha-blending-direct3d-9"></a><span data-ttu-id="8a26c-103">Mistura alfa (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="8a26c-103">Alpha Blending (Direct3D 9)</span></span>

<span data-ttu-id="8a26c-104">A mesclagem alfa é usada para exibir uma imagem que tem pixels transparentes ou semi-transparente.</span><span class="sxs-lookup"><span data-stu-id="8a26c-104">Alpha blending is used to display an image that has transparent or semi-transparent pixels.</span></span> <span data-ttu-id="8a26c-105">Além de um canal de cores vermelho, verde e azul, cada pixel em um bitmap alfa tem um componente de transparência conhecido como seu canal alfa.</span><span class="sxs-lookup"><span data-stu-id="8a26c-105">In addition to a red, green, and blue color channel, each pixel in an alpha bitmap has a transparency component known as its alpha channel.</span></span> <span data-ttu-id="8a26c-106">Normalmente, o canal alfa contém tantos bits quanto um canal de cores.</span><span class="sxs-lookup"><span data-stu-id="8a26c-106">The alpha channel typically contains as many bits as a color channel.</span></span> <span data-ttu-id="8a26c-107">Por exemplo, um canal alfa de 8 bits pode representar 256 níveis de transparência, de 0 (o pixel inteiro é transparente) a 255 (o pixel inteiro é opaco).</span><span class="sxs-lookup"><span data-stu-id="8a26c-107">For example, an 8-bit alpha channel can represent 256 levels of transparency, from 0 (the entire pixel is transparent) to 255 (the entire pixel is opaque).</span></span> <span data-ttu-id="8a26c-108">A lista a seguir mostra alguns efeitos especiais que você pode criar usando a mistura alfa.</span><span class="sxs-lookup"><span data-stu-id="8a26c-108">The list below shows some special effects you can create using alpha blending.</span></span>

<span data-ttu-id="8a26c-109">A cor pode ser definida com ou sem valores Alfa.</span><span class="sxs-lookup"><span data-stu-id="8a26c-109">Color can be defined with or without alpha values.</span></span> <span data-ttu-id="8a26c-110">Color sem alfa é a cor RGB com alfa é armazenada como ARGB.</span><span class="sxs-lookup"><span data-stu-id="8a26c-110">Color without alpha is RGB color with alpha is stored as ARGB.</span></span> <span data-ttu-id="8a26c-111">Dados de vértice, dados de material e dados de textura podem ser usados para fornecer transparência do objeto.</span><span class="sxs-lookup"><span data-stu-id="8a26c-111">Vertex data, material data and texture data can be used to give object's transparency.</span></span> <span data-ttu-id="8a26c-112">O buffer de quadros também pode ser usado para gerar efeitos de transparência.</span><span class="sxs-lookup"><span data-stu-id="8a26c-112">The frame buffer can also be used to generate transparency effects.</span></span>

-   [<span data-ttu-id="8a26c-113">Vértice alfa (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="8a26c-113">Vertex Alpha (Direct3D 9)</span></span>](vertex-alpha.md)
-   [<span data-ttu-id="8a26c-114">Material alfa (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="8a26c-114">Material Alpha (Direct3D 9)</span></span>](material-alpha.md)
-   [<span data-ttu-id="8a26c-115">Textura alfa (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="8a26c-115">Texture Alpha (Direct3D 9)</span></span>](texture-alpha.md)
-   [<span data-ttu-id="8a26c-116">Buffer de quadro alfa (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="8a26c-116">Frame Buffer Alpha (Direct3D 9)</span></span>](frame-buffer-alpha.md)
-   [<span data-ttu-id="8a26c-117">Processamento alfa de destino (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="8a26c-117">Render Target Alpha (Direct3D 9)</span></span>](render-target-alpha.md)

<span data-ttu-id="8a26c-118">Exemplos que demonstram alfa incluem:</span><span class="sxs-lookup"><span data-stu-id="8a26c-118">Samples that demonstrate alpha include:</span></span>

-   [<span data-ttu-id="8a26c-119">Mural (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="8a26c-119">Billboarding (Direct3D 9)</span></span>](billboarding.md)
-   [<span data-ttu-id="8a26c-120">Nuvens, fumaça e trilhas Vapors (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="8a26c-120">Clouds, Smoke, and Vapor Trails (Direct3D 9)</span></span>](clouds--smoke--and-vapor-trails.md)
-   [<span data-ttu-id="8a26c-121">Fogo, flares e explosões (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="8a26c-121">Fire, Flares, and Explosions (Direct3D 9)</span></span>](fire--flares--and-explosions.md)

## <a name="related-topics"></a><span data-ttu-id="8a26c-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8a26c-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8a26c-123">Renderização de Direct3D</span><span class="sxs-lookup"><span data-stu-id="8a26c-123">Direct3D Rendering</span></span>](direct3d-rendering.md)
</dt> </dl>

 

 



