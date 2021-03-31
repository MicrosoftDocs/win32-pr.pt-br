---
title: Agendar um storyboard
description: Depois que um Storyboard é criado, ele é agendado pelo Gerenciador de animação.
ms.assetid: f3c8fe34-8bca-4421-a390-9e0ba9af27b4
keywords:
- Animação de storyboards do Windows, agendamento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3feae253804d20711c9bbd8ed50895f43272a3f4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104004959"
---
# <a name="schedule-a-storyboard"></a>Agendar um storyboard

Depois que um Storyboard é criado, ele é agendado pelo Gerenciador de animação.

## <a name="overview"></a>Visão geral

Por padrão, cada Storyboard começa imediatamente quando está agendado. Isso significa que, quando um storyboard começa a animar uma ou mais variáveis, ele pode interromper qualquer outro storyboard animando as mesmas variáveis. No entanto, um aplicativo pode especificar outros comportamentos determinando a prioridade relativa entre storyboards.

Depois que um storyboard tiver sido agendado, ele não poderá mais ser alterado. No entanto, depois que um storyboard tiver sido removido da agenda, ele poderá ser agendado para reprodução novamente. Os desenvolvedores devem ter cuidado ao reutilizar storyboards, pois isso só deve ser feito quando não há nenhuma chance de que o mesmo storyboard precise ser colocado na fila devido a uma ação do usuário quando ele já está em execução ou na fila na agenda.

## <a name="example-code"></a>Código de exemplo

O código de exemplo a seguir é extraído de MainWindow. cpp [na animação de](application-driven-animation-sample.md) exemplos de animação do Windows e [animação orientada por temporizador](timer-driven-animation-sample.md). Ele usa o método [**IUIAnimationStoryboard:: Schedule**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-schedule) para agendar o storyboard. Esse método requer a hora atual como um parâmetro.


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

Antes de iniciar esta etapa, você deve ter concluído esta etapa: [criar um storyboard e adicionar transições](updating---timer-driven-animation.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**IUIAnimationStoryboard:: Schedule**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-schedule)
</dt> <dt>

[**IUIAnimationTimer:: getTime**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtimer-gettime)
</dt> <dt>

[Visão geral do storyboard](storyboard-construction.md)
</dt> </dl>

 

 




