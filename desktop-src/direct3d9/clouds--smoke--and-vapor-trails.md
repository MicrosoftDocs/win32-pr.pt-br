---
description: As nuvens, a fumaça e as trilhas de vapor podem ser criadas por uma extensão da técnica de mensagem.
ms.assetid: c5607327-de46-4241-a01a-4adfe0bbf6fb
title: Nuvens, fumaça e trilhas Vapors (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f60bce89e23b2b2aab7affbb6947cab4d11c33ed
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104569697"
---
# <a name="clouds-smoke-and-vapor-trails-direct3d-9"></a><span data-ttu-id="f7643-103">Nuvens, fumaça e trilhas Vapors (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="f7643-103">Clouds, Smoke, and Vapor Trails (Direct3D 9)</span></span>

<span data-ttu-id="f7643-104">As nuvens, a fumaça e as trilhas de vapor podem ser criadas por uma extensão da técnica de mensagem.</span><span class="sxs-lookup"><span data-stu-id="f7643-104">Clouds, smoke, and vapor trails can all be created by an extension of the billboarding technique.</span></span> <span data-ttu-id="f7643-105">Consulte a [mensagem (Direct3D 9)](billboarding.md).</span><span class="sxs-lookup"><span data-stu-id="f7643-105">See [Billboarding (Direct3D 9)](billboarding.md).</span></span> <span data-ttu-id="f7643-106">Ao girar o mural em dois eixos em vez de um, seu aplicativo pode permitir que o usuário exiba uma mensagem de qualquer ângulo.</span><span class="sxs-lookup"><span data-stu-id="f7643-106">By rotating the billboard on two axes instead of one, your application can enable the user to view a billboard from any angle.</span></span> <span data-ttu-id="f7643-107">Normalmente, um aplicativo gira o mural nos eixos horizontal e vertical.</span><span class="sxs-lookup"><span data-stu-id="f7643-107">Typically, an application rotates the billboard on the horizontal and vertical axes.</span></span>

<span data-ttu-id="f7643-108">Para fazer uma nuvem simples, seu aplicativo pode girar um primitivo retangular em um ou dois eixos para que o primitivo gire o usuário.</span><span class="sxs-lookup"><span data-stu-id="f7643-108">To make a simple cloud, your application can rotate a rectangular primitive on one or two axes so that the primitive faces the user.</span></span> <span data-ttu-id="f7643-109">Uma textura semelhante à de nuvem pode ser aplicada ao primitivo com transparência.</span><span class="sxs-lookup"><span data-stu-id="f7643-109">A cloud-like texture can then be applied to the primitive with transparency.</span></span> <span data-ttu-id="f7643-110">Para obter detalhes sobre como aplicar texturas transparentes a primitivos, consulte [mesclagem de textura (Direct3D 9)](texture-blending.md).</span><span class="sxs-lookup"><span data-stu-id="f7643-110">For details on applying transparent textures to primitives, see [Texture Blending (Direct3D 9)](texture-blending.md).</span></span> <span data-ttu-id="f7643-111">Você pode animar a nuvem aplicando uma série de texturas ao longo do tempo.</span><span class="sxs-lookup"><span data-stu-id="f7643-111">You can animate the cloud by applying a series of textures over time.</span></span>

<span data-ttu-id="f7643-112">Um aplicativo pode criar nuvens mais complexas formando-as a partir de um grupo de primitivos.</span><span class="sxs-lookup"><span data-stu-id="f7643-112">An application can create more complex clouds by forming them from a group of primitives.</span></span> <span data-ttu-id="f7643-113">Cada parte da nuvem é um primitivo retangular.</span><span class="sxs-lookup"><span data-stu-id="f7643-113">Each part of the cloud is a rectangular primitive.</span></span> <span data-ttu-id="f7643-114">Os primitivos podem ser movidos independentemente ao longo do tempo para dar a aparência de uma névoa dinâmica.</span><span class="sxs-lookup"><span data-stu-id="f7643-114">The primitives can be moved independently over time to give the appearance of a dynamic mist.</span></span> <span data-ttu-id="f7643-115">A ilustração a seguir mostra esse conceito.</span><span class="sxs-lookup"><span data-stu-id="f7643-115">The following illustration shows this concept.</span></span>

![ilustração de primitivos que formam nuvens mais complexas](images/cloud.png)

<span data-ttu-id="f7643-117">A aparência da fumaça é exibida de maneira semelhante às nuvens.</span><span class="sxs-lookup"><span data-stu-id="f7643-117">The appearance of smoke is displayed in a manner similar to clouds.</span></span> <span data-ttu-id="f7643-118">Normalmente, ele requer vários murals, como nuvens complexas.</span><span class="sxs-lookup"><span data-stu-id="f7643-118">It typically requires multiple billboards, like complex clouds.</span></span> <span data-ttu-id="f7643-119">A fumaça geralmente billows e aumenta com o tempo, portanto, os murals que compõem a fumaça Plume precisam se mover de acordo.</span><span class="sxs-lookup"><span data-stu-id="f7643-119">Smoke usually billows and rises over time, so the billboards that make up the smoke plume need to move accordingly.</span></span> <span data-ttu-id="f7643-120">Talvez seja necessário adicionar mais murals à medida que o Plume aumentar e dispersar.</span><span class="sxs-lookup"><span data-stu-id="f7643-120">You may need to add more billboards as the plume rises and disperses.</span></span>

<span data-ttu-id="f7643-121">Uma trilha de vapor é uma plume de fumaça que não aumenta.</span><span class="sxs-lookup"><span data-stu-id="f7643-121">A vapor trail is a smoke plume that doesn't rise.</span></span> <span data-ttu-id="f7643-122">No entanto, como uma plume de fumaça, ela se espalha ao longo do tempo.</span><span class="sxs-lookup"><span data-stu-id="f7643-122">However, like a smoke plume, it disperses over time.</span></span> <span data-ttu-id="f7643-123">A ilustração a seguir mostra a técnica de usar os murals para simular uma trilha de vapor.</span><span class="sxs-lookup"><span data-stu-id="f7643-123">The following illustration shows the technique of using billboards to simulate a vapor trail.</span></span>

![ilustração de murals que simulam uma trilha vapor](images/vapor.png)

## <a name="related-topics"></a><span data-ttu-id="f7643-125">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f7643-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f7643-126">Exemplos alfa</span><span class="sxs-lookup"><span data-stu-id="f7643-126">Alpha Examples</span></span>](alpha-examples.md)
</dt> </dl>

 

 



