---
description: A \_ opção de soquete de nível de proteção IPv6 \_ permite que os desenvolvedores coloquem restrições de acesso em soquetes IPv6.
ms.assetid: bfb934b3-1e86-431f-a21c-880048d32d35
title: IPV6_PROTECTION_LEVEL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e2a8dd70bb1fb5b21f74f8939f11da0d9e2a3ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105810628"
---
# <a name="ipv6_protection_level"></a><span data-ttu-id="de6a7-103">\_Nível de proteção IPv6 \_</span><span class="sxs-lookup"><span data-stu-id="de6a7-103">IPV6\_PROTECTION\_LEVEL</span></span>

<span data-ttu-id="de6a7-104">A \_ opção de soquete de nível de proteção IPv6 \_ permite que os desenvolvedores coloquem restrições de acesso em soquetes IPv6.</span><span class="sxs-lookup"><span data-stu-id="de6a7-104">The IPV6\_PROTECTION\_LEVEL socket option enables developers to place access restrictions on IPv6 sockets.</span></span> <span data-ttu-id="de6a7-105">Essas restrições permitem que um aplicativo em execução em uma LAN privada proteja-se de modo simples e robusto contra ataques externos.</span><span class="sxs-lookup"><span data-stu-id="de6a7-105">Such restrictions enable an application running on a private LAN to simply and robustly harden itself against external attacks.</span></span> <span data-ttu-id="de6a7-106">A \_ opção de soquete de nível de proteção IPv6 \_ amplia ou limita o escopo de um soquete de escuta, habilitando o acesso irrestrito de usuários públicos e privados quando apropriado ou restringindo o acesso somente ao mesmo site, conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="de6a7-106">The IPV6\_PROTECTION\_LEVEL socket option widens or narrows the scope of a listening socket, enabling unrestricted access from public and private users when appropriate, or restricting access only to the same site, as required.</span></span>

<span data-ttu-id="de6a7-107">\_No momento, o nível de proteção IPv6 \_ tem três níveis de proteção definidos.</span><span class="sxs-lookup"><span data-stu-id="de6a7-107">IPV6\_PROTECTION\_LEVEL currently has three defined protection levels.</span></span>



