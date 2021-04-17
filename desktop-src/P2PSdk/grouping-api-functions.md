---
description: 'A API de agrupamento do usa as seguintes funções:'
ms.assetid: 56ea2880-b468-4816-b6c9-5780c807b3f1
title: Agrupando funções de API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17d2970ca68d69b16a32cf7a6d546a5852b07dd0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105754516"
---
# <a name="grouping-api-functions"></a><span data-ttu-id="7ae81-103">Agrupando funções de API</span><span class="sxs-lookup"><span data-stu-id="7ae81-103">Grouping API Functions</span></span>

<span data-ttu-id="7ae81-104">A API de agrupamento do usa as seguintes funções:</span><span class="sxs-lookup"><span data-stu-id="7ae81-104">The Grouping API uses the following functions:</span></span>

## <a name="group-initialization-and-cleanup-functions"></a><span data-ttu-id="7ae81-105">Funções de inicialização e limpeza de grupo</span><span class="sxs-lookup"><span data-stu-id="7ae81-105">Group Initialization and Cleanup Functions</span></span>



| <span data-ttu-id="7ae81-106">Função</span><span class="sxs-lookup"><span data-stu-id="7ae81-106">Function</span></span>                                       | <span data-ttu-id="7ae81-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="7ae81-107">Description</span></span>                                                                                                            |
|------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7ae81-108">**PeerGroupShutdown**</span><span class="sxs-lookup"><span data-stu-id="7ae81-108">**PeerGroupShutdown**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupshutdown) | <span data-ttu-id="7ae81-109">Fecha um grupo de pares criado com [**PeerGroupStartup**](/windows/desktop/api/P2P/nf-p2p-peergroupstartup) e descarta todos os recursos alocados.</span><span class="sxs-lookup"><span data-stu-id="7ae81-109">Closes a peer group created with [**PeerGroupStartup**](/windows/desktop/api/P2P/nf-p2p-peergroupstartup) and disposes of any allocated resources.</span></span> |
| [<span data-ttu-id="7ae81-110">**PeerGroupStartup**</span><span class="sxs-lookup"><span data-stu-id="7ae81-110">**PeerGroupStartup**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupstartup)   | <span data-ttu-id="7ae81-111">Inicia um grupo de pares usando uma versão solicitada da infraestrutura de pares.</span><span class="sxs-lookup"><span data-stu-id="7ae81-111">Initiates a peer group by using a requested version of the Peer infrastructure.</span></span>                                        |



 

## <a name="group-creation-and-access-functions"></a><span data-ttu-id="7ae81-112">Funções de criação e acesso de grupo</span><span class="sxs-lookup"><span data-stu-id="7ae81-112">Group Creation and Access Functions</span></span>



