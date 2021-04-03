---
title: Noções básicas sobre problemas de Threading
description: Este tópico descreve cenários de Threading comuns para implementações do cliente de automação da interface do usuário da Microsoft e explica como evitar problemas que podem ocorrer se um cliente usa o Threading incorretamente.
ms.assetid: 0772969a-da55-488e-8b21-7368434df8a9
keywords:
- clientes, problemas de threading de automação da interface do usuário
- clientes, problemas de Threading
- clientes, modelo de Threading do manipulador de eventos
- clientes, modelo de Threading do manipulador de eventos de automação da interface do usuário
- clientes, afinidade de automação da interface do usuário
- clientes, afinidade
- Automação da interface do usuário, problemas de Threading
- Automação da interface do usuário, modelo de Threading do manipulador de eventos
- Automação da interface do usuário, afinidade
- problemas com threading
- modelo de Threading do manipulador de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a002132efe4055bb247c7d7290e271e153ac297e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007601"
---
# <a name="understanding-threading-issues"></a><span data-ttu-id="1bb4c-114">Noções básicas sobre problemas de Threading</span><span class="sxs-lookup"><span data-stu-id="1bb4c-114">Understanding Threading Issues</span></span>

<span data-ttu-id="1bb4c-115">Este tópico descreve cenários de Threading comuns para implementações do cliente de automação da interface do usuário da Microsoft e explica como evitar problemas que podem ocorrer se um cliente usa o Threading incorretamente.</span><span class="sxs-lookup"><span data-stu-id="1bb4c-115">This topic describes common threading scenarios for Microsoft UI Automation client implementations and explains how to avoid problems that can occur if a client uses threading incorrectly.</span></span>

