---
title: Inscrevendo-se em eventos de automação da interface do usuário
description: A automação da interface do usuário da Microsoft permite que os clientes assinem eventos de interesse. Esse recurso melhora o desempenho ao eliminar a necessidade de sondar continuamente os elementos da interface do usuário no sistema para ver se alguma informação, estrutura ou estado foi alterada.
ms.assetid: 7019ecb8-6123-4e00-926c-6725d7e71385
keywords:
- clientes, eventos de automação da interface do usuário
- clientes, eventos para automação da interface do usuário
- Automação da interface do usuário, eventos para clientes
- Automação da interface do usuário, eventos de cliente
- Automação da interface do usuário, inscrevendo-se em eventos
- Automação da interface do usuário, métodos de assinatura
- Automação da interface do usuário, exemplos de código
- Automação da interface do usuário, exemplos
- Automação da interface do usuário, amostras
- assinando eventos de Automação de Interface de Usuário
- eventos, assinatura de automação da interface do usuário
- Exemplos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a0e8dd4cb2d810ad8423c1fa4f75020a9489ceb72acbe1483cb439e943b5676
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119505296"
---
# <a name="subscribing-to-ui-automation-events"></a>Inscrevendo-se em eventos de automação da interface do usuário

A automação da interface do usuário da Microsoft permite que os clientes assinem eventos de interesse. Esse recurso melhora o desempenho ao eliminar a necessidade de sondar continuamente os elementos da interface do usuário no sistema para ver se alguma informação, estrutura ou estado foi alterada.

A eficiência também é aprimorada pela capacidade de escutar eventos somente dentro de um escopo definido. Por exemplo, um cliente pode escutar alterações de seleção em um item de uma lista, na própria lista ou em uma caixa de diálogo inteira.

> [!Note]  
> Não presuma que todos os eventos possíveis sejam gerados por um provedor de automação de interface do usuário. por exemplo, nem todas as alterações de propriedade fazem com que os eventos sejam gerados pelos provedores de proxy padrão para os controles Windows Forms e Microsoft Win32.

 

Para obter uma visão mais ampla dos eventos de automação da interface do usuário, consulte [visão geral dos eventos de automação da IU](uiauto-eventsoverview.md).

> [!Note]  
> Antes de implementar um manipulador de eventos, você deve estar familiarizado com os problemas de Threading descritos em [noções básicas sobre problemas de Threading](uiauto-threading.md).

 

Este tópico inclui as seções a seguir.

