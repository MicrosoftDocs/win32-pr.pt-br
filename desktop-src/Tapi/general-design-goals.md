---
description: A lista a seguir contém as metas de design TAPI MSP.
ms.assetid: 286b96c1-047b-4cb9-a189-af2818cfec58
title: Metas gerais de design
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 052bbf607e71986678acca29d17d587bfa5bccf5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105761967"
---
# <a name="general-design-goals"></a><span data-ttu-id="e01f2-103">Metas gerais de design</span><span class="sxs-lookup"><span data-stu-id="e01f2-103">General Design Goals</span></span>

<span data-ttu-id="e01f2-104">A lista a seguir contém as metas de design TAPI MSP.</span><span class="sxs-lookup"><span data-stu-id="e01f2-104">The following list contains the TAPI MSP design goals.</span></span>

-   <span data-ttu-id="e01f2-105">As classes base foram mantidas simples, com membros e métodos introduzidos apenas quando absolutamente necessário.</span><span class="sxs-lookup"><span data-stu-id="e01f2-105">Base classes have been kept simple, with members and methods introduced only when absolutely necessary.</span></span>
-   <span data-ttu-id="e01f2-106">Herança simples.</span><span class="sxs-lookup"><span data-stu-id="e01f2-106">Simple inheritance.</span></span> <span data-ttu-id="e01f2-107">Não há várias heranças entre classes, embora várias heranças sejam usadas para as interfaces.</span><span class="sxs-lookup"><span data-stu-id="e01f2-107">No multiple inheritance among classes, although multiple inheritance is used for the interfaces.</span></span>
-   <span data-ttu-id="e01f2-108">O bloqueio ocorre apenas em uma direção para evitar o deadlock.</span><span class="sxs-lookup"><span data-stu-id="e01f2-108">Locking happens only in one direction to prevent deadlock.</span></span> <span data-ttu-id="e01f2-109">Os métodos no objeto de chamada que exigem o bloqueio na chamada podem chamar métodos no fluxo que exigem o bloqueio no fluxo.</span><span class="sxs-lookup"><span data-stu-id="e01f2-109">Methods on the call object that require the lock on the call might call methods on the stream that require the lock on the stream.</span></span> <span data-ttu-id="e01f2-110">No entanto, os métodos no fluxo que exigem o bloqueio no fluxo nunca chamarão um método na chamada que exige um bloqueio na chamada.</span><span class="sxs-lookup"><span data-stu-id="e01f2-110">However, methods on the stream that require the lock on the stream will never call a method on the call that requires a lock on the call.</span></span>
-   <span data-ttu-id="e01f2-111">RefCounts são usados para proteger o acesso.</span><span class="sxs-lookup"><span data-stu-id="e01f2-111">Refcounts are used to protect access.</span></span> <span data-ttu-id="e01f2-112">Todos os retornos de chamada postados no pool de threads contêm refCounts.</span><span class="sxs-lookup"><span data-stu-id="e01f2-112">All callbacks posted to the thread pool hold refcounts.</span></span> <span data-ttu-id="e01f2-113">O Refcount é cancelado quando a espera é cancelada.</span><span class="sxs-lookup"><span data-stu-id="e01f2-113">The refcount is canceled when the wait is canceled.</span></span> <span data-ttu-id="e01f2-114">O objeto de endereço tem refCounts nos terminais.</span><span class="sxs-lookup"><span data-stu-id="e01f2-114">The Address object has refcounts on Terminals.</span></span> <span data-ttu-id="e01f2-115">Os objetos de chamada têm refCounts no endereço e em fluxos.</span><span class="sxs-lookup"><span data-stu-id="e01f2-115">Call objects have refcounts on the Address and on Streams.</span></span> <span data-ttu-id="e01f2-116">Os objetos de fluxo têm refCounts em chamadas e terminais.</span><span class="sxs-lookup"><span data-stu-id="e01f2-116">Stream objects have refcounts on Calls and Terminals.</span></span> <span data-ttu-id="e01f2-117">Os terminais têm refCounts em fluxos.</span><span class="sxs-lookup"><span data-stu-id="e01f2-117">The Terminals have refcounts on Streams.</span></span> <span data-ttu-id="e01f2-118">A quebra de refCounts circular quando o método de desligamento nos objetos address e Call é chamado.</span><span class="sxs-lookup"><span data-stu-id="e01f2-118">The circular refcounts break when the shutdown method on the Address and Call objects is called.</span></span>

 

 



