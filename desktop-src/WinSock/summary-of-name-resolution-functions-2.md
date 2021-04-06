---
description: 'As funções de resolução de nomes podem ser agrupadas em três categorias: instalação de serviço, consultas de cliente e auxiliar (com macros).'
ms.assetid: c16a7163-11f5-4ad6-9df1-9bad2a964e48
title: Resumo das funções de resolução de nomes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5969cb2cf145124446374dcb86eb1e0a8a837c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647124"
---
# <a name="summary-of-name-resolution-functions"></a><span data-ttu-id="f42f5-103">Resumo das funções de resolução de nomes</span><span class="sxs-lookup"><span data-stu-id="f42f5-103">Summary of Name Resolution Functions</span></span>

<span data-ttu-id="f42f5-104">As funções de resolução de nomes podem ser agrupadas em três categorias: instalação de serviço, consultas de cliente e auxiliar (com macros).</span><span class="sxs-lookup"><span data-stu-id="f42f5-104">The name resolution functions can be grouped into three categories: Service installation, client queries, and helper (with macros).</span></span> <span data-ttu-id="f42f5-105">As seções a seguir identificam as funções em cada categoria e descrevem brevemente o uso pretendido.</span><span class="sxs-lookup"><span data-stu-id="f42f5-105">The sections that follow identify the functions in each category and briefly describe their intended use.</span></span> <span data-ttu-id="f42f5-106">As estruturas de dados-chave também são descritas.</span><span class="sxs-lookup"><span data-stu-id="f42f5-106">Key data structures are also described.</span></span>

## <a name="service-installation"></a><span data-ttu-id="f42f5-107">Instalação do serviço</span><span class="sxs-lookup"><span data-stu-id="f42f5-107">Service Installation</span></span>

-   [<span data-ttu-id="f42f5-108">**WSAInstallServiceClass**</span><span class="sxs-lookup"><span data-stu-id="f42f5-108">**WSAInstallServiceClass**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsainstallserviceclassa)
-   [<span data-ttu-id="f42f5-109">**WSARemoveServiceClass**</span><span class="sxs-lookup"><span data-stu-id="f42f5-109">**WSARemoveServiceClass**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsaremoveserviceclass)
-   [<span data-ttu-id="f42f5-110">**WSASetService**</span><span class="sxs-lookup"><span data-stu-id="f42f5-110">**WSASetService**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsasetservicea)

<span data-ttu-id="f42f5-111">Quando a classe de serviço necessária ainda não existir, um aplicativo usará [**WSAInstallServiceClass**](/windows/desktop/api/Winsock2/nf-winsock2-wsainstallserviceclassa) para instalar uma nova classe de serviço fornecendo um nome de classe de serviço, um GUID para o identificador de classe de serviço e uma série de estruturas [**WSANSCLASSINFO**](/windows/desktop/api/Winsock2/ns-winsock2-wsansclassinfow) .</span><span class="sxs-lookup"><span data-stu-id="f42f5-111">When the required service class does not already exist, an application uses [**WSAInstallServiceClass**](/windows/desktop/api/Winsock2/nf-winsock2-wsainstallserviceclassa) to install a new service class by supplying a service class name, a GUID for the service class identifier, and a series of [**WSANSCLASSINFO**](/windows/desktop/api/Winsock2/ns-winsock2-wsansclassinfow) structures.</span></span> <span data-ttu-id="f42f5-112">Essas estruturas são específicas para um namespace específico e fornecem valores comuns, como números de porta TCP recomendados ou identificadores SAP do NetWare.</span><span class="sxs-lookup"><span data-stu-id="f42f5-112">These structures are each specific to a particular namespace, and supply common values such as recommended TCP port numbers or NetWare SAP Identifiers.</span></span> <span data-ttu-id="f42f5-113">Uma classe de serviço pode ser removida chamando [**WSARemoveServiceClass**](/windows/desktop/api/Winsock2/nf-winsock2-wsaremoveserviceclass) e fornecendo o GUID correspondente ao identificador de classe.</span><span class="sxs-lookup"><span data-stu-id="f42f5-113">A service class can be removed by calling [**WSARemoveServiceClass**](/windows/desktop/api/Winsock2/nf-winsock2-wsaremoveserviceclass) and supplying the GUID corresponding to the class identifier.</span></span>

