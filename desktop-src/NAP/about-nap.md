---
title: Sobre a NAP
description: Sobre a NAP
ms.assetid: c5dc4956-dcb7-4fcf-b4cc-2fac016427dd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac4227e1291945fa2d3b7876df27c2cc18cdfde2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635010"
---
# <a name="about-nap"></a><span data-ttu-id="edc82-103">Sobre a NAP</span><span class="sxs-lookup"><span data-stu-id="edc82-103">About NAP</span></span>

> [!Note]  
> <span data-ttu-id="edc82-104">A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10</span><span class="sxs-lookup"><span data-stu-id="edc82-104">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="edc82-105">A NAP (proteção de acesso à rede) foi criada para ajudar os administradores a manter a integridade dos computadores na rede, o que ajuda a manter a integridade geral da rede.</span><span class="sxs-lookup"><span data-stu-id="edc82-105">Network Access Protection (NAP) is designed to help administrators maintain the health of the computers on the network, which in turns helps maintain the overall integrity of the network.</span></span> <span data-ttu-id="edc82-106">Ele não foi projetado para proteger uma rede contra usuários mal-intencionados.</span><span class="sxs-lookup"><span data-stu-id="edc82-106">It is not designed to secure a network from malicious users.</span></span> <span data-ttu-id="edc82-107">Por exemplo, se um computador tiver todo o software e as configurações que a política de acesso à rede exigir, o computador será considerado Íntegro ou em conformidade, e ele receberá o acesso apropriado à rede.</span><span class="sxs-lookup"><span data-stu-id="edc82-107">For example, if a computer has all the software and configurations that the network access policy requires, the computer is considered healthy or compliant, and it will be granted the appropriate access to the network.</span></span> <span data-ttu-id="edc82-108">A NAP não impede que um usuário autorizado com um computador em conformidade carregue um programa mal-intencionado na rede ou esteja participando de outro comportamento inadequado.</span><span class="sxs-lookup"><span data-stu-id="edc82-108">NAP does not prevent an authorized user with a compliant computer from uploading a malicious program to the network or engaging in other inappropriate behavior.</span></span>

<span data-ttu-id="edc82-109">Para proteger o acesso a uma rede, uma infraestrutura de rede precisa fornecer as seguintes áreas de funcionalidade:</span><span class="sxs-lookup"><span data-stu-id="edc82-109">To protect access to a network, a network infrastructure needs to provide the following areas of functionality:</span></span>

-   <span data-ttu-id="edc82-110">Validação de integridade: determina se os computadores estão em conformidade com os requisitos de integridade do sistema.</span><span class="sxs-lookup"><span data-stu-id="edc82-110">Health validation: Determines whether the computers are compliant with system health requirements.</span></span>
-   <span data-ttu-id="edc82-111">Restrição de rede: restringe o acesso à rede ou à comunicação para clientes que não estão em conformidade com os requisitos de integridade do sistema.</span><span class="sxs-lookup"><span data-stu-id="edc82-111">Network restriction: Restricts access to the network or communication for clients that do not comply with system health requirements.</span></span>
-   <span data-ttu-id="edc82-112">Correção: fornece as atualizações necessárias para permitir que o computador corrija seu estado de integridade não compatível.</span><span class="sxs-lookup"><span data-stu-id="edc82-112">Remediation: Provides necessary updates to allow the computer to correct its noncompliant health state.</span></span>
-   <span data-ttu-id="edc82-113">Conformidade contínua: permite o acesso à rede, desde que o computador do usuário atenda aos requisitos da política de integridade.</span><span class="sxs-lookup"><span data-stu-id="edc82-113">Ongoing compliance: Permits access to the network as long as the user's computer meets health policy requirements.</span></span>

<span data-ttu-id="edc82-114">O Windows XP com Service Pack 3 (SP3), o Windows Vista e o Windows Server 2008 fornecem métodos de imposição de NAP para a configuração de endereço DHCP, conexões de rede virtual privada (VPN) baseadas em acesso remoto, conexões com e sem fio com base no IEEE 802.1 X e comunicações baseadas em IPsec (Internet Protocol Security).</span><span class="sxs-lookup"><span data-stu-id="edc82-114">Windows XP with Service Pack 3 (SP3), Windows Vista, and Windows Server 2008 provide NAP enforcement methods for Dynamic Host Configuration Protocol (DHCP) address configuration, remote access-based virtual private network (VPN) connections, IEEE 802.1X-authenticated wired and wireless connections, and Internet Protocol security (IPsec)-based communications.</span></span> <span data-ttu-id="edc82-115">Além disso, a plataforma NAP dá suporte a uma arquitetura por meio da qual a validação de integridade, a restrição de rede, a correção e a conformidade contínua têm suporte de componentes adicionais que podem ser fornecidos por fornecedores de software de terceiros ou pela Microsoft.</span><span class="sxs-lookup"><span data-stu-id="edc82-115">The NAP platform additionally supports an architecture through which health validation, network restriction, remediation, and ongoing compliance are supported by additional components that can be supplied by third-party software vendors or by Microsoft.</span></span>

<span data-ttu-id="edc82-116">A plataforma NAP inclui os seguintes componentes:</span><span class="sxs-lookup"><span data-stu-id="edc82-116">The NAP platform includes the following components:</span></span>

-   [<span data-ttu-id="edc82-117">Arquitetura de cliente NAP</span><span class="sxs-lookup"><span data-stu-id="edc82-117">NAP Client Architecture</span></span>](nap-client-architecture.md)
-   [<span data-ttu-id="edc82-118">Arquitetura do lado do servidor NAP</span><span class="sxs-lookup"><span data-stu-id="edc82-118">NAP Server-side Architecture</span></span>](nap-server-side-architecture.md)
-   [<span data-ttu-id="edc82-119">Comunicação do cliente NAP e do componente do lado do servidor</span><span class="sxs-lookup"><span data-stu-id="edc82-119">NAP Client and Server-side Component Communication</span></span>](nap-client-and-server-side-component-communication.md)

<span data-ttu-id="edc82-120">O cliente NAP requer o Windows Vista, o Windows XP com SP3 ou o Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="edc82-120">The NAP client requires Windows Vista, Windows XP with SP3, or Windows Server 2008.</span></span> <span data-ttu-id="edc82-121">O servidor de diretiva de integridade NAP e os pontos de imposição de NAP para imposição de DHCP, VPN e IPsec exigem o Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="edc82-121">The NAP health policy server and NAP enforcement points for DHCP, VPN, and IPsec enforcement require Windows Server 2008.</span></span>

 

 




