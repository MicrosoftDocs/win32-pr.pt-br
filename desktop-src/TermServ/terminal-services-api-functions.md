---
title: Serviços de Área de Trabalho Remota funções de API
description: As funções a seguir são usadas com Serviços de Área de Trabalho Remota.
ms.assetid: e99a86ee-af0e-46db-8dad-69703ca84fa0
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e94a2168f5ad4501b9725b72923c98ea97cc707c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641269"
---
# <a name="remote-desktop-services-api-functions"></a><span data-ttu-id="809f4-103">Serviços de Área de Trabalho Remota funções de API</span><span class="sxs-lookup"><span data-stu-id="809f4-103">Remote Desktop Services API Functions</span></span>

<span data-ttu-id="809f4-104">As funções a seguir são usadas com Serviços de Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="809f4-104">The following functions are used with Remote Desktop Services.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="809f4-105">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="809f4-105">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="809f4-106">**ProcessIdToSessionId**</span><span class="sxs-lookup"><span data-stu-id="809f4-106">**ProcessIdToSessionId**</span></span>](/windows/win32/api/processthreadsapi/nf-processthreadsapi-processidtosessionid)
</dt> <dd>

<span data-ttu-id="809f4-107">Recupera a sessão de Serviços de Área de Trabalho Remota associada a um processo especificado.</span><span class="sxs-lookup"><span data-stu-id="809f4-107">Retrieves the Remote Desktop Services session associated with a specified process.</span></span>

</dd> <dt>

[<span data-ttu-id="809f4-108">**TLSConnectToLsServer**</span><span class="sxs-lookup"><span data-stu-id="809f4-108">**TLSConnectToLsServer**</span></span>](tlsconnecttolsserver.md)
</dt> <dd>

<span data-ttu-id="809f4-109">Abre um identificador para o servidor de licença de Área de Trabalho Remota especificado.</span><span class="sxs-lookup"><span data-stu-id="809f4-109">Opens a handle to the specified Remote Desktop license server.</span></span>

</dd> <dt>

[<span data-ttu-id="809f4-110">**TLSDisconnectFromServer**</span><span class="sxs-lookup"><span data-stu-id="809f4-110">**TLSDisconnectFromServer**</span></span>](tlsdisconnectfromserver.md)
</dt> <dd>

<span data-ttu-id="809f4-111">Fecha um identificador aberto para um servidor de licença Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="809f4-111">Closes an open handle to a Remote Desktop license server.</span></span>

</dd> <dt>

[<span data-ttu-id="809f4-112">**TLSGetServerCertificate**</span><span class="sxs-lookup"><span data-stu-id="809f4-112">**TLSGetServerCertificate**</span></span>](tlsgetservercertificate.md)
</dt> <dd>

<span data-ttu-id="809f4-113">Retorna o certificado do servidor de licença Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="809f4-113">Returns the certificate of the Remote Desktop license server.</span></span>

</dd> <dt>

[<span data-ttu-id="809f4-114">**TLSKeyPackEnumBegin**</span><span class="sxs-lookup"><span data-stu-id="809f4-114">**TLSKeyPackEnumBegin**</span></span>](tlskeypackenumbegin.md)
</dt> <dd>

<span data-ttu-id="809f4-115">Inicia a enumeração por meio de todos os pacotes de chaves instalados em um servidor de licença Área de Trabalho Remota com base nos critérios de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="809f4-115">Begins enumeration through all key packs that are installed on a Remote Desktop license server based on search criteria.</span></span>

</dd> <dt>

[<span data-ttu-id="809f4-116">**TLSKeyPackEnumEnd**</span><span class="sxs-lookup"><span data-stu-id="809f4-116">**TLSKeyPackEnumEnd**</span></span>](tlskeypackenumend.md)
</dt> <dd>

<span data-ttu-id="809f4-117">Continua de uma chamada anterior para a função [**TLSKeyPackEnumBegin**](tlskeypackenumbegin.md) e encerra a enumeração.</span><span class="sxs-lookup"><span data-stu-id="809f4-117">Continues from a previous call to the [**TLSKeyPackEnumBegin**](tlskeypackenumbegin.md) function and terminates the enumeration.</span></span>

</dd> <dt>

[<span data-ttu-id="809f4-118">**TLSKeyPackEnumNext**</span><span class="sxs-lookup"><span data-stu-id="809f4-118">**TLSKeyPackEnumNext**</span></span>](tlskeypackenumnext.md)
</dt> <dd>

