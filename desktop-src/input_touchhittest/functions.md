---
title: Funções (Teste de Toque/ Toque)
description: Os tópicos nesta seção fornecem as especificações de referência para funções de Teste de Toque.
ms.assetid: C7275A12-4F76-485D-896F-3CCB8CE92F8E
keywords:
- interação do usuário
- input
- ponteiro
- touch
ms.topic: article
ms.date: 02/07/2020
ms.openlocfilehash: 83ab93fbff031423b6478926e499077ac78b1aec686d596ca069fda6d1b2298b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118248353"
---
# <a name="touch-hit-testing-functions"></a>Funções de teste de toque

Os tópicos nesta seção fornecem as especificações de referência para as [funções de Teste de Toque.](functions.md)

## <a name="in-this-section"></a>Nesta seção

| Tópico | Descrição |
| --- | --- |
| [**EvaluateProximityToPolygon**](/windows/win32/api/winuser/nf-winuser-evaluateproximitytopolygon)<br/> | Retorna a pontuação de um polígono como o destino de toque provável (em comparação com todos os outros polígonos que intersecção da área de contato de toque) e um ponto de toque ajustado dentro do polígono. <br/> |
| [**EvaluateProximityToRect**](/windows/win32/api/winuser/nf-winuser-evaluateproximitytorect)<br/> | Retorna a pontuação de um retângulo como o destino de toque provável, em comparação com todos os outros retângulos que cruzam a área de contato de toque e um ponto de toque ajustado dentro do retângulo. <br/> |
| [**PackTouchHitTestingProximityEvaluation**](/windows/win32/api/winuser/nf-winuser-packtouchhittestingproximityevaluation)<br/> | Retorna a pontuação de avaliação de proximidade e as coordenadas de ponto de toque ajustadas como um valor empacotado para o retorno de chamada WM_TOUCHHITTESTING [mensagem.](../inputmsg/wm-touchhittesting.md) <br/> |
| [**RegisterTouchHitTestingWindow**](/windows/win32/api/winuser/nf-winuser-registertouchhittestingwindow)<br/> | Registra uma janela para processar a [notificação WM_TOUCHHITTESTING](../inputmsg/wm-touchhittesting.md) dados<br/> |

## <a name="related-topics"></a>Tópicos relacionados

[Referência de teste de toque de toque](touchhittest-reference.md)
