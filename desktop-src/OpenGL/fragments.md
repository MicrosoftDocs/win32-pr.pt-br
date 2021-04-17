---
title: Fragmentos
description: Fragmentos
ms.assetid: bc400251-32c4-4477-ba0c-a0046fe85327
keywords:
- OpenGL, fragmentos
- Pipeline de processamento de OpenGL, fragmentos
- fragmentos OpenGL
- framebuffers, fragmentos modificando pixels
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00e2b4c2dc36e24c4fd9baa82b28fa4d336f69b5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105757003"
---
# <a name="fragments"></a><span data-ttu-id="5eae0-107">Fragmentos</span><span class="sxs-lookup"><span data-stu-id="5eae0-107">Fragments</span></span>

<span data-ttu-id="5eae0-108">Um fragmento produzido pela rasterização modifica o pixel correspondente no framebuffer somente se ele passar os seguintes testes:</span><span class="sxs-lookup"><span data-stu-id="5eae0-108">A fragment produced by rasterization modifies the corresponding pixel in the framebuffer only if it passes the following tests:</span></span>

-   [<span data-ttu-id="5eae0-109">Teste de propriedade de pixel</span><span class="sxs-lookup"><span data-stu-id="5eae0-109">Pixel ownership test</span></span>](pixel-ownership-test.md)
-   [<span data-ttu-id="5eae0-110">Teste de tesoura</span><span class="sxs-lookup"><span data-stu-id="5eae0-110">Scissor test</span></span>](scissor-test.md)
-   [<span data-ttu-id="5eae0-111">Teste alfa</span><span class="sxs-lookup"><span data-stu-id="5eae0-111">Alpha test</span></span>](alpha-test.md)
-   [<span data-ttu-id="5eae0-112">Teste de estêncil</span><span class="sxs-lookup"><span data-stu-id="5eae0-112">Stencil test</span></span>](stencil-test.md)
-   [<span data-ttu-id="5eae0-113">Teste de buffer de profundidade</span><span class="sxs-lookup"><span data-stu-id="5eae0-113">Depth-buffer test</span></span>](depth-buffer-test.md)

<span data-ttu-id="5eae0-114">Se ele passar, os dados do fragmento poderão substituir os valores de framebuffer existentes, ou você poderá combiná-los com os dados existentes no framebuffer, dependendo do estado de determinados modos.</span><span class="sxs-lookup"><span data-stu-id="5eae0-114">If it passes, the fragment's data can replace the existing framebuffer values, or you can combine it with existing data in the framebuffer, depending on the state of certain modes.</span></span> <span data-ttu-id="5eae0-115">Você pode combinar o fragmento com dados no framebuffer por:</span><span class="sxs-lookup"><span data-stu-id="5eae0-115">You can combine the fragment with data in the framebuffer by:</span></span>

-   [<span data-ttu-id="5eae0-116">Mesclagem</span><span class="sxs-lookup"><span data-stu-id="5eae0-116">Blending</span></span>](blending.md)
-   [<span data-ttu-id="5eae0-117">Pontilhado</span><span class="sxs-lookup"><span data-stu-id="5eae0-117">Dithering</span></span>](dithering.md)
-   [<span data-ttu-id="5eae0-118">Operações lógicas</span><span class="sxs-lookup"><span data-stu-id="5eae0-118">Logical operations</span></span>](logical-operations.md)

 

 




