---
description: Quando uma determinada ação é executada, os eventos do sistema (prefixados com ISG \_ ) são enviados e recebidos quase instantaneamente pelo aplicativo.
ms.assetid: deca6d17-fe2c-4130-88ca-d0605bcb6084
title: Linha do tempo de mensagens do mouse e eventos do sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8aee3e6cb7882e1628fee0d2bc40f79ed1e29f55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105815548"
---
# <a name="timeline-of-mouse-messages-and-system-events"></a>Linha do tempo de mensagens do mouse e eventos do sistema

Quando uma determinada ação é executada, os eventos do sistema (prefixados com ISG \_ ) são enviados e recebidos quase instantaneamente pelo aplicativo. As mensagens do mouse (prefixadas com o WM \_ ) são enviadas quando a ação é executada e são recebidas pelo aplicativo após o tempo que leva para o evento ser processado pelo serviço de mensagens do Microsoft Windows. Além disso, **CursorDown** e **CursorUp** são eventos de caneta que são recebidos do hardware da caneta. Eles são enviados quando a caneta eletrônica toca a tela e quando ela é levantada da tela, respectivamente.

Eventos de caneta e mensagens do mouse não são sincronizados. Não há nenhuma garantia de que as mensagens de mouse e os eventos de caneta correspondentes ocorrerão em uma ordem específica. O gráfico a seguir mostra a sequência esperada, mas não sempre previsível, de eventos do sistema e do mouse que são enviados. Observe no gráfico que os eventos do mouse estão atrasados quando eventos de gesto do sistema são detectados.

![sequência esperada de eventos do sistema e do mouse para entrada de caneta](images/ccdafa48-13c0-4af7-aec5-ed162be4bbe7.jpg)

## <a name="important-implementation-considerations"></a>Considerações de implementação importantes

Considere o seguinte ao desenvolver para mensagens do mouse e eventos do sistema:

-   Os eventos de caneta e as mensagens do mouse são enviados a um aplicativo, independentemente de a caneta ou o mouse ser usado.
-   Se o seu aplicativo escuta mensagens de caneta e de mouse, é difícil prever a relação das mensagens e, portanto, o comportamento eventual. Eventos de caneta e mensagens do mouse não são sincronizados. Não há nenhuma garantia de que mensagens de mouse e eventos de caneta correspondentes (como WM \_ LBUTTONDOWN e **ISG \_ Tap**, ou WM \_ LBUTTONDBLCLK e **ISG \_ DBLTAP**) ocorrerão em uma ordem específica. A relação entre essas mensagens é complexa.
-   É recomendável não misturar e combinar eventos de mouse e caneta no mesmo recurso de aplicativo. Por exemplo, um recurso de aplicativo que responde a **CursorDown** e **MouseUp** pode não se comportar como esperado agora ou com versões futuras do SDK do Tablet PC.
-   Para a sequência de eventos de espera, se o usuário arrastar a caneta eletrônica antes de a sequência ser concluída, os eventos enviados corresponderão ao arrastar para a esquerda. Por exemplo, quando o arrastar é iniciado, **ISG \_ arrastar** e WM \_ LBUTTONDOWN são enviados. Quando a caneta é eventualmente levantada, o **CursorUp** e o WM \_ LBUTTONUP são enviados. O evento de gesto do sistema pode não ser acionado imediatamente porque ele deve determinar que tipo de evento está ocorrendo.
-   Um toque duplo com uma caneta eletrônica geralmente é menos preciso do que um clique duplo com um mouse. Isso é proveniente da natureza inerente de executar um toque duplo com uma caneta eletrônica. Como o usuário deve levantar a caneta eletrônica para executar um toque duplo, o tempo entre os toques geralmente é maior que o tempo correspondente entre cliques de um clique duplo. Além disso, é provável que os dois toques da caneta do Tablet ocorram nas coordenadas da tela que estão além das que são para os dois cliques do mouse. Para acomodar isso, o Windows XP Tablet PC Edition tem configurações para a distância temporal e espacial entre os dois toques de um toque duplo que são separados das configurações do mouse para um clique duplo. Essas configurações podem ser ajustadas nas configurações do Tablet e da caneta no painel de controle.

Devido a essas considerações, os aplicativos devem escutar apenas um conjunto de mensagens em vez de ambos. Se você estiver criando um aplicativo habilitado para caneta, escute somente as mensagens do sistema e da caneta. Essas mensagens são previsíveis e funcionam bem com a caneta eletrônica. Se você estiver criando um aplicativo que não está habilitado para caneta, escute apenas as mensagens do mouse.

 

 



