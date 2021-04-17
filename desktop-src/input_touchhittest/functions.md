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
# <a name="touch-hit-testing-functions"></a>Funções de teste de colisão de toque

Os tópicos nesta seção fornecem as especificações de referência para as [funções de teste de toque](functions.md).

## <a name="in-this-section"></a>Nesta seção

| Tópico | Descrição |
| --- | --- |
| [**EvaluateProximityToPolygon**](/windows/win32/api/winuser/nf-winuser-evaluateproximitytopolygon)<br/> | Retorna a pontuação de um polígono como o destino de toque provável (comparado a todos os outros polígonos que interseccionam a área de contato de toque) e um ponto de toque ajustado no polígono. <br/> |
| [**EvaluateProximityToRect**](/windows/win32/api/winuser/nf-winuser-evaluateproximitytorect)<br/> | Retorna a pontuação de um retângulo como o destino de toque provável, em comparação com todos os outros retângulos que interseccionam a área de contato de toque e um ponto de toque ajustado dentro do retângulo. <br/> |
| [**PackTouchHitTestingProximityEvaluation**](/windows/win32/api/winuser/nf-winuser-packtouchhittestingproximityevaluation)<br/> | Retorna a pontuação de avaliação de proximidade e as coordenadas de ponto de toque ajustadas como um valor embalado para o retorno de chamada de [WM_TOUCHHITTESTING mensagem](../inputmsg/wm-touchhittesting.md) . <br/> |
| [**RegisterTouchHitTestingWindow**](/windows/win32/api/winuser/nf-winuser-registertouchhittestingwindow)<br/> | Registra uma janela para processar a notificação de [WM_TOUCHHITTESTING](../inputmsg/wm-touchhittesting.md)<br/> |

## <a name="related-topics"></a>Tópicos relacionados

[Referência de teste de colisão de toque](touchhittest-reference.md)
