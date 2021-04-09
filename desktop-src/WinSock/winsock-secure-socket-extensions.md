---
description: As extensões de soquete seguro para Winsock permitem que um aplicativo de soquete controle a segurança de seu tráfego em uma rede.
ms.assetid: 023a9f96-814f-40c3-a186-ae0a0c9baef2
title: Extensões do Winsock Secure Socket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b62ee593b3abbb3bb0f8dbf27b79d6868f04fc0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010480"
---
# <a name="winsock-secure-socket-extensions"></a><span data-ttu-id="45d10-103">Extensões do Winsock Secure Socket</span><span class="sxs-lookup"><span data-stu-id="45d10-103">Winsock Secure Socket Extensions</span></span>

<span data-ttu-id="45d10-104">As extensões de soquete seguro para Winsock permitem que um aplicativo de soquete controle a segurança de seu tráfego em uma rede.</span><span class="sxs-lookup"><span data-stu-id="45d10-104">The secure socket extensions to Winsock allow a socket application to control the security of their traffic over a network.</span></span> <span data-ttu-id="45d10-105">Essas extensões permitem que um aplicativo forneça a política de segurança e os requisitos para seu tráfego de rede e consulte as configurações de segurança aplicadas.</span><span class="sxs-lookup"><span data-stu-id="45d10-105">These extensions allow an application to provide security policy and requirements for their network traffic, and query the security settings applied.</span></span> <span data-ttu-id="45d10-106">Por exemplo, um aplicativo pode usar essas extensões para consultar o token de segurança de mesmo nível que pode ser usado para executar verificações de acesso no nível do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="45d10-106">For example, an application can use these extensions to query the peer security token that can be used to perform application level access checks.</span></span>

<span data-ttu-id="45d10-107">As extensões de soquete seguro destinam-se a integrar os serviços fornecidos pelo IPsec e outros protocolos de segurança com a estrutura do Winsock.</span><span class="sxs-lookup"><span data-stu-id="45d10-107">The secure socket extensions are intended to integrate the services provided by IPsec and other security protocols with the Winsock framework.</span></span> <span data-ttu-id="45d10-108">Antes do Windows Vista, no Windows Server 2003 e no Windows XP, o IPsec foi configurado por um administrador por meio de políticas locais e de domínio.</span><span class="sxs-lookup"><span data-stu-id="45d10-108">Prior to Windows Vista, on Windows Server 2003 and Windows XP, IPsec has been configured by an administrator via local and domain policies.</span></span> <span data-ttu-id="45d10-109">No Windows Vista, as extensões de soquete seguro permitem que os aplicativos configurem total ou parcialmente e controlem a segurança de seu tráfego de rede no nível do soquete.</span><span class="sxs-lookup"><span data-stu-id="45d10-109">On Windows Vista, the secure socket extensions instead allow applications to entirely or partially configure and control the security of their network traffic at the socket level.</span></span>

<span data-ttu-id="45d10-110">Os aplicativos já podem proteger o tráfego de rede usando APIs públicas, como gerenciamento de IPsec, plataforma de filtragem do Windows e SSPI (interface do provedor de suporte de segurança).</span><span class="sxs-lookup"><span data-stu-id="45d10-110">Applications can already secure network traffic by using public APIs, such as IPsec management, Windows Filtering Platform and Security Support Provider Interface (SSPI).</span></span> <span data-ttu-id="45d10-111">No entanto, o uso dessas APIs pode tornar o aplicativo mais difícil de desenvolver e pode dificultar a configuração e a implantação.</span><span class="sxs-lookup"><span data-stu-id="45d10-111">However, using these APIs may make the application more difficult to develop, and may make it more difficult to configure and deploy.</span></span> <span data-ttu-id="45d10-112">As extensões do Winsock Secure Socket foram projetadas para simplificar o desenvolvimento de aplicativos de rede que exigem o tráfego de rede seguro, permitindo que o Winsock lide com a maior parte da complexidade.</span><span class="sxs-lookup"><span data-stu-id="45d10-112">The Winsock secure socket extensions have been designed to simplify the development of network applications that require secure network traffic by letting Winsock handle most of the complexity.</span></span>

