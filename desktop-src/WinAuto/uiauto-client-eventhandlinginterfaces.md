---
title: Interfaces de manipulação de eventos para clientes
description: Esta seção descreve as interfaces de manipulação de eventos para aplicativos cliente de automação de interface do usuário não gerenciado.
ms.assetid: ce9c4044-f46b-42b7-af44-05aee728a0e8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 458be6fcf5ce47f285d46c0e61f80e0897f15613
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105807961"
---
# <a name="event-handling-interfaces-for-clients"></a><span data-ttu-id="4683d-103">Interfaces de manipulação de eventos para clientes</span><span class="sxs-lookup"><span data-stu-id="4683d-103">Event Handling Interfaces for Clients</span></span>

<span data-ttu-id="4683d-104">Esta seção descreve as interfaces de manipulação de eventos para aplicativos cliente de automação de interface do usuário não gerenciado.</span><span class="sxs-lookup"><span data-stu-id="4683d-104">This section describes the event handling interfaces for unmanaged UI Automation client applications.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="4683d-105">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="4683d-105">In this section</span></span>



| <span data-ttu-id="4683d-106">Interface</span><span class="sxs-lookup"><span data-stu-id="4683d-106">Interface</span></span>                                                                                                              | <span data-ttu-id="4683d-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="4683d-107">Description</span></span>                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4683d-108">**IUIAutomationChangesEventHandler**</span><span class="sxs-lookup"><span data-stu-id="4683d-108">**IUIAutomationChangesEventHandler**</span></span>](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationchangeseventhandler)<br/>                         | <span data-ttu-id="4683d-109">Expõe um método para manipular eventos de automação da interface do usuário da Microsoft que ocorrem quando uma propriedade é alterada.</span><span class="sxs-lookup"><span data-stu-id="4683d-109">Exposes a method to handle Microsoft UI Automation events that occur when a property is changed.</span></span><br/>                      |
| [<span data-ttu-id="4683d-110">**IUIAutomationEventHandler**</span><span class="sxs-lookup"><span data-stu-id="4683d-110">**IUIAutomationEventHandler**</span></span>](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationeventhandler)<br/>                                       | <span data-ttu-id="4683d-111">Expõe um método para manipular eventos de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="4683d-111">Exposes a method to handle UI Automation events.</span></span><br/>                                                                      |
| [<span data-ttu-id="4683d-112">**IUIAutomationFocusChangedEventHandler**</span><span class="sxs-lookup"><span data-stu-id="4683d-112">**IUIAutomationFocusChangedEventHandler**</span></span>](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationfocuschangedeventhandler)<br/>               | <span data-ttu-id="4683d-113">Expõe um método para manipular eventos que são gerados quando o foco do teclado é movido para outro elemento de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="4683d-113">Exposes a method to handle events that are raised when the keyboard focus moves to another UI Automation element.</span></span><br/>     |
| [<span data-ttu-id="4683d-114">**IUIAutomationNotificationEventHandler**</span><span class="sxs-lookup"><span data-stu-id="4683d-114">**IUIAutomationNotificationEventHandler**</span></span>](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationnotificationeventhandler)<br/>               | <span data-ttu-id="4683d-115">Expõe um método para manipular eventos de notificação de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="4683d-115">Exposes a method to handle UI Automation notification events.</span></span><br/>                                                         |
| [<span data-ttu-id="4683d-116">**IUIAutomationPropertyChangedEventHandler**</span><span class="sxs-lookup"><span data-stu-id="4683d-116">**IUIAutomationPropertyChangedEventHandler**</span></span>](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationpropertychangedeventhandler)<br/>         | <span data-ttu-id="4683d-117">Expõe um método para manipular eventos de automação da interface do usuário que ocorrem quando uma propriedade é alterada.</span><span class="sxs-lookup"><span data-stu-id="4683d-117">Exposes a method to handle UI Automation events that occur when a property is changed.</span></span><br/>                                |
| [<span data-ttu-id="4683d-118">**IUIAutomationStructureChangedEventHandler**</span><span class="sxs-lookup"><span data-stu-id="4683d-118">**IUIAutomationStructureChangedEventHandler**</span></span>](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationstructurechangedeventhandler)<br/>       | <span data-ttu-id="4683d-119">Expõe um método para manipular eventos que ocorrem quando a estrutura da árvore de automação da interface do usuário é alterada.</span><span class="sxs-lookup"><span data-stu-id="4683d-119">Exposes a method to handle events that occur when the UI Automation tree structure is changed.</span></span><br/>                        |
| [<span data-ttu-id="4683d-120">**IUIAutomationTextEditTextChangedEventHandler**</span><span class="sxs-lookup"><span data-stu-id="4683d-120">**IUIAutomationTextEditTextChangedEventHandler**</span></span>](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextedittextchangedeventhandler)<br/> | <span data-ttu-id="4683d-121">Expõe um método para manipular eventos que ocorrem quando a automação da interface do usuário relata um evento de alteração de texto dos controles de edição de texto.</span><span class="sxs-lookup"><span data-stu-id="4683d-121">Exposes a method to handle events that occur when UI Automation reports a text-changed event from text edit controls.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="4683d-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4683d-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4683d-123">Clientes de automação da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="4683d-123">UI Automation Clients</span></span>](uiauto-entry-uiautoclientsforwin32apps.md)
</dt> </dl>

 

 