<span data-ttu-id="809f4-119">Continua de uma chamada anterior para a função [**TLSKeyPackEnumBegin**](tlskeypackenumbegin.md) e retorna o próximo pacote de chaves instalado em um servidor de licença área de trabalho remota que corresponde aos critérios de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="809f4-119">Continues from a previous call to the [**TLSKeyPackEnumBegin**](tlskeypackenumbegin.md) function and returns the next key pack that is installed on a Remote Desktop license server that matches the search criteria.</span></span>

</dd> <dt>

[<span data-ttu-id="809f4-120">**TLSLicenseEnumBegin**</span><span class="sxs-lookup"><span data-stu-id="809f4-120">**TLSLicenseEnumBegin**</span></span>](tlslicenseenumbegin.md)
</dt> <dd>

<span data-ttu-id="809f4-121">Inicia a enumeração de licenças emitidas pelo servidor de licença Área de Trabalho Remota com base nos critérios de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="809f4-121">Begins enumeration of licenses that are issued by the Remote Desktop license server based on search criteria.</span></span>

</dd> <dt>

[<span data-ttu-id="809f4-122">**TLSLicenseEnumEnd**</span><span class="sxs-lookup"><span data-stu-id="809f4-122">**TLSLicenseEnumEnd**</span></span>](tlslicenseenumend.md)
</dt> <dd>

<span data-ttu-id="809f4-123">Continua de uma chamada anterior para a função [**TLSLicenseEnumBegin**](tlslicenseenumbegin.md) e encerra a enumeração.</span><span class="sxs-lookup"><span data-stu-id="809f4-123">Continues from a previous call to the [**TLSLicenseEnumBegin**](tlslicenseenumbegin.md) function and terminates the enumeration.</span></span>

</dd> <dt>

[<span data-ttu-id="809f4-124">**TLSLicenseEnumNext**</span><span class="sxs-lookup"><span data-stu-id="809f4-124">**TLSLicenseEnumNext**</span></span>](tlslicenseenumnext.md)
</dt> <dd>

<span data-ttu-id="809f4-125">Continua de uma chamada anterior para a função [**TLSLicenseEnumBegin**](tlslicenseenumbegin.md) e retorna a próxima licença instalada em um servidor de licença área de trabalho remota que corresponde aos critérios de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="809f4-125">Continues from a previous call to the [**TLSLicenseEnumBegin**](tlslicenseenumbegin.md) function and returns the next license that is installed on a Remote Desktop license server that matches the search criteria.</span></span>

</dd> <dt>

[<span data-ttu-id="809f4-126">**VirtualChannelClose**</span><span class="sxs-lookup"><span data-stu-id="809f4-126">**VirtualChannelClose**</span></span>](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelclose)
</dt> <dd>

<span data-ttu-id="809f4-127">Fecha a extremidade do cliente de um canal virtual.</span><span class="sxs-lookup"><span data-stu-id="809f4-127">Closes the client end of a virtual channel.</span></span>

</dd> <dt>

[<span data-ttu-id="809f4-128">**VirtualChannelEntry**</span><span class="sxs-lookup"><span data-stu-id="809f4-128">**VirtualChannelEntry**</span></span>](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelentry)
</dt> <dd>

<span data-ttu-id="809f4-129">Um ponto de entrada definido pelo aplicativo para a DLL do lado do cliente de um aplicativo que usa Serviços de Área de Trabalho Remota canais virtuais.</span><span class="sxs-lookup"><span data-stu-id="809f4-129">An application-defined entry point for the client-side DLL of an application that uses Remote Desktop Services virtual channels.</span></span>

</dd> <dt>

[<span data-ttu-id="809f4-130">**VirtualChannelInit**</span><span class="sxs-lookup"><span data-stu-id="809f4-130">**VirtualChannelInit**</span></span>](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelinit)
</dt> <dd>

<span data-ttu-id="809f4-131">Inicializa o acesso de uma DLL de cliente para Serviços de Área de Trabalho Remota canais virtuais.</span><span class="sxs-lookup"><span data-stu-id="809f4-131">Initializes a client DLL's access to Remote Desktop Services virtual channels.</span></span>

</dd> <dt>