<span data-ttu-id="45d10-113">Essas extensões de soquete seguro estão disponíveis no Windows Vista e versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="45d10-113">These secure socket extensions are available on Windows Vista and later.</span></span>

## <a name="secure-socket-functions"></a><span data-ttu-id="45d10-114">Funções de soquete seguro</span><span class="sxs-lookup"><span data-stu-id="45d10-114">Secure Socket Functions</span></span>

<span data-ttu-id="45d10-115">As funções de extensão de soquete seguro são as seguintes:</span><span class="sxs-lookup"><span data-stu-id="45d10-115">The secure socket extension functions are as follows:</span></span>

-   [<span data-ttu-id="45d10-116">**WSADeleteSocketPeerTargetName**</span><span class="sxs-lookup"><span data-stu-id="45d10-116">**WSADeleteSocketPeerTargetName**</span></span>](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsadeletesocketpeertargetname)
-   [<span data-ttu-id="45d10-117">**WSAImpersonateSocketPeer**</span><span class="sxs-lookup"><span data-stu-id="45d10-117">**WSAImpersonateSocketPeer**</span></span>](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsaimpersonatesocketpeer)
-   [<span data-ttu-id="45d10-118">**WSAQuerySocketSecurity**</span><span class="sxs-lookup"><span data-stu-id="45d10-118">**WSAQuerySocketSecurity**</span></span>](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsaquerysocketsecurity)
-   [<span data-ttu-id="45d10-119">**WSARevertImpersonation**</span><span class="sxs-lookup"><span data-stu-id="45d10-119">**WSARevertImpersonation**</span></span>](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsarevertimpersonation)
-   [<span data-ttu-id="45d10-120">**WSASetSocketPeerTargetName**</span><span class="sxs-lookup"><span data-stu-id="45d10-120">**WSASetSocketPeerTargetName**</span></span>](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsasetsocketpeertargetname)
-   [<span data-ttu-id="45d10-121">**WSASetSocketSecurity**</span><span class="sxs-lookup"><span data-stu-id="45d10-121">**WSASetSocketSecurity**</span></span>](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsasetsocketsecurity)

> [!Note]  
> <span data-ttu-id="45d10-122">Atualmente, as funções de soquete seguro dão suporte apenas ao protocolo IPsec e estão disponíveis no Windows Vista e versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="45d10-122">The secure socket functions currently support only the IPsec protocol and are available on Windows Vista and later.</span></span>

 

<span data-ttu-id="45d10-123">As estruturas e enumerações usadas pelas funções de soquete seguro são as seguintes:</span><span class="sxs-lookup"><span data-stu-id="45d10-123">The structures and enumerations used by the secure socket functions are as follows:</span></span>

-   [<span data-ttu-id="45d10-124">**\_nome de \_ destino de par de soquete \_**</span><span class="sxs-lookup"><span data-stu-id="45d10-124">**SOCKET\_PEER\_TARGET\_NAME**</span></span>](/windows/desktop/api/Mstcpip/ns-mstcpip-socket_peer_target_name)
-   [<span data-ttu-id="45d10-125">**\_protocolo de segurança de soquete \_**</span><span class="sxs-lookup"><span data-stu-id="45d10-125">**SOCKET\_SECURITY\_PROTOCOL**</span></span>](/windows/desktop/api/Mstcpip/ne-mstcpip-socket_security_protocol)
-   [<span data-ttu-id="45d10-126">**\_informações de \_ consulta de segurança de soquete \_**</span><span class="sxs-lookup"><span data-stu-id="45d10-126">**SOCKET\_SECURITY\_QUERY\_INFO**</span></span>](/windows/desktop/api/Mstcpip/ns-mstcpip-socket_security_query_info)
-   [<span data-ttu-id="45d10-127">**\_modelo de \_ consulta de segurança de soquete \_**</span><span class="sxs-lookup"><span data-stu-id="45d10-127">**SOCKET\_SECURITY\_QUERY\_TEMPLATE**</span></span>](/windows/desktop/api/Mstcpip/ns-mstcpip-socket_security_query_template)
-   [<span data-ttu-id="45d10-128">**\_configurações de segurança de soquete \_**</span><span class="sxs-lookup"><span data-stu-id="45d10-128">**SOCKET\_SECURITY\_SETTINGS**</span></span>](/windows/desktop/api/Mstcpip/ns-mstcpip-socket_security_settings)
-   [<span data-ttu-id="45d10-129">**configurações de segurança de soquete \_ \_ \_ IPSec**</span><span class="sxs-lookup"><span data-stu-id="45d10-129">**SOCKET\_SECURITY\_SETTINGS\_IPSEC**</span></span>](/windows/desktop/api/Mstcpip/ns-mstcpip-socket_security_settings_ipsec)