| <span data-ttu-id="de6a7-108">Nível de proteção</span><span class="sxs-lookup"><span data-stu-id="de6a7-108">Protection level</span></span>                                                                                                                                 | <span data-ttu-id="de6a7-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="de6a7-109">Description</span></span>                                                                                                                                                                                                                                                                                                                        |
|--------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="de6a7-110"><span id="PROTECTION_LEVEL_UNRESTRICTED"></span><span id="protection_level_unrestricted"></span>nível de proteção \_ \_ irrestrito</span><span class="sxs-lookup"><span data-stu-id="de6a7-110"><span id="PROTECTION_LEVEL_UNRESTRICTED"></span><span id="protection_level_unrestricted"></span>PROTECTION\_LEVEL\_UNRESTRICTED</span></span><br/>       | <span data-ttu-id="de6a7-111">Usado por aplicativos projetados para operar na Internet, incluindo aplicativos que aproveitam recursos de passagem NAT do IPv6 incorporados ao Windows (Teredo, por exemplo).</span><span class="sxs-lookup"><span data-stu-id="de6a7-111">Used by applications designed to operate across the Internet, including applications taking advantage of IPv6 NAT traversal capabilities built into Windows (Teredo, for example).</span></span> <span data-ttu-id="de6a7-112">Esses aplicativos podem ignorar firewalls IPv4, de modo que os aplicativos devem ser protegidos contra ataques de Internet direcionados à porta aberta.</span><span class="sxs-lookup"><span data-stu-id="de6a7-112">These applications may bypass IPv4 firewalls, so applications must be hardened against Internet attacks directed at the opened port.</span></span><br/> |
| <span data-ttu-id="de6a7-113"><span id="PROTECTION_LEVEL_EDGERESTRICTED"></span><span id="protection_level_edgerestricted"></span>nível de proteção \_ \_ EDGERESTRICTED</span><span class="sxs-lookup"><span data-stu-id="de6a7-113"><span id="PROTECTION_LEVEL_EDGERESTRICTED"></span><span id="protection_level_edgerestricted"></span>PROTECTION\_LEVEL\_EDGERESTRICTED</span></span><br/> | <span data-ttu-id="de6a7-114">Usado por aplicativos projetados para operar pela Internet.</span><span class="sxs-lookup"><span data-stu-id="de6a7-114">Used by applications designed to operate across the Internet.</span></span> <span data-ttu-id="de6a7-115">Essa configuração não permite passagem NAT usando a implementação do Windows Teredo.</span><span class="sxs-lookup"><span data-stu-id="de6a7-115">This setting does not allow NAT traversal using the Windows Teredo implementation.</span></span> <span data-ttu-id="de6a7-116">Esses aplicativos podem ignorar firewalls IPv4, de modo que os aplicativos devem ser protegidos contra ataques de Internet direcionados à porta aberta.</span><span class="sxs-lookup"><span data-stu-id="de6a7-116">These applications may bypass IPv4 firewalls, so applications must be hardened against Internet attacks directed at the opened port.</span></span><br/>                                   |
| <span data-ttu-id="de6a7-117"><span id="PROTECTION_LEVEL_RESTRICTED"></span><span id="protection_level_restricted"></span>nível de proteção \_ \_ restrito</span><span class="sxs-lookup"><span data-stu-id="de6a7-117"><span id="PROTECTION_LEVEL_RESTRICTED"></span><span id="protection_level_restricted"></span>PROTECTION\_LEVEL\_RESTRICTED</span></span><br/>             | <span data-ttu-id="de6a7-118">Usado por aplicativos de intranet que não implementam cenários da Internet.</span><span class="sxs-lookup"><span data-stu-id="de6a7-118">Used by intranet applications that do not implement Internet scenarios.</span></span> <span data-ttu-id="de6a7-119">Esses aplicativos geralmente não são testados nem protegidos contra ataques do estilo usado na Internet.</span><span class="sxs-lookup"><span data-stu-id="de6a7-119">These applications are generally not tested or hardened against Internet-style attacks.</span></span><br/> <span data-ttu-id="de6a7-120">Essa configuração limitará o tráfego recebido para apenas link-local.</span><span class="sxs-lookup"><span data-stu-id="de6a7-120">This setting will limit the received traffic to link-local only.</span></span><br/>                                                                             |



 

<span data-ttu-id="de6a7-121">O exemplo de código a seguir fornece os valores definidos para cada um:</span><span class="sxs-lookup"><span data-stu-id="de6a7-121">The following code example provides the defined values for each:</span></span>

``` syntax
#define PROTECTION_LEVEL_UNRESTRICTED   10  /* for peer-to-peer apps */
#define PROTECTION_LEVEL_EDGERESTRICTED 20  /* Same as unrestricted, except for Teredo  */
#define PROTECTION_LEVEL_RESTRICTED     30  /* for Intranet apps     */
```

<span data-ttu-id="de6a7-122">Esses valores são mutuamente exclusivos e não podem ser combinados em uma única chamada de função [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) .</span><span class="sxs-lookup"><span data-stu-id="de6a7-122">These values are mutually exclusive, and cannot be combined in a single [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) function call.</span></span> <span data-ttu-id="de6a7-123">Outros valores para essa opção de soquete são reservados.</span><span class="sxs-lookup"><span data-stu-id="de6a7-123">Other values for this socket option are reserved.</span></span> <span data-ttu-id="de6a7-124">Esses níveis de proteção se aplicam somente a conexões de entrada.</span><span class="sxs-lookup"><span data-stu-id="de6a7-124">These protection levels apply only to incoming connections.</span></span> <span data-ttu-id="de6a7-125">A definição dessa opção de soquete não tem nenhum efeito sobre os pacotes de saída ou conexões.</span><span class="sxs-lookup"><span data-stu-id="de6a7-125">Setting this socket option has no effect on outbound packets or connections.</span></span>

<span data-ttu-id="de6a7-126">No Windows 7 e no Windows Server 2008 R2, o valor padrão para o \_ nível de proteção IPv6 \_ não é especificado e o **\_ \_ padrão de nível de proteção** é definido como-1, um valor ilegal para o nível de proteção IPv6 \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="de6a7-126">On Windows 7 and Windows Server 2008 R2, the default value for IPV6\_PROTECTION\_LEVEL is unspecified and **PROTECTION\_LEVEL\_DEFAULT** is defined to -1, an illegal value for IPV6\_PROTECTION\_LEVEL.</span></span>