[<span data-ttu-id="809f4-132">*VirtualChannelInitEvent*</span><span class="sxs-lookup"><span data-stu-id="809f4-132">*VirtualChannelInitEvent*</span></span>](/windows/desktop/api/Cchannel/nc-cchannel-channel_init_event_fn)
</dt> <dd>

<span data-ttu-id="809f4-133">Uma função de retorno de chamada definida pelo aplicativo que Serviços de Área de Trabalho Remota chamadas para notificar a DLL de cliente dos eventos de canal virtual.</span><span class="sxs-lookup"><span data-stu-id="809f4-133">An application-defined callback function that Remote Desktop Services calls to notify the client DLL of virtual channel events.</span></span>

</dd> <dt>

[<span data-ttu-id="809f4-134">**VirtualChannelOpen**</span><span class="sxs-lookup"><span data-stu-id="809f4-134">**VirtualChannelOpen**</span></span>](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelopen)
</dt> <dd>

<span data-ttu-id="809f4-135">Abre a extremidade do cliente de um canal virtual.</span><span class="sxs-lookup"><span data-stu-id="809f4-135">Opens the client end of a virtual channel.</span></span>

</dd> <dt>

[<span data-ttu-id="809f4-136">*VirtualChannelOpenEvent*</span><span class="sxs-lookup"><span data-stu-id="809f4-136">*VirtualChannelOpenEvent*</span></span>](/windows/desktop/api/Cchannel/nc-cchannel-channel_open_event_fn)
</dt> <dd>

<span data-ttu-id="809f4-137">Uma função de retorno de chamada definida pelo aplicativo que Serviços de Área de Trabalho Remota chamadas para notificar a DLL do cliente de eventos para um canal virtual específico.</span><span class="sxs-lookup"><span data-stu-id="809f4-137">An application-defined callback function that Remote Desktop Services calls to notify the client DLL of events for a specific virtual channel.</span></span>

</dd> <dt>

[<span data-ttu-id="809f4-138">**VirtualChannelWrite**</span><span class="sxs-lookup"><span data-stu-id="809f4-138">**VirtualChannelWrite**</span></span>](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelwrite)
</dt> <dd>

<span data-ttu-id="809f4-139">Envia dados da extremidade do cliente de um canal virtual para um aplicativo de parceiro na extremidade do servidor.</span><span class="sxs-lookup"><span data-stu-id="809f4-139">Sends data from the client end of a virtual channel to a partner application on the server end.</span></span>

</dd> <dt>

[<span data-ttu-id="809f4-140">**WTSCloseServer**</span><span class="sxs-lookup"><span data-stu-id="809f4-140">**WTSCloseServer**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtscloseserver)
</dt> <dd>

<span data-ttu-id="809f4-141">Fecha um identificador aberto para um servidor de Host da Sessão da Área de Trabalho Remota (Host da Sessão RD).</span><span class="sxs-lookup"><span data-stu-id="809f4-141">Closes an open handle to a Remote Desktop Session Host (RD Session Host) server.</span></span>

</dd> <dt>

[<span data-ttu-id="809f4-142">**WTSConnectSession**</span><span class="sxs-lookup"><span data-stu-id="809f4-142">**WTSConnectSession**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsconnectsessiona)
</dt> <dd>

<span data-ttu-id="809f4-143">Conecta uma sessão de Serviços de Área de Trabalho Remota a uma sessão existente no computador local.</span><span class="sxs-lookup"><span data-stu-id="809f4-143">Connects a Remote Desktop Services session to an existing session on the local computer.</span></span>

</dd> <dt>

[<span data-ttu-id="809f4-144">**WTSCreateListener**</span><span class="sxs-lookup"><span data-stu-id="809f4-144">**WTSCreateListener**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtscreatelistenera)
</dt> <dd>

<span data-ttu-id="809f4-145">Cria um novo ouvinte Serviços de Área de Trabalho Remota ou configura um ouvinte existente.</span><span class="sxs-lookup"><span data-stu-id="809f4-145">Creates a new Remote Desktop Services listener or configures an existing listener.</span></span>

</dd> <dt>

[<span data-ttu-id="809f4-146">**WTSDisconnectSession**</span><span class="sxs-lookup"><span data-stu-id="809f4-146">**WTSDisconnectSession**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsdisconnectsession)
</dt> <dd>