<span data-ttu-id="45d10-130">As funções de soquete seguro são simples de usar para aplicativos normais e são flexíveis o suficiente para aplicativos que precisam de um alto grau de controle sobre sua segurança.</span><span class="sxs-lookup"><span data-stu-id="45d10-130">The secure socket functions are simple to use for normal applications and are flexible enough for applications that need a high degree of control over their security.</span></span> <span data-ttu-id="45d10-131">Essas funções possibilitam manter o mecanismo de segurança subjacente oculto do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="45d10-131">These functions make it possible to keep the underlying security mechanism hidden from the application.</span></span> <span data-ttu-id="45d10-132">Um aplicativo pode especificar requisitos de segurança genéricos e permitir que o administrador controle o protocolo de segurança que é usado para dar suporte aos requisitos.</span><span class="sxs-lookup"><span data-stu-id="45d10-132">An application can specify generic security requirements and let the administrator control the security protocol that is used to support the requirements.</span></span> <span data-ttu-id="45d10-133">Embora seja possível estender essas funções para adicionar outros protocolos de segurança, no momento, apenas o IPsec se integra com as funções de soquete seguro.</span><span class="sxs-lookup"><span data-stu-id="45d10-133">While it is possible to extend these functions to add other security protocols, currently only IPsec integrates with the secure socket functions.</span></span>

<span data-ttu-id="45d10-134">A função [**WSASetSocketSecurity**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsasetsocketsecurity) permite que um aplicativo habilite a segurança e aplique configurações de segurança antes que uma conexão seja estabelecida.</span><span class="sxs-lookup"><span data-stu-id="45d10-134">The [**WSASetSocketSecurity**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsasetsocketsecurity) function allows an application to enable security and apply security settings before a connection is established.</span></span>

<span data-ttu-id="45d10-135">A função [**WSASetSocketPeerTargetName**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsasetsocketpeertargetname) permite que um aplicativo especifique o nome de destino correspondente a uma entidade par.</span><span class="sxs-lookup"><span data-stu-id="45d10-135">The [**WSASetSocketPeerTargetName**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsasetsocketpeertargetname) function allows an application to specify the target name corresponding to a peer entity.</span></span> <span data-ttu-id="45d10-136">O protocolo de segurança selecionado usará essas informações ao autenticar o par.</span><span class="sxs-lookup"><span data-stu-id="45d10-136">The selected security protocol will use this information when authenticating the peer.</span></span> <span data-ttu-id="45d10-137">Esse recurso aborda as preocupações com ataques intermediários confiáveis.</span><span class="sxs-lookup"><span data-stu-id="45d10-137">This feature addresses concerns about trusted man-in-the-middle attacks.</span></span>

<span data-ttu-id="45d10-138">A função [**WSADeleteSocketPeerTargetName**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsadeletesocketpeertargetname) é usada para excluir um nome de par especificado anteriormente para um soquete.</span><span class="sxs-lookup"><span data-stu-id="45d10-138">The [**WSADeleteSocketPeerTargetName**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsadeletesocketpeertargetname) function is used to delete a previously specified peer name for a socket.</span></span>

