---
title: ODJ_WIN7BLOB
description: Definição de IDL de ODJ_WIN7BLOB
ms.assetid: 5802e00c-b943-45d8-8298-5c2b4b996b85
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 2083648636bd58c64314ba22852839f89ed4461d
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/14/2020
ms.locfileid: "104294583"
---
# <a name="odj_win7blob-structure"></a><span data-ttu-id="51382-103">Estrutura de ODJ_WIN7BLOB</span><span class="sxs-lookup"><span data-stu-id="51382-103">ODJ_WIN7BLOB structure</span></span>

<span data-ttu-id="51382-104">Contém as informações básicas necessárias para ingressar um cliente em um domínio.</span><span class="sxs-lookup"><span data-stu-id="51382-104">Contains the basic information required to join a client to a domain.</span></span>

## <a name="syntax"></a><span data-ttu-id="51382-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="51382-105">Syntax</span></span>

```C++
typedef struct _ODJ_WIN7BLOB
{
    [string] wchar_t *lpDomain;
    [string] wchar_t *lpMachineName;
    [string] wchar_t *lpMachinePassword;
    ODJ_POLICY_DNS_DOMAIN_INFO  DnsDomainInfo;
    DOMAIN_CONTROLLER_INFOW DcInfo;
    DWORD Options;
} ODJ_WIN7BLOB;
```

## <a name="members"></a><span data-ttu-id="51382-106">Membros</span><span class="sxs-lookup"><span data-stu-id="51382-106">Members</span></span>

### <a name="lpdomain"></a><span data-ttu-id="51382-107">lpDomain</span><span class="sxs-lookup"><span data-stu-id="51382-107">lpDomain</span></span>

<span data-ttu-id="51382-108">Deve ser definido como o nome de domínio.</span><span class="sxs-lookup"><span data-stu-id="51382-108">Must be set to the domain name.</span></span>

### <a name="lpmachinename"></a><span data-ttu-id="51382-109">lpMachineName</span><span class="sxs-lookup"><span data-stu-id="51382-109">lpMachineName</span></span>

<span data-ttu-id="51382-110">Deve ser definido como o nome do computador.</span><span class="sxs-lookup"><span data-stu-id="51382-110">Must be set to the machine name.</span></span>

### <a name="lpmachinepassword"></a><span data-ttu-id="51382-111">lpMachinePassword</span><span class="sxs-lookup"><span data-stu-id="51382-111">lpMachinePassword</span></span>

<span data-ttu-id="51382-112">Deve ser definido como uma senha de texto não criptografado para a conta de computador identificada por lpMachineName</span><span class="sxs-lookup"><span data-stu-id="51382-112">Must be set to a cleartext password for the machine account identified by lpMachineName</span></span>

### <a name="dnsdomaininfo"></a><span data-ttu-id="51382-113">DnsDomainInfo</span><span class="sxs-lookup"><span data-stu-id="51382-113">DnsDomainInfo</span></span>

<span data-ttu-id="51382-114">Contém informações sobre o domínio que está sendo ingressado.</span><span class="sxs-lookup"><span data-stu-id="51382-114">Contains information about the domain being joined.</span></span>

### <a name="dcinfo"></a><span data-ttu-id="51382-115">DcInfo</span><span class="sxs-lookup"><span data-stu-id="51382-115">DcInfo</span></span>

<span data-ttu-id="51382-116">Contém informações de nomenclatura e endereçamento sobre o controlador de domínio que foi usado para criar a conta de computador Active Directory.</span><span class="sxs-lookup"><span data-stu-id="51382-116">Contains naming and addressing information about the domain controller that was used to create the machine account Active Directory.</span></span>

### <a name="options"></a><span data-ttu-id="51382-117">Opções</span><span class="sxs-lookup"><span data-stu-id="51382-117">Options</span></span>

<span data-ttu-id="51382-118">Deve ser definido como zero.</span><span class="sxs-lookup"><span data-stu-id="51382-118">Must be set to zero.</span></span>

## <a name="see-also"></a><span data-ttu-id="51382-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="51382-119">See also</span></span>

[<span data-ttu-id="51382-120">**Definições de IDL de ingresso no domínio offline**</span><span class="sxs-lookup"><span data-stu-id="51382-120">**Offline Domain Join IDL Definitions**</span></span>](odj-idl.md)

[<span data-ttu-id="51382-121">**\_informações de \_ \_ domínio DNS da política \_ ODJ**</span><span class="sxs-lookup"><span data-stu-id="51382-121">**ODJ\_POLICY\_DNS\_DOMAIN\_INFO**</span></span>](odj-odj_policy_dns_domain_info.md)

[<span data-ttu-id="51382-122">**DOMAIN_CONTROLLER_INFOW**</span><span class="sxs-lookup"><span data-stu-id="51382-122">**DOMAIN_CONTROLLER_INFOW**</span></span>](/windows/win32/api/dsgetdc/ns-dsgetdc-domain_controller_infow)