<span data-ttu-id="809f4-147">Desconecta o usuário conectado da sessão de Serviços de Área de Trabalho Remota especificada sem fechar a sessão.</span><span class="sxs-lookup"><span data-stu-id="809f4-147">Disconnects the logged-on user from the specified Remote Desktop Services session without closing the session.</span></span>

</dd> <dt>

[<span data-ttu-id="809f4-148">**WTSEnableChildSessions**</span><span class="sxs-lookup"><span data-stu-id="809f4-148">**WTSEnableChildSessions**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenablechildsessions)
</dt> <dd>

<span data-ttu-id="809f4-149">Habilita ou desabilita [sessões filho](child-sessions.md).</span><span class="sxs-lookup"><span data-stu-id="809f4-149">Enables or disables [Child Sessions](child-sessions.md).</span></span>

</dd> <dt>

[<span data-ttu-id="809f4-150">**WTSEnumerateListeners**</span><span class="sxs-lookup"><span data-stu-id="809f4-150">**WTSEnumerateListeners**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenumeratelistenersa)
</dt> <dd>

<span data-ttu-id="809f4-151">Enumera todos os ouvintes Serviços de Área de Trabalho Remota em um servidor Host da Sessão RD.</span><span class="sxs-lookup"><span data-stu-id="809f4-151">Enumerates all the Remote Desktop Services listeners on a RD Session Host server.</span></span>

</dd> <dt>

[<span data-ttu-id="809f4-152">**WTSEnumerateProcesses**</span><span class="sxs-lookup"><span data-stu-id="809f4-152">**WTSEnumerateProcesses**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenumerateprocessesa)
</dt> <dd>

<span data-ttu-id="809f4-153">Recupera informações sobre os processos ativos em um servidor de Host da Sessão RD especificado.</span><span class="sxs-lookup"><span data-stu-id="809f4-153">Retrieves information about the active processes on a specified RD Session Host server.</span></span>

</dd> <dt>

[<span data-ttu-id="809f4-154">**WTSEnumerateProcessesEx**</span><span class="sxs-lookup"><span data-stu-id="809f4-154">**WTSEnumerateProcessesEx**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenumerateprocessesexa)
</dt> <dd>

<span data-ttu-id="809f4-155">Recupera informações sobre os processos ativos no servidor de Host da Sessão RD especificado ou no servidor de Host de Virtualização de Área de Trabalho Remota (host de Virtualização RD).</span><span class="sxs-lookup"><span data-stu-id="809f4-155">Retrieves information about the active processes on the specified RD Session Host server or Remote Desktop Virtualization Host (RD Virtualization Host) server.</span></span>

</dd> <dt>

[<span data-ttu-id="809f4-156">**WTSEnumerateServers**</span><span class="sxs-lookup"><span data-stu-id="809f4-156">**WTSEnumerateServers**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenumerateserversa)
</dt> <dd>

<span data-ttu-id="809f4-157">Retorna uma lista de todos os servidores de Host da Sessão RD dentro do domínio especificado.</span><span class="sxs-lookup"><span data-stu-id="809f4-157">Returns a list of all RD Session Host servers within the specified domain.</span></span>

</dd> <dt>

[<span data-ttu-id="809f4-158">**WTSEnumerateSessions**</span><span class="sxs-lookup"><span data-stu-id="809f4-158">**WTSEnumerateSessions**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenumeratesessionsa)
</dt> <dd>

<span data-ttu-id="809f4-159">Recupera uma lista de sessões em um servidor Host da Sessão RD.</span><span class="sxs-lookup"><span data-stu-id="809f4-159">Retrieves a list of sessions on a RD Session Host server.</span></span>

</dd> <dt>

[<span data-ttu-id="809f4-160">**WTSEnumerateSessionsEx**</span><span class="sxs-lookup"><span data-stu-id="809f4-160">**WTSEnumerateSessionsEx**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenumeratesessionsexa)
</dt> <dd>

<span data-ttu-id="809f4-161">Recupera uma lista de sessões em um servidor de Host da Sessão RD ou servidor host de virtualização de área de trabalho especificado.</span><span class="sxs-lookup"><span data-stu-id="809f4-161">Retrieves a list of sessions on a specified RD Session Host server or RD Virtualization Host server.</span></span>

</dd> <dt>