| <span data-ttu-id="7ae81-113">Função</span><span class="sxs-lookup"><span data-stu-id="7ae81-113">Function</span></span>                                                                       | <span data-ttu-id="7ae81-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="7ae81-114">Description</span></span>                                                                                                                                                                                                  |
|--------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7ae81-115">**PeerGroupClose**</span><span class="sxs-lookup"><span data-stu-id="7ae81-115">**PeerGroupClose**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupclose)                                       | <span data-ttu-id="7ae81-116">Invalida o identificador de grupo de pares obtido por uma chamada anterior para a função [**PeerGroupCreate**](/windows/desktop/api/P2P/nf-p2p-peergroupcreate), [**PeerGroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin)ou [**PeerGroupOpen**](/windows/desktop/api/P2P/nf-p2p-peergroupopen) .</span><span class="sxs-lookup"><span data-stu-id="7ae81-116">Invalidates the peer group handle obtained by a previous call to the [**PeerGroupCreate**](/windows/desktop/api/P2P/nf-p2p-peergroupcreate), [**PeerGroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin), or [**PeerGroupOpen**](/windows/desktop/api/P2P/nf-p2p-peergroupopen) function.</span></span> |
| [<span data-ttu-id="7ae81-117">**PeerGroupConnect**</span><span class="sxs-lookup"><span data-stu-id="7ae81-117">**PeerGroupConnect**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupconnect)                                   | <span data-ttu-id="7ae81-118">Inicia uma pesquisa PNRP para um grupo de pares e tenta se conectar a ele.</span><span class="sxs-lookup"><span data-stu-id="7ae81-118">Initiates a PNRP search for a peer group and attempts to connect to it.</span></span> <span data-ttu-id="7ae81-119">Depois que essa função é chamada com êxito, um par pode se comunicar com outros membros do grupo de pares.</span><span class="sxs-lookup"><span data-stu-id="7ae81-119">After this function is called successfully, a peer can communicate with other members of the peer group.</span></span>                             |
| [<span data-ttu-id="7ae81-120">**PeerGroupConnectByAddress**</span><span class="sxs-lookup"><span data-stu-id="7ae81-120">**PeerGroupConnectByAddress**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupconnectbyaddress)                 | <span data-ttu-id="7ae81-121">Tenta se conectar ao grupo de pares ao qual outros computadores com endereços IPv6 conhecidos estão participando.</span><span class="sxs-lookup"><span data-stu-id="7ae81-121">Attempts to connect to the peer group that other peers with known IPv6 addresses are participating in.</span></span>                                                                                                       |
| [<span data-ttu-id="7ae81-122">**PeerGroupCreate**</span><span class="sxs-lookup"><span data-stu-id="7ae81-122">**PeerGroupCreate**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupcreate)                                     | <span data-ttu-id="7ae81-123">Cria um novo grupo de pares.</span><span class="sxs-lookup"><span data-stu-id="7ae81-123">Creates a new peer group.</span></span>                                                                                                                                                                                    |
| [<span data-ttu-id="7ae81-124">**PeerGroupCreateInvitation**</span><span class="sxs-lookup"><span data-stu-id="7ae81-124">**PeerGroupCreateInvitation**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupcreateinvitation)                 | <span data-ttu-id="7ae81-125">Retorna uma cadeia de caracteres XML que pode ser usada pelo par especificado para ingressar em um grupo.</span><span class="sxs-lookup"><span data-stu-id="7ae81-125">Returns an XML string that can be used by the specified peer to join a group.</span></span>                                                                                                                                |
| [<span data-ttu-id="7ae81-126">**PeerGroupCreatePasswordInvitation**</span><span class="sxs-lookup"><span data-stu-id="7ae81-126">**PeerGroupCreatePasswordInvitation**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupcreatepasswordinvitation) | <span data-ttu-id="7ae81-127">Retorna uma cadeia de caracteres XML que pode ser usada pelo par especificado para ingressar em um grupo com uma senha correspondente.</span><span class="sxs-lookup"><span data-stu-id="7ae81-127">Returns an XML string that can be used by the specified peer to join a group with a matching password.</span></span>                                                                                                       |
| [<span data-ttu-id="7ae81-128">**PeerGroupDelete**</span><span class="sxs-lookup"><span data-stu-id="7ae81-128">**PeerGroupDelete**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupdelete)                                     | <span data-ttu-id="7ae81-129">Exclui os dados locais e o certificado associado a um grupo de pares.</span><span class="sxs-lookup"><span data-stu-id="7ae81-129">Deletes the local data and certificate associated with a peer group.</span></span>                                                                                                                                         |
| [<span data-ttu-id="7ae81-130">**PeerGroupGetStatus**</span><span class="sxs-lookup"><span data-stu-id="7ae81-130">**PeerGroupGetStatus**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupgetstatus)                               | <span data-ttu-id="7ae81-131">Recupera o status atual de um grupo.</span><span class="sxs-lookup"><span data-stu-id="7ae81-131">Retrieves the current status of a group.</span></span>                                                                                                                                                                     |
| [<span data-ttu-id="7ae81-132">**PeerGroupIssueCredentials**</span><span class="sxs-lookup"><span data-stu-id="7ae81-132">**PeerGroupIssueCredentials**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupissuecredentials)                 | <span data-ttu-id="7ae81-133">As credenciais de problemas, incluindo um GMC, para uma identidade específica e, opcionalmente, retornam uma cadeia de caracteres XML de convite, o ponto convidado pode usar para ingressar em um grupo de pares.</span><span class="sxs-lookup"><span data-stu-id="7ae81-133">Issues credentials, including a GMC, to a specific identity, and optionally returns an invitation XML string the invited peer can use to join a peer group.</span></span>                                                  |
| [<span data-ttu-id="7ae81-134">**PeerGroupJoin**</span><span class="sxs-lookup"><span data-stu-id="7ae81-134">**PeerGroupJoin**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupjoin)                                         | <span data-ttu-id="7ae81-135">Permite que um par com um convite ingresse em um grupo de pares existente.</span><span class="sxs-lookup"><span data-stu-id="7ae81-135">Allows a peer with an invitation to join an existing peer group.</span></span>                                                                                                                                             |
| [<span data-ttu-id="7ae81-136">**PeerGroupOpen**</span><span class="sxs-lookup"><span data-stu-id="7ae81-136">**PeerGroupOpen**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupopen)                                         | <span data-ttu-id="7ae81-137">Abre um grupo de pares que um par criou ou ingressou.</span><span class="sxs-lookup"><span data-stu-id="7ae81-137">Opens a peer group that a peer has created or joined.</span></span>                                                                                                                                                        |
| [<span data-ttu-id="7ae81-138">**PeerGroupParseInvitation**</span><span class="sxs-lookup"><span data-stu-id="7ae81-138">**PeerGroupParseInvitation**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupparseinvitation)                   | <span data-ttu-id="7ae81-139">Retorna uma estrutura de [**\_ \_ informações de convite de mesmo nível**](/windows/desktop/api/P2P/ns-p2p-peer_invitation_info) com os detalhes de um convite específico.</span><span class="sxs-lookup"><span data-stu-id="7ae81-139">Returns a [**PEER\_INVITATION\_INFO**](/windows/desktop/api/P2P/ns-p2p-peer_invitation_info) structure with the details of a specific invitation.</span></span>                                                                                        |
| [<span data-ttu-id="7ae81-140">**PeerGroupPasswordJoin**</span><span class="sxs-lookup"><span data-stu-id="7ae81-140">**PeerGroupPasswordJoin**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergrouppasswordjoin)                         | <span data-ttu-id="7ae81-141">Permite que um par com um convite e a senha correta ingressem em um grupo de pares protegido por senha.</span><span class="sxs-lookup"><span data-stu-id="7ae81-141">Allows a peer with an invitation and the correct password to join a password-protected peer group.</span></span>                                                                                                           |



 

