---
title: ODJ_POLICY_DNS_DOMAIN_INFO
description: Definição de IDL de ODJ_POLICY_DNS_DOMAIN_INFO
ms.assetid: 44b1145f-3bdd-42cd-a88f-9b41888cc644
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 36b7759451811844a91b3ee66ff3460fa4c4db34
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/14/2020
ms.locfileid: "103642947"
---
# <a name="odj_policy_dns_domain_info-structure"></a><span data-ttu-id="75f59-103">Estrutura de ODJ_POLICY_DNS_DOMAIN_INFO</span><span class="sxs-lookup"><span data-stu-id="75f59-103">ODJ_POLICY_DNS_DOMAIN_INFO structure</span></span>

<span data-ttu-id="75f59-104">Contém informações sobre o domínio e a floresta para os quais um cliente deve ser associado.</span><span class="sxs-lookup"><span data-stu-id="75f59-104">Contains information about the domain and forest that a client should be joined to.</span></span>

## <a name="syntax"></a><span data-ttu-id="75f59-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="75f59-105">Syntax</span></span>

```C++
typedef struct _ODJ_POLICY_DNS_DOMAIN_INFO
{
    ODJ_UNICODE_STRING Name;
    ODJ_UNICODE_STRING DnsDomainName;
    ODJ_UNICODE_STRING DnsForestName;
    GUID DomainGuid;
    PODJ_SID Sid;
} ODJ_POLICY_DNS_DOMAIN_INFO;
```

## <a name="members"></a><span data-ttu-id="75f59-106">Membros</span><span class="sxs-lookup"><span data-stu-id="75f59-106">Members</span></span>

### <a name="name"></a><span data-ttu-id="75f59-107">Name</span><span class="sxs-lookup"><span data-stu-id="75f59-107">Name</span></span>

<span data-ttu-id="75f59-108">Deve ser definido como um nome de domínio NetBIOS.</span><span class="sxs-lookup"><span data-stu-id="75f59-108">Must be set to a Netbios domain name.</span></span>

### <a name="dnsdomainname"></a><span data-ttu-id="75f59-109">DnsDomainName</span><span class="sxs-lookup"><span data-stu-id="75f59-109">DnsDomainName</span></span>

<span data-ttu-id="75f59-110">Deve ser definido como um nome de domínio no formato DNS.</span><span class="sxs-lookup"><span data-stu-id="75f59-110">Must be set to a domain name in DNS format.</span></span>

### <a name="dnsforestname"></a><span data-ttu-id="75f59-111">DnsForestName</span><span class="sxs-lookup"><span data-stu-id="75f59-111">DnsForestName</span></span>

<span data-ttu-id="75f59-112">Deve ser definido como um nome de floresta no formato DNS.</span><span class="sxs-lookup"><span data-stu-id="75f59-112">Must be set to a forest name in DNS format.</span></span>

### <a name="domainguid"></a><span data-ttu-id="75f59-113">DomainGuid</span><span class="sxs-lookup"><span data-stu-id="75f59-113">DomainGuid</span></span>

<span data-ttu-id="75f59-114">Deve ser definido como o GUID de domínio.</span><span class="sxs-lookup"><span data-stu-id="75f59-114">Must be set to the domain guid.</span></span>

### <a name="sid"></a><span data-ttu-id="75f59-115">Sid</span><span class="sxs-lookup"><span data-stu-id="75f59-115">Sid</span></span>

<span data-ttu-id="75f59-116">Deve ser definido como o SID do domínio.</span><span class="sxs-lookup"><span data-stu-id="75f59-116">Must be set to the domain sid.</span></span>

## <a name="see-also"></a><span data-ttu-id="75f59-117">Consulte também</span><span class="sxs-lookup"><span data-stu-id="75f59-117">See also</span></span>

[<span data-ttu-id="75f59-118">**Definições de IDL de ingresso no domínio offline**</span><span class="sxs-lookup"><span data-stu-id="75f59-118">**Offline Domain Join IDL Definitions**</span></span>](odj-idl.md)

[<span data-ttu-id="75f59-119">**\_cadeia de \_ caracteres Unicode ODJ**</span><span class="sxs-lookup"><span data-stu-id="75f59-119">**ODJ\_UNICODE\_STRING**</span></span>](odj-odj_unicode_string.md)

[<span data-ttu-id="75f59-120">**ODJ \_ Sid**</span><span class="sxs-lookup"><span data-stu-id="75f59-120">**ODJ\_SID**</span></span>](odj-odj_sid.md)