<span data-ttu-id="f42f5-114">Quando existe uma classe de serviço, as instâncias específicas de um serviço podem ser instaladas ou removidas por meio do [**WSASetService**](/windows/desktop/api/Winsock2/nf-winsock2-wsasetservicea).</span><span class="sxs-lookup"><span data-stu-id="f42f5-114">Once a service class exists, specific instances of a service can be installed or removed through [**WSASetService**](/windows/desktop/api/Winsock2/nf-winsock2-wsasetservicea).</span></span> <span data-ttu-id="f42f5-115">Essa função usa uma estrutura [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) como um parâmetro de entrada junto com um código de operação e sinalizadores de operação.</span><span class="sxs-lookup"><span data-stu-id="f42f5-115">This function takes a [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) structure as an input parameter along with an operation code and operation flags.</span></span> <span data-ttu-id="f42f5-116">O código da operação indica se o serviço está sendo instalado ou removido.</span><span class="sxs-lookup"><span data-stu-id="f42f5-116">The operation code indicates whether the service is being installed or removed.</span></span> <span data-ttu-id="f42f5-117">A estrutura **WSAQUERYSET** fornece todas as informações relevantes sobre o serviço, incluindo o identificador de classe de serviço, o nome do serviço (para essa instância), o identificador de namespace aplicável e as informações de protocolo e um conjunto de endereços de transporte no qual o serviço escuta.</span><span class="sxs-lookup"><span data-stu-id="f42f5-117">The **WSAQUERYSET** structure provides all of the relevant information about the service including service class identifier, service name (for this instance), applicable namespace identifier and protocol information, and a set of transport addresses at which the service listens.</span></span> <span data-ttu-id="f42f5-118">Os serviços devem invocar **WSASetService** quando forem inicializados para anunciar sua presença em namespaces dinâmicos.</span><span class="sxs-lookup"><span data-stu-id="f42f5-118">Services should invoke **WSASetService** when they initialize to advertise their presence in dynamic namespaces.</span></span>

## <a name="client-query"></a><span data-ttu-id="f42f5-119">Consulta do cliente</span><span class="sxs-lookup"><span data-stu-id="f42f5-119">Client Query</span></span>

-   [<span data-ttu-id="f42f5-120">**WSAEnumNameSpaceProviders**</span><span class="sxs-lookup"><span data-stu-id="f42f5-120">**WSAEnumNameSpaceProviders**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumnamespaceprovidersa)
-   [<span data-ttu-id="f42f5-121">**WSALookupServiceBegin**</span><span class="sxs-lookup"><span data-stu-id="f42f5-121">**WSALookupServiceBegin**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina)
-   [<span data-ttu-id="f42f5-122">**WSALookupServiceNext**</span><span class="sxs-lookup"><span data-stu-id="f42f5-122">**WSALookupServiceNext**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta)
-   [<span data-ttu-id="f42f5-123">**WSALookupServiceEnd**</span><span class="sxs-lookup"><span data-stu-id="f42f5-123">**WSALookupServiceEnd**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend)

