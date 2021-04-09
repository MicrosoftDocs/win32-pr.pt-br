---
description: Necessidades de desempenho de usuários e administradores com aplicativos Windows Sockets (Winsock).
ms.assetid: 6c4365c6-a406-497b-a313-1faeb3e3b7f5
title: 'Necessidades de desempenho: usuários e administradores'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 009a8178cf1d7516e9c16493916f8cf911752b9b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010482"
---
# <a name="performance-needs-users-and-administrators"></a><span data-ttu-id="46d57-103">Necessidades de desempenho: usuários e administradores</span><span class="sxs-lookup"><span data-stu-id="46d57-103">Performance Needs: Users and Administrators</span></span>

<span data-ttu-id="46d57-104">Os usuários julgam o desempenho do aplicativo de acordo com sua experiência:</span><span class="sxs-lookup"><span data-stu-id="46d57-104">Users judge application performance by their experience:</span></span>

-   <span data-ttu-id="46d57-105">O aplicativo é rápido para responder?</span><span class="sxs-lookup"><span data-stu-id="46d57-105">Is the application quick to respond?</span></span>
-   <span data-ttu-id="46d57-106">Um ícone de ampulheta é exibido enquanto as operações em segundo plano são executadas?</span><span class="sxs-lookup"><span data-stu-id="46d57-106">Is an hourglass icon displayed while background operations are carried out?</span></span>
-   <span data-ttu-id="46d57-107">O aplicativo é iniciado e fechado rapidamente?</span><span class="sxs-lookup"><span data-stu-id="46d57-107">Does the application launch and close quickly?</span></span>
-   <span data-ttu-id="46d57-108">Os erros são manipulados de forma compreensível?</span><span class="sxs-lookup"><span data-stu-id="46d57-108">Are errors handled in an understandable way?</span></span>

<span data-ttu-id="46d57-109">Para resumir, os usuários querem que os aplicativos sejam rápidos e previsíveis.</span><span class="sxs-lookup"><span data-stu-id="46d57-109">To summarize, users want applications to be fast and predictable.</span></span>

<span data-ttu-id="46d57-110">Por outro lado, os administradores costumam avaliar o desempenho de um aplicativo em quão eficientemente ele usa os recursos de rede.</span><span class="sxs-lookup"><span data-stu-id="46d57-110">In contrast, administrators often judge an application's performance on how efficiently it uses network resources.</span></span> <span data-ttu-id="46d57-111">Os administradores podem perguntar:</span><span class="sxs-lookup"><span data-stu-id="46d57-111">Administrators may ask:</span></span>

-   <span data-ttu-id="46d57-112">O aplicativo tem baixa sobrecarga e um uso de rede eficiente?</span><span class="sxs-lookup"><span data-stu-id="46d57-112">Does the application have low overhead and efficient network usage?</span></span>
-   <span data-ttu-id="46d57-113">O número mínimo de conexões é usado, portanto, meu servidor pode atender o máximo possível de usuários de uma vez?</span><span class="sxs-lookup"><span data-stu-id="46d57-113">Are the minimum number of connections used, so my server can service as many users at once as possible?</span></span>
-   <span data-ttu-id="46d57-114">Estou constantemente ligando para o helpdesk?</span><span class="sxs-lookup"><span data-stu-id="46d57-114">Am I constantly calling helpdesk?</span></span>

<span data-ttu-id="46d57-115">Em suma, os administradores querem que os aplicativos sejam dimensionados.</span><span class="sxs-lookup"><span data-stu-id="46d57-115">In short, administrators want applications to scale.</span></span>

## <a name="best-practices-for-performance-needs"></a><span data-ttu-id="46d57-116">Práticas recomendadas para necessidades de desempenho</span><span class="sxs-lookup"><span data-stu-id="46d57-116">Best Practices for Performance Needs</span></span>

<span data-ttu-id="46d57-117">Ao desenvolver um aplicativo do Windows Sockets, esses requisitos de desempenho são convertidos em regras úteis.</span><span class="sxs-lookup"><span data-stu-id="46d57-117">When developing a Windows Sockets application, these performance requirements translate into useful rules.</span></span>

-   <span data-ttu-id="46d57-118">Fazer com que os aplicativos de rede sejam inicializados rapidamente.</span><span class="sxs-lookup"><span data-stu-id="46d57-118">Have network applications initialize quickly.</span></span>

    <span data-ttu-id="46d57-119">A interface do usuário não deve esperar por respostas de rede.</span><span class="sxs-lookup"><span data-stu-id="46d57-119">The user interface should not have to wait for network responses.</span></span> <span data-ttu-id="46d57-120">Algumas tarefas podem ser executadas antes que a rede esteja disponível ou sem a rede.</span><span class="sxs-lookup"><span data-stu-id="46d57-120">Some tasks can be performed before the network is available, or without the network.</span></span> <span data-ttu-id="46d57-121">Se a rede não estiver respondendo, o usuário poderá precisar da interface do usuário para operações simples, como fechar o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="46d57-121">If the network is not responding, the user may need the user interface for simple operations, such as closing the application.</span></span>

