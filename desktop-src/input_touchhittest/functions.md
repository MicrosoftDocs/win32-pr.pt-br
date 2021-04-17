---
title: Funções (teste de clique de toque)
description: Os tópicos nesta seção fornecem as especificações de referência para as funções de teste de toque.
ms.assetid: C7275A12-4F76-485D-896F-3CCB8CE92F8E
keywords:
- interação do usuário
- input
- ponteiro
- touch
ms.topic: article
ms.date: 02/07/2020
ms.openlocfilehash: 03fcb4fb3fbe4f56e288703316f4b6e3ff02bba4
ms.sourcegitcommit: 4570ac533e129ff88b23f2c2b69e0140ead3a4a4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/26/2021
ms.locfileid: "105794633"
---
# <a name="touch-hit-testing-functions"></a><span data-ttu-id="7ebc6-107">Funções de teste de colisão de toque</span><span class="sxs-lookup"><span data-stu-id="7ebc6-107">Touch Hit Testing functions</span></span>

<span data-ttu-id="7ebc6-108">Os tópicos nesta seção fornecem as especificações de referência para as [funções de teste de toque](functions.md).</span><span class="sxs-lookup"><span data-stu-id="7ebc6-108">The topics in this section provide the reference specifications for [Touch Hit Testing functions](functions.md).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="7ebc6-109">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="7ebc6-109">In this section</span></span>

| <span data-ttu-id="7ebc6-110">Tópico</span><span class="sxs-lookup"><span data-stu-id="7ebc6-110">Topic</span></span> | <span data-ttu-id="7ebc6-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="7ebc6-111">Description</span></span> |
| --- | --- |
| [<span data-ttu-id="7ebc6-112">**EvaluateProximityToPolygon**</span><span class="sxs-lookup"><span data-stu-id="7ebc6-112">**EvaluateProximityToPolygon**</span></span>](/windows/win32/api/winuser/nf-winuser-evaluateproximitytopolygon)<br/> | <span data-ttu-id="7ebc6-113">Retorna a pontuação de um polígono como o destino de toque provável (comparado a todos os outros polígonos que interseccionam a área de contato de toque) e um ponto de toque ajustado no polígono.</span><span class="sxs-lookup"><span data-stu-id="7ebc6-113">Returns the score of a polygon as the probable touch target (compared to all other polygons that intersect the touch contact area) and an adjusted touch point within the polygon.</span></span> <br/> |
| [<span data-ttu-id="7ebc6-114">**EvaluateProximityToRect**</span><span class="sxs-lookup"><span data-stu-id="7ebc6-114">**EvaluateProximityToRect**</span></span>](/windows/win32/api/winuser/nf-winuser-evaluateproximitytorect)<br/> | <span data-ttu-id="7ebc6-115">Retorna a pontuação de um retângulo como o destino de toque provável, em comparação com todos os outros retângulos que interseccionam a área de contato de toque e um ponto de toque ajustado dentro do retângulo.</span><span class="sxs-lookup"><span data-stu-id="7ebc6-115">Returns the score of a rectangle as the probable touch target, compared to all other rectangles that intersect the touch contact area, and an adjusted touch point within the rectangle.</span></span> <br/> |
| [<span data-ttu-id="7ebc6-116">**PackTouchHitTestingProximityEvaluation**</span><span class="sxs-lookup"><span data-stu-id="7ebc6-116">**PackTouchHitTestingProximityEvaluation**</span></span>](/windows/win32/api/winuser/nf-winuser-packtouchhittestingproximityevaluation)<br/> | <span data-ttu-id="7ebc6-117">Retorna a pontuação de avaliação de proximidade e as coordenadas de ponto de toque ajustadas como um valor embalado para o retorno de chamada de [WM_TOUCHHITTESTING mensagem](../inputmsg/wm-touchhittesting.md) .</span><span class="sxs-lookup"><span data-stu-id="7ebc6-117">Returns the proximity evaluation score and the adjusted touch-point coordinates as a packed value for the [WM_TOUCHHITTESTING message](../inputmsg/wm-touchhittesting.md) callback.</span></span> <br/> |
| [<span data-ttu-id="7ebc6-118">**RegisterTouchHitTestingWindow**</span><span class="sxs-lookup"><span data-stu-id="7ebc6-118">**RegisterTouchHitTestingWindow**</span></span>](/windows/win32/api/winuser/nf-winuser-registertouchhittestingwindow)<br/> | <span data-ttu-id="7ebc6-119">Registra uma janela para processar a notificação de [WM_TOUCHHITTESTING](../inputmsg/wm-touchhittesting.md)</span><span class="sxs-lookup"><span data-stu-id="7ebc6-119">Registers a window to process the [WM_TOUCHHITTESTING](../inputmsg/wm-touchhittesting.md) notification</span></span><br/> |

## <a name="related-topics"></a><span data-ttu-id="7ebc6-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7ebc6-120">Related topics</span></span>

[<span data-ttu-id="7ebc6-121">Referência de teste de colisão de toque</span><span class="sxs-lookup"><span data-stu-id="7ebc6-121">Touch Hit Testing Reference</span></span>](touchhittest-reference.md)
