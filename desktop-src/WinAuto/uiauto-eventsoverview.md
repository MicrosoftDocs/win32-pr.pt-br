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
# <a name="ui-automation-events-overview"></a><span data-ttu-id="37ed2-113">Visão geral sobre eventos de automação de interface do usuário</span><span class="sxs-lookup"><span data-stu-id="37ed2-113">UI Automation Events Overview</span></span>

<span data-ttu-id="37ed2-114">A notificação de eventos de automação da interface do usuário da Microsoft é um recurso importante para tecnologias assistenciais, como leitores de tela e ampliadores de tela.</span><span class="sxs-lookup"><span data-stu-id="37ed2-114">Microsoft UI Automation event notification is a key feature for assistive technologies, such as screen readers and screen magnifiers.</span></span> <span data-ttu-id="37ed2-115">Esses clientes de automação da interface do usuário rastreiam eventos que são gerados por provedores de automação da interface do usuário quando algo acontece na interface do usuário e usam as informações para notificar os usuários finais.</span><span class="sxs-lookup"><span data-stu-id="37ed2-115">These UI Automation clients track events that are raised by UI Automation providers when something happens in the UI and use the information to notify end users.</span></span>

<span data-ttu-id="37ed2-116">A eficiência é aprimorada permitindo que os aplicativos de provedor gerem eventos de forma seletiva, dependendo se algum cliente estiver inscrito nesses eventos ou não, se nenhum cliente estiver ouvindo nenhum evento.</span><span class="sxs-lookup"><span data-stu-id="37ed2-116">Efficiency is improved by allowing provider applications to raise events selectively, depending on whether any clients are subscribed to those events, or not at all, if no clients are listening for any events.</span></span>

<span data-ttu-id="37ed2-117">Os eventos de Automação da Interface do Usuário estão nas seguintes categorias.</span><span class="sxs-lookup"><span data-stu-id="37ed2-117">UI Automation events fall into the following categories.</span></span>