## <a name="group-and-member-information-functions"></a><span data-ttu-id="7ae81-142">Funções de informações de grupo e membro</span><span class="sxs-lookup"><span data-stu-id="7ae81-142">Group and Member Information Functions</span></span>



| <span data-ttu-id="7ae81-143">Função</span><span class="sxs-lookup"><span data-stu-id="7ae81-143">Function</span></span>                                                 | <span data-ttu-id="7ae81-144">Descrição</span><span class="sxs-lookup"><span data-stu-id="7ae81-144">Description</span></span>                                                                                                                        |
|----------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7ae81-145">**PeerGroupEnumMembers**</span><span class="sxs-lookup"><span data-stu-id="7ae81-145">**PeerGroupEnumMembers**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupenummembers)     | <span data-ttu-id="7ae81-146">Cria uma enumeração de membros do grupo de pares disponíveis e as informações de associação associadas.</span><span class="sxs-lookup"><span data-stu-id="7ae81-146">Creates an enumeration of available peer group members and the associated membership information.</span></span>                                  |
| [<span data-ttu-id="7ae81-147">**PeerGroupGetProperties**</span><span class="sxs-lookup"><span data-stu-id="7ae81-147">**PeerGroupGetProperties**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupgetproperties) | <span data-ttu-id="7ae81-148">Recupera informações sobre as propriedades de um grupo especificado.</span><span class="sxs-lookup"><span data-stu-id="7ae81-148">Retrieves information on the properties of a specified group.</span></span>                                                                      |
| [<span data-ttu-id="7ae81-149">**PeerGroupSetProperties**</span><span class="sxs-lookup"><span data-stu-id="7ae81-149">**PeerGroupSetProperties**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupsetproperties) | <span data-ttu-id="7ae81-150">Define as propriedades atuais do grupo de pares.</span><span class="sxs-lookup"><span data-stu-id="7ae81-150">Sets the current peer group properties.</span></span> <span data-ttu-id="7ae81-151">Na versão 1,0 dessa API, somente o criador do grupo de pares pode executar essa operação.</span><span class="sxs-lookup"><span data-stu-id="7ae81-151">In version 1.0 of this API, only the creator of the peer group can perform this operation.</span></span> |



 

## <a name="records-and-record-management-functions"></a><span data-ttu-id="7ae81-152">Funções de gerenciamento de registros e registro</span><span class="sxs-lookup"><span data-stu-id="7ae81-152">Records and Record Management Functions</span></span>



