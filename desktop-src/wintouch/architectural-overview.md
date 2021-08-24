---
title: Visão geral da arquitetura
description: Esta visão geral da arquitetura fornece contexto para a API Windows Touch para Tecnologias de Tablet e Toque e explica como ela se encaixa na arquitetura Windows 7.
ms.assetid: b284e96f-0998-408c-ae84-92a3acdc3014
keywords:
- Windows Toque, visão geral da arquitetura
- Windows Toque, manipulações
- Windows Toque, mensagens
- Windows Toque, inércia
- Windows Toque, gestos
- gestos, sobre
- manipulações, sobre
- inércia, sobre
- processador de manipulação, visão geral da arquitetura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36b5ce003c88a66e96072fa9f96bc6ae73bd91cb39f53e03ab3748dd14a194d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119448639"
---
# <a name="architectural-overview"></a>Visão geral da arquitetura

Esta visão geral da arquitetura fornece contexto para a API Windows Touch para Tecnologias de Tablet e Toque e explica como ela se encaixa na arquitetura Windows 7.

## <a name="messages-for-windows-touch-input-and-gestures"></a>Mensagens para Windows e gestos de toque

Os recursos de mensagens para Windows Touch são habilitados escutando e interpretando mensagens durante a execução. A ilustração a seguir mostra como as mensagens são geradas do hardware e enviadas aos aplicativos Windows 7.

![ilustração mostrando como o Windows 7 envia mensagens do hardware multitouch para um aplicativo](images/wm-multitouch-messaging.png)

Na coluna mais à esquerda da ilustração, o hardware sensível ao toque recebe a entrada de um usuário. Em seguida, um driver se comunica entre o hardware e o sistema operacional. Em seguida, o sistema operacional gera uma [**mensagem WM \_ TOUCH**](wm-touchdown.md) ou [**WM \_ GESTURE**](wm-gesture.md) que é enviada para o HWND de um aplicativo. Em seguida, o aplicativo atualiza a interface do usuário considerando as informações encapsuladas na mensagem.

Os aplicativos recebem gestos por padrão. A menos que um aplicativo se registre para mensagens de entrada Windows Touch com a função [**RegisterTouchWindow,**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow) as notificações de gestos (mensagens [**WM \_ GESTURE)**](wm-gesture.md) são criadas pelo Windows enviadas para essa janela de aplicativo. Se uma janela do aplicativo se registrar para receber mensagens de toque, as notificações Windows entrada touch (mensagens [**WM \_ TOUCH)**](wm-touchdown.md) serão enviadas para essa janela do aplicativo. Windows Mensagens de toque e gesto são greedy no sentido de que, depois que um toque é feito ou um gesto começa em uma janela do aplicativo, todas as mensagens são enviadas para esse aplicativo até que o gesto seja concluído ou o toque primário seja concluído.

Para suporte herdado, Windows interpreta mensagens [**WM \_ GESTURE**](wm-gesture.md) se elas estão em bolhas e, em seguida, ENVIAR ou POSTAR mensagens apropriadas que são mapeadas para o gesto. Para evitar a quebra do suporte herdado, certifique-se de encaminhar mensagens WM \_ GESTURE usando [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca). Mais informações sobre o suporte herdamento podem ser encontradas na seção Windows Visão geral de [gestos de toque.](windows-touch-gestures-overview.md)

## <a name="manipulations-and-inertia"></a>Manipulações e inércia

Windows Os programadores de toque devem ser capazes de interpretar gestos de várias fontes de uma maneira significativa para o gesto que está ocorrendo. A Microsoft fornece a API de manipulação para executar esses cálculos. As manipulações são essencialmente gestos com valores associados a eles que descrevem todo o gesto. Depois de conectar os dados de entrada ao processador de manipulação, você pode recuperar informações pertinentes à ação que o usuário faz no objeto. A figura a seguir mostra uma maneira de usar manipulações.

![ilustração mostrando as mensagens de toque do Windows passadas para o processador de manipulação de um objeto, que manipula eventos com a \- interface imanipulationevents](images/manipulation-arch.png)

No canto superior esquerdo da ilustração, o usuário tocada na tela, o que cria mensagens de toque. Essas mensagens contêm uma coordenada x e uma coordenada y que são usadas para determinar o objeto que está em foco. O objeto em foco contém um processador de manipulação. Em seguida, na mensagem [**WM \_ TOUCH**](wm-touchdown.md) com o sinalizador **TOUCHEVENTF \_ UP,** o objeto no foco do usuário é selecionado, o processador de manipulação é referenciado e a mensagem é enviada para o processador de manipulação. As **mensagens WM \_ TOUCH** subsequentes associadas a esse contato são enviadas para o processador de manipulação até que a mensagem **WM \_ TOUCH** com o sinalizador **TOUCHEVENTF \_ UP** seja recebida e o objeto selecionado seja desreferenciado. Na seção inferior direita da ilustração, um sink de evento de manipulação que implementa a interface [**\_ IManipulationEvents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) é usado para manipular os eventos de manipulação, que são gerados enquanto as mensagens de toque estão sendo criadas. O sink de evento pode executar atualizações na interface com base nos eventos de manipulação enquanto eles ocorrem.

No Windows Touch, é comum incorporar a física simples para que os objetos sejam parar sem problemas, em vez de parar de forma tão repentina quando não estão mais sendo tocados. A Microsoft fornece a API de Inércia para executar os cálculos para essas físicas simples para que seu aplicativo possa se comportar de maneira semelhante a outros aplicativos. Isso também economiza o esforço necessário para criar uma funcionalidade de física robusta. A figura a seguir mostra como você pode usar a inércia.

![ilustração mostrando mensagens de toque do Windows passadas para a interface iinertiaprocessor de um objeto, que gera eventos com a \- interface imanipulationevents](images/inertia-arch.png)

Observe as semelhanças entre inércia e manipulação. A única diferença entre os dois é que, no caso de inércia, as mensagens interpretadas são entregues a um processador de inércia em vez de um processador de manipulação e o processador de inércia gera os eventos. No canto superior esquerdo da ilustração, na mensagem [**WM \_ TOUCH**](wm-touchdown.md) com o sinalizador **TOUCHEVENTF \_ UP,** as mensagens de toque são usadas para identificar um objeto em foco que contém um processador de inércia e um processador de manipulação. As **mensagens WM \_ TOUCH** subsequentes são enviadas para o processador de manipulação e o processador de manipulação executa atualizações na interface do usuário do aplicativo. Depois que a manipulação é concluída, os valores de velocidade da manipulação são usados para configurar um processador de inércia. Conforme ilustrado na coluna intermediária, o método [**Process**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-process) [**ou ProcessTime**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-processtime) é chamado na interface [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) usando um temporizador ou outro loop em um thread separado até que as chamadas indiquem que o processador terminou o processamento. Embora essas chamadas sejam feitas, os eventos de manipulação são gerados, que são tratados por um sink de evento de manipulação com base na interface [**\_ IManipulationEvents.**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) Na seção inferior direita da ilustração, esse sink de evento executa atualizações na interface do usuário do aplicativo com base em eventos de manipulação quando eles ocorrem por meio de manipuladores de eventos no sink de eventos.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Guia de programação](programming-guide.md)
</dt> </dl>

 

 