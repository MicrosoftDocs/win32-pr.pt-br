---
title: Estruturas de API Serviços de Área de Trabalho Remota
description: Lista as estruturas usadas com a API de Serviços de Área de Trabalho Remota.
ms.assetid: 5d467241-499c-4038-8d9c-4244457e484f
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22fb8de65f7f234f85eb8071cc66743c9c26cc9b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084568"
---
# <a name="remote-desktop-services-api-structures"></a><span data-ttu-id="b6e2a-103">Estruturas de API Serviços de Área de Trabalho Remota</span><span class="sxs-lookup"><span data-stu-id="b6e2a-103">Remote Desktop Services API Structures</span></span>

<span data-ttu-id="b6e2a-104">As estruturas a seguir são usadas com a API Serviços de Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="b6e2a-104">The following structures are used with the Remote Desktop Services API.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="b6e2a-105">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="b6e2a-105">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="b6e2a-106">**DEF. de canal \_**</span><span class="sxs-lookup"><span data-stu-id="b6e2a-106">**CHANNEL\_DEF**</span></span>](/windows/desktop/api/Pchannel/ns-pchannel-tagchannel_def)
</dt> <dd>

<span data-ttu-id="b6e2a-107">Contém o nome e as opções de um canal virtual Serviços de Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="b6e2a-107">Contains the name and options of a Remote Desktop Services virtual channel.</span></span>

</dd> <dt>

[<span data-ttu-id="b6e2a-108">**\_pontos de entrada de canal \_**</span><span class="sxs-lookup"><span data-stu-id="b6e2a-108">**CHANNEL\_ENTRY\_POINTS**</span></span>](/windows/win32/api/cchannel/ns-cchannel-channel_entry_points)
</dt> <dd>

<span data-ttu-id="b6e2a-109">Contém ponteiros para as funções chamadas por uma DLL do lado do cliente para acessar canais virtuais.</span><span class="sxs-lookup"><span data-stu-id="b6e2a-109">Contains pointers to the functions called by a client-side DLL to access virtual channels.</span></span>

</dd> <dt>

[<span data-ttu-id="b6e2a-110">**\_cabeçalho de PDU do canal \_**</span><span class="sxs-lookup"><span data-stu-id="b6e2a-110">**CHANNEL\_PDU\_HEADER**</span></span>](/windows/win32/api/pchannel/ns-pchannel-channel_pdu_header)
</dt> <dd>

<span data-ttu-id="b6e2a-111">Contém informações sobre um bloco de dados que está sendo recebido pela extremidade do servidor de um canal virtual.</span><span class="sxs-lookup"><span data-stu-id="b6e2a-111">Contains information about a data block being received by the server end of a virtual channel.</span></span>

</dd> <dt>

[<span data-ttu-id="b6e2a-112">**LSKeyPack**</span><span class="sxs-lookup"><span data-stu-id="b6e2a-112">**LSKeyPack**</span></span>](lskeypack.md)
</dt> <dd>

<span data-ttu-id="b6e2a-113">Contém informações sobre um pacote de chaves de licenciamento Serviços de Área de Trabalho Remota específico.</span><span class="sxs-lookup"><span data-stu-id="b6e2a-113">Contains information about a specific Remote Desktop Services licensing key pack.</span></span>

</dd> <dt>

[<span data-ttu-id="b6e2a-114">**LSLicense**</span><span class="sxs-lookup"><span data-stu-id="b6e2a-114">**LSLicense**</span></span>](lslicense.md)
</dt> <dd>

<span data-ttu-id="b6e2a-115">Contém informações sobre uma licença de Serviços de Área de Trabalho Remota específica.</span><span class="sxs-lookup"><span data-stu-id="b6e2a-115">Contains information about a specific Remote Desktop Services license.</span></span>

</dd> <dt>

[<span data-ttu-id="b6e2a-116">**WTSCLIENT**</span><span class="sxs-lookup"><span data-stu-id="b6e2a-116">**WTSCLIENT**</span></span>](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtsclienta)
</dt> <dd>