<span data-ttu-id="45d10-139">Depois que uma conexão é estabelecida, a função [**WSAQuerySocketSecurity**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsaquerysocketsecurity) permite que um aplicativo consulte as propriedades de segurança da conexão, que pode incluir o acesso de pares ou o token de acesso do computador.</span><span class="sxs-lookup"><span data-stu-id="45d10-139">After a connection is established, the [**WSAQuerySocketSecurity**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsaquerysocketsecurity) function allows an application to query the security properties of the connection, which can include the peer access or computer access token.</span></span>

<span data-ttu-id="45d10-140">Depois que uma conexão é estabelecida, a função [**WSAImpersonateSocketPeer**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsaimpersonatesocketpeer) permite que um aplicativo represente a entidade de segurança correspondente a um par de soquetes para executar a autorização em nível de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="45d10-140">After a connection is established, the [**WSAImpersonateSocketPeer**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsaimpersonatesocketpeer) function allows an application to impersonate the security principal corresponding to a socket peer in order to perform application-level authorization.</span></span>

<span data-ttu-id="45d10-141">O [**WSARevertImpersonation**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsarevertimpersonation) permite que um aplicativo encerre a representação de um par de soquetes.</span><span class="sxs-lookup"><span data-stu-id="45d10-141">The [**WSARevertImpersonation**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsarevertimpersonation) allows an application to terminate the impersonation of a socket peer.</span></span>

## <a name="secure-socket-architecture"></a><span data-ttu-id="45d10-142">Arquitetura de soquete seguro</span><span class="sxs-lookup"><span data-stu-id="45d10-142">Secure Socket Architecture</span></span>

![arquitetura básica das extensões de soquete de segurança do Winsock](images/ss-arch.png)

