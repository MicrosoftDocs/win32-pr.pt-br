---
title: Autenticação, autorização e contabilização RADIUS
description: O NPS dá suporte total ao protocolo RADIUS (serviço RADIUS). O protocolo RADIUS é o padrão de fato para a autenticação de usuário remota e está documentado em RFC 2865 e RFC 2866.
ms.assetid: 3e00d555-355c-4a4c-a389-ab44e9ed9ca9
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cce45bbc6e4802ed5137849a5b22520c8a4badbb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366390"
---
# <a name="radius-authentication-authorization-and-accounting"></a><span data-ttu-id="df68b-104">Autenticação, autorização e contabilização RADIUS</span><span class="sxs-lookup"><span data-stu-id="df68b-104">RADIUS Authentication, Authorization, and Accounting</span></span>

> [!Note]  
> <span data-ttu-id="df68b-105">O IAS (serviço de autenticação da Internet) foi renomeado como NPS (servidor de políticas de rede) a partir do Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="df68b-105">Internet Authentication Service (IAS) was renamed Network Policy Server (NPS) starting with Windows Server 2008.</span></span> <span data-ttu-id="df68b-106">O conteúdo deste tópico aplica-se ao IAS e ao NPS.</span><span class="sxs-lookup"><span data-stu-id="df68b-106">The content of this topic applies to both IAS and NPS.</span></span> <span data-ttu-id="df68b-107">Em todo o texto, o NPS é usado para fazer referência a todas as versões do serviço, incluindo as versões originalmente chamadas de IAS.</span><span class="sxs-lookup"><span data-stu-id="df68b-107">Throughout the text, NPS is used to refer to all versions of the service, including the versions originally referred to as IAS.</span></span>

 