-   <span data-ttu-id="46d57-122">Não aguarde a rede ser desligada.</span><span class="sxs-lookup"><span data-stu-id="46d57-122">Do not wait for the network for shutdown.</span></span>

    <span data-ttu-id="46d57-123">Aplicativos cliente-servidor gravados corretamente tratam desconexões anuladas normalmente.</span><span class="sxs-lookup"><span data-stu-id="46d57-123">Properly written client-server applications handle abortive disconnects gracefully.</span></span> <span data-ttu-id="46d57-124">Não inicie uma operação potencialmente demorada, como sincronizar arquivos ou pastas com um servidor, que não pode ser interrompido no desligamento.</span><span class="sxs-lookup"><span data-stu-id="46d57-124">Do not initiate a potentially lengthy operation, such as synchronizing files or folders with a server, that cannot be interrupted on shutdown.</span></span> <span data-ttu-id="46d57-125">As redes não são responsivas consistentemente, portanto, até mesmo as pequenas operações poderiam provar tempo demorado.</span><span class="sxs-lookup"><span data-stu-id="46d57-125">Networks are not consistently responsive, so even small operations could prove time consuming.</span></span> <span data-ttu-id="46d57-126">Forneça comentários positivos para os usuários, incluindo indicações de progresso e tempos de conclusão estimados.</span><span class="sxs-lookup"><span data-stu-id="46d57-126">Provide positive feedback for users, including indications of progress and estimated completion times.</span></span>

-   <span data-ttu-id="46d57-127">Garanta uma interface do usuário responsiva.</span><span class="sxs-lookup"><span data-stu-id="46d57-127">Ensure a responsive user interface.</span></span>

    <span data-ttu-id="46d57-128">A capacidade de resposta do aplicativo ajuda a eliminar chamadas de helpdesk desnecessárias.</span><span class="sxs-lookup"><span data-stu-id="46d57-128">Application responsiveness helps eliminate unnecessary helpdesk calls.</span></span> <span data-ttu-id="46d57-129">Uma boa diretriz para resposta interativa é de 500 milissegundos.</span><span class="sxs-lookup"><span data-stu-id="46d57-129">A good guideline for interactive response is 500 milliseconds.</span></span> <span data-ttu-id="46d57-130">Os usuários percebem pausas por mais de 500 milissegundos como um retardo no desempenho.</span><span class="sxs-lookup"><span data-stu-id="46d57-130">Users perceive pauses longer than 500 milliseconds as a lag in performance.</span></span> <span data-ttu-id="46d57-131">Os aplicativos devem ser responsivos o suficiente para fornecer ao usuário confiança sobre o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="46d57-131">Applications should be responsive enough to provide the user with confidence about the application.</span></span>

-   <span data-ttu-id="46d57-132">Analisar erros de rede.</span><span class="sxs-lookup"><span data-stu-id="46d57-132">Scrutinize network errors.</span></span>

    <span data-ttu-id="46d57-133">Nem todos os erros de rede são críticos.</span><span class="sxs-lookup"><span data-stu-id="46d57-133">Not all network errors are critical.</span></span> <span data-ttu-id="46d57-134">Por exemplo, um aplicativo que recebeu ou postou todos os seus dados pode, provavelmente, ignorar erros ao fechar a conexão.</span><span class="sxs-lookup"><span data-stu-id="46d57-134">For example, an application that has received or posted all of its data can likely ignore errors when closing the connection.</span></span> <span data-ttu-id="46d57-135">Não presuma que a rede ou o usuário esteja disponível; Trate erros sem intervenção do usuário ou ignore-os se os erros forem não críticos.</span><span class="sxs-lookup"><span data-stu-id="46d57-135">Do not assume the network or the user is available; either handle errors without user intervention, or ignore them if errors are noncritical.</span></span>

-   <span data-ttu-id="46d57-136">Um aplicativo deve definir seus próprios tempos limite razoáveis.</span><span class="sxs-lookup"><span data-stu-id="46d57-136">An application should define its own reasonable time outs.</span></span>

    <span data-ttu-id="46d57-137">Por exemplo, uma solicitação do Windows Sockets Connect () pode bloquear em algumas condições para até 21 segundos.</span><span class="sxs-lookup"><span data-stu-id="46d57-137">For example, a Windows Sockets connect() request may block under some conditions for as much as 21 seconds.</span></span> <span data-ttu-id="46d57-138">Os aplicativos podem precisar introduzir seus próprios tempos limite conforme apropriado para seus usuários.</span><span class="sxs-lookup"><span data-stu-id="46d57-138">Applications may need to introduce their own time outs as appropriate for their users.</span></span>