-   <span data-ttu-id="45d10-144">Um aplicativo chama as funções de soquete seguro para definir ou consultar as configurações de segurança de um soquete.</span><span class="sxs-lookup"><span data-stu-id="45d10-144">An application calls the secure socket functions to set or query security settings for a socket.</span></span>
-   <span data-ttu-id="45d10-145">As funções de soquete seguro são um conjunto de funções de extensão de tipo seguro que encapsulam chamadas para a função [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) usando valores definidos recentemente para o parâmetro *DwIoControlCode* disponível no Windows Vista e posterior.</span><span class="sxs-lookup"><span data-stu-id="45d10-145">The secure socket functions are a set of type-safe extension functions that wrap calls to the [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) function using newly-defined values for the *dwIoControlCode* parameter available on Windows Vista and later.</span></span> <span data-ttu-id="45d10-146">Esses IOCTLs são tratados pela pilha de rede.</span><span class="sxs-lookup"><span data-stu-id="45d10-146">These IOCTLs are handled by the network stack.</span></span>
-   <span data-ttu-id="45d10-147">A pilha de rede direcionará a chamada para a [camada de aplicação (ALE)](../fwp/application-layer-enforcement--ale-.md) junto com a alça do ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="45d10-147">The network stack will direct the call to [Application Layer Enforcement (ALE)](../fwp/application-layer-enforcement--ale-.md) along with the endpoint handle.</span></span> <span data-ttu-id="45d10-148">Para as funções [**WSADeleteSocketPeerTargetName**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsadeletesocketpeertargetname), [**WSASetSocketPeerTargetName**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsasetsocketpeertargetname)e [**WSASetSocketSecurity**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsasetsocketsecurity) , a EPA definirá as configurações do aplicativo no ponto de extremidade local.</span><span class="sxs-lookup"><span data-stu-id="45d10-148">For the [**WSADeleteSocketPeerTargetName**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsadeletesocketpeertargetname), [**WSASetSocketPeerTargetName**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsasetsocketpeertargetname), and [**WSASetSocketSecurity**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsasetsocketsecurity) functions, ALE will configure the application's settings on the local endpoint.</span></span> <span data-ttu-id="45d10-149">Para a função [**WSAQuerySocketSecurity**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsaquerysocketsecurity) , a Ale lerá as informações solicitadas dos pontos de extremidade locais e remotos aplicáveis.</span><span class="sxs-lookup"><span data-stu-id="45d10-149">For the [**WSAQuerySocketSecurity**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsaquerysocketsecurity) function, ALE will read the requested information from applicable local and remote endpoints.</span></span>
-   <span data-ttu-id="45d10-150">Com base em eventos de soquete, a ALE (aplicação de camada de aplicativo) impõe políticas para a arquitetura de soquete seguro usando a plataforma de filtragem do Windows.</span><span class="sxs-lookup"><span data-stu-id="45d10-150">Based on socket events, Application Layer Enforcement (ALE) enforces policies for the secure socket architecture using the Windows Filtering Platform.</span></span> <span data-ttu-id="45d10-151">Para obter mais informações, consulte [sobre a plataforma de filtragem do Windows](../fwp/about-windows-filtering-platform.md) e a [camada de aplicação (ALE)](../fwp/application-layer-enforcement--ale-.md).</span><span class="sxs-lookup"><span data-stu-id="45d10-151">For more information, see [About Windows Filtering Platform](../fwp/about-windows-filtering-platform.md) and [Application Layer Enforcement (ALE)](../fwp/application-layer-enforcement--ale-.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="45d10-152">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="45d10-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="45d10-153">Sobre a plataforma de filtragem do Windows</span><span class="sxs-lookup"><span data-stu-id="45d10-153">About Windows Filtering Platform</span></span>](../fwp/about-windows-filtering-platform.md)
</dt> <dt>

[<span data-ttu-id="45d10-154">Exemplos de Winsock avançados usando extensões de soquete seguro</span><span class="sxs-lookup"><span data-stu-id="45d10-154">Advanced Winsock Samples Using Secure Socket Extensions</span></span>](advanced-winsock-samples-using-secure-socket-extensions.md)
</dt> <dt>

[<span data-ttu-id="45d10-155">Aplicação da camada de aplicativo (EPA)</span><span class="sxs-lookup"><span data-stu-id="45d10-155">Application Layer Enforcement (ALE)</span></span>](../fwp/application-layer-enforcement--ale-.md)
</dt> <dt>

[<span data-ttu-id="45d10-156">Configuração de IPsec</span><span class="sxs-lookup"><span data-stu-id="45d10-156">IPsec Configuration</span></span>](../fwp/ipsec-configuration.md)
</dt> <dt>

[<span data-ttu-id="45d10-157">Funções IPsec</span><span class="sxs-lookup"><span data-stu-id="45d10-157">IPsec Functions</span></span>](../fwp/fwp-ipsec-functions.md)
</dt> <dt>

[<span data-ttu-id="45d10-158">Programação de Winsock seguro</span><span class="sxs-lookup"><span data-stu-id="45d10-158">Secure Winsock Programming</span></span>](secure-winsock-programming.md)
</dt> <dt>

[<span data-ttu-id="45d10-159">SSPI (interface do provedor de suporte de segurança)</span><span class="sxs-lookup"><span data-stu-id="45d10-159">Security Support Provider Interface (SSPI)</span></span>](../rpc/security-support-provider-interface-sspi-.md)
</dt> <dt>

[<span data-ttu-id="45d10-160">Usando extensões de soquete seguro</span><span class="sxs-lookup"><span data-stu-id="45d10-160">Using Secure Socket Extensions</span></span>](using-secure-socket-extensions.md)
</dt> <dt>

[<span data-ttu-id="45d10-161">Plataforma de filtragem do Windows</span><span class="sxs-lookup"><span data-stu-id="45d10-161">Windows Filtering Platform</span></span>](../fwp/windows-filtering-platform-start-page.md)
</dt> <dt>

[<span data-ttu-id="45d10-162">Funções da API da Windows Filtering Platform</span><span class="sxs-lookup"><span data-stu-id="45d10-162">Windows Filtering Platform API Functions</span></span>](../fwp/fwp-functions.md)
</dt> </dl>

 

 
