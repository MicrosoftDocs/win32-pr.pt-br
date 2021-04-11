---
title: Compartimentos
description: Compartimentos
ms.assetid: 7bffab6f-be40-4d3a-9342-6f81557a9656
keywords:
- TSF (estrutura de serviços de texto), compartimentos
- TSF (estrutura de serviços de texto), compartimentos
- serviços de texto, compartimentos
- Aplicativos habilitados para TSF, compartimentos
- compartimentos
- TSF (estrutura de serviços de texto), tipos de compartimentos
- TSF (estrutura de serviços de texto), tipos de compartimentos
- serviços de texto, tipos de compartimentos
- Aplicativos habilitados para TSF, tipos de compartimentos
- tipos de compartimentos
- TSF (estrutura de serviços de texto), notificações de alteração de compartimento
- TSF (estrutura de serviços de texto), notificações de alteração de compartimento
- serviços de texto, notificações de alteração de compartimento
- Aplicativos habilitados para TSF, notificações de alteração de compartimento
- notificações de alteração de compartimento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76636c684ee74f7e452b5602ebfd59d6d1947b0f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159568"
---
# <a name="compartments"></a><span data-ttu-id="beebb-118">Compartimentos</span><span class="sxs-lookup"><span data-stu-id="beebb-118">Compartments</span></span>

## <a name="compartment-types"></a><span data-ttu-id="beebb-119">Tipos de compartimentos</span><span class="sxs-lookup"><span data-stu-id="beebb-119">Compartment Types</span></span>

<span data-ttu-id="beebb-120">Há vários tipos diferentes de compartimentos.</span><span class="sxs-lookup"><span data-stu-id="beebb-120">There are several different types of compartments.</span></span> <span data-ttu-id="beebb-121">Há um compartimento global, e cada Gerenciador de threads, o Gerenciador de documentos e o contexto podem conter um compartimento.</span><span class="sxs-lookup"><span data-stu-id="beebb-121">There is a global compartment, and each thread manager, document manager, and context can contain a compartment.</span></span>

<span data-ttu-id="beebb-122">O compartimento global permite que os clientes compartilhem dados entre processos.</span><span class="sxs-lookup"><span data-stu-id="beebb-122">The global compartment enables clients to share data across processes.</span></span> <span data-ttu-id="beebb-123">Para obter o Gerenciador de compartimento global, chame [**ITfThreadMgr:: GetGlobalCompartment**](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-getglobalcompartment).</span><span class="sxs-lookup"><span data-stu-id="beebb-123">To obtain the global compartment manager, call [**ITfThreadMgr::GetGlobalCompartment**](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-getglobalcompartment).</span></span>

<span data-ttu-id="beebb-124">O Gerenciador de threads contém um Gerenciador de compartimentos que contém as compartimentos por thread.</span><span class="sxs-lookup"><span data-stu-id="beebb-124">The thread manager contains a compartment manager that contains compartments on a per-thread basis.</span></span> <span data-ttu-id="beebb-125">Isso permite que os dados sejam compartilhados em um thread.</span><span class="sxs-lookup"><span data-stu-id="beebb-125">This allows data to be shared within a thread.</span></span> <span data-ttu-id="beebb-126">Para obter um Gerenciador de compartimentos do Gerenciador de threads, chame **ITfThreadMgr:: QueryInterface** com \_ ITfCompartmentMgr IID.</span><span class="sxs-lookup"><span data-stu-id="beebb-126">To obtain a thread manager compartment manager, call **ITfThreadMgr::QueryInterface** with IID\_ITfCompartmentMgr.</span></span>

<span data-ttu-id="beebb-127">Cada Gerenciador de documentos criado também contém um Gerenciador de compartimentos.</span><span class="sxs-lookup"><span data-stu-id="beebb-127">Each document manager created also contains a compartment manager.</span></span> <span data-ttu-id="beebb-128">Isso permite que os dados sejam compartilhados em um gerente de documento específico.</span><span class="sxs-lookup"><span data-stu-id="beebb-128">This allows data to be shared within a specific document manager.</span></span> <span data-ttu-id="beebb-129">Para obter o Gerenciador de compartimento do Gerenciador de documentos, chame **ITfDocumentMgr:: QueryInterface** com \_ ITfCompartmentMgr IID.</span><span class="sxs-lookup"><span data-stu-id="beebb-129">To obtain the document manager compartment manager, call **ITfDocumentMgr::QueryInterface** with IID\_ITfCompartmentMgr.</span></span>

