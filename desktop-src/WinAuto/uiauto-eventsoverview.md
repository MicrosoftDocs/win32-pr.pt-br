---
title: Visão geral sobre eventos de automação de interface do usuário
description: A notificação de eventos de automação da interface do usuário da Microsoft é um recurso importante para tecnologias assistenciais, como leitores de tela e ampliadores de tela.
ms.assetid: 0ded64ba-188e-427e-897f-4381237ace75
keywords:
- Automação da interface do usuário, visão geral de eventos
- Automação da interface do usuário, categorias de evento
- Automação da interface do usuário, notificações de eventos
- notificações de eventos
- eventos, categorias
- eventos, notificações de eventos
- Eventos de alteração de propriedade
- Eventos de ação do elemento
- Eventos de alteração de estrutura
- Eventos de alteração de área de trabalho global
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9ddd61ed72ae0e92a13f6b59b493427fd7be421
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294106"
---
# <a name="ui-automation-events-overview"></a>Visão geral sobre eventos de automação de interface do usuário

A notificação de eventos de automação da interface do usuário da Microsoft é um recurso importante para tecnologias assistenciais, como leitores de tela e ampliadores de tela. Esses clientes de automação da interface do usuário rastreiam eventos que são gerados por provedores de automação da interface do usuário quando algo acontece na interface do usuário e usam as informações para notificar os usuários finais.

A eficiência é aprimorada permitindo que os aplicativos de provedor gerem eventos de forma seletiva, dependendo se algum cliente estiver inscrito nesses eventos ou não, se nenhum cliente estiver ouvindo nenhum evento.

Os eventos de Automação da Interface do Usuário estão nas seguintes categorias.



| Categoria de evento        | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Alteração da propriedade       | Gerado quando uma propriedade no elemento de automação da interface do usuário ou padrão de controle é alterada. Por exemplo, se um cliente precisar monitorar um controle de caixa de seleção de aplicativo, ele poderá se registrar para escutar um evento de alteração de propriedade na propriedade [**IUIAutomationTogglePattern:: CurrentToggleState**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtogglepattern-get_currenttogglestate) . Quando o controle caixa de seleção está marcado ou desmarcado, o provedor gera o evento e o cliente pode agir conforme necessário. |
| Ação de elemento        | Gerado quando uma alteração na interface do usuário é resultante de uma atividade programática ou de usuários finais, por exemplo, quando um botão é clicado ou invocado por meio de [**IUIAutomationInvokePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationinvokepattern).                                                                                                                                                                                                                                                     |
| Alteração de estrutura      | Gerado quando a estrutura da árvore de automação da interface do usuário é alterada. A estrutura muda quando novos itens da interface do usuário se tornam visíveis, ocultos ou são removidos da área de trabalho.                                                                                                                                                                                                                                                                                                              |
| Alteração global na área de trabalho | Gerado quando ocorrem ações de interesse global para o cliente, como quando o foco muda de um elemento para outro ou quando uma janela é fechada.                                                                                                                                                                                                                                                                                                                      |
| Notificação          | Gerado quando um aplicativo chama a função [**UiaRaiseNotificationEvent**](https://www.bing.com/search?q=**UiaRaiseNotificationEvent**) . [**NotificationKind**](/windows/win32/api/uiautomationcore/ne-uiautomationcore-notificationkind) indica o tipo da notificação.                                                                                                                                                                                                                                                 |



 

Alguns eventos não indicam necessariamente que o estado da interface do usuário mudou. Por exemplo, se o usuário tabular para um campo de entrada de texto e clicar em um botão para atualizar o campo, um evento [**\_ \_ TextChangedEventId de texto UIA**](uiauto-event-ids.md) será gerado, mesmo que o usuário não tenha realmente alterado o texto. Ao processar um evento, pode ser necessário que o aplicativo cliente verifique se algo realmente mudou antes de executar uma ação.

Os eventos a seguir podem ser gerados mesmo quando o estado da interface do usuário não foi alterado.

-   [**UIA \_ AutomationPropertyChangedEventId**](uiauto-event-ids.md) (dependendo da propriedade que foi alterada)
-   [**UIA \_ SelectionItem \_ ElementSelectedEventId**](uiauto-event-ids.md)
-   [**\_InvalidatedEventId de seleção de UIA \_**](uiauto-event-ids.md)
-   [**\_TextChangedEventId de texto UIA \_**](uiauto-event-ids.md)

Para obter uma descrição de todos os eventos de automação da interface do usuário, consulte [identificadores de evento](uiauto-event-ids.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Inscrevendo-se em eventos de automação da interface do usuário](uiauto-eventsforclients.md)
</dt> </dl>

 

 