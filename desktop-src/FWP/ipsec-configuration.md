---
title: Configuração de IPsec
description: A WFP (Windows Filtering Platform) é a plataforma subjacente para o Firewall do Windows com segurança avançada.
ms.assetid: d54b5caa-daea-4231-9909-7a8d388df661
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78af8e3d0a23713c0505082555fe260bc562dfa4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103917246"
---
# <a name="ipsec-configuration"></a><span data-ttu-id="b84df-103">Configuração de IPsec</span><span class="sxs-lookup"><span data-stu-id="b84df-103">IPsec Configuration</span></span>

<span data-ttu-id="b84df-104">A WFP (Windows Filtering Platform) é a plataforma subjacente para o Firewall do Windows com segurança avançada.</span><span class="sxs-lookup"><span data-stu-id="b84df-104">Windows Filtering Platform (WFP) is the underlying platform for Windows Firewall with Advanced Security.</span></span> <span data-ttu-id="b84df-105">A WFP é usada para configurar regras de filtragem de rede, que incluem regras que regem a proteção do tráfego de rede com IPsec.</span><span class="sxs-lookup"><span data-stu-id="b84df-105">WFP is used to configure network filtering rules, which include rules that govern securing network traffic with IPsec.</span></span> <span data-ttu-id="b84df-106">Os desenvolvedores de aplicativos podem configurar o IPsec diretamente usando a API WFP, a fim de aproveitar um modelo de filtragem de tráfego de rede mais granular do que o modelo exposto por meio do snap-in do MMC (console de gerenciamento Microsoft) para o Firewall do Windows com segurança avançada.</span><span class="sxs-lookup"><span data-stu-id="b84df-106">Application developers may configure IPsec directly using the WFP API, in order to take advantage of a more granular network traffic filtering model than the model exposed through the Microsoft Management Console (MMC) snap-in for Windows Firewall with Advanced Security.</span></span>

## <a name="what-is-ipsec"></a><span data-ttu-id="b84df-107">O que é IPsec</span><span class="sxs-lookup"><span data-stu-id="b84df-107">What is IPsec</span></span>

<span data-ttu-id="b84df-108">O IPsec (Internet Protocol Security) é um conjunto de protocolos de segurança usados para transferir os pacotes de IP confidencialmente pela Internet.</span><span class="sxs-lookup"><span data-stu-id="b84df-108">Internet Protocol Security (IPsec) is a set of security protocols used to transfer IP packets confidentially across the Internet.</span></span> <span data-ttu-id="b84df-109">O IPsec é obrigatório para todas as implementações de IPv6 e opcional para IPv4.</span><span class="sxs-lookup"><span data-stu-id="b84df-109">IPsec is mandatory for all IPv6 implementations and optional for IPv4.</span></span>

<span data-ttu-id="b84df-110">O tráfego IP protegido tem dois cabeçalhos IPsec opcionais, que identificam os tipos de proteção de criptografia aplicados ao pacote IP e incluem informações para decodificar o pacote protegido.</span><span class="sxs-lookup"><span data-stu-id="b84df-110">Secured IP traffic has two optional IPsec headers, which identify the types of cryptographic protection applied to the IP packet and include information for decoding the protected packet.</span></span>

<span data-ttu-id="b84df-111">O cabeçalho da carga de segurança de encapsulamento (ESP) é usado para privacidade e proteção contra modificações mal-intencionadas por meio da autenticação e criptografia opcional.</span><span class="sxs-lookup"><span data-stu-id="b84df-111">The Encapsulating Security Payload (ESP) header is used for privacy and protection against malicious modification by performing authentication and optional encryption.</span></span> <span data-ttu-id="b84df-112">Ele pode ser usado para tráfego que atravessa roteadores NAT (conversão de endereços de rede).</span><span class="sxs-lookup"><span data-stu-id="b84df-112">It can be used for traffic that traverses Network Address Translation (NAT) routers.</span></span>