<span data-ttu-id="de6a7-127">No Windows Vista e no Windows Server 2008, o valor padrão para o \_ nível de proteção IPv6 é o nível de \_ **proteção \_ \_ irrestrito** e o **\_ \_ padrão de nível de proteção** é definido como-1, um valor ilegal para o nível de proteção IPv6 \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="de6a7-127">On Windows Vista and Windows Server 2008, the default value for IPV6\_PROTECTION\_LEVEL is **PROTECTION\_LEVEL\_UNRESTRICTED** and **PROTECTION\_LEVEL\_DEFAULT** is defined to -1, an illegal value for IPV6\_PROTECTION\_LEVEL.</span></span>

<span data-ttu-id="de6a7-128">No Windows Server 2003 e no Windows XP, o valor padrão para o \_ nível de proteção IPv6 é o nível de \_ **proteção \_ \_ EDGERESTRICTED** e o **\_ \_ padrão de nível de proteção** é definido para ser o nível de **proteção \_ \_ EDGERESTRICTED**.</span><span class="sxs-lookup"><span data-stu-id="de6a7-128">On Windows Server 2003 and Windows XP, the default value for IPV6\_PROTECTION\_LEVEL is **PROTECTION\_LEVEL\_EDGERESTRICTED** and **PROTECTION\_LEVEL\_DEFAULT** is defined to be **PROTECTION\_LEVEL\_EDGERESTRICTED**.</span></span>

> [!Note]  
> <span data-ttu-id="de6a7-129">A \_ opção de soquete de nível de proteção IPv6 \_ deve ser definida antes do soquete ser associado.</span><span class="sxs-lookup"><span data-stu-id="de6a7-129">The IPV6\_PROTECTION\_LEVEL socket option should be set before the socket is bound.</span></span> <span data-ttu-id="de6a7-130">Caso contrário, os pacotes recebidos entre chamadas [**BIND**](/windows/desktop/api/winsock/nf-winsock-bind) e [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) estarão em conformidade com o **nível de proteção \_ \_ EDGERESTRICTED** e poderão ser entregues ao aplicativo.</span><span class="sxs-lookup"><span data-stu-id="de6a7-130">Otherwise, packets received between [**bind**](/windows/desktop/api/winsock/nf-winsock-bind) and [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) calls will conform to **PROTECTION\_LEVEL\_EDGERESTRICTED**, and may be delivered to the application.</span></span>

 

<span data-ttu-id="de6a7-131">A tabela a seguir descreve o efeito de aplicar cada nível de proteção a um soquete de escuta.</span><span class="sxs-lookup"><span data-stu-id="de6a7-131">The following table describes the effect of applying each protection level to a listening socket.</span></span>

<span data-ttu-id="de6a7-132">Nível de proteção</span><span class="sxs-lookup"><span data-stu-id="de6a7-132">Protection level</span></span>

<span data-ttu-id="de6a7-133">Tráfego de entrada permitido</span><span class="sxs-lookup"><span data-stu-id="de6a7-133">Incoming traffic permitted</span></span>

<span data-ttu-id="de6a7-134">Mesmo site</span><span class="sxs-lookup"><span data-stu-id="de6a7-134">Same site</span></span>

<span data-ttu-id="de6a7-135">Externo</span><span class="sxs-lookup"><span data-stu-id="de6a7-135">External</span></span>

<span data-ttu-id="de6a7-136">NAT Traversal (Teredo)</span><span class="sxs-lookup"><span data-stu-id="de6a7-136">NAT traversal (Teredo)</span></span>

<span data-ttu-id="de6a7-137">nível de proteção \_ \_ restrito</span><span class="sxs-lookup"><span data-stu-id="de6a7-137">PROTECTION\_LEVEL\_RESTRICTED</span></span>

<span data-ttu-id="de6a7-138">Sim</span><span class="sxs-lookup"><span data-stu-id="de6a7-138">Yes</span></span>

<span data-ttu-id="de6a7-139">Não</span><span class="sxs-lookup"><span data-stu-id="de6a7-139">No</span></span>

<span data-ttu-id="de6a7-140">Não</span><span class="sxs-lookup"><span data-stu-id="de6a7-140">No</span></span>