<span data-ttu-id="b6e2a-117">Contém informações sobre um cliente de Conexão de Área de Trabalho Remota (RDC).</span><span class="sxs-lookup"><span data-stu-id="b6e2a-117">Contains information about a Remote Desktop Connection (RDC) client.</span></span>

</dd> <dt>

[<span data-ttu-id="b6e2a-118">**WTSCONFIGINFO**</span><span class="sxs-lookup"><span data-stu-id="b6e2a-118">**WTSCONFIGINFO**</span></span>](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtsconfiginfoa)
</dt> <dd>

<span data-ttu-id="b6e2a-119">Contém informações sobre uma sessão de Serviços de Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="b6e2a-119">Contains information about a Remote Desktop Services session.</span></span>

</dd> <dt>

[<span data-ttu-id="b6e2a-120">**WTSINFO**</span><span class="sxs-lookup"><span data-stu-id="b6e2a-120">**WTSINFO**</span></span>](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtsinfoa)
</dt> <dd>

<span data-ttu-id="b6e2a-121">Contém informações sobre uma sessão de Serviços de Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="b6e2a-121">Contains information about a Remote Desktop Services session.</span></span>

</dd> <dt>

[<span data-ttu-id="b6e2a-122">**WTSINFOEX**</span><span class="sxs-lookup"><span data-stu-id="b6e2a-122">**WTSINFOEX**</span></span>](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtsinfoexa)
</dt> <dd>

<span data-ttu-id="b6e2a-123">Contém uma União de [**\_ nível de WTSINFOEX**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtsinfoex_level_a) que contém informações estendidas sobre uma sessão de serviços de área de trabalho remota.</span><span class="sxs-lookup"><span data-stu-id="b6e2a-123">Contains a [**WTSINFOEX\_LEVEL**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtsinfoex_level_a) union that contains extended information about a Remote Desktop Services session.</span></span>

</dd> <dt>

[<span data-ttu-id="b6e2a-124">**WTSINFOEX \_ LEVEL1**</span><span class="sxs-lookup"><span data-stu-id="b6e2a-124">**WTSINFOEX\_LEVEL1**</span></span>](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtsinfoex_level1_a)
</dt> <dd>

<span data-ttu-id="b6e2a-125">Contém informações estendidas sobre uma sessão de Serviços de Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="b6e2a-125">Contains extended information about a Remote Desktop Services session.</span></span>

</dd> <dt>

[<span data-ttu-id="b6e2a-126">**WTSLISTENERCONFIG**</span><span class="sxs-lookup"><span data-stu-id="b6e2a-126">**WTSLISTENERCONFIG**</span></span>](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtslistenerconfiga)
</dt> <dd>

<span data-ttu-id="b6e2a-127">Contém informações sobre um ouvinte de Serviços de Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="b6e2a-127">Contains information about a Remote Desktop Services listener.</span></span>

</dd> <dt>

[<span data-ttu-id="b6e2a-128">**\_endereço IP do WTSSBX \_**</span><span class="sxs-lookup"><span data-stu-id="b6e2a-128">**WTSSBX\_IP\_ADDRESS**</span></span>](/windows/win32/api/tssbx/ns-tssbx-wtssbx_ip_address)
</dt> <dd>

<span data-ttu-id="b6e2a-129">Contém informações sobre o endereço IP de um recurso de rede.</span><span class="sxs-lookup"><span data-stu-id="b6e2a-129">Contains information about the IP address of a network resource.</span></span>

</dd> <dt>

[<span data-ttu-id="b6e2a-130">**\_informações de \_ conexão do computador WTSSBX \_**</span><span class="sxs-lookup"><span data-stu-id="b6e2a-130">**WTSSBX\_MACHINE\_CONNECT\_INFO**</span></span>](/windows/win32/api/tssbx/ns-tssbx-wtssbx_machine_connect_info)
</dt> <dd>

<span data-ttu-id="b6e2a-131">Contém informações sobre um computador que está aceitando conexões remotas.</span><span class="sxs-lookup"><span data-stu-id="b6e2a-131">Contains information about a computer that is accepting remote connections.</span></span>

</dd> <dt>

