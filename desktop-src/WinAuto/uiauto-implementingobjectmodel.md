---
title: Padrão de controle ObjectModel
description: Descreve as diretrizes e convenções para implementar o IObjectModelProvider, incluindo informações sobre métodos. O padrão de controle ObjectModel é usado para expor um ponteiro para o modelo de objeto subjacente de um documento.
ms.assetid: 90A6937E-0E98-41EF-8EEB-E23CB71510E4
keywords:
- Automação da interface do usuário, implementando o padrão de controle ObjectModel
- Automação da interface do usuário, padrão de controle ObjectModel
- Automação da interface do usuário, IObjectModelProvider
- IObjectModelProvider
- Implementando o padrão de controle ObjectModel Automation UI
- Padrão de controle ObjectModel
- padrões de controle, IObjectModelProvider
- padrões de controle, implementando a automação da interface do usuário ObjectModel
- padrões de controle, ObjectModel
- interfaces, IObjectModelProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54ff115233faf19f93963153a0b2a0a1ff52c3f8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294275"
---
# <a name="objectmodel-control-pattern"></a><span data-ttu-id="8df21-114">Padrão de controle ObjectModel</span><span class="sxs-lookup"><span data-stu-id="8df21-114">ObjectModel Control Pattern</span></span>

<span data-ttu-id="8df21-115">Descreve as diretrizes e convenções para implementar o [**IObjectModelProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iobjectmodelprovider), incluindo informações sobre métodos.</span><span class="sxs-lookup"><span data-stu-id="8df21-115">Describes guidelines and conventions for implementing [**IObjectModelProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iobjectmodelprovider), including information about methods.</span></span> <span data-ttu-id="8df21-116">O padrão de controle **ObjectModel** é usado para expor um ponteiro para o modelo de objeto subjacente de um documento.</span><span class="sxs-lookup"><span data-stu-id="8df21-116">The **ObjectModel** control pattern is used to expose a pointer to the underlying object model of a document.</span></span>

<span data-ttu-id="8df21-117">Muitos aplicativos implementam modelos de objetos avançados que agregam valor além do que a automação da interface do usuário da Microsoft fornece.</span><span class="sxs-lookup"><span data-stu-id="8df21-117">Many applications implement rich object models that add value beyond what Microsoft UI Automation provides.</span></span> <span data-ttu-id="8df21-118">Esse padrão de controle permite que um cliente navegue de um elemento de automação da interface do usuário para o modelo de objeto subjacente.</span><span class="sxs-lookup"><span data-stu-id="8df21-118">This control pattern allows a client to navigate from a UI Automation element into the underlying object model.</span></span>

