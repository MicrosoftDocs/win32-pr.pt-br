---
title: Agendar um storyboard
description: Depois que um storyboard é criado, ele é agendado pelo gerenciador de animação.
ms.assetid: f3c8fe34-8bca-4421-a390-9e0ba9af27b4
keywords:
- storyboards Windows Animação, agendamento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 013adc114fd09f518c34bc15ca2e7799381b6cee3dfeeedaf3b26fcae6d506e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120008166"
---
# <a name="schedule-a-storyboard"></a>Agendar um storyboard

Depois que um storyboard é criado, ele é agendado pelo gerenciador de animação.

## <a name="overview"></a>Visão geral

Por padrão, cada storyboard é iniciado imediatamente quando ele é agendado. Isso significa que, quando um storyboard começa a animar uma ou mais variáveis, ele pode interromper qualquer outro storyboard animando essas mesmas variáveis. No entanto, um aplicativo pode especificar outros comportamentos determinando a prioridade relativa entre storyboards.

Depois que um storyboard tiver sido agendado, ele não poderá mais ser alterado. No entanto, depois que um storyboard tiver sido removido do agendamento, ele poderá ser agendado para reprodução novamente. Os desenvolvedores devem ter cuidado ao re-usar storyboards, pois isso só deve ser feito quando não há nenhuma chance de que o mesmo storyboard precise ser enxuado devido a uma ação do usuário quando ele já estiver em reprodução ou na fila no agendamento.

## <a name="example-code"></a>Código de exemplo

O código de exemplo a seguir é retirado de MainWindow.cpp nos [exemplos](application-driven-animation-sample.md) de animação Windows animação controlada por aplicativo e animação controlada [por temporizador.](timer-driven-animation-sample.md) Ele usa o [**método IUIAnimationStoryboard::Schedule**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-schedule) para agendar o storyboard. Esse método requer a hora atual como um parâmetro.


```
// Get the current time and schedule the storyboard for play

UI_ANIMATION_SECONDS secondsNow;
hr = m_pAnimationTimer->GetTime(
    &secondsNow
    );
if (SUCCEEDED(hr))
{
    hr = pStoryboard->Schedule(
        secondsNow
    );
}
```



## <a name="previous-step"></a>Etapa anterior

Antes de iniciar esta etapa, você deve ter concluído esta etapa: [Criar um storyboard e adicionar transições.](updating---timer-driven-animation.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**IUIAnimationStoryboard::Schedule**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-schedule)
</dt> <dt>

[**IUIAnimationTimer::GetTime**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtimer-gettime)
</dt> <dt>

[Visão geral do storyboard](storyboard-construction.md)
</dt> </dl>

 

 




