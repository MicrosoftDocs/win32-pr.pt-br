---
title: Funções do utilitário NAP
description: As funções do utilitário a seguir dão suporte à API NAP.
ms.assetid: 0819067c-cca5-4140-8b4d-f3b996826152
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 260c423909011c81f52ea89ce8d3137b35c55167
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635668"
---
# <a name="nap-utility-functions"></a><span data-ttu-id="69355-103">Funções do utilitário NAP</span><span class="sxs-lookup"><span data-stu-id="69355-103">NAP Utility Functions</span></span>

> [!Note]  
> <span data-ttu-id="69355-104">A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10</span><span class="sxs-lookup"><span data-stu-id="69355-104">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="69355-105">As funções do utilitário a seguir dão suporte à API NAP.</span><span class="sxs-lookup"><span data-stu-id="69355-105">The following utility functions support the NAP API.</span></span>

<span data-ttu-id="69355-106">Todas as interfaces COM com suporte do sistema NAP usam regras de gerenciamento de memória COM padrão e o alocador de memória COM (CoTaskMemAlloc e CoTaskMemFree).</span><span class="sxs-lookup"><span data-stu-id="69355-106">All the COM interfaces supported by the NAP system use standard COM memory management rules and the COM memory allocator (CoTaskMemAlloc and CoTaskMemFree).</span></span>

-   <span data-ttu-id="69355-107">EM parâmetros — alocados e liberados pelo chamador.</span><span class="sxs-lookup"><span data-stu-id="69355-107">IN parameters — allocated and freed by caller.</span></span>
-   <span data-ttu-id="69355-108">Parâmetros de saída — alocados pelo receptor, liberados pelo chamador usando CoTaskMem \* ()</span><span class="sxs-lookup"><span data-stu-id="69355-108">OUT parameters — allocated by callee, freed by caller using CoTaskMem\*()</span></span>
-   <span data-ttu-id="69355-109">Parâmetros de entrada/saída — alocados pelo chamador, liberados e realocados pelo receptor, por fim liberados pelo chamador, usando CoTaskMem \* ()</span><span class="sxs-lookup"><span data-stu-id="69355-109">IN/OUT parameters — allocated by caller, freed and reallocated by callee, ultimately freed by caller, using CoTaskMem\*()</span></span>

<span data-ttu-id="69355-110">Nas funções FreeXxx (), todos os ponteiros inseridos também serão liberados.</span><span class="sxs-lookup"><span data-stu-id="69355-110">In the FreeXxx() functions, all embedded pointers will also be freed.</span></span>

-   [<span data-ttu-id="69355-111">**AllocConnections**</span><span class="sxs-lookup"><span data-stu-id="69355-111">**AllocConnections**</span></span>](allocconnections-func.md)
-   [<span data-ttu-id="69355-112">**AllocCountedString**</span><span class="sxs-lookup"><span data-stu-id="69355-112">**AllocCountedString**</span></span>](alloccountedstring-func.md)
-   [<span data-ttu-id="69355-113">**AllocFixupInfo**</span><span class="sxs-lookup"><span data-stu-id="69355-113">**AllocFixupInfo**</span></span>](allocfixupinfo-func.md)
-   [<span data-ttu-id="69355-114">**FreeConnections**</span><span class="sxs-lookup"><span data-stu-id="69355-114">**FreeConnections**</span></span>](freeconnections-func.md)
-   [<span data-ttu-id="69355-115">**FreeCountedString**</span><span class="sxs-lookup"><span data-stu-id="69355-115">**FreeCountedString**</span></span>](freecountedstring-func.md)
-   [<span data-ttu-id="69355-116">**FreeFixupInfo**</span><span class="sxs-lookup"><span data-stu-id="69355-116">**FreeFixupInfo**</span></span>](freefixupinfo-func.md)
-   [<span data-ttu-id="69355-117">**FreeIsolationInfo**</span><span class="sxs-lookup"><span data-stu-id="69355-117">**FreeIsolationInfo**</span></span>](freeisolationinfo-func.md)
-   [<span data-ttu-id="69355-118">**FreeIsolationInfoEx**</span><span class="sxs-lookup"><span data-stu-id="69355-118">**FreeIsolationInfoEx**</span></span>](freeisolationinfoex.md)
-   [<span data-ttu-id="69355-119">**FreeNapComponentRegistrationInfoArray**</span><span class="sxs-lookup"><span data-stu-id="69355-119">**FreeNapComponentRegistrationInfoArray**</span></span>](freenapcomponentregistrationinfoarray-func.md)
-   [<span data-ttu-id="69355-120">**FreeNetworkSoH**</span><span class="sxs-lookup"><span data-stu-id="69355-120">**FreeNetworkSoH**</span></span>](freenetworksoh-func.md)
-   [<span data-ttu-id="69355-121">**FreePrivateData**</span><span class="sxs-lookup"><span data-stu-id="69355-121">**FreePrivateData**</span></span>](freeprivatedata-func.md)
-   [<span data-ttu-id="69355-122">**FreeSoH**</span><span class="sxs-lookup"><span data-stu-id="69355-122">**FreeSoH**</span></span>](freesoh-func.md)
-   [<span data-ttu-id="69355-123">**FreeSoHAttributeValue**</span><span class="sxs-lookup"><span data-stu-id="69355-123">**FreeSoHAttributeValue**</span></span>](freesohattributevalue-func.md)
-   [<span data-ttu-id="69355-124">**FreeSystemHealthAgentState**</span><span class="sxs-lookup"><span data-stu-id="69355-124">**FreeSystemHealthAgentState**</span></span>](freesystemhealthagentstate-func.md)
-   [<span data-ttu-id="69355-125">**InitializeNapAgentNotifier**</span><span class="sxs-lookup"><span data-stu-id="69355-125">**InitializeNapAgentNotifier**</span></span>](initializenapagentnotifier.md)
-   [<span data-ttu-id="69355-126">**UninitializeNapAgentNotifier**</span><span class="sxs-lookup"><span data-stu-id="69355-126">**UninitializeNapAgentNotifier**</span></span>](uninitializenapagentnotifier.md)

 

 




