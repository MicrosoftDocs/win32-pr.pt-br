---
title: Visão geral sobre eventos de automação de interface do usuário
description: A notificação Automação da Interface do Usuário eventos da Microsoft é um recurso fundamental para tecnologias adaptativas, como leitores de tela e lupas de tela.
ms.assetid: 0ded64ba-188e-427e-897f-4381237ace75
keywords:
- Automação da Interface do Usuário,visão geral de eventos
- Automação da Interface do Usuário, categorias de evento
- Automação da Interface do Usuário, notificações de eventos
- notificações de eventos
- eventos, categorias
- eventos, notificações de eventos
- Eventos de alteração de propriedade
- Eventos de ação de elemento
- Eventos de alteração de estrutura
- Eventos globais de alteração da área de trabalho
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ec99a479d390c72232f28521394b2d178f1ad76c913d72ec80aa0a4c93e0d57
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119859566"
---
# <a name="ui-automation-events-overview"></a>Visão geral sobre eventos de automação de interface do usuário

A notificação Automação da Interface do Usuário eventos da Microsoft é um recurso fundamental para tecnologias adaptativas, como leitores de tela e lupas de tela. Esses Automação da Interface do Usuário clientes rastreia eventos gerados por provedores Automação da Interface do Usuário quando algo acontece na interface do usuário e usam as informações para notificar os usuários finais.

A eficiência é aprimorada permitindo que os aplicativos do provedor aumentem eventos seletivamente, dependendo se algum cliente está inscrito nesses eventos ou não, se nenhum cliente estiver escutando eventos.

Os eventos de Automação da Interface do Usuário estão nas seguintes categorias.



| Categoria de evento        | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Alteração da propriedade       | Gerado quando uma propriedade no Automação da Interface do Usuário padrão de controle ou elemento é mudada. Por exemplo, se um cliente precisar monitorar um controle de caixa de seleção de aplicativo, ele poderá se registrar para escutar um evento de alteração de propriedade na propriedade [**IUIAutomationTogglePattern::CurrentToggleState.**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtogglepattern-get_currenttogglestate) Quando o controle de caixa de seleção está marcado ou desmarcado, o provedor a gera e o cliente pode agir conforme necessário. |
| Ação de elemento        | Gerado quando uma alteração na interface do usuário resulta do usuário final ou da atividade programática, por exemplo, quando um botão é clicado ou invocado por meio de [**IUIAutomationInvokePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationinvokepattern).                                                                                                                                                                                                                                                     |
| Alteração de estrutura      | Gerado quando a estrutura da árvore Automação da Interface do Usuário muda. A estrutura muda quando novos itens da interface do usuário se tornam visíveis, ocultos ou são removidos da área de trabalho.                                                                                                                                                                                                                                                                                                              |
| Alteração global da área de trabalho | Gerado quando ocorrem ações de interesse global para o cliente, como quando o foco muda de um elemento para outro ou quando uma janela é fechada.                                                                                                                                                                                                                                                                                                                      |
| Notificação          | Gerado quando um aplicativo chama a [**função UiaRaiseNotificationEvent.**](https://www.bing.com/search?q=**UiaRaiseNotificationEvent**) [**NotificationKind**](/windows/win32/api/uiautomationcore/ne-uiautomationcore-notificationkind) indica o tipo da notificação.                                                                                                                                                                                                                                                 |



 

Alguns eventos não indicam necessariamente que o estado da interface do usuário mudou. Por exemplo, se o usuário for tabulado para um campo de entrada de texto e clicar em um botão para atualizar o campo, um evento [**\_ \_ TextChangedEventId**](uiauto-event-ids.md) da UIA será gerado, mesmo que o usuário não tenha realmente alterado o texto. Ao processar um evento, pode ser necessário que o aplicativo cliente verifique se algo realmente mudou antes de executar uma ação.

Os eventos a seguir podem ser gerados mesmo quando o estado da interface do usuário não foi alterado.

-   [**UIA \_ AutomationPropertyChangedEventId**](uiauto-event-ids.md) (dependendo da propriedade que foi alterada)
-   [**Elemento UIA \_ \_ SelectionItemSelectedEventId**](uiauto-event-ids.md)
-   [**Seleção de UIA \_ \_ InvalidatedEventId**](uiauto-event-ids.md)
-   [**Texto \_ \_ UIAChangedEventId**](uiauto-event-ids.md)

Para ver uma descrição de todos Automação da Interface do Usuário eventos, consulte [Identificadores de eventos](uiauto-event-ids.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Assinando eventos Automação da Interface do Usuário eventos](uiauto-eventsforclients.md)
</dt> </dl>

 

 