<span data-ttu-id="beebb-130">Cada contexto criado também contém um Gerenciador de compartimentos.</span><span class="sxs-lookup"><span data-stu-id="beebb-130">Each context created also contains a compartment manager.</span></span> <span data-ttu-id="beebb-131">Isso permite que os dados sejam compartilhados em um contexto específico.</span><span class="sxs-lookup"><span data-stu-id="beebb-131">This allows data to be shared within a specific context.</span></span> <span data-ttu-id="beebb-132">Para obter um Gerenciador de compartimento de contexto, chame **ITfContext:: QueryInterface** com \_ ITfCompartmentMgr IID.</span><span class="sxs-lookup"><span data-stu-id="beebb-132">To obtain a context compartment manager, call **ITfContext::QueryInterface** with IID\_ITfCompartmentMgr.</span></span>

## <a name="creating-and-deleting-a-compartment"></a><span data-ttu-id="beebb-133">Criando e excluindo um compartimento</span><span class="sxs-lookup"><span data-stu-id="beebb-133">Creating and Deleting a Compartment</span></span>

<span data-ttu-id="beebb-134">Um compartimento é criado na primeira vez que [**ITfCompartmentMgr:: getcompartmentid**](/windows/desktop/api/Msctf/nf-msctf-itfcompartmentmgr-getcompartment) é chamado com o GUID do compartimento.</span><span class="sxs-lookup"><span data-stu-id="beebb-134">A compartment is created the first time [**ITfCompartmentMgr::GetCompartment**](/windows/desktop/api/Msctf/nf-msctf-itfcompartmentmgr-getcompartment) is called with the compartment GUID.</span></span> <span data-ttu-id="beebb-135">O cliente de instalação deve definir o valor inicial do compartimento usando [**ITfCompartment:: SetValue**](/windows/desktop/api/Msctf/nf-msctf-itfcompartment-setvalue).</span><span class="sxs-lookup"><span data-stu-id="beebb-135">The installing client should set the initial value of the compartment using [**ITfCompartment::SetValue**](/windows/desktop/api/Msctf/nf-msctf-itfcompartment-setvalue).</span></span> <span data-ttu-id="beebb-136">Até que um valor seja definido, o valor do compartimento estará vazio.</span><span class="sxs-lookup"><span data-stu-id="beebb-136">Until a value is set, the compartment value is empty.</span></span> <span data-ttu-id="beebb-137">Por isso, não é possível verificar se o compartimento existia antes que **getcompartmentid** fosse chamado.</span><span class="sxs-lookup"><span data-stu-id="beebb-137">Because of this, there is no way to verify that the compartment existed before **GetCompartment** was called.</span></span> <span data-ttu-id="beebb-138">Para evitar essa situação, o cliente de instalação deve definir o valor como um valor inicial para que outros clientes possam determinar se o compartimento já existe.</span><span class="sxs-lookup"><span data-stu-id="beebb-138">To avoid this situation, the installing client should set the value to some initial value so that other clients can determine if the compartment already exists.</span></span>

<span data-ttu-id="beebb-139">O método [**ITfCompartmentMgr:: ClearCompartment**](/windows/desktop/api/Msctf/nf-msctf-itfcompartmentmgr-clearcompartment) é usado para remover um compartimento.</span><span class="sxs-lookup"><span data-stu-id="beebb-139">The [**ITfCompartmentMgr::ClearCompartment**](/windows/desktop/api/Msctf/nf-msctf-itfcompartmentmgr-clearcompartment) method is used to remove a compartment.</span></span> <span data-ttu-id="beebb-140">Todas as referências existentes ao compartimento são marcadas como inválidas.</span><span class="sxs-lookup"><span data-stu-id="beebb-140">Any existing references to the compartment are marked invalid.</span></span>

## <a name="obtaining-compartments"></a><span data-ttu-id="beebb-141">Obtendo compartimentos</span><span class="sxs-lookup"><span data-stu-id="beebb-141">Obtaining Compartments</span></span>