<span data-ttu-id="b84df-113">O Cabeçalho de Autenticação (AH) é usado somente para proteção contra modificações mal-intencionadas por meio da autenticação.</span><span class="sxs-lookup"><span data-stu-id="b84df-113">The Authentication Header (AH) is used only for protection against malicious modification by performing authentication.</span></span> <span data-ttu-id="b84df-114">Ele não pode ser usado para tráfego que atravessa roteadores NAT.</span><span class="sxs-lookup"><span data-stu-id="b84df-114">It cannot be used for traffic that traverses NAT routers.</span></span>

<span data-ttu-id="b84df-115">Para obter mais informações sobre IPsec, consulte também:</span><span class="sxs-lookup"><span data-stu-id="b84df-115">For more information on IPsec, see also:</span></span>

<dl>

<span data-ttu-id="b84df-116">[Referência técnica de IPsec](/previous-versions/windows/it-pro/windows-server-2003/cc740240(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="b84df-116">[IPsec Technical Reference](/previous-versions/windows/it-pro/windows-server-2003/cc740240(v=ws.10))</span></span>  
</dl>

## <a name="what-is-ike"></a><span data-ttu-id="b84df-117">O que é IKE</span><span class="sxs-lookup"><span data-stu-id="b84df-117">What is IKE</span></span>

<span data-ttu-id="b84df-118">O protocolo IKE (IKE) é um protocolo de troca de chaves que faz parte do conjunto de protocolos IPsec.</span><span class="sxs-lookup"><span data-stu-id="b84df-118">Internet Key Exchange (IKE) is a key exchange protocol that is part of the IPsec protocol set.</span></span> <span data-ttu-id="b84df-119">O IKE é usado durante a configuração de uma conexão segura e realiza a troca segura de chaves secretas e outros parâmetros relacionados à proteção sem a intervenção do usuário.</span><span class="sxs-lookup"><span data-stu-id="b84df-119">IKE is used while setting up a secure connection and accomplishes the safe exchange of secret keys and other protection-related parameters without the intervention of the user.</span></span>

<span data-ttu-id="b84df-120">Para obter mais informações sobre IKE, consulte também:</span><span class="sxs-lookup"><span data-stu-id="b84df-120">For more information on IKE, see also:</span></span>

<dl>

<span data-ttu-id="b84df-121">[protocolo IKE](/previous-versions/windows/it-pro/windows-server-2003/cc784994(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="b84df-121">[Internet Key Exchange](/previous-versions/windows/it-pro/windows-server-2003/cc784994(v=ws.10))</span></span>  
</dl>

## <a name="what-is-authip"></a><span data-ttu-id="b84df-122">O que é AuthIP</span><span class="sxs-lookup"><span data-stu-id="b84df-122">What is AuthIP</span></span>

<span data-ttu-id="b84df-123">O protocolo Authenticated IP (AuthIP) é um novo protocolo de troca de chaves que expande o IKE da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="b84df-123">Authenticated Internet Protocol (AuthIP) is a new key exchange protocol that expands IKE as follows.</span></span>

<dl> <span data-ttu-id="b84df-124">Embora o IKE dê suporte apenas às credenciais de autenticação do computador, o AuthIP também oferece suporte a:</span><span class="sxs-lookup"><span data-stu-id="b84df-124">While IKE only supports computer authentication credentials, AuthIP also supports:</span></span>

-   <span data-ttu-id="b84df-125">Credenciais do usuário: NTLM, Kerberos, certificados.</span><span class="sxs-lookup"><span data-stu-id="b84df-125">User credentials: NTLM, Kerberos, certificates.</span></span>
-   <span data-ttu-id="b84df-126">Certificados de integridade NAP (proteção de acesso à rede).</span><span class="sxs-lookup"><span data-stu-id="b84df-126">Network Access Protection (NAP) health certificates.</span></span>
-   <span data-ttu-id="b84df-127">Credencial anônima, usada para autenticação opcional.</span><span class="sxs-lookup"><span data-stu-id="b84df-127">Anonymous credential, used for optional authentication.</span></span>
-   <span data-ttu-id="b84df-128">Combinação de credenciais; por exemplo, uma combinação de credenciais Kerberos de computador e de usuário.</span><span class="sxs-lookup"><span data-stu-id="b84df-128">Combination of credentials; for example, a combination of machine and user Kerberos credentials.</span></span>

  
<span data-ttu-id="b84df-129">O AuthIP tem um mecanismo de repetição de autenticação que verifica todos os métodos de autenticação configurados antes de falhar a conexão.</span><span class="sxs-lookup"><span data-stu-id="b84df-129">AuthIP has an authentication-retry mechanism that verifies all configured authentication methods before failing the connection.</span></span>  
<span data-ttu-id="b84df-130">O AuthIP pode ser usado com soquetes seguros para implementar o tráfego protegido por IPsec baseado em aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b84df-130">AuthIP can be used with secure sockets to implement application-based IPsec secured traffic.</span></span> <span data-ttu-id="b84df-131">Ele fornece:</span><span class="sxs-lookup"><span data-stu-id="b84df-131">It provides:</span></span>

-   <span data-ttu-id="b84df-132">Autenticação por soquete e criptografia.</span><span class="sxs-lookup"><span data-stu-id="b84df-132">Per-socket authentication and encryption.</span></span> <span data-ttu-id="b84df-133">Consulte [**WSASetSocketSecurity**](/windows/desktop/api/ws2tcpip/nf-ws2tcpip-wsasetsocketsecurity) para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="b84df-133">See [**WSASetSocketSecurity**](/windows/desktop/api/ws2tcpip/nf-ws2tcpip-wsasetsocketsecurity) for more information.</span></span>
-   <span data-ttu-id="b84df-134">Representação do cliente.</span><span class="sxs-lookup"><span data-stu-id="b84df-134">Client impersonation.</span></span> <span data-ttu-id="b84df-135">(O IPsec representa o contexto de segurança no qual o soquete é criado.)</span><span class="sxs-lookup"><span data-stu-id="b84df-135">(IPsec impersonates the security context under which the socket is created.)</span></span>
-   <span data-ttu-id="b84df-136">Validação de nome de par de entrada e saída.</span><span class="sxs-lookup"><span data-stu-id="b84df-136">Inbound and outbound peer name validation.</span></span> <span data-ttu-id="b84df-137">Consulte [**WSASetSocketPeerTargetName**](/windows/desktop/api/ws2tcpip/nf-ws2tcpip-wsasetsocketpeertargetname) para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="b84df-137">See [**WSASetSocketPeerTargetName**](/windows/desktop/api/ws2tcpip/nf-ws2tcpip-wsasetsocketpeertargetname) for more information.</span></span>

  
</dl>

<span data-ttu-id="b84df-138">Para obter mais informações sobre AuthIP, consulte também:</span><span class="sxs-lookup"><span data-stu-id="b84df-138">For more information on AuthIP, see also:</span></span>

<dl>

[<span data-ttu-id="b84df-139">AuthIP no Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b84df-139">AuthIP in Windows Vista</span></span>](https://www.microsoft.com/technet/community/columns/cableguy/cg0806.mspx)  
</dl>

## <a name="what-is-an-ipsec-policy"></a><span data-ttu-id="b84df-140">O que é uma política IPsec</span><span class="sxs-lookup"><span data-stu-id="b84df-140">What is an IPsec Policy</span></span>

<span data-ttu-id="b84df-141">Uma política IPsec é um conjunto de regras que determinam qual tipo de tráfego IP precisa ser protegido usando IPsec e como proteger esse tráfego.</span><span class="sxs-lookup"><span data-stu-id="b84df-141">An IPsec policy is a set of rules that determine which type of IP traffic needs to be secured using IPsec and how to secure that traffic.</span></span> <span data-ttu-id="b84df-142">Apenas uma política IPsec está ativa em um computador ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="b84df-142">Only one IPsec policy is active on a computer at one time.</span></span>

<span data-ttu-id="b84df-143">Para saber mais sobre como implementar diretivas IPsec, abra o snap-in do MMC diretiva de segurança local (secpol. msc), pressione F1 para exibir a ajuda e, em seguida, selecione criando e usando políticas IPsec do Sumário.</span><span class="sxs-lookup"><span data-stu-id="b84df-143">To learn more about implementing IPsec policies, open the Local Security Policy MMC snap-in (secpol.msc), press F1 to display the Help, and then select Creating and Using IPsec Policies from the table of contents.</span></span>

<span data-ttu-id="b84df-144">Para obter mais informações sobre diretivas IPsec, consulte também:</span><span class="sxs-lookup"><span data-stu-id="b84df-144">For more information on IPsec policies, see also:</span></span>

<dl>

<span data-ttu-id="b84df-145">[Visão geral dos conceitos da política IPsec](/previous-versions/windows/it-pro/windows-server-2003/cc776080(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="b84df-145">[Overview of IPsec Policy Concepts](/previous-versions/windows/it-pro/windows-server-2003/cc776080(v=ws.10))</span></span>  
<span data-ttu-id="b84df-146">[Descrição de uma política IPsec](/previous-versions/windows/it-pro/windows-server-2003/cc781593(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="b84df-146">[Description of an IPsec Policy](/previous-versions/windows/it-pro/windows-server-2003/cc781593(v=ws.10))</span></span>  
</dl>

## <a name="how-to-use-wfp-to-configure-ipsec-policies"></a><span data-ttu-id="b84df-147">Como usar o WFP para configurar as políticas de IPsec</span><span class="sxs-lookup"><span data-stu-id="b84df-147">How to Use WFP to Configure IPsec Policies</span></span>

<span data-ttu-id="b84df-148">A implementação do IPsec da Microsoft usa a plataforma de filtragem do Windows para configurar as políticas de IPsec.</span><span class="sxs-lookup"><span data-stu-id="b84df-148">The Microsoft implementation of IPsec uses Windows Filtering Platform to setup IPsec policies.</span></span> <span data-ttu-id="b84df-149">As diretivas IPsec são implementadas pela adição de filtros em várias camadas de WFP, como a seguir.</span><span class="sxs-lookup"><span data-stu-id="b84df-149">IPsec policies are implemented by adding filters at various WFP layers as follows.</span></span>

-   <span data-ttu-id="b84df-150">Na camada FWPM \_ \_ IKEEXT \_ V {4 \| 6} camadas, adicione filtros que especificam as políticas de negociação usadas pelos módulos de chaveamento (Ike/AuthIP) durante as trocas de modo principal (mm).</span><span class="sxs-lookup"><span data-stu-id="b84df-150">At the FWPM\_LAYER\_IKEEXT\_V{4\|6} layers add filters that specify the negotiation policies used by the keying modules (IKE/AuthIP) during Main Mode (MM) exchanges.</span></span> <span data-ttu-id="b84df-151">Os métodos de autenticação e os algoritmos criptográficos são especificados nessas camadas.</span><span class="sxs-lookup"><span data-stu-id="b84df-151">Authentication methods and cryptographic algorithms are specified at these layers.</span></span>
-   <span data-ttu-id="b84df-152">Na camada FWPM \_ \_ IPSec \_ V {4 \| 6} camadas, adicione filtros que especificam as políticas de negociação usadas pelos módulos de criação de chaves durante as trocas de modo rápido (QM) e modo estendido (em).</span><span class="sxs-lookup"><span data-stu-id="b84df-152">At the FWPM\_LAYER\_IPSEC\_V{4\|6} layers add filters that specify the negotiation policies used by the keying modules during Quick Mode (QM) and Extended Mode (EM) exchanges.</span></span> <span data-ttu-id="b84df-153">Os cabeçalhos IPsec (AH/ESP) e os algoritmos criptográficos são especificados nessas camadas.</span><span class="sxs-lookup"><span data-stu-id="b84df-153">IPsec headers (AH/ESP) and cryptographic algorithms are specified at these layers.</span></span>

    <span data-ttu-id="b84df-154">Uma política de negociação é especificada como um contexto de provedor de política associado ao filtro.</span><span class="sxs-lookup"><span data-stu-id="b84df-154">A negotiation policy is specified as a policy provider context associated with the filter.</span></span> <span data-ttu-id="b84df-155">O módulo de chaveamento enumera os contextos do provedor de política com base nas características de tráfego e obtém a política a ser usada para a negociação de segurança.</span><span class="sxs-lookup"><span data-stu-id="b84df-155">The keying module enumerates the policy provider contexts based on the traffic characteristics and obtains the policy to use for the security negotiation.</span></span>

    > [!Note]  
    > <span data-ttu-id="b84df-156">A API WFP pode ser usada para especificar as associações de segurança (SAs) diretamente e, portanto, ignorar a política de negociação do módulo de chave.</span><span class="sxs-lookup"><span data-stu-id="b84df-156">The WFP API can be used to specify the Security Associations (SAs) directly and therefore to ignore the keying module negotiation policy.</span></span>

     

-   <span data-ttu-id="b84df-157">Nas camadas FWPM do \_ transporte de entrada da camada \_ \_ \_ v {4 \| 6} e do transporte de saída da camada do FWPM \_ \_ \_ \_ v {4 \| 6}, adicione filtros que invoquem textos explicativos e determine qual fluxo de tráfego deve ser protegido.</span><span class="sxs-lookup"><span data-stu-id="b84df-157">At the FWPM\_LAYER\_INBOUND\_TRANSPORT\_V{4\|6} and FWPM\_LAYER\_OUTBOUND\_TRANSPORT\_V{4\|6} layers add filters that invoke callouts and determine which traffic flow should be secured.</span></span>
-   <span data-ttu-id="b84df-158">No FWPM da \_ camada \_ de \_ autenticação Ale, aceite as \_ \_ \_ camadas V {4 \| 6} adicionar filtros que implementam a filtragem de identidade e a política por aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b84df-158">At the FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6} layers add filters that implement identity filtering and per-application policy.</span></span>

<span data-ttu-id="b84df-159">O diagrama a seguir ilustra a interação dos vários componentes de WFP, em relação à operação de IPsec.</span><span class="sxs-lookup"><span data-stu-id="b84df-159">The following diagram illustrates the interaction of the various WFP components, with respect to IPsec operation.</span></span>![configuração de IPSec usando a plataforma de filtragem do Windows](images/ipsec-configuration.jpg)

<span data-ttu-id="b84df-161">Quando o IPsec é configurado, ele se integra com o WFP e estende os recursos de filtragem de WFP, fornecendo informações a serem usadas como condições de filtragem nas camadas de autorização da camada de aplicação (ALE).</span><span class="sxs-lookup"><span data-stu-id="b84df-161">Once IPsec is configured, it integrates with WFP and extends the WFP filtering capabilities by providing information to be used as filtering conditions at the Application Layer Enforcement (ALE) authorization layers.</span></span> <span data-ttu-id="b84df-162">Por exemplo, o IPsec fornece a identidade do usuário remoto e do computador remoto, que a WFP expõe na conexão ALE e aceita camadas de autorização.</span><span class="sxs-lookup"><span data-stu-id="b84df-162">For example, IPsec provides the remote user and remote machine identity, which WFP exposes at the ALE connect and accept authorization layers.</span></span> <span data-ttu-id="b84df-163">Essas informações podem ser usadas para a autorização de identidade remota refinada por uma implementação de firewall baseada em WFP.</span><span class="sxs-lookup"><span data-stu-id="b84df-163">This information can be used for fine-grained remote identity authorization by a WFP-based firewall implementation.</span></span>

<span data-ttu-id="b84df-164">Veja abaixo uma política de isolamento de exemplo que pode ser implementada usando o IPsec:</span><span class="sxs-lookup"><span data-stu-id="b84df-164">Below is a sample isolation policy that may be implemented using IPsec:</span></span>

-   <span data-ttu-id="b84df-165">Camadas FWPM de \_ camada \_ \_ V { \| 4 6} – autenticação Kerberos.</span><span class="sxs-lookup"><span data-stu-id="b84df-165">FWPM\_LAYER\_IKEEXT\_V{4\|6} layers – Kerberos authentication.</span></span>
-   <span data-ttu-id="b84df-166">\_Camada FWPM \_ IPSec \_ V {4 \| 6} camadas – Ah/SHA-1.</span><span class="sxs-lookup"><span data-stu-id="b84df-166">FWPM\_LAYER\_IPSEC\_V{4\|6} layers – AH/SHA-1.</span></span>
-   <span data-ttu-id="b84df-167">\_ \_ Transporte de entrada da camada FWPM \_ \_ v {4 \| 6} e \_ FWPM \_ camada \_ de transporte de saída \_ v {4 \| 6} camadas – descoberta de negociação para todo o tráfego de rede.</span><span class="sxs-lookup"><span data-stu-id="b84df-167">FWPM\_LAYER\_INBOUND\_TRANSPORT\_V{4\|6} and FWPM\_LAYER\_OUTBOUND\_TRANSPORT\_V{4\|6} layers - negotiation discovery for all network traffic.</span></span>
-   <span data-ttu-id="b84df-168">FWPM \_ de \_ autenticação Ale de camada \_ \_ \_ \_ de rede aceita V {4 \| 6} camadas-IPSec necessário para todo o tráfego de redes.</span><span class="sxs-lookup"><span data-stu-id="b84df-168">FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6} layers - IPsec required for all network traffic.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b84df-169">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b84df-169">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="b84df-170">**Camadas WFP**</span><span class="sxs-lookup"><span data-stu-id="b84df-170">**WFP Layers**</span></span>
</dt> <dt>

[<span data-ttu-id="b84df-171">**Filtrando identificadores de camada**</span><span class="sxs-lookup"><span data-stu-id="b84df-171">**Filtering Layer Identifiers**</span></span>](management-filtering-layer-identifiers-.md)
</dt> <dt>

[<span data-ttu-id="b84df-172">Camadas ALE</span><span class="sxs-lookup"><span data-stu-id="b84df-172">ALE Layers</span></span>](ale-layers.md)
</dt> <dt>

<span data-ttu-id="b84df-173">**Cenários de política IPsec implementados usando a API WFP:**</span><span class="sxs-lookup"><span data-stu-id="b84df-173">**IPsec Policy Scenarios Implemented using WFP API:**</span></span>
</dt> <dt>

[<span data-ttu-id="b84df-174">Modo de transporte</span><span class="sxs-lookup"><span data-stu-id="b84df-174">Transport Mode</span></span>](regular-transport-mode.md)
</dt> <dt>

[<span data-ttu-id="b84df-175">Modo de transporte de descoberta de negociação</span><span class="sxs-lookup"><span data-stu-id="b84df-175">Negotiation Discovery Transport Mode</span></span>](negotiation-discovery-transport-mode.md)
</dt> <dt>

[<span data-ttu-id="b84df-176">Modo de transporte de descoberta de negociação no modo de limite</span><span class="sxs-lookup"><span data-stu-id="b84df-176">Negotiation Discovery Transport Mode in Boundary Mode</span></span>](negotiation-discovery-transport-mode-in-boundary-mode.md)
</dt> <dt>

[<span data-ttu-id="b84df-177">Modo de túnel</span><span class="sxs-lookup"><span data-stu-id="b84df-177">Tunnel Mode</span></span>](tunnel-mode.md)
</dt> <dt>

[<span data-ttu-id="b84df-178">Criptografia garantida</span><span class="sxs-lookup"><span data-stu-id="b84df-178">Guaranteed Encryption</span></span>](guaranteed-encryption.md)
</dt> <dt>

[<span data-ttu-id="b84df-179">Autorização de identidade remota</span><span class="sxs-lookup"><span data-stu-id="b84df-179">Remote Identity Authorization</span></span>](remote-identity-authorization.md)
</dt> <dt>

[<span data-ttu-id="b84df-180">SAs IPsec manual</span><span class="sxs-lookup"><span data-stu-id="b84df-180">Manual IPsec SAs</span></span>](manual-ipsec-sas.md)
</dt> <dt>

[<span data-ttu-id="b84df-181">Isenções de IKE/AuthIP</span><span class="sxs-lookup"><span data-stu-id="b84df-181">IKE/AuthIP Exemptions</span></span>](ike-exemptions.md)
</dt> <dt>

<span data-ttu-id="b84df-182">**Soluções IPsec:**</span><span class="sxs-lookup"><span data-stu-id="b84df-182">**IPsec Solutions:**</span></span>
</dt> <dt>

<span data-ttu-id="b84df-183">[Isolamento de domínio e servidor](/previous-versions/windows/it-pro/windows-server-2003/cc776080(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="b84df-183">[Server and Domain Isolation](/previous-versions/windows/it-pro/windows-server-2003/cc776080(v=ws.10))</span></span>
</dt> </dl>

 

 