<span data-ttu-id="1bb4c-116">Este tópico contém as seguintes seções:</span><span class="sxs-lookup"><span data-stu-id="1bb4c-116">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="1bb4c-117">Automação da interface do usuário e thread da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="1bb4c-117">UI Automation and the UI Thread</span></span>](#ui-automation-and-the-ui-thread)
-   [<span data-ttu-id="1bb4c-118">Modelo de threading para manipuladores de eventos</span><span class="sxs-lookup"><span data-stu-id="1bb4c-118">Threading Model for Event Handlers</span></span>](#threading-model-for-event-handlers)
-   [<span data-ttu-id="1bb4c-119">Afinidade de apartamento COM em Windows de 64 bits</span><span class="sxs-lookup"><span data-stu-id="1bb4c-119">COM Apartment Affinity on 64-bit Windows</span></span>](#com-apartment-affinity-on-64-bit-windows)
-   [<span data-ttu-id="1bb4c-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1bb4c-120">Related topics</span></span>](#related-topics)

## <a name="ui-automation-and-the-ui-thread"></a><span data-ttu-id="1bb4c-121">Automação da interface do usuário e thread da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="1bb4c-121">UI Automation and the UI Thread</span></span>

<span data-ttu-id="1bb4c-122">Devido à maneira como a automação da interface do usuário usa mensagens do Windows, os conflitos podem ocorrer quando um aplicativo cliente tenta interagir com sua própria interface do usuário no thread da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="1bb4c-122">Because of the way UI Automation uses Windows messages, conflicts can occur when a client application attempts to interact with its own UI on the UI thread.</span></span> <span data-ttu-id="1bb4c-123">Esses conflitos podem levar a um desempenho muito lento ou até mesmo fazer com que o aplicativo pare de responder.</span><span class="sxs-lookup"><span data-stu-id="1bb4c-123">These conflicts can lead to very slow performance, or even cause the application to stop responding.</span></span>

<span data-ttu-id="1bb4c-124">Se o seu aplicativo cliente se destina a interagir com todos os elementos na área de trabalho, incluindo sua própria interface do usuário, você deve fazer todas as chamadas de automação da interface do usuário de um thread separado.</span><span class="sxs-lookup"><span data-stu-id="1bb4c-124">If your client application is intended to interact with all elements on the desktop, including its own UI, you should make all UI Automation calls from a separate thread.</span></span> <span data-ttu-id="1bb4c-125">Isso inclui a localização de elementos, por exemplo, usando [**IUIAutomationTreeWalker**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtreewalker) ou o método [**IUIAutomationElement:: FindAll**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findall) e o uso de padrões de controle.</span><span class="sxs-lookup"><span data-stu-id="1bb4c-125">This includes locating elements, for example, by using [**IUIAutomationTreeWalker**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtreewalker) or the [**IUIAutomationElement::FindAll**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findall) method and using control patterns.</span></span> <span data-ttu-id="1bb4c-126">Esse thread não deve possuir nenhuma janela e deve ser um thread de modelo MTA (multithreaded apartment) Component Object Model (COM) (um que inicializa o COM chamando [CoInitializeEx](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) com o sinalizador **coinit \_ multi-threaded** .)</span><span class="sxs-lookup"><span data-stu-id="1bb4c-126">This thread should not own any windows, and should be a Component Object Model (COM) Multithreaded Apartment (MTA) model thread (one that initializes COM by calling [CoInitializeEx](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) with the **COINIT\_MULTITHREADED** flag.)</span></span>

<span data-ttu-id="1bb4c-127">É seguro fazer chamadas de automação da interface do usuário em um manipulador de eventos de automação da interface do usuário, pois o manipulador de eventos é sempre chamado em um thread que não seja da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="1bb4c-127">It is safe to make UI Automation calls in a UI Automation event handler, because the event handler is always called on a non-UI thread.</span></span> <span data-ttu-id="1bb4c-128">No entanto, ao assinar eventos que podem se originar da interface do usuário do aplicativo cliente, você deve fazer a chamada para [**IUIAutomation:: AddAutomationEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addautomationeventhandler)ou um método relacionado, em um thread que não seja de interface do usuário (que também deve ser um thread MTA).</span><span class="sxs-lookup"><span data-stu-id="1bb4c-128">However, when subscribing to events that may originate from your client application UI, you must make the call to [**IUIAutomation::AddAutomationEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addautomationeventhandler), or a related method, on a non-UI thread (which should also be an MTA thread).</span></span> <span data-ttu-id="1bb4c-129">Remova os manipuladores de eventos no mesmo thread.</span><span class="sxs-lookup"><span data-stu-id="1bb4c-129">Remove event handlers on the same thread.</span></span>

<span data-ttu-id="1bb4c-130">Um cliente de automação de interface do usuário não deve usar vários threads para adicionar ou remover manipuladores de eventos.</span><span class="sxs-lookup"><span data-stu-id="1bb4c-130">A UI Automation client should not use multiple threads to add or remove event handlers.</span></span> <span data-ttu-id="1bb4c-131">Um comportamento inesperado pode ocorrer se um manipulador de eventos estiver sendo adicionado ou removido enquanto outro estiver sendo adicionado ou removido no mesmo processo de cliente.</span><span class="sxs-lookup"><span data-stu-id="1bb4c-131">Unexpected behavior can result if one event handler is being added or removed while another is being added or removed in the same client process.</span></span>

## <a name="threading-model-for-event-handlers"></a><span data-ttu-id="1bb4c-132">Modelo de threading para manipuladores de eventos</span><span class="sxs-lookup"><span data-stu-id="1bb4c-132">Threading Model for Event Handlers</span></span>

<span data-ttu-id="1bb4c-133">Um cliente de automação de interface do usuário deve usar o modelo de Threading do MTA COM para threads que implementam manipuladores de eventos.</span><span class="sxs-lookup"><span data-stu-id="1bb4c-133">A UI Automation client should use the COM MTA threading model for threads that implement event handlers.</span></span> <span data-ttu-id="1bb4c-134">O uso do modelo STA (single-threaded apartment) pode causar problemas como, por exemplo, impedir que os clientes removam manipuladores de eventos do thread.</span><span class="sxs-lookup"><span data-stu-id="1bb4c-134">Using the Single-threaded Apartment (STA) model can cause problems such as preventing clients from removing event handlers from the thread.</span></span>

## <a name="com-apartment-affinity-on-64-bit-windows"></a><span data-ttu-id="1bb4c-135">Afinidade de apartamento COM em Windows de 64 bits</span><span class="sxs-lookup"><span data-stu-id="1bb4c-135">COM Apartment Affinity on 64-bit Windows</span></span>

<span data-ttu-id="1bb4c-136">De acordo com a especificação COM, o tempo de vida de um objeto remoto é regido pelo tempo de vida do apartamento em que a função [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) é chamada para criar o objeto.</span><span class="sxs-lookup"><span data-stu-id="1bb4c-136">According to the COM specification, the lifetime of a remote object is governed by the lifetime of the apartment where the [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) function is called to create the object.</span></span> <span data-ttu-id="1bb4c-137">Quando o apartamento original é desligado, o objeto remoto também é liberado.</span><span class="sxs-lookup"><span data-stu-id="1bb4c-137">When the original apartment shuts down, the remote object is also released.</span></span>

<span data-ttu-id="1bb4c-138">Para clientes de automação da interface do usuário, esse comportamento de COM pode significar que o tempo de vida do auxiliar remoto 32/64 (criado por UIAutomationCore.dll) usado por um elemento de 32 bits é regido pelo tempo de vida do apartamento do thread que criou o elemento.</span><span class="sxs-lookup"><span data-stu-id="1bb4c-138">For UI Automation clients, this COM behavior can mean that the lifetime of the remote 32/64 helper (created by UIAutomationCore.dll) used by a 32-bit element is governed by the apartment lifetime of the thread that created the element.</span></span> <span data-ttu-id="1bb4c-139">Se o cliente de automação da interface do usuário realizar marshaling do elemento para outro thread, o elemento poderá se tornar invalidado quando o apartamento de origem for desligado.</span><span class="sxs-lookup"><span data-stu-id="1bb4c-139">If the UI Automation client marshals the element to another thread, the element can become invalidated when the originating apartment shuts down.</span></span> <span data-ttu-id="1bb4c-140">O cliente de automação da interface do usuário deve lidar com esses problemas normalmente Capturando erros ao usar elementos de automação empacotados.</span><span class="sxs-lookup"><span data-stu-id="1bb4c-140">The UI Automation client should handle these issues gracefully by catching errors while using marshaled automation elements.</span></span>

<span data-ttu-id="1bb4c-141">O mesmo problema pode ocorrer com um cliente de automação de interface do usuário de 32 bits que tem elementos de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="1bb4c-141">The same issue can occur with a 32-bit UI Automation client that has 64-bit elements.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1bb4c-142">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1bb4c-142">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="1bb4c-143">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="1bb4c-143">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="1bb4c-144">Obtendo elementos da automação interface do usuário</span><span class="sxs-lookup"><span data-stu-id="1bb4c-144">Obtaining UI Automation Elements</span></span>](uiauto-obtainingelements.md)
</dt> <dt>

[<span data-ttu-id="1bb4c-145">Inscrevendo-se em eventos de automação da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="1bb4c-145">Subscribing to UI Automation Events</span></span>](uiauto-eventsforclients.md)
</dt> <dt>

[<span data-ttu-id="1bb4c-146">Visão geral sobre eventos de automação de interface do usuário</span><span class="sxs-lookup"><span data-stu-id="1bb4c-146">UI Automation Events Overview</span></span>](uiauto-eventsoverview.md)
</dt> <dt>

<span data-ttu-id="1bb4c-147">**Outros recursos**</span><span class="sxs-lookup"><span data-stu-id="1bb4c-147">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="1bb4c-148">INFORMAÇÕES: descrições e trabalho de modelos de Threading OLE</span><span class="sxs-lookup"><span data-stu-id="1bb4c-148">INFO: Descriptions and Workings of OLE Threading Models</span></span>](https://support.microsoft.com/kb/150777)
</dt> </dl>

 

 