<span data-ttu-id="beebb-142">Usando a interface [**ITfCompartmentMgr**](/windows/desktop/api/Msctf/nn-msctf-itfcompartmentmgr) , um cliente pode enumerar compartimentos chamando [**ITfCompartmentMgr:: EnumCompartments**](/windows/desktop/api/Msctf/nf-msctf-itfcompartmentmgr-enumcompartments).</span><span class="sxs-lookup"><span data-stu-id="beebb-142">Using the [**ITfCompartmentMgr**](/windows/desktop/api/Msctf/nn-msctf-itfcompartmentmgr) interface, a client can enumerate compartments by calling [**ITfCompartmentMgr::EnumCompartments**](/windows/desktop/api/Msctf/nf-msctf-itfcompartmentmgr-enumcompartments).</span></span> <span data-ttu-id="beebb-143">Esse método fornece um objeto **IEnumGUID** que contém os GUIDs de todos os compartimentos instalados.</span><span class="sxs-lookup"><span data-stu-id="beebb-143">This method provides an **IEnumGUID** object that contains the GUIDs of all of the installed compartments.</span></span>

<span data-ttu-id="beebb-144">Usando o GUID do compartimento, **ITfCompartmentMgr:: getcompartmentid** é usado para obter um compartimento específico.</span><span class="sxs-lookup"><span data-stu-id="beebb-144">Using the compartment GUID , **ITfCompartmentMgr::GetCompartment** is used to obtain a specific compartment.</span></span> <span data-ttu-id="beebb-145">Esse método fornece ao chamador um objeto [**ITfCompartment**](/windows/desktop/api/Msctf/nn-msctf-itfcompartment) que pode obter e definir os dados do compartimento.</span><span class="sxs-lookup"><span data-stu-id="beebb-145">This method provides the caller with an [**ITfCompartment**](/windows/desktop/api/Msctf/nn-msctf-itfcompartment) object that can obtain and set the compartment data.</span></span>

## <a name="receiving-compartment-change-notifications"></a><span data-ttu-id="beebb-146">Recebendo notificações de alteração de compartimento</span><span class="sxs-lookup"><span data-stu-id="beebb-146">Receiving Compartment Change Notifications</span></span>

<span data-ttu-id="beebb-147">Quando o valor de um compartimento é alterado, o Gerenciador de TSF notifica todos os coletores de aviso instalados de que o compartimento foi alterado.</span><span class="sxs-lookup"><span data-stu-id="beebb-147">When the value of a compartment changes, the TSF manager notifies any installed advise sinks that the compartment has changed.</span></span> <span data-ttu-id="beebb-148">Para instalar um coletor de aviso de alteração de compartimento, crie um objeto que implemente [**ITfCompartmentEventSink**](/windows/desktop/api/Msctf/nn-msctf-itfcompartmenteventsink).</span><span class="sxs-lookup"><span data-stu-id="beebb-148">To install a compartment change advise sink, create an object that implements [**ITfCompartmentEventSink**](/windows/desktop/api/Msctf/nn-msctf-itfcompartmenteventsink).</span></span> <span data-ttu-id="beebb-149">Em seguida, chame **ITfCompartment:: QueryInterface** com ITFSOURCE de IID \_ no objeto de compartimento a ser monitorado para obter uma interface [**ITfSource**](/windows/desktop/api/Msctf/nn-msctf-itfsource) .</span><span class="sxs-lookup"><span data-stu-id="beebb-149">Then call **ITfCompartment::QueryInterface** with IID\_ITfSource on the compartment object to be monitored to obtain an [**ITfSource**](/windows/desktop/api/Msctf/nn-msctf-itfsource) interface.</span></span> <span data-ttu-id="beebb-150">Agora, chame [**ITfSource:: AdviseSink**](/windows/desktop/api/Msctf/nf-msctf-itfsource-advisesink) com IID \_ ITfCompartmentEventSink e o ponteiro para o objeto **ITfCompartmentEventSink** .</span><span class="sxs-lookup"><span data-stu-id="beebb-150">Now call [**ITfSource::AdviseSink**](/windows/desktop/api/Msctf/nf-msctf-itfsource-advisesink) with IID\_ITfCompartmentEventSink and the pointer to the **ITfCompartmentEventSink** object.</span></span> <span data-ttu-id="beebb-151">Quando o valor do compartimento é alterado, o [**ITfCompartmentEventSink:: OnChange**](/windows/desktop/api/Msctf/nf-msctf-itfcompartmenteventsink-onchange) do coletor de aviso é chamado com o GUID do compartimento.</span><span class="sxs-lookup"><span data-stu-id="beebb-151">When the value of the compartment changes, the advise sink's [**ITfCompartmentEventSink::OnChange**](/windows/desktop/api/Msctf/nf-msctf-itfcompartmenteventsink-onchange) is called with the GUID of the compartment.</span></span> <span data-ttu-id="beebb-152">O coletor de aviso pode chamar [**ITfCompartment:: GetValue**](/windows/desktop/api/Msctf/nf-msctf-itfcompartment-getvalue) para obter o novo valor.</span><span class="sxs-lookup"><span data-stu-id="beebb-152">The advise sink can call [**ITfCompartment::GetValue**](/windows/desktop/api/Msctf/nf-msctf-itfcompartment-getvalue) to obtain the new value.</span></span>

