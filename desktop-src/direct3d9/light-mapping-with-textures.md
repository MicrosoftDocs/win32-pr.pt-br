---
description: Para um app renderizar uma cena 3D de forma realista, ele deve considerar o efeito que as fontes de luz tem sobre a aparência da cena.
ms.assetid: ff2037e4-2cf6-4247-b93f-13f0078f3b58
title: Mapeamento claro com texturas (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5652446562e4c66390d67e11fa624a4a5659b85
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105784635"
---
# <a name="light-mapping-with-textures-direct3d-9"></a><span data-ttu-id="c35f0-103">Mapeamento claro com texturas (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="c35f0-103">Light Mapping with Textures (Direct3D 9)</span></span>

<span data-ttu-id="c35f0-104">Para um app renderizar uma cena 3D de forma realista, ele deve considerar o efeito que as fontes de luz tem sobre a aparência da cena.</span><span class="sxs-lookup"><span data-stu-id="c35f0-104">For an application to realistically render a 3D scene, it must take into account the effect that light sources have on the appearance of the scene.</span></span> <span data-ttu-id="c35f0-105">Embora as técnicas como sombreamento simples e de Gouraud sejam ferramentas valiosas nesse sentido, elas podem ser insuficientes para suas necessidades.</span><span class="sxs-lookup"><span data-stu-id="c35f0-105">Although techniques such as flat and Gouraud shading are valuable tools in this respect, they can be insufficient for your needs.</span></span> <span data-ttu-id="c35f0-106">O Direct3D oferece suporte à passagem múltipla e à mesclagem de textura múltipla.</span><span class="sxs-lookup"><span data-stu-id="c35f0-106">Direct3D supports multipass and multiple texture blending.</span></span> <span data-ttu-id="c35f0-107">Esses recursos permitem que o app renderize cenas com uma aparência mais realista do que as cenas renderizadas somente com técnicas de sombreamento.</span><span class="sxs-lookup"><span data-stu-id="c35f0-107">These capabilities enable your application to render scenes with a more realistic appearance than scenes rendered with shading techniques alone.</span></span> <span data-ttu-id="c35f0-108">Ao aplicar um ou mais mapas de luz, o app pode mapear áreas de luz e sombra nos primitivos.</span><span class="sxs-lookup"><span data-stu-id="c35f0-108">By applying one or more light maps, your application can map areas of light and shadow onto its primitives.</span></span>

<span data-ttu-id="c35f0-109">Um mapa de luz é uma textura ou um grupo de texturas que contém informações sobre a iluminação em uma cena 3D.</span><span class="sxs-lookup"><span data-stu-id="c35f0-109">A light map is a texture or group of textures that contains information about lighting in a 3D scene.</span></span> <span data-ttu-id="c35f0-110">Você pode armazenar as informações de iluminação nos valores de alfa do mapa de luz, nos valores de cor ou em ambos.</span><span class="sxs-lookup"><span data-stu-id="c35f0-110">You can store the lighting information in the alpha values of the light map, in the color values, or in both.</span></span>

<span data-ttu-id="c35f0-111">Se você implementar o mapeamento de luz usando a mesclagem de textura de passagem múltipla, o app deve renderizar o mapa de luz nos primitivos na primeira passagem.</span><span class="sxs-lookup"><span data-stu-id="c35f0-111">If you implement light mapping using multipass texture blending, your application should render the light map onto its primitives on the first pass.</span></span> <span data-ttu-id="c35f0-112">Ele deve usar uma segunda passada para renderizar a textura base.</span><span class="sxs-lookup"><span data-stu-id="c35f0-112">It should use a second pass to render the base texture.</span></span> <span data-ttu-id="c35f0-113">A exceção é o mapeamento de luz especular.</span><span class="sxs-lookup"><span data-stu-id="c35f0-113">The exception to this is specular light mapping.</span></span> <span data-ttu-id="c35f0-114">Nesse caso, renderize a textura base primeiro; em seguida, adicione o mapa de luz.</span><span class="sxs-lookup"><span data-stu-id="c35f0-114">In that case, render the base texture first; then add the light map.</span></span>

<span data-ttu-id="c35f0-115">A mistura de textura múltipla permite que o app renderize o mapa de luz e a textura base em uma passagem.</span><span class="sxs-lookup"><span data-stu-id="c35f0-115">Multiple texture blending enables your application to render the light map and the base texture in one pass.</span></span> <span data-ttu-id="c35f0-116">Se o hardware do usuário fornece mistura de textura múltipla, o app deve aproveitar isso ao executar o mapeamento de luz.</span><span class="sxs-lookup"><span data-stu-id="c35f0-116">If the user's hardware provides for multiple texture blending, your application should take advantage of it when performing light mapping.</span></span> <span data-ttu-id="c35f0-117">Isso melhora significativamente o desempenho do app.</span><span class="sxs-lookup"><span data-stu-id="c35f0-117">This significantly improves your application's performance.</span></span>

<span data-ttu-id="c35f0-118">Com mapas de luz, um app Direct3D pode conseguir uma variedade de efeitos de iluminação ao renderizar primitivos.</span><span class="sxs-lookup"><span data-stu-id="c35f0-118">Using light maps, a Direct3D application can achieve a variety of lighting effects when it renders primitives.</span></span> <span data-ttu-id="c35f0-119">Ele pode mapear não apenas as luzes monocromáticas e coloridas em uma cena, mas também pode adicionar detalhes como realces especulares e iluminação difusa.</span><span class="sxs-lookup"><span data-stu-id="c35f0-119">It can map not only monochrome and colored lights in a scene, but it can also add details such as specular highlights and diffuse lighting.</span></span>

<span data-ttu-id="c35f0-120">As informações sobre o uso da mistura de textura do Direct3D para executar o mapeamento de luz são apresentadas nos tópicos a seguir.</span><span class="sxs-lookup"><span data-stu-id="c35f0-120">Information on using Direct3D texture blending to perform light mapping is presented in the following topics.</span></span>

-   [<span data-ttu-id="c35f0-121">Mapas leves monocromáticos (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="c35f0-121">Monochrome Light Maps (Direct3D 9)</span></span>](monochrome-light-maps.md)
-   [<span data-ttu-id="c35f0-122">Mapas de luz de cor (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="c35f0-122">Color Light Maps (Direct3D 9)</span></span>](color-light-maps.md)
-   [<span data-ttu-id="c35f0-123">Mapas de luz especulares (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="c35f0-123">Specular Light Maps (Direct3D 9)</span></span>](specular-light-maps.md)
-   [<span data-ttu-id="c35f0-124">Mapas de luz difusa (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="c35f0-124">Diffuse Light Maps (Direct3D 9)</span></span>](diffuse-light-maps.md)

## <a name="related-topics"></a><span data-ttu-id="c35f0-125">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c35f0-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c35f0-126">Mesclagem de textura</span><span class="sxs-lookup"><span data-stu-id="c35f0-126">Texture Blending</span></span>](texture-blending.md)
</dt> </dl>

 

 