<span data-ttu-id="df68b-108">O NPS dá suporte total ao protocolo RADIUS (serviço RADIUS).</span><span class="sxs-lookup"><span data-stu-id="df68b-108">NPS fully supports the Remote Authentication Dial-In User Service (RADIUS) protocol.</span></span> <span data-ttu-id="df68b-109">O protocolo RADIUS é o padrão de fato para a autenticação de usuário remota e está documentado em [rfc 2865](https://www.ietf.org/rfc/rfc2865.txt) e [RFC 2866](https://www.ietf.org/rfc/rfc2866.txt).</span><span class="sxs-lookup"><span data-stu-id="df68b-109">The RADIUS protocol is the de facto standard for remote user authentication and it is documented in [RFC 2865](https://www.ietf.org/rfc/rfc2865.txt) and [RFC 2866](https://www.ietf.org/rfc/rfc2866.txt).</span></span>

## <a name="radius-authentication-and-authorization"></a><span data-ttu-id="df68b-110">Autenticação e autorização RADIUS</span><span class="sxs-lookup"><span data-stu-id="df68b-110">RADIUS Authentication and Authorization</span></span>

<span data-ttu-id="df68b-111">O diagrama a seguir mostra um cliente de autenticação ("usuário") que se conecta a um NAS (servidor de acesso à rede) por meio de uma conexão dial-up, usando o protocolo PPP (PPP).</span><span class="sxs-lookup"><span data-stu-id="df68b-111">The following diagram shows an authenticating client ("User") connecting to a Network Access Server (NAS) over a dial-up connection, using the Point-to-Point Protocol (PPP).</span></span> <span data-ttu-id="df68b-112">Para autenticar o usuário, o NAS entra em contato com um servidor remoto que executa o NPS.</span><span class="sxs-lookup"><span data-stu-id="df68b-112">In order to authenticate the User, the NAS contacts a remote server running NPS.</span></span> <span data-ttu-id="df68b-113">O NAS e o servidor NPS se comunicam usando o protocolo RADIUS.</span><span class="sxs-lookup"><span data-stu-id="df68b-113">The NAS and the NPS server communicate using the RADIUS protocol.</span></span>

![autenticação de usuário remoto](images/ias01.png)

<span data-ttu-id="df68b-115">Um NAS Opera como um cliente de um servidor ou servidores que dão suporte ao protocolo RADIUS.</span><span class="sxs-lookup"><span data-stu-id="df68b-115">A NAS operates as a client of a server or servers that support the RADIUS protocol.</span></span> <span data-ttu-id="df68b-116">Os servidores que oferecem suporte ao protocolo RADIUS são geralmente chamados de servidores RADIUS.</span><span class="sxs-lookup"><span data-stu-id="df68b-116">Servers that support the RADIUS protocol are generally referred to as the RADIUS servers.</span></span> <span data-ttu-id="df68b-117">O cliente RADIUS, ou seja, o NAS, passa informações sobre o usuário para servidores RADIUS designados e, em seguida, atua na resposta que os servidores retornam.</span><span class="sxs-lookup"><span data-stu-id="df68b-117">The RADIUS client, that is, the NAS, passes information about the User to designated RADIUS servers, and then acts on the response that the servers return.</span></span> <span data-ttu-id="df68b-118">A solicitação enviada pelo NAS para o servidor RADIUS a fim de autenticar o usuário geralmente é chamada de "solicitação de autenticação".</span><span class="sxs-lookup"><span data-stu-id="df68b-118">The request sent by the NAS to the RADIUS server in order to authenticate the User is generally called an "authentication request."</span></span>

<span data-ttu-id="df68b-119">Se um servidor RADIUS autenticar o usuário com êxito, o servidor RADIUS retornará informações de configuração para o NAS para que ele possa fornecer serviço de rede ao usuário.</span><span class="sxs-lookup"><span data-stu-id="df68b-119">If a RADIUS server authenticates the User successfully, the RADIUS server returns configuration information to the NAS so that it can provide network service to the user.</span></span> <span data-ttu-id="df68b-120">Essas informações de configuração são compostas por "autorizações" e contêm, entre outras, o tipo de serviço que o NAS pode fornecer ao usuário (por exemplo, PPP ou telnet).</span><span class="sxs-lookup"><span data-stu-id="df68b-120">This configuration information is composed of "authorizations" and contains, among others, the type of service NAS may provide to the User (for example, PPP, or telnet).</span></span>

<span data-ttu-id="df68b-121">Enquanto o servidor RADIUS está processando a solicitação de autenticação, ele pode executar funções de autorização, como verificar o número de telefone do usuário e verificar se o usuário já tem uma sessão em andamento.</span><span class="sxs-lookup"><span data-stu-id="df68b-121">While the RADIUS server is processing the authentication request, it can perform authorization functions such as verifying the user's telephone number and checking whether the user already has a session in progress.</span></span> <span data-ttu-id="df68b-122">O servidor RADIUS pode determinar se o usuário já tem uma sessão em andamento contatando um servidor de estado.</span><span class="sxs-lookup"><span data-stu-id="df68b-122">The RADIUS server can determine whether the user already has a session in progress by contacting a state server.</span></span>

<span data-ttu-id="df68b-123">Para obter mais informações sobre autenticação e autorização RADIUS, consulte [RFC 2865](https://www.ietf.org/rfc/rfc2865.txt).</span><span class="sxs-lookup"><span data-stu-id="df68b-123">For more information on RADIUS authentication and authorization, see [RFC 2865](https://www.ietf.org/rfc/rfc2865.txt).</span></span>

## <a name="radius-accounting"></a><span data-ttu-id="df68b-124">Contabilização RADIUS</span><span class="sxs-lookup"><span data-stu-id="df68b-124">RADIUS Accounting</span></span>

<span data-ttu-id="df68b-125">O servidor RADIUS também coleta uma variedade de informações enviadas pelo NAS que podem ser usadas para contabilidade e para relatórios sobre a atividade de rede.</span><span class="sxs-lookup"><span data-stu-id="df68b-125">The RADIUS server also collects a variety of information sent by the NAS that can be used for accounting and for reporting on network activity.</span></span> <span data-ttu-id="df68b-126">O cliente RADIUS envia informações para servidores RADIUS designados quando o usuário faz logon e faz logoff.</span><span class="sxs-lookup"><span data-stu-id="df68b-126">The RADIUS client sends information to designated RADIUS servers when the User logs on and logs off.</span></span> <span data-ttu-id="df68b-127">O cliente RADIUS pode enviar informações de uso adicionais periodicamente enquanto a sessão está em andamento.</span><span class="sxs-lookup"><span data-stu-id="df68b-127">The RADIUS client may send additional usage information on a periodic basis while the session is in progress.</span></span> <span data-ttu-id="df68b-128">As solicitações enviadas pelo cliente para o servidor para registrar logon/logoff e informações de uso geralmente são chamadas de "solicitações de contabilização".</span><span class="sxs-lookup"><span data-stu-id="df68b-128">The requests sent by the client to the server to record logon/logoff and usage information are generally called "accounting requests."</span></span>

<span data-ttu-id="df68b-129">Para obter mais informações sobre estatísticas RADIUS, consulte [RFC 2866](https://www.ietf.org/rfc/rfc2866.txt).</span><span class="sxs-lookup"><span data-stu-id="df68b-129">For more information on RADIUS accounting, see [RFC 2866](https://www.ietf.org/rfc/rfc2866.txt).</span></span>

## <a name="radius-proxy"></a><span data-ttu-id="df68b-130">Proxy RADIUS</span><span class="sxs-lookup"><span data-stu-id="df68b-130">RADIUS Proxy</span></span>

<span data-ttu-id="df68b-131">Um servidor RADIUS pode atuar como um cliente proxy para outros servidores RADIUS.</span><span class="sxs-lookup"><span data-stu-id="df68b-131">A RADIUS server can act as a proxy client to other RADIUS servers.</span></span> <span data-ttu-id="df68b-132">Nesses casos, o servidor RADIUS contatado pelo NAS passa a solicitação de autenticação ou de contabilização para outro servidor RADIUS que realmente realiza a autenticação ou a tarefa de contabilidade.</span><span class="sxs-lookup"><span data-stu-id="df68b-132">In these cases, the RADIUS server contacted by the NAS passes the authentication or accounting request to another RADIUS server that actually performs the authentication or the accounting task.</span></span>

## <a name="related-topics"></a><span data-ttu-id="df68b-133">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="df68b-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="df68b-134">Serviço de autenticação da Internet e servidor de políticas de rede</span><span class="sxs-lookup"><span data-stu-id="df68b-134">Internet Authentication Service and Network Policy Server</span></span>](internet-authentication-service-vs-network-policy-server.md)
</dt> <dt>

[<span data-ttu-id="df68b-135">Pacotes de contabilização RADIUS</span><span class="sxs-lookup"><span data-stu-id="df68b-135">RADIUS Accounting Packets</span></span>](/windows/desktop/Nps/ias-radius-accounting-packets)
</dt> <dt>

[<span data-ttu-id="df68b-136">Trabalhando com um servidor de estado</span><span class="sxs-lookup"><span data-stu-id="df68b-136">Working with a State Server</span></span>](/windows/desktop/Nps/ias-working-with-a-state-server)
</dt> </dl>

 

 