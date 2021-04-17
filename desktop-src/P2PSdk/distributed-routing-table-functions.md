---
description: A API de DRT (tabela de roteamento distribuído) utiliza as funções a seguir.
ms.assetid: 1ceff217-d410-47fa-99a2-8588f001859e
title: Funções de tabela de roteamento distribuído
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cd48c3a60f458285ce5f607f9ab6bcf7a557cd9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105770364"
---
# <a name="distributed-routing-table-functions"></a><span data-ttu-id="34137-103">Funções de tabela de roteamento distribuído</span><span class="sxs-lookup"><span data-stu-id="34137-103">Distributed Routing Table Functions</span></span>

<span data-ttu-id="34137-104">A API de DRT (tabela de roteamento distribuído) utiliza as funções a seguir.</span><span class="sxs-lookup"><span data-stu-id="34137-104">The Distributed Routing Table (DRT) API utilizes the following functions.</span></span>

## <a name="lifetime-management-functions"></a><span data-ttu-id="34137-105">Funções de gerenciamento de tempo de vida</span><span class="sxs-lookup"><span data-stu-id="34137-105">Lifetime Management Functions</span></span>



| <span data-ttu-id="34137-106">Função</span><span class="sxs-lookup"><span data-stu-id="34137-106">Function</span></span>                                           | <span data-ttu-id="34137-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="34137-107">Description</span></span>                                                                                                    |
|----------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="34137-108">**DrtOpen**</span><span class="sxs-lookup"><span data-stu-id="34137-108">**DrtOpen**</span></span>](/windows/desktop/api/drt/nf-drt-drtopen)                         | <span data-ttu-id="34137-109">Cria uma instância DRT local usando critérios especificados pela estrutura [**de \_ configurações DRT**](/windows/desktop/api/drt/ns-drt-drt_settings) .</span><span class="sxs-lookup"><span data-stu-id="34137-109">Creates a local DRT instance using criteria specified by the [**DRT\_SETTINGS**](/windows/desktop/api/drt/ns-drt-drt_settings) structure.</span></span>  |
| [<span data-ttu-id="34137-110">**DrtClose**</span><span class="sxs-lookup"><span data-stu-id="34137-110">**DrtClose**</span></span>](/windows/desktop/api/drt/nf-drt-drtclose)                       | <span data-ttu-id="34137-111">Fecha e remove a instância local do DRT.</span><span class="sxs-lookup"><span data-stu-id="34137-111">Closes and removes the local instance of the DRT.</span></span>                                                              |
| [<span data-ttu-id="34137-112">**DrtGetEventData**</span><span class="sxs-lookup"><span data-stu-id="34137-112">**DrtGetEventData**</span></span>](/windows/desktop/api/drt/nf-drt-drtgeteventdata)         | <span data-ttu-id="34137-113">Recupera dados de evento associados a um evento sinalizado.</span><span class="sxs-lookup"><span data-stu-id="34137-113">Retrieves event data associated with a signaled event.</span></span>                                                         |
| [<span data-ttu-id="34137-114">**DrtGetEventDataSize**</span><span class="sxs-lookup"><span data-stu-id="34137-114">**DrtGetEventDataSize**</span></span>](/windows/desktop/api/drt/nf-drt-drtgeteventdatasize) | <span data-ttu-id="34137-115">Retorna o tamanho da estrutura [**de \_ \_ dados de evento DRT**](/windows/desktop/api/drt/ns-drt-drt_event_data) associada a um evento sinalizado.</span><span class="sxs-lookup"><span data-stu-id="34137-115">Returns the size of the [**DRT\_EVENT\_DATA**](/windows/desktop/api/drt/ns-drt-drt_event_data) structure associated with a signaled event.</span></span> |



 

## <a name="module-management-functions"></a><span data-ttu-id="34137-116">Funções de gerenciamento de módulo</span><span class="sxs-lookup"><span data-stu-id="34137-116">Module Management Functions</span></span>



