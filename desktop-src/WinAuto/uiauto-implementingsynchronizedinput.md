---
title: Padrão de controle SynchronizedInput
description: Descreve as diretrizes e convenções para implementar o ISynchronizedInputProvider, incluindo informações sobre propriedades e métodos.
ms.assetid: 3e2d65ea-8093-4e65-b43e-28478ec74607
keywords:
- Automação da interface do usuário, implementando o padrão de controle SynchronizedInput
- Automação da interface do usuário, padrão de controle SynchronizedInput
- Automação da interface do usuário, ISynchronizedInputProvider
- ISynchronizedInputProvider
- Implementando padrões de controle SynchronizedInput de automação da interface do usuário
- Padrões de controle SynchronizedInput
- padrões de controle, ISynchronizedInputProvider
- padrões de controle, implementando a automação da interface do usuário SynchronizedInput
- padrões de controle, SynchronizedInput
- interfaces, ISynchronizedInputProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 105e75163fdac742adaad6b778c251b4b7b8ae70
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105798385"
---
# <a name="synchronizedinput-control-pattern"></a><span data-ttu-id="ff0ad-113">Padrão de controle SynchronizedInput</span><span class="sxs-lookup"><span data-stu-id="ff0ad-113">SynchronizedInput Control Pattern</span></span>

<span data-ttu-id="ff0ad-114">Descreve as diretrizes e convenções para implementar o [**ISynchronizedInputProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-isynchronizedinputprovider), incluindo informações sobre propriedades e métodos.</span><span class="sxs-lookup"><span data-stu-id="ff0ad-114">Describes guidelines and conventions for implementing [**ISynchronizedInputProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-isynchronizedinputprovider), including information about properties and methods.</span></span> <span data-ttu-id="ff0ad-115">O padrão de controle **SynchronizedInput** permite que os aplicativos cliente do Microsoft UI Automation direcionem a entrada do mouse ou do teclado para um elemento específico da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="ff0ad-115">The **SynchronizedInput** control pattern enables Microsoft UI Automation client applications to direct the mouse or keyboard input to a specific UI element.</span></span>

<span data-ttu-id="ff0ad-116">Esse padrão de controle normalmente é usado em scripts de teste automatizados para enviar entrada de mouse ou de teclado para um elemento de interface de usuário específico e, em seguida, verificar se o elemento recebeu a entrada.</span><span class="sxs-lookup"><span data-stu-id="ff0ad-116">This control pattern is typically used in automated test scripts to send mouse or keyboard input to a specific user-interface element, and then verify that the element received the input.</span></span>