[<span data-ttu-id="809f4-162">**WTSFreeMemory**</span><span class="sxs-lookup"><span data-stu-id="809f4-162">**WTSFreeMemory**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsfreememory)
</dt> <dd>

<span data-ttu-id="809f4-163">Libera memória alocada por uma função Serviços de Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="809f4-163">Frees memory allocated by a Remote Desktop Services function.</span></span>

</dd> <dt>

[<span data-ttu-id="809f4-164">**WTSFreeMemoryEx**</span><span class="sxs-lookup"><span data-stu-id="809f4-164">**WTSFreeMemoryEx**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsfreememoryexa)
</dt> <dd>

<span data-ttu-id="809f4-165">Libera memória que contém [**informações de \_ processo WTS por \_ \_ exemplo**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_process_info_exa) , ou [**WTS informações de \_ sessão \_ \_ 1**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_session_info_1a) , alocadas por uma função serviços de área de trabalho remota.</span><span class="sxs-lookup"><span data-stu-id="809f4-165">Frees memory that contains [**WTS\_PROCESS\_INFO\_EX**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_process_info_exa) or [**WTS\_SESSION\_INFO\_1**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_session_info_1a) structures allocated by a Remote Desktop Services function.</span></span>

</dd> <dt>

[<span data-ttu-id="809f4-166">**WTSGetActiveConsoleSessionId**</span><span class="sxs-lookup"><span data-stu-id="809f4-166">**WTSGetActiveConsoleSessionId**</span></span>](/windows/desktop/api/Winbase/nf-winbase-wtsgetactiveconsolesessionid)
</dt> <dd>

<span data-ttu-id="809f4-167">Recupera o identificador de sessão da sessão de console.</span><span class="sxs-lookup"><span data-stu-id="809f4-167">Retrieves the session identifier of the console session.</span></span>

</dd> <dt>

[<span data-ttu-id="809f4-168">**WTSGetChildSessionId**</span><span class="sxs-lookup"><span data-stu-id="809f4-168">**WTSGetChildSessionId**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsgetchildsessionid)
</dt> <dd>

<span data-ttu-id="809f4-169">Recupera o identificador de sessão filho, se presente.</span><span class="sxs-lookup"><span data-stu-id="809f4-169">Retrieves the child session identifier, if present.</span></span>

</dd> <dt>

[<span data-ttu-id="809f4-170">**WTSGetListenerSecurity**</span><span class="sxs-lookup"><span data-stu-id="809f4-170">**WTSGetListenerSecurity**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsgetlistenersecuritya)
</dt> <dd>

<span data-ttu-id="809f4-171">Recupera o descritor de segurança de um ouvinte de Serviços de Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="809f4-171">Retrieves the security descriptor of a Remote Desktop Services listener.</span></span>

</dd> <dt>

[<span data-ttu-id="809f4-172">**WTSIsChildSessionsEnabled**</span><span class="sxs-lookup"><span data-stu-id="809f4-172">**WTSIsChildSessionsEnabled**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsischildsessionsenabled)
</dt> <dd>

<span data-ttu-id="809f4-173">Determina se as sessões filhas estão habilitadas.</span><span class="sxs-lookup"><span data-stu-id="809f4-173">Determines whether child sessions are enabled.</span></span>

</dd> <dt>

[<span data-ttu-id="809f4-174">**WTSLogoffSession**</span><span class="sxs-lookup"><span data-stu-id="809f4-174">**WTSLogoffSession**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtslogoffsession)
</dt> <dd>

<span data-ttu-id="809f4-175">Faz logoff de uma sessão de Serviços de Área de Trabalho Remota especificada.</span><span class="sxs-lookup"><span data-stu-id="809f4-175">Logs off a specified Remote Desktop Services session.</span></span>

</dd> <dt>

[<span data-ttu-id="809f4-176">**WTSOpenServer**</span><span class="sxs-lookup"><span data-stu-id="809f4-176">**WTSOpenServer**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsopenservera)
</dt> <dd>

<span data-ttu-id="809f4-177">Abre um identificador para o servidor de Host da Sessão RD especificado.</span><span class="sxs-lookup"><span data-stu-id="809f4-177">Opens a handle to the specified RD Session Host server.</span></span>

</dd> <dt>

[<span data-ttu-id="809f4-178">**WTSOpenServerEx**</span><span class="sxs-lookup"><span data-stu-id="809f4-178">**WTSOpenServerEx**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsopenserverexa)
</dt> <dd>