<span data-ttu-id="f42f5-124">A função [**WSAEnumNameSpaceProviders**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumnamespaceprovidersa) permite que um aplicativo descubra quais namespaces são acessíveis por meio de instalações de resolução de nome do Winsock.</span><span class="sxs-lookup"><span data-stu-id="f42f5-124">The [**WSAEnumNameSpaceProviders**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumnamespaceprovidersa) function allows an application to discover which namespaces are accessible through Winsock name resolution facilities.</span></span> <span data-ttu-id="f42f5-125">Ele também permite que um aplicativo determine se um determinado namespace tem suporte por mais de um provedor de namespace e para descobrir o identificador do provedor para qualquer provedor de namespace específico.</span><span class="sxs-lookup"><span data-stu-id="f42f5-125">It also allows an application to determine whether a given namespace is supported by more than one namespace provider, and to discover the provider identifier for any particular namespace provider.</span></span> <span data-ttu-id="f42f5-126">Usando um identificador de provedor, o aplicativo pode restringir uma operação de consulta a um provedor de namespace especificado.</span><span class="sxs-lookup"><span data-stu-id="f42f5-126">Using a provider identifier, the application can restrict a query operation to a specified namespace provider.</span></span>

<span data-ttu-id="f42f5-127">Namespace do Winsock – as operações de consulta envolvem uma série de chamadas: [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina), seguidas por uma ou mais chamadas para [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta) e terminando com uma chamada para [**WSALookupServiceEnd**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend).</span><span class="sxs-lookup"><span data-stu-id="f42f5-127">Winsock namespace–query operations involve a series of calls: [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina), followed by one or more calls to [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta) and ending with a call to [**WSALookupServiceEnd**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend).</span></span> <span data-ttu-id="f42f5-128">**WSALookupServiceBegin** usa uma estrutura [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) como entrada para definir os parâmetros de consulta junto com um conjunto de sinalizadores para fornecer controle adicional sobre a operação de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="f42f5-128">**WSALookupServiceBegin** takes a [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) structure as input to define the query parameters along with a set of flags to provide additional control over the search operation.</span></span> <span data-ttu-id="f42f5-129">Ele retorna um identificador de consulta que é usado nas chamadas subsequentes para **WSALookupServiceNext** e **WSALookupServiceEnd**.</span><span class="sxs-lookup"><span data-stu-id="f42f5-129">It returns a query handle which is used in the subsequent calls to **WSALookupServiceNext** and **WSALookupServiceEnd**.</span></span>

<span data-ttu-id="f42f5-130">O aplicativo invoca [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta) para obter os resultados da consulta, com os resultados fornecidos em um buffer [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) fornecido pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f42f5-130">The application invokes [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta) to obtain query results, with results supplied in an application-supplied [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) buffer.</span></span> <span data-ttu-id="f42f5-131">O aplicativo continua chamando **WSALookupServiceNext** até que o código de erro WSA \_ E \_ não \_ mais seja retornado, indicando que todos os resultados foram recuperados.</span><span class="sxs-lookup"><span data-stu-id="f42f5-131">The application continues to call **WSALookupServiceNext** until the error code WSA\_E\_NO\_MORE is returned indicating that all results have been retrieved.</span></span> <span data-ttu-id="f42f5-132">Em seguida, a pesquisa é encerrada por uma chamada para [**WSALookupServiceEnd**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend).</span><span class="sxs-lookup"><span data-stu-id="f42f5-132">The search is then terminated by a call to [**WSALookupServiceEnd**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend).</span></span> <span data-ttu-id="f42f5-133">A função **WSALookupServiceEnd** também pode ser usada para cancelar um **WSALookupServiceNext** pendente no momento quando chamado de outro thread.</span><span class="sxs-lookup"><span data-stu-id="f42f5-133">The **WSALookupServiceEnd** function can also be used to cancel a currently pending **WSALookupServiceNext** when called from another thread.</span></span>

