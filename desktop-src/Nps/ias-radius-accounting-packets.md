---
title: Registrando em log com o servidor de políticas de rede
description: Registrando em log com o servidor de políticas de rede
ms.assetid: 903d89bd-c223-4f29-9eaf-1dc28d27a32a
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5117ce15731ea656913b47525387a48a39aa414c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294294"
---
# <a name="logging-with-network-policy-server"></a><span data-ttu-id="bd40e-103">Registrando em log com o servidor de políticas de rede</span><span class="sxs-lookup"><span data-stu-id="bd40e-103">Logging With Network Policy Server</span></span>

> [!Note]  
> <span data-ttu-id="bd40e-104">O IAS (serviço de autenticação da Internet) foi renomeado como NPS (servidor de políticas de rede) a partir do Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="bd40e-104">Internet Authentication Service (IAS) was renamed Network Policy Server (NPS) starting with Windows Server 2008.</span></span> <span data-ttu-id="bd40e-105">O conteúdo deste tópico aplica-se ao IAS e ao NPS.</span><span class="sxs-lookup"><span data-stu-id="bd40e-105">The content of this topic applies to both IAS and NPS.</span></span> <span data-ttu-id="bd40e-106">Em todo o texto, o NPS é usado para fazer referência a todas as versões do serviço, incluindo as versões originalmente chamadas de IAS.</span><span class="sxs-lookup"><span data-stu-id="bd40e-106">Throughout the text, NPS is used to refer to all versions of the service, including the versions originally referred to as IAS.</span></span>

 

