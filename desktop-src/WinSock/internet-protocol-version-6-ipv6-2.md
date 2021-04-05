---
description: É importante garantir que novos aplicativos Winsock, bem como aplicativos existentes, sejam totalmente compatíveis com o IPv6.
ms.assetid: 48aa6be8-e8a2-48a5-aa71-3e5ed7032551
title: IPv6 (Protocolo IP Versão 6)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9647b70571b0bc81cbea508cf2e3bb55662efdf0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827112"
---
# <a name="internet-protocol-version-6-ipv6"></a><span data-ttu-id="caedb-103">IPv6 (Protocolo IP Versão 6)</span><span class="sxs-lookup"><span data-stu-id="caedb-103">Internet Protocol Version 6 (IPv6)</span></span>

<span data-ttu-id="caedb-104">É importante garantir que novos aplicativos Winsock, bem como aplicativos existentes, sejam totalmente compatíveis com o IPv6.</span><span class="sxs-lookup"><span data-stu-id="caedb-104">It is important to ensure that new Winsock applications as well as existing applications are fully compatible with IPv6.</span></span> <span data-ttu-id="caedb-105">A disponibilidade do espaço de endereço IPv4 para novas alocações de endereço IPv4 foi esgotada para a Ásia e o Pacífico em 2011.</span><span class="sxs-lookup"><span data-stu-id="caedb-105">The availability of the IPv4 address space for new IPv4 address allocations was exhausted for Asia and the Pacific in 2011.</span></span> <span data-ttu-id="caedb-106">Espera-se que outras partes do mundo sejam esgotadas em alguns anos.</span><span class="sxs-lookup"><span data-stu-id="caedb-106">Other parts of the world are expected to be exhausted in a few years.</span></span>

<span data-ttu-id="caedb-107">Um percentual crescente de novos sites e serviços está disponível usando endereços IPv6.</span><span class="sxs-lookup"><span data-stu-id="caedb-107">A growing percentage of new websites and services are available using IPv6 addresses.</span></span> <span data-ttu-id="caedb-108">Muitos usuários da Internet em mercados emergentes dependem do IPv6 para acesso à Internet.</span><span class="sxs-lookup"><span data-stu-id="caedb-108">Many Internet users in emerging markets are dependent on IPv6 for Internet access.</span></span>

<span data-ttu-id="caedb-109">A Microsoft tem um longo compromisso de dar suporte ao IPv6.</span><span class="sxs-lookup"><span data-stu-id="caedb-109">Microsoft has a long commitment of supporting IPv6.</span></span> <span data-ttu-id="caedb-110">O suporte completo a IPv6 é fornecido no Windows XP com Service Pack 1 (SP1) e posterior.</span><span class="sxs-lookup"><span data-stu-id="caedb-110">Full IPv6 support is provided on Windows XP with Service Pack 1 (SP1) and later.</span></span>

<span data-ttu-id="caedb-111">Este documento fornece informações sobre o suporte do Winsock para IPv6:</span><span class="sxs-lookup"><span data-stu-id="caedb-111">This document provides information about the Winsock support for IPv6:</span></span>

-   [<span data-ttu-id="caedb-112">Usando IPv6</span><span class="sxs-lookup"><span data-stu-id="caedb-112">Using IPv6</span></span>](using-ipv6-2.md)
-   [<span data-ttu-id="caedb-113">Usando o Internet Explorer para acessar sites IPv6</span><span class="sxs-lookup"><span data-stu-id="caedb-113">Using Internet Explorer to Access IPv6 Websites</span></span>](using-internet-explorer-to-access-ipv6-web-sites-2.md)
-   [<span data-ttu-id="caedb-114">Configurações recomendadas para IPv6</span><span class="sxs-lookup"><span data-stu-id="caedb-114">Recommended Configurations for IPv6</span></span>](recommended-configurations-2.md)
-   [<span data-ttu-id="caedb-115">Tópicos adicionais sobre IPv6</span><span class="sxs-lookup"><span data-stu-id="caedb-115">Additional IPv6 Topics</span></span>](additional-topics-2.md)

<span data-ttu-id="caedb-116">Para obter informações adicionais sobre como adicionar funcionalidades do IPv6 aos seus aplicativos do Windows Sockets, consulte [Guia do IPv6 para aplicativos do Windows Sockets](ipv6-guide-for-windows-sockets-applications-2.md).</span><span class="sxs-lookup"><span data-stu-id="caedb-116">For additional information on adding IPv6 capability to your Windows Sockets applications, see [IPv6 Guide for Windows Sockets Applications](ipv6-guide-for-windows-sockets-applications-2.md).</span></span>

<span data-ttu-id="caedb-117">Uma introdução ao protocolo IPv6 juntamente com visões gerais sobre a implantação e tecnologias de transição IPv6 está disponível no TechNet no [Microsoft Internet Protocol versão 6 (IPv6)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/dd379473(v=ws.10)).</span><span class="sxs-lookup"><span data-stu-id="caedb-117">An introduction to the IPv6 protocol along with overviews on deployment and IPv6 transitioning technologies is available on Technet at [Microsoft Internet Protocol Version 6 (IPv6)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/dd379473(v=ws.10)).</span></span>

## <a name="related-topics"></a><span data-ttu-id="caedb-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="caedb-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="caedb-119">Guia IPv6 para aplicativos do Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="caedb-119">IPv6 Guide for Windows Sockets Applications</span></span>](ipv6-guide-for-windows-sockets-applications-2.md)
</dt> <dt>

[<span data-ttu-id="caedb-120">Suporte a IPv6</span><span class="sxs-lookup"><span data-stu-id="caedb-120">IPv6 Support</span></span>](ipv6-support-2.md)
</dt> <dt>

[<span data-ttu-id="caedb-121">Versão prévia da tecnologia IPv6 para Windows 2000</span><span class="sxs-lookup"><span data-stu-id="caedb-121">IPv6 Technology Preview for Windows 2000</span></span>](https://www.microsoft.com/downloads/details.aspx?FamilyID=27b1e6a6-bbdd-43c9-af57-dae19795a088)
</dt> <dt>

<span data-ttu-id="caedb-122">[Protocolo IP versão 6 (IPv6) da Microsoft](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/dd379473(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="caedb-122">[Microsoft Internet Protocol Version 6 (IPv6)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/dd379473(v=ws.10))</span></span>
</dt> </dl>

 

 