[<span data-ttu-id="b6e2a-132">**\_informações do computador WTSSBX \_**</span><span class="sxs-lookup"><span data-stu-id="b6e2a-132">**WTSSBX\_MACHINE\_INFO**</span></span>](/windows/win32/api/tssbx/ns-tssbx-wtssbx_machine_info)
</dt> <dd>

<span data-ttu-id="b6e2a-133">Contém informações sobre um computador e seu estado atual.</span><span class="sxs-lookup"><span data-stu-id="b6e2a-133">Contains information about a computer and its current state.</span></span>

</dd> <dt>

[<span data-ttu-id="b6e2a-134">**\_informações da sessão WTSSBX \_**</span><span class="sxs-lookup"><span data-stu-id="b6e2a-134">**WTSSBX\_SESSION\_INFO**</span></span>](/windows/win32/api/tssbx/ns-tssbx-wtssbx_session_info)
</dt> <dd>

<span data-ttu-id="b6e2a-135">Contém informações sobre as sessões que estão disponíveis para Conexão de Área de Trabalho Remota Agente (agente de conexão RD).</span><span class="sxs-lookup"><span data-stu-id="b6e2a-135">Contains information about sessions that are available to Remote Desktop Connection Broker (RD Connection Broker).</span></span>

</dd> <dt>

[<span data-ttu-id="b6e2a-136">**notificação de WTSSESSION \_**</span><span class="sxs-lookup"><span data-stu-id="b6e2a-136">**WTSSESSION\_NOTIFICATION**</span></span>](/windows/win32/api/winuser/ns-winuser-wtssession_notification)
</dt> <dd>

<span data-ttu-id="b6e2a-137">Fornece informações sobre a notificação de alteração de sessão.</span><span class="sxs-lookup"><span data-stu-id="b6e2a-137">Provides information about the session change notification.</span></span> <span data-ttu-id="b6e2a-138">Um serviço recebe essa estrutura em sua função [*HandlerEx*](/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex) em resposta a um evento de alteração de sessão.</span><span class="sxs-lookup"><span data-stu-id="b6e2a-138">A service receives this structure in its [*HandlerEx*](/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex) function in response to a session change event.</span></span>

</dd> <dt>

[<span data-ttu-id="b6e2a-139">**WTSUSERCONFIG**</span><span class="sxs-lookup"><span data-stu-id="b6e2a-139">**WTSUSERCONFIG**</span></span>](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtsuserconfiga)
</dt> <dd>

<span data-ttu-id="b6e2a-140">Contém informações de configuração para um usuário em um controlador de domínio ou em um servidor Host da Sessão da Área de Trabalho Remota (Host da Sessão RD).</span><span class="sxs-lookup"><span data-stu-id="b6e2a-140">Contains configuration information for a user on a domain controller or Remote Desktop Session Host (RD Session Host) server.</span></span>

</dd> <dt>

[<span data-ttu-id="b6e2a-141">**\_endereço do cliente WTS \_**</span><span class="sxs-lookup"><span data-stu-id="b6e2a-141">**WTS\_CLIENT\_ADDRESS**</span></span>](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_client_address)
</dt> <dd>

<span data-ttu-id="b6e2a-142">Contém o endereço de rede do cliente de uma sessão de Serviços de Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="b6e2a-142">Contains the client network address of a Remote Desktop Services session.</span></span>

</dd> <dt>

[<span data-ttu-id="b6e2a-143">**\_exibição do cliente WTS \_**</span><span class="sxs-lookup"><span data-stu-id="b6e2a-143">**WTS\_CLIENT\_DISPLAY**</span></span>](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_client_display)
</dt> <dd>

<span data-ttu-id="b6e2a-144">Contém informações sobre a exibição de um cliente de Conexão de Área de Trabalho Remota (RDC).</span><span class="sxs-lookup"><span data-stu-id="b6e2a-144">Contains information about the display of a Remote Desktop Connection (RDC) client.</span></span>

</dd> <dt>

[<span data-ttu-id="b6e2a-145">**\_informações do processo WTS \_**</span><span class="sxs-lookup"><span data-stu-id="b6e2a-145">**WTS\_PROCESS\_INFO**</span></span>](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_process_infoa)
</dt> <dd>