| <span data-ttu-id="34137-117">Função</span><span class="sxs-lookup"><span data-stu-id="34137-117">Function</span></span>                                                                           | <span data-ttu-id="34137-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="34137-118">Description</span></span>                                                                                                                           |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="34137-119">**DrtCreatePnrpBootstrapResolver**</span><span class="sxs-lookup"><span data-stu-id="34137-119">**DrtCreatePnrpBootstrapResolver**</span></span>](/windows/desktop/api/drt/nf-drt-drtcreatepnrpbootstrapresolver)           | <span data-ttu-id="34137-120">Cria um resolvedor de inicialização com base no protocolo PNRP.</span><span class="sxs-lookup"><span data-stu-id="34137-120">Creates a bootstrap resolver based on the PNRP protocol.</span></span>                                                                              |
| [<span data-ttu-id="34137-121">**DrtDeletePnrpBootstrapResolver**</span><span class="sxs-lookup"><span data-stu-id="34137-121">**DrtDeletePnrpBootstrapResolver**</span></span>](/windows/desktop/api/drt/nf-drt-drtdeletepnrpbootstrapresolver)           | <span data-ttu-id="34137-122">Exclui um resolvedor de inicialização com base no protocolo PNRP.</span><span class="sxs-lookup"><span data-stu-id="34137-122">Deletes a bootstrap resolver based on the PNRP protocol.</span></span>                                                                              |
| [<span data-ttu-id="34137-123">**DrtCreateDnsBootstrapResolver**</span><span class="sxs-lookup"><span data-stu-id="34137-123">**DrtCreateDnsBootstrapResolver**</span></span>](/windows/desktop/api/drt/nf-drt-drtcreatednsbootstrapresolver)             | <span data-ttu-id="34137-124">Cria um provedor de inicialização que entrará em contato com um host bem conhecido pelo nome.</span><span class="sxs-lookup"><span data-stu-id="34137-124">Creates a bootstrap provider that will contact a well known host by name.</span></span>                                                             |
| [<span data-ttu-id="34137-125">**DrtDeleteDnsBootstrapResolver**</span><span class="sxs-lookup"><span data-stu-id="34137-125">**DrtDeleteDnsBootstrapResolver**</span></span>](/windows/desktop/api/drt/nf-drt-drtdeletednsbootstrapresolver)             | <span data-ttu-id="34137-126">Exclui um provedor de inicialização que entrará em contato com um host bem conhecido pelo nome.</span><span class="sxs-lookup"><span data-stu-id="34137-126">Deletes a bootstrap provider that will contact a well known host by name.</span></span>                                                             |
| [<span data-ttu-id="34137-127">**DrtCreateIpv6UdpTransport**</span><span class="sxs-lookup"><span data-stu-id="34137-127">**DrtCreateIpv6UdpTransport**</span></span>](/windows/desktop/api/drt/nf-drt-drtcreateipv6udptransport)                     | <span data-ttu-id="34137-128">Cria um transporte com base no protocolo UDP IPv6.</span><span class="sxs-lookup"><span data-stu-id="34137-128">Creates a transport based on the IPv6 UDP protocol.</span></span>                                                                                   |
| [<span data-ttu-id="34137-129">**DrtDeleteIpv6UdpTransport**</span><span class="sxs-lookup"><span data-stu-id="34137-129">**DrtDeleteIpv6UdpTransport**</span></span>](/windows/desktop/api/drt/nf-drt-drtdeleteipv6udptransport)                     | <span data-ttu-id="34137-130">Exclui um transporte com base no protocolo UDP IPv6.</span><span class="sxs-lookup"><span data-stu-id="34137-130">Deletes a transport based on the IPv6 UDP protocol.</span></span>                                                                                   |
| [<span data-ttu-id="34137-131">**DrtCreateDerivedKeySecurityProvider**</span><span class="sxs-lookup"><span data-stu-id="34137-131">**DrtCreateDerivedKeySecurityProvider**</span></span>](/windows/desktop/api/drt/nf-drt-drtcreatederivedkeysecurityprovider) | <span data-ttu-id="34137-132">Cria um provedor de segurança de chave derivada para o DRT.</span><span class="sxs-lookup"><span data-stu-id="34137-132">Creates a derived key security provider for the DRT.</span></span>                                                                                  |
| [<span data-ttu-id="34137-133">**DrtCreateDerivedKey**</span><span class="sxs-lookup"><span data-stu-id="34137-133">**DrtCreateDerivedKey**</span></span>](/windows/desktop/api/drt/nf-drt-drtcreatederivedkey)                                 | <span data-ttu-id="34137-134">Cria uma chave que pode ser utilizada por [**DrtRegisterKey**](/windows/desktop/api/drt/nf-drt-drtregisterkey) quando a DRT estiver usando um provedor de segurança de chave derivada.</span><span class="sxs-lookup"><span data-stu-id="34137-134">Creates a key that can be utilized by [**DrtRegisterKey**](/windows/desktop/api/drt/nf-drt-drtregisterkey) when the DRT is using a derived key security provider.</span></span> |
| [<span data-ttu-id="34137-135">**DrtDeleteDerivedKeySecurityProvider**</span><span class="sxs-lookup"><span data-stu-id="34137-135">**DrtDeleteDerivedKeySecurityProvider**</span></span>](/windows/desktop/api/drt/nf-drt-drtdeletederivedkeysecurityprovider) | <span data-ttu-id="34137-136">Exclui um provedor de segurança de chave derivada para o DRT.</span><span class="sxs-lookup"><span data-stu-id="34137-136">Deletes a derived key security provider for the DRT.</span></span>                                                                                  |
| [<span data-ttu-id="34137-137">**DrtCreateNullSecurityProvider**</span><span class="sxs-lookup"><span data-stu-id="34137-137">**DrtCreateNullSecurityProvider**</span></span>](/windows/desktop/api/drt/nf-drt-drtcreatenullsecurityprovider)             | <span data-ttu-id="34137-138">Cria um provedor de segurança nulo.</span><span class="sxs-lookup"><span data-stu-id="34137-138">Creates a null security provider.</span></span> <span data-ttu-id="34137-139">Esse provedor de segurança não exige que os nós autentiquem chaves.</span><span class="sxs-lookup"><span data-stu-id="34137-139">This security provider does not require nodes to authenticate keys.</span></span>                                 |
| [<span data-ttu-id="34137-140">**DrtDeleteNullSecurityProvider**</span><span class="sxs-lookup"><span data-stu-id="34137-140">**DrtDeleteNullSecurityProvider**</span></span>](/windows/desktop/api/drt/nf-drt-drtdeletenullsecurityprovider)             | <span data-ttu-id="34137-141">Exclui um provedor de segurança nulo.</span><span class="sxs-lookup"><span data-stu-id="34137-141">Deletes a null security provider.</span></span>                                                                                                     |



 