-   [Registrando manipuladores de eventos](#registering-event-handlers)
-   [Exemplos](#examples)
-   [Tópicos relacionados](#related-topics)

## <a name="registering-event-handlers"></a>Registrando manipuladores de eventos

Os aplicativos cliente assinam eventos de um tipo específico registrando um manipulador de eventos, usando um dos seguintes métodos [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) .



| Método de assinatura                                                                                                                                                                                                | Tipo de evento       | Interface de retorno de chamada                                                                                    |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------|-------------------------------------------------------------------------------------------------------|
| [**AddFocusChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addfocuschangedeventhandler)                                                                                                                            | Alteração de foco     | [**IUIAutomationFocusChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationfocuschangedeventhandler)         |
| [**AddPropertyChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addpropertychangedeventhandler), [ **AddPropertyChangedEventHandlerNativeArray**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addpropertychangedeventhandlernativearray) | Alteração da propriedade  | [**IUIAutomationPropertyChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationpropertychangedeventhandler)   |
| [**AddStructureChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addstructurechangedeventhandler)                                                                                                                    | Alteração de estrutura | [**IUIAutomationStructureChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationstructurechangedeventhandler) |
| [**AddNotificationEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation5-addnotificationeventhandler)                                                                                                                           | Notificação     | [**IUIAutomationNotificationEventHandler**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationnotificationeventhandler)         |
| [**AddAutomationEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addautomationeventhandler)                                                                                                                                | Outros eventos     | [**IUIAutomationEventHandler**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationeventhandler)                                 |



 

Quando um cliente adiciona um manipulador de eventos para todos os descendentes (os [**\_ descendentes TreeScope**](/windows/desktop/api/UIAutomationClient/ne-uiautomationclient-treescope)), a automação da interface do usuário adiciona apenas um manipulador para a raiz da subárvore e o manipulador escuta em todos os descendentes. A automação da interface do usuário não Adiciona manipuladores de eventos recursivamente.

Quando um cliente chama o método [**IUIAutomation:: RemoveAllEventHandlers**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-removealleventhandlers) , a automação da interface do usuário remove todos os manipuladores de eventos do processo do cliente.

Para receber e manipular eventos, você implementa um objeto de manipulação de eventos que expõe uma interface de retorno de chamada, e você deve registrar o objeto chamando um método de registro de evento, como [**IUIAutomation:: AddPropertyChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addpropertychangedeventhandler). A interface de retorno de chamada tem um único método; A automação da interface do usuário chama esse método quando o evento é processado.

No desligamento, ou quando eventos de automação da interface do usuário não são mais interessantes para o aplicativo, os clientes de automação da interface do usuário devem chamar um ou mais dos seguintes métodos [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) .

> [!Note]  
> Um cliente de automação de interface do usuário não deve usar vários threads para adicionar ou remover manipuladores de eventos. Um comportamento inesperado pode ocorrer se um manipulador de eventos estiver sendo adicionado ou removido enquanto outro estiver sendo adicionado ou removido no mesmo processo de cliente.

 



| Método                                                                                                | Descrição                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**RemoveAutomationEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-removeautomationeventhandler)             | Cancela o registro de um manipulador de eventos que foi registrado usando [**AddAutomationEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addautomationeventhandler).                                                                                                                                  |
| [**RemoveFocusChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-removefocuschangedeventhandler)         | Cancela o registro de um manipulador de eventos que foi registrado usando [**AddFocusChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addfocuschangedeventhandler).                                                                                                                              |
| [**RemovePropertyChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-removepropertychangedeventhandler)   | Cancela o registro de um manipulador de eventos que foi registrado usando [**AddPropertyChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addpropertychangedeventhandler) ou [**AddPropertyChangedEventHandlerNativeArray**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addpropertychangedeventhandlernativearray). |
| [**RemoveStructureChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-removestructurechangedeventhandler) | Cancela o registro de um manipulador de eventos que foi registrado usando [**AddStructureChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addstructurechangedeventhandler).                                                                                                                      |
| [**RemoveNotificationEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation5-removenotificationeventhandler)        | Cancela o registro de um manipulador de eventos que Weas registrado usando [**AddNotificationEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation5-addnotificationeventhandler).                                                                                                                            |
| [**RemoveAllEventHandlers**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-removealleventhandlers)                         | Cancela o registro de todos os manipuladores de eventos registrados.                                                                                                                                                                                                                                      |



 

É possível que um evento seja entregue a um manipulador de eventos após o cancelamento da assinatura do manipulador, se o evento for recebido simultaneamente com a solicitação para cancelar a assinatura do evento. A prática recomendada é seguir o padrão de Component Object Model (COM) e evitar destruir o objeto manipulador de eventos até que sua contagem de referência tenha atingido zero. Destruir um manipulador de eventos imediatamente após a desentrada de eventos pode resultar em uma violação de acesso se um evento for entregue tardiamente.

## <a name="examples"></a>Exemplos

Para obter exemplos de código que mostram como manipular eventos de automação da interface do usuário, consulte [como implementar manipuladores de eventos](uiauto-howto-implement-event-handlers.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Conceitua**
</dt> <dt>

[Visão geral sobre eventos de automação de interface do usuário](uiauto-eventsoverview.md)
</dt> <dt>

[Noções básicas sobre problemas de Threading](uiauto-threading.md)
</dt> </dl>

 

 