<span data-ttu-id="809f4-179">Abre um identificador para o servidor de Host da Sessão RD especificado ou para o servidor host de virtualização de área de trabalho remota.</span><span class="sxs-lookup"><span data-stu-id="809f4-179">Opens a handle to the specified RD Session Host server or RD Virtualization Host server.</span></span>

</dd> <dt>

[<span data-ttu-id="809f4-180">**WTSQueryListenerConfig**</span><span class="sxs-lookup"><span data-stu-id="809f4-180">**WTSQueryListenerConfig**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsquerylistenerconfiga)
</dt> <dd>

<span data-ttu-id="809f4-181">Recupera informações de configuração para um ouvinte de Serviços de Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="809f4-181">Retrieves configuration information for a Remote Desktop Services listener.</span></span>

</dd> <dt>

[<span data-ttu-id="809f4-182">**WTSQuerySessionInformation**</span><span class="sxs-lookup"><span data-stu-id="809f4-182">**WTSQuerySessionInformation**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsquerysessioninformationa)
</dt> <dd>

<span data-ttu-id="809f4-183">Recupera informações de sessão para a sessão especificada no servidor de Host da Sessão RD especificado.</span><span class="sxs-lookup"><span data-stu-id="809f4-183">Retrieves session information for the specified session on the specified RD Session Host server.</span></span>

</dd> <dt>

[<span data-ttu-id="809f4-184">**WTSQueryUserConfig**</span><span class="sxs-lookup"><span data-stu-id="809f4-184">**WTSQueryUserConfig**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsqueryuserconfiga)
</dt> <dd>

<span data-ttu-id="809f4-185">Recupera informações de configuração para o usuário especificado no controlador de domínio ou servidor de Host da Sessão RD especificado.</span><span class="sxs-lookup"><span data-stu-id="809f4-185">Retrieves configuration information for the specified user on the specified domain controller or RD Session Host server.</span></span>

</dd> <dt>

[<span data-ttu-id="809f4-186">**WTSQueryUserToken**</span><span class="sxs-lookup"><span data-stu-id="809f4-186">**WTSQueryUserToken**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsqueryusertoken)
</dt> <dd>

<span data-ttu-id="809f4-187">Obtém o token de acesso primário do usuário conectado especificado pela ID de sessão.</span><span class="sxs-lookup"><span data-stu-id="809f4-187">Obtains the primary access token of the logged-on user specified by the session ID.</span></span>

</dd> <dt>

[<span data-ttu-id="809f4-188">**WTSRegisterSessionNotification**</span><span class="sxs-lookup"><span data-stu-id="809f4-188">**WTSRegisterSessionNotification**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsregistersessionnotification)
</dt> <dd>

<span data-ttu-id="809f4-189">Registra a janela especificada para receber notificações de alteração de sessão.</span><span class="sxs-lookup"><span data-stu-id="809f4-189">Registers the specified window to receive session change notifications.</span></span>

</dd> <dt>

[<span data-ttu-id="809f4-190">**WTSRegisterSessionNotificationEx**</span><span class="sxs-lookup"><span data-stu-id="809f4-190">**WTSRegisterSessionNotificationEx**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsregistersessionnotificationex)
</dt> <dd>

<span data-ttu-id="809f4-191">Registra a janela especificada para receber notificações de alteração de sessão.</span><span class="sxs-lookup"><span data-stu-id="809f4-191">Registers the specified window to receive session change notifications.</span></span>

</dd> <dt>

[<span data-ttu-id="809f4-192">**WTSSendMessage**</span><span class="sxs-lookup"><span data-stu-id="809f4-192">**WTSSendMessage**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtssendmessagea)
</dt> <dd>

<span data-ttu-id="809f4-193">Exibe uma caixa de mensagem na área de trabalho do cliente de uma sessão de Serviços de Área de Trabalho Remota especificada.</span><span class="sxs-lookup"><span data-stu-id="809f4-193">Displays a message box on the client desktop of a specified Remote Desktop Services session.</span></span>

</dd> <dt>

[<span data-ttu-id="809f4-194">**WTSSetListenerSecurity**</span><span class="sxs-lookup"><span data-stu-id="809f4-194">**WTSSetListenerSecurity**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtssetlistenersecuritya)
</dt> <dd>