## <a name="registration-functions"></a><span data-ttu-id="34137-142">Funções de registro</span><span class="sxs-lookup"><span data-stu-id="34137-142">Registration Functions</span></span>



| <span data-ttu-id="34137-143">Função</span><span class="sxs-lookup"><span data-stu-id="34137-143">Function</span></span>                                     | <span data-ttu-id="34137-144">Descrição</span><span class="sxs-lookup"><span data-stu-id="34137-144">Description</span></span>                                                    |
|----------------------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="34137-145">**DrtRegisterKey**</span><span class="sxs-lookup"><span data-stu-id="34137-145">**DrtRegisterKey**</span></span>](/windows/desktop/api/drt/nf-drt-drtregisterkey)     | <span data-ttu-id="34137-146">Registra uma chave no DRT.</span><span class="sxs-lookup"><span data-stu-id="34137-146">Registers a key in the DRT.</span></span>                                    |
| [<span data-ttu-id="34137-147">**DrtUpdateKey**</span><span class="sxs-lookup"><span data-stu-id="34137-147">**DrtUpdateKey**</span></span>](/windows/desktop/api/drt/nf-drt-drtupdatekey)         | <span data-ttu-id="34137-148">Atualiza os dados de aplicativo associados a uma chave registrada.</span><span class="sxs-lookup"><span data-stu-id="34137-148">Updates the application data associated with a registered key.</span></span> |
| [<span data-ttu-id="34137-149">**DrtUnregisterKey**</span><span class="sxs-lookup"><span data-stu-id="34137-149">**DrtUnregisterKey**</span></span>](/windows/desktop/api/drt/nf-drt-drtunregisterkey) | <span data-ttu-id="34137-150">Cancela o registro de uma chave do DRT.</span><span class="sxs-lookup"><span data-stu-id="34137-150">Deregisters a key from the DRT.</span></span>                                |



 

