---
description: Ao criar cenas 3D, um aplicativo pode, às vezes, obter vantagens de desempenho renderizando objetos 2D de forma que eles pareçam ser objetos 3D. Essa é a ideia básica por trás da técnica de mural.
ms.assetid: 6637a9ce-6731-4f60-8b76-854e86b10bdd
title: Mural (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e287624ef8800f0b66941e826e211d044b7bf27
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105788972"
---
# <a name="billboarding-direct3d-9"></a><span data-ttu-id="c9733-104">Mural (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="c9733-104">Billboarding (Direct3D 9)</span></span>

<span data-ttu-id="c9733-105">Ao criar cenas 3D, um aplicativo pode, às vezes, obter vantagens de desempenho renderizando objetos 2D de forma que eles pareçam ser objetos 3D.</span><span class="sxs-lookup"><span data-stu-id="c9733-105">When creating 3D scenes, an application can sometimes gain performance advantages by rendering 2D objects in a way that makes them appear to be 3D objects.</span></span> <span data-ttu-id="c9733-106">Essa é a ideia básica por trás da técnica de mural.</span><span class="sxs-lookup"><span data-stu-id="c9733-106">This is the basic idea behind the technique of billboarding.</span></span>

<span data-ttu-id="c9733-107">Um mural no sentido normal da palavra é um sinal ao longo de um Roadway.</span><span class="sxs-lookup"><span data-stu-id="c9733-107">A billboard in the normal sense of the word is a sign along a roadway.</span></span> <span data-ttu-id="c9733-108">Os aplicativos Microsoft Direct3D podem criar e renderizar esse tipo de mensagem definindo um sólido retangular e aplicando uma textura a ele.</span><span class="sxs-lookup"><span data-stu-id="c9733-108">Microsoft Direct3D applications can create and render this type of billboard by defining a rectangular solid and applying a texture to it.</span></span> <span data-ttu-id="c9733-109">A mensagem de erro no aspecto mais especializado de gráficos 3D é uma extensão disso.</span><span class="sxs-lookup"><span data-stu-id="c9733-109">Billboarding in the more specialized sense of 3D graphics is an extension of this.</span></span> <span data-ttu-id="c9733-110">O objetivo é fazer com que objetos 2D pareçam ser 3D.</span><span class="sxs-lookup"><span data-stu-id="c9733-110">The goal is to make 2D objects appear to be 3D.</span></span> <span data-ttu-id="c9733-111">A técnica é aplicar uma textura que contenha a imagem do objeto a um primitivo retangular.</span><span class="sxs-lookup"><span data-stu-id="c9733-111">The technique is to apply a texture that contains the object's image to a rectangular primitive.</span></span> <span data-ttu-id="c9733-112">O primitivo é girado para que ele sempre gire o usuário.</span><span class="sxs-lookup"><span data-stu-id="c9733-112">The primitive is rotated so that it always faces the user.</span></span> <span data-ttu-id="c9733-113">Não importa se a imagem do objeto não é retangular.</span><span class="sxs-lookup"><span data-stu-id="c9733-113">It doesn't matter if the object's image is not rectangular.</span></span> <span data-ttu-id="c9733-114">Partes do mural podem se tornar transparentes, portanto, as partes da imagem do mural que você não deseja ver não são visíveis.</span><span class="sxs-lookup"><span data-stu-id="c9733-114">Portions of the billboard can be made transparent, so the parts of the billboard image that you don't want seen are not visible.</span></span>

<span data-ttu-id="c9733-115">Muitos jogos empregam a mensagem para sprites animados.</span><span class="sxs-lookup"><span data-stu-id="c9733-115">Many games employ billboarding for animated sprites.</span></span> <span data-ttu-id="c9733-116">Por exemplo, quando o usuário está passando por um labirinto 3D, ele pode ver armas ou recompensas que podem ser coletadas.</span><span class="sxs-lookup"><span data-stu-id="c9733-116">For instance, when the user is moving through a 3D maze, he or she may see weapons or rewards that can be picked up.</span></span> <span data-ttu-id="c9733-117">Normalmente, elas são imagens 2D texturizadas em um primitivo retangular.</span><span class="sxs-lookup"><span data-stu-id="c9733-117">These are typically 2D images textured on a rectangular primitive.</span></span> <span data-ttu-id="c9733-118">A mensagem é geralmente usada em jogos para renderizar imagens de árvores, bushes e nuvens.</span><span class="sxs-lookup"><span data-stu-id="c9733-118">Billboarding is often used in games to render images of trees, bushes, and clouds.</span></span>

<span data-ttu-id="c9733-119">Quando uma imagem é aplicada a um mural, o primitivo retangular deve primeiro ser girado para que a imagem resultante gire o usuário.</span><span class="sxs-lookup"><span data-stu-id="c9733-119">When an image is applied to a billboard, the rectangular primitive must first be rotated so that the resulting image faces the user.</span></span> <span data-ttu-id="c9733-120">Seu aplicativo deve então convertê-lo em posição.</span><span class="sxs-lookup"><span data-stu-id="c9733-120">Your application must then translate it into position.</span></span> <span data-ttu-id="c9733-121">Em seguida, o aplicativo pode aplicar uma textura à primitiva.</span><span class="sxs-lookup"><span data-stu-id="c9733-121">The application can then apply a texture to the primitive.</span></span>

<span data-ttu-id="c9733-122">O mural funciona melhor para objetos simétricos, especialmente objetos que são simétricos ao longo do eixo vertical.</span><span class="sxs-lookup"><span data-stu-id="c9733-122">Billboarding works best for symmetrical objects, especially objects that are symmetrical along the vertical axis.</span></span> <span data-ttu-id="c9733-123">Ele também exige que a altitude do ponto de vista não aumente muito.</span><span class="sxs-lookup"><span data-stu-id="c9733-123">It also requires that the altitude of the viewpoint doesn't increase too much.</span></span> <span data-ttu-id="c9733-124">Se o usuário tiver permissão para exibir o exibido a partir de acima, será imediatamente aparente que o objeto é 2D em vez de 3D.</span><span class="sxs-lookup"><span data-stu-id="c9733-124">If the user is allowed to view the billboarded from above, it becomes readily apparent that the object is 2D rather than 3D.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c9733-125">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c9733-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c9733-126">Exemplos alfa</span><span class="sxs-lookup"><span data-stu-id="c9733-126">Alpha Examples</span></span>](alpha-examples.md)
</dt> </dl>

 

 