<span data-ttu-id="de6a7-141">nível de proteção \_ \_ EDGERESTRICTED</span><span class="sxs-lookup"><span data-stu-id="de6a7-141">PROTECTION\_LEVEL\_EDGERESTRICTED</span></span>

<span data-ttu-id="de6a7-142">Sim</span><span class="sxs-lookup"><span data-stu-id="de6a7-142">Yes</span></span>

<span data-ttu-id="de6a7-143">Sim</span><span class="sxs-lookup"><span data-stu-id="de6a7-143">Yes</span></span>

<span data-ttu-id="de6a7-144">Não</span><span class="sxs-lookup"><span data-stu-id="de6a7-144">No</span></span>

<span data-ttu-id="de6a7-145">nível de proteção \_ \_ irrestrito</span><span class="sxs-lookup"><span data-stu-id="de6a7-145">PROTECTION\_LEVEL\_UNRESTRICTED</span></span>

<span data-ttu-id="de6a7-146">Sim</span><span class="sxs-lookup"><span data-stu-id="de6a7-146">Yes</span></span>

<span data-ttu-id="de6a7-147">Sim</span><span class="sxs-lookup"><span data-stu-id="de6a7-147">Yes</span></span>

<span data-ttu-id="de6a7-148">Sim</span><span class="sxs-lookup"><span data-stu-id="de6a7-148">Yes</span></span>



 

<span data-ttu-id="de6a7-149">Na tabela acima, a mesma coluna de **site** é uma combinação do seguinte:</span><span class="sxs-lookup"><span data-stu-id="de6a7-149">In the table above, the **Same site** column is a combination of the following:</span></span>

-   <span data-ttu-id="de6a7-150">Vincular endereços locais</span><span class="sxs-lookup"><span data-stu-id="de6a7-150">Link local addresses</span></span>
-   <span data-ttu-id="de6a7-151">Endereços locais do site</span><span class="sxs-lookup"><span data-stu-id="de6a7-151">Site Local addresses</span></span>
-   <span data-ttu-id="de6a7-152">Endereços globais conhecidos por pertencerem ao mesmo site (correspondendo à tabela de prefixo do site)</span><span class="sxs-lookup"><span data-stu-id="de6a7-152">Global addresses known to belong to the same site (matching the site prefix table)</span></span>

<span data-ttu-id="de6a7-153">No Windows 7 e no Windows Server 2008 R2, o valor padrão para o \_ nível de proteção IPv6 \_ não é especificado.</span><span class="sxs-lookup"><span data-stu-id="de6a7-153">On Windows 7 and Windows Server 2008 R2, the default value for IPV6\_PROTECTION\_LEVEL is unspecified.</span></span> <span data-ttu-id="de6a7-154">Se não houver nenhum software de firewall com reconhecimento de borda instalado no computador local (o Firewall do Windows está desabilitado ou algum outro firewall está instalado e ignora o tráfego de Teredo), você receberá o tráfego de Teredo somente se definir a \_ opção de soquete de nível de proteção IPv6 \_ como nível de **proteção \_ \_ irrestrito**.</span><span class="sxs-lookup"><span data-stu-id="de6a7-154">If there is no edge-traversal aware firewall software installed on the local computer (Windows firewall is disabled or some other firewall is installed that ignores Teredo traffic), you will receive Teredo traffic only if you set the IPV6\_PROTECTION\_LEVEL socket option to **PROTECTION\_LEVEL\_UNRESTRICTED**.</span></span> <span data-ttu-id="de6a7-155">No entanto, o Firewall do Windows ou qualquer política de firewall com reconhecimento de borda transversal pode ignorar essa opção com base nas configurações de política do firewall.</span><span class="sxs-lookup"><span data-stu-id="de6a7-155">However, Windows firewall or any edge-traversal aware firewall policy may ignore this option based on policy settings for the firewall.</span></span> <span data-ttu-id="de6a7-156">Ao definir essa opção de soquete para o **nível de proteção \_ \_ irrestrito**, o aplicativo está comunicando sua intenção explícita de receber o tráfego de borda atravessado pelo firewall do host instalado no computador local.</span><span class="sxs-lookup"><span data-stu-id="de6a7-156">By setting this socket option to **PROTECTION\_LEVEL\_UNRESTRICTED**, the application is communicating its explicit intent to receive edge traversed traffic by the host firewall installed on the local machine.</span></span> <span data-ttu-id="de6a7-157">Portanto, se houver um firewall de host com reconhecimento de borda, ele terá a decisão final sobre a aceitação de um pacote.</span><span class="sxs-lookup"><span data-stu-id="de6a7-157">So if there is an edge-traversal aware host firewall installed, it will have the final decision on accepting a packet.</span></span> <span data-ttu-id="de6a7-158">Por padrão, sem qualquer conjunto de opções de soquete:</span><span class="sxs-lookup"><span data-stu-id="de6a7-158">By default, without any socket option set:</span></span>

