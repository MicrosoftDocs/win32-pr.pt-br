---
description: A lista a seguir fornece descrições concisas de cada estrutura SPI do Winsock. Para obter informações adicionais sobre qualquer estrutura de SPI do Winsock, clique no nome da estrutura.
ms.assetid: 0e198e36-c025-4745-a841-3a23ea3d40aa
title: Estruturas SPI do Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da37b5a7ea166af3e3c335f2d520034509e57391
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164863"
---
# <a name="winsock-spi-structures"></a><span data-ttu-id="4710b-104">Estruturas SPI do Winsock</span><span class="sxs-lookup"><span data-stu-id="4710b-104">Winsock SPI Structures</span></span>

<span data-ttu-id="4710b-105">A lista a seguir fornece descrições concisas de cada estrutura SPI do Winsock.</span><span class="sxs-lookup"><span data-stu-id="4710b-105">The following list provides concise descriptions of each Winsock SPI structure.</span></span> <span data-ttu-id="4710b-106">Para obter informações adicionais sobre qualquer estrutura de SPI do Winsock, clique no nome da estrutura.</span><span class="sxs-lookup"><span data-stu-id="4710b-106">For additional information on any Winsock SPI structure, click the structure name.</span></span>



| <span data-ttu-id="4710b-107">Estrutura de SPI do Winsock</span><span class="sxs-lookup"><span data-stu-id="4710b-107">Winsock SPI structure</span></span>                                         | <span data-ttu-id="4710b-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="4710b-108">Description</span></span>                                                                                                   |
|---------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4710b-109">**\_rotina NSP**</span><span class="sxs-lookup"><span data-stu-id="4710b-109">**NSP\_ROUTINE**</span></span>](/windows/desktop/api/Ws2spi/ns-ws2spi-nsp_routine)                           | <span data-ttu-id="4710b-110">Contém informações sobre as funções implementadas por um provedor de provedor de serviços de namespace versão 1 (NSPv1).</span><span class="sxs-lookup"><span data-stu-id="4710b-110">Contains information on the functions implemented by a namespace service provider version 1 (NSPv1) provider.</span></span> |
| [<span data-ttu-id="4710b-111">**\_Rotina NSPV2**</span><span class="sxs-lookup"><span data-stu-id="4710b-111">**NSPV2\_ROUTINE**</span></span>](/windows/desktop/api/Ws2spi/ns-ws2spi-nspv2_routine)                       | <span data-ttu-id="4710b-112">Contém informações sobre as funções implementadas por um provedor de provedor de serviços de namespace versão 2 (NSPv2).</span><span class="sxs-lookup"><span data-stu-id="4710b-112">Contains information on the functions implemented by a namespace service provider version 2 (NSPv2) provider.</span></span> |
| [<span data-ttu-id="4710b-113">**WSATHREADID**</span><span class="sxs-lookup"><span data-stu-id="4710b-113">**WSATHREADID**</span></span>](/windows/desktop/api/Ws2spi/ns-ws2spi-wsathreadid)                          | <span data-ttu-id="4710b-114">Permite que um provedor identifique um thread no qual as chamadas de procedimento assíncrono (APCs) podem ser enfileiradas.</span><span class="sxs-lookup"><span data-stu-id="4710b-114">Enables a provider to identify a thread on which asynchronous procedure calls (APCs) can be queued.</span></span>           |
| [<span data-ttu-id="4710b-115">**\_informações de \_ auditoria do provedor de WSC \_**</span><span class="sxs-lookup"><span data-stu-id="4710b-115">**WSC\_PROVIDER\_AUDIT\_INFO**</span></span>](/windows/desktop/api/Ws2spi/ns-ws2spi-wsc_provider_audit_info) | <span data-ttu-id="4710b-116">Contém informações de auditoria para uma entrada de LSP (provedor de serviço em camadas).</span><span class="sxs-lookup"><span data-stu-id="4710b-116">Contains audit information for a layered service provider (LSP) entry.</span></span>                                        |
| [<span data-ttu-id="4710b-117">**WSPDATA**</span><span class="sxs-lookup"><span data-stu-id="4710b-117">**WSPDATA**</span></span>](/windows/desktop/api/Ws2spi/ns-ws2spi-wspdata)                                  | <span data-ttu-id="4710b-118">Contém informações do provedor de serviços.</span><span class="sxs-lookup"><span data-stu-id="4710b-118">Contains service provider information.</span></span>                                                                        |
| [<span data-ttu-id="4710b-119">**\_tabela WSPPROC**</span><span class="sxs-lookup"><span data-stu-id="4710b-119">**WSPPROC\_TABLE**</span></span>](/windows/desktop/api/Ws2spi/ns-ws2spi-wspproc_table)                       | <span data-ttu-id="4710b-120">Contém uma tabela de ponteiros para funções de provedor de serviço.</span><span class="sxs-lookup"><span data-stu-id="4710b-120">Contains a table of pointers to service provider functions.</span></span>                                                   |
| [<span data-ttu-id="4710b-121">**WSPUPCALLTABLE**</span><span class="sxs-lookup"><span data-stu-id="4710b-121">**WSPUPCALLTABLE**</span></span>](/windows/desktop/api/Ws2spi/ns-ws2spi-wspupcalltable)                      | <span data-ttu-id="4710b-122">Contém uma tabela de ponteiros para funções de chamada de provedor de serviço.</span><span class="sxs-lookup"><span data-stu-id="4710b-122">Contains a table of pointers to service provider upcall functions.</span></span>                                            |



 

 

 



