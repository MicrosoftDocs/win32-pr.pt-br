---
description: O processo de captura é o mesmo para cada uma das quatro interfaces NPP.
ms.assetid: f778aba5-8f66-4fc9-830b-f830c364da56
title: O processo de captura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e0ca1987266b7e042713f1d1c292cf63d5e3ccf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104569186"
---
# <a name="the-capture-process"></a><span data-ttu-id="11149-103">O processo de captura</span><span class="sxs-lookup"><span data-stu-id="11149-103">The Capture Process</span></span>

<span data-ttu-id="11149-104">O processo de captura é o mesmo para cada uma das quatro interfaces NPP.</span><span class="sxs-lookup"><span data-stu-id="11149-104">The capture process is the same for each of the four NPP interfaces.</span></span> <span data-ttu-id="11149-105">Em cada caso, o processo inclui:</span><span class="sxs-lookup"><span data-stu-id="11149-105">In each case, the process includes:</span></span>

-   <span data-ttu-id="11149-106">Obtendo o objeto de interface NPP a ser usado</span><span class="sxs-lookup"><span data-stu-id="11149-106">Obtaining the NPP interface object to use</span></span>
-   <span data-ttu-id="11149-107">Conectando-se à rede</span><span class="sxs-lookup"><span data-stu-id="11149-107">Connecting to the network</span></span>
-   <span data-ttu-id="11149-108">Iniciando e, em seguida, parando a [ *captura*](c.md)</span><span class="sxs-lookup"><span data-stu-id="11149-108">Starting and then stopping the [*capture*](c.md)</span></span>
-   <span data-ttu-id="11149-109">Desconectando da rede</span><span class="sxs-lookup"><span data-stu-id="11149-109">Disconnecting from the network</span></span>

> [!Note]  
> <span data-ttu-id="11149-110">Ao obter o objeto de interface que você deseja, certifique-se de chamar apenas os métodos incluídos nessa interface.</span><span class="sxs-lookup"><span data-stu-id="11149-110">When you obtain the interface object that you want, ensure you call only the methods included in that interface.</span></span> <span data-ttu-id="11149-111">A ilustração a seguir mostra que cada interface fornece métodos semelhantes para capturar dados de rede.</span><span class="sxs-lookup"><span data-stu-id="11149-111">The following illustration shows each interface provides similar methods for capturing network data.</span></span> <span data-ttu-id="11149-112">Um erro será retornado se você se conectar à rede com uma interface e, em seguida, tentar executar uma captura usando os métodos de outra interface.</span><span class="sxs-lookup"><span data-stu-id="11149-112">An error is returned if you connect to the network with one interface and then try to run a capture using the methods from another interface.</span></span>

 

<span data-ttu-id="11149-113">As ilustrações a seguir mostram duas maneiras diferentes de executar uma captura.</span><span class="sxs-lookup"><span data-stu-id="11149-113">The following illustrations show two different ways you could run a capture.</span></span> <span data-ttu-id="11149-114">A primeira ilustração mostra como executar uma ou mais capturas sequenciais, permitindo que você crie qualquer número de capturas independentes.</span><span class="sxs-lookup"><span data-stu-id="11149-114">The first illustration shows how to run one or more sequential captures, allowing you to create any number of independent captures.</span></span>

![captura sequencial](images/capt1.png)

<span data-ttu-id="11149-116">Conforme mostrado acima, depois de se conectar à rede, você pode iniciar e parar uma captura quantas vezes desejar, iniciando uma nova captura e gerando novas estatísticas toda vez que reiniciar a captura.</span><span class="sxs-lookup"><span data-stu-id="11149-116">As shown above, after you connect to the network you can start and stop a capture as many times as you wish, starting a new capture and generating new statistics every time you restart the capture.</span></span> <span data-ttu-id="11149-117">Por exemplo, para uma captura atrasada usando a interface [**IDelaydC**](idelaydc.md) , um novo [*arquivo de captura*](c.md) será criado cada vez que a captura for reiniciada.</span><span class="sxs-lookup"><span data-stu-id="11149-117">For example, for a delayed capture using the [**IDelaydC**](idelaydc.md) interface, a new [*capture file*](c.md) would be created each time you restarted the capture.</span></span>

