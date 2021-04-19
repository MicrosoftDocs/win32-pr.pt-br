---
description: Adicionar a neblina a uma cena 3D pode aprimorar o realm, fornecer ambiance ou definir um humor, e os artefatos obscuros às vezes são causados quando a geometria distante chega à exibição.
ms.assetid: 42045e96-43aa-4cec-82b5-0b46a7d5097b
title: Neblina (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44b9ed234bef0f3dea76baa98390f25e9b2003a6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105771319"
---
# <a name="fog-direct3d-9"></a><span data-ttu-id="7b019-103">Neblina (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="7b019-103">Fog (Direct3D 9)</span></span>

<span data-ttu-id="7b019-104">Adicionar a neblina a uma cena 3D pode aprimorar o realm, fornecer ambiance ou definir um humor, e os artefatos obscuros às vezes são causados quando a geometria distante chega à exibição.</span><span class="sxs-lookup"><span data-stu-id="7b019-104">Adding fog to a 3D scene can enhance realism, provide ambiance or set a mood, and obscure artifacts sometimes caused when distant geometry comes into view.</span></span> <span data-ttu-id="7b019-105">O Direct3D dá suporte a dois modelos de neblina, sombra de pixel e neblina de vértice, cada um com seus próprios recursos e interface de programação.</span><span class="sxs-lookup"><span data-stu-id="7b019-105">Direct3D supports two fog models, pixel fog and vertex fog, each with its own features and programming interface.</span></span>

<span data-ttu-id="7b019-106">Essencialmente, a neblina é implementada combinando a cor dos objetos em uma cena com uma cor de neblina escolhida com base na profundidade de um objeto em uma cena ou em sua distância do ponto de vista.</span><span class="sxs-lookup"><span data-stu-id="7b019-106">Essentially, fog is implemented by blending the color of objects in a scene with a chosen fog color based on the depth of an object in a scene or its distance from the viewpoint.</span></span> <span data-ttu-id="7b019-107">À medida que os objetos crescem mais distantes, sua cor original se mistura cada vez mais com a cor de neblina escolhida, criando a ilusão de que o objeto está sendo mais obscuro por pequenas partículas flutuantes na cena.</span><span class="sxs-lookup"><span data-stu-id="7b019-107">As objects grow more distant, their original color blends more and more with the chosen fog color, creating the illusion that the object is being increasingly obscured by tiny particles floating in the scene.</span></span> <span data-ttu-id="7b019-108">A ilustração a seguir mostra uma cena renderizada sem neblina e uma cena semelhante renderizada com a neblina habilitada.</span><span class="sxs-lookup"><span data-stu-id="7b019-108">The following illustration shows a scene rendered without fog, and a similar scene rendered with fog enabled.</span></span>

![ilustração da mesma cena com e sem sombra](images/fogcomp.png)

<span data-ttu-id="7b019-110">Nesta ilustração, a cena à esquerda tem um horizonte claro, além do qual nenhum cenário está visível, embora fique visível no mundo real.</span><span class="sxs-lookup"><span data-stu-id="7b019-110">In this illustration, the scene on the left has a clear horizon, beyond which no scenery is visible, even though it would be visible in the real world.</span></span> <span data-ttu-id="7b019-111">A cena à direita obscurece o horizonte usando uma cor de neblina idêntica à cor do plano de fundo, fazendo com que os polígonos pareçam desaparecer na distância.</span><span class="sxs-lookup"><span data-stu-id="7b019-111">The scene on the right obscures the horizon by using a fog color identical to the background color, making polygons appear to fade into the distance.</span></span> <span data-ttu-id="7b019-112">Ao combinar efeitos discretos de neblina com o design de cena criativa, você pode adicionar humor e suavizar a cor dos objetos em uma cena.</span><span class="sxs-lookup"><span data-stu-id="7b019-112">By combining discrete fog effects with creative scene design you can add mood and soften the color of objects in a scene.</span></span>

<span data-ttu-id="7b019-113">O Direct3D fornece duas maneiras de adicionar a neblina a uma cena: sombra de pixel e neblina de vértice, chamados de como os efeitos de neblina são aplicados.</span><span class="sxs-lookup"><span data-stu-id="7b019-113">Direct3D provides two ways to add fog to a scene: pixel fog and vertex fog, named for how the fog effects are applied.</span></span> <span data-ttu-id="7b019-114">Para obter detalhes, consulte [sombra de pixel (Direct3D 9)](pixel-fog.md) e [neblina de vértice (Direct3D 9)](vertex-fog.md).</span><span class="sxs-lookup"><span data-stu-id="7b019-114">For details, see [Pixel Fog (Direct3D 9)](pixel-fog.md) and [Vertex Fog (Direct3D 9)](vertex-fog.md).</span></span> <span data-ttu-id="7b019-115">Em suma, a neblina de pixel – também chamada de sombra de tabela – é implementada no driver de dispositivo e a neblina de vértice é implementada no mecanismo de iluminação Direct3D.</span><span class="sxs-lookup"><span data-stu-id="7b019-115">In short, pixel fog - also called table fog - is implemented in the device driver and vertex fog is implemented in the Direct3D lighting engine.</span></span> <span data-ttu-id="7b019-116">Um aplicativo pode implementar a neblina com um sombreador de vértice e sombra de pixel simultaneamente, se desejado.</span><span class="sxs-lookup"><span data-stu-id="7b019-116">An application can implement fog with a vertex shader, and pixel fog simultaneously if desired.</span></span>

> [!Note]  
> <span data-ttu-id="7b019-117">Independentemente de você usar sombra de pixel ou vértice, seu aplicativo deve fornecer uma matriz de projeção compatível para garantir que os efeitos de neblina sejam aplicados corretamente.</span><span class="sxs-lookup"><span data-stu-id="7b019-117">Regardless of whether you use pixel or vertex fog, your application must provide a compliant projection matrix to ensure that fog effects are properly applied.</span></span> <span data-ttu-id="7b019-118">Essa restrição se aplica até mesmo a aplicativos que não usam o mecanismo de transformação e iluminação do Direct3D.</span><span class="sxs-lookup"><span data-stu-id="7b019-118">This restriction applies even to applications that do not use the Direct3D transformation and lighting engine.</span></span> <span data-ttu-id="7b019-119">Para obter detalhes adicionais sobre como você pode fornecer uma matriz apropriada, consulte [projetion Transform (Direct3D 9)](projection-transform.md).</span><span class="sxs-lookup"><span data-stu-id="7b019-119">For additional details about how you can provide an appropriate matrix, see [Projection Transform (Direct3D 9)](projection-transform.md).</span></span>

 

<span data-ttu-id="7b019-120">Os tópicos a seguir apresentam a neblina e apresentam informações sobre como usar vários recursos de neblina em aplicativos Direct3D.</span><span class="sxs-lookup"><span data-stu-id="7b019-120">The following topics introduce fog and present information about using various fog features in Direct3D applications.</span></span>

-   [<span data-ttu-id="7b019-121">Fórmulas de neblina (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="7b019-121">Fog Formulas (Direct3D 9)</span></span>](fog-formulas.md)
-   [<span data-ttu-id="7b019-122">Parâmetros de neblina (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="7b019-122">Fog Parameters (Direct3D 9)</span></span>](fog-parameters.md)
-   [<span data-ttu-id="7b019-123">Fusão de neblina (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="7b019-123">Fog Blending (Direct3D 9)</span></span>](fog-blending.md)
-   [<span data-ttu-id="7b019-124">Cor da neblina (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="7b019-124">Fog Color (Direct3D 9)</span></span>](fog-color.md)
-   [<span data-ttu-id="7b019-125">Neblina de vértice (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="7b019-125">Vertex Fog (Direct3D 9)</span></span>](vertex-fog.md)
-   [<span data-ttu-id="7b019-126">Sombra de pixel (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="7b019-126">Pixel Fog (Direct3D 9)</span></span>](pixel-fog.md)

<span data-ttu-id="7b019-127">A fusão de neblina é controlada por Estados de renderização; Ele não faz parte do pipeline de pixel programável.</span><span class="sxs-lookup"><span data-stu-id="7b019-127">Fog blending is controlled by render states; it is not part of the programmable pixel pipeline.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7b019-128">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7b019-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7b019-129">Renderização de Direct3D</span><span class="sxs-lookup"><span data-stu-id="7b019-129">Direct3D Rendering</span></span>](direct3d-rendering.md)
</dt> </dl>

 

 