| <span data-ttu-id="7ae81-153">Função</span><span class="sxs-lookup"><span data-stu-id="7ae81-153">Function</span></span>                                                 | <span data-ttu-id="7ae81-154">Descrição</span><span class="sxs-lookup"><span data-stu-id="7ae81-154">Description</span></span>                                                                          |
|----------------------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="7ae81-155">**PeerGroupAddRecord**</span><span class="sxs-lookup"><span data-stu-id="7ae81-155">**PeerGroupAddRecord**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupaddrecord)         | <span data-ttu-id="7ae81-156">Adiciona um novo registro ao grupo par, que é propagado para todos os pares participantes.</span><span class="sxs-lookup"><span data-stu-id="7ae81-156">Adds a new record to the peer group, which is propagated to all participating peers.</span></span> |
| [<span data-ttu-id="7ae81-157">**PeerGroupDeleteRecord**</span><span class="sxs-lookup"><span data-stu-id="7ae81-157">**PeerGroupDeleteRecord**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupdeleterecord)   | <span data-ttu-id="7ae81-158">Exclui um registro de um grupo de pares.</span><span class="sxs-lookup"><span data-stu-id="7ae81-158">Deletes a record from a peer group.</span></span> <span data-ttu-id="7ae81-159">Somente o criador de um registro pode excluí-lo.</span><span class="sxs-lookup"><span data-stu-id="7ae81-159">Only the creator of a record can delete it.</span></span>      |
| [<span data-ttu-id="7ae81-160">**PeerGroupEnumRecords**</span><span class="sxs-lookup"><span data-stu-id="7ae81-160">**PeerGroupEnumRecords**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupenumrecords)     | <span data-ttu-id="7ae81-161">Cria uma enumeração de registros de grupo de pares.</span><span class="sxs-lookup"><span data-stu-id="7ae81-161">Creates an enumeration of peer group records.</span></span>                                        |
| [<span data-ttu-id="7ae81-162">**PeerGroupGetRecord**</span><span class="sxs-lookup"><span data-stu-id="7ae81-162">**PeerGroupGetRecord**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupgetrecord)         | <span data-ttu-id="7ae81-163">Recupera um registro de grupo específico.</span><span class="sxs-lookup"><span data-stu-id="7ae81-163">Retrieves a specific group record.</span></span>                                                   |
| [<span data-ttu-id="7ae81-164">**PeerGroupSearchRecords**</span><span class="sxs-lookup"><span data-stu-id="7ae81-164">**PeerGroupSearchRecords**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupsearchrecords) | <span data-ttu-id="7ae81-165">Pesquisa o banco de dados do grupo par local em busca de registros que correspondam aos critérios fornecidos.</span><span class="sxs-lookup"><span data-stu-id="7ae81-165">Searches the local peer group database for records that match the supplied criteria.</span></span> |
| [<span data-ttu-id="7ae81-166">**PeerGroupUpdateRecord**</span><span class="sxs-lookup"><span data-stu-id="7ae81-166">**PeerGroupUpdateRecord**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupupdaterecord)   | <span data-ttu-id="7ae81-167">Atualiza um registro dentro de um grupo de pares específico.</span><span class="sxs-lookup"><span data-stu-id="7ae81-167">Updates a record within a specific peer group.</span></span>                                       |



 

## <a name="group-database-importexport-functions"></a><span data-ttu-id="7ae81-168">Funções de importação/exportação de banco de dados de grupo</span><span class="sxs-lookup"><span data-stu-id="7ae81-168">Group Database Import/Export Functions</span></span>