<span data-ttu-id="ff0ad-117">Este tópico inclui as seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="ff0ad-117">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="ff0ad-118">Diretrizes e convenções de implementação</span><span class="sxs-lookup"><span data-stu-id="ff0ad-118">Implementation Guidelines and Conventions</span></span>](#implementation-guidelines-and-conventions)
-   [<span data-ttu-id="ff0ad-119">Membros necessários para **ISynchronizedInputProvider**</span><span class="sxs-lookup"><span data-stu-id="ff0ad-119">Required Members for **ISynchronizedInputProvider**</span></span>](#required-members-for-isynchronizedinputprovider)
-   [<span data-ttu-id="ff0ad-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ff0ad-120">Related topics</span></span>](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="ff0ad-121">Diretrizes e convenções de implementação</span><span class="sxs-lookup"><span data-stu-id="ff0ad-121">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="ff0ad-122">Ao implementar o padrão de controle **SynchronizedInput** , observe as seguintes diretrizes e convenções:</span><span class="sxs-lookup"><span data-stu-id="ff0ad-122">When implementing the **SynchronizedInput** control pattern, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="ff0ad-123">Quando o método [**ISynchronizedInputProvider:: StartListening**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-isynchronizedinputprovider-startlistening) é chamado, o provedor de automação da interface do usuário deve iniciar a verificação da entrada do tipo especificado e, em seguida, executar uma das seguintes ações:</span><span class="sxs-lookup"><span data-stu-id="ff0ad-123">When the [**ISynchronizedInputProvider::StartListening**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-isynchronizedinputprovider-startlistening) method is called, the UI Automation provider should start checking for input of the specified type, and then take one of the following actions:</span></span>
    -   <span data-ttu-id="ff0ad-124">Quando a entrada correspondente é encontrada para o elemento, o provedor deve gerar o evento [**UIA \_ InputReachedTargetEventId**](uiauto-event-ids.md) .</span><span class="sxs-lookup"><span data-stu-id="ff0ad-124">When matching input is found for the element, the provider should raise the [**UIA\_InputReachedTargetEventId**](uiauto-event-ids.md) event.</span></span>
    -   <span data-ttu-id="ff0ad-125">Quando a entrada correspondente é encontrada, mas ela atingiu um elemento diferente, o provedor deve gerar o evento [**UIA \_ InputReachedOtherElementEventId**](uiauto-event-ids.md) .</span><span class="sxs-lookup"><span data-stu-id="ff0ad-125">When matching input is found, but it reached a different element, the provider should raise the [**UIA\_InputReachedOtherElementEventId**](uiauto-event-ids.md) event.</span></span>
    -   <span data-ttu-id="ff0ad-126">Quando uma entrada incompatível é encontrada, o provedor deve descartar a entrada e gerar o evento [**UIA \_ InputDiscardedEventId**](uiauto-event-ids.md) .</span><span class="sxs-lookup"><span data-stu-id="ff0ad-126">When mismatched input is found, the provider should discard the input and raise the [**UIA\_InputDiscardedEventId**](uiauto-event-ids.md) event.</span></span>
-   <span data-ttu-id="ff0ad-127">O provedor de automação de interface do usuário deve descartar a entrada se for para um elemento que não seja o elemento atual.</span><span class="sxs-lookup"><span data-stu-id="ff0ad-127">The UI Automation provider must discard the input if it is for an element other than the current element.</span></span>
-   <span data-ttu-id="ff0ad-128">Quando o elemento recebe a entrada, ou quando o método [**ISynchronizedInputProvider:: Cancel**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-isynchronizedinputprovider-cancel) é chamado, o provedor para de verificar a entrada e continua normalmente.</span><span class="sxs-lookup"><span data-stu-id="ff0ad-128">When the element receives the input, or when the [**ISynchronizedInputProvider::Cancel**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-isynchronizedinputprovider-cancel) method is called, the provider stops checking input and continues as normal.</span></span>
-   <span data-ttu-id="ff0ad-129">Se [**ISynchronizedInputProvider:: StartListening**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-isynchronizedinputprovider-startlistening) for chamado quando o provedor já estiver ouvindo a entrada, o provedor deverá retornar [**UIA \_ E \_ INVALIDOPERATION**](uiauto-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="ff0ad-129">If [**ISynchronizedInputProvider::StartListening**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-isynchronizedinputprovider-startlistening) is called when the provider is already listening for input, the provider should return [**UIA\_E\_INVALIDOPERATION**](uiauto-error-codes.md).</span></span>

## <a name="required-members-for-isynchronizedinputprovider"></a><span data-ttu-id="ff0ad-130">Membros necessários para **ISynchronizedInputProvider**</span><span class="sxs-lookup"><span data-stu-id="ff0ad-130">Required Members for **ISynchronizedInputProvider**</span></span>

<span data-ttu-id="ff0ad-131">As propriedades, os métodos e os eventos a seguir são necessários para implementar a interface [**ISynchronizedInputProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-isynchronizedinputprovider) .</span><span class="sxs-lookup"><span data-stu-id="ff0ad-131">The following properties, methods, and events are required for implementing the [**ISynchronizedInputProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-isynchronizedinputprovider) interface.</span></span>



| <span data-ttu-id="ff0ad-132">Membros necessários</span><span class="sxs-lookup"><span data-stu-id="ff0ad-132">Required members</span></span>                                                                         | <span data-ttu-id="ff0ad-133">Tipo de membro</span><span class="sxs-lookup"><span data-stu-id="ff0ad-133">Member type</span></span> | <span data-ttu-id="ff0ad-134">Observações</span><span class="sxs-lookup"><span data-stu-id="ff0ad-134">Notes</span></span> |
|------------------------------------------------------------------------------------------|-------------|-------|
| [<span data-ttu-id="ff0ad-135">**StartListening**</span><span class="sxs-lookup"><span data-stu-id="ff0ad-135">**StartListening**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-isynchronizedinputprovider-startlistening)               | <span data-ttu-id="ff0ad-136">Método</span><span class="sxs-lookup"><span data-stu-id="ff0ad-136">Method</span></span>      | <span data-ttu-id="ff0ad-137">Nenhum</span><span class="sxs-lookup"><span data-stu-id="ff0ad-137">None</span></span>  |
| [<span data-ttu-id="ff0ad-138">**Cancelar**</span><span class="sxs-lookup"><span data-stu-id="ff0ad-138">**Cancel**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-isynchronizedinputprovider-cancel)                               | <span data-ttu-id="ff0ad-139">Método</span><span class="sxs-lookup"><span data-stu-id="ff0ad-139">Method</span></span>      | <span data-ttu-id="ff0ad-140">Nenhum</span><span class="sxs-lookup"><span data-stu-id="ff0ad-140">None</span></span>  |
| [<span data-ttu-id="ff0ad-141">**UIA \_ InputReachedTargetEventId**</span><span class="sxs-lookup"><span data-stu-id="ff0ad-141">**UIA\_InputReachedTargetEventId**</span></span>](uiauto-event-ids.md) | <span data-ttu-id="ff0ad-142">Evento</span><span class="sxs-lookup"><span data-stu-id="ff0ad-142">Event</span></span>       | <span data-ttu-id="ff0ad-143">Nenhum</span><span class="sxs-lookup"><span data-stu-id="ff0ad-143">None</span></span>  |



 

## <a name="related-topics"></a><span data-ttu-id="ff0ad-144">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ff0ad-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ff0ad-145">Visão Geral de Padrões de Controle de Automação de Interface de Usuário</span><span class="sxs-lookup"><span data-stu-id="ff0ad-145">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> </dl>

 

 




