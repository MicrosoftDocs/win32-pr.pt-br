---
title: Servidores de Active Directory e DNS dinâmico
description: Os servidores de Active Directory publicam seus endereços de modo que os clientes possam encontrá-los sabendo apenas o nome de domínio.
ms.assetid: b4928d53-2629-4ddb-bb43-ce7a187b41e2
ms.tgt_platform: multiple
keywords:
- Active Directory de DNS dinâmico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 971987cb73b65e46b36eda4c713054ba2796e63b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103634809"
---
# <a name="active-directory-servers-and-dynamic-dns"></a><span data-ttu-id="4b0da-104">Servidores de Active Directory e DNS dinâmico</span><span class="sxs-lookup"><span data-stu-id="4b0da-104">Active Directory Servers and Dynamic DNS</span></span>

<span data-ttu-id="4b0da-105">Os servidores de Active Directory publicam seus endereços de modo que os clientes possam encontrá-los sabendo apenas o nome de domínio.</span><span class="sxs-lookup"><span data-stu-id="4b0da-105">The Active Directory servers publish their addresses such that clients can find them knowing only the domain name.</span></span> <span data-ttu-id="4b0da-106">Os servidores de Active Directory são publicados usando os registros de recursos de serviço (SRV RRs) no DNS.</span><span class="sxs-lookup"><span data-stu-id="4b0da-106">Active Directory servers are published using the Service Resource Records (SRV RRs) in DNS.</span></span> <span data-ttu-id="4b0da-107">O RR SRV é um registro DNS usado para mapear o nome de um serviço para o endereço de um servidor que oferece o serviço.</span><span class="sxs-lookup"><span data-stu-id="4b0da-107">The SRV RR is a DNS record used to map the name of a service to the address of a server that offers the service.</span></span> <span data-ttu-id="4b0da-108">O nome de um RR SRV está neste formato:</span><span class="sxs-lookup"><span data-stu-id="4b0da-108">The name of a SRV RR is in this form:</span></span>


```C++
<service>.<protocol>.<domain>
```



<span data-ttu-id="4b0da-109">Os servidores de Active Directory oferecem o serviço LDAP sobre o protocolo TCP para que os nomes publicados sejam "LDAP. TCP. <domain> ".</span><span class="sxs-lookup"><span data-stu-id="4b0da-109">Active Directory servers offer the LDAP service over the TCP protocol so that published names are "ldap.tcp.<domain>".</span></span> <span data-ttu-id="4b0da-110">Portanto, o RR SRV para fabrikam.com é "ldap.tcp.fabrikam.com".</span><span class="sxs-lookup"><span data-stu-id="4b0da-110">Thus, the SRV RR for fabrikam.com is "ldap.tcp.fabrikam.com".</span></span> <span data-ttu-id="4b0da-111">Dados adicionais sobre o RR SRV indicam a prioridade e o peso do servidor, permitindo que os clientes escolham o melhor servidor para suas necessidades.</span><span class="sxs-lookup"><span data-stu-id="4b0da-111">Additional data about the SRV RR indicates the priority and weight for the server, enabling clients to choose the best server for their needs.</span></span>

<span data-ttu-id="4b0da-112">Quando um servidor de Active Directory é instalado, ele usa o DNS dinâmico para publicar a si mesmo.</span><span class="sxs-lookup"><span data-stu-id="4b0da-112">When an Active Directory server is installed, it uses Dynamic DNS to publish itself.</span></span> <span data-ttu-id="4b0da-113">Como os endereços TCP/IP estão sujeitos a alterações, os servidores verificam periodicamente seus registros para certificar-se de que estão corretos e atualizá-los se necessário.</span><span class="sxs-lookup"><span data-stu-id="4b0da-113">Because TCP/IP addresses are subject to change, servers periodically verify their registrations to be sure they are correct, and update them if necessary.</span></span>

<span data-ttu-id="4b0da-114">O DNS dinâmico é uma adição recente ao padrão de DNS.</span><span class="sxs-lookup"><span data-stu-id="4b0da-114">Dynamic DNS is a recent addition to the DNS standard.</span></span> <span data-ttu-id="4b0da-115">O DNS dinâmico define um protocolo para atualizar dinamicamente um servidor DNS com novos dados.</span><span class="sxs-lookup"><span data-stu-id="4b0da-115">Dynamic DNS defines a protocol for dynamically updating a DNS server with new data.</span></span> <span data-ttu-id="4b0da-116">Antes do DNS dinâmico, os administradores eram solicitados a configurar manualmente os registros armazenados por servidores DNS.</span><span class="sxs-lookup"><span data-stu-id="4b0da-116">Prior to Dynamic DNS, administrators were required to manually configure the records stored by DNS servers.</span></span>

 

 