<span data-ttu-id="809f4-195">Configura o descritor de segurança de um ouvinte Serviços de Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="809f4-195">Configures the security descriptor of a Remote Desktop Services listener.</span></span>

</dd> <dt>

[<span data-ttu-id="809f4-196">**WTSSetUserConfig**</span><span class="sxs-lookup"><span data-stu-id="809f4-196">**WTSSetUserConfig**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtssetuserconfiga)
</dt> <dd>

<span data-ttu-id="809f4-197">Modifica as informações de configuração para o usuário especificado no controlador de domínio ou servidor de Host da Sessão RD especificado.</span><span class="sxs-lookup"><span data-stu-id="809f4-197">Modifies configuration information for the specified user on the specified domain controller or RD Session Host server.</span></span>

</dd> <dt>

[<span data-ttu-id="809f4-198">**WTSShutdownSystem**</span><span class="sxs-lookup"><span data-stu-id="809f4-198">**WTSShutdownSystem**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsshutdownsystem)
</dt> <dd>

<span data-ttu-id="809f4-199">Desliga (e, opcionalmente, reinicia) o servidor de Host da Sessão RD especificado.</span><span class="sxs-lookup"><span data-stu-id="809f4-199">Shuts down (and optionally restarts) the specified RD Session Host server.</span></span>

</dd> <dt>

[<span data-ttu-id="809f4-200">**WTSStartRemoteControlSession**</span><span class="sxs-lookup"><span data-stu-id="809f4-200">**WTSStartRemoteControlSession**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsstartremotecontrolsessiona)
</dt> <dd>

<span data-ttu-id="809f4-201">Inicia o controle remoto de outra sessão de Serviços de Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="809f4-201">Starts the remote control of another Remote Desktop Services session.</span></span> <span data-ttu-id="809f4-202">Você deve chamar essa função de uma sessão remota.</span><span class="sxs-lookup"><span data-stu-id="809f4-202">You must call this function from a remote session.</span></span>

</dd> <dt>

[<span data-ttu-id="809f4-203">**WTSStopRemoteControlSession**</span><span class="sxs-lookup"><span data-stu-id="809f4-203">**WTSStopRemoteControlSession**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsstopremotecontrolsession)
</dt> <dd>

<span data-ttu-id="809f4-204">Interrompe uma sessão de controle remoto.</span><span class="sxs-lookup"><span data-stu-id="809f4-204">Stops a remote control session.</span></span>

</dd> <dt>

[<span data-ttu-id="809f4-205">**WTSTerminateProcess**</span><span class="sxs-lookup"><span data-stu-id="809f4-205">**WTSTerminateProcess**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsterminateprocess)
</dt> <dd>

<span data-ttu-id="809f4-206">Encerra o processo especificado no servidor de Host da Sessão RD especificado.</span><span class="sxs-lookup"><span data-stu-id="809f4-206">Terminates the specified process on the specified RD Session Host server.</span></span>

</dd> <dt>

[<span data-ttu-id="809f4-207">**WTSUnRegisterSessionNotification**</span><span class="sxs-lookup"><span data-stu-id="809f4-207">**WTSUnRegisterSessionNotification**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsunregistersessionnotification)
</dt> <dd>

<span data-ttu-id="809f4-208">Cancela o registro da janela especificada para que ela não receba outras notificações de alteração de sessão.</span><span class="sxs-lookup"><span data-stu-id="809f4-208">Unregisters the specified window so that it receives no further session change notifications.</span></span>

</dd> <dt>

[<span data-ttu-id="809f4-209">**WTSUnRegisterSessionNotificationEx**</span><span class="sxs-lookup"><span data-stu-id="809f4-209">**WTSUnRegisterSessionNotificationEx**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsunregistersessionnotificationex)
</dt> <dd>

<span data-ttu-id="809f4-210">Cancela o registro da janela especificada para que ela não receba outras notificações de alteração de sessão.</span><span class="sxs-lookup"><span data-stu-id="809f4-210">Unregisters the specified window so that it receives no further session change notifications.</span></span>

</dd> <dt>

[<span data-ttu-id="809f4-211">**WTSVirtualChannelClose**</span><span class="sxs-lookup"><span data-stu-id="809f4-211">**WTSVirtualChannelClose**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelclose)
</dt> <dd>