<span data-ttu-id="f42f5-134">No Windows Sockets 2, códigos de erro conflitantes são definidos para WSAENOMORE (10102) e WSA \_ e \_ não \_ mais (10110).</span><span class="sxs-lookup"><span data-stu-id="f42f5-134">In Windows Sockets 2, conflicting error codes are defined for WSAENOMORE (10102) and WSA\_E\_NO\_MORE (10110).</span></span> <span data-ttu-id="f42f5-135">O código de erro WSAENOMORE será removido em uma versão futura e somente o WSA \_ e \_ não \_ será mais mantido.</span><span class="sxs-lookup"><span data-stu-id="f42f5-135">The error code WSAENOMORE will be removed in a future version and only WSA\_E\_NO\_MORE will remain.</span></span> <span data-ttu-id="f42f5-136">No entanto, para o Windows Sockets 2, os aplicativos devem verificar WSAENOMORE e WSA e \_ \_ não \_ mais a maior compatibilidade possível com provedores de namespace que usam um deles.</span><span class="sxs-lookup"><span data-stu-id="f42f5-136">For Windows Sockets 2, however, applications should check for both WSAENOMORE and WSA\_E\_NO\_MORE for the widest possible compatibility with namespace providers that use either one.</span></span>

## <a name="helper-functions"></a><span data-ttu-id="f42f5-137">Funções auxiliares</span><span class="sxs-lookup"><span data-stu-id="f42f5-137">Helper Functions</span></span>

-   [<span data-ttu-id="f42f5-138">**WSAGetServiceClassNameByClassId**</span><span class="sxs-lookup"><span data-stu-id="f42f5-138">**WSAGetServiceClassNameByClassId**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsagetserviceclassnamebyclassida)
-   [<span data-ttu-id="f42f5-139">**WSAAddressToString**</span><span class="sxs-lookup"><span data-stu-id="f42f5-139">**WSAAddressToString**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsaaddresstostringa)
-   [<span data-ttu-id="f42f5-140">**WSAStringToAddress**</span><span class="sxs-lookup"><span data-stu-id="f42f5-140">**WSAStringToAddress**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsastringtoaddressa)
-   [<span data-ttu-id="f42f5-141">**WSAGetServiceClassInfo**</span><span class="sxs-lookup"><span data-stu-id="f42f5-141">**WSAGetServiceClassInfo**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsagetserviceclassinfoa)

<span data-ttu-id="f42f5-142">As funções auxiliares de resolução de nomes incluem uma função para recuperar um nome de classe de serviço dado um identificador de classe de serviço, um par de funções usadas para converter um endereço de transporte entre uma estrutura [**SOCKADDR**](sockaddr-2.md) e uma representação de cadeia de caracteres ASCII, uma função para recuperar as informações de esquema de classe de serviço para uma determinada classe de serviço e um conjunto de macros para mapear serviços bem</span><span class="sxs-lookup"><span data-stu-id="f42f5-142">The name resolution helper functions include a function to retrieve a service class name given a service class identifier, a pair of functions used to translate a transport address between a [**SOCKADDR**](sockaddr-2.md) structure and an ASCII string representation, a function to retrieve the service class schema information for a given service class, and a set of macros for mapping well known services to preallocated GUIDs.</span></span>

<span data-ttu-id="f42f5-143">As seguintes macros do Winsock2. h auxiliam no mapeamento entre classes de serviço bem conhecidas e esses namespaces:</span><span class="sxs-lookup"><span data-stu-id="f42f5-143">The following macros from Winsock2.h aid in mapping between well known service classes and these namespaces:</span></span>