| <span data-ttu-id="7ae81-169">Função</span><span class="sxs-lookup"><span data-stu-id="7ae81-169">Function</span></span>                                                   | <span data-ttu-id="7ae81-170">Descrição</span><span class="sxs-lookup"><span data-stu-id="7ae81-170">Description</span></span>                                                                                                                                                                               |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7ae81-171">**PeerGroupExportDatabase**</span><span class="sxs-lookup"><span data-stu-id="7ae81-171">**PeerGroupExportDatabase**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupexportdatabase) | <span data-ttu-id="7ae81-172">Exporta um banco de dados de grupo de pares para um arquivo específico, que pode ser transportado para outro computador e importado com a função [**PeerGroupImportDatabase**](/windows/desktop/api/P2P/nf-p2p-peergroupimportdatabase) .</span><span class="sxs-lookup"><span data-stu-id="7ae81-172">Exports a peer group database to a specific file, which can be transported to another computer and imported with the [**PeerGroupImportDatabase**](/windows/desktop/api/P2P/nf-p2p-peergroupimportdatabase) function.</span></span> |
| [<span data-ttu-id="7ae81-173">**PeerGroupImportDatabase**</span><span class="sxs-lookup"><span data-stu-id="7ae81-173">**PeerGroupImportDatabase**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupimportdatabase) | <span data-ttu-id="7ae81-174">Importa um banco de dados de grupo de pares de um arquivo local.</span><span class="sxs-lookup"><span data-stu-id="7ae81-174">Imports a peer group database from a local file.</span></span>                                                                                                                                          |



 

## <a name="direct-connection-functions"></a><span data-ttu-id="7ae81-175">Funções de conexão direta</span><span class="sxs-lookup"><span data-stu-id="7ae81-175">Direct Connection Functions</span></span>



| <span data-ttu-id="7ae81-176">Função</span><span class="sxs-lookup"><span data-stu-id="7ae81-176">Function</span></span>                                                                 | <span data-ttu-id="7ae81-177">Descrição</span><span class="sxs-lookup"><span data-stu-id="7ae81-177">Description</span></span>                                                         |
|--------------------------------------------------------------------------|---------------------------------------------------------------------|
| [<span data-ttu-id="7ae81-178">**PeerGroupCloseDirectConnection**</span><span class="sxs-lookup"><span data-stu-id="7ae81-178">**PeerGroupCloseDirectConnection**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupclosedirectconnection) | <span data-ttu-id="7ae81-179">Fecha uma conexão direta específica entre dois pares.</span><span class="sxs-lookup"><span data-stu-id="7ae81-179">Closes a specific direct connection between two peers.</span></span>              |
| [<span data-ttu-id="7ae81-180">**PeerGroupEnumConnections**</span><span class="sxs-lookup"><span data-stu-id="7ae81-180">**PeerGroupEnumConnections**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupenumconnections)             | <span data-ttu-id="7ae81-181">Cria uma enumeração de conexões atualmente ativas no par.</span><span class="sxs-lookup"><span data-stu-id="7ae81-181">Creates an enumeration of connections currently active on the peer.</span></span> |
| [<span data-ttu-id="7ae81-182">**PeerGroupOpenDirectConnection**</span><span class="sxs-lookup"><span data-stu-id="7ae81-182">**PeerGroupOpenDirectConnection**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupopendirectconnection)   | <span data-ttu-id="7ae81-183">Estabelece uma conexão direta com outro par em um grupo de pares.</span><span class="sxs-lookup"><span data-stu-id="7ae81-183">Establishes a direct connection with another peer in a peer group.</span></span>  |
| [<span data-ttu-id="7ae81-184">**PeerGroupSendData**</span><span class="sxs-lookup"><span data-stu-id="7ae81-184">**PeerGroupSendData**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupsenddata)                           | <span data-ttu-id="7ae81-185">Envia dados para um membro em uma conexão de vizinho ou direta.</span><span class="sxs-lookup"><span data-stu-id="7ae81-185">Sends data to a member over a neighbor or direct connection.</span></span>        |



 

## <a name="group-events-infrastructure"></a><span data-ttu-id="7ae81-186">Infraestrutura de eventos de grupo</span><span class="sxs-lookup"><span data-stu-id="7ae81-186">Group Events Infrastructure</span></span>