## <a name="search-functions"></a><span data-ttu-id="34137-151">Funções de pesquisa</span><span class="sxs-lookup"><span data-stu-id="34137-151">Search Functions</span></span>



| <span data-ttu-id="34137-152">Função</span><span class="sxs-lookup"><span data-stu-id="34137-152">Function</span></span>                                                 | <span data-ttu-id="34137-153">Descrição</span><span class="sxs-lookup"><span data-stu-id="34137-153">Description</span></span>                                                                                                                                                                                                             |
|----------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="34137-154">**DrtStartSearch**</span><span class="sxs-lookup"><span data-stu-id="34137-154">**DrtStartSearch**</span></span>](/windows/desktop/api/drt/nf-drt-drtstartsearch)                 | <span data-ttu-id="34137-155">Pesquisa a DRT em busca de uma chave usando critérios especificados na estrutura de [**\_ \_ informações de pesquisa DRT**](/windows/desktop/api/drt/ns-drt-drt_search_info) .</span><span class="sxs-lookup"><span data-stu-id="34137-155">Searches the DRT for a key using criteria specified in the [**DRT\_SEARCH\_INFO**](/windows/desktop/api/drt/ns-drt-drt_search_info) structure.</span></span>                                                                                                      |
| [<span data-ttu-id="34137-156">**DrtContinueSearch**</span><span class="sxs-lookup"><span data-stu-id="34137-156">**DrtContinueSearch**</span></span>](/windows/desktop/api/drt/nf-drt-drtcontinuesearch)           | <span data-ttu-id="34137-157">Continua um \_ caminho de \_ retorno de pesquisa DRT \_ pesquisando uma chave no DRT.</span><span class="sxs-lookup"><span data-stu-id="34137-157">Continues a DRT\_SEARCH\_RETURN\_PATH search for a key in the DRT.</span></span> <span data-ttu-id="34137-158">Essa função é usada somente quando o sinalizador **fIterative** é definido como **true** na estrutura de [**\_ \_ informações de pesquisa DRT**](/windows/desktop/api/drt/ns-drt-drt_search_info) associada.</span><span class="sxs-lookup"><span data-stu-id="34137-158">This function is used only when the **fIterative** flag is set to **TRUE** in the associated [**DRT\_SEARCH\_INFO**](/windows/desktop/api/drt/ns-drt-drt_search_info) structure.</span></span> |
| [<span data-ttu-id="34137-159">**DrtGetSearchResult**</span><span class="sxs-lookup"><span data-stu-id="34137-159">**DrtGetSearchResult**</span></span>](/windows/desktop/api/drt/nf-drt-drtgetsearchresult)         | <span data-ttu-id="34137-160">Recupera os resultados da pesquisa.</span><span class="sxs-lookup"><span data-stu-id="34137-160">Retrieves the search result(s).</span></span>                                                                                                                                                                                         |
| [<span data-ttu-id="34137-161">**DrtGetSearchResultSize**</span><span class="sxs-lookup"><span data-stu-id="34137-161">**DrtGetSearchResultSize**</span></span>](/windows/desktop/api/drt/nf-drt-drtgetsearchresultsize) | <span data-ttu-id="34137-162">Retorna o tamanho do próximo resultado de pesquisa disponível.</span><span class="sxs-lookup"><span data-stu-id="34137-162">Returns the size of the next available search result.</span></span>                                                                                                                                                                   |
| [<span data-ttu-id="34137-163">**DrtGetSearchPath**</span><span class="sxs-lookup"><span data-stu-id="34137-163">**DrtGetSearchPath**</span></span>](/windows/desktop/api/drt/nf-drt-drtgetsearchpath)             | <span data-ttu-id="34137-164">Retorna uma lista de nós contatados durante a operação de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="34137-164">Returns a list of nodes contacted during the search operation.</span></span>                                                                                                                                                          |
| [<span data-ttu-id="34137-165">**DrtGetSearchPathSize**</span><span class="sxs-lookup"><span data-stu-id="34137-165">**DrtGetSearchPathSize**</span></span>](/windows/desktop/api/drt/nf-drt-drtgetsearchpathsize)     | <span data-ttu-id="34137-166">Retorna o tamanho do caminho de pesquisa, que representa o número de nós utilizados na operação de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="34137-166">Returns the size of the search path, which represents the number of nodes utilized in the search operation.</span></span>                                                                                                             |
| [<span data-ttu-id="34137-167">**DrtEndSearch**</span><span class="sxs-lookup"><span data-stu-id="34137-167">**DrtEndSearch**</span></span>](/windows/desktop/api/drt/nf-drt-drtendsearch)                     | <span data-ttu-id="34137-168">Cancela uma pesquisa de uma chave em uma DRT e, como resultado, o retorno dos resultados por meio do [**\_ \_ resultado da pesquisa DRT**](/windows/desktop/api/drt/ns-drt-drt_search_result) é interrompido.</span><span class="sxs-lookup"><span data-stu-id="34137-168">Cancels a search for a key in a DRT, and as a result, the return of results via [**DRT\_SEARCH\_RESULT**](/windows/desktop/api/drt/ns-drt-drt_search_result) is stopped.</span></span> <span data-ttu-id="34137-169">Essa API pode ser chamada a qualquer momento depois que uma pesquisa é emitida.</span><span class="sxs-lookup"><span data-stu-id="34137-169">This API can be called at any point after a search is issued.</span></span>              |



 

