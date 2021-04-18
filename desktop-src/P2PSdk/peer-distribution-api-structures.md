---
description: O serviço de distribuição de pares da Microsoft dá suporte às seguintes estruturas.
ms.assetid: 26badfe6-3a5a-4c2e-9ef1-534c2e8573d0
title: Estruturas de API de distribuição de pares
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcc9fbf86c242406aa86b7dd30497ba4c5085488
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105750456"
---
# <a name="peer-distribution-api-structures"></a><span data-ttu-id="18d42-103">Estruturas de API de distribuição de pares</span><span class="sxs-lookup"><span data-stu-id="18d42-103">Peer Distribution API Structures</span></span>

<span data-ttu-id="18d42-104">O serviço de distribuição de pares da Microsoft dá suporte às seguintes estruturas.</span><span class="sxs-lookup"><span data-stu-id="18d42-104">The Microsoft Peer Distribution service supports the following structures.</span></span>



| <span data-ttu-id="18d42-105">Estrutura</span><span class="sxs-lookup"><span data-stu-id="18d42-105">Structure</span></span>                                                              | <span data-ttu-id="18d42-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="18d42-106">Description</span></span>                                                                                                                                                                                                                                                                              |
|------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="18d42-107">**\_ \_ informações básicas do cliente do PEERDIST \_**</span><span class="sxs-lookup"><span data-stu-id="18d42-107">**PEERDIST\_CLIENT\_BASIC\_INFO**</span></span>](/windows/desktop/api/peerdist/ns-peerdist-peerdist_client_basic_info)    | <span data-ttu-id="18d42-108">Indica se há ou não muitos clientes baixando simultaneamente o mesmo conteúdo.</span><span class="sxs-lookup"><span data-stu-id="18d42-108">Indicates whether or not there are many clients simultaneously downloading the same content.</span></span>                                                                                                                                                                                             |
| [<span data-ttu-id="18d42-109">**\_marca de conteúdo PEERDIST \_**</span><span class="sxs-lookup"><span data-stu-id="18d42-109">**PEERDIST\_CONTENT\_TAG**</span></span>](/windows/win32/api/peerdist/ns-peerdist-peerdist_content_tag)                 | <span data-ttu-id="18d42-110">Contém uma marca fornecida pelo cliente, que é um valor de entrada para [**PeerDistClientOpenContent**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientopencontent).</span><span class="sxs-lookup"><span data-stu-id="18d42-110">Contains a client supplied tag which is an input value for [**PeerDistClientOpenContent**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientopencontent).</span></span> <span data-ttu-id="18d42-111">A marca está associada ao segmento de conteúdo e é usada em APIs de gerenciamento de conteúdo, como [**PeerDistClientFlushContent**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientflushcontent).</span><span class="sxs-lookup"><span data-stu-id="18d42-111">The tag is associated with the content segment and is used in content management APIs, like [**PeerDistClientFlushContent**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientflushcontent).</span></span> |
| [<span data-ttu-id="18d42-112">**\_Opções de publicação PEERDIST \_**</span><span class="sxs-lookup"><span data-stu-id="18d42-112">**PEERDIST\_PUBLICATION\_OPTIONS**</span></span>](/windows/desktop/api/peerdist/ns-peerdist-peerdist_publication_options) | <span data-ttu-id="18d42-113">Contém opções de publicação, incluindo as informações de versão da API e possíveis sinalizadores de opção.</span><span class="sxs-lookup"><span data-stu-id="18d42-113">Contains publication options, including the API version information and possible option flags.</span></span>                                                                                                                                                                                           |
| [<span data-ttu-id="18d42-114">**opções de recuperação de pares \_ \_**</span><span class="sxs-lookup"><span data-stu-id="18d42-114">**PEER\_RETRIEVAL\_OPTIONS**</span></span>](/windows/desktop/api/peerdist/ns-peerdist-peerdist_retrieval_options)         | <span data-ttu-id="18d42-115">Contém a versão das informações de conteúdo a serem recuperadas.</span><span class="sxs-lookup"><span data-stu-id="18d42-115">Contains version of the content information to retrieve.</span></span>                                                                                                                                                                                                                                 |
| [<span data-ttu-id="18d42-116">**\_informações de status do PEERDIST \_**</span><span class="sxs-lookup"><span data-stu-id="18d42-116">**PEERDIST\_STATUS\_INFO**</span></span>](/windows/desktop/api/peerdist/ns-peerdist-peerdist_status_info)                 | <span data-ttu-id="18d42-117">Contém informações sobre o status atual e os recursos do serviço do BranchCache no computador local.</span><span class="sxs-lookup"><span data-stu-id="18d42-117">Contains information about the current status and capabilities of the BranchCache service on the local computer.</span></span>                                                                                                                                                                         |



 

## <a name="related-topics"></a><span data-ttu-id="18d42-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="18d42-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="18d42-119">Referência da API de distribuição de pares</span><span class="sxs-lookup"><span data-stu-id="18d42-119">Peer Distribution API Reference</span></span>](peer-distribution-api-reference.md)
</dt> </dl>

 

 