<span data-ttu-id="11149-118">No entanto, também esteja ciente de que sempre que reiniciar o processo de captura, você deverá chamar o método configure apropriado para reconfigurar a conexão.</span><span class="sxs-lookup"><span data-stu-id="11149-118">However, also be aware that every time you restart the capture process you must call the appropriate configure method to reconfigure the connection.</span></span> <span data-ttu-id="11149-119">Para a chamada inicial para iniciar a captura, a conexão é configurada pela chamada para conectar-se à rede.</span><span class="sxs-lookup"><span data-stu-id="11149-119">For the initial call to start the capture, the connection is configured by the call to connect to the network.</span></span>

<span data-ttu-id="11149-120">A segunda ilustração mostra como você pode executar uma única captura Pausando e reiniciando.</span><span class="sxs-lookup"><span data-stu-id="11149-120">The second illustration shows how you could run a single capture by pausing and restarting.</span></span>

![captura única Pausando e reiniciando](images/capt2.png)

<span data-ttu-id="11149-122">Nesse caso, você pode pausar e reiniciar uma captura quantas vezes desejar.</span><span class="sxs-lookup"><span data-stu-id="11149-122">In this case, you can pause and restart a capture as many times as you want.</span></span> <span data-ttu-id="11149-123">Com essa abordagem, você pode executar uma captura cujos dados (e suas estatísticas relacionadas) são registrados como uma única captura.</span><span class="sxs-lookup"><span data-stu-id="11149-123">With this approach, you can run a capture whose data (and its related statistics) are recorded as a single capture.</span></span> <span data-ttu-id="11149-124">Por exemplo, para executar uma captura atrasada usando a interface [**IDelaydC**](idelaydc.md) , todas as informações de rede capturadas seriam salvas em um único [*arquivo de captura*](c.md).</span><span class="sxs-lookup"><span data-stu-id="11149-124">For example, to perform a delayed capture using the [**IDelaydC**](idelaydc.md) interface, all the captured network information would be saved in a single [*capture file*](c.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="11149-125">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="11149-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="11149-126">**CreateNPPInterface**</span><span class="sxs-lookup"><span data-stu-id="11149-126">**CreateNPPInterface**</span></span>](createnppinterface.md)
</dt> <dt>

[<span data-ttu-id="11149-127">**IDelaydC:: configurar**</span><span class="sxs-lookup"><span data-stu-id="11149-127">**IDelaydC::Configure**</span></span>](idelaydc-configure.md)
</dt> <dt>

[<span data-ttu-id="11149-128">**IDelaydC:: conectar**</span><span class="sxs-lookup"><span data-stu-id="11149-128">**IDelaydC::Connect**</span></span>](idelaydc-connect.md)
</dt> <dt>

[<span data-ttu-id="11149-129">**IDelaydC::D isconnect**</span><span class="sxs-lookup"><span data-stu-id="11149-129">**IDelaydC::Disconnect**</span></span>](idelaydc-disconnect.md)
</dt> <dt>

[<span data-ttu-id="11149-130">**IDelaydC::P ause**</span><span class="sxs-lookup"><span data-stu-id="11149-130">**IDelaydC::Pause**</span></span>](idelaydc-pause.md)
</dt> <dt>

[<span data-ttu-id="11149-131">**IDelaydC:: retomar**</span><span class="sxs-lookup"><span data-stu-id="11149-131">**IDelaydC::Resume**</span></span>](idelaydc-resume.md)
</dt> <dt>

[<span data-ttu-id="11149-132">**IDelaydC:: iniciar**</span><span class="sxs-lookup"><span data-stu-id="11149-132">**IDelaydC::Start**</span></span>](idelaydc-start.md)
</dt> <dt>

[<span data-ttu-id="11149-133">**IDelaydC:: Stop**</span><span class="sxs-lookup"><span data-stu-id="11149-133">**IDelaydC::Stop**</span></span>](idelaydc-stop.md)
</dt> <dt>

[<span data-ttu-id="11149-134">**IESP:: configurar**</span><span class="sxs-lookup"><span data-stu-id="11149-134">**IESP::Configure**</span></span>](iesp-configure.md)
</dt> <dt>

[<span data-ttu-id="11149-135">**IESP:: conectar**</span><span class="sxs-lookup"><span data-stu-id="11149-135">**IESP::Connect**</span></span>](iesp-connect.md)
</dt> <dt>

[<span data-ttu-id="11149-136">**IESP::D isconnect**</span><span class="sxs-lookup"><span data-stu-id="11149-136">**IESP::Disconnect**</span></span>](iesp-disconnect.md)
</dt> <dt>

[<span data-ttu-id="11149-137">**IESP::P ause**</span><span class="sxs-lookup"><span data-stu-id="11149-137">**IESP::Pause**</span></span>](iesp-pause.md)
</dt> <dt>

[<span data-ttu-id="11149-138">**IESP:: retomar**</span><span class="sxs-lookup"><span data-stu-id="11149-138">**IESP::Resume**</span></span>](iesp-resume.md)
</dt> <dt>

[<span data-ttu-id="11149-139">**IESP:: iniciar**</span><span class="sxs-lookup"><span data-stu-id="11149-139">**IESP::Start**</span></span>](iesp-start.md)
</dt> <dt>

[<span data-ttu-id="11149-140">**IESP:: Stop**</span><span class="sxs-lookup"><span data-stu-id="11149-140">**IESP::Stop**</span></span>](iesp-stop.md)
</dt> <dt>

[<span data-ttu-id="11149-141">**IRTC:: configurar**</span><span class="sxs-lookup"><span data-stu-id="11149-141">**IRTC::Configure**</span></span>](irtc-configure.md)
</dt> <dt>

[<span data-ttu-id="11149-142">**IRTC:: conectar**</span><span class="sxs-lookup"><span data-stu-id="11149-142">**IRTC::Connect**</span></span>](irtc-connect.md)
</dt> <dt>

[<span data-ttu-id="11149-143">**IRTC::D isconnect**</span><span class="sxs-lookup"><span data-stu-id="11149-143">**IRTC::Disconnect**</span></span>](irtc-disconnect.md)
</dt> <dt>

[<span data-ttu-id="11149-144">**IRTC::P ause**</span><span class="sxs-lookup"><span data-stu-id="11149-144">**IRTC::Pause**</span></span>](irtc-pause.md)
</dt> <dt>

[<span data-ttu-id="11149-145">**IRTC:: retomar**</span><span class="sxs-lookup"><span data-stu-id="11149-145">**IRTC::Resume**</span></span>](irtc-resume.md)
</dt> <dt>

[<span data-ttu-id="11149-146">**IRTC:: iniciar**</span><span class="sxs-lookup"><span data-stu-id="11149-146">**IRTC::Start**</span></span>](irtc-start.md)
</dt> <dt>

[<span data-ttu-id="11149-147">**IRTC:: Stop**</span><span class="sxs-lookup"><span data-stu-id="11149-147">**IRTC::Stop**</span></span>](irtc-stop.md)
</dt> <dt>

[<span data-ttu-id="11149-148">**IStats:: configurar**</span><span class="sxs-lookup"><span data-stu-id="11149-148">**IStats::Configure**</span></span>](istats-configure.md)
</dt> <dt>

[<span data-ttu-id="11149-149">**IStats:: conectar**</span><span class="sxs-lookup"><span data-stu-id="11149-149">**IStats::Connect**</span></span>](istats-connect.md)
</dt> <dt>

[<span data-ttu-id="11149-150">**IStats::D isconnect**</span><span class="sxs-lookup"><span data-stu-id="11149-150">**IStats::Disconnect**</span></span>](istats-disconnect.md)
</dt> <dt>

[<span data-ttu-id="11149-151">**IStats::P ause**</span><span class="sxs-lookup"><span data-stu-id="11149-151">**IStats::Pause**</span></span>](istats-pause.md)
</dt> <dt>

[<span data-ttu-id="11149-152">**IStats:: retomar**</span><span class="sxs-lookup"><span data-stu-id="11149-152">**IStats::Resume**</span></span>](istats-resume.md)
</dt> <dt>

[<span data-ttu-id="11149-153">**IStats:: iniciar**</span><span class="sxs-lookup"><span data-stu-id="11149-153">**IStats::Start**</span></span>](istats-start.md)
</dt> <dt>

[<span data-ttu-id="11149-154">**IStats:: Stop**</span><span class="sxs-lookup"><span data-stu-id="11149-154">**IStats::Stop**</span></span>](istats-stop.md)
</dt> </dl>

 

 