-   <span data-ttu-id="de6a7-159">o se o Firewall do Windows estiver habilitado (ou se outro firewall de host com reconhecimento de borda estiver instalado) no computador local, o que for imposto será observado.</span><span class="sxs-lookup"><span data-stu-id="de6a7-159">o If Windows firewall is enabled (or another edge-traversal aware host firewall is installed) on the local computer, whatever it enforces will be observed.</span></span> <span data-ttu-id="de6a7-160">O firewall de host com reconhecimento de borda típico bloqueará o tráfego de Teredo por padrão.</span><span class="sxs-lookup"><span data-stu-id="de6a7-160">Typical edge-traversal aware host firewall will block Teredo traffic by default.</span></span> <span data-ttu-id="de6a7-161">Portanto, os aplicativos observarão o padrão como se fosse o **nível de proteção \_ \_ EDGERESTRICTED**.</span><span class="sxs-lookup"><span data-stu-id="de6a7-161">Therefore applications will observe the default as if it was **PROTECTION\_LEVEL\_EDGERESTRICTED**.</span></span>
-   <span data-ttu-id="de6a7-162">o se o Firewall do Windows não estiver habilitado e nenhum outro firewall de host com reconhecimento de borda estiver instalado no sistema local, o padrão será **o \_ nível \_ de proteção EDGERESTRICTED**.</span><span class="sxs-lookup"><span data-stu-id="de6a7-162">o If Windows firewall is not enabled and no other edge-traversal aware host firewall is installed on the local system, the default will be **PROTECTION\_LEVEL\_EDGERESTRICTED**.</span></span>

<span data-ttu-id="de6a7-163">No Windows Vista e no Windows Server 2008, o valor padrão para \_ nível de proteção IPv6 \_ é o nível de **proteção \_ \_ irrestrito**.</span><span class="sxs-lookup"><span data-stu-id="de6a7-163">On Windows Vista and Windows Server 2008, the default value for IPV6\_PROTECTION\_LEVEL is **PROTECTION\_LEVEL\_UNRESTRICTED**.</span></span> <span data-ttu-id="de6a7-164">Mas o valor efetivo depende se o Firewall do Windows está habilitado.</span><span class="sxs-lookup"><span data-stu-id="de6a7-164">But the effective value depends on whether Windows firewall is enabled.</span></span> <span data-ttu-id="de6a7-165">O Firewall do Windows tem reconhecimento de percurso de borda (reconhecimento de Teredo), independentemente do valor definido para o nível de proteção IPV6 e ignora se o nível de proteção \_ \_ IPv6 \_ \_ é **\_ \_ irrestrito no nível de proteção**.</span><span class="sxs-lookup"><span data-stu-id="de6a7-165">The Windows firewall is edge-traversal aware (Teredo aware), no matter what value is set for the IPV6\_PROTECTION\_LEVEL and ignores if IPV6\_PROTECTION\_LEVEL is **PROTECTION\_LEVEL\_UNRESTRICTED**.</span></span> <span data-ttu-id="de6a7-166">Portanto, o valor efetivo depende da política de firewall.</span><span class="sxs-lookup"><span data-stu-id="de6a7-166">So the effective value depends on the firewall policy.</span></span> <span data-ttu-id="de6a7-167">Quando o Firewall do Windows está desabilitado e nenhum outro firewall com reconhecimento de borda, está instalado no computador local, o valor padrão do \_ nível de proteção IPv6 \_ é **\_ \_ irrestrito de nível de proteção**.</span><span class="sxs-lookup"><span data-stu-id="de6a7-167">When Windows firewall is disabled and no other edge-traversal aware firewall is installed on the local computer, the default value for IPV6\_PROTECTION\_LEVEL is **PROTECTION\_LEVEL\_UNRESTRICTED**.</span></span>

