---
description: Um grupo de métodos que é usado para manipular bloqueios.
ms.assetid: ba4cc37c-bd2f-446f-8b3d-bc2a2e2e4de4
title: Métodos CShareLockNH
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b16a979c5d1f111c92a64376c48f4c0ed1a165ca
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105756008"
---
# <a name="csharelocknh-methods"></a><span data-ttu-id="5c64c-103">Métodos CShareLockNH</span><span class="sxs-lookup"><span data-stu-id="5c64c-103">CShareLockNH Methods</span></span>

<span data-ttu-id="5c64c-104">Um grupo de métodos que é usado para manipular bloqueios.</span><span class="sxs-lookup"><span data-stu-id="5c64c-104">A group of methods that is used to manipulate locks.</span></span>

## <a name="methods"></a><span data-ttu-id="5c64c-105">Métodos</span><span class="sxs-lookup"><span data-stu-id="5c64c-105">Methods</span></span>

<span data-ttu-id="5c64c-106">Os métodos a seguir são exportados por Rwnh.dll.</span><span class="sxs-lookup"><span data-stu-id="5c64c-106">The following are methods exported by Rwnh.dll.</span></span>



| <span data-ttu-id="5c64c-107">Método</span><span class="sxs-lookup"><span data-stu-id="5c64c-107">Method</span></span>                                                                   | <span data-ttu-id="5c64c-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="5c64c-108">Description</span></span>                                                     |
|--------------------------------------------------------------------------|-----------------------------------------------------------------|
| [<span data-ttu-id="5c64c-109">**ExclusiveLock**</span><span class="sxs-lookup"><span data-stu-id="5c64c-109">**ExclusiveLock**</span></span>](csharelocknh--exclusivelock.md)                     | <span data-ttu-id="5c64c-110">Adquire um bloqueio de leitor/gravador.</span><span class="sxs-lookup"><span data-stu-id="5c64c-110">Acquires a reader/writer lock.</span></span>                                  |
| [<span data-ttu-id="5c64c-111">**ExclusiveToPartial**</span><span class="sxs-lookup"><span data-stu-id="5c64c-111">**ExclusiveToPartial**</span></span>](csharelocknh--exclusivetopartial.md)           | <span data-ttu-id="5c64c-112">Altera o estado.</span><span class="sxs-lookup"><span data-stu-id="5c64c-112">Changes the state.</span></span>                                              |
| [<span data-ttu-id="5c64c-113">**ExclusiveUnlock**</span><span class="sxs-lookup"><span data-stu-id="5c64c-113">**ExclusiveUnlock**</span></span>](csharelocknh--exclusiveunlock.md)                 | <span data-ttu-id="5c64c-114">Libera um bloqueio.</span><span class="sxs-lookup"><span data-stu-id="5c64c-114">Releases a lock.</span></span>                                                |
| [<span data-ttu-id="5c64c-115">**FirstPartialToExclusive**</span><span class="sxs-lookup"><span data-stu-id="5c64c-115">**FirstPartialToExclusive**</span></span>](csharelocknh--firstpartialtoexclusive.md) | <span data-ttu-id="5c64c-116">Usado na conversão de um bloqueio parcial para um bloqueio exclusivo.</span><span class="sxs-lookup"><span data-stu-id="5c64c-116">Used in converting a partial lock to an exclusive lock.</span></span>         |
| [<span data-ttu-id="5c64c-117">**PartialLock**</span><span class="sxs-lookup"><span data-stu-id="5c64c-117">**PartialLock**</span></span>](csharelocknh--partiallock.md)                         | <span data-ttu-id="5c64c-118">Impede que mais de um thread conclua a aquisição de um bloqueio.</span><span class="sxs-lookup"><span data-stu-id="5c64c-118">Prevents more than one thread from completing acquiring a lock.</span></span> |
| [<span data-ttu-id="5c64c-119">**PartialUnlock**</span><span class="sxs-lookup"><span data-stu-id="5c64c-119">**PartialUnlock**</span></span>](csharelocknh--partialunlock.md)                     | <span data-ttu-id="5c64c-120">Libera um bloqueio parcial.</span><span class="sxs-lookup"><span data-stu-id="5c64c-120">Releases a partial lock.</span></span>                                        |
| [<span data-ttu-id="5c64c-121">**ShareLock**</span><span class="sxs-lookup"><span data-stu-id="5c64c-121">**ShareLock**</span></span>](csharelocknh--sharelock.md)                             | <span data-ttu-id="5c64c-122">Obtém um bloqueio para o modo compartilhado.</span><span class="sxs-lookup"><span data-stu-id="5c64c-122">Obtains a lock for shared mode.</span></span>                                 |
| [<span data-ttu-id="5c64c-123">**ShareUnlock**</span><span class="sxs-lookup"><span data-stu-id="5c64c-123">**ShareUnlock**</span></span>](csharelocknh--shareunlock.md)                         | <span data-ttu-id="5c64c-124">Libera um bloqueio do modo compartilhado.</span><span class="sxs-lookup"><span data-stu-id="5c64c-124">Releases a lock from shared mode.</span></span>                               |
| [<span data-ttu-id="5c64c-125">**SharedToPartial**</span><span class="sxs-lookup"><span data-stu-id="5c64c-125">**SharedToPartial**</span></span>](csharelocknh--sharedtopartial.md)                 | <span data-ttu-id="5c64c-126">Obtém um bloqueio parcial.</span><span class="sxs-lookup"><span data-stu-id="5c64c-126">Obtains a partial lock.</span></span>                                         |
| [<span data-ttu-id="5c64c-127">**TryExclusiveLock**</span><span class="sxs-lookup"><span data-stu-id="5c64c-127">**TryExclusiveLock**</span></span>](csharelocknh--tryexclusivelock.md)               | <span data-ttu-id="5c64c-128">Obtém um bloqueio exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="5c64c-128">Obtains a lock exclusively.</span></span>                                     |



 

 

 