| <span data-ttu-id="7ae81-187">Função</span><span class="sxs-lookup"><span data-stu-id="7ae81-187">Function</span></span>                                                     | <span data-ttu-id="7ae81-188">Descrição</span><span class="sxs-lookup"><span data-stu-id="7ae81-188">Description</span></span>                                                                                    |
|--------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7ae81-189">**PeerGroupGetEventData**</span><span class="sxs-lookup"><span data-stu-id="7ae81-189">**PeerGroupGetEventData**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupgeteventdata)       | <span data-ttu-id="7ae81-190">Permite que um aplicativo recupere os dados retornados por um evento de agrupamento.</span><span class="sxs-lookup"><span data-stu-id="7ae81-190">Allows an application to retrieve the data returned by a grouping event.</span></span>                       |
| [<span data-ttu-id="7ae81-191">**PeerGroupRegisterEvent**</span><span class="sxs-lookup"><span data-stu-id="7ae81-191">**PeerGroupRegisterEvent**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupregisterevent)     | <span data-ttu-id="7ae81-192">Registra um par para eventos de grupo de pares específicos.</span><span class="sxs-lookup"><span data-stu-id="7ae81-192">Registers a peer for specific peer group events.</span></span>                                               |
| [<span data-ttu-id="7ae81-193">**PeerGroupUnregisterEvent**</span><span class="sxs-lookup"><span data-stu-id="7ae81-193">**PeerGroupUnregisterEvent**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupunregisterevent) | <span data-ttu-id="7ae81-194">Cancela o registro de um par da notificação de eventos de pares associados ao identificador de evento fornecido.</span><span class="sxs-lookup"><span data-stu-id="7ae81-194">Unregisters a peer from notification of peer events associated with the supplied event handle.</span></span> |



 

## <a name="group-time-conversion-functions"></a><span data-ttu-id="7ae81-195">Funções de conversão de tempo de grupo</span><span class="sxs-lookup"><span data-stu-id="7ae81-195">Group Time Conversion Functions</span></span>



| <span data-ttu-id="7ae81-196">Função</span><span class="sxs-lookup"><span data-stu-id="7ae81-196">Function</span></span>                                                                     | <span data-ttu-id="7ae81-197">Descrição</span><span class="sxs-lookup"><span data-stu-id="7ae81-197">Description</span></span>                                                                                                                   |
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7ae81-198">**PeerGroupPeerTimeToUniversalTime**</span><span class="sxs-lookup"><span data-stu-id="7ae81-198">**PeerGroupPeerTimeToUniversalTime**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergrouppeertimetouniversaltime) | <span data-ttu-id="7ae81-199">Converte o valor de tempo de referência mantido do grupo de pares em um valor de hora localizado apropriado para exibição em um computador par.</span><span class="sxs-lookup"><span data-stu-id="7ae81-199">Converts the peer group-maintained reference time value to a localized time value appropriate for display on a peer computer.</span></span> |
| [<span data-ttu-id="7ae81-200">**PeerGroupUniversalTimeToPeerTime**</span><span class="sxs-lookup"><span data-stu-id="7ae81-200">**PeerGroupUniversalTimeToPeerTime**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupuniversaltimetopeertime) | <span data-ttu-id="7ae81-201">Converte um valor de hora local do computador de um par em um valor de tempo de grupo de pares comum.</span><span class="sxs-lookup"><span data-stu-id="7ae81-201">Converts a local time value from a peer's computer to a common peer group time value.</span></span>                                         |



 

## <a name="group-configuration-functions"></a><span data-ttu-id="7ae81-202">Funções de configuração de grupo</span><span class="sxs-lookup"><span data-stu-id="7ae81-202">Group Configuration Functions</span></span>



| <span data-ttu-id="7ae81-203">Função</span><span class="sxs-lookup"><span data-stu-id="7ae81-203">Function</span></span>                                               | <span data-ttu-id="7ae81-204">Descrição</span><span class="sxs-lookup"><span data-stu-id="7ae81-204">Description</span></span>                                                                                                                       |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7ae81-205">**PeerGroupExportConfig**</span><span class="sxs-lookup"><span data-stu-id="7ae81-205">**PeerGroupExportConfig**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupexportconfig) | <span data-ttu-id="7ae81-206">Exporta a configuração de grupo para um par como uma cadeia de caracteres XML que contém a identidade, o nome do grupo e o GMC para a identidade.</span><span class="sxs-lookup"><span data-stu-id="7ae81-206">Exports the group configuration for a peer as an XML string that contains the identity, group name, and the GMC for the identity.</span></span> |
| [<span data-ttu-id="7ae81-207">**PeerGroupImportConfig**</span><span class="sxs-lookup"><span data-stu-id="7ae81-207">**PeerGroupImportConfig**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupimportconfig) | <span data-ttu-id="7ae81-208">Importa uma configuração de grupo de pares para uma identidade com base nas configurações específicas em uma cadeia de caracteres de configuração XML fornecida.</span><span class="sxs-lookup"><span data-stu-id="7ae81-208">Imports a peer group configuration for an identity based on the specific settings in a supplied XML configuration string.</span></span>         |



 

 

 