-   <span data-ttu-id="46d57-139">Minimizar a sobrecarga de protocolo.</span><span class="sxs-lookup"><span data-stu-id="46d57-139">Minimize protocol overhead.</span></span>

    <span data-ttu-id="46d57-140">Conservar a largura de banda da rede está parcialmente prestes a minimizar a sobrecarga de protocolo incorrida pelo seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="46d57-140">Conserving network bandwidth is partially about minimizing the protocol overhead incurred by your application.</span></span> <span data-ttu-id="46d57-141">Ele também está prestes a eliminar o tráfego de rede desnecessário.</span><span class="sxs-lookup"><span data-stu-id="46d57-141">It is also about eliminating unnecessary network traffic.</span></span> <span data-ttu-id="46d57-142">Protocolos com uma sobrecarga de cabeçalho inferior podem ser usados para transferir dados de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="46d57-142">Protocols with a lower header overhead can be used to transfer application data.</span></span> <span data-ttu-id="46d57-143">Por exemplo, ao enviar quantidades menores de dados não críticos ou repetíveis, use UDP em oposição ao TCP para reduzir a sobrecarga associada ao estabelecimento e à manutenção da conexão.</span><span class="sxs-lookup"><span data-stu-id="46d57-143">For example, when sending smaller amounts of noncritical or repeatable data, use UDP as opposed to TCP to reduce the overhead associated with connection establishment and maintenance.</span></span> <span data-ttu-id="46d57-144">Se os mesmos dados precisarem ser enviados a vários destinatários, considere multicast.</span><span class="sxs-lookup"><span data-stu-id="46d57-144">If the same data must be sent to multiple recipients, consider multicast.</span></span> <span data-ttu-id="46d57-145">Lembre-se de que os aplicativos UDP não são controlados por fluxo — o envio por push além da largura de banda disponível pode causar uma falha catastrófica na rede.</span><span class="sxs-lookup"><span data-stu-id="46d57-145">Be aware that UDP applications are not flow-controlled—pushing beyond the available bandwidth can cause catastrophic network failure.</span></span> <span data-ttu-id="46d57-146">O utilitário netstat pode ser usado com as opções **-** e e **-s** para exibir estatísticas de vários protocolos.</span><span class="sxs-lookup"><span data-stu-id="46d57-146">The Netstat utility can be used with its **-e** and **-s** options to display statistics for various protocols.</span></span>

-   <span data-ttu-id="46d57-147">Conservar recursos do sistema.</span><span class="sxs-lookup"><span data-stu-id="46d57-147">Conserve system resources.</span></span>

    <span data-ttu-id="46d57-148">Os recursos do sistema podem ser consumidos rapidamente se o retentor adequado não for usado.</span><span class="sxs-lookup"><span data-stu-id="46d57-148">System resources can be consumed quickly if proper restraint is not used.</span></span> <span data-ttu-id="46d57-149">Por exemplo, soquetes e conexões TCP consomem recursos.</span><span class="sxs-lookup"><span data-stu-id="46d57-149">For example, sockets and TCP connections consume resources.</span></span> <span data-ttu-id="46d57-150">Não use várias conexões TCP por cliente, em que uma atenderá à finalidade do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="46d57-150">Do not use several TCP connections per client where one will serve the application's purpose.</span></span>

<span data-ttu-id="46d57-151">Para aplicativos transacionais, boa experiência do usuário e baixa utilização da rede não são metas conflitantes.</span><span class="sxs-lookup"><span data-stu-id="46d57-151">For transactional applications, good user experience and low network utilization are not conflicting goals.</span></span> <span data-ttu-id="46d57-152">A rede é um afunilamento.</span><span class="sxs-lookup"><span data-stu-id="46d57-152">The network is a bottleneck.</span></span> <span data-ttu-id="46d57-153">Aplicativos com uso intensivo de rede passam mais tempo aguardando, e aplicativos de rede bem escritos são projetados para minimizar o tempo de espera desnecessário, tanto para a interface do usuário quanto para as transmissões de rede.</span><span class="sxs-lookup"><span data-stu-id="46d57-153">Network-intensive applications spend more time waiting, and well written network applications are designed to minimize unnecessary wait time, both for the user interface and for network transmissions.</span></span>

## <a name="related-topics"></a><span data-ttu-id="46d57-154">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="46d57-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="46d57-155">Aplicativos de alto desempenho do Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="46d57-155">High-performance Windows Sockets Applications</span></span>](high-performance-windows-sockets-applications-2.md)
</dt> <dt>

[<span data-ttu-id="46d57-156">Dimensões de desempenho</span><span class="sxs-lookup"><span data-stu-id="46d57-156">Performance Dimensions</span></span>](performance-dimensions-2.md)
</dt> </dl>

 

 



