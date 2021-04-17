---
title: Problemas especiais de portabilidade do íris GL
description: Problemas especiais de portabilidade do íris GL
ms.assetid: dcf7967a-2867-4443-a1c8-8335c6fe016a
keywords:
- OpenGL no Windows, portabilidade do íris GL
- portando para OpenGL, íris GL
- Portabilidade OpenGL, íris GL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1273a873f3a39a5d237f9a5845a72f87156e001c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105769302"
---
# <a name="special-iris-gl-porting-issues"></a><span data-ttu-id="ba3e0-106">Problemas especiais de portabilidade do íris GL</span><span class="sxs-lookup"><span data-stu-id="ba3e0-106">Special IRIS GL Porting Issues</span></span>

<span data-ttu-id="ba3e0-107">Os tópicos a seguir descrevem técnicas para portar partes específicas do seu código de íris GL para o código OpenGL.</span><span class="sxs-lookup"><span data-stu-id="ba3e0-107">The following topics describe techniques for porting specific parts of your IRIS GL code to OpenGL code.</span></span>

-   [<span data-ttu-id="ba3e0-108">Portando greset</span><span class="sxs-lookup"><span data-stu-id="ba3e0-108">Porting greset</span></span>](porting-greset.md)
-   [<span data-ttu-id="ba3e0-109">Funções de "Get" de íris do enporting</span><span class="sxs-lookup"><span data-stu-id="ba3e0-109">Porting IRIS GL "Get" Functions</span></span>](porting-iris-gl-get-functions.md)
-   [<span data-ttu-id="ba3e0-110">Portando código que requer uma posição de gráficos atual</span><span class="sxs-lookup"><span data-stu-id="ba3e0-110">Porting Code that Requires a Current Graphics Position</span></span>](porting-code-that-requires-a-current-graphics-position.md)
-   [<span data-ttu-id="ba3e0-111">Portando funções de desenho</span><span class="sxs-lookup"><span data-stu-id="ba3e0-111">Porting Drawing Functions</span></span>](porting-drawing-functions.md)
-   [<span data-ttu-id="ba3e0-112">Transportando a cor, o sombreamento e o código Writemask</span><span class="sxs-lookup"><span data-stu-id="ba3e0-112">Porting Color, Shading, and Writemask Code</span></span>](porting-color--shading--and-writemask-code.md)
-   [<span data-ttu-id="ba3e0-113">Portando operações de pixel</span><span class="sxs-lookup"><span data-stu-id="ba3e0-113">Porting Pixel Operations</span></span>](porting-pixel-operations.md)
-   [<span data-ttu-id="ba3e0-114">Advertência de profundidade de portabilidade e comandos de neblina</span><span class="sxs-lookup"><span data-stu-id="ba3e0-114">Porting Depth Cueing and Fog Commands</span></span>](porting-depth-cueing-and-fog-commands.md)
-   [<span data-ttu-id="ba3e0-115">Funções de curva e superfície de portabilidade</span><span class="sxs-lookup"><span data-stu-id="ba3e0-115">Porting Curve and Surface Functions</span></span>](porting-curve-and-surface-functions.md)
-   [<span data-ttu-id="ba3e0-116">Portando funções de anti-aliasing</span><span class="sxs-lookup"><span data-stu-id="ba3e0-116">Porting Antialiasing Functions</span></span>](porting-antialiasing-functions.md)
-   [<span data-ttu-id="ba3e0-117">Portando chamadas de buffer de acumulação</span><span class="sxs-lookup"><span data-stu-id="ba3e0-117">Porting Accumulation Buffer Calls</span></span>](porting-accumulation-buffer-calls.md)
-   [<span data-ttu-id="ba3e0-118">Portando chamadas de plano de estêncil</span><span class="sxs-lookup"><span data-stu-id="ba3e0-118">Porting Stencil Plane Calls</span></span>](porting-stencil-plane-calls.md)
-   [<span data-ttu-id="ba3e0-119">Portando listas de exibição</span><span class="sxs-lookup"><span data-stu-id="ba3e0-119">Porting Display Lists</span></span>](porting-display-lists.md)
-   [<span data-ttu-id="ba3e0-120">Portando defs, associações e conjuntos</span><span class="sxs-lookup"><span data-stu-id="ba3e0-120">Porting Defs, Binds, and Sets</span></span>](porting-defs--binds--and-sets.md)
-   [<span data-ttu-id="ba3e0-121">Portando funções de iluminação e materiais</span><span class="sxs-lookup"><span data-stu-id="ba3e0-121">Porting Lighting and Materials Functions</span></span>](porting-lighting-and-materials-functions.md)
-   [<span data-ttu-id="ba3e0-122">Portando funções de textura</span><span class="sxs-lookup"><span data-stu-id="ba3e0-122">Porting Texture Functions</span></span>](porting-texture-functions.md)
-   [<span data-ttu-id="ba3e0-123">Portando funções de separação</span><span class="sxs-lookup"><span data-stu-id="ba3e0-123">Porting Picking Functions</span></span>](porting-picking-functions.md)
-   [<span data-ttu-id="ba3e0-124">Portando funções de comentários</span><span class="sxs-lookup"><span data-stu-id="ba3e0-124">Porting Feedback Functions</span></span>](porting-feedback-functions.md)

 

 