## <a name="related-topics"></a><span data-ttu-id="beebb-153">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="beebb-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="beebb-154">**ITfCompartmentMgr**</span><span class="sxs-lookup"><span data-stu-id="beebb-154">**ITfCompartmentMgr**</span></span>](/windows/desktop/api/Msctf/nn-msctf-itfcompartmentmgr)
</dt> <dt>

[<span data-ttu-id="beebb-155">**ITfCompartment**</span><span class="sxs-lookup"><span data-stu-id="beebb-155">**ITfCompartment**</span></span>](/windows/desktop/api/Msctf/nn-msctf-itfcompartment)
</dt> <dt>

[<span data-ttu-id="beebb-156">**ITfCompartmentEventSink**</span><span class="sxs-lookup"><span data-stu-id="beebb-156">**ITfCompartmentEventSink**</span></span>](/windows/desktop/api/Msctf/nn-msctf-itfcompartmenteventsink)
</dt> <dt>

[<span data-ttu-id="beebb-157">**TfClientId**</span><span class="sxs-lookup"><span data-stu-id="beebb-157">**TfClientId**</span></span>](tfclientid.md)
</dt> <dt>

[<span data-ttu-id="beebb-158">**ITfThreadMgr::GetGlobalCompartment**</span><span class="sxs-lookup"><span data-stu-id="beebb-158">**ITfThreadMgr::GetGlobalCompartment**</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-getglobalcompartment)
</dt> <dt>

[<span data-ttu-id="beebb-159">**ITfCompartmentMgr:: getcompartmentid**</span><span class="sxs-lookup"><span data-stu-id="beebb-159">**ITfCompartmentMgr::GetCompartment**</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcompartmentmgr-getcompartment)
</dt> <dt>

[<span data-ttu-id="beebb-160">**ITfCompartment:: SetValue**</span><span class="sxs-lookup"><span data-stu-id="beebb-160">**ITfCompartment::SetValue**</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcompartment-setvalue)
</dt> <dt>

[<span data-ttu-id="beebb-161">**ITfCompartmentMgr::ClearCompartment**</span><span class="sxs-lookup"><span data-stu-id="beebb-161">**ITfCompartmentMgr::ClearCompartment**</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcompartmentmgr-clearcompartment)
</dt> <dt>

[<span data-ttu-id="beebb-162">**ITfCompartmentMgr::EnumCompartments**</span><span class="sxs-lookup"><span data-stu-id="beebb-162">**ITfCompartmentMgr::EnumCompartments**</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcompartmentmgr-enumcompartments)
</dt> <dt>

[<span data-ttu-id="beebb-163">**ITfSource**</span><span class="sxs-lookup"><span data-stu-id="beebb-163">**ITfSource**</span></span>](/windows/desktop/api/Msctf/nn-msctf-itfsource)
</dt> <dt>

[<span data-ttu-id="beebb-164">**ITfSource:: AdviseSink**</span><span class="sxs-lookup"><span data-stu-id="beebb-164">**ITfSource::AdviseSink**</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfsource-advisesink)
</dt> <dt>

[<span data-ttu-id="beebb-165">**ITfCompartmentEventSink:: OnChange**</span><span class="sxs-lookup"><span data-stu-id="beebb-165">**ITfCompartmentEventSink::OnChange**</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcompartmenteventsink-onchange)
</dt> </dl>

 

 