| <span data-ttu-id="37ed2-118">Categoria de evento</span><span class="sxs-lookup"><span data-stu-id="37ed2-118">Event Category</span></span>        | <span data-ttu-id="37ed2-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="37ed2-119">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="37ed2-120">Alteração da propriedade</span><span class="sxs-lookup"><span data-stu-id="37ed2-120">Property change</span></span>       | <span data-ttu-id="37ed2-121">Gerado quando uma propriedade no elemento de automação da interface do usuário ou padrão de controle é alterada.</span><span class="sxs-lookup"><span data-stu-id="37ed2-121">Raised when a property on UI Automation element or control pattern changes.</span></span> <span data-ttu-id="37ed2-122">Por exemplo, se um cliente precisar monitorar um controle de caixa de seleção de aplicativo, ele poderá se registrar para escutar um evento de alteração de propriedade na propriedade [**IUIAutomationTogglePattern:: CurrentToggleState**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtogglepattern-get_currenttogglestate) .</span><span class="sxs-lookup"><span data-stu-id="37ed2-122">For example, if a client needs to monitor an application check box control, it can register to listen for a property change event on the [**IUIAutomationTogglePattern::CurrentToggleState**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtogglepattern-get_currenttogglestate) property.</span></span> <span data-ttu-id="37ed2-123">Quando o controle caixa de seleção está marcado ou desmarcado, o provedor gera o evento e o cliente pode agir conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="37ed2-123">When the check box control is checked or unchecked, the provider raises the event and the client can act as necessary.</span></span> |
| <span data-ttu-id="37ed2-124">Ação de elemento</span><span class="sxs-lookup"><span data-stu-id="37ed2-124">Element action</span></span>        | <span data-ttu-id="37ed2-125">Gerado quando uma alteração na interface do usuário é resultante de uma atividade programática ou de usuários finais, por exemplo, quando um botão é clicado ou invocado por meio de [**IUIAutomationInvokePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationinvokepattern).</span><span class="sxs-lookup"><span data-stu-id="37ed2-125">Raised when a change in the UI results from end user or programmatic activity, for example, when a button is clicked or invoked through [**IUIAutomationInvokePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationinvokepattern).</span></span>                                                                                                                                                                                                                                                     |
| <span data-ttu-id="37ed2-126">Alteração de estrutura</span><span class="sxs-lookup"><span data-stu-id="37ed2-126">Structure change</span></span>      | <span data-ttu-id="37ed2-127">Gerado quando a estrutura da árvore de automação da interface do usuário é alterada.</span><span class="sxs-lookup"><span data-stu-id="37ed2-127">Raised when the structure of the UI Automation tree changes.</span></span> <span data-ttu-id="37ed2-128">A estrutura muda quando novos itens da interface do usuário se tornam visíveis, ocultos ou são removidos da área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="37ed2-128">The structure changes when new UI items become visible, hidden, or removed on the desktop.</span></span>                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="37ed2-129">Alteração global na área de trabalho</span><span class="sxs-lookup"><span data-stu-id="37ed2-129">Global desktop change</span></span> | <span data-ttu-id="37ed2-130">Gerado quando ocorrem ações de interesse global para o cliente, como quando o foco muda de um elemento para outro ou quando uma janela é fechada.</span><span class="sxs-lookup"><span data-stu-id="37ed2-130">Raised when actions of global interest to the client occur, such as when the focus shifts from one element to another, or when a window closes.</span></span>                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="37ed2-131">Notificação</span><span class="sxs-lookup"><span data-stu-id="37ed2-131">Notification</span></span>          | <span data-ttu-id="37ed2-132">Gerado quando um aplicativo chama a função [**UiaRaiseNotificationEvent**](https://www.bing.com/search?q=**UiaRaiseNotificationEvent**) .</span><span class="sxs-lookup"><span data-stu-id="37ed2-132">Raised when an app calls the [**UiaRaiseNotificationEvent**](https://www.bing.com/search?q=**UiaRaiseNotificationEvent**) function.</span></span> <span data-ttu-id="37ed2-133">[**NotificationKind**](/windows/win32/api/uiautomationcore/ne-uiautomationcore-notificationkind) indica o tipo da notificação.</span><span class="sxs-lookup"><span data-stu-id="37ed2-133">[**NotificationKind**](/windows/win32/api/uiautomationcore/ne-uiautomationcore-notificationkind) indicates the type of the notification.</span></span>                                                                                                                                                                                                                                                 |



 

<span data-ttu-id="37ed2-134">Alguns eventos não indicam necessariamente que o estado da interface do usuário mudou.</span><span class="sxs-lookup"><span data-stu-id="37ed2-134">Some events do not necessarily mean that the state of the UI has changed.</span></span> <span data-ttu-id="37ed2-135">Por exemplo, se o usuário tabular para um campo de entrada de texto e clicar em um botão para atualizar o campo, um evento [**\_ \_ TextChangedEventId de texto UIA**](uiauto-event-ids.md) será gerado, mesmo que o usuário não tenha realmente alterado o texto.</span><span class="sxs-lookup"><span data-stu-id="37ed2-135">For example, if the user tabs to a text entry field, and then clicks a button to update the field, a [**UIA\_Text\_TextChangedEventId**](uiauto-event-ids.md) event is raised, even if the user did not actually change the text.</span></span> <span data-ttu-id="37ed2-136">Ao processar um evento, pode ser necessário que o aplicativo cliente verifique se algo realmente mudou antes de executar uma ação.</span><span class="sxs-lookup"><span data-stu-id="37ed2-136">When processing an event, it may be necessary for a client application to check whether anything has actually changed before taking action.</span></span>

<span data-ttu-id="37ed2-137">Os eventos a seguir podem ser gerados mesmo quando o estado da interface do usuário não foi alterado.</span><span class="sxs-lookup"><span data-stu-id="37ed2-137">The following events may be raised even when the state of the UI has not changed.</span></span>

-   <span data-ttu-id="37ed2-138">[**UIA \_ AutomationPropertyChangedEventId**](uiauto-event-ids.md) (dependendo da propriedade que foi alterada)</span><span class="sxs-lookup"><span data-stu-id="37ed2-138">[**UIA\_AutomationPropertyChangedEventId**](uiauto-event-ids.md) (depending on the property that has changed)</span></span>
-   [<span data-ttu-id="37ed2-139">**UIA \_ SelectionItem \_ ElementSelectedEventId**</span><span class="sxs-lookup"><span data-stu-id="37ed2-139">**UIA\_SelectionItem\_ElementSelectedEventId**</span></span>](uiauto-event-ids.md)
-   [<span data-ttu-id="37ed2-140">**\_InvalidatedEventId de seleção de UIA \_**</span><span class="sxs-lookup"><span data-stu-id="37ed2-140">**UIA\_Selection\_InvalidatedEventId**</span></span>](uiauto-event-ids.md)
-   [<span data-ttu-id="37ed2-141">**\_TextChangedEventId de texto UIA \_**</span><span class="sxs-lookup"><span data-stu-id="37ed2-141">**UIA\_Text\_TextChangedEventId**</span></span>](uiauto-event-ids.md)

<span data-ttu-id="37ed2-142">Para obter uma descrição de todos os eventos de automação da interface do usuário, consulte [identificadores de evento](uiauto-event-ids.md).</span><span class="sxs-lookup"><span data-stu-id="37ed2-142">For a description of all UI Automation events, see [Event Identifiers](uiauto-event-ids.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="37ed2-143">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="37ed2-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="37ed2-144">Inscrevendo-se em eventos de automação da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="37ed2-144">Subscribing to UI Automation Events</span></span>](uiauto-eventsforclients.md)
</dt> </dl>

 

 