<span data-ttu-id="809f4-212">Fecha um identificador de canal virtual aberto.</span><span class="sxs-lookup"><span data-stu-id="809f4-212">Closes an open virtual channel handle.</span></span>

</dd> <dt>

[<span data-ttu-id="809f4-213">**WTSVirtualChannelOpen**</span><span class="sxs-lookup"><span data-stu-id="809f4-213">**WTSVirtualChannelOpen**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelopen)
</dt> <dd>

<span data-ttu-id="809f4-214">Abre um identificador para a extremidade do servidor de um canal virtual especificado.</span><span class="sxs-lookup"><span data-stu-id="809f4-214">Opens a handle to the server end of a specified virtual channel.</span></span>

</dd> <dt>

[<span data-ttu-id="809f4-215">**WTSVirtualChannelOpenEx**</span><span class="sxs-lookup"><span data-stu-id="809f4-215">**WTSVirtualChannelOpenEx**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelopenex)
</dt> <dd>

<span data-ttu-id="809f4-216">Cria um canal virtual de maneira semelhante a [**WTSVirtualChannelOpen**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelopen).</span><span class="sxs-lookup"><span data-stu-id="809f4-216">Creates a virtual channel in a manner similar to [**WTSVirtualChannelOpen**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelopen).</span></span>

</dd> <dt>

[<span data-ttu-id="809f4-217">**WTSVirtualChannelPurgeInput**</span><span class="sxs-lookup"><span data-stu-id="809f4-217">**WTSVirtualChannelPurgeInput**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelpurgeinput)
</dt> <dd>

<span data-ttu-id="809f4-218">Exclui todos os dados de entrada na fila enviados do cliente para o servidor em um canal virtual especificado.</span><span class="sxs-lookup"><span data-stu-id="809f4-218">Deletes all queued input data sent from the client to the server on a specified virtual channel.</span></span>

</dd> <dt>

[<span data-ttu-id="809f4-219">**WTSVirtualChannelPurgeOutput**</span><span class="sxs-lookup"><span data-stu-id="809f4-219">**WTSVirtualChannelPurgeOutput**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelpurgeoutput)
</dt> <dd>

<span data-ttu-id="809f4-220">Exclui todos os dados de saída na fila enviados do servidor para o cliente em um canal virtual especificado.</span><span class="sxs-lookup"><span data-stu-id="809f4-220">Deletes all queued output data sent from the server to the client on a specified virtual channel.</span></span>

</dd> <dt>

[<span data-ttu-id="809f4-221">**WTSVirtualChannelQuery**</span><span class="sxs-lookup"><span data-stu-id="809f4-221">**WTSVirtualChannelQuery**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelquery)
</dt> <dd>

<span data-ttu-id="809f4-222">Retorna informações sobre um canal virtual especificado.</span><span class="sxs-lookup"><span data-stu-id="809f4-222">Returns information about a specified virtual channel.</span></span>

</dd> <dt>

[<span data-ttu-id="809f4-223">**WTSVirtualChannelRead**</span><span class="sxs-lookup"><span data-stu-id="809f4-223">**WTSVirtualChannelRead**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelread)
</dt> <dd>

<span data-ttu-id="809f4-224">Lê dados da extremidade do servidor de um canal virtual.</span><span class="sxs-lookup"><span data-stu-id="809f4-224">Reads data from the server end of a virtual channel.</span></span>

</dd> <dt>

[<span data-ttu-id="809f4-225">**WTSVirtualChannelWrite**</span><span class="sxs-lookup"><span data-stu-id="809f4-225">**WTSVirtualChannelWrite**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelwrite)
</dt> <dd>

<span data-ttu-id="809f4-226">Grava dados na extremidade do servidor de um canal virtual.</span><span class="sxs-lookup"><span data-stu-id="809f4-226">Writes data to the server end of a virtual channel.</span></span>

</dd> <dt>

[<span data-ttu-id="809f4-227">**WTSWaitSystemEvent**</span><span class="sxs-lookup"><span data-stu-id="809f4-227">**WTSWaitSystemEvent**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtswaitsystemevent)
</dt> <dd>

<span data-ttu-id="809f4-228">Aguarda um evento de Serviços de Área de Trabalho Remota antes de retornar ao chamador.</span><span class="sxs-lookup"><span data-stu-id="809f4-228">Waits for a Remote Desktop Services event before returning to the caller.</span></span>

</dd> </dl>

 

 