<span data-ttu-id="bd40e-107">A tabela a seguir descreve apenas os aspectos mais importantes dos pacotes de contabilização RADIUS.</span><span class="sxs-lookup"><span data-stu-id="bd40e-107">The following table describes only the most important aspects of the RADIUS accounting packets.</span></span> <span data-ttu-id="bd40e-108">O documento solicitação de comentários de contabilidade RADIUS ([RFC 2866](https://www.ietf.org/rfc/rfc2866.txt)) fornece informações detalhadas sobre esses pacotes.</span><span class="sxs-lookup"><span data-stu-id="bd40e-108">The RADIUS Accounting Request for Comments document ([RFC 2866](https://www.ietf.org/rfc/rfc2866.txt)) provides detailed information on these packets.</span></span>

<span data-ttu-id="bd40e-109">Os pacotes de contabilização RADIUS podem ser divididos nas categorias a seguir.</span><span class="sxs-lookup"><span data-stu-id="bd40e-109">RADIUS accounting packets can be divided into the following categories.</span></span>



| <span data-ttu-id="bd40e-110">Pacote de contabilidade</span><span class="sxs-lookup"><span data-stu-id="bd40e-110">Accounting packet</span></span>  | <span data-ttu-id="bd40e-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="bd40e-111">Description</span></span>                                                                                                                                                                                                                |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd40e-112">Accounting-On</span><span class="sxs-lookup"><span data-stu-id="bd40e-112">Accounting-On</span></span>      | <span data-ttu-id="bd40e-113">Enviado pelo NAS (servidor de acesso à rede) para indicar que ele foi reiniciado.</span><span class="sxs-lookup"><span data-stu-id="bd40e-113">Sent by the Network Access Server (NAS) to indicate that it has restarted.</span></span><br/> <span data-ttu-id="bd40e-114">Contém nas-Identifier/IPAddress.</span><span class="sxs-lookup"><span data-stu-id="bd40e-114">Contains nas-identifier/ipaddress.</span></span><br/>                                                                                        |
| <span data-ttu-id="bd40e-115">Accounting-Off</span><span class="sxs-lookup"><span data-stu-id="bd40e-115">Accounting-Off</span></span>     | <span data-ttu-id="bd40e-116">Enviado pelo NAS para indicar que está sendo desligado.</span><span class="sxs-lookup"><span data-stu-id="bd40e-116">Sent by the NAS to indicate that it is being shutdown.</span></span><br/> <span data-ttu-id="bd40e-117">Contém nas-Identifier/IPAddress.</span><span class="sxs-lookup"><span data-stu-id="bd40e-117">Contains nas-identifier/ipaddress.</span></span><br/>                                                                                                            |
| <span data-ttu-id="bd40e-118">Accounting-Start</span><span class="sxs-lookup"><span data-stu-id="bd40e-118">Accounting-Start</span></span>   | <span data-ttu-id="bd40e-119">Enviado pelo NAS, depois que o usuário foi autenticado e autorizado, para indicar o início de uma sessão de usuário.</span><span class="sxs-lookup"><span data-stu-id="bd40e-119">Sent by the NAS, after the user was authenticated and authorized, to indicate the start of a user session.</span></span> <br/> <span data-ttu-id="bd40e-120">Contém userid, nas-Identifier/IPAddress, além de outras informações recebidas do NAS.</span><span class="sxs-lookup"><span data-stu-id="bd40e-120">Contains userid, nas-identifier/ipaddress, plus other information received from the NAS.</span></span><br/> |
| <span data-ttu-id="bd40e-121">Accounting-Stop</span><span class="sxs-lookup"><span data-stu-id="bd40e-121">Accounting-Stop</span></span>    | <span data-ttu-id="bd40e-122">Enviado pelo NAS para indicar o fim de uma sessão de usuário.</span><span class="sxs-lookup"><span data-stu-id="bd40e-122">Sent by the NAS to indicate the end of a user session.</span></span><br/> <span data-ttu-id="bd40e-123">Contém userid, nas-Identifier/IPAddress, além de outras informações recebidas do NAS.</span><span class="sxs-lookup"><span data-stu-id="bd40e-123">Contains userid, nas-identifier/ipaddress, plus other information received from the NAS.</span></span><br/>                                                      |
| <span data-ttu-id="bd40e-124">Accounting-Interim</span><span class="sxs-lookup"><span data-stu-id="bd40e-124">Accounting-Interim</span></span> | <span data-ttu-id="bd40e-125">Pode ser enviado periodicamente pelo NAS para cada usuário conectado no NAS.</span><span class="sxs-lookup"><span data-stu-id="bd40e-125">Could be sent periodically by the NAS for each user that is logged on at the NAS.</span></span> <br/> <span data-ttu-id="bd40e-126">Esse recurso geralmente tem suporte em versões mais recentes do NAS.</span><span class="sxs-lookup"><span data-stu-id="bd40e-126">This feature is generally supported in newer versions of NAS.</span></span><br/>                                                     |



 

<span data-ttu-id="bd40e-127">Os seguintes problemas são importantes para considerar ao coletar informações de contabilidade disponibilizadas por meio do RADIUS:</span><span class="sxs-lookup"><span data-stu-id="bd40e-127">The following issues are important to consider when collecting accounting information made available through RADIUS:</span></span>

-   <span data-ttu-id="bd40e-128">Em casos raros, os pacotes podem ser perdidos durante a transmissão e talvez nunca cheguem ao servidor RADIUS.</span><span class="sxs-lookup"><span data-stu-id="bd40e-128">In rare cases, packets could be lost during transmission and may never reach the RADIUS server.</span></span>
-   <span data-ttu-id="bd40e-129">O servidor RADIUS não será notificado se o NAS abortar.</span><span class="sxs-lookup"><span data-stu-id="bd40e-129">The RADIUS server is not notified if the NAS aborts.</span></span>
-   <span data-ttu-id="bd40e-130">A ISDN dá suporte a várias sessões e cada sessão gera um par de pacotes de início/término de contabilidade.</span><span class="sxs-lookup"><span data-stu-id="bd40e-130">ISDN supports multiple sessions and each session generates an Accounting-Start/-Stop pair of packets.</span></span> <span data-ttu-id="bd40e-131">Há um atributo de contabilidade chamado identificador de várias sessões que identifica claramente esses pacotes de várias sessões.</span><span class="sxs-lookup"><span data-stu-id="bd40e-131">There is an accounting attribute called multi-session identifier that clearly identifies such multi-session packets.</span></span> <span data-ttu-id="bd40e-132">Verifique o identificador de várias sessões, além do identificador de sessão, para calcular o número de sessões.</span><span class="sxs-lookup"><span data-stu-id="bd40e-132">Check for the multi-session identifier in addition to the session identifier to calculate the number of sessions.</span></span>

## <a name="requests-logged-by-nps"></a><span data-ttu-id="bd40e-133">Solicitações registradas pelo NPS</span><span class="sxs-lookup"><span data-stu-id="bd40e-133">Requests Logged by NPS</span></span>

<span data-ttu-id="bd40e-134">Por padrão, o NPS não registra nenhum dado.</span><span class="sxs-lookup"><span data-stu-id="bd40e-134">By default, NPS does not log any data.</span></span> <span data-ttu-id="bd40e-135">O NPS pode ser configurado, usando a interface do usuário do NPS (NPS. msc), para registrar as solicitações a seguir.</span><span class="sxs-lookup"><span data-stu-id="bd40e-135">NPS can be configured, using the NPS user interface (nps.msc), to log the following requests.</span></span>



| <span data-ttu-id="bd40e-136">Pacote registrado</span><span class="sxs-lookup"><span data-stu-id="bd40e-136">Logged packet</span></span>          | <span data-ttu-id="bd40e-137">Descrição</span><span class="sxs-lookup"><span data-stu-id="bd40e-137">Description</span></span>                                                                                                                                  |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd40e-138">Solicitação de contabilidade</span><span class="sxs-lookup"><span data-stu-id="bd40e-138">Accounting Request</span></span>     | <span data-ttu-id="bd40e-139">Qualquer um dos pacotes de contabilidade descritos na tabela anterior.</span><span class="sxs-lookup"><span data-stu-id="bd40e-139">Any of the accounting packets described in the previous table.</span></span><br/>                                                                    |
| <span data-ttu-id="bd40e-140">Solicitação de autenticação</span><span class="sxs-lookup"><span data-stu-id="bd40e-140">Authentication Request</span></span> | <span data-ttu-id="bd40e-141">Enviado pelo NAS em nome do usuário que está se conectando.</span><span class="sxs-lookup"><span data-stu-id="bd40e-141">Sent by the NAS on behalf of the connecting user.</span></span><br/> <span data-ttu-id="bd40e-142">As entradas de log contêm apenas atributos de entrada.</span><span class="sxs-lookup"><span data-stu-id="bd40e-142">The log entries contain only incoming attributes.</span></span><br/>                    |
| <span data-ttu-id="bd40e-143">Aceitação de autenticação</span><span class="sxs-lookup"><span data-stu-id="bd40e-143">Authentication Accept</span></span>  | <span data-ttu-id="bd40e-144">Enviado pelo NPS para indicar que a conexão do usuário deve ser aceita.</span><span class="sxs-lookup"><span data-stu-id="bd40e-144">Sent by NPS to indicate that the user connection should be accepted.</span></span><br/> <span data-ttu-id="bd40e-145">As entradas de log contêm apenas atributos de saída.</span><span class="sxs-lookup"><span data-stu-id="bd40e-145">The log entries contain only outgoing attributes.</span></span><br/> |
| <span data-ttu-id="bd40e-146">Rejeição de autenticação</span><span class="sxs-lookup"><span data-stu-id="bd40e-146">Authentication Reject</span></span>  | <span data-ttu-id="bd40e-147">Enviado pelo NPS para indicar que a conexão do usuário deve ser rejeitada.</span><span class="sxs-lookup"><span data-stu-id="bd40e-147">Sent by NPS to indicate that the user connection should be rejected.</span></span><br/> <span data-ttu-id="bd40e-148">As entradas de log contêm apenas atributos de saída.</span><span class="sxs-lookup"><span data-stu-id="bd40e-148">The log entries contain only outgoing attributes.</span></span><br/> |



 

<span data-ttu-id="bd40e-149">Os dados registrados pelo NPS podem ir para um arquivo de texto no servidor NPS ou em um banco de dados SQL central.</span><span class="sxs-lookup"><span data-stu-id="bd40e-149">Data logged by NPS can go to a text file on the NPS server or to a central SQL database.</span></span> <span data-ttu-id="bd40e-150">Para obter mais informações sobre o log SQL do NPS, consulte [programação do SQL](sql-programmability.md).</span><span class="sxs-lookup"><span data-stu-id="bd40e-150">For more information on NPS SQL logging, see [SQL Programmability](sql-programmability.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="bd40e-151">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="bd40e-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bd40e-152">Serviço de autenticação da Internet e servidor de políticas de rede</span><span class="sxs-lookup"><span data-stu-id="bd40e-152">Internet Authentication Service and Network Policy Server</span></span>](internet-authentication-service-vs-network-policy-server.md)
</dt> <dt>

[<span data-ttu-id="bd40e-153">Autenticação, autorização e contabilização RADIUS</span><span class="sxs-lookup"><span data-stu-id="bd40e-153">RADIUS Authentication, Authorization, and Accounting</span></span>](/windows/desktop/Nps/ias-radius-authentication-and-accounting)
</dt> <dt>

[<span data-ttu-id="bd40e-154">Trabalhando com um servidor de estado</span><span class="sxs-lookup"><span data-stu-id="bd40e-154">Working with a State Server</span></span>](/windows/desktop/Nps/ias-working-with-a-state-server)
</dt> </dl>

 

