---
title: Visão geral da arquitetura
description: Essa visão geral da arquitetura fornece contexto para a API de toque do Windows para tecnologias de Tablet e Touch e explica como ela se encaixa na arquitetura maior do Windows 7.
ms.assetid: b284e96f-0998-408c-ae84-92a3acdc3014
keywords:
- Windows Touch, visão geral da arquitetura
- Windows Touch, manipulações
- Windows Touch, mensagens
- Windows Touch, inércia
- Toque do Windows, gestos
- gestos, sobre
- manipulações, sobre
- inércia, sobre
- processador de manipulação, visão geral da arquitetura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b807113211d77f0aad0ed01fc24570d033063474
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103917320"
---
# <a name="architectural-overview"></a>Visão geral da arquitetura

Essa visão geral da arquitetura fornece contexto para a API de toque do Windows para tecnologias de Tablet e Touch e explica como ela se encaixa na arquitetura maior do Windows 7.

## <a name="messages-for-windows-touch-input-and-gestures"></a>Mensagens para entrada e gestos do Windows Touch

Os recursos do sistema de mensagens para Windows Touch são habilitados ouvindo e interpretando mensagens durante a execução. A ilustração a seguir mostra como as mensagens são geradas do hardware e enviadas aos aplicativos pelo Windows 7.

![ilustração mostrando como o Windows 7 envia mensagens do hardware multitoque para um aplicativo](images/wm-multitouch-messaging.png)

Na coluna mais à esquerda da ilustração, o hardware sensível ao toque recebe a entrada de um usuário. Em seguida, um driver se comunica entre o hardware e o sistema operacional. Em seguida, o sistema operacional gera uma mensagem [**de \_ gesto**](wm-gesture.md) do [**WM \_ Touch**](wm-touchdown.md) ou do WM que é enviada para o HWND de um aplicativo. Em seguida, o aplicativo atualiza a interface do usuário de acordo com as informações encapsuladas na mensagem.

Por padrão, os aplicativos recebem gestos. A menos que um aplicativo seja registrado para mensagens de entrada de toque do Windows com a função [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow) , as notificações para gestos (mensagens de [**\_ gesto do WM**](wm-gesture.md) ) são criadas pelo Windows e enviadas para essa janela de aplicativo. Se uma janela de aplicativo for registrada para receber mensagens de toque, as notificações para entrada do Windows Touch (mensagens de [**\_ toque do WM**](wm-touchdown.md) ) serão enviadas para essa janela de aplicativo. As mensagens de toque e gesto do Windows são ávidos no sentido de que, depois que um toque é feito ou um gesto começa em uma janela de aplicativo, todas as mensagens são enviadas para esse aplicativo até que o gesto seja concluído ou o toque primário seja concluído.

Para suporte herdado, o Windows interpreta mensagens de [**\_ gesto do WM**](wm-gesture.md) se elas forem consumidas e ENVIARá ou lançará as mensagens apropriadas que são mapeadas para o gesto. Para evitar a interrupção do suporte herdado, certifique-se de encaminhar mensagens de gesto do WM \_ usando [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca). Mais informações sobre o suporte herdado podem ser encontradas na seção [visão geral dos gestos do Windows Touch](windows-touch-gestures-overview.md).

## <a name="manipulations-and-inertia"></a>Manipulações e inércia

Os programadores do Windows Touch devem ser capazes de interpretar gestos de várias fontes de uma maneira que seja significativa para o gesto em andamento. A Microsoft fornece a API de manipulação para executar esses cálculos. As manipulações são essencialmente gestos com valores associados a elas que descrevem todo o gesto. Depois de conectar os dados de entrada ao processador de manipulação, você pode recuperar informações pertinentes à ação que o usuário faz no objeto. A figura a seguir mostra uma maneira que você pode usar manipulações.

![ilustração mostrando mensagens de toque do Windows passadas para o processador de manipulação de um objeto, que manipula eventos com a \- interface imanipulationevents](images/manipulation-arch.png)

Na parte superior esquerda da ilustração, o usuário tocou na tela, que cria mensagens de toque. Essas mensagens contêm uma coordenada x e uma coordenada y que são usadas para determinar o objeto que está em foco. O objeto em foco contém um processador de manipulação. Em seguida, na mensagem do [**WM \_ Touch**](wm-touchdown.md) com o sinalizador **TOUCHEVENTF \_ up** , o objeto no foco do usuário é selecionado, o processador de manipulação é referenciado e a mensagem é enviada para o processador de manipulação. As próximas mensagens do **WM \_ Touch** associadas a este contato são enviadas para o processador de manipulação até que a mensagem do **WM \_ Touch** com o sinalizador **TOUCHEVENTF \_ up** seja recebida e o objeto selecionado seja desreferenciado. Na seção inferior direita da ilustração, um coletor de eventos de manipulação que implementa a interface [**\_ IManipulationEvents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) é usado para manipular os eventos de manipulação, que são gerados enquanto as mensagens de toque estão sendo criadas. O coletor de eventos pode executar atualizações na interface com base nos eventos de manipulação enquanto eles ocorrem.

Em aplicativos Windows Touch, é comum incorporar uma física simples para que os objetos cheguem a uma parada tranqüila, em vez de serem interrompidos abruptamente quando não estiverem mais sendo tocados. A Microsoft fornece a API inércia para executar os cálculos para essas física simples, de forma que seu aplicativo possa se comportar de maneira semelhante a outros aplicativos. Isso também poupa o esforço necessário para criar uma funcionalidade de física robusta. A figura a seguir mostra como você pode usar o inércia.

![ilustração mostrando mensagens de toque do Windows passadas para a interface IInertiaProcessor de um objeto, que gera eventos com a \- interface imanipulationevents](images/inertia-arch.png)

Observe as semelhanças entre inércia e manipulação. A única diferença entre os dois é que, no caso do inércia, as mensagens interpretadas são enviadas para um processador inércia em vez de um processador de manipulação e o processador inércia gera os eventos. Na parte superior esquerda da ilustração, na mensagem do [**WM \_ Touch**](wm-touchdown.md) com o sinalizador **TOUCHEVENTF \_ up** , as mensagens de toque são usadas para identificar um objeto em foco que contém um processador inércia e um processador de manipulação. As próximas mensagens do **WM \_ Touch** são enviadas para o processador de manipulação e o processador de manipulação executa atualizações na interface do usuário do aplicativo. Depois que a manipulação for concluída, os valores de velocidade da manipulação serão usados para configurar um processador inércia. Conforme ilustrado na coluna do meio, o método [**processo**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-process) ou [**processtime**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-processtime) é chamado na interface [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) usando um temporizador ou outro loop em um thread separado até que as chamadas indiquem que o processamento do processador terminou. Embora essas chamadas sejam feitas, os eventos de manipulação são gerados, que são tratados por um coletor de eventos de manipulação com base na interface [**\_ IManipulationEvents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) . Na seção inferior direita da ilustração, esse coletor de eventos executa atualizações na interface do usuário do aplicativo com base em eventos de manipulação quando eles ocorrem por meio de manipuladores de eventos no coletor de eventos.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Guia de programação](programming-guide.md)
</dt> </dl>

 

 