---
title: Recebendo tráfego não solicitado por Teredo
description: O Teredo fornece conectividade global usando recursos de passagem de NAT e IPv6.
ms.assetid: 0c03d1bb-15f8-4e77-9a96-e182b1d190ac
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a5c7ffe7b84cfa325b3ecd8c0858ad96445e629
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641535"
---
# <a name="receiving-unsolicited-traffic-over-teredo"></a><span data-ttu-id="e2cb7-103">Recebendo tráfego não solicitado por Teredo</span><span class="sxs-lookup"><span data-stu-id="e2cb7-103">Receiving Unsolicited Traffic Over Teredo</span></span>

<span data-ttu-id="e2cb7-104">O [Teredo](about-teredo.md) fornece conectividade global usando recursos de passagem de NAT e IPv6.</span><span class="sxs-lookup"><span data-stu-id="e2cb7-104">[Teredo](about-teredo.md) provides global connectivity using IPv6 and NAT traversal capabilities.</span></span> <span data-ttu-id="e2cb7-105">No entanto, muitos aplicativos, incluindo ponto a ponto, exigirão que o Teredo receba tráfego não solicitado da Internet.</span><span class="sxs-lookup"><span data-stu-id="e2cb7-105">However, many applications, including peer-to-peer, will require Teredo to receive unsolicited traffic from the Internet.</span></span> <span data-ttu-id="e2cb7-106">Um aplicativo pode ser programado para receber tráfego em uma única interface IPv6 ou em todas as interfaces compatíveis com IPv6.</span><span class="sxs-lookup"><span data-stu-id="e2cb7-106">An application can be programmed to receive traffic over a single IPv6 interface or all IPv6-capable interfaces.</span></span> <span data-ttu-id="e2cb7-107">Esta documentação descreve os requisitos para aplicativos que usam a interface Teredo para receber tráfego IPv6 não solicitado.</span><span class="sxs-lookup"><span data-stu-id="e2cb7-107">This documentation describes the requirements for applications that use the Teredo interface to receive unsolicited IPv6 traffic.</span></span>

<span data-ttu-id="e2cb7-108">Um aplicativo receberá tráfego não solicitado pela interface teredo somente se o aplicativo estiver registrado no firewall do [Windows](/previous-versions/windows/desktop/ics/windows-firewall-start-page).</span><span class="sxs-lookup"><span data-stu-id="e2cb7-108">An application will receive unsolicited traffic over the Teredo interface only if the application is registered with [Windows Firewall](/previous-versions/windows/desktop/ics/windows-firewall-start-page).</span></span> <span data-ttu-id="e2cb7-109">Para receber o tráfego não solicitado, deve ocorrer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="e2cb7-109">In order to receive unsolicited traffic the following must occur:</span></span>

-   <span data-ttu-id="e2cb7-110">Os usuários devem ser instruídos a usar o MMC (console de gerenciamento Microsoft) para habilitar a opção de "passagem de borda" para um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e2cb7-110">Users must be instructed to use of the Microsoft Management Console (MMC) to enable the "Edge Traversal" option for an application.</span></span> <span data-ttu-id="e2cb7-111">Essa opção está disponível em Firewall do Windows Snap-In--> <application name> --> guia "avançado". A opção "travessia de borda" deve ser habilitada individualmente para cada aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e2cb7-111">This option is available under Windows Firewall Snap-In --> <application name> --> "Advanced" tab. The "Edge Traversal" option must be enabled individually for each application.</span></span>

-   <span data-ttu-id="e2cb7-112">A opção "travessia de borda" é habilitada pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e2cb7-112">The "Edge Traversal" option is enabled by the application.</span></span> <span data-ttu-id="e2cb7-113">É possível que aplicativos com capacidade de receber tráfego não solicitado registrem-se no firewall do Windows para "travessia de borda" e recebam tráfego não solicitado pela interface teredo.</span><span class="sxs-lookup"><span data-stu-id="e2cb7-113">It is possible for applications capable of receiving unsolicited traffic to register with Windows Firewall for "Edge Traversal" and receive unsolicited traffic over the Teredo interface.</span></span> <span data-ttu-id="e2cb7-114">Para fazer isso, um aplicativo deve chamar a API [**INetFwPolicy2**](/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwpolicy2) com a opção "travessia de borda" definida como Variant \_ true.</span><span class="sxs-lookup"><span data-stu-id="e2cb7-114">To do this an application must call the [**INetFwPolicy2**](/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwpolicy2) API with the "Edge Traversal" option set to VARIANT\_TRUE.</span></span> <span data-ttu-id="e2cb7-115">O consentimento do usuário é necessário para essa chamada à API antes que um aplicativo tenha permissão para escutar o tráfego.</span><span class="sxs-lookup"><span data-stu-id="e2cb7-115">User consent is required for this API call before an application is permitted to listen for the traffic.</span></span>

-   <span data-ttu-id="e2cb7-116">O aplicativo define a opção de soquete de [ \_ \_ nível de proteção](/windows/desktop/WinSock/ipv6-protection-level) do Winsock IPv6 para o **nível de proteção \_ \_ irrestrito** via [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt).</span><span class="sxs-lookup"><span data-stu-id="e2cb7-116">The application sets the Winsock [IPV6\_PROTECTION\_LEVEL](/windows/desktop/WinSock/ipv6-protection-level) socket option to **PROTECTION\_LEVEL\_UNRESTRICTED** via [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt).</span></span> <span data-ttu-id="e2cb7-117">Isso permitirá que o aplicativo receba o tráfego de percurso de borda.</span><span class="sxs-lookup"><span data-stu-id="e2cb7-117">This will allow the application to receive Edge Traversal traffic.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e2cb7-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e2cb7-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e2cb7-119">Recebendo tráfego solicitado por Teredo</span><span class="sxs-lookup"><span data-stu-id="e2cb7-119">Receiving Solicited Traffic Over Teredo</span></span>](receiving-solicited-traffic-over-teredo.md)
</dt> </dl>

 

 