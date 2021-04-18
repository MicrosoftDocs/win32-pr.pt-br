---
description: 'A API do provedor de namespace do PNRP usa as seguintes estruturas:'
ms.assetid: 697fb99a-259f-429c-8818-0d725255bc86
title: Estruturas PNRP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a78e2ee85f3673395ade31417c79c010354f16b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105756575"
---
# <a name="pnrp-structures"></a><span data-ttu-id="fc3e3-103">Estruturas PNRP</span><span class="sxs-lookup"><span data-stu-id="fc3e3-103">PNRP Structures</span></span>

<span data-ttu-id="fc3e3-104">A API do provedor de namespace do PNRP usa as seguintes estruturas:</span><span class="sxs-lookup"><span data-stu-id="fc3e3-104">The PNRP Namespace Provider API uses the following structures:</span></span>



| <span data-ttu-id="fc3e3-105">Estrutura</span><span class="sxs-lookup"><span data-stu-id="fc3e3-105">Structure</span></span>                                                             | <span data-ttu-id="fc3e3-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="fc3e3-106">Description</span></span>                                                                                                                                                         |
|-----------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fc3e3-107">**informações de ponto de \_ extremidade PNRP par \_ \_**</span><span class="sxs-lookup"><span data-stu-id="fc3e3-107">**PEER\_PNRP\_ENDPOINT\_INFO**</span></span>](/windows/desktop/api/P2P/ns-p2p-peer_pnrp_endpoint_info)         | <span data-ttu-id="fc3e3-108">Contém os endereços IP e os dados associados a um ponto de extremidade par.</span><span class="sxs-lookup"><span data-stu-id="fc3e3-108">Contains the IP addresses and data associated with a peer endpoint.</span></span>                                                                                                 |
| [<span data-ttu-id="fc3e3-109">**\_informações de \_ nuvem \_ PNRP par**</span><span class="sxs-lookup"><span data-stu-id="fc3e3-109">**PEER\_PNRP\_CLOUD\_INFO**</span></span>](/windows/desktop/api/P2P/ns-p2p-peer_pnrp_cloud_info)               | <span data-ttu-id="fc3e3-110">Contém informações sobre uma nuvem PNRP (Peer Name Resolution Protocol).</span><span class="sxs-lookup"><span data-stu-id="fc3e3-110">Contains information about a Peer Name Resolution Protocol (PNRP) cloud.</span></span>                                                                                            |
| [<span data-ttu-id="fc3e3-111">**\_informações de \_ registro de PNRP de pares \_**</span><span class="sxs-lookup"><span data-stu-id="fc3e3-111">**PEER\_PNRP\_REGISTRATION\_INFO**</span></span>](/windows/desktop/api/P2P/ns-p2p-peer_pnrp_registration_info) | <span data-ttu-id="fc3e3-112">Contém as informações fornecidas por uma identidade de par quando ele se registra em uma nuvem PNRP.</span><span class="sxs-lookup"><span data-stu-id="fc3e3-112">Contains the information provided by a peer identity when it registers with a PNRP cloud.</span></span>                                                                           |
| [<span data-ttu-id="fc3e3-113">PNRP e BLOB</span><span class="sxs-lookup"><span data-stu-id="fc3e3-113">PNRP and BLOB</span></span>](pnrp-and-blob.md)                                    | <span data-ttu-id="fc3e3-114">Passa dados para a estrutura [**WSAQUERYSET**](winsock-nsp-reference-links.md) durante chamadas para várias funções.</span><span class="sxs-lookup"><span data-stu-id="fc3e3-114">Passes data to the [**WSAQUERYSET**](winsock-nsp-reference-links.md) structure during calls to several functions.</span></span>                                                  |
| [<span data-ttu-id="fc3e3-115">PNRP e WSAQUERYSET</span><span class="sxs-lookup"><span data-stu-id="fc3e3-115">PNRP and WSAQUERYSET</span></span>](pnrp-and-wsaqueryset.md)                      | <span data-ttu-id="fc3e3-116">Facilita a resolução de nomes e a enumeração de nomes e nuvens.</span><span class="sxs-lookup"><span data-stu-id="fc3e3-116">Facilitates the resolving of names and the enumeration of names and clouds.</span></span>                                                                                         |
| [<span data-ttu-id="fc3e3-117">**\_ID da nuvem PNRP \_**</span><span class="sxs-lookup"><span data-stu-id="fc3e3-117">**PNRP\_CLOUD\_ID**</span></span>](/windows/desktop/api/Pnrpdef/ns-pnrpdef-pnrp_cloud_id)                              | <span data-ttu-id="fc3e3-118">Contém os valores que definem uma nuvem de rede.</span><span class="sxs-lookup"><span data-stu-id="fc3e3-118">Contains the values that define a network cloud.</span></span>                                                                                                                    |
| [<span data-ttu-id="fc3e3-119">**PNRPCLOUDINFO**</span><span class="sxs-lookup"><span data-stu-id="fc3e3-119">**PNRPCLOUDINFO**</span></span>](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpcloudinfo)                                | <span data-ttu-id="fc3e3-120">Apontado pelo membro **lpBlob** da estrutura [**WSAQUERYSET**](winsock-nsp-reference-links.md) .</span><span class="sxs-lookup"><span data-stu-id="fc3e3-120">Pointed to by the **lpBlob** member of the [**WSAQUERYSET**](winsock-nsp-reference-links.md) structure.</span></span>                                                            |
| [<span data-ttu-id="fc3e3-121">**PNRPINFO \_ v1**</span><span class="sxs-lookup"><span data-stu-id="fc3e3-121">**PNRPINFO\_V1**</span></span>](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1)                                      | <span data-ttu-id="fc3e3-122">Apontado pelo membro **lpBlob** da estrutura [**WSAQUERYSET**](winsock-nsp-reference-links.md)</span><span class="sxs-lookup"><span data-stu-id="fc3e3-122">Pointed to by the **lpBlob** member of the [**WSAQUERYSET**](winsock-nsp-reference-links.md) structure</span></span>                                                             |
| <span data-ttu-id="fc3e3-123">[**PNRPINFO \_ v2**](/previous-versions/windows/desktop/legacy/aa371671(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="fc3e3-123">[**PNRPINFO\_V2**](/previous-versions/windows/desktop/legacy/aa371671(v=vs.85))</span></span>                                   | <span data-ttu-id="fc3e3-124">Apontado pelo membro **lpBlob** da estrutura [**WSAQUERYSET**](winsock-nsp-reference-links.md) e fornece suporte para dados opacos específicos do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="fc3e3-124">Pointed to by the **lpBlob** member of the [**WSAQUERYSET**](winsock-nsp-reference-links.md) structure, and provides support for application-specific opaque data.</span></span> |



 

 

 