<span data-ttu-id="b6e2a-146">Contém informações sobre um processo em execução em um servidor de Host da Sessão RD.</span><span class="sxs-lookup"><span data-stu-id="b6e2a-146">Contains information about a process running on a RD Session Host server.</span></span>

</dd> <dt>

[<span data-ttu-id="b6e2a-147">**informações do processo WTS por \_ \_ \_ exemplo**</span><span class="sxs-lookup"><span data-stu-id="b6e2a-147">**WTS\_PROCESS\_INFO\_EX**</span></span>](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_process_info_exa)
</dt> <dd>

<span data-ttu-id="b6e2a-148">Contém informações estendidas sobre um processo em execução em um servidor de Host da Sessão RD.</span><span class="sxs-lookup"><span data-stu-id="b6e2a-148">Contains extended information about a process running on a RD Session Host server.</span></span>

</dd> <dt>

<span data-ttu-id="b6e2a-149">[**\_informações do produto WTS \_**](https://msdn.microsoft.com/library/Mt283722(v=VS.85).aspx)</span><span class="sxs-lookup"><span data-stu-id="b6e2a-149">[**WTS\_PRODUCT\_INFO**](https://msdn.microsoft.com/library/Mt283722(v=VS.85).aspx)</span></span>
</dt> <dd>

<span data-ttu-id="b6e2a-150">Os detalhes da licença de produto que é necessária para se conectar a um servidor de terminal.</span><span class="sxs-lookup"><span data-stu-id="b6e2a-150">The details of the product license that is required to connect to a terminal server.</span></span>

</dd> <dt>

[<span data-ttu-id="b6e2a-151">**\_informações do servidor WTS \_**</span><span class="sxs-lookup"><span data-stu-id="b6e2a-151">**WTS\_SERVER\_INFO**</span></span>](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_server_infoa)
</dt> <dd>

<span data-ttu-id="b6e2a-152">Contém informações sobre um servidor Serviços de Área de Trabalho Remota específico.</span><span class="sxs-lookup"><span data-stu-id="b6e2a-152">Contains information about a specific Remote Desktop Services server.</span></span>

</dd> <dt>

[<span data-ttu-id="b6e2a-153">**\_endereço da sessão WTS \_**</span><span class="sxs-lookup"><span data-stu-id="b6e2a-153">**WTS\_SESSION\_ADDRESS**</span></span>](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_session_address)
</dt> <dd>

<span data-ttu-id="b6e2a-154">Contém o endereço IP virtual atribuído a uma sessão.</span><span class="sxs-lookup"><span data-stu-id="b6e2a-154">Contains the virtual IP address assigned to a session.</span></span>

</dd> <dt>

[<span data-ttu-id="b6e2a-155">**\_informações da sessão WTS \_**</span><span class="sxs-lookup"><span data-stu-id="b6e2a-155">**WTS\_SESSION\_INFO**</span></span>](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_session_infoa)
</dt> <dd>

<span data-ttu-id="b6e2a-156">Contém informações sobre uma sessão de cliente em um servidor de Host da Sessão RD.</span><span class="sxs-lookup"><span data-stu-id="b6e2a-156">Contains information about a client session on a RD Session Host server.</span></span>

</dd> <dt>

[<span data-ttu-id="b6e2a-157">**Informações de sessão do WTS \_ \_ \_ 1**</span><span class="sxs-lookup"><span data-stu-id="b6e2a-157">**WTS\_SESSION\_INFO\_1**</span></span>](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_session_info_1a)
</dt> <dd>

<span data-ttu-id="b6e2a-158">Contém informações estendidas sobre uma sessão de cliente em um servidor de Host da Sessão RD ou Host de Virtualização de Área de Trabalho Remota (host de virtualização de área de trabalho remota).</span><span class="sxs-lookup"><span data-stu-id="b6e2a-158">Contains extended information about a client session on a RD Session Host server or Remote Desktop Virtualization Host (RD Virtualization Host) server.</span></span>

</dd> </dl>

 

 