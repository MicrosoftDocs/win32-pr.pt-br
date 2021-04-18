---
description: Algumas das opções de soquete do Windows Sockets 2 são resumidas na tabela a seguir.
ms.assetid: 6731d27c-fb7d-421a-badf-0cad6a4712ea
title: Opções de soquete e IOCTLs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 472d37bd8d2d97eead66d7c9d2319e57fc5dafde
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105814561"
---
# <a name="socket-options-and-ioctls"></a><span data-ttu-id="0faad-103">Opções de soquete e IOCTLs</span><span class="sxs-lookup"><span data-stu-id="0faad-103">Socket Options and IOCTLs</span></span>

<span data-ttu-id="0faad-104">Algumas das opções de soquete do Windows Sockets 2 são resumidas na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="0faad-104">Some of the socket options for Windows Sockets 2 are summarized in the following table.</span></span> <span data-ttu-id="0faad-105">Informações mais detalhadas são fornecidas na seção 4 em [**WSPGetSockOpt**](/previous-versions/windows/hardware/network/ff566292(v=vs.85)) e/ou [**WSPSetSockOpt**](/previous-versions/windows/hardware/network/ff566318(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="0faad-105">More detailed information is provided in section 4 under [**WSPGetSockOpt**](/previous-versions/windows/hardware/network/ff566292(v=vs.85)) and/or [**WSPSetSockOpt**](/previous-versions/windows/hardware/network/ff566318(v=vs.85)).</span></span> <span data-ttu-id="0faad-106">Há outras novas opções de soquete específicas de protocolo que podem ser encontradas no anexo Protocol-Specific.</span><span class="sxs-lookup"><span data-stu-id="0faad-106">There are other new protocol-specific socket options which can be found in the Protocol-Specific Annex.</span></span> <span data-ttu-id="0faad-107">Uma lista completa de [**Opções de soquete**](socket-options.md) para Windows Sockets está disponível na referência do Winsock.</span><span class="sxs-lookup"><span data-stu-id="0faad-107">A complete list of [**Socket Options**](socket-options.md) for Windows Sockets are available in the Winsock reference.</span></span>

<span data-ttu-id="0faad-108">Para obter um resumo de alguns dos IOCTLs do Winsock, consulte [Resumo dos opcodes do soquete do IOCTL](summary-of-socket-ioctl-opcodes-2.md).</span><span class="sxs-lookup"><span data-stu-id="0faad-108">For a a summary of some of the Winsock Ioctls, see [Summary of Socket Ioctl Opcodes](summary-of-socket-ioctl-opcodes-2.md).</span></span> <span data-ttu-id="0faad-109">Uma lista completa de [**IOCTLs do Winsock**](winsock-ioctls.md) está disponível na referência do Winsock.</span><span class="sxs-lookup"><span data-stu-id="0faad-109">A complete list of [**Winsock IOCTLs**](winsock-ioctls.md) are available in the Winsock reference.</span></span>

## <a name="summary-of-common-socket-options"></a><span data-ttu-id="0faad-110">Resumo das opções de soquetes comuns</span><span class="sxs-lookup"><span data-stu-id="0faad-110">Summary of Common Socket Options</span></span>

<span data-ttu-id="0faad-111">Um provedor de serviços Winsock deve reconhecer todas essas opções e (para [**WSPGetSockOpt**](/previous-versions/windows/hardware/network/ff566292(v=vs.85))) retornar valores plausível para cada.</span><span class="sxs-lookup"><span data-stu-id="0faad-111">A Winsock service provider must recognize all of these options, and (for [**WSPGetSockOpt**](/previous-versions/windows/hardware/network/ff566292(v=vs.85))) return plausible values for each.</span></span> <span data-ttu-id="0faad-112">O valor padrão para cada opção é mostrado na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="0faad-112">The default value for each option is shown in the following table.</span></span>

<span data-ttu-id="0faad-113">Valor</span><span class="sxs-lookup"><span data-stu-id="0faad-113">Value</span></span>

<span data-ttu-id="0faad-114">Type</span><span class="sxs-lookup"><span data-stu-id="0faad-114">Type</span></span>

<span data-ttu-id="0faad-115">Significado</span><span class="sxs-lookup"><span data-stu-id="0faad-115">Meaning</span></span>

<span data-ttu-id="0faad-116">Padrão</span><span class="sxs-lookup"><span data-stu-id="0faad-116">Default</span></span>

<span data-ttu-id="0faad-117">Observação</span><span class="sxs-lookup"><span data-stu-id="0faad-117">Note</span></span>

<span data-ttu-id="0faad-118"><span id="SO_ACCEPTCONN"></span><span id="so_acceptconn"></span>\_ACCEPTCONN</span><span class="sxs-lookup"><span data-stu-id="0faad-118"><span id="SO_ACCEPTCONN"></span><span id="so_acceptconn"></span>SO\_ACCEPTCONN</span></span>

<span data-ttu-id="0faad-119">BOOL</span><span class="sxs-lookup"><span data-stu-id="0faad-119">BOOL</span></span>

<span data-ttu-id="0faad-120">O soquete está ouvindo.</span><span class="sxs-lookup"><span data-stu-id="0faad-120">Socket is listening.</span></span>

<span data-ttu-id="0faad-121">FALSE, a menos que um [**WSPListen**](/previous-versions/windows/hardware/network/ff566297(v=vs.85)) tenha sido executado.</span><span class="sxs-lookup"><span data-stu-id="0faad-121">FALSE unless a [**WSPListen**](/previous-versions/windows/hardware/network/ff566297(v=vs.85)) has been performed.</span></span>

<span data-ttu-id="0faad-122"><span id="SO_BROADCAST"></span><span id="so_broadcast"></span>\_difusão</span><span class="sxs-lookup"><span data-stu-id="0faad-122"><span id="SO_BROADCAST"></span><span id="so_broadcast"></span>SO\_BROADCAST</span></span>

<span data-ttu-id="0faad-123">BOOL</span><span class="sxs-lookup"><span data-stu-id="0faad-123">BOOL</span></span>

<span data-ttu-id="0faad-124">O soquete está configurado para a transmissão e o recebimento de mensagens de difusão.</span><span class="sxs-lookup"><span data-stu-id="0faad-124">Socket is configured for the transmission and receipt of broadcast messages.</span></span>

<span data-ttu-id="0faad-125">FALSE</span><span class="sxs-lookup"><span data-stu-id="0faad-125">FALSE</span></span>

<span data-ttu-id="0faad-126"><span id="SO_DEBUG"></span><span id="so_debug"></span>\_depuração</span><span class="sxs-lookup"><span data-stu-id="0faad-126"><span id="SO_DEBUG"></span><span id="so_debug"></span>SO\_DEBUG</span></span>

<span data-ttu-id="0faad-127">BOOL</span><span class="sxs-lookup"><span data-stu-id="0faad-127">BOOL</span></span>

<span data-ttu-id="0faad-128">A depuração está habilitada.</span><span class="sxs-lookup"><span data-stu-id="0faad-128">Debugging is enabled.</span></span>

<span data-ttu-id="0faad-129">FALSE</span><span class="sxs-lookup"><span data-stu-id="0faad-129">FALSE</span></span>

<span data-ttu-id="0faad-130">Encontrei</span><span class="sxs-lookup"><span data-stu-id="0faad-130">(i)</span></span>

<span data-ttu-id="0faad-131"><span id="SO_DONTLINGER"></span><span id="so_dontlinger"></span>\_DONTLINGER</span><span class="sxs-lookup"><span data-stu-id="0faad-131"><span id="SO_DONTLINGER"></span><span id="so_dontlinger"></span>SO\_DONTLINGER</span></span>

<span data-ttu-id="0faad-132">BOOL</span><span class="sxs-lookup"><span data-stu-id="0faad-132">BOOL</span></span>

<span data-ttu-id="0faad-133">Se for true, a \_ opção for remanescente será desabilitada.</span><span class="sxs-lookup"><span data-stu-id="0faad-133">If true, the SO\_LINGER option is disabled.</span></span>

<span data-ttu-id="0faad-134">TRUE</span><span class="sxs-lookup"><span data-stu-id="0faad-134">TRUE</span></span>

<span data-ttu-id="0faad-135"><span id="SO_DONTROUTE"></span><span id="so_dontroute"></span>\_DONTROUTE</span><span class="sxs-lookup"><span data-stu-id="0faad-135"><span id="SO_DONTROUTE"></span><span id="so_dontroute"></span>SO\_DONTROUTE</span></span>

<span data-ttu-id="0faad-136">BOOL</span><span class="sxs-lookup"><span data-stu-id="0faad-136">BOOL</span></span>

<span data-ttu-id="0faad-137">O roteamento está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="0faad-137">Routing is disabled.</span></span> <span data-ttu-id="0faad-138">É bem-sucedida, mas é ignorado em \_ soquetes inet de AF; falha em \_ soquetes INET6 de AF com [WSAENOPROTOOPT](windows-sockets-error-codes-2.md).</span><span class="sxs-lookup"><span data-stu-id="0faad-138">Succeeds but is ignored on AF\_INET sockets; fails on AF\_INET6 sockets with [WSAENOPROTOOPT](windows-sockets-error-codes-2.md).</span></span> <span data-ttu-id="0faad-139">Sem suporte em Soquetes ATM (resulta em um erro).</span><span class="sxs-lookup"><span data-stu-id="0faad-139">Not supported on ATM sockets (results in an error).</span></span>

<span data-ttu-id="0faad-140">FALSE</span><span class="sxs-lookup"><span data-stu-id="0faad-140">FALSE</span></span>

<span data-ttu-id="0faad-141">Encontrei</span><span class="sxs-lookup"><span data-stu-id="0faad-141">(i)</span></span>

<span data-ttu-id="0faad-142"><span id="SO_ERROR"></span><span id="so_error"></span>\_erro</span><span class="sxs-lookup"><span data-stu-id="0faad-142"><span id="SO_ERROR"></span><span id="so_error"></span>SO\_ERROR</span></span>

<span data-ttu-id="0faad-143">INT</span><span class="sxs-lookup"><span data-stu-id="0faad-143">int</span></span>

<span data-ttu-id="0faad-144">Recupera o status de erro e limpe.</span><span class="sxs-lookup"><span data-stu-id="0faad-144">Retrieves error status and clear.</span></span>

<span data-ttu-id="0faad-145">0</span><span class="sxs-lookup"><span data-stu-id="0faad-145">0</span></span>

<span data-ttu-id="0faad-146"><span id="SO_GROUP_ID"></span><span id="so_group_id"></span>Portanto, a \_ ID do grupo \_</span><span class="sxs-lookup"><span data-stu-id="0faad-146"><span id="SO_GROUP_ID"></span><span id="so_group_id"></span>SO\_GROUP\_ID</span></span>

<span data-ttu-id="0faad-147">GROUP</span><span class="sxs-lookup"><span data-stu-id="0faad-147">GROUP</span></span>

<span data-ttu-id="0faad-148">Reservado.</span><span class="sxs-lookup"><span data-stu-id="0faad-148">Reserved.</span></span>

<span data-ttu-id="0faad-149">NULO</span><span class="sxs-lookup"><span data-stu-id="0faad-149">NULL</span></span>

<span data-ttu-id="0faad-150">Obter somente</span><span class="sxs-lookup"><span data-stu-id="0faad-150">Get only</span></span>

<span data-ttu-id="0faad-151"><span id="SO_GROUP_PRIORITY"></span><span id="so_group_priority"></span>Portanto \_ , \_ prioridade de grupo</span><span class="sxs-lookup"><span data-stu-id="0faad-151"><span id="SO_GROUP_PRIORITY"></span><span id="so_group_priority"></span>SO\_GROUP\_PRIORITY</span></span>

<span data-ttu-id="0faad-152">INT</span><span class="sxs-lookup"><span data-stu-id="0faad-152">int</span></span>

<span data-ttu-id="0faad-153">Reservado.</span><span class="sxs-lookup"><span data-stu-id="0faad-153">Reserved.</span></span>

<span data-ttu-id="0faad-154">0</span><span class="sxs-lookup"><span data-stu-id="0faad-154">0</span></span>

[<span data-ttu-id="0faad-155">**Portanto, \_ KeepAlive**</span><span class="sxs-lookup"><span data-stu-id="0faad-155">**SO\_KEEPALIVE**</span></span>](so-keepalive.md)

<span data-ttu-id="0faad-156">BOOL</span><span class="sxs-lookup"><span data-stu-id="0faad-156">BOOL</span></span>

<span data-ttu-id="0faad-157">As keepalives estão sendo enviadas.</span><span class="sxs-lookup"><span data-stu-id="0faad-157">Keepalives are being sent.</span></span> <span data-ttu-id="0faad-158">Sem suporte em Soquetes ATM (resulta em um erro).</span><span class="sxs-lookup"><span data-stu-id="0faad-158">Not supported on ATM sockets (results in an error).</span></span>

<span data-ttu-id="0faad-159">FALSE</span><span class="sxs-lookup"><span data-stu-id="0faad-159">FALSE</span></span>

<span data-ttu-id="0faad-160">Encontrei</span><span class="sxs-lookup"><span data-stu-id="0faad-160">(i)</span></span>

<span data-ttu-id="0faad-161"><span id="SO_LINGER"></span><span id="so_linger"></span>Então, \_ remanescente</span><span class="sxs-lookup"><span data-stu-id="0faad-161"><span id="SO_LINGER"></span><span id="so_linger"></span>SO\_LINGER</span></span>

<span data-ttu-id="0faad-162">Estrutura persistente</span><span class="sxs-lookup"><span data-stu-id="0faad-162">Structure linger</span></span>

<span data-ttu-id="0faad-163">Retorna as opções atuais remanescentes.</span><span class="sxs-lookup"><span data-stu-id="0faad-163">Returns the current linger options.</span></span>

<span data-ttu-id="0faad-164">l \_ Onoff é 0</span><span class="sxs-lookup"><span data-stu-id="0faad-164">l\_onoff is 0</span></span>

<span data-ttu-id="0faad-165"><span id="SO_MAX_MSG_SIZE"></span><span id="so_max_msg_size"></span>Portanto \_ , \_ tamanho máximo da mensagem \_</span><span class="sxs-lookup"><span data-stu-id="0faad-165"><span id="SO_MAX_MSG_SIZE"></span><span id="so_max_msg_size"></span>SO\_MAX\_MSG\_SIZE</span></span>

<span data-ttu-id="0faad-166">INT</span><span class="sxs-lookup"><span data-stu-id="0faad-166">int</span></span>

<span data-ttu-id="0faad-167">Tamanho máximo de saída de uma mensagem para tipos de soquete de mensagem.</span><span class="sxs-lookup"><span data-stu-id="0faad-167">Maximum outbound size of a message for message socket types.</span></span> <span data-ttu-id="0faad-168">Não há nenhuma provisão para determinar o tamanho máximo da mensagem de entrada.</span><span class="sxs-lookup"><span data-stu-id="0faad-168">There is no provision to determine the maximum inbound message size.</span></span> <span data-ttu-id="0faad-169">Não tem significado para soquetes orientados a fluxo.</span><span class="sxs-lookup"><span data-stu-id="0faad-169">Has no meaning for stream-oriented sockets.</span></span>

<span data-ttu-id="0faad-170">Dependente de implementação</span><span class="sxs-lookup"><span data-stu-id="0faad-170">Implementation dependent</span></span>

<span data-ttu-id="0faad-171">Obter somente</span><span class="sxs-lookup"><span data-stu-id="0faad-171">Get only</span></span>

<span data-ttu-id="0faad-172"><span id="SO_OOBINLINE"></span><span id="so_oobinline"></span>\_OOBINLINE</span><span class="sxs-lookup"><span data-stu-id="0faad-172"><span id="SO_OOBINLINE"></span><span id="so_oobinline"></span>SO\_OOBINLINE</span></span>

<span data-ttu-id="0faad-173">BOOL</span><span class="sxs-lookup"><span data-stu-id="0faad-173">BOOL</span></span>

<span data-ttu-id="0faad-174">Os dados OOB estão sendo recebidos no fluxo de dados normal.</span><span class="sxs-lookup"><span data-stu-id="0faad-174">OOB data is being received in the normal data stream.</span></span>

<span data-ttu-id="0faad-175">FALSE</span><span class="sxs-lookup"><span data-stu-id="0faad-175">FALSE</span></span>

<span data-ttu-id="0faad-176"><span id="SO_PROTOCOL_INFOW"></span><span id="so_protocol_infow"></span>Portanto \_ , \_ INFOW de protocolo</span><span class="sxs-lookup"><span data-stu-id="0faad-176"><span id="SO_PROTOCOL_INFOW"></span><span id="so_protocol_infow"></span>SO\_PROTOCOL\_INFOW</span></span>

<span data-ttu-id="0faad-177">[ **\_ informações de WSAPROTOCOL** de estrutura](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa)</span><span class="sxs-lookup"><span data-stu-id="0faad-177">structure [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa)</span></span>

<span data-ttu-id="0faad-178">Descrição das informações de protocolo para o protocolo que está associado a este Soquete.</span><span class="sxs-lookup"><span data-stu-id="0faad-178">Description of protocol information for the protocol that is bound to this socket.</span></span>

<span data-ttu-id="0faad-179">Dependente de protocolo</span><span class="sxs-lookup"><span data-stu-id="0faad-179">Protocol dependent</span></span>

<span data-ttu-id="0faad-180">Obter somente</span><span class="sxs-lookup"><span data-stu-id="0faad-180">Get only</span></span>

<span data-ttu-id="0faad-181"><span id="SO_RCVBUF"></span><span id="so_rcvbuf"></span>\_RCVBUF</span><span class="sxs-lookup"><span data-stu-id="0faad-181"><span id="SO_RCVBUF"></span><span id="so_rcvbuf"></span>SO\_RCVBUF</span></span>

<span data-ttu-id="0faad-182">INT</span><span class="sxs-lookup"><span data-stu-id="0faad-182">int</span></span>

<span data-ttu-id="0faad-183">O espaço total de buffer por soquete reservado para receives.</span><span class="sxs-lookup"><span data-stu-id="0faad-183">The total per-socket buffer space reserved for receives.</span></span> <span data-ttu-id="0faad-184">Isso não está relacionado ao \_ tamanho máximo \_ \_ da mensagem e não corresponde necessariamente ao tamanho da janela de recepção TCP.</span><span class="sxs-lookup"><span data-stu-id="0faad-184">This is unrelated to SO\_MAX\_MSG\_SIZE and does not necessarily correspond to the size of the TCP receive window.</span></span>

<span data-ttu-id="0faad-185">Dependente de implementação</span><span class="sxs-lookup"><span data-stu-id="0faad-185">Implementation dependent</span></span>

<span data-ttu-id="0faad-186">Encontrei</span><span class="sxs-lookup"><span data-stu-id="0faad-186">(i)</span></span>

<span data-ttu-id="0faad-187"><span id="SO_REUSEADDR"></span><span id="so_reuseaddr"></span>\_REUSEADDR</span><span class="sxs-lookup"><span data-stu-id="0faad-187"><span id="SO_REUSEADDR"></span><span id="so_reuseaddr"></span>SO\_REUSEADDR</span></span>

<span data-ttu-id="0faad-188">BOOL</span><span class="sxs-lookup"><span data-stu-id="0faad-188">BOOL</span></span>

<span data-ttu-id="0faad-189">O endereço ao qual esse soquete está associado pode ser usado por outras pessoas.</span><span class="sxs-lookup"><span data-stu-id="0faad-189">The address to which this socket is bound can be used by others.</span></span> <span data-ttu-id="0faad-190">Não aplicável em Soquetes ATM.</span><span class="sxs-lookup"><span data-stu-id="0faad-190">Not applicable on ATM sockets.</span></span>

<span data-ttu-id="0faad-191">FALSE</span><span class="sxs-lookup"><span data-stu-id="0faad-191">FALSE</span></span>

<span data-ttu-id="0faad-192"><span id="SO_SNDBUF"></span><span id="so_sndbuf"></span>\_SNDBUF</span><span class="sxs-lookup"><span data-stu-id="0faad-192"><span id="SO_SNDBUF"></span><span id="so_sndbuf"></span>SO\_SNDBUF</span></span>

<span data-ttu-id="0faad-193">INT</span><span class="sxs-lookup"><span data-stu-id="0faad-193">int</span></span>

<span data-ttu-id="0faad-194">O espaço total de buffer por soquete reservado para envios.</span><span class="sxs-lookup"><span data-stu-id="0faad-194">The total per-socket buffer space reserved for sends.</span></span> <span data-ttu-id="0faad-195">Isso não está relacionado ao \_ tamanho máximo \_ \_ da mensagem e não corresponde necessariamente ao tamanho de uma janela de envio TCP.</span><span class="sxs-lookup"><span data-stu-id="0faad-195">This is unrelated to SO\_MAX\_MSG\_SIZE and does not necessarily correspond to the size of a TCP send window.</span></span>

<span data-ttu-id="0faad-196">Dependente de implementação</span><span class="sxs-lookup"><span data-stu-id="0faad-196">Implementation dependent</span></span>

<span data-ttu-id="0faad-197">Encontrei</span><span class="sxs-lookup"><span data-stu-id="0faad-197">(i)</span></span>

<span data-ttu-id="0faad-198"><span id="SO_TYPE"></span><span id="so_type"></span>Portanto, \_ digite</span><span class="sxs-lookup"><span data-stu-id="0faad-198"><span id="SO_TYPE"></span><span id="so_type"></span>SO\_TYPE</span></span>

<span data-ttu-id="0faad-199">INT</span><span class="sxs-lookup"><span data-stu-id="0faad-199">int</span></span>

<span data-ttu-id="0faad-200">O tipo de soquete (por exemplo, fluxo de SOCK \_ ).</span><span class="sxs-lookup"><span data-stu-id="0faad-200">The type of the socket (for example, SOCK\_STREAM).</span></span>

<span data-ttu-id="0faad-201">Conforme criado por meio do soquete.</span><span class="sxs-lookup"><span data-stu-id="0faad-201">As created through socket.</span></span>

<span data-ttu-id="0faad-202"><span id="PVD_CONFIG"></span><span id="pvd_config"></span>configuração do PVD \_</span><span class="sxs-lookup"><span data-stu-id="0faad-202"><span id="PVD_CONFIG"></span><span id="pvd_config"></span>PVD\_CONFIG</span></span>

<span data-ttu-id="0faad-203">caractere de longe \*</span><span class="sxs-lookup"><span data-stu-id="0faad-203">char FAR \*</span></span>

<span data-ttu-id="0faad-204">Um objeto de estrutura de dados opaco que contém informações de configuração do provedor de serviços.</span><span class="sxs-lookup"><span data-stu-id="0faad-204">An opaque data structure object containing configuration information of the service provider.</span></span>

<span data-ttu-id="0faad-205">Dependente de implementação</span><span class="sxs-lookup"><span data-stu-id="0faad-205">Implementation dependent</span></span>

<span data-ttu-id="0faad-206"><span id="TCP_NODELAY"></span><span id="tcp_nodelay"></span>TCP \_ NOdelay</span><span class="sxs-lookup"><span data-stu-id="0faad-206"><span id="TCP_NODELAY"></span><span id="tcp_nodelay"></span>TCP\_NODELAY</span></span>

<span data-ttu-id="0faad-207">BOOL</span><span class="sxs-lookup"><span data-stu-id="0faad-207">BOOL</span></span>

<span data-ttu-id="0faad-208">Desabilita o algoritmo Nagle para união de envio.</span><span class="sxs-lookup"><span data-stu-id="0faad-208">Disables the Nagle algorithm for send coalescing.</span></span>

<span data-ttu-id="0faad-209">Dependente de implementação</span><span class="sxs-lookup"><span data-stu-id="0faad-209">Implementation dependent</span></span>

<span data-ttu-id="0faad-210">(i) um provedor de serviços pode ignorar silenciosamente essa opção em [**WSPSetSockOpt**](/previous-versions/windows/hardware/network/ff566318(v=vs.85)) e retornar um valor constante para [**WSPGetSockOpt**](/previous-versions/windows/hardware/network/ff566292(v=vs.85)), ou pode aceitar um valor para **WSPSetSockOpt** e retornar o valor correspondente em **WSPGetSockOpt** sem usar o valor de forma alguma.</span><span class="sxs-lookup"><span data-stu-id="0faad-210">(i) A service provider may silently ignore this option on [**WSPSetSockOpt**](/previous-versions/windows/hardware/network/ff566318(v=vs.85)) and return a constant value for [**WSPGetSockOpt**](/previous-versions/windows/hardware/network/ff566292(v=vs.85)), or it may accept a value for **WSPSetSockOpt** and return the corresponding value in **WSPGetSockOpt** without using the value in any way.</span></span>



 

## <a name="related-topics"></a><span data-ttu-id="0faad-211">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0faad-211">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0faad-212">**Opções de soquete**</span><span class="sxs-lookup"><span data-stu-id="0faad-212">**Socket Options**</span></span>](socket-options.md)
</dt> <dt>

[<span data-ttu-id="0faad-213">**Opções de soquete de soquete de SOL \_**</span><span class="sxs-lookup"><span data-stu-id="0faad-213">**SOL\_SOCKET Socket Options**</span></span>](sol-socket-socket-options.md)
</dt> <dt>

[<span data-ttu-id="0faad-214">**\_Opções de soquete TCP IPPROTO**</span><span class="sxs-lookup"><span data-stu-id="0faad-214">**IPPROTO\_TCP Socket Options**</span></span>](ipproto-tcp-socket-options.md)
</dt> <dt>

[<span data-ttu-id="0faad-215">**\_Opções de soquete UDP IPPROTO**</span><span class="sxs-lookup"><span data-stu-id="0faad-215">**IPPROTO\_UDP Socket Options**</span></span>](ipproto-udp-socket-options.md)
</dt> <dt>

[<span data-ttu-id="0faad-216">**Winsock IOCTLs**</span><span class="sxs-lookup"><span data-stu-id="0faad-216">**Winsock IOCTLs**</span></span>](winsock-ioctls.md)
</dt> </dl>

 

 