<span data-ttu-id="de6a7-168">No Windows Server 2003 e no Windows XP, o valor padrão para o \_ nível de proteção IPv6 é o nível de \_ **proteção \_ \_ EDGERESTRICTED**.</span><span class="sxs-lookup"><span data-stu-id="de6a7-168">On Windows Server 2003 and Windows XP, the default value for IPV6\_PROTECTION\_LEVEL is **PROTECTION\_LEVEL\_EDGERESTRICTED**.</span></span> <span data-ttu-id="de6a7-169">A menos que você tenha definido a \_ opção de soquete de nível de proteção IPv6 para o \_ **nível de proteção \_ \_ irrestrito**, você não receberá nenhum tráfego Teredo.</span><span class="sxs-lookup"><span data-stu-id="de6a7-169">Unless you have set the IPV6\_PROTECTION\_LEVEL socket option to **PROTECTION\_LEVEL\_UNRESTRICTED**, you would not receive any Teredo traffic.</span></span>

<span data-ttu-id="de6a7-170">Dependendo do nível de proteção do IPV6 \_ \_ , um aplicativo que requer tráfego não solicitado da Internet pode não ser capaz de receber tráfego não solicitado.</span><span class="sxs-lookup"><span data-stu-id="de6a7-170">Depending on the IPV6\_PROTECTION\_LEVEL, an application that requires unsolicited traffic from the Internet may not be capable of receiving unsolicited traffic.</span></span> <span data-ttu-id="de6a7-171">No entanto, esses requisitos não são necessários para receber tráfego solicitado pela interface do Windows Teredo.</span><span class="sxs-lookup"><span data-stu-id="de6a7-171">However, these requirements are not necessary for receiving solicited traffic over the Windows Teredo interface.</span></span> <span data-ttu-id="de6a7-172">Para obter mais detalhes sobre a interação com o Teredo, consulte [recebendo tráfego solicitado por Teredo](../teredo/receiving-solicited-traffic-over-teredo.md).</span><span class="sxs-lookup"><span data-stu-id="de6a7-172">For more details on the interaction with Teredo, see [Receiving Solicited Traffic Over Teredo](../teredo/receiving-solicited-traffic-over-teredo.md).</span></span>

<span data-ttu-id="de6a7-173">Quando os pacotes de entrada ou conexões são recusados devido ao nível de proteção definido, a rejeição é tratada como se nenhum aplicativo estivesse escutando nesse soquete.</span><span class="sxs-lookup"><span data-stu-id="de6a7-173">When incoming packets or connections are refused due to the set protection level, rejection is handled as if no application was listening on that socket.</span></span>

> [!Note]
>
> <span data-ttu-id="de6a7-174">A opção de soquete de nível de proteção IPV6 não \_ \_ necessariamente coloca restrições de acesso em soquetes IPv6 ou restrição de NAT transversal usando algum método diferente do Windows Teredo ou até mesmo usando outra implementação de Teredo por outro fornecedor.</span><span class="sxs-lookup"><span data-stu-id="de6a7-174">The IPV6\_PROTECTION\_LEVEL socket option does not necessarily place access restrictions on IPv6 sockets or restrict NAT traversal using some method other than Windows Teredo or even using another implementation of Teredo by another vendor.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="de6a7-175">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="de6a7-175">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="de6a7-176">**getsockopt**</span><span class="sxs-lookup"><span data-stu-id="de6a7-176">**getsockopt**</span></span>](/windows/desktop/api/winsock/nf-winsock-getsockopt)
</dt> <dt>

[<span data-ttu-id="de6a7-177">Recebendo tráfego solicitado por Teredo</span><span class="sxs-lookup"><span data-stu-id="de6a7-177">Receiving Solicited Traffic Over Teredo</span></span>](../teredo/receiving-solicited-traffic-over-teredo.md)
</dt> <dt>

[<span data-ttu-id="de6a7-178">**setsockopt**</span><span class="sxs-lookup"><span data-stu-id="de6a7-178">**setsockopt**</span></span>](/windows/desktop/api/winsock/nf-winsock-setsockopt)
</dt> </dl>

 

 
