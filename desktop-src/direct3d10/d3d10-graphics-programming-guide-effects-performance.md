---
description: Considerações sobre desempenho (Direct3D 10)
ms.assetid: 9f029be5-4ce0-46ca-909b-adaa980398e7
title: Considerações sobre desempenho (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ba2dbe00475efebdb6ff5d772b3eccd6cd4263a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010139"
---
# <a name="performance-considerations-direct3d-10"></a><span data-ttu-id="b3d1b-103">Considerações sobre desempenho (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="b3d1b-103">Performance Considerations (Direct3D 10)</span></span>

## <a name="using-effect-pools"></a><span data-ttu-id="b3d1b-104">Usando pools de efeito</span><span class="sxs-lookup"><span data-stu-id="b3d1b-104">Using Effect Pools</span></span>

<span data-ttu-id="b3d1b-105">É comum que os pipelines de renderização usem muitos sombreadores para renderizar diferentes tipos de objeto e efeitos especiais.</span><span class="sxs-lookup"><span data-stu-id="b3d1b-105">It is common for rendering pipelines to use many shaders to render different object types and special effects.</span></span> <span data-ttu-id="b3d1b-106">O sombreador é uma mistura de Estados que um comum entre todos os sombreadores, como uma matriz mundial ou uma posição clara, e outro estado específico para cada sombreador, como a cor difusa de um objeto ou o cálculo de realce especulativo.</span><span class="sxs-lookup"><span data-stu-id="b3d1b-106">The shader are a mixture of states that a common among all the shaders such as a world matrix or a light position, and other state that is specific to each shader such as an object's diffuse color, or specular highlight calculation.</span></span> <span data-ttu-id="b3d1b-107">Um pool de efeitos é um local na memória para armazenar o estado que é usado em vários sombreadores, bem como objetos de dispositivo comuns, como sombreadores, objetos de estado de renderização e buffers de constantes.</span><span class="sxs-lookup"><span data-stu-id="b3d1b-107">An effect pool is a place in memory to store state that is used across many shaders, as well as common device objects such as shaders, render state objects and constant buffers.</span></span> <span data-ttu-id="b3d1b-108">A melhoria de desempenho resulta da atualização do Estado comum uma vez para todos os sombreadores que precisam desse Estado.</span><span class="sxs-lookup"><span data-stu-id="b3d1b-108">The performance improvement results from updating the common state once for all the shaders that need that state.</span></span>

<span data-ttu-id="b3d1b-109">Um pool de efeitos é um local de memória compartilhada para o estado de efeito.</span><span class="sxs-lookup"><span data-stu-id="b3d1b-109">An effect pool is a shared memory location for effect state.</span></span> <span data-ttu-id="b3d1b-110">Um pool é criado de forma semelhante a um efeito; Ele pode ser criado a partir da memória (ou um arquivo ou um recurso).</span><span class="sxs-lookup"><span data-stu-id="b3d1b-110">A pool is created similarly to an effect; it can be created from memory (or a file or a resource).</span></span> <span data-ttu-id="b3d1b-111">Isso leva a dois tipos diferentes de efeitos: um efeito global que não depende do estado em outro efeito em vez de um efeito filho que depende do estado em outro efeito.</span><span class="sxs-lookup"><span data-stu-id="b3d1b-111">This leads to two different types of effects: a global effect that does not depend on state in other effect versus a child effect which depends on state in another effect.</span></span>

<span data-ttu-id="b3d1b-112">Você especifica se um efeito é um efeito global (o caso padrão) ou um efeito filho (fornecendo o sinalizador de [ \_ \_ \_ \_ efeito filho de compilação de efeito d3d10](d3d10-effect.md) ) quando o efeito é criado.</span><span class="sxs-lookup"><span data-stu-id="b3d1b-112">You specify whether an effect is a global effect (the default case) or a child effect (by supplying the [D3D10\_EFFECT\_COMPILE\_CHILD\_EFFECT](d3d10-effect.md) flag) when the effect is created.</span></span> <span data-ttu-id="b3d1b-113">Um efeito global pode servir como um pool de efeito; um efeito filho não pode ser um pool de efeitos.</span><span class="sxs-lookup"><span data-stu-id="b3d1b-113">A global effect can serve as an effect pool; a child effect cannot be an effect pool.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b3d1b-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b3d1b-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b3d1b-115">Renderizando um efeito</span><span class="sxs-lookup"><span data-stu-id="b3d1b-115">Rendering an Effect</span></span>](d3d10-graphics-programming-guide-effects-render.md)
</dt> <dt>

[<span data-ttu-id="b3d1b-116">Efeitos (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="b3d1b-116">Effects (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-effects.md)
</dt> </dl>

 

 



