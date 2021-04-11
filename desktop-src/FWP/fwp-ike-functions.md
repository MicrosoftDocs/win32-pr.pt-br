---
title: Funções IKE/AuthIP
description: (WFP) funções usadas para interagir com módulos de criação de chaves \ 8212; protocolo IKE (IKE), protocolo IKE v2 (IKEv2) e protocolo Authenticated IP (AuthIP).
ms.assetid: df36b6cc-a304-4426-8f16-1bf92fd721e1
keywords:
- Funções protocolo IKE API da plataforma de filtragem do Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6cce5d3e2393bb1a83ebf816375f537318bb4b1f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292446"
---
# <a name="ikeauthip-functions"></a><span data-ttu-id="8f805-104">Funções IKE/AuthIP</span><span class="sxs-lookup"><span data-stu-id="8f805-104">IKE/AuthIP Functions</span></span>

<span data-ttu-id="8f805-105">As funções da WFP (plataforma de filtragem do Windows) usadas para interagir com módulos de chaveamento, protocolo IKE (IKE), protocolo IKE v2 (IKEv2) e protocolo Authenticated IP (AuthIP) — são as seguintes.</span><span class="sxs-lookup"><span data-stu-id="8f805-105">The Windows Filtering Platform (WFP) functions used to interact with keying modules—Internet Key Exchange (IKE), Internet Key Exchange v2 (IKEv2), and Authenticated Internet Protocol (AuthIP)—are as follows.</span></span>

-   <span data-ttu-id="8f805-106">IkeextGetStatistics:</span><span class="sxs-lookup"><span data-stu-id="8f805-106">IkeextGetStatistics:</span></span>
    -   <span data-ttu-id="8f805-107">[**IkeextGetStatistics0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextgetstatistics0) (Windows Vista)</span><span class="sxs-lookup"><span data-stu-id="8f805-107">[**IkeextGetStatistics0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextgetstatistics0) (Windows Vista)</span></span>
    -   <span data-ttu-id="8f805-108">[**IkeextGetStatistics1**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextgetstatistics1) (Windows 7 e posterior)</span><span class="sxs-lookup"><span data-stu-id="8f805-108">[**IkeextGetStatistics1**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextgetstatistics1) (Windows 7 and later)</span></span>
-   [<span data-ttu-id="8f805-109">**IkeextSaCreateEnumHandle0**</span><span class="sxs-lookup"><span data-stu-id="8f805-109">**IkeextSaCreateEnumHandle0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsacreateenumhandle0)
-   [<span data-ttu-id="8f805-110">**IkeextSaDbGetSecurityInfo0**</span><span class="sxs-lookup"><span data-stu-id="8f805-110">**IkeextSaDbGetSecurityInfo0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsadbgetsecurityinfo0)
-   [<span data-ttu-id="8f805-111">**IkeextSaDbSetSecurityInfo0**</span><span class="sxs-lookup"><span data-stu-id="8f805-111">**IkeextSaDbSetSecurityInfo0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsadbsetsecurityinfo0)
-   [<span data-ttu-id="8f805-112">**IkeextSaDeleteById0**</span><span class="sxs-lookup"><span data-stu-id="8f805-112">**IkeextSaDeleteById0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsadeletebyid0)
-   [<span data-ttu-id="8f805-113">**IkeextSaDestroyEnumHandle0**</span><span class="sxs-lookup"><span data-stu-id="8f805-113">**IkeextSaDestroyEnumHandle0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsadestroyenumhandle0)
-   <span data-ttu-id="8f805-114">IkeextSaEnum:</span><span class="sxs-lookup"><span data-stu-id="8f805-114">IkeextSaEnum:</span></span>
    -   <span data-ttu-id="8f805-115">[**IkeextSaEnum0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsaenum0) (Windows Vista)</span><span class="sxs-lookup"><span data-stu-id="8f805-115">[**IkeextSaEnum0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsaenum0) (Windows Vista)</span></span>
    -   <span data-ttu-id="8f805-116">[**IkeextSaEnum1**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsaenum1) (Windows 7)</span><span class="sxs-lookup"><span data-stu-id="8f805-116">[**IkeextSaEnum1**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsaenum1) (Windows 7)</span></span>
    -   <span data-ttu-id="8f805-117">[**IkeextSaEnum2**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsaenum2) (Windows 8)</span><span class="sxs-lookup"><span data-stu-id="8f805-117">[**IkeextSaEnum2**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsaenum2) (Windows 8)</span></span>
-   <span data-ttu-id="8f805-118">IkeextSaGetById:</span><span class="sxs-lookup"><span data-stu-id="8f805-118">IkeextSaGetById:</span></span>
    -   <span data-ttu-id="8f805-119">[**IkeextSaGetById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsagetbyid0) (Windows Vista)</span><span class="sxs-lookup"><span data-stu-id="8f805-119">[**IkeextSaGetById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsagetbyid0) (Windows Vista)</span></span>
    -   <span data-ttu-id="8f805-120">[**IkeextSaGetById1**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsagetbyid1) (Windows 7)</span><span class="sxs-lookup"><span data-stu-id="8f805-120">[**IkeextSaGetById1**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsagetbyid1) (Windows 7)</span></span>
    -   <span data-ttu-id="8f805-121">[**IkeextSaGetById2**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsagetbyid2) (Windows 8)</span><span class="sxs-lookup"><span data-stu-id="8f805-121">[**IkeextSaGetById2**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsagetbyid2) (Windows 8)</span></span>

 

 