<span data-ttu-id="8df21-119">Este tópico inclui as seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="8df21-119">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="8df21-120">Diretrizes e convenções de implementação</span><span class="sxs-lookup"><span data-stu-id="8df21-120">Implementation Guidelines and Conventions</span></span>](#implementation-guidelines-and-conventions)
-   [<span data-ttu-id="8df21-121">Membros necessários para **IObjectModelProvider**</span><span class="sxs-lookup"><span data-stu-id="8df21-121">Required Members for **IObjectModelProvider**</span></span>](#required-members-for-iobjectmodelprovider)
-   [<span data-ttu-id="8df21-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8df21-122">Related topics</span></span>](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="8df21-123">Diretrizes e convenções de implementação</span><span class="sxs-lookup"><span data-stu-id="8df21-123">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="8df21-124">Ao implementar o padrão de controle **ObjectModel** , observe as seguintes diretrizes e convenções:</span><span class="sxs-lookup"><span data-stu-id="8df21-124">When implementing the **ObjectModel** control pattern, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="8df21-125">O método [**IObjectModelProvider:: GetUnderlyingObjectModel**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iobjectmodelprovider-getunderlyingobjectmodel) deve retornar um ponteiro para o objeto que é o mais próximo possível do elemento de interface do usuário de origem.</span><span class="sxs-lookup"><span data-stu-id="8df21-125">The [**IObjectModelProvider::GetUnderlyingObjectModel**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iobjectmodelprovider-getunderlyingobjectmodel) method should return a pointer to the object that is as close as possible to the source UI element.</span></span> <span data-ttu-id="8df21-126">Por exemplo, em um navegador da Web, um provedor de automação de interface do usuário para um único elemento deve retornar um ponteiro de modelo de objeto para o elemento.</span><span class="sxs-lookup"><span data-stu-id="8df21-126">For example, in a web browser, a UI Automation provider for a single element should return an object model pointer for the element.</span></span> <span data-ttu-id="8df21-127">Retornar um ponteiro de modelo de objeto para a raiz do documento seria muito menos útil.</span><span class="sxs-lookup"><span data-stu-id="8df21-127">Returning an object model pointer for the document root would be far less useful.</span></span>
-   <span data-ttu-id="8df21-128">Espera-se que o cliente do padrão de controle **ObjectModel** tenha o IID para a interface que ele está procurando, que é o motivo pelo qual é suficiente retornar um ponteiro simples [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="8df21-128">The client of the **ObjectModel** control pattern is expected to have the IID for the interface they are seeking, which is why it is enough to return a simple [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) pointer.</span></span>
-   <span data-ttu-id="8df21-129">Como a automação da interface do usuário realiza marshaling do ponteiro para o processo do cliente, o provedor deve esperar que o cliente acesse o modelo de objeto usando práticas COM (Standard Component Object Model).</span><span class="sxs-lookup"><span data-stu-id="8df21-129">Because UI Automation marshals the pointer to the client process, the provider should expect the client to access the object model using standard Component Object Model (COM) practices.</span></span>

## <a name="required-members-for-iobjectmodelprovider"></a><span data-ttu-id="8df21-130">Membros necessários para **IObjectModelProvider**</span><span class="sxs-lookup"><span data-stu-id="8df21-130">Required Members for **IObjectModelProvider**</span></span>

<span data-ttu-id="8df21-131">O método a seguir é necessário para implementar a interface [**IObjectModelProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iobjectmodelprovider) .</span><span class="sxs-lookup"><span data-stu-id="8df21-131">The following method is required for implementing the [**IObjectModelProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iobjectmodelprovider) interface.</span></span>



| <span data-ttu-id="8df21-132">Membros necessários</span><span class="sxs-lookup"><span data-stu-id="8df21-132">Required members</span></span>                                                                             | <span data-ttu-id="8df21-133">Tipo de membro</span><span class="sxs-lookup"><span data-stu-id="8df21-133">Member type</span></span> | <span data-ttu-id="8df21-134">Observações</span><span class="sxs-lookup"><span data-stu-id="8df21-134">Notes</span></span>                                                                                                                                                                                                   |
|----------------------------------------------------------------------------------------------|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8df21-135">**GetUnderlyingObjectModel**</span><span class="sxs-lookup"><span data-stu-id="8df21-135">**GetUnderlyingObjectModel**</span></span>](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iobjectmodelprovider-getunderlyingobjectmodel) | <span data-ttu-id="8df21-136">Método</span><span class="sxs-lookup"><span data-stu-id="8df21-136">Method</span></span>      | <span data-ttu-id="8df21-137">Retorna um ponteiro COM para o modelo de objeto subjacente.</span><span class="sxs-lookup"><span data-stu-id="8df21-137">Returns a COM pointer to the underlying object model.</span></span> <span data-ttu-id="8df21-138">Espera-se que o cliente chame o método [**IUnknown:: QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para recuperar ponteiros de modelo de objeto específicos.</span><span class="sxs-lookup"><span data-stu-id="8df21-138">The client is expected to call the [**IUnknown::QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) method to retrieve specific object model pointers.</span></span> |



 

<span data-ttu-id="8df21-139">Este padrão de controle não tem eventos associados.</span><span class="sxs-lookup"><span data-stu-id="8df21-139">This control pattern has no associated events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8df21-140">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8df21-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8df21-141">Tipos de controle e seus padrões de controle com suporte</span><span class="sxs-lookup"><span data-stu-id="8df21-141">Control Types and Their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

[<span data-ttu-id="8df21-142">Visão Geral de Padrões de Controle de Automação de Interface de Usuário</span><span class="sxs-lookup"><span data-stu-id="8df21-142">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="8df21-143">Visão geral da árvore de automação de interface do usuário</span><span class="sxs-lookup"><span data-stu-id="8df21-143">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> </dl>

 

 