| <span data-ttu-id="f42f5-144">Macro</span><span class="sxs-lookup"><span data-stu-id="f42f5-144">Macro</span></span>                                                                                                            | <span data-ttu-id="f42f5-145">Descrição</span><span class="sxs-lookup"><span data-stu-id="f42f5-145">Description</span></span>                                                                                                                |
|------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f42f5-146">SVCID \_ TCP (porta) SVCID \_ UDP (porta)</span><span class="sxs-lookup"><span data-stu-id="f42f5-146">SVCID\_TCP(Port) SVCID\_UDP(Port)</span></span><br/> <span data-ttu-id="f42f5-147">SVCID \_ NetWare (tipo de objeto)</span><span class="sxs-lookup"><span data-stu-id="f42f5-147">SVCID\_NETWARE(Object Type)</span></span><br/>                              | <span data-ttu-id="f42f5-148">Dada uma porta para TCP/IP ou UDP/IP ou o tipo de objeto no caso do NetWare, retorna o GUID (número da porta na ordem do host).</span><span class="sxs-lookup"><span data-stu-id="f42f5-148">Given a port for TCP/IP or UDP/IP or the object type in the case of NetWare, returns the GUID (port number in host order).</span></span> |
| <span data-ttu-id="f42f5-149">IS \_ SVCID \_ TCP (GUID) é \_ SVCID \_ UDP (GUID)</span><span class="sxs-lookup"><span data-stu-id="f42f5-149">IS\_SVCID\_TCP(GUID)IS\_SVCID\_UDP(GUID)</span></span><br/> <span data-ttu-id="f42f5-150">é \_ SVCID \_ NetWare (GUID)</span><span class="sxs-lookup"><span data-stu-id="f42f5-150">IS\_SVCID\_NETWARE(GUID)</span></span><br/>                          | <span data-ttu-id="f42f5-151">Retornará **true** se o GUID estiver dentro do intervalo permitido.</span><span class="sxs-lookup"><span data-stu-id="f42f5-151">Returns **TRUE** if the GUID is within the allowable range.</span></span>                                                                |
| <span data-ttu-id="f42f5-152">SET \_ TCP \_ SVCID (GUID, porta) Set \_ UDP \_ SVCID (GUID, porta)</span><span class="sxs-lookup"><span data-stu-id="f42f5-152">SET\_TCP\_SVCID(GUID, port)SET\_UDP\_SVCID(GUID, port)</span></span><br/>                                                | <span data-ttu-id="f42f5-153">Inicializa uma estrutura de GUID com o equivalente de GUID para um número de porta TCP ou UDP (o número da porta deve estar na ordem do host).</span><span class="sxs-lookup"><span data-stu-id="f42f5-153">Initializes a GUID structure with the GUID equivalent for a TCP or UDP port number (port number must be in host order).</span></span>    |
| <span data-ttu-id="f42f5-154">PORTA \_ da \_ \_ porta TCP (GUID) SVCID \_ do \_ SVCID \_ UDP (GUID)</span><span class="sxs-lookup"><span data-stu-id="f42f5-154">PORT\_FROM\_SVCID\_TCP(GUID)PORT\_FROM\_SVCID\_UDP(GUID)</span></span><br/> <span data-ttu-id="f42f5-155">SAPId \_ da \_ SVCID \_ NetWare (GUID)</span><span class="sxs-lookup"><span data-stu-id="f42f5-155">SAPID\_FROM\_SVCID\_NETWARE(GUID)</span></span><br/> | <span data-ttu-id="f42f5-156">Retorna a porta ou o tipo de objeto associado ao GUID (número da porta na ordem do host).</span><span class="sxs-lookup"><span data-stu-id="f42f5-156">Returns the port or object type associated with the GUID (port number in host order).</span></span>                                      |



 

## <a name="related-topics"></a><span data-ttu-id="f42f5-157">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f42f5-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f42f5-158">**getaddrinfo**</span><span class="sxs-lookup"><span data-stu-id="f42f5-158">**getaddrinfo**</span></span>](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo)
</dt> <dt>

[<span data-ttu-id="f42f5-159">**GetAddrInfoEx**</span><span class="sxs-lookup"><span data-stu-id="f42f5-159">**GetAddrInfoEx**</span></span>](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfoexa)
</dt> <dt>

[<span data-ttu-id="f42f5-160">**GetAddrInfoW**</span><span class="sxs-lookup"><span data-stu-id="f42f5-160">**GetAddrInfoW**</span></span>](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfow)
</dt> <dt>

[<span data-ttu-id="f42f5-161">**getnameinfo**</span><span class="sxs-lookup"><span data-stu-id="f42f5-161">**getnameinfo**</span></span>](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo)
</dt> <dt>

[<span data-ttu-id="f42f5-162">**GetNameInfoW**</span><span class="sxs-lookup"><span data-stu-id="f42f5-162">**GetNameInfoW**</span></span>](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfow)
</dt> <dt>

[<span data-ttu-id="f42f5-163">Estruturas de dados de resolução de nomes</span><span class="sxs-lookup"><span data-stu-id="f42f5-163">Name Resolution Data Structures</span></span>](name-resolution-data-structures-2.md)
</dt> <dt>

[<span data-ttu-id="f42f5-164">Modelo de resolução de nomes</span><span class="sxs-lookup"><span data-stu-id="f42f5-164">Name Resolution Model</span></span>](name-resolution-model-2.md)
</dt> <dt>

[<span data-ttu-id="f42f5-165">Resolução de nomes independente de protocolo</span><span class="sxs-lookup"><span data-stu-id="f42f5-165">Protocol-Independent Name Resolution</span></span>](protocol-independent-name-resolution-2.md)
</dt> <dt>

[<span data-ttu-id="f42f5-166">Registro e resolução de nome</span><span class="sxs-lookup"><span data-stu-id="f42f5-166">Registration and Name Resolution</span></span>](registration-and-name-resolution-2.md)
</dt> <dt>

[<span data-ttu-id="f42f5-167">**SOCKADDR**</span><span class="sxs-lookup"><span data-stu-id="f42f5-167">**SOCKADDR**</span></span>](sockaddr-2.md)
</dt> <dt>

[<span data-ttu-id="f42f5-168">**WSAEnumNameSpaceProviders**</span><span class="sxs-lookup"><span data-stu-id="f42f5-168">**WSAEnumNameSpaceProviders**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumnamespaceprovidersa)
</dt> <dt>

[<span data-ttu-id="f42f5-169">**WSAGetServiceClassNameByClassId**</span><span class="sxs-lookup"><span data-stu-id="f42f5-169">**WSAGetServiceClassNameByClassId**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsagetserviceclassnamebyclassida)
</dt> <dt>

[<span data-ttu-id="f42f5-170">**WSAInstallServiceClass**</span><span class="sxs-lookup"><span data-stu-id="f42f5-170">**WSAInstallServiceClass**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsainstallserviceclassa)
</dt> <dt>

[<span data-ttu-id="f42f5-171">**WSALookupServiceBegin**</span><span class="sxs-lookup"><span data-stu-id="f42f5-171">**WSALookupServiceBegin**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina)
</dt> <dt>

[<span data-ttu-id="f42f5-172">**WSALookupServiceEnd**</span><span class="sxs-lookup"><span data-stu-id="f42f5-172">**WSALookupServiceEnd**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend)
</dt> <dt>

[<span data-ttu-id="f42f5-173">**WSALookupServiceNext**</span><span class="sxs-lookup"><span data-stu-id="f42f5-173">**WSALookupServiceNext**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta)
</dt> <dt>

[<span data-ttu-id="f42f5-174">**WSARemoveServiceClass**</span><span class="sxs-lookup"><span data-stu-id="f42f5-174">**WSARemoveServiceClass**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsaremoveserviceclass)
</dt> <dt>

[<span data-ttu-id="f42f5-175">**WSASetService**</span><span class="sxs-lookup"><span data-stu-id="f42f5-175">**WSASetService**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsasetservicea)
</dt> <dt>

[<span data-ttu-id="f42f5-176">**WSAQUERYSET**</span><span class="sxs-lookup"><span data-stu-id="f42f5-176">**WSAQUERYSET**</span></span>](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw)
</dt> <dt>

[<span data-ttu-id="f42f5-177">**WSANSCLASSINFO**</span><span class="sxs-lookup"><span data-stu-id="f42f5-177">**WSANSCLASSINFO**</span></span>](/windows/desktop/api/Winsock2/ns-winsock2-wsansclassinfow)
</dt> </dl>

 

 