## <a name="instance-name-functions"></a><span data-ttu-id="34137-170">Funções de nome de instância</span><span class="sxs-lookup"><span data-stu-id="34137-170">Instance Name Functions</span></span>



| <span data-ttu-id="34137-171">Função</span><span class="sxs-lookup"><span data-stu-id="34137-171">Function</span></span>                                                 | <span data-ttu-id="34137-172">Descrição</span><span class="sxs-lookup"><span data-stu-id="34137-172">Description</span></span>                                                      |
|----------------------------------------------------------|------------------------------------------------------------------|
| [<span data-ttu-id="34137-173">**DrtGetInstanceName**</span><span class="sxs-lookup"><span data-stu-id="34137-173">**DrtGetInstanceName**</span></span>](/windows/desktop/api/drt/nf-drt-drtgetinstancename)         | <span data-ttu-id="34137-174">Obtém o nome associado a uma instância de DRT.</span><span class="sxs-lookup"><span data-stu-id="34137-174">Gets the name associated with a DRT instance.</span></span>                    |
| [<span data-ttu-id="34137-175">**DrtGetInstanceNameSize**</span><span class="sxs-lookup"><span data-stu-id="34137-175">**DrtGetInstanceNameSize**</span></span>](/windows/desktop/api/drt/nf-drt-drtgetinstancenamesize) | <span data-ttu-id="34137-176">Retorna o tamanho do nome da instância da tabela de roteamento distribuído.</span><span class="sxs-lookup"><span data-stu-id="34137-176">Returns the size of the Distributed Routing Table instance name.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="34137-177">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="34137-177">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="34137-178">Enumerações de tabela de roteamento distribuído</span><span class="sxs-lookup"><span data-stu-id="34137-178">Distributed Routing Table Enumerations</span></span>](distributed-routing-table-enumerations.md)
</dt> <dt>

[<span data-ttu-id="34137-179">Estruturas de tabela de roteamento distribuído</span><span class="sxs-lookup"><span data-stu-id="34137-179">Distributed Routing Table Structures</span></span>](distributed-routing-table-structures.md)
</dt> <dt>

[<span data-ttu-id="34137-180">Referência de API de Tabela de roteamento distribuído</span><span class="sxs-lookup"><span data-stu-id="34137-180">Distributed Routing Table API Reference</span></span>](distributed-routing-table-api-reference.md)
</dt> </dl